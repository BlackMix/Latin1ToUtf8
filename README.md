# Latin1ToUtf8 by Mix

UPDATE BD.TableUtf8 AS U1, BD.TableLatin1 AS U2 
SET U1.{ here } = CONVERT(CAST(CONVERT(U2.{ here } USING latin1) AS BINARY) USING utf8)
WHERE U1.id = U2.id 


{ here } = is the field of the table you want to convert

U1 = new bd in utf8

U2 = old bd in latin1
