# init
既存ディレクトリでリポジトリの初期化を行う。

	$ git init --template <template-directory>

他のディレクトリをテンプレートとして使う

# config
設定コマンド

### author 設定
    $ git config --global user.name "hoge fuga"
    $ git config --global user.email hoge.fuga@piyo.com

### エディター設定
    $ git config --global core.editor emacs

などなど


##

# commit
追跡している変更内容をリポジトリへ記録する。

# status

Working tree の状態を表示する．

    $ git status

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

# reset
コミットを再設定を行う。

	$ git reset --soft
ソフト

	$ git reset --mixed
ミックス

	$ git reset --head
ハード

# diff
Show changes between commits, commit and working tree, etc
コミット間、コミットをworking treeの変更を表示する。

## Example

    $ git diff


# merge
2つかそれ以上の開発ヒストリーを統合する。

    $ git merge fixes enhancements

# filter-branch
履歴を大規模に変更する

例)
    $ git filter-branch --tree-filter <command>

プロジェクトの各チェックアウトに対して指定したコマンドを実行する

