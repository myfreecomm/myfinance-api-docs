## Múltiplas contas

> Exemplo de utilização com múltiplas contas

```shell
$ curl -u 7ezUPAqq8T1ny0w1bSXr \
       -H "Accept: application/xml" \
       -H "Content-type: application/xml" \
       -H "ACCOUNT_ID: 1" \
       -X GET http://app.myfinance.com.br/people/816
```

### Tenho mais de uma conta, como devo proceder?

Caso você possua acesso a várias contas, será necessário informar o ID da conta que deseja utilizar.

Isto é feito através do `header` `ACCOUNT_ID` enviado no cabeçalho da requisição.