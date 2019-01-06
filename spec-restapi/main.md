# REST API 仕様(概要)


# 機能一覧 (αレベル)

## 公開エンドポイント

認証なしで使えるエンドポイント

* [画像送信(麻雀牌14のオブジェクト取得)](image.md) : `POST /(db)/(container)/:room/@image`
* [点数計算](calc.md) : `GET /(db)/(container)/:room/:item/@calc`



# 機能一覧 (β1レベル)

## 公開エンドポイント

認証なしで使えるエンドポイント

* [Login](login.md) : `POST /db/container/@login`

## 認証が必要なエンドポイント

JWTの有効なTokenがHEADERに必要なエンドポイント


### ルーム関連

ルームの操作を行う。ログインユーザ 権限 `ANY_PERMISSION??` が必要:

* [ルーム一覧](rooms/get.md) : `GET /(db)/(container)`
* [ルームを作る](rooms/post.md) : `POST /(db)/(container)`
* [ルームの設定を見る](rooms/content/get.md) : `GET /(db)/(container)/(content)`
* [ルームの設定を更新](rooms/content/patch.md) : `PATCH /(db)/(container)/(content)`
* [ルームを削除](rooms/content/delete.md) : `DELETE /(db)/(container)/(content)`
* [ルームに登録されているユーザ一覧](rooms/content/sharing/get.md) : `GET /(db)/(container)/(content)/@sharing`
* [ルームに登録されているユーザを更新](rooms/content/sharing/post.md) : `POST /(db)/(container)/(content)/@sharing`


### 投稿関連

投稿(計算)の実行や一覧を行う。ルーム登録ユーザ 権限 `ANY_PERMISSION??` が必要

* [投稿一覧]() : `GET /(db)/(container)/(content)`
* [新規投稿]() : `POST /(db)/(container)/(content)`
* [投稿の編集]() : `PATCH /(db)/(container)/(content)/(item)`
* [投稿の削除]() : `DELETE /(db)/(container)/(content)/(item)`
* [画像アップロード]() : `PATCH /(db)/(container)/(content)/@upload/file`
* [画像ダウンロード]() : `GET /(db)/(container)/(content)/@download/file`  # TODO
* [投稿プッシュ]() : `GET /(db)/(container)/(content)/@message`


## 機能一覧 (β2レベル)

## 公開エンドポイント

認証なしで使えるエンドポイント

* TBD

## 認証が必要なエンドポイント

JWTの有効なTokenがHEADERに必要なエンドポイント

### ログインしているユーザに関係

ログインしているユーザ自身の情報表示や情報の更新:

* [登録情報を見る](user/get.md) : `GET /api/user/`
* [登録情報の更新](user/put.md) : `PUT /api/user/`

### アカウント関連

アカウントの操作を行う。管理者権限 `ANY_PERMISSION??` が必要:

* [アカウント一覧](accounts/get.md) : `GET /api/accounts/`
* [新規アカウントの作成](accounts/post.md) : `POST /db/container/users`
* [アカウント情報を見る](accounts/pk/get.md) : `GET /api/accounts/:pk/`
* [アカウント情報を更新](accounts/pk/put.md) : `PUT /api/accounts/:pk/`
* [アカウントを削除](accounts/pk/delete.md) : `DELETE /api/accounts/:pk/`

