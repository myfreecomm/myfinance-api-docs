# Categorias

O recurso `Category` representa uma categoria ou subcategoria cadastrada em seu MyFinance.

As categorias estão associadas diretamente à sua `Account` no MyFinance, isto é, são compartilhados entre todas as entidades (`Entity`) de sua conta no MyFinance.

As categorias podem ser associadas à outros objetos (`FinancialTranscation` e `FinancialAccount`) tanto através de seu `ID` (seu código identificador único no sistema) quanto através de seu nome completo (atributo `full_name`).

Para isso, os nomes devem ser únicos no contexto do seu MyFinance.
