---
author: []
related: []
publisher:
  url: 'https://bugs.mysql.com'
  name: Mysql
  favicon: 'https://bugs.mysql.com/favicon.ico'
  domain: bugs.mysql.com
keywords:
  - stmt
  - table
  - sqltables
  - database
  - catalog
  - information_schema
  - dbc
  - patch
  - query
  - row
description: 'An entry has been added to the 5.1.7 changelog: The SQLTables() function required approximately two to four minutes to return the list of 400 tables in a database. The SHOW TABLE STATUS query used by SQLTables() was extremely slow for InnoDB tables with a large number of rows because the query was calculating the approximate number of rows in each table.'
inLanguage: en
app_links: []
isBasedOnUrl: 'https://bugs.mysql.com/bug.php?id=43664'
title: 'MySQL Bugs: #43664: SQLTables is very slow due to SHOW TABLE STATUS'
datePublished: '2016-05-02T23:32:53.234Z'
dateModified: '2016-05-02T19:08:20.490Z'
starred: false
sourcePath: _posts/2016-05-02-mysql-bugs-43664-sqltables-is-very-slow-due-to-show-table.md
published: true
inFeed: true
hasPage: false
inNav: false
_context: 'http://schema.org'
_type: MediaObject

---
<article style=""><h1>MySQL Bugs: #43664: SQLTables is very slow due to SHOW TABLE STATUS</h1><p>An entry has been added to the 5.1.7 changelog: The SQLTables() function required approximately two to four minutes to return the list of 400 tables in a database. The SHOW TABLE STATUS query used by SQLTables() was extremely slow for InnoDB tables with a large number of rows because the query was calculating the approximate number of rows in each table.</p><img src="https://bugs.mysql.com/images/mysql_100x52-64.gif" /></article>