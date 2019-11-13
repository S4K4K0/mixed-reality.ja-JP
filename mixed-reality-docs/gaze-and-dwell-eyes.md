---
title: 目の視線入力とドウェル
description: 目の視線入力とドウェル入力モデルの概要
author: sostel
ms.author: sostel
ms.date: 10/29/2019
ms.topic: article
ms.localizationpriority: high
keywords: 視線追跡, Mixed Reality, 入力, 目の視線入力, 目のターゲット設定, HoloLens 2, 視線に基づく選択, ドウェル
ms.openlocfilehash: 0ec5d5e3b7f56038c7be9930a4468d286b388a65
ms.sourcegitcommit: 2cf3f19146d6a7ba71bbc4697a59064b4822b539
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/12/2019
ms.locfileid: "73926609"
---
# <a name="eye-gaze-and-dwell"></a>目の視線入力とドウェル

_"目の視線入力とドウェル"_ 操作モデルは、[目の視線入力とコミット](gaze-and-commit.md)操作モデルの特殊なケースです。
1. ターゲットを見つめるだけ 
2. そのターゲットを選択するという意図を示すために、次のように明示的なセカンダリ入力を実行します。_選択するターゲットをただ見つめ続ける_。

## <a name="advantages-of-the-eye-gaze-and-dwell-interaction-model"></a>"目の視線入力とドウェル" 操作モデルの利点 
タスクやツールの保持などで既に手がふさがっている場合、ホログラムの操作に手を使えないことがあります。
ホログラム選択のためのハンズフリーな代替操作として、"目の視線入力とドウェル" があります。これは、言い換えるなら、 _"見てから、見つめ続ける"_ ことです。 このアプローチの利点は、頭や体を十分に動かすことのできない非常に制約のあるユーザーであっても、ホログラムを操作できることです (非常に狭い作業環境など)。
ユーザーが選択したいターゲットを見つめ続けるだけで、プロセスを示す別のドウェル フィードバックが表示されます。


## <a name="challenges-of-the-eye-gaze-and-dwell-interaction-model"></a>"目の視線入力とドウェル" 操作モデルの課題
一般的には、ドウェル ベースのアクティブ化は、音声入力もハンド入力も利用できない場合の最後のフォールバックとしてのみ使用することをお勧めします。 これは、ドウェル時間の選択がかなり難しい場合があるためです。 初級ユーザーはドウェル時間が長くても問題ないのに対し、上級ユーザーはエクスペリエンスをすばやく効率的にナビゲートすることを好みます。 その結果、ユーザーの特定のニーズに合わせてドウェル時間を調整することが困難になります。
ドウェル時間が短すぎる場合:ホログラムが目の視線入力すべてに反応してしまい、ユーザーが当惑する可能性があります。 ドウェル時間が長すぎる場合:ユーザーが長時間ターゲットを見つめ続けなければならないため、エクスペリエンスが遅すぎてスムーズさが足りないと感じる可能性があります。

## <a name="design-recommendations"></a>設計の推奨事項
ドウェル フィードバックには、ツー ステート アプローチを使用することをお勧めします。
1. *開始遅延*:ユーザーがターゲットを見つめ始めても、すぐには何も生じません。これは、すぐ何かが生じると、ユーザー エクスペリエンスが不快で当惑させるものになる可能性があるためです。 代わりに、タイマーが起動して、ユーザーが意図的にそのターゲットを注視しているのか、単にその上を目線が移動しただけなのかを検出します。
2. *ドウェル フィードバックの開始:* ユーザーが意図的にそのターゲットを注視していることが確認されると、ドウェル フィードバックが表示され、ドウェルのアクティブ化が開始されようとしていることがユーザーに通知されます。 150 から 250 ミリ秒の開始時間を、特定の近接度で (ユーザーが大きなターゲットを注視しているか見回しているか) 指定することをお勧めします。  
3. *継続的なフィードバック:* ユーザーがターゲットを見つめ続けている間、継続進行状況インジケーターが表示されるので、ユーザーはそのターゲットを見つめ続ける必要があることがわかります。 特に目の視線入力の場合は、大きめの円や球がまず表示され、その円や球が収縮して小さくなるようにすることにより、_ユーザーの視覚的注意を引く_ことをお勧めします。 最終状態 (小さい円) のインジケーターを表示することで、ドウェルが完了するタイミングをユーザーに知らせることができます。 サンプル図を次に示します。 
4. *完了:* ユーザーがターゲットを注視し続けると (さらに 650 から 850 ミリ秒)、ドウェルのアクティブ化が完了し、見つめていたターゲットが選択されます。

![ドウェルの状態](images/eyes_dwellstate_recommendation.png)<br>

## <a name="see-also"></a>関連項目
* [視線追跡](eye-tracking.md)
* [目の視線入力とコミット](gaze-and-commit-eyes.md)
* [視線入力とコミット](gaze-and-commit.md)
* [視線入力とドウェル](gaze-and-dwell.md)
* [音声入力](voice-design.md)