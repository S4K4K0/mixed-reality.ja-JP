---
title: Unity 開発の概要
description: 構築の作業開始の複合現実アプリ Unity でします。
author: thetuvix
ms.author: alexturn
ms.date: 03/21/2018
ms.topic: article
keywords: Unity では、実際には、開発、作業の開始、新しいプロジェクト、移植、機能、カメラ、シミュレーション、エミュレーション、ドキュメントの混在
ms.openlocfilehash: fc40ef4eae31cf22f640be2666c5af3afb717ff3
ms.sourcegitcommit: 384b0087899cd835a3a965f75c6f6c607c9edd1b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/12/2019
ms.locfileid: "59604548"
---
# <a name="unity-development-overview"></a><span data-ttu-id="04692-104">Unity 開発の概要</span><span class="sxs-lookup"><span data-stu-id="04692-104">Unity development overview</span></span>

<span data-ttu-id="04692-105">最も高速パスのビルド方法、 [mixed reality アプリ](app-views.md)は[Unity](http://aka.ms/HoloLensUnity)。</span><span class="sxs-lookup"><span data-stu-id="04692-105">The fastest path to building a [mixed reality app](app-views.md) is with [Unity](http://aka.ms/HoloLensUnity).</span></span> <span data-ttu-id="04692-106">探索する時間を取ることをお勧めします。、 [Unity チュートリアル](https://unity3d.com/learn/tutorials)します。</span><span class="sxs-lookup"><span data-stu-id="04692-106">We recommend you take the time to explore the [Unity tutorials](https://unity3d.com/learn/tutorials).</span></span> <span data-ttu-id="04692-107">Unity が包括的で資産が必要な場合[Asset Store](https://www.assetstore.unity3d.com/)します。</span><span class="sxs-lookup"><span data-stu-id="04692-107">If you need assets, Unity has a comprehensive [Asset Store](https://www.assetstore.unity3d.com/).</span></span> <span data-ttu-id="04692-108">アクセスすることができます、Unity の基本的な知識を蓄積した後、 [Mixed Reality Academy](academy.md)を Unity での複合現実開発の詳細を参照してください。</span><span class="sxs-lookup"><span data-stu-id="04692-108">Once you have built up a basic understanding of Unity, you can visit the [Mixed Reality Academy](academy.md) to learn the specifics of mixed reality development with Unity.</span></span> <span data-ttu-id="04692-109">参照してください、 [Unity Mixed Reality フォーラム](http://forum.unity3d.com/forums/hololens.102/)が発生する問題の解決策を見つけて、コミュニティの構築、Unity での複合現実アプリの残りの部分とかかわります。</span><span class="sxs-lookup"><span data-stu-id="04692-109">Be sure to visit the [Unity Mixed Reality forums](http://forum.unity3d.com/forums/hololens.102/) to engage with the rest of the community building mixed reality apps in Unity and find solutions to problems you might run into.</span></span>

## <a name="porting-an-existing-unity-app-to-windows-mixed-reality"></a><span data-ttu-id="04692-110">Windows Mixed Reality への既存の Unity アプリの移植</span><span class="sxs-lookup"><span data-stu-id="04692-110">Porting an existing Unity app to Windows Mixed Reality</span></span>

<span data-ttu-id="04692-111">Windows Mixed Reality を移植する既存の Unity プロジェクトを使用する場合はと共にに従って、 [Unity 移植のガイド](porting-guides.md)を開始します。</span><span class="sxs-lookup"><span data-stu-id="04692-111">If you have an existing Unity project that you're porting to Windows Mixed Reality, follow along with the [Unity porting guide](porting-guides.md) to get started.</span></span>

## <a name="configuring-a-new-unity-project-for-windows-mixed-reality"></a><span data-ttu-id="04692-112">Windows Mixed Reality を新しい Unity プロジェクトを構成します。</span><span class="sxs-lookup"><span data-stu-id="04692-112">Configuring a new Unity project for Windows Mixed Reality</span></span>

<span data-ttu-id="04692-113">まず、Unity を使用した複合現実アプリの構築を開始する[ツールをインストールする](install-the-tools.md)します。</span><span class="sxs-lookup"><span data-stu-id="04692-113">To get started building mixed reality apps with Unity, first [install the tools](install-the-tools.md).</span></span> <span data-ttu-id="04692-114">HoloLens ではなく Windows Mixed Reality イマーシブ ヘッドセットする対象とするが場合、は、ここでは、Unity の特別なバージョンを必要があります。</span><span class="sxs-lookup"><span data-stu-id="04692-114">If you'll be targeting Windows Mixed Reality immersive headsets rather than HoloLens, you'll need a special version of Unity for now.</span></span>

<span data-ttu-id="04692-115">新しい Unity プロジェクトをいま作成した場合は、少数の Unity の設定の 2 つのカテゴリに分類、Windows Mixed Reality を変更する必要があります。 プロジェクトごとおよびシーンごと。</span><span class="sxs-lookup"><span data-stu-id="04692-115">If you've just created a new Unity project, there are a small set of Unity settings you'll need to change for Windows Mixed Reality, broken down into two categories: per-project and per-scene.</span></span>

### <a name="per-project-settings"></a><span data-ttu-id="04692-116">プロジェクトの設定</span><span class="sxs-lookup"><span data-stu-id="04692-116">Per-project settings</span></span>

<span data-ttu-id="04692-117">Windows Mixed Reality を対象とは、まず、ユニバーサル Windows プラットフォーム アプリとしてエクスポートする Unity プロジェクトを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04692-117">To target Windows Mixed Reality, you first need to set your Unity project to export as a Universal Windows Platform app:</span></span>
1. <span data-ttu-id="04692-118">選択**ファイル > の設定を作成しています.**</span><span class="sxs-lookup"><span data-stu-id="04692-118">Select **File > Build Settings...**</span></span>
2. <span data-ttu-id="04692-119">選択**ユニバーサル Windows プラットフォーム**、プラットフォームに一覧表示し、クリックして**スイッチ プラットフォーム**</span><span class="sxs-lookup"><span data-stu-id="04692-119">Select **Universal Windows Platform** in the Platform list and click **Switch Platform**</span></span>
3. <span data-ttu-id="04692-120">設定**SDK**に**ユニバーサル 10**</span><span class="sxs-lookup"><span data-stu-id="04692-120">Set **SDK** to **Universal 10**</span></span>
4. <span data-ttu-id="04692-121">設定**ターゲット デバイス**に**任意のデバイス**イマーシブ ヘッドセットをサポートするかに切り替えてに**HoloLens**</span><span class="sxs-lookup"><span data-stu-id="04692-121">Set **Target device** to **Any Device** to support immersive headsets or switch to **HoloLens**</span></span>
5. <span data-ttu-id="04692-122">設定**ビルドの種類**に**D3D**</span><span class="sxs-lookup"><span data-stu-id="04692-122">Set **Build Type** to **D3D**</span></span>
6. <span data-ttu-id="04692-123">設定**UWP SDK**に**インストールされている最新**</span><span class="sxs-lookup"><span data-stu-id="04692-123">Set **UWP SDK** to **Latest installed**</span></span>

<span data-ttu-id="04692-124">Unity エクスポートしようとしましたが、アプリが作成することを把握できるようにする必要があります、[没入型ビュー](app-views.md) 2D ビューではなく。</span><span class="sxs-lookup"><span data-stu-id="04692-124">We then need to let Unity know that the app we are trying to export should create an [immersive view](app-views.md) instead of a 2D view.</span></span> <span data-ttu-id="04692-125">そのために、「仮想現実サポート」を有効にします。</span><span class="sxs-lookup"><span data-stu-id="04692-125">We do that by enabling "Virtual Reality Supported":</span></span>
1. <span data-ttu-id="04692-126">**ビルド設定しています.** ウィンドウを開いて、**プレーヤー設定しています.**</span><span class="sxs-lookup"><span data-stu-id="04692-126">From the **Build Settings...** window, open **Player Settings...**</span></span>
2. <span data-ttu-id="04692-127">選択、**ユニバーサル Windows プラットフォームの設定** タブ</span><span class="sxs-lookup"><span data-stu-id="04692-127">Select the **Settings for Universal Windows Platform** tab</span></span>
3. <span data-ttu-id="04692-128">展開、 **XR 設定**グループ</span><span class="sxs-lookup"><span data-stu-id="04692-128">Expand the **XR Settings** group</span></span>
4. <span data-ttu-id="04692-129">**XR 設定** セクションで、チェック、**仮想現実サポート**を追加するチェック ボックスをオン、**仮想現実デバイス**一覧。</span><span class="sxs-lookup"><span data-stu-id="04692-129">In the **XR Settings** section, check the **Virtual Reality Supported** checkbox to add the **Virtual Reality Devices** list.</span></span>
5. <span data-ttu-id="04692-130">**XR 設定**グループで、ことを確認します **"Windows Mixed Reality"** サポートされているデバイスとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="04692-130">In the **XR Settings** group, confirm that **"Windows Mixed Reality"** is listed as a supported device.</span></span> <span data-ttu-id="04692-131">(この場合がありますに表示されます"Windows Holographic"として以前のバージョンの Unity)</span><span class="sxs-lookup"><span data-stu-id="04692-131">(this may appear as "Windows Holographic" in older versions of Unity)</span></span>

<span data-ttu-id="04692-132">アプリは、基本的な holographic レンダリングと空間の入力を今すぐ実行できます。</span><span class="sxs-lookup"><span data-stu-id="04692-132">Your app can now do basic holographic rendering and spatial input.</span></span> <span data-ttu-id="04692-133">さらに移動し、特定の機能を活用するには、アプリは、自らのマニフェストで適切な機能を宣言しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="04692-133">To go further and take advantage of certain functionality, your app must declare the appropriate capabilities in its manifest.</span></span> <span data-ttu-id="04692-134">すべての後続のプロジェクトのエクスポートに含まれるように、Unity でマニフェストの宣言を作成できます。</span><span class="sxs-lookup"><span data-stu-id="04692-134">The manifest declarations can be made in Unity so they are included in every subsequent project export.</span></span> <span data-ttu-id="04692-135">設定がある**プレーヤー設定 > ユニバーサル Windows プラットフォームの設定 > 発行の設定 > 機能**します。</span><span class="sxs-lookup"><span data-stu-id="04692-135">The setting are found in **Player Settings > Settings for Universal Windows Platform > Publishing Settings > Capabilities**.</span></span> <span data-ttu-id="04692-136">For Mixed Reality Unity Api の一般的な使用を有効にするための適用可能な機能は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="04692-136">The applicable capabilities for enabling commonly-used Unity APIs for Mixed Reality are:</span></span>

|  <span data-ttu-id="04692-137">機能</span><span class="sxs-lookup"><span data-stu-id="04692-137">Capability</span></span>  |  <span data-ttu-id="04692-138">Api の機能を必要とします。</span><span class="sxs-lookup"><span data-stu-id="04692-138">APIs requiring capability</span></span> | 
|----------|----------|
|  <span data-ttu-id="04692-139">SpatialPerception</span><span class="sxs-lookup"><span data-stu-id="04692-139">SpatialPerception</span></span>  |  <span data-ttu-id="04692-140">SurfaceObserver (へのアクセスを[空間マッピング](spatial-mapping.md)HoloLens でメッシュ)&mdash;*ヘッドセットの一般的な空間の追跡に必要な機能もありません*</span><span class="sxs-lookup"><span data-stu-id="04692-140">SurfaceObserver (access to [spatial mapping](spatial-mapping.md) meshes on HoloLens)&mdash;*No capability needed for general spatial tracking of the headset*</span></span> | 
|  <span data-ttu-id="04692-141">WebCam</span><span class="sxs-lookup"><span data-stu-id="04692-141">WebCam</span></span>  |  <span data-ttu-id="04692-142">PhotoCapture と VideoCapture</span><span class="sxs-lookup"><span data-stu-id="04692-142">PhotoCapture and VideoCapture</span></span> | 
|  <span data-ttu-id="04692-143">PicturesLibrary/VideosLibrary</span><span class="sxs-lookup"><span data-stu-id="04692-143">PicturesLibrary / VideosLibrary</span></span>  |  <span data-ttu-id="04692-144">PhotoCapture または VideoCapture、それぞれ (格納するときにキャプチャしたコンテンツ)</span><span class="sxs-lookup"><span data-stu-id="04692-144">PhotoCapture or VideoCapture, respectively (when storing the captured content)</span></span> | 
|  <span data-ttu-id="04692-145">マイク</span><span class="sxs-lookup"><span data-stu-id="04692-145">Microphone</span></span>  |  <span data-ttu-id="04692-146">VideoCapture (オーディオをキャプチャ) するときに、DictationRecognizer、GrammarRecognizer、および KeywordRecognizer</span><span class="sxs-lookup"><span data-stu-id="04692-146">VideoCapture (when capturing audio), DictationRecognizer, GrammarRecognizer, and KeywordRecognizer</span></span> | 
|  <span data-ttu-id="04692-147">internetClient</span><span class="sxs-lookup"><span data-stu-id="04692-147">InternetClient</span></span>  |  <span data-ttu-id="04692-148">DictationRecognizer (および Unity Profiler を使用する)</span><span class="sxs-lookup"><span data-stu-id="04692-148">DictationRecognizer (and to use the Unity Profiler)</span></span> | 

<span data-ttu-id="04692-149">**Unity の品質の設定**</span><span class="sxs-lookup"><span data-stu-id="04692-149">**Unity quality settings**</span></span>

<span data-ttu-id="04692-150">![Unity の品質の設定](images/unityqualitysettings-350px.png)</span><span class="sxs-lookup"><span data-stu-id="04692-150">![Unity quality settings](images/unityqualitysettings-350px.png)</span></span><br>
<span data-ttu-id="04692-151">*Unity の品質の設定*</span><span class="sxs-lookup"><span data-stu-id="04692-151">*Unity quality settings*</span></span>

<span data-ttu-id="04692-152">HoloLens では、mobile クラス GPU があります。</span><span class="sxs-lookup"><span data-stu-id="04692-152">HoloLens has a mobile-class GPU.</span></span> <span data-ttu-id="04692-153">場合は、アプリは、HoloLens をターゲットとするが、完全なフレーム レートを維持するということを確認する最速のパフォーマンス チューニング、品質設定します。</span><span class="sxs-lookup"><span data-stu-id="04692-153">If your app is targeting HoloLens, you'll want the quality settings tuned for fastest performance to ensure we maintain full framerate:</span></span>
1. <span data-ttu-id="04692-154">選択**編集 > プロジェクトの設定 > 品質**</span><span class="sxs-lookup"><span data-stu-id="04692-154">Select **Edit > Project Settings > Quality**</span></span>
2. <span data-ttu-id="04692-155">選択、**ドロップダウン**下、 **Windows ストア**ロゴと選択**Fastest**します。</span><span class="sxs-lookup"><span data-stu-id="04692-155">Select the **dropdown** under the **Windows Store** logo and select **Fastest**.</span></span> <span data-ttu-id="04692-156">設定すると正しく適用はご存知でしょう Windows ストアの列のボックスと**Fastest**行は緑色です。</span><span class="sxs-lookup"><span data-stu-id="04692-156">You'll know the setting is applied correctly when the box in the Windows Store column and **Fastest** row is green.</span></span>

### <a name="per-scene-settings"></a><span data-ttu-id="04692-157">シーンごとの設定</span><span class="sxs-lookup"><span data-stu-id="04692-157">Per-scene settings</span></span>

<span data-ttu-id="04692-158">**Unity のカメラ設定**</span><span class="sxs-lookup"><span data-stu-id="04692-158">**Unity camera settings**</span></span>

<span data-ttu-id="04692-159">![Unity のカメラ設定](images/unitycamerasettings.png)</span><span class="sxs-lookup"><span data-stu-id="04692-159">![Unity camera settings](images/unitycamerasettings.png)</span></span><br>
<span data-ttu-id="04692-160">*Unity のカメラ設定*</span><span class="sxs-lookup"><span data-stu-id="04692-160">*Unity camera settings*</span></span>

<span data-ttu-id="04692-161">「仮想現実サポート」チェック ボックスを有効にすると、 [Unity カメラ](camera-in-unity.md)コンポーネント ハンドル[追跡とステレオスコ ピック レンダリング ヘッド](rendering.md)します。</span><span class="sxs-lookup"><span data-stu-id="04692-161">Once you enable the "Virtual Reality Supported" checkbox, the [Unity Camera](camera-in-unity.md) component handles [head tracking and stereoscopic rendering](rendering.md).</span></span> <span data-ttu-id="04692-162">これを行うカスタム カメラに置き換える必要はありません。</span><span class="sxs-lookup"><span data-stu-id="04692-162">There is no need to replace it with a custom camera to do this.</span></span>

<span data-ttu-id="04692-163">アプリでは、具体的には HoloLens をターゲットが場合、は、現実の世界をアプリに表示されますので、デバイスの透過的な表示、最適化するために変更する必要があるいくつかの設定があります。</span><span class="sxs-lookup"><span data-stu-id="04692-163">If your app is targeting HoloLens specifically, there are a few settings that need to be changed to optimize for the device's transparent displays, so your app will show through to the physical world:</span></span>
1. <span data-ttu-id="04692-164">**階層**を選択、 **Main Camera**</span><span class="sxs-lookup"><span data-stu-id="04692-164">In the **Hierarchy**, select the **Main Camera**</span></span>
2. <span data-ttu-id="04692-165">**インスペクター**パネルで、設定、変換**位置**に**0, 0, 0**ユーザー ヘッドの位置が、Unity の世界配信元で起動するようです。</span><span class="sxs-lookup"><span data-stu-id="04692-165">In the **Inspector** panel, set the transform **position** to **0, 0, 0** so the location of the users head starts at the Unity world origin.</span></span>
3. <span data-ttu-id="04692-166">変更**フラグをクリア**に**単色**します。</span><span class="sxs-lookup"><span data-stu-id="04692-166">Change **Clear Flags** to **Solid Color**.</span></span>
4. <span data-ttu-id="04692-167">変更、**バック グラウンド**する色**RGBA 0,0,0,0**します。</span><span class="sxs-lookup"><span data-stu-id="04692-167">Change the **Background** color to **RGBA 0,0,0,0**.</span></span> <span data-ttu-id="04692-168">黒は、HoloLens で透明としてレンダリングします。</span><span class="sxs-lookup"><span data-stu-id="04692-168">Black renders as transparent in HoloLens.</span></span>
5. <span data-ttu-id="04692-169">変更**Clipping - つまり近く**を[推奨 HoloLens](camera-in-unity.md#clip-planes) 0.85 (メートル)。</span><span class="sxs-lookup"><span data-stu-id="04692-169">Change **Clipping Planes - Near** to the [HoloLens recommended](camera-in-unity.md#clip-planes) 0.85 (meters).</span></span>

<span data-ttu-id="04692-170">削除し、新しいカメラを作成した場合、カメラが確認**タグ**として**MainCamera**します。</span><span class="sxs-lookup"><span data-stu-id="04692-170">If you delete and create a new camera, make sure your camera is **Tagged** as **MainCamera**.</span></span>

## <a name="adding-mixed-reality-capabilities-and-inputs"></a><span data-ttu-id="04692-171">複合現実の機能および入力の追加</span><span class="sxs-lookup"><span data-stu-id="04692-171">Adding mixed reality capabilities and inputs</span></span>

<span data-ttu-id="04692-172">前述のように、プロジェクトを構成したら、(カメラ) などの標準の Unity ゲーム オブジェクトが点灯直後の**取り付けられているスケール エクスペリエンス**、ユーザーとして自動的に更新するカメラの位置に移動します。自分の頭世界をします。</span><span class="sxs-lookup"><span data-stu-id="04692-172">Once you've configured your project as described above, standard Unity game objects (such as the camera) will light up immediately for a **seated-scale experience**, with the camera's position updated automatically as the user moves their head through the world.</span></span>

<span data-ttu-id="04692-173">Windows Mixed Reality 機能のサポートを追加するなど、[空間ステージ](coordinate-systems.md#spatial-coordinate-systems)、[ジェスチャ、モーションのコント ローラー](gestures-and-motion-controllers-in-unity.md)または[音声入力](voice-input-in-unity.md)に直接組み込まれている Api を使用して実現されますUnity です。</span><span class="sxs-lookup"><span data-stu-id="04692-173">Adding support for Windows Mixed Reality features such as [spatial stages](coordinate-systems.md#spatial-coordinate-systems), [gestures, motion controllers](gestures-and-motion-controllers-in-unity.md) or [voice input](voice-input-in-unity.md) is achieved using APIs built directly into Unity.</span></span>

<span data-ttu-id="04692-174">最初の手順は、確認する必要があります、[スケールが発生する](coordinate-systems.md)アプリを対象とします。</span><span class="sxs-lookup"><span data-stu-id="04692-174">Your first step should be to review the [experience scales](coordinate-systems.md) that your app can target:</span></span>
* <span data-ttu-id="04692-175">ビルドに必要な場合、**向き専用**または**取り付けられているスケール エクスペリエンス**、設定する必要があります Unity に領域の種類の追跡の[静止](coordinate-systems-in-unity.md#building-an-orientation-only-or-seated-scale-experience)。</span><span class="sxs-lookup"><span data-stu-id="04692-175">If you're looking to build an **orientation-only** or **seated-scale experience**, you'll need to set Unity's tracking space type to [Stationary](coordinate-systems-in-unity.md#building-an-orientation-only-or-seated-scale-experience).</span></span>
* <span data-ttu-id="04692-176">ビルドに必要な場合、**継続スケール**または**ルーム スケール エクスペリエンス**、Unity のことを確認する必要がありますに正常に設定されて領域の種類を追跡[RoomScale](coordinate-systems-in-unity.md#building-an-orientation-only-or-seated-scale-experience)します。</span><span class="sxs-lookup"><span data-stu-id="04692-176">If you're looking to build a **standing-scale** or **room-scale experience**, you'll need to ensure Unity's tracking space type is successfully set to [RoomScale](coordinate-systems-in-unity.md#building-an-orientation-only-or-seated-scale-experience).</span></span>
* <span data-ttu-id="04692-177">ビルドに必要な場合、**世界規模**、HoloLens でエクスペリエンスをユーザーが 5 m を超えるローミングできるようにすることを使用する必要があります、 [WorldAnchor](coordinate-systems-in-unity.md#building-a-world-scale-experience)コンポーネント。</span><span class="sxs-lookup"><span data-stu-id="04692-177">If you're looking to build a **world-scale** experience on HoloLens, letting users roam beyond 5 meters, you'll need to use the [WorldAnchor](coordinate-systems-in-unity.md#building-a-world-scale-experience) component.</span></span>

<span data-ttu-id="04692-178">すべての複合現実アプリ用のコア ビルディング ブロックは、その他の Unity Api を使用した一貫性のある方法で公開されます。</span><span class="sxs-lookup"><span data-stu-id="04692-178">All of the core building blocks for mixed reality apps are exposed in a manner consistent with other Unity APIs:</span></span>
* [<span data-ttu-id="04692-179">カメラ</span><span class="sxs-lookup"><span data-stu-id="04692-179">Camera</span></span>](camera-in-unity.md)
* [<span data-ttu-id="04692-180">座標系</span><span class="sxs-lookup"><span data-stu-id="04692-180">Coordinate systems</span></span>](coordinate-systems-in-unity.md)
* [<span data-ttu-id="04692-181">視線入力</span><span class="sxs-lookup"><span data-stu-id="04692-181">Gaze</span></span>](gaze-in-unity.md)
* [<span data-ttu-id="04692-182">ジェスチャとアニメーション コント ローラー</span><span class="sxs-lookup"><span data-stu-id="04692-182">Gestures and motion controllers</span></span>](gestures-and-motion-controllers-in-unity.md)
* [<span data-ttu-id="04692-183">音声入力</span><span class="sxs-lookup"><span data-stu-id="04692-183">Voice input</span></span>](voice-input-in-unity.md)
* [<span data-ttu-id="04692-184">永続化</span><span class="sxs-lookup"><span data-stu-id="04692-184">Persistence</span></span>](persistence-in-unity.md)
* [<span data-ttu-id="04692-185">空間のサウンド</span><span class="sxs-lookup"><span data-stu-id="04692-185">Spatial sound</span></span>](spatial-sound-in-unity.md)
* [<span data-ttu-id="04692-186">空間マッピング</span><span class="sxs-lookup"><span data-stu-id="04692-186">Spatial mapping</span></span>](spatial-mapping-in-unity.md)

<span data-ttu-id="04692-187">多くの複合現実アプリは、使用する Unity アプリにも公開するその他の主な機能があります。</span><span class="sxs-lookup"><span data-stu-id="04692-187">There are other key features that many mixed reality apps will want to use, which are also exposed to Unity apps:</span></span>
* [<span data-ttu-id="04692-188">共有エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="04692-188">Shared experiences</span></span>](shared-experiences-in-unity.md)
* [<span data-ttu-id="04692-189">場所を特定できるカメラ</span><span class="sxs-lookup"><span data-stu-id="04692-189">Locatable camera</span></span>](locatable-camera-in-unity.md)
* [<span data-ttu-id="04692-190">フォーカス ポイント</span><span class="sxs-lookup"><span data-stu-id="04692-190">Focus point</span></span>](focus-point-in-unity.md)
* [<span data-ttu-id="04692-191">損失の追跡</span><span class="sxs-lookup"><span data-stu-id="04692-191">Tracking loss</span></span>](tracking-loss-in-unity.md)
* <span data-ttu-id="04692-192">[[キーボード]](keyboard-input-in-unity.md)</span><span class="sxs-lookup"><span data-stu-id="04692-192">[Keyboard](keyboard-input-in-unity.md)</span></span>

## <a name="running-your-unity-project-on-a-real-or-simulated-device"></a><span data-ttu-id="04692-193">実際、またはシミュレートされたデバイスで Unity プロジェクトを実行しています。</span><span class="sxs-lookup"><span data-stu-id="04692-193">Running your Unity project on a real or simulated device</span></span>

<span data-ttu-id="04692-194">次の手順は、ようになったら、holographic の Unity プロジェクトをテストする準備ができて、[をエクスポートし、Unity Visual Studio ソリューションをビルド](exporting-and-building-a-unity-visual-studio-solution.md)します。</span><span class="sxs-lookup"><span data-stu-id="04692-194">Once you've got your holographic Unity project ready to test out, your next step is to [export and build a Unity Visual Studio solution](exporting-and-building-a-unity-visual-studio-solution.md).</span></span>

<span data-ttu-id="04692-195">手の形でその VS ソリューションとできますし、アプリを実行する 3 つの方法のいずれかでいずれかを使用して実際またはシミュレーション上のデバイス。</span><span class="sxs-lookup"><span data-stu-id="04692-195">With that VS solution in hand, you can then run your app in one of three ways, using either a real or simulated device:</span></span>
* [<span data-ttu-id="04692-196">実際 HoloLens や Windows Mixed Reality イマーシブ ヘッドセットを展開します。</span><span class="sxs-lookup"><span data-stu-id="04692-196">Deploy to a real HoloLens or Windows Mixed Reality immersive headset</span></span>](using-visual-studio.md)
* [<span data-ttu-id="04692-197">HoloLens のエミュレーターへのデプロイします。</span><span class="sxs-lookup"><span data-stu-id="04692-197">Deploy to the HoloLens emulator</span></span>](using-the-hololens-emulator.md)
* [<span data-ttu-id="04692-198">Windows Mixed Reality イマーシブ ヘッドセット シミュレーターへのデプロイします。</span><span class="sxs-lookup"><span data-stu-id="04692-198">Deploy to the Windows Mixed Reality immersive headset simulator</span></span>](using-the-windows-mixed-reality-simulator.md)

## <a name="unity-documentation"></a><span data-ttu-id="04692-199">Unity のドキュメント</span><span class="sxs-lookup"><span data-stu-id="04692-199">Unity documentation</span></span>

<span data-ttu-id="04692-200">このドキュメントの他使用可能な Windows デベロッパー センターでは、Unity は Unity エディターと共に Windows Mixed Reality 機能のドキュメントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="04692-200">In addition to this documentation available on the Windows Dev Center, Unity installs documentation for Windows Mixed Reality functionality alongside the Unity Editor.</span></span> <span data-ttu-id="04692-201">Unity のドキュメントには、2 つのセクションが含まれています。 提供されています。</span><span class="sxs-lookup"><span data-stu-id="04692-201">The Unity provided documentation includes two separate sections:</span></span>
1. <span data-ttu-id="04692-202">**Unity スクリプトのリファレンス**</span><span class="sxs-lookup"><span data-stu-id="04692-202">**Unity scripting reference**</span></span>
    * <span data-ttu-id="04692-203">ドキュメントのこのセクションには、Unity が提供するスクリプト API の詳細が含まれています。</span><span class="sxs-lookup"><span data-stu-id="04692-203">This section of the documentation contains details of the scripting API that Unity provides.</span></span>
    * <span data-ttu-id="04692-204">Unity エディターからを通じてアクセス可能な**ヘルプ > スクリプトのリファレンス**</span><span class="sxs-lookup"><span data-stu-id="04692-204">Accessible from the Unity Editor through **Help > Scripting Reference**</span></span>
2. <span data-ttu-id="04692-205">**Unity マニュアル**</span><span class="sxs-lookup"><span data-stu-id="04692-205">**Unity manual**</span></span>
    * <span data-ttu-id="04692-206">このマニュアルは、高度な基本的な手法から Unity を使用する方法を学習するために設計されています。</span><span class="sxs-lookup"><span data-stu-id="04692-206">This manual is designed to help you learn how to use Unity, from basic to advanced techniques.</span></span>
    * <span data-ttu-id="04692-207">Unity エディターからを通じてアクセス可能な**ヘルプ > 手動**</span><span class="sxs-lookup"><span data-stu-id="04692-207">Accessible from the Unity Editor through **Help > Manual**</span></span>

## <a name="see-also"></a><span data-ttu-id="04692-208">関連項目</span><span class="sxs-lookup"><span data-stu-id="04692-208">See also</span></span>
* [<span data-ttu-id="04692-209">MR 基礎 100:Unity の概要</span><span class="sxs-lookup"><span data-stu-id="04692-209">MR Basics 100: Getting started with Unity</span></span>](holograms-100.md)
* [<span data-ttu-id="04692-210">Unity の推奨設定</span><span class="sxs-lookup"><span data-stu-id="04692-210">Recommended settings for Unity</span></span>](recommended-settings-for-unity.md)
* [<span data-ttu-id="04692-211">Unity のパフォーマンスに関する推奨事項</span><span class="sxs-lookup"><span data-stu-id="04692-211">Performance recommendations for Unity</span></span>](performance-recommendations-for-unity.md)
* [<span data-ttu-id="04692-212">エクスポートして、Unity Visual Studio ソリューションを構築します。</span><span class="sxs-lookup"><span data-stu-id="04692-212">Exporting and building a Unity Visual Studio solution</span></span>](exporting-and-building-a-unity-visual-studio-solution.md)
* [<span data-ttu-id="04692-213">HoloLens の Unity アプリを使用して Windows 名前空間の使用</span><span class="sxs-lookup"><span data-stu-id="04692-213">Using the Windows namespace with Unity apps for HoloLens</span></span>](using-the-windows-namespace-with-unity-apps-for-hololens.md)
* [<span data-ttu-id="04692-214">Unity と Visual Studio を使用するためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="04692-214">Best practices for working with Unity and Visual Studio</span></span>](best-practices-for-working-with-unity-and-visual-studio.md)
* [<span data-ttu-id="04692-215">Unity の再生モード</span><span class="sxs-lookup"><span data-stu-id="04692-215">Unity Play Mode</span></span>](unity-play-mode.md)
* [<span data-ttu-id="04692-216">移植のガイド</span><span class="sxs-lookup"><span data-stu-id="04692-216">Porting guides</span></span>](porting-guides.md)