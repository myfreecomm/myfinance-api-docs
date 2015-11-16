## Informações da categoria

> `GET /categories/:id`

```shell
$ curl -u 7ezUPAqq8T1ny0w1bSXr:x \
       -X GET https://app.myfinance.com.br/categories/111
```

> Exemplo de resposta

<pre class="headers highlight json">
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8
Date: Wed, 26 Jan 2011 13:11:23 GMT
</pre>
```json
{
  "category": {
    "cost": true,
    "created_at": "2012-10-31T11:59:29-02:00",
    "force_destroy": false,
    "excel_import_id": null,
    "full_name": "Proventos / Salário",
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
HTTP/1.1 200 OK
Content-Type: application/xml; charset=utf-8
Date: Wed, 26 Jan 2011 13:11:23 GMT
</pre>
```xml
<?xml version="1.0" encoding="UTF-8"?>
<category>
  <cost type="boolean">true</cost>
  <created-at type="datetime">2012-10-31T11:59:29-02:00</created-at>
  <excel-import-id type="integer" nil="true"/>
  <force-destroy type="boolean">false</force-destroy>
  <full-name>Proventos / Salário</full-name>
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

Retorna os atributos da categoria especificada com uma resposta `200: Ok`.