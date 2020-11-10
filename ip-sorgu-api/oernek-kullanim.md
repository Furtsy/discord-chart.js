# Örnek Kullanım

{% api-method method="get" host="https://furtsy.wtf" path="/ip-sorgu/:ip" %}
{% api-method-summary %}
ip adresinin bilgileri çekmek
{% endapi-method-summary %}

{% api-method-description %}
:ip çekmek istediğiniz ipyi girmelisiniz
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="ip\_postakod" type="string" required=false %}
ipinin posta konunu gösterir
{% endapi-method-parameter %}

{% api-method-parameter name="ip\_kordinat" type="string" required=false %}
ipnin kordinatı gösterir
{% endapi-method-parameter %}

{% api-method-parameter name="ip\_yer" type="string" required=false %}
ipin yerinin gösterir
{% endapi-method-parameter %}

{% api-method-parameter name="şehir" type="string" required=false %}
şehiri gösterir
{% endapi-method-parameter %}

{% api-method-parameter name="ip" type="string" %}
getletiğiniz ipyi gösterir
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{"ip":"134.238.9.18","şehir":"Atlantic City","ip_yer":"New Jersey","ip_kordinat":"39.3642,-74.4231","ip_postakod":"08404"}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```
{"hata": "bulunumadı"}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



