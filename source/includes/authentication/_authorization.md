## Autorização de uso da API

> Exemplo de resposta com erro por não estar autorizado a acessar a API

```json
{
  "error": "Seu plano não permite o uso da API."
}
```

```xml
<?xml version="1.0" encoding="UTF-8"?>
<errors>
  <error>Seu plano não permite o uso da API.</error>
</errors>
```

Apenas usuários de contas em planos Plus ou superior têm acesso autorizado à API.
Caso o acesso à API seja feito utilizando um `authentication_token` de um usuário cujo plano não permite acesso à API, uma resposta de erro `403: Forbidden` será retornada.