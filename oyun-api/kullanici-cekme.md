# Kullanıcı Çekme

{% api-method method="get" host="https://furtsy.wtf" path="/api/oyun/oyunid/kullanicilar/ip/port" %}
{% api-method-summary %}
Kullanıcıları Çekme
{% endapi-method-summary %}

{% api-method-description %}
Sunucuda oynayan kullanıcıların isimlerini çekersiniz
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="Oyuncular" type="string" required=false %}
oyuncuların isimlerini gösterir
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Başarılı şekilde çektiniz
{% endapi-method-response-example-description %}

```
{"Oyuncular":"oyuncu1,oyuncu2"}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Sunucu bilgileri yanlış veya engelleniyor
{% endapi-method-response-example-description %}

```
{}
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

