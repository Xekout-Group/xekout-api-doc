# Salvar credenciais do Hotjar

{% api-method method="post" host="https://dev-api.xekout.app" path="/v1/admin/apps/hotjar/:subdomain" %}
{% api-method-summary %}
Salvar credenciais do Hotjar
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="subdomain" required=true %}
Subdomain da loja cadastrada na Xekout.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Prefix" %}
Bearer Token JWT para autenticação.
{% endapi-method-parameter %}

{% api-method-parameter name="Authentication" required=true %}
Usado na construção de uma chave para armazenamento de token em todos os provedores de armazenamento.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="code" type="string" required=true %}
ID do site no Hotjar.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
  "status": "success",
  "code": 201000,
  "message": "App Hotjar saved successfuly"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
  "status": "error",
  "code": 404013,
  "message": "Tenant not found"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}
