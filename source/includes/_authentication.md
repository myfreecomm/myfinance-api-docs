# Autenticação

> Exemplo de chamada API autenticada (onde 7ezUPAqq8T1ny0w1bSXr é o authentication_token do usuário):

```shell
$ curl -u 7ezUPAqq8T1ny0w1bSXr \
       -H "Accept: application/xml" \
       -H "Content-type: application/xml" \
       -X GET https://app.myfinance.com.br/people/816
```


Todo acesso à API é feito do ponto de vista de um usuário existente no MyFinance.

Sendo assim, toda requisição à API deverá ser autenticada via HTTP Basic utilizando um token de acesso.

No entant, em vez de utilizar o login e senha do usuário, como é tradicional, deve-se fornecer o `authentication_token` do usuário (uma string de até 60 caracteres encontrada na página de perfil do usuário no Passaporte Web) no campo 'login' e uma string vazia no campo 'password'.

Alguns clientes HTTP podem reclamar do fato do campo 'password' estar vazio, nesse caso pode-se informar 'X' como senha que o sistema irá ignorar.

<aside class="notice">
Lembre-se de substituir <code>7ezUPAqq8T1ny0w1bSXr</code> pelo seu <code>authentication_token</code>.
</aside>