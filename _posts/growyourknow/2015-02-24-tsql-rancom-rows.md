---
layout: post
categories: [GrowYourKnow]
title: Concatenate Strings in TSQL
tags : [tsql,code,how-to,tips,microsoft,sql-server]
pagename: blog
date: 2015-02-24 00:31:00 CDT
---

Sometimes it can be useful to randomly select a value (or row) from a table. One easy way to do this is to sort the table using a column that contains random values, and then select the first row. The following query illustrates this concept.

```SQL
-- initialize example data
DECLARE @Data TABLE (Id int IDENTITY(1,1), Caption varchar(25))

INSERT INTO @Data (Caption)
SELECT 'Apple'
UNION SELECT 'Orange'
UNION SELECT 'Banana'
UNION SELECT 'Pear'
UNION SELECT 'Mango'
UNION SELECT 'Kiwi'

-- query
SELECT TOP 1
Caption
FROM @Data
ORDER BY NEWID()
```

>It's worth noting that this isn't the fastest code in the world. While it's fine for rarely-run data samples, I wouldn't use it in an oft-called production routine.

Every time you run this query, you'll be presented with a random fruit from the list.

> Written with [StackEdit](https://stackedit.io/).