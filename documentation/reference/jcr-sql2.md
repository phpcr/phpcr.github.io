---
layout: default
title: JCR-SQL2 Reference
---
JCR-SQL2 is a query language similar to SQL which is used by JCR and thus also PHPCR.

Some things to note:

- Unlike most other SQL dialects, JCR-SQL2 only supports SELECT statements.
- JCR-SQL2 selects from *node types* not *tables*.
- `LIMIT BY` and `OFFSET` are not supported.
- Namespaced node types should always be surrounded by square brackets (`[` and `]`).

In the following examples I will use the PHPCR shell to execute the queries.

## Basics

The basic query grammer is defined as:

    Query ::= 'SELECT' columns

    'FROM' Source

    ['WHERE' Constraint]

    ['ORDER BY' orderings]

This should be familiar to anybody with a background in SQL.

So `WHERE` and `ORDER BY` are optional, and `SELECT` and `FROM` are mandatory.

- `columns` can either be a wildcard (e.g. `*` or `selector.*`) or a list of column names
or both.
- `source` can be a simple node type name, or a join source.
- `where` is a list of criteria for selecting the records
- `order by` determines which fields will be used to order the result set and in which direction.

The following are valid statements

{% highlight sql %}
SELECT title FROM [myCms:article];
SELECT * FROM [myCms:article] ORDER BY title
SELECT a.* FROM [myCms:article] AS a;
{% endhighlight %}
