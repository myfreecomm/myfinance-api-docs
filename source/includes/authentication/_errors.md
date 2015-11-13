## Erros na autenticação

### `authentication_token` inválido

> Exemplo de requisição sem informações de autenticação

```shell
$ curl -H "Accept: application/xml" \
       -H "Content-type: application/xml" \
       -X GET -https://app.myfinance.com.br/people/816

```

```json
{
  "error": "unauthenticated"
}

```

```xml
<?xml version="1.0" encoding="UTF-8"?>
<errors>
  <error>unauthenticated</error>
</errors>
```

Caso o usuário deixe de informar um `authentication_token` ou este seja inválido, o sistema retornará um erro `401: Unauthorized`

### Erro ao não informar o `header` `ACCOUNT_ID`

> Exemplo de resposta com erro ao não informar o `header` `ACCOUNT_ID`

```shell
$ curl -u 7ezUPAqq8T1ny0w1bSXr:x \
       -H "Accept: application/xml" \
       -H "Content-type: application/xml" \
       -X GET http://app.myfinance.com.br/people/816
```

```json
{
  "error": "O cabeçalho da requisição não possui o atributo ACCOUNT_ID",
  "status": "unprocessable_entity",
  "accounts": [{"account":{"id":1,"name":"Conta Um"}},{"account":{"id":2,"name":"Conta 2"}}]
}
```

```xml
<?xml version="1.0" encoding="UTF-8"?>
<errors>
  <error>O cabeçalho da requisição não possui o atributo ACCOUNT_ID</error>
  <status>unprocessable_entity</status>
  <accounts type="array">
    <account>
      <id type="integer">1</id>
      <name>Conta Um</name>
    </account>
    <account>
      <id type="integer">2</id>
      <name>Conta Dois</name>
    </account>
  </accounts>
</errors>
```

Se o `header` `ACCOUNT_ID` não for informado ou o valor informado não estiver associado ao `authentication_token` utilizado,
o sistema retornará uma mesagem de erro `422: Unprocessable Entity`.