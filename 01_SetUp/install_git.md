## Git のインストールと基本設定

ここではコマンドラインで`git`コマンドを使用できるようにするために
gitのインストールの仕方と、基本設定の仕方を説明します。

自分はWindowsユーザーですが、基本的な操作はどのOSでもほとんど同じなので、
MacやLinuxユーザーの方でも問題ないです。

### 1 gitのインストール

1. [こちら](https://git-scm.com/downloads)のサイトにアクセスをして自分のOS環境の環境を選択しインストールを開始します

2. インストールができたら`git`コマンドが使えるか確認します
次のコマンドを打って結果が返されればgitが正常にインストールされています

```powershell

git -v

>> git version 2.38.0.windows.1
```

上記の結果が返ってこなかった場合

- PCの再起動をしてみる<br>
<t>インストールできてもその変更がpcに反映されていないことがあります。<br>
<t>pcの本体を再起動してもう一度上記のコマンドを実行します

- 環境変数を確認してみる<br>
<t>再起動しても治らなかった場合`git`コマンドの実行ファイルがpcの環境変数に登録されていない可能性があります。<br>
<t>システムの環境変数を確認し、`git`の実行ファイルのパスが保存されているか確認します
                        
### 2 Gitの基本設定

gitをインストールできたら`ユーザー名`と`メールアドレス`を設定します。<br>
これはすべてのgitコミットにこの情報が用いられます

コマンド操作、GUI操作のどちらかで設定が可能ですが、今回はコマンド操作で行います
`git config`で設定することができます

```powershell

git config --global user.name "<your name>"
git config --global user.email <your email>

```

できたら確認をします

```powershell
git config user.name
>> <your name>

git config user.email
>> <your email>
```

結果が返ってきたら設定完了です。
その他の設定は[git公式サイトのドキュメント](https://git-scm.com/book/ja/v2/%E4%BD%BF%E3%81%84%E5%A7%8B%E3%82%81%E3%82%8B-%E6%9C%80%E5%88%9D%E3%81%AEGit%E3%81%AE%E6%A7%8B%E6%88%90)を参考にしてみてください
