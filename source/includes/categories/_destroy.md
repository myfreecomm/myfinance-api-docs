## Excluir categoria

> `DELETE /categories/:id`

```shell
$ curl -u 7ezUPAqq8T1ny0w1bSXr:x \
       -X DELETE https://app.myfinance.com.br/categories/1
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


Exclui a categoria especificada, retornando uma resposta com corpo vazio e status `202: Accepted`.

<aside class="notice">
Em caso de sucesso, todos os recursos previamente associados ao categoria apagado continuarão existindo, porém não estarão associados a nenhum categoria!
</aside>