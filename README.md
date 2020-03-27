An implementation of transformer in PyTorch

## PyTorchで言語データを扱うには？
torchtextと呼ばれるライブラリを用いるのがよい。
よくある（テキスト, ラベル）で組になったデータを扱うには、

1. テキストデータ、ラベルデータに対し、行う処理を定義
2. `torchtext.data.TabularDataset`を用いtsvファイルを読み込み（多分csvでもいける？）

詳しくはutil.pyを参照。

## 
