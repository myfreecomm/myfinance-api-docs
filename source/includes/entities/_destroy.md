## Excluir entidade

> `DELETE /entities/:id`

```shell
$ curl -u 7ezUPAqq8T1ny0w1bSXr:x \
       -X DELETE https://app.myfinance.com.br/entities/1
```

> Exemplo de resposta

<pre class="headers highlight json">
HTTP/1.1 202 Accepted
Content-Type: application/json; charset=utf-8
Date: Fri, 13 Nov 2015 14:21:03 GMT
</pre>

<pre class="headers highlight xml">
HTTP/1.1 202 Accepted
Content-Type: application/xml; charset=utf-8
Date: Fri, 13 Nov 2015 14:21:03 GMT
</pre>


Exclui a entidade especificada, retornando uma resposta com corpo vazio e status `202: Accepted`.

<aside class="warning">
Todos os recursos associados à entidade apagada também serão apagados!
</aside>

A última entidade de uma Account não pode ser excluída. Caso você tente excluir a última entidade de uma conta, receberá uma resposta de erro `422: Unprocessable entity` com uma resposta no body:

`{ "base": ["Só existe uma entidade.", "Não é possível apagar esta entidade."]}`.

Outras mensagens de erro podem ocorrer:

- Existem Contas que precisam ser apagadas
- Existem Contas a Pagar/Contas a Receber que precisam ser apagadas
- Existem Centro de Custo/Receita que precisam ser apagados

Se for o parâmetro `force_destroy` com valor `true`estiver presente, o myfinance considerará que o você deseja excluir todos os dados relacionados à entidade e não retornará as mensagens de erro acima.

<aside class="notice">
A exclusão é feita em background. Enquanto a exclusão não tiver sido concluída, a entidade continuará constando na lista de entidades da conta, porém virá com o atributo `deleted_at` preenchido com a data e hora do momento da solicitação da exclusão.
</aside>