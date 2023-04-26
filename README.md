# sql-busca

SELECT C.NOME +' '+ C.SOBRENOME AS CLIENTE,

C.SEXO AS SEXO_CLIENTE,

P.PRODUTO AS PRODUTO,

CA.NOME AS CATEGORIA,

N.IDNOTA AS NOTA_FISCAL,

N.DATA AS DATA_NOTA,

QUANTIDADE,

VALOR AS PRECO_PRODUTO,

I.TOTAL AS TOTAL_ITEM,

N.TOTAL AS TOTAL_NOTA,

FP.FORMA AS FORMA_PAGAMENTO

FROM CLIENTE C

INNER JOIN NOTA_FISCAL N

ON C.IDCLIENTE = N.ID_CLIENTE

INNER JOIN FORMA_PAGAMENTO FP

ON IDFORMA = ID_FORMA

INNER JOIN ITEM_NOTA I

ON N.IDNOTA = I.ID_NOTA_FISCAL

INNER JOIN PRODUTO P

ON P.IDPRODUTO = I.ID_PRODUTO

INNER JOIN CATEGORIA CA

ON IDCATEGORIA = ID_CATEGORIA

ORDER BY 5

GO
