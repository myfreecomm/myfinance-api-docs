## Suspensão do acesso

> Exemplo de resposta com erro

```json
{
  "error": "Conta bloqueada por falta de pagamento. Entre em contato conosco via suporte@myfinance.com.br"
}
```

```xml
<?xml version="1.0" encoding="UTF-8"?>
<errors>
  <error>Conta bloqueada por falta de pagamento. Entre em contato conosco via suporte@myfinance.com.br</error>
</errors>
```

Caso o sistema não localize o último pagamento de mensalidade, o acesso à API será bloqueado após 10 dias a contar da data de vencimento.

<aside class="notice">
Nenhum dado da conta será apagado, apenas o acesso será suspenso até a identificação do pagamento. O usuário deverá entrar em contato com o suporte para regularizar sua situação.
</aside>

Caso o acesso à API seja efetuado neste período (10 dias após o vencimento da mensalidade), o sistema retornará uma mensagem de erro `402: Payment Required`.