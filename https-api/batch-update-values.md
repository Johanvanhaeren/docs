---
description: >-
  If you need your values to have the same timestamp you can use the following
  format
---

# Batch Update Values

{% api-method method="get" host="https://blynk.cloud" path="/external/api/batch/update?token={token}&{pin1}={value1}&{pin2}={value2}" %}
{% api-method-summary %}
Batch update
{% endapi-method-summary %}

{% api-method-description %}
**Example:**  
`https://blynk.cloud/external/api/update?token=bFFtSHNCZZDWQ__Zs96cP5jLMhLoJofg&pin=v0&value=33.00&value=44.00`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="token" type="string" required=false %}
auth token of the device
{% endapi-method-parameter %}

{% api-method-parameter name="pin" type="string" required=true %}
virtual pin
{% endapi-method-parameter %}

{% api-method-parameter name="value" type="string" required=true %}
the value will be parsed as the   
Datastream data type \(int, double, string
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

