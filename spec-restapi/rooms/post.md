# ルームを作る

新規にルームを作る。


**URL** : `/(db)/(container)`

**Method** : `POST`

**Auth required** : YES

**Permissions required** : TBD

**Data constraints**

Provide name of Account to be created.

```json
{
    "name": "[unicode 64 chars max]"
}
```

**Data example** All fields must be sent.

```json
{
    "name": "Build something project dot com"
}
```

## Success Response

**Condition** : ルームの作成成功

**Code** : `201 CREATED`

**Content example**

```json
{
    "id": 123,
    "name": "Build something project dot com",
    "url": "http://testserver/api/accounts/123/"
}
```

## Error Responses

**Condition** : すでに同じIDでルームがある場合

**Code** : `303 SEE OTHER`

**Headers** : `Location: http://testserver/api/accounts/123/`

**Content** : `{}`

### Or

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