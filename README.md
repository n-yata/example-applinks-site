# example-applinks-site

### firebaseでのアプリ生成
firebase cliがあること前提  
```
# フォルダ作成してその配下に初期リソース配置
$ mkdir example-link
$ cd example-link
$ firebase init hosting
# 作成したフォルダ内のpublic配下に.well-knownフォルダとファイルを配置後、デプロイ
# デプロイ時に聞かれる質問はすべてEnter
$ firebase deploy

# 削除する場合（your-site-idは Firebase Console の Hosting タブで確認）
$ firebase hosting:delete --site your-site-id
```

### abdでのdeeplink確認コマンド
adb shell 'am start -a android.intent.action.VIEW -c android.intent.category.BROWSABLE -d "https://my-project.web.app/details"' com.deeplink.cookbook

### ディープリンクの検証サイト
https://developers.google.com/digital-asset-links/tools/generator?hl=ja

### 補足
アプリの設定から「デフォルトで開く」を設定する

```
# firebase CLI の初期設定
$ firebase login
$ firebase login:list
$ firebase projects:list
$ firebase use --add
$ firebase use
```