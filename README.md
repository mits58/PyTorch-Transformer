An implementation of transformer in PyTorch

## PyTorchで言語データを扱うには？
torchtextと呼ばれるライブラリを用いるのがよい。
よくある（テキスト, ラベル）で組になったデータを扱うには、

1. テキストデータ、ラベルデータに対し、行う処理を定義
2. `torchtext.data.TabularDataset`を用いtsvファイルを読み込み（多分csvでもいける？）

詳しくはutil.pyを参照。

## 忘れがちなword2vecによるベクトル表現方法の詳細
「ある単語の表現は、その周囲によく出てくる単語の表現と類似している」という考えがもとになっている。

実際にベクトル表現を行う手法としては大きく2つ。

1. Continuous Bag-of-Words (CBoW)
2. Skip-gram

### CBowについて
1. まずは、大量のテキストをそれぞれ単語分割。
  - 例えば「」
