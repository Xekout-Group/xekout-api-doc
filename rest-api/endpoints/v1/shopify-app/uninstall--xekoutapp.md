---
description: Webhook para capturar evento de desinstalação de app no dashboard da Shopify.
---

# Desinstalação do XekoutApp

{% api-method method="post" host="https://dev-api.xekout.app" path="/v1/shopify/uninstall" %}
{% api-method-summary %}
Uninstall
{% endapi-method-summary %}

{% api-method-description %}
Este endpoint permite desinstalar o app XekoutApp em uma loja cadastrada na plataforma do Shopify.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="shop\_owner" type="string" required=true %}
Nome do dono da loja no Shopify.
{% endapi-method-parameter %}

{% api-method-parameter name="customer\_email" type="string" required=true %}
Email do dono da loja no Shopify.
{% endapi-method-parameter %}

{% api-method-parameter name="domain" type="string" required=true %}
Domínio da loja no Shopify.
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=true %}
Email da loja no Shopify.
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
Nome da loja no Shopify.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="integer" required=true %}
Identificador da loja no Shopify.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
A desinstalação ocorreu com sucesso.
{% endapi-method-response-example-description %}

```text
Ok
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Falha ao tentar capturar dados necessários para processar a operação.
{% endapi-method-response-example-description %}

```text
{
  "status": "error",
  "code": 400103,
  "message": "Data for webhook invalid"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Não possui autorização para completar a operação.
{% endapi-method-response-example-description %}

```text
{
  "status": "error",
  "code": 401100,
  "message": "Operation not permitted"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="warning" %}
A Shopify envia todos os dados referente ao cadastro da loja, assim como da pessoa que gerencia ela, porém esses dados são os necessários para desativar o cadastro da loja assim como do admin.
{% endhint %}

