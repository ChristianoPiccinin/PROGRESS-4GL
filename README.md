# PROGRESS-4GL

## Variaveis
```Progress OpenEdge
/*Declaração de variaveis*/
DEFINE VARIABLE c AS CHARACTER   NO-UNDO.
DEFINE VARIABLE i AS INTEGER     NO-UNDO.
DEFINE VARIABLE d AS DECIMAL     NO-UNDO.
DEFINE VARIABLE l AS LOGICAL     NO-UNDO.
```

## Laços de Repetição
```ABL
DO i = 1 TO 12:
  month-quota[i] = 0.
END. 

REPEAT i = 1 TO 12:
  month-quota[i] = 0.
END. 
 

FOR EACH customer:
  DISPLAY name credit-limit.
  PAUSE 3.
  IF credit-limit > 80000 THEN DO:
       credit-limit = 80000.
       DISPLAY name credit-limit.
  END.
END.

```

## Temp-tables
```progress

DEFINE TEMP-TABLE ttCallParam NO-UNDO 
    FIELD iParamNo       AS INTEGER 
    FIELD cParamName     AS CHARACTER 
    FIELD cDataType      AS CHARACTER 
    FIELD cIOMode        AS CHARACTER 
    FIELD cCharacter     AS CHARACTER 
    FIELD tDate          AS DATE 
    FIELD lLogical       AS LOGICAL 
    FIELD iInteger       AS INTEGER 
    FIELD dDecimal       AS DECIMAL 
    INDEX pudx IS UNIQUE PRIMARY 
      iParamNo. 

```

## Condicionais
```progress
IF condition THEN expression1 ELSE expression2 

CASE pay-stat:
  WHEN 1 THEN
    MESSAGE "This account is unpaid.".
  WHEN 2 THEN  
    MESSAGE "This account is partially paid.".
  WHEN 3 THEN  
    MESSAGE "This account is paid in full.".
END CASE. 
```


