## Compressão gzip

> Exemplo de utilização da compressão `gzip`

```shell
$ curl -u 7ezUPAqq8T1ny0w1bSXr:x \
       -H 'Accept: application/json' \
       -H 'Content-type: application/json' \
       -H 'Accept-Encoding: gzip' \
       -X GET https://app.myfinance.com.br/entities/2593/attachments/25940
```

A compressão gzip é considerada sem perda de dados. As vantagens de utilizá-la são o menor uso da largura de banda e a maior velocidade na resposta.

Para utilizar o recurso da compressão gzip nas requisições, basta adicionar o header `Accept-Encoding` com o valor `gzip`.

Caso a resposta esteja comprimida, ela conterá um header `Content-Encoding` com o valor `gzip`.

Em alguns casos, mesmo que o servidor mande uma resposta comprimida, a requisição pode vir sem compressão, pois pode existir algum proxy no caminho da resposta que realize a descompressão dos dados (podendo ou não remover o header `Content-Encoding`).

No exemplo ao lado, a requisição sem compressão possui um tamanho de 604 bytes. Quando comprimida, possui um tamanho de 290 bytes.