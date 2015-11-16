## Criar categoria

> `POST /categories`

```shell
$ curl -u 7ezUPAqq8T1ny0w1bSXr:x \
       -X POST https://app.myfinance.com.br/categories \
       -d '
        {
          "category":{
            "name":"Categoria Tal",
          }
        }
       '
```

> Exemplo de resposta

<pre class="headers highlight json">
HTTP/1.1 201 Created
Location: https://app.myfinance.com.br/categories/111
Content-Type: application/json; charset=utf-8
Date: Wed, 26 Jan 2011 13:27:00 GMT
</pre>
```json
{
  "category":{
    "cost":true,
    "created_at":"2012-11-07T17:05:53-02:00",
    "excel_import_id":null,
    "force_destroy":false,
    "full_name":"Categoria Tal",
    "id":73,
    "imported_from_sync":false,
    "interested_users_ids":[1],
    "modified_by_sync":false,
    "name":"Categoria Tal",
    "parent_id":null,
    "revenue":true,
    "updated_at":"2012-11-07T17:05:53-02:00",
    "use_count":0
  }
}
```

<pre class="headers highlight xml">
HTTP/1.1 201 Created
Location: https://app.myfinance.com.br/categories/111
Content-Type: application/xml; charset=utf-8
Date: Wed, 26 Jan 2011 13:27:00 GMT
</pre>
```xml
<?xml version="1.0" encoding="UTF-8"?>
<category>
  <cost type="boolean">true</cost>
  <created-at type="datetime">2012-11-07T17:10:28-02:00</created-at>
  <excel-import-id type="integer" nil="true"></excel-import-id>
  <force-destroy type="boolean">false</force-destroy>
  <full-name>Categoria Tal</full-name>
  <id type="integer">73</id>
  <imported-from-sync type="boolean">false</imported-from-sync>
  <interested-users-ids type="array">
    <interested-users-id type="integer">1</interested-users-id>
  </interested-users-ids>
  <modified-by-sync type="boolean">false</modified-by-sync>
  <name>Categoria Tal</name>
  <parent-id type="integer" nil="true"></parent-id>
  <revenue type="boolean">true</revenue>
  <updated-at type="datetime">2012-11-07T17:10:28-02:00</updated-at>
  <use-count type="integer">0</use-count>
</category>
```

Cria uma nova categoria com os parâmetros informados. Em caso de sucesso, retorna `201: Created`, juntamente com a URI da categoria criada no cabeçalho `Location` da resposta HTTP.

Em caso de falha, retorna `422: Unprocessable entity` juntamente com a descrição dos erros.