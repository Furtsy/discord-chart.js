# Pingi Çekme

{% api-method method="get" host="https://furtsy.wtf" path="/api/oyun/oyunid/ping/ip/port" %}
{% api-method-summary %}
Sunucu pingi çekme
{% endapi-method-summary %}

{% api-method-description %}
Sunucunun pingini çekmeniz
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="Ping" type="number" %}
Sunucudaki pingi çekersiniz
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Başarılı şekilde çektiniz.
{% endapi-method-response-example-description %}

```
{"Ping":"164"}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Çekmek istediğiniz sunucu yanlış veya sunucu engelliyor
{% endapi-method-response-example-description %}

```
{}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### Örnek Kullanım

```text
let ip = ''//ip 
let port = ''//port 
let oyunid = ''
require("request")(`https://furtsy.wtf/api/oyun/${oyunid}/ping/${ip}/${port}`, async function (err, resp, body) { 
body = JSON.parse(body); 
console.log("Ping:" + `${body.Ping}`) 
}) 
```



