# Anacondaチュートリアル
pythonのパッケージ管理ツールであるAnacondaをインストールし、
仮想環境の構築、ライブラリのインストール、仮想環境の切り替えなどを行います。

Anacondaの公式サイト  
https://www.anaconda.com/distribution/

Anacondaは各ユーザーが自分のホームディレクトリ直下でインストールし、自分のホームディレクトリ直下で仮想環境を構築できるのが特徴です。  
同じサーバー上で複数人が研究開発を行うとしても、python環境が各ユーザーのホームディレクトリ上で閉じるので、ユーザー間で同じpython環境を共有しなくてもよくなります。

Anacondaをインストールしてもいいのですが、必要十分以上なものがくっついてきてしまうので、
今回はMiniconda（必要最低限のツールパッケージ）をインストールしていきます。  
別にAnacondaでもいいです。特に手順は変わりません。

インストールの様子などは、以下のサイトを見たほうが正直わかりやすいです。  
[Anaconda を利用した Python のインストール](http://pythondatascience.plavox.info/pythonのインストール/anaconda-ubuntu-linux)

## Minicondaダウンロード
以下のサイトから各環境に対応するMinicondaインストーラをダウンロードします。  
https://conda.io/miniconda.html

自分のPCにインストールする場合はそれに対応するバージョン、研究用サーバー（Linux）にインストールする場合はそれに対応したバージョンをダウンロードしましょう。  

うちの研究用サーバーの場合は、Linux64-bitです。  
pythonのバージョンは3系で問題ないでしょう。  
2系を使いたい場合も、あとから仮想環境を構築して扱うことができます。

研究用サーバーにインストールする場合は、ダウンロードしたインストーラをscpでサーバーの自分のホーム直下に移すように。  
以降は研究用サーバーにインストールするという前提で進めていきます。

## Minicondaインストール
サーバーにsshして、lsなどでホーム直下に’Miniconda3-latest-Linux-x86_64.sh’があることを確認しましょう。  
確認できたら、以下のコマンドでMinicondaをインストールします。
```bash
bash Miniconda3-latest-Linux-x86_64.sh
```
これでインストールが始まるはずです。

途中、ライセンスが表示されると思うので、スペースキーなどでスクロールして'yes'を入力しましょう。

次にインストールする場所を尋ねられるはずなので、何も入力せずにEnterを押します。

最後に.bashrcの環境変数PATHにMinicondaの場所を追加するか尋ねられると思いますが、それも'yes'と入力しましょう。　　
ここでyesと入れ忘れた場合は、
```bash
echo 'export PATH=/home/{ユーザー名}/anaconda3/bin:$PATH' >> ~/.bashrc
```
で、PATHに環境変数を自分で追加します。{ユーザー名}には自分のユーザー名を入れること。  
私の場合は、
```bash
echo 'export PATH=/home/washio/anaconda3/bin:$PATH' >> ~/.bashrc
```
とります。

これでMinicondaのインストールが完了しました。  
一度ログアウトして再ログインするか、
```bash
source ~/.bashrc
```
で.bashrcを読み込んでください。

## 仮想環境の作成
