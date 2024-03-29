# light-api-server

## 特徴

- 依存パッケージがありません。
- ~~テストもしっかりあります。~~
  - ごめんなさい書けませんでした。（非同期を倒せず・・・）

## 動かし方

- 以下で起動します。

```yarn
yarn start
```

- 以下でテスト実行できます。（ただしうまく動きません）

```yarn
yarn test
```

## 使い方

設定類は全部 config.json で行うようにしています。

```json
{
  "port": 3000,
  "resources": ["fruit", "meat"]
}
```

| Key       | Value                                  |
| --------- | -------------------------------------- |
| port      | 起動用のポートです。                   |
| resources | リソースです。配列で設定してください。 |

## アクセス方法

上記の例だと、fruit と meat のリソースが定義されています。

| Do           | Method | URI         |
| ------------ | ------ | ----------- |
| Create       | POST   | /fruit      |
| Read(ALL)    | GET    | /fruit      |
| Read(SEARCH) | GET    | /fruit?id=1 |
| Update       | POST   | /fruit?id=1 |
| Delete       | DELETE | /fruit?id=1 |

## docker-compose

docker-compose を用意しました。
以下コマンドで実行、終了できます。

```bash
# 起動
docker-compose up -d

# 終了
docker-compose down
```
