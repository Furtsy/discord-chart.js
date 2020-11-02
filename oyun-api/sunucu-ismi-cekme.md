# Sunucu İsmi Çekme

{% api-method method="get" host="https://furtsy.wtf" path="/api/oyun/oyunid/isim/ip/port" %}
{% api-method-summary %}
Sunucu ismini çekme
{% endapi-method-summary %}

{% api-method-description %}
Çektiğiniz sunucunun sunucu ismini çekersiniz
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="Sunucu\_İsmi" type="string" %}
Sunucu ismini gösterir
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Başarılı şekilde çektiniz
{% endapi-method-response-example-description %}

```
{"Sunucu_İsmi":"isim"}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Çekmek istediğiniz bilgiler yanlış veya sunucu bilgi çekmeyi engelliyor
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
let oyunid = ''//https://furtsy.wtf/oyunidler
require("request")(`https://furtsy.wtf/api/oyun/${oyunid}/isim/${ip}/${port}`, async function (err, resp, body) { 
body = JSON.parse(body); 
console.log("Sunucu İsmi:" + `${body.Sunucu_İsmi}`) 
}) 
```

