## Listar categorias

> `GET /categories`

```shell
$ curl -u 7ezUPAqq8T1ny0w1bSXr:x \
       -X GET https://app.myfinance.com.br/categories
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
    "category": {
      "account_id": 1,
        "cost": true,
          "created_at": "2012-10-31T11:59:28-02:00",
            "excel_import_id": null,
            "force_destroy": false,
            "full_name": "Diversão",
            "guid": null,
            "id": 5,
            "imported_from_sync": false,
            "interested_users_ids": [],
            "modified_by_sync": false,
            "name": "Diversão",
            "parent_id": null,
            "revenue": true,
            "updated_at": "2012-10-31T11:59:28-02:00",
            "use_count": 1
        }
    },
    {
      "category": {
        "account_id": 1,
          "cost": true,
            "created_at": "2012-10-31T11:59:29-02:00",
            "excel_import_id": null,
            "force_destroy": false,
            "full_name": "Luxo",
            "guid": null,
            "id": 6,
            "imported_from_sync": false,
            "interested_users_ids": [],
            "modified_by_sync": false,
            "name": "Luxo",
            "parent_id": null,
            "revenue": true,
            "updated_at": "2012-10-31T11:59:29-02:00",
            "use_count": 0
        }
    },
    {
      "category": {
        "account_id": 1,
          "cost": true,
            "created_at": "2012-10-31T11:59:29-02:00",
            "excel_import_id": null,
            "force_destroy": false,
            "full_name": "Luxo / Veiculos",
            "guid": null,
            "id": 7,
            "imported_from_sync": false,
            "interested_users_ids": [],
            "modified_by_sync": false,
            "name": "Veiculos",
            "parent_id": 6,
            "revenue": true,
            "updated_at": "2012-10-31T11:59:29-02:00",
            "use_count": 1
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
<categories type="array">
  <category>
    <cost type="boolean">true</cost>
    <created-at type="datetime">2012-10-31T11:59:28-02:00</created-at>
    <excel-import-id type="integer" nil="true"/>
    <force-destroy type="boolean">false</force-destroy>
    <full-name>Diversão</full-name>
    <id type="integer">5</id>
    <imported-from-sync type="boolean">false</imported-from-sync>
    <interested-users-ids type="array"/>
    <modified-by-sync type="boolean">false</modified-by-sync>
    <name>Diversão</name>
    <parent-id type="integer" nil="true"/>
    <revenue type="boolean">true</revenue>
    <updated-at type="datetime">2012-10-31T11:59:28-02:00</updated-at>
    <use-count type="integer">1</use-count>
  </category>
  <category>
    <cost type="boolean">true</cost>
    <created-at type="datetime">2012-10-31T11:59:29-02:00</created-at>
    <excel-import-id type="integer" nil="true"/>
    <force-destroy type="boolean">false</force-destroy>
    <full-name>Luxo</full-name>
    <id type="integer">6</id>
    <imported-from-sync type="boolean">false</imported-from-sync>
    <interested-users-ids type="array"/>
    <modified-by-sync type="boolean">false</modified-by-sync>
    <name>Luxo</name>
    <parent-id type="integer" nil="true"/>
    <revenue type="boolean">true</revenue>
    <updated-at type="datetime">2012-10-31T11:59:29-02:00</updated-at>
    <use-count type="integer">0</use-count>
  </category>
  <category>
    <cost type="boolean">true</cost>
    <created-at type="datetime">2012-10-31T11:59:29-02:00</created-at>
    <excel-import-id type="integer" nil="true"/>
    <force-destroy type="boolean">false</force-destroy>
    <full-name>Luxo / Veiculos</full-name>
    <id type="integer">7</id>
    <imported-from-sync type="boolean">false</imported-from-sync>
    <interested-users-ids type="array"/>
    <modified-by-sync type="boolean">false</modified-by-sync>
    <name>Veiculos</name>
    <parent-id type="integer">6</parent-id>
    <revenue type="boolean">true</revenue>
    <updated-at type="datetime">2012-10-31T11:59:29-02:00</updated-at>
    <use-count type="integer">1</use-count>
  </category>
  <category>
    <cost type="boolean">true</cost>
    <created-at type="datetime">2012-10-31T11:59:23-02:00</created-at>
    <excel-import-id type="integer" nil="true"/>
    <force-destroy type="boolean">false</force-destroy>
    <full-name>Moradia</full-name>
    <id type="integer">1</id>
    <imported-from-sync type="boolean">false</imported-from-sync>
    <interested-users-ids type="array"/>
    <modified-by-sync type="boolean">false</modified-by-sync>
    <name>Moradia</name>
    <parent-id type="integer" nil="true"/>
    <revenue type="boolean">true</revenue>
    <updated-at type="datetime">2012-10-31T11:59:23-02:00</updated-at>
    <use-count type="integer">0</use-count>
  </category>
  <category>
    <cost type="boolean">true</cost>
    <created-at type="datetime">2012-10-31T11:59:24-02:00</created-at>
    <excel-import-id type="integer" nil="true"/>
    <force-destroy type="boolean">false</force-destroy>
    <full-name>Moradia / Aluguél</full-name>
    <id type="integer">3</id>
    <imported-from-sync type="boolean">false</imported-from-sync>
    <interested-users-ids type="array"/>
    <modified-by-sync type="boolean">false</modified-by-sync>
    <name>Aluguél</name>
    <parent-id type="integer">1</parent-id>
    <revenue type="boolean">true</revenue>
    <updated-at type="datetime">2012-10-31T11:59:24-02:00</updated-at>
    <use-count type="integer">61</use-count>
  </category>
  <category>
    <cost type="boolean">true</cost>
    <created-at type="datetime">2012-10-31T11:59:25-02:00</created-at>
    <excel-import-id type="integer" nil="true"/>
    <force-destroy type="boolean">false</force-destroy>
    <full-name>Moradia / contas</full-name>
    <id type="integer">4</id>
    <imported-from-sync type="boolean">false</imported-from-sync>
    <interested-users-ids type="array"/>
    <modified-by-sync type="boolean">false</modified-by-sync>
    <name>contas</name>
    <parent-id type="integer">1</parent-id>
    <revenue type="boolean">true</revenue>
    <updated-at type="datetime">2012-10-31T11:59:25-02:00</updated-at>
    <use-count type="integer">183</use-count>
  </category>
  <category>
    <cost type="boolean">true</cost>
    <created-at type="datetime">2012-10-31T11:59:23-02:00</created-at>
    <excel-import-id type="integer" nil="true"/>
    <force-destroy type="boolean">false</force-destroy>
    <full-name>Moradia / Lazer</full-name>
    <id type="integer">2</id>
    <imported-from-sync type="boolean">false</imported-from-sync>
    <interested-users-ids type="array"/>
    <modified-by-sync type="boolean">false</modified-by-sync>
    <name>Lazer</name>
    <parent-id type="integer">1</parent-id>
    <revenue type="boolean">true</revenue>
    <updated-at type="datetime">2012-10-31T11:59:23-02:00</updated-at>
    <use-count type="integer">61</use-count>
  </category>
  <category>
    <cost type="boolean">true</cost>
    <created-at type="datetime">2012-10-31T11:59:29-02:00</created-at>
    <excel-import-id type="integer" nil="true"/>
    <force-destroy type="boolean">false</force-destroy>
    <full-name>Proventos</full-name>
    <id type="integer">8</id>
    <imported-from-sync type="boolean">false</imported-from-sync>
    <interested-users-ids type="array"/>
    <modified-by-sync type="boolean">false</modified-by-sync>
    <name>Proventos</name>
    <parent-id type="integer" nil="true"/>
    <revenue type="boolean">true</revenue>
    <updated-at type="datetime">2012-10-31T11:59:29-02:00</updated-at>
    <use-count type="integer">0</use-count>
  </category>
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
</categories>

```

Retorna uma lista de todas as categorias da `Account`.