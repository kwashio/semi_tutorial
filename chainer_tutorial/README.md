# Chainer tutorial
ここでは、深層学習フレームワークChainerについてのチュートリアルを行います。
Chainerは可変長系列を直感的に扱えるのが特徴です。
まずは公式のイントロダクションを御覧ください。  
https://docs.chainer.org/en/stable/tutorial/basic.html  
上の内容を踏まえた上で、このチュートリアルでは主に機械翻訳で使われるEncoder−Decoder＋Attentionモデルを実装していきます。

## chainer_tutorial.ipynb
Chainerの特徴についておさらいし、モデルの書き方のテンプレート、今回用いるレイヤーの紹介を行います。

## Encoder-Decoder.ipynb
実際にEncoder−Decoderモデルを実装し、小規模なデータにちゃんとフィッティングできるかを確かめます。

## Encoder-Decoder_withAttention.ipynb
Encoder−DecoderモデルにAttentionを導入します。  
Attentionは一行で導入できるような機能はChainer側で用意されていないので、構造をしっかりと理解し、Chainerの関数を組み合わせて実装していきます。  


## 話さないこと

### GPUの使い方
今回はモデルの記述にフォーカスを当てたので、こちらは書いていません。  
Chainerを使ってGPUで計算を行うのは、公式にもチュートリアルがありますし、ググったら情報が出て来るので、そう難しくはありません。

### Trainer関係の使い方
公式のイントロダクションには出てくるTrainer。  
便利そうではあるのですがドキュメントもいまいち充実しておらず、一からソースを読む気力もなかったので、今回は端折っています。