# init
既存ディレクトリでローカルリポジトリの初期化を行う。

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

# commit
追跡している変更内容をローカルリポジトリへ記録する。

# status

Working tree の状態を表示する．

    $ git status

# fetch

他のリモートリポジトリから objects と refs をダウンロードする．

    $ git fetch [<options>] [<repository> [<refspec>...]]

全てのリモートリポジトリを fetch する．

    $ git fetch --all

フェッチした後，既にリモートリポジトリに存在しない追跡ブランチがあれば，それを削除する．

    $ git fetch -p

# pull

他のリモートリポジトリの内容を自分のローカルリポジトリに取り込む。デフォルトでは、git fetch した後、git merge する

# push

ローカルリポジトリの情報を、リモートリポジトリに反映する。

# checkout

checkoutは特定のブランチ又はリビジョンの内容にワークツリーを変更する

    $ git checkout [< branch >]

指定のブランチの最新にワークツリーを変更する

# add
追加や変更したファイルをコミット対象に含める。

# grep
指定のパターンにマッチする行を表示する。
検索対象は、　work tree, blobs。

# branch

ブランチを一覧する

# log

リビジョンログを表示する
リビジョンの番号と変更者名、日付、リビジョンメッセージを表示する

# gc
Gitローカルリポジトリ内のオブジェクトの圧縮や不要ファイルの削除

# reset
リビジョンを再設定を行う。

    $ git reset --soft
ワークツリーとインデックスを保持したまま、特定のリビジョンまでブランチを戻す

    $ git reset --mixed
インデックスを保持したまま、特定のリビジョンまでブランチを戻す。ワークツリーの内容は削除される

    $ git reset --head
全ての変更を破棄し特定のリビジョンまでブランチを戻す。

# diff
Show changes between commits, commit and working tree, etc
リビジョン間、リビジョンをworking treeの変更を表示する。

## Example

    $ git diff


origin/master との diff を表示する．

    $ git diff origin/master

# merge
2つかそれ以上の開発ヒストリーを統合する。

    $ git merge fixes enhancements

# filter-branch
履歴を大規模に変更する

例)

    $ git filter-branch --tree-filter <command>

プロジェクトの各チェックアウトに対して指定したコマンドを実行する

# clone
リモートリポジトリを新規ディレクトリにクローンする

ex.)    
    $ git clone git://git.kernel.org/pub/scm/.../linux.git my-linux    

# rebase
自分の祖先を付け替える

(master)  A ┬ B - C
(develop)　 └D[HAED]

    $ git rebase master

(master) A - B - C - D
