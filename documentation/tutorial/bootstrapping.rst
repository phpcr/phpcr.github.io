Bootstrapping
=============

You will need to make sure your php classes are available. Usually this means activating an autoloader. For a standalone project, just use the file generated by composer at vendor/.composer/autoload.php
PHPCR and Jackalope follow the PSR-0 standard. If you want your own autoloading, use a PSR-0 compatible autoloader and configure it to find the code folder.

Once you have autoloading set up, bootstrap jackalope-jackrabbit like this:

.. code-block:: php

    <?php
    require("vendor/autoload.php");

    // factory (the *only* implementation specific part)
    $factoryclass = '\Jackalope\RepositoryFactoryJackrabbit';
    // the parameters would typically live in a configuration file
    // see your implementation for required and optional parameters
    $parameters = array('jackalope.jackrabbit_uri' => 'http://localhost:8080/server');

    // end of implementation specific configuration
    // from here on, the whole code does not need to be changed when using different implementations

    $factory = new $factoryclass();
    $repository = $factory->getRepository($parameters);
    if (null === $repository) {
        var_dump($parameters);
        die('There where missing parameters, the factory could not create a repository');
    }

    // the login parameters would typically live in a configuration file

    $workspacename = 'default';
    $user = 'admin';
    $pass = 'admin';

    // create credentials and log in to get a session
    $credentials = new \PHPCR\SimpleCredentials($user, $pass);
    try {
        $session = $repository->login($credentials, $workspacename);
    } catch(\PHPCR\LoginException $e) {
        die('Invalid credentials: '.$e->getMessage());
    } catch(\PHPCR\NoSuchWorkspaceException $e) {
        die("No workspace $workspacename: ".$e->getMessage());
    }

    // if we get here, we have a session object that can be used to read and write the repository
