---
title: Unreal での空間アンカー
description: Unreal で空間アンカーを使用するためのガイド
author: hferrone
ms.author: v-haferr
ms.date: 06/10/2020
ms.topic: article
ms.localizationpriority: high
keywords: Unreal, Unreal Engine 4, UE4, HoloLens, HoloLens 2, Mixed Reality, 開発, 機能, ドキュメント, ガイド, ホログラム, 空間アンカー
ms.openlocfilehash: 58394f4e27aff5070d55ed5f0d62cd81ff579d1f
ms.sourcegitcommit: 45da0a056fa42088ff81ccdd11232830fbe8430f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2020
ms.locfileid: "84720318"
---
# <a name="spatial-anchors-in-unreal"></a>Unreal での空間アンカー

## <a name="overview"></a>概要

空間アンカーは、アプリケーション セッション間で現実世界の空間にホログラムを保存するために使用されます。  これらは、Unreal では **ARPin** として示され、今後のセッションで読み込まれるように HoloLens のアンカー ストアに保存されます。 

## <a name="checking-the-anchor-store"></a>アンカー ストアの確認

アンカーを保存または読み込む前に、アンカー ストアの準備ができているかどうか確認する必要があります。  アンカー ストアの準備が整う前に、いずれかの HoloLens アンカー関数を呼び出すと、失敗します。  

![空間アンカー ストア準備完了](images/unreal-spatialanchors-store-ready.PNG)

## <a name="saving-anchors"></a>アンカーの保存

アプリケーションにコンポーネントがあり、それをワールドに固定する必要がある場合は、次のシーケンスを使用してアンカー ストアに保存できます。 

![空間アンカーの保存](images/unreal-spatialanchors-save.PNG)

次のように分類されます。
1. 既知の場所でアクターを生成します。
2. その場所とアクターのクラスに基づく名前を使用して、**ARPin** を作成します。 
3. アクターを **ARPin** に追加し、そのピンを HoloLens アンカー ストアに保存します。  
    * 選択するアンカー名は一意である必要があります。この例では現在のタイムスタンプを使用します。 

4. アンカーがアンカー ストアに正常に保存された場合、HoloLens デバイス ポータルの **[システム] > [Map manager]\(マップ マネージャー\) > [Anchor Files Saved On Device]\(デバイスに保存されたアンカー ファイル\)** でそのアンカーを調べることができます。 

## <a name="loading-anchors"></a>アンカーの読み込み

アプリケーションが起動すると、次のブループリントを使用して、コンポーネントをアンカー位置に復元できます。

![空間アンカーの読み込み](images/unreal-spatialanchors-load.PNG)

次のように分類されます。
1. アンカー ストア内のすべてのアンカーを反復処理します。 
2. ID でアクターを生成します。
3. そのアクターをアンカー ストアから **ARPin** にピン留めします。  

    * アンカーは、保存された位置に基づいてワールドにホログラムを再配置する必要があるため、ID に対してアクターを生成することが重要です。 ここで追加した変換によってアンカーにオフセットが追加されます。 

アンカーの保存された名前によって異なるアクターを生成できるように、アンカー ID も照会されます。 

## <a name="removing-anchors"></a>アンカーの削除 

アンカーが終了したら、**Remove ARPin from WMRAnchor Store** および **Remove All ARPins from WMRAnchor Store** コンポーネントを使用して個々のアンカーまたはアンカー ストア全体を削除することができます。

![空間アンカーの削除](images/unreal-spatialanchors-remove.PNG)

> [!NOTE]
> Spatial Anchors はまだベータ版であるため、最新の情報と機能を確認してください。

## <a name="see-also"></a>関連項目
* [空間アンカー](spatial-anchors.md)
* [座標系](coordinate-systems.md)
