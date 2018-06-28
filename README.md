# Get offers

{% api-method method="get" host="http://{api\_domain}" path="/api/gateway/offers" %}
{% api-method-summary %}
Get Cakes
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="token" type="string" required=true %}
Api Token
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="number" required=false %}
Page
{% endapi-method-parameter %}

{% api-method-parameter name="limit" type="number" required=false %}
Limit
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
  "data": [
    {
      "id": 1026,
      "name": "LUCKY NUMBERS SERVICE-TH-DTAC",
      "tracking_url": "http://c0c.xyz/rest/ck/o/1/1026?click_id={click_id}&sub_id={YOUR_PUBLISHER_ID}&s1=1000060271&s5={source}",
      "payout_model": "CPA",
      "payout_type": "Fixed",
      "payout": "0.3200",
      "preview_url": "http://preview.adx.mob.cool/rest/o/preview/1026",
      "is_adult": false,
      "allow_incentive": false,
      "rating": 0,
      "description": "",
      "target": {
        "country": {
          "allow": [
            "TH"
          ],
          "deny": null
        },
        "carrier": {
          "allow": [
            {
              "country": "TH",
              "carrier": "dtac",
              "carrier_alias": [
                "dtac TriNet"
              ]
            }
          ],
          "deny": null
        },
        "device": {
          "allow": null,
          "deny": null
        },
        "connection_type": "Cellular"
      }
    },
    {
      "id": 1027,
      "name": "Unlimited Games-CM-Orange",
      "tracking_url": "http://c0c.xyz/rest/ck/o/1/1027?click_id={click_id}&sub_id={YOUR_PUBLISHER_ID}&s1=1000060271&s5={source}",
      "payout_model": "CPA",
      "payout_type": "Fixed",
      "payout": "0.1200",
      "preview_url": "http://preview.adx.mob.cool/rest/o/preview/1027",
      "is_adult": false,
      "allow_incentive": false,
      "rating": 0,
      "description": "",
      "target": {
        "country": {
          "allow": [
            "CM"
          ],
          "deny": null
        },
        "carrier": {
          "allow": [
            {
              "country": "CM",
              "carrier": "Orange",
              "carrier_alias": null
            }
          ],
          "deny": null
        },
        "device": {
          "allow": [
            "Other",
            "Android Phone",
            "Symbian"
          ],
          "deny": null
        },
        "connection_type": "All"
      }
    }
  ],
  "meta": {
    "pagination": {
      "total": 293,
      "count": 100,
      "per_page": 100,
      "current_page": 1,
      "total_pages": 3,
      "links": {
        "next": "http://{api_domain}/api/gateway/offers?limit=100&token=3df15eb0e9d75350fd400d71e742f01ed8bb4e81&page=2"
      }
    }
  }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "message": "Ain't no cake like that."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### Response

| Section | Parameters | Type | Description |
| --- | --- | --- | --- | --- | --- | --- | --- |
|  | id | uint64 | Identifies of this offer. |
|  | name | string | Name of this offer. |
|  | tracking\_url | string | Offer tracking url, you can go to your publisher console change query macros. |
|  | payout\_model | string | Payout model of this offer, Enum\(CPI, CPA, CPL, CPC, CPM, CPS\). |
|  | payout\_type | string | Payout type of this offer, Enum\(Fixed, Dynamic\). |
|  | payout | string | Payout of this offer, Only display on payout\_type equal to Fixed. |
|  | preview\_url | string | Preview url of this offer. |
|  | is\_adult | string | Preview url of this offer. |
|  | allow_incentive | string | Preview url of this offer. |
|  | rating | string | Preview url of this offer. |
|  | description | string | Preview url of this offer. |
| target | country | string | Preview url of this offer. |
| target | carrier | string | Preview url of this offer. |
| target | device | string | Preview url of this offer. |
| target | connection_type | string | Preview url of this offer. |


