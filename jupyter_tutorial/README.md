# Jupyter Notebookチュートリアル
ここでは、pythonの処理とデータの可視化・分析をよりインタラクティブに行えるJupyter Notebookというツールについて紹介します。

## インストール
Anacondaかpipが入っているならインストールは簡単です。
```bash
conda install jupyter
```
あるいは、
```bash
pip install jupyter
```
でインストールできます。

## 起動
```bash
jupyter notebook
```
とコマンド入力することで起動できます。  
自動的にwebブラウザに`Home`のタブが立ち上がると思います。

立ち上がらない場合は、`http://localhost:8888`に自分でアクセスしましょう。

## ノートブックを作る
右上の`New`から、`Notebooks > python2 or python3`で新しいノートブックが作ることができます。  
以降の説明はノートブックで行います。