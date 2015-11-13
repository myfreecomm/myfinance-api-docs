## Listar entidades

> `GET /entities`

```shell
$ curl -u 7ezUPAqq8T1ny0w1bSXr:x \
       -X GET https://app.myfinance.com.br/entities
```

> Exemplo de resposta

<pre class="headers highlight json">
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8
Date: Wed, 26 Jan 2011 13:11:23 GMT
</pre>
```json
[
  {
    "entity":
      {
        "created_at":"2011-07-14T11:37:30-03:00",
        "federation_subscription_number":"",
        "force_destroy":false,"id":12,
        "name":"Nova",
        "updated_at":"2011-07-14T11:37:30-03:00",
        "deleted_at":null
      }
  },
  {
    "entity":
      {
        "created_at":"2011-07-08T15:05:51-03:00",
        "federation_subscription_number":"11111111111",
        "force_destroy":false,
        "account_id":1,
        "id":1,
        "name":"Minhas Finanças",
        "updated_at":"2011-07-14T15:13:43-03:00",
        "deleted_at":null
      }
  }
]

```

<pre class="headers highlight xml">
HTTP/1.1 200 OK
Content-Type: application/xml; charset=utf-8
Date: Wed, 26 Jan 2011 13:11:23 GMT
</pre>
```xml
<?xml version="1.0" encoding="UTF-8"?>
<entities type="array">
  <entity>
    <created-at type="datetime">2011-07-14T11:37:30-03:00</created-at>
    <federation-subscription-number nil="true"></federation-subscription-number>
    <force-destroy type="boolean">false</force-destroy>
    <account-id type="integer">1</account-id>
    <id type="integer">12</id>
    <name>Nova</name>
    <updated-at type="datetime">2011-07-14T11:37:30-03:00</updated-at>
    <deleted-at type="datetime" nil="true"></deleted-at>
  </entity>
  <entity>
    <created-at type="datetime">2011-07-08T15:05:51-03:00</created-at>
    <federation-subscription-number>11111111111</federation-subscription-number>
    <force-destroy type="boolean">false</force-destroy>
    <id type="integer">1</id>
    <name>Minhas Finanças</name>
    <updated-at type="datetime">2011-07-14T15:13:43-03:00</updated-at>
    <deleted-at type="datetime" nil="true"></deleted-at>
  </entity>
</entities>

```

Retorna uma lista de todas as entidades da `Account`.