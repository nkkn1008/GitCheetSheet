# init  
既存ディレクトリでリポジトリの初期化を行う。
>>>>>>> b0cc4c4d0c4ba32b28b201ec1b3b60532f3f8fc7

## fetch

全てのリモートを fetch する．

    $ git fetch --all

フェッチした後，既にリモートに存在しない追跡ブランチがあれば，それを削除する．

    $ git fetch -p

# git pull

他のリポジトリの内容を自分のリポジトリに取り込む。デフォルトでは、git fetch した後、get merge する

# push

ローカルリポジトリの情報を、リモートリポジトリに反映する。

# checkout

checkoutは特定のブランチ又はコミットの内容にワークツリーを変更する

### git checkout [< branch >]


指定のブランチの最新にワークツリーを変更する

# add
追加や変更したファイルをコミット可能にする。

# branch

ブランチを一覧する
