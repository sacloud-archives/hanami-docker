# hanami

## > Resource monitoring and hook for the SAKURA Cloud

[hanami](https://github.com/sacloud/hanami)用Dockerイメージ

## 使い方(dockerコマンドを直接使う場合)

### 起動コマンド書式

```bash
docker run -it --rm sacloud/hanami [オプション]
```

`hanami`コマンドの基本的な使い方は[Hanamiドキュメント](https://sacloud.github.io/hanami/)を参照してください。

### 実行例

必須パラメータ(さくらのクラウド[トークン、シークレット])をオプション指定しています。

```bash
docker run -it --rm sacloud/hanami --token "Your Token" --secret "Your Secret" 
```

パラメータは環境変数で渡すことも可能です。

```bash
docker run -it --rm -e SAKURACLOUD_ACCESS_TOKEN -e SAKURACLOUD_ACCESS_TOKEN_SECRET sacloud/hanami
```

## 使い方(whalebrewを使う場合)

```bash
# インストール
whalebrew install sacloud/hanami
# 実行(-e SAKURACLOUD_ACCESS_TOKEN -e SAKURACLOUD_ACCESS_TOKEN_SECRET -v $PWD:/workdir が指定されている状態となる)
hanami -h
```
