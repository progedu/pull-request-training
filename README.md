# gitコマンド
## １行で表示する
```
git log --oneline
```
## ファイル指定で変更差分を表示する
```
git log -p index.html
```
## 表示するコミット数を制限する
```
git log -n <コミット数>
```
## ローカルとリポジトリからファイルを削除する
```
git rm <ファイル名>
git rm -r <ディレクトリ名>
```
## リモートリポジトリ（github）を新規追加する
```
originというショートカットでurlのリモートリポジトリを登録する
git remote add origin htttps://github.com/user/repo.git
```
## ステージした変更を取り消す
- ステージから取り消すだけなので、ローカルのファイルには影響を与えない
```
git reset HEAD <ファイル名>
git reset HEAD <ディレクトリ名>

全変更を取り消す
git reset HEAD .
```
## リモートから情報をローカルに取得する 　ワークツリーには反映されない
```
git fetch <リモート名>
git fetch origin
ワークツリーに反映する場合は、
git merge <反映するブランチ名>
```
## fetch + merge = pull （注意：pullのときにマージされるのは今いるブランチ）
```
git pull
```
## ブランチの一覧を表示する
```
すべてのブランチを表示する（リモートブランチも）
git branch -a 
```
## ブランチを切り替える
```
ブランチを切り替える
git checkout <既存ブランチ名>
ブランチを新規作成して切り替える
git checkout -b <新ブランチ名>
```
