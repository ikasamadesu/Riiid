# Riiid! Answer Correctness

## train.csv

- row_id : 列のidコード
- timestamp : ミリ秒でのユーザーインタラクションと操作完了の時間？
- user_id : ユーザーのID
- content_id : user interactionのID（出題とか？）
- content_type_id : 1はクイズ、0はレクチャー動画
- task_container_id : 質問のバッチ毎ID。例としては動画前に3問出題 = 同じIDを保有
- user_answer : ユーザーの回答。-1はnullを示す
- answered_correctly : 正解したか。-1はnullを示す
- prior_question_elapsed_time : 前質問の束で、回答にかかった時間の長さ平均（ミリ秒）間のレクチャー時間は無視
- prior_question_had_explanation : 回答後、説明と回答を見たか

## questions.csv

- question_id : 質問は0、content_id列の外部キー
- bundle_id : 一緒に出題されるコード（バンドルコード）
- correct_answer : 問題の正解（trainのは、ユーザーが選択した値）
- part : TOEICの関連セクション
- tags : 質問のタグコード。意味は未提供。

## lectures.csv

- lecture_id : 講義は1　tainのcontent_idの外部キー
- part : 講義のトップレベルカテゴリコード（？）
- tag : 講義にタグコード
- type_of : 講義の主な目的

A japanese translated notebook
https://www.kaggle.com/takiyu/japanese-riiid