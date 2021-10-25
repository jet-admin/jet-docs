[comment]: # ($page_title=HTTP requests API)

{% api-method method="post" host="https://" path="api.jetadmin.io/api/proxy\_request/" %}
{% api-method-summary %}
Send request through Jet Admin proxy
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
JWT eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJ0b2tlbl9Cfb....
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="project" type="string" required=true %}
Project unique name
{% endapi-method-parameter %}

{% api-method-parameter name="environment" type="string" required=true %}
Environment unique name \(default is prod\)
{% endapi-method-parameter %}

{% api-method-parameter name="resource" type="string" required=false %}
Resource unique name
{% endapi-method-parameter %}

{% api-method-parameter name="method" type="string" required=true %}
HTTP method \(GET, POST, PUT, PATCH, DELETE, etc.\)
{% endapi-method-parameter %}

{% api-method-parameter name="url" type="string" required=true %}
HTTP URL
{% endapi-method-parameter %}

{% api-method-parameter name="query\_params" type="array" required=false %}
JSON formatted array, for example:  
\[{"foo":"q","value":"bar"}\]
{% endapi-method-parameter %}

{% api-method-parameter name="headers" type="array" required=false %}
JSON formatted array, for example:  
\[{"name":"Authorization","value":"Header {-sso.9b4348ec965d4c68818aec4e15dc536f.access\_token-}"}\] 
{% endapi-method-parameter %}

{% api-method-parameter name="body\_type" type="string" required=false %}
Body type \(JSON, GraphQL, FormUrlEncoded, FormData, Raw\)
{% endapi-method-parameter %}

{% api-method-parameter name="body" type="string" required=false %}
Body depending on selected Body type
{% endapi-method-parameter %}

{% api-method-parameter name="secret\_tokens" type="string" required=false %}
Comma separated list of used secret tokens, for example:  
sso.9b4348ec965d4c68818aec4e15dc536f.access\_token
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Response returned by provided HTTP URL
{% endapi-method-response-example-description %}

```
[any data]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

