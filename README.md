

# lerna環境を作成

[![lerna](https://img.shields.io/badge/maintained%20with-lerna-cc00ff.svg)](https://lerna.js.org/)

## 始め方

  npm i -g lerna 
  npx lerna init


### 既存パッケージに追加したnpmパッケージのグローバル化は
- devDependenciesがrootのpackage.jsonに集約される
    lerna link convert
- 未検証
    lerna import パッケージ名

### npmパッケージ追加

#### lernaコマンドでの追加
    npx lerna create @kintone/rest-api-client

#### yarn ワークスペースへの追加はパッケージを指定して
    yarn workspace @kintone/rest-api-client add form-data

#### 共通のパッケージ追加は -W を追加して
    yarn add -W --dev typescript prettier eslint

### 全てのパッケージに対し、予め全パッケージに追加した実行scriptをを実行するには
    lerna run "実行script"


### パッケージ取り込み

    git clone git@github.com:sen-corporation/hoisys_note.git packages/note
    git clone git@github.com:sen-corporation/hoisys_manage.git packages/manage
    git clone git@github.com:sen-corporation/hoisys.git packages/hoisys
