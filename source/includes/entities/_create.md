## Criar entidade

> `POST /entities`

```shell
$ curl -u 7ezUPAqq8T1ny0w1bSXr:x \
       -X POST https://app.myfinance.com.br/entities \
       -d '
        {
          "entity": {
            "name": "Daily Bugle"
          }
        }
       '
```

> Exemplo de resposta

<pre class="headers highlight json">
HTTP/1.1 201 Created
Location: https://app.myfinance.com.br/entities/111
Content-Type: application/json; charset=utf-8
Date: Wed, 26 Jan 2011 13:27:00 GMT
</pre>
```json
{
  "entity": {
    "account_id": 1,
    "created_at": "2011-07-14T16:10:15-03:00",
    "federation_subscription_number": null,
    "force_destroy": false,
    "id": 111,
    "name": "Daily Bugle",
    "updated_at": "2011-07-14T16:10:15-03:00",
    "deleted_at": null
  }
}
```

<pre class="headers highlight xml">
HTTP/1.1 201 Created
Location: https://app.myfinance.com.br/entities/111
Content-Type: application/xml; charset=utf-8
Date: Wed, 26 Jan 2011 13:27:00 GMT
</pre>
```xml
<?xml version="1.0" encoding="UTF-8"?>
<entity>
  <created-at type="datetime">2011-07-14T15:42:51-03:00</created-at>
  <federation-subscription-number nil="true"></federation-subscription-number>
  <force-destroy type="boolean">false</force-destroy>
  <account-id type="integer">1</account-id>
  <id type="integer">111</id>
  <name>Daily Bugle</name>
  <updated-at type="datetime">2011-07-14T15:42:51-03:00</updated-at>
  <deleted-at type="datetime" nil="true"></deleted-at>
</entity>
```


Cria uma nova entidade com os parâmetros informados. Em caso de sucesso, retorna `201: Created`, juntamente com a URI da entidade criada no cabeçalho `Location` da resposta HTTP.

Em caso de falha, retorna `422: Unprocessable entity` juntamente com a descrição dos erros.