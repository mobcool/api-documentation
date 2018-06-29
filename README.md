# Get offers

{% api-method method="get" host="http://{api\_domain}" path="/api/gateway/offers" %}
{% api-method-summary %}
Get Offers
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get all offers.
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
Offers successfully retrieved.
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
    },
    {
      "id": 5497,
      "name": "Cooking Craze - A Fast & Fun Restaurant Chef Game",
      "tracking_url": "http://c0c.xyz/rest/ck/o/1/5497?click_id={click_id}&sub_id={publisher_id}.{traffic_id}&sc={source}",
      "payout_model": "CPI",
      "payout_type": "Fixed",
      "payout": "0.4100",
      "preview_url": "",
      "conversion_flow": "",
      "is_adult": false,
      "allow_incentive": false,
      "rating": 0,
      "description": "Dash around the kitchen & serve food fast in this addictively fun cooking game!",
      "target": {
        "country": {
          "allow": [
            "US"
          ],
          "deny": null
        },
        "carrier": {
          "allow": null,
          "deny": null
        },
        "device": {
          "allow": [
            "Android Phone",
            "Android Tablet"
          ],
          "deny": null
        },
        "connection_type": "All"
      },
      "app": {
        "platform": "Android",
        "package_name": "com.bigfishgames.cookingcrazegooglef2p",
        "title": "Cooking Craze - A Fast & Fun Restaurant Chef Game",
        "icon_url": "https://lh3.googleusercontent.com/frpsUnXoy6n3VDJzTmDNacbEhFhgnPwrKT3z67JJZsS3F-5yFqpbBQ3WCeuNHciCyA=w150",
        "store_url": "",
        "rating": 4.5,
        "category": "Arcade",
        "min_os_version": "4.1",
        "size": "90521"
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Response

| Section | Parameters | Type | Description |
| --- | --- | --- | --- | --- | --- | --- | --- |
|  | id | Integer | Identifies of this offer. |
|  | name | String | Name of this offer. |
|  | tracking\_url | String | Offer tracking url, you can go to your publisher console change query macros. |
|  | payout\_model | String | Payout model of this offer, Enum\(CPI, CPA, CPL, CPC, CPM, CPS\). |
|  | payout\_type | String | Payout type of this offer, Enum\(Fixed, Dynamic\). |
|  | payout | String | Payout of this offer, Only display on payout\_type equal to Fixed. |
|  | preview\_url | String | Preview url of this offer. |
|  | is\_adult | Boolean | TRUE if this offer contains adult. |
|  | allow\_incentive | Boolean | TRUE if this offer is allowed in incentive mode. |
|  | rating | Float | Rating of the offer, Range: 0-5 |
|  | description | String | Description of offer. |
| target | country | Object | Contains allow and deny array: countries ISO code. |
| target | carrier | Object | Contains allow and deny array: country, carrier, carrier\_alias |
| target | device | Object | Contains allow and deny array: devices. |
| target | connection\_type | String | Enum\(All, Wifi, Cellular\). |
| app | platform | String | Os platform. Enum\(Android, iOS\) of this offer's app. |
| app | package\_name | String | Android package\_name or iOS bound\_id of this offer's app. |
| app | title | String | Title of this offer's app. |
| app | icon\_url | String | Icon url of this offer's app. |
| app | store\_url | String | Store url of this offer's app. |
| app | rating | String | Rating of this offer's app. |
| app | category | String | Category of this offer's app. |
| app | min\_os\_version | String | Min os version of this offer's app. |
| app | size | String | Size of this offer's app. |

#### Response\_Target\_Country

| Section | Parameters | Type | Description |
| --- | --- | --- |
|  | allow | StringArray | Allow countries ISO code.If allow is equal to null, It does allow any country. |
|  | deny | StringArray | Deny countries ISO code. If deny is equal to null, it does not deny any country. Deny countries only display on allow equal to null. |

#### Response\_Target\_Carrier

| Section | Parameters | Type | Description |
| --- | --- | --- | --- | --- | --- | --- |
| allow | country | String | Allow carrier's country ISO code. |
| allow | carrier | String | Allow carrier's name. |
| allow | carrier\_alias | StringArray | Allow carrier's alias. |
| deny | country | String | Deny carrier's country ISO code. |
| deny | carrier | String | Deny carrier's name. |
| deny | carrier\_alias | StringArray | Deny carrier's alias. |

#### Response\_Target\_Device

| Section | Parameters | Type | Description |
| --- | --- | --- |
|  | allow | StringArray | Allow devices.Enum\(Android Phone, Android Tablet, iPhone, iPad, Mac, PC, BlackBerry Phone, Blackberry Tablet, Windows Phone, Symbian, Feature Phone, Other\) |
|  | deny | StringArray | Deny devices.Enum\(Android Phone, Android Tablet, iPhone, iPad, Mac, PC, BlackBerry Phone, Blackberry Tablet, Windows Phone, Symbian, Feature Phone, Other\) |



