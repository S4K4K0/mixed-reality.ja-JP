---
title: 進行状況の表示
description: プログレス コントロールは、時間のかかる操作が進行中であることを示すフィードバックをユーザーに返します。
author: cre8ivepark
ms.author: dongpark
ms.date: 03/21/2018
ms.topic: article
keywords: Windows Mixed Reality、設計、コントロール、ui、ux
ms.openlocfilehash: d028b8717dae0e04a9a1104a8a4b7803023334ef
ms.sourcegitcommit: 6844930427b658ae31f642c395cd8a3b3cdbf857
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/07/2020
ms.locfileid: "75723211"
---
# <a name="progress-indicator"></a>進行状況インジケーター

<br>

<img src="images/UX/MRTK_ProgressIndicator.gif" alt="Progress ring example in HoloLens" width="940px">

プログレス コントロールは、時間のかかる操作が進行中であることを示すフィードバックをユーザーに返します。 使用されているインジケーターに応じて、進行状況インジケーターが表示されているときはユーザーはアプリを操作できないことを知らせたり、待ち時間の長さを示したりできます。

<br>

---

## <a name="types-of-progress"></a>プログレス コントロールの種類

何が起こっているかについてユーザー情報を提供することが重要です。 混合環境では、アプリから視覚的なフィードバックが得られない場合、ユーザーは物理環境またはオブジェクトによって簡単に気にすることができます。 データが読み込まれたりシーンが更新されたりするなど、数秒かかる状況では、視覚的なインジケーターを表示することをお勧めします。 操作が進行しているユーザーを表示するには、**進行状況バー**または**進行状況のリング**の2つのオプションがあります。

:::row:::
    :::column:::
        ### <a name="progress-barbr"></a>進行状況バー<br>
        進行状況バーには、タスクの完了率が表示されます。 このメソッドは、期間が既知 (有限) の操作中に使用する必要がありますが、進行中のユーザーとアプリとの対話をブロックすることはできません。<br>
        <br>
        *イメージ: HoloLens での進行状況バーの例*
    :::column-end:::
        :::column:::
        ![space](images/spacer-20x582.png)<br>
       HoloLens](images/640px-progressbar.jpg) の進行状況バーの例 ![<br>
    :::column-end:::
:::row-end:::

<br>

---

:::row:::
    :::column:::
        ### <a name="progress-ringbr"></a>進行状況リング<br>
        進行状況のリングは不確定な状態であるため、操作が完了するまで他のユーザー操作がブロックされたときに使用する必要があります。<br>
        <br>
        *イメージ: HoloLens での進行状況リングの例*
    :::column-end:::
        :::column:::
        ![space](images/spacer-20x582.png)<br>
       HoloLens](images/640px-progressring.jpg) での ![の進行状況リングの例<br>
    :::column-end:::
:::row-end:::

<br>

---

:::row:::
    :::column:::
        ### <a name="progress-with-a-custom-objectbr"></a>カスタムオブジェクトの進行状況<br>
        独自のカスタム 2D/3D オブジェクトを使用して進行状況の制御をカスタマイズすることで、アプリの個性とブランド id に追加できます。<br>
        <br>
        *イメージ: HoloLens でのカスタムメッシュの例の進行状況*
    :::column-end:::
        :::column:::
        ![space](images/spacer-20x582.png)<br>
       HoloLens](images/640px-progresscustom.jpg) でカスタムメッシュの例を使用して進行状況を ![<br>
    :::column-end:::
:::row-end:::

<br>

---

## <a name="best-practices"></a>ベスト プラクティス
* ユーザーが簡単にヘッドを空の領域に移動してコンテキストを失うことがあるため、 [billboarding またはタグ](billboarding-and-tag-along.md)を進行状況の表示に密に結合します。 ユーザーが何も表示できない場合、アプリがクラッシュしたように見えることがあります。 Billboarding とタグは、進行状況の prefab に組み込まれています。
* ユーザーに対して何が起こっているかに関するステータス情報を常に提供するのが適切です。 Progress prefab には、状態を提供するための Windows 標準のリングの種類の進行状況など、さまざまな視覚スタイルが用意されています。 また、進行状況のスタイルをアプリのブランドに合わせる必要がある場合は、アニメーションでカスタムメッシュを使用することもできます。

<br>

---

## <a name="progress-indicator-in-mrtk-mixed-reality-toolkit-for-unity"></a>Unity 用 MRTK (Mixed Reality Toolkit) の進行状況インジケーター

* [MRTK-進行状況インジケーター prefabs](https://github.com/microsoft/MixedRealityToolkit-Unity/tree/mrtk_release/Assets/MixedRealityToolkit.SDK/Features/UX/Prefabs/ProgressIndicators)
* [MRTK-シーン移行サービス](https://microsoft.github.io/MixedRealityToolkit-Unity/Documentation/Extensions/SceneTransitionService/SceneTransitionServiceOverview.html)


<br>

---

## <a name="see-also"></a>「

* [カーソル](cursors.md)
* [ハンド レイ](point-and-commit.md)
* [ボタン](button.md)
* [対話可能なオブジェクト](interactable-object.md)
* [境界ボックスとアプリ バー](app-bar-and-bounding-box.md)
* [操作](direct-manipulation.md)
* [ハンド メニュー](hand-menu.md)
* [メニューの近く](near-menu.md)
* [オブジェクト コレクション](object-collection.md)
* [音声コマンド](voice-input.md)
* [キーボード](keyboard.md)
* [ヒント](tooltip.md)
* [スレート](slate.md)
* [スライダー](slider.md)
* [シェーダー](shader.md)
* [Billboard と Tag-along](billboarding-and-tag-along.md)
* [進行状況を表示する](progress.md)
* [表面吸着](surface-magnetism.md)
