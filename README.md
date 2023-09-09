<img src="image/do_not_answer.png" alt="do_not_answer">

# Do-Not-Answer-Ja: A Dataset for Evaluating Safeguards in Japanse LLMs

## 概要
2023年8月にメルボルン大学から公開された安全性評価データセット『Do-Not-Answer』を日本語LLMの評価においても使用できるように日本語に自動翻訳し、さらに日本文化も考慮して修正したデータセット。本レポジトリではGPT4（gpt-4-0613）にて評価するコードも同封しています。
## Do-Not-Answerの特徴
- 5つのリスク領域とさらに細かい12のリスクカテゴリの観点でプロンプトを作成しLLM応答の安全性を包括的に評価できるように作成された全部で939レコードのデータセット
- データセットを使用して6つのLLMの応答を収集し、その応答が安全か否かを人間が評価
- 人間が安全性評価した結果と比較して、GPT4、Longformerでの評価結果も遜色ないものを得ることができ自動評価できることを確認
## Do-Not-Answer-Jaについて
メルボルン大学が公開しているデータセットを日本語にGoogle翻訳を用いて自動翻訳し、さらに自動翻訳の不自然さや日本文化を考慮した内容の修正を行い作成しました。
### HuggingFace

## 各種コードの説明
### get response
各LLMのresponse収集に使用したコード（コード整理中のため後日アップロードします）
### evaluate
評価データセットの指示に対するresponseをGPT4（gpt-4-0613）にて評価するコード
### get summary
xxxx_response_annotated.csvを読み込み、トータルでの評価結果および5つのリスク領域ごとの評価結果を集計するコード（コード整理中のため後日アップロードします）
## 評価結果
### Japanese LLM Safety Laederboard
|Model Name|Total|Ⅰ. Information Hazards|Ⅱ. Malicious Uses|Ⅲ. Discrimination, Exclusion, Toxicity, Hateful, Offensive|Ⅳ. Misinformation Harms|Ⅴ. Human-Chatbot Interaction Harms|
|:----|:----|:----|:----|:----|:----|:----|
|ELYZA-japanese-Llama-2-7b-instruct|0.892|0.883|0.893|0.852|0.897|0.966|
|japanese-stablelm-instruct-alpha-7b|0.785|0.871|0.737|0.693|0.761|0.872|
|bilingual-gpt-neox-4b-instruction-ppo|0.731|0.806|0.753|0.614|0.645|0.812|
### 各モデルの傾向
## ライセンス
レポジトリ内のコードについてはApache2.0、データセットについてはオリジナルデータセットのライセンスを継承しCC-BY-NC-SA4.0になります。
