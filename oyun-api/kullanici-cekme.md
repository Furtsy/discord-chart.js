# Kullanıcı Çekme

{% api-method method="get" host="https://furtsy.wtf/api/oyun/csgo/kullanicilar/185.171.25.21/27015" path="" %}
{% api-method-summary %}
Metot:get
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="Oyuncular" type="string" required=false %}
oyuncuları gösterir
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Örnek kullanım

```text
let ip = ''//ip 
let port = ''//port 
let oyunid = ''
require("request")(`https://furtsy.wtf/api/oyun/${oyunid}/kullanicilar/${ip}/${port}`, async function (err, resp, body) { 
body = JSON.parse(body); 
console.log("Oyuncular:" + `${body.Oyuncular}`) 
}) 
```

