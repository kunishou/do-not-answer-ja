# Do-Not-Answer-Ja: A Dataset for Evaluating Safeguards in Japanse LLMs

## 概要
2023年8月にメルボルン大学から公開された安全性評価データセット『Do-Not-Answer』を日本語LLMの評価においても使用できるように翻訳、修正したデータセット。本レポジトリではGPT4（xxxx）での評価するコードを同封している。
## Do-Not-Answerの特徴
- 5つのリスク領域と12の危険性の観点でLLM応答の安全性を評価できるように作成された939レコードのデータセット
- データセットを使用して6つのLLMの応答を収集し、その応答が安全か否かを人間が評価
- 人間が安全性評価した結果と比較して、GPT4、Longformerでの評価結果も遜色ないものを得ることができ自動評価できることを確認
## Do-Not-Answer-Jaについて
### 作成方法
### HuggingFace
## 各種コードの説明
### get response
### evaluate
### get summary
## 評価結果
### Japanese LLM Safety Laederboard
### 各モデルの傾向
## ライセンス
レポジトリ内のコードについてはApache2.0，データセットについてはオリジナルデータセットのライセンスを継承しCC-BY-NC-SA4.0
