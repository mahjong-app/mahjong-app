# ルーム一覧

閲覧可能なルームの一覧を返す

**URL** : `/(db)/(container)`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : TBD

**Data constraints** : `{}`

## Success Responses

**Condition** : 一つもルームが見れない場合

**Code** : `200 OK`

**Content** : `{[]}`

### OR

**Condition** : 一つ以上ルームが見れる場合

**Code** : `200 OK`

**Content** : 

```json
[
    {
    }
]
```