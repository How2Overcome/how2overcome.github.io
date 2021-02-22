---
layout: single
title: "VSCODE SQLTools를 활용한 Postgresql 사용법"
date: 2021-02-07 09:05:00 -0400
categories: Tool
tags: [SQL, PostgreSQL, VSCODE] 
---




```sql
CREATE SCHEMA h2o;

CREATE TABLE h2o.temp_table
(
          col_1 INT
     ,    col_2 VARCHAR
);

INSERT INTO h2o.temp_table
SELECT    1  AS col_1
     ,   'a' AS col_2
 UNION ALL
SELECT    2  AS col_1
     ,   'b' AS col_2
 UNION ALL
SELECT    3  AS col_1
     ,   'c' AS col_2
 UNION ALL
SELECT    4  AS col_1
     ,   'd' AS col_2
 UNION ALL
SELECT    5  AS col_1
     ,   'e' AS col_2
 UNION ALL
SELECT    6  AS col_1
     ,   'f' AS col_2
;

SELECT    col_1
     ,    col_2
  FROM    h2o.temp_table
;
```

_실행하려는 SQL영역을 드래그_ 후 [`Ctrl+E`]를 누르면 SQL이 실행 된다.

현재 사용중인 VSCODE 버전 때문인지.  
아니면, 다른 해당 Plugin 버전 때문인지.  