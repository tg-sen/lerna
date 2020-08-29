

# lerna環境を作成

[![lerna](https://img.shields.io/badge/maintained%20with-lerna-cc00ff.svg)](https://lerna.js.org/)

  npm i -g lerna 



### 既存パッケージに追加したnpmパッケージのグローバル化は
- devDependenciesがrootのpackage.jsonに集約される
    lerna link convert
- 未検証
    lerna import パッケージ名

### パッケージ追加は
    npx lerna create @kintone/rest-api-client

### yarn ワークスペースへのパッケージの追加はパッケージを指定して
    yarn workspace @kintone/rest-api-client add form-data

### 共通のパッケージの追加は -W を追加して
    yarn add -W --dev typescript prettier eslint

### 全てのパッケージに共通して実行するには
    lerna run "実行script"
