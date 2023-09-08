# ExcelToSql
Format Excel data into common SQL formats

The tool currently has the following functions

-------------------------------

**Format for IN**

Changes

    Val1    
    Val2
    Val3

into

    ('Val1',
    'Val2',
    'Val3')    
 -----------
**Format for VALUE**

Changes

    Val1 ValA
    Val2 ValB
    Val3 ValC

into

    ('Val1','ValA'),
    ('Val2','ValB'),
    ('Val3','ValC')    
----
**Comma Separated**

Changes

    Val1    
    Val2
    Val3

into

    Val1,Val2,Val3
---
**Empty Select**

Changes

    Val1    
    Val2
    Val3

into

    SELECT
      '' [Val1],
      '' [Val2],
      '' [Val3]

I use this for when someone sends me a request along the lines of "I need a report with these columns". Then I can start with what's above and basically fill in the blanks.
---
**Case Statement**

Changes

    Val1 ValA
    Val2 ValB
    Val3 ValC

into

    CASE [field]
    WHEN 'Val1' THEN 'ValA'
    WHEN 'Val2' THEN 'ValB'
    WHEN 'Val3' THEN 'ValC'
    END

I rarely use this but when I do it's because someone sent me a file containing mapping information
