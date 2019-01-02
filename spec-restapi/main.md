# REST API 仕様(概要)


# 機能一覧 (αレベル)

## 公開エンドポイント

認証なしで使えるエンドポイント

* [Login](login.md) : `POST /api/@login`

## 認証が必要なエンドポイント

JWTの有効なTokenがHEADERに必要なエンドポイント

### ログインしているユーザに関係

ログインしているユーザ自身の情報表示や情報の更新:

* [登録情報を見る](user/get.md) : `GET /api/user/`
* [登録情報の更新](user/put.md) : `PUT /api/user/`

### アカウント関連

アカウントの操作を行う。管理者権限 `ANY_PERMISSION??` が必要:

* [アカウント一覧](accounts/get.md) : `GET /api/accounts/`
* [新規アカウントの作成](accounts/post.md) : `POST /api/accounts/`
* [アカウント情報を見る](accounts/pk/get.md) : `GET /api/accounts/:pk/`
* [アカウント情報を更新](accounts/pk/put.md) : `PUT /api/accounts/:pk/`
* [アカウントを削除](accounts/pk/delete.md) : `DELETE /api/accounts/:pk/`


### ルーム関連

ルームの操作を行う。ログインユーザ 権限 `ANY_PERMISSION??` が必要:

* [ルーム一覧]() : `GET /`
* [ルームを作る]() : `POST /`
* [ルームの設定を見る]() : `GET /`
* [ルームの設定を更新]() : `PATCH /`
* [ルームを削除]() : `DELETE /`
* [ルームに登録されているユーザ一覧]() : `GET /@share`
* [ルームに登録されているユーザを更新]() : `PATCH /@share`


### 投稿関連

投稿(計算)の実行や一覧を行う。ルーム登録ユーザ 権限 `ANY_PERMISSION??` が必要

* [投稿一覧]() : `GET /`
* [新規投稿]() : `POST /`
* [投稿の編集]() : `PATCH /`
* [投稿の削除]() : `DELETE /`



## 機能一覧 (βレベル)

TBD


