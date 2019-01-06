# 点数計算

麻雀牌14の情報を元に、点数を返す

**URL** : `/(db)/(container)/:room/:item/@calc`

**URL Parameters** : 

* `room=[string]` room は、固定値の予定 TBD
* `item=[string]` item は、送信された画像のID TBD


**Method** : `GET`

**Auth required** : NO

**Permissions required** : TBD

**Data constraints** : 

```json
{
    "name": "Build something project dot com"
}
```

## Success Responses

**Condition** : 計算が成功した場合

**Code** : `200 OK`

**Content** : 

```json
[
    {
    }
]
```

## Error Responses

**Condition** : 入力値にエラーがある場合

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "name": [
        "This field is required."
    ]
}
```
