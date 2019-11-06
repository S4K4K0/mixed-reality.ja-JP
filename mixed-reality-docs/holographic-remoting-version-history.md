---
title: Holographic リモート処理のバージョン履歴
description: HoloLens 2 での Holographic リモート処理のバージョン履歴。
author: NPohl-MSFT
ms.author: nopohl
ms.date: 10/21/2019
ms.topic: article
keywords: HoloLens、リモート処理、Holographic リモート処理
ms.openlocfilehash: 75e7c276560b4efbbdcbf2ea7579ed5ad7aadb4d
ms.sourcegitcommit: 6bc6757b9b273a63f260f1716c944603dfa51151
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "73439233"
---
# <a name="holographic-remoting-version-history"></a><span data-ttu-id="643d5-104">Holographic リモート処理のバージョン履歴</span><span class="sxs-lookup"><span data-stu-id="643d5-104">Holographic Remoting Version History</span></span>

> [!IMPORTANT]
> <span data-ttu-id="643d5-105">このガイダンスは、HoloLens 2 の Holographic リモート処理に固有のものです。</span><span class="sxs-lookup"><span data-stu-id="643d5-105">This guidance is specific to Holographic Remoting on HoloLens 2.</span></span>

## <span data-ttu-id="643d5-106">バージョン 2.0.14 (2019 年10月26日)<a name="v2.0.14"></a></span><span class="sxs-lookup"><span data-stu-id="643d5-106">Version 2.0.14 (October 26, 2019) <a name="v2.0.14"></a></span></span>
* <span data-ttu-id="643d5-107">New PerceptionDevice Api のサポート (Windows 10 11 月2019更新プログラム)。</span><span class="sxs-lookup"><span data-stu-id="643d5-107">Support for new PerceptionDevice APIs (Windows 10 November 2019 Update).</span></span>
* <span data-ttu-id="643d5-108">SpatialGestureRecognizer によって保留中のジェスチャイベントがトリガーされない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="643d5-108">Fixed issue which prevent hold gesture events being triggered by SpatialGestureRecognizer.</span></span>
* <span data-ttu-id="643d5-109">SetBoundingVolume を使用するときの theading の問題を修正しています。</span><span class="sxs-lookup"><span data-stu-id="643d5-109">Fixed theading issue when using SpatialSurfaceObserver.SetBoundingVolume.</span></span>

## <span data-ttu-id="643d5-110">バージョン 2.0.12 (2019 年10月18日)<a name="v2.0.12"></a></span><span class="sxs-lookup"><span data-stu-id="643d5-110">Version 2.0.12 (October 18, 2019) <a name="v2.0.12"></a></span></span>
* <span data-ttu-id="643d5-111">NavigationRail (X/Y/Z) を使用するときの SpatialGestureRecognizer のクラッシュを修正します。</span><span class="sxs-lookup"><span data-stu-id="643d5-111">Fixed crash in SpatialGestureRecognizer when using NavigationRail(X/Y/Z).</span></span>

## <span data-ttu-id="643d5-112">バージョン 2.0.10 (2019 年10月10日)<a name="v2.0.10"></a></span><span class="sxs-lookup"><span data-stu-id="643d5-112">Version 2.0.10 (October 10, 2019) <a name="v2.0.10"></a></span></span>
* <span data-ttu-id="643d5-113">VR コントローラーの [トリガー] ボタンを使用するときのクラッシュを修正します。</span><span class="sxs-lookup"><span data-stu-id="643d5-113">Fixed crash when using trigger button of VR controllers.</span></span> <span data-ttu-id="643d5-114">Holographic リモート処理はコントローラーを完全にサポートしていません。 HoloLens 2 とペアになっている場合は、[トリガー] ボタンと [Windows] ボタンのみが動作します。</span><span class="sxs-lookup"><span data-stu-id="643d5-114">Holographic Remoting does not fully support controllers, only the trigger button and the Windows button are working if paired with HoloLens 2.</span></span>

## <span data-ttu-id="643d5-115">バージョン 2.0.9 (2019 年9月19日)<a name="v2.0.9"></a></span><span class="sxs-lookup"><span data-stu-id="643d5-115">Version 2.0.9 (September 19, 2019) <a name="v2.0.9"></a></span></span>
* <span data-ttu-id="643d5-116">[SpatialAnchorExporter](https://docs.microsoft.com/uwp/api/windows.perception.spatial.spatialanchorexporter)のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="643d5-116">Added support for [SpatialAnchorExporter](https://docs.microsoft.com/uwp/api/windows.perception.spatial.spatialanchorexporter)</span></span>
* <span data-ttu-id="643d5-117">次のメンバーを提供する新しいインターフェイス ```IPlayerContext2``` (```PlayerContext```によって実装されます) を追加しました。</span><span class="sxs-lookup"><span data-stu-id="643d5-117">Added new interface ```IPlayerContext2``` (implemented by ```PlayerContext```) providing the following members:</span></span>
  - <span data-ttu-id="643d5-118">[BlitRemoteFrameTimeout](holographic-remoting-create-player.md#BlitRemoteFrameTimeout)プロパティ。</span><span class="sxs-lookup"><span data-stu-id="643d5-118">[BlitRemoteFrameTimeout](holographic-remoting-create-player.md#BlitRemoteFrameTimeout)  property.</span></span>
* <span data-ttu-id="643d5-119">```Failed_RemoteFrameTooOld``` 値を ```BlitResult``` に追加しました</span><span class="sxs-lookup"><span data-stu-id="643d5-119">Added ```Failed_RemoteFrameTooOld``` value to ```BlitResult```</span></span>
* <span data-ttu-id="643d5-120">安定性と信頼性の向上</span><span class="sxs-lookup"><span data-stu-id="643d5-120">Stability and reliability improvements</span></span>

## <span data-ttu-id="643d5-121">バージョン 2.0.8 (2019 年8月20日)<a name="v2.0.8"></a></span><span class="sxs-lookup"><span data-stu-id="643d5-121">Version 2.0.8 (August 20, 2019) <a name="v2.0.8"></a></span></span>

* <span data-ttu-id="643d5-122">[IDXGISurface2](https://docs.microsoft.com/windows/win32/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) as パラメーターを指定して[HolographicCameraRenderingParameters](https://docs.microsoft.com/uwp/api/windows.graphics.holographic.holographiccamerarenderingparameters.commitdirect3d11depthbuffer)を呼び出すときのクラッシュを修正します。</span><span class="sxs-lookup"><span data-stu-id="643d5-122">Fixed crash when calling [HolographicCameraRenderingParameters.CommitDirect3D11DepthBuffer](https://docs.microsoft.com/uwp/api/windows.graphics.holographic.holographiccamerarenderingparameters.commitdirect3d11depthbuffer) with a [IDXGISurface2](https://docs.microsoft.com/windows/win32/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) as parameter.</span></span>
* <span data-ttu-id="643d5-123">安定性と信頼性の向上</span><span class="sxs-lookup"><span data-stu-id="643d5-123">Stability and reliability improvements</span></span>

## <span data-ttu-id="643d5-124">バージョン 2.0.7 (2019 年7月26日)<a name="v2.0.7"></a></span><span class="sxs-lookup"><span data-stu-id="643d5-124">Version 2.0.7 (July 26, 2019) <a name="v2.0.7"></a></span></span>

* <span data-ttu-id="643d5-125">HoloLens 2 の Holographic リモート処理の最初のパブリックリリース。</span><span class="sxs-lookup"><span data-stu-id="643d5-125">First public release of Holographic Remoting for HoloLens 2.</span></span>

## <a name="see-also"></a><span data-ttu-id="643d5-126">参照</span><span class="sxs-lookup"><span data-stu-id="643d5-126">See Also</span></span>
* [<span data-ttu-id="643d5-127">カスタム Holographic リモート処理プレーヤーアプリの作成</span><span class="sxs-lookup"><span data-stu-id="643d5-127">Writing a custom Holographic Remoting player app</span></span>](holographic-remoting-create-player.md)
* [<span data-ttu-id="643d5-128">Holographic Remoting ホストアプリの作成</span><span class="sxs-lookup"><span data-stu-id="643d5-128">Writing a Holographic Remoting host app</span></span>](holographic-remoting-create-host.md)
* [<span data-ttu-id="643d5-129">Holographic リモート処理のトラブルシューティングと制限事項</span><span class="sxs-lookup"><span data-stu-id="643d5-129">Holographic Remoting troubleshooting and limitations</span></span>](holographic-remoting-troubleshooting.md)
* [<span data-ttu-id="643d5-130">Holographic Remoting ソフトウェア ライセンス条項</span><span class="sxs-lookup"><span data-stu-id="643d5-130">Holographic Remoting software license terms</span></span>](https://docs.microsoft.com/legal/mixed-reality/microsoft-holographic-remoting-software-license-terms)
* [<span data-ttu-id="643d5-131">Microsoft のプライバシーに関する声明</span><span class="sxs-lookup"><span data-stu-id="643d5-131">Microsoft Privacy Statement</span></span>](https://go.microsoft.com/fwlink/?LinkId=521839)