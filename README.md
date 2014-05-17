# init
既存ディレクトリでリポジトリの初期化を行う。

# fetch

他のリポジトリから objects と refs をダウンロードする．

    $ git fetch [<options>] [<repository> [<refspec>...]]

全てのリモートを fetch する．

    $ git fetch --all

フェッチした後，既にリモートに存在しない追跡ブランチがあれば，それを削除する．

    $ git fetch -p

# pull

他のリポジトリの内容を自分のリポジトリに取り込む。デフォルトでは、git fetch した後、get merge する

# push

ローカルリポジトリの情報を、リモートリポジトリに反映する。

# checkout

checkoutは特定のブランチ又はコミットの内容にワークツリーを変更する

	$ git checkout [< branch >]

指定のブランチの最新にワークツリーを変更する

# add
追加や変更したファイルをコミット可能にする。

# grep
指定のパターンにマッチする行を表示する。
検索対象は、　work tree, blobs。

# branch

ブランチを一覧する

# log

コミットログを表示する
コミットの番号と変更者名、日付、コミットメッセージを表示する

# gc
Gitリポジトリ内のオブジェクトの圧縮や不要ファイルの削除
