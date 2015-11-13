# Entidades

Uma entidade representa uma unidade organizacional e ela pode ser uma pessoa jurídica ou uma pessoa física.

Toda `Account` tem no mínimo uma entidade. Os usuários que quiserem administrar empresas diferentes ou separar a gestão financeira entre matriz e filiais, por exemplo, poderão utilizar entidades diferentes.

A maior parte dos recursos da API estarão aninhados à uma entidade específica, como por exemplo as Contas (DepositAccount), Lançamentos (FinancialTransaction), Contas a Pagar (PayableAccount), etc.