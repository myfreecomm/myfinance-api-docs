## Atualizar categoria

> `PUT /categories/:id`

```shell
$ curl -u 7ezUPAqq8T1ny0w1bSXr:x \
       -X PUT https://app.myfinance.com.br/categories/111 \
       -d '
        {
          "entity": {
            "name": "Categoria atualizada"
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
  "category": {
    "cost": true,
    "created_at": "2012-10-31T11:59:29-02:00",
    "force_destroy": false,
    "excel_import_id": null,
    "full_name": "Categoria atualizada",
    "id": 9,
    "imported_from_sync": false,
    "interested_users_ids": [],
    "modified_by_sync": false,
    "name": "Salário",
    "parent_id": 8,
    "revenue": true,
    "updated_at": "2012-10-31T11:59:29-02:00",
    "use_count": 1
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
  <created-at type="datetime">2012-10-31T11:59:29-02:00</created-at>
  <excel-import-id type="integer" nil="true"/>
  <force-destroy type="boolean">false</force-destroy>
  <full-name>Categoria atualizada</full-name>
  <id type="integer">9</id>
  <imported-from-sync type="boolean">false</imported-from-sync>
  <interested-users-ids type="array"/>
  <modified-by-sync type="boolean">false</modified-by-sync>
  <name>Salário</name>
  <parent-id type="integer">8</parent-id>
  <revenue type="boolean">true</revenue>
  <updated-at type="datetime">2012-10-31T11:59:29-02:00</updated-at>
  <use-count type="integer">1</use-count>
</category>
```


Altera a categoria especificada. Retorna uma resposta com o objeto alterado e `200: Ok` em caso de sucesso ou uma resposta `422: Unprocessable entity` com a descrição dos erros em caso de falha.

