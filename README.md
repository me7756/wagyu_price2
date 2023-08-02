# Git Lesson

## リモートリポジトリとローカルリポジトリとはそれぞれ何でしょうか？
- リモートリポジトリとは、専用のサーバーに配置して複数人で共有するためのリポジトリ。
- ローカルリポジトリとは、ユーザーひとりひとりが利用するために、手元のPC上に配置するリポジトリ

- Github以外のホスティングサービスとしてはBitbucket,GitLab,Gitbucket,Assemblaなどがある

## プッシュとマージの違いは何でしょうか？
- プッシュとは、自分の手元のローカルリポジトリの変更履歴をリモートリポジトリにアップロードすること
- マージとは、現在のブランチへ他のブランチの更新を取り込むこと。リモートリポジトリから最新情報をローカルリポジトリに持ってくることをfetchといい、fetchで持ってきた最新情報をmasterブランチに反映する際にもマージを使う


## コミットとプッシュの違い
- コミットは変更をローカルリポジトリに反映させること
- プッシュはローカルリポジトリの変更をリモートリポジトリに反映させること

## コミットのメッセージはどのように書いてあげるのが最適でしょうか？
- どんな編集を行ったのか正確に表し、ひと目でどんな変更を行ったのかわかるように書く
- コミットメッセージによく用いられるプレフィックスとしては、新機能の追加を表すfeat、修正を表すfix、ドキュメントの変更を表すdocs、コードのスタイル修正（セミコロンの追加など）を表すstyle、コードのリファクタリング（機能の変更なし）を表すrefactor、テストコードの追加や修正を表すtest、ビルドプロセスやツールの変更を表すchoreなどがある


## ローカルでマージするフローと、プルリクエストでマージするフローの違いは何でしょうか？
- git checkout で取り込みたい場所に移動しgit merge 取り込みたい対象 で取り込む
- レビューをしてもらい承認されたらリポジトリの管理者にマージをしてもらう

## コンフリクトを起こしてしまった場合、どう対処すべきですか？
- 先にマージされた変更内容を取り込むか、後にマージしようとしている変更内容を取り込む、もしくはどちらの変更内容も取り込む。取り込み作業が終わったらコンフリクト解決で行った作業内容をコミットする