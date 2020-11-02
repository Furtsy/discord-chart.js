# Online Kişi Sayısını Çekme

{% api-method method="get" host="https://furtsy.wtf" path="/api/oyun/oyunid/online/ip/port" %}
{% api-method-summary %}
Online sayıyı çekme
{% endapi-method-summary %}

{% api-method-description %}
Çektiğiniz sunucunun online sayısını ve maksimum sayısını çekersiniz
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="Online" type="number" required=false %}
Suncudaki aktif kişi sayısını gösterir
{% endapi-method-parameter %}

{% api-method-parameter name="Maks" type="number" %}
Sunucunun maksimum sayısını gösterir
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Başarılı şekilde çektiniz
{% endapi-method-response-example-description %}

```
{"Maks":"22","Online":"7"}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Eğer bilgiler yanlışsa veya çekemiyorsa.
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
require("request")(`https://furtsy.wtf/api/oyun/${oyunid}/online/${ip}/${port}`, async function (err, resp, body) { 
body = JSON.parse(body); 
console.log("Online Kişi:" + `${body.Online}/${body.Maks}`)
})
```



