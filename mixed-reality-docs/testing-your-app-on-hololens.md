---
title: HoloLens でアプリのテスト
description: ガイダンスと、HoloLens のアプリをテストするための推奨事項
author: JonMLyons
ms.author: jlyons
ms.date: 02/24/2019
ms.topic: article
keywords: HoloLens のテスト
ms.openlocfilehash: 35e8eff230cdcd719952ad2633ec610c9a9a26a0
ms.sourcegitcommit: 384b0087899cd835a3a965f75c6f6c607c9edd1b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/12/2019
ms.locfileid: "59599974"
---
# <a name="testing-your-app-on-hololens"></a><span data-ttu-id="2a23f-104">HoloLens でアプリのテスト</span><span class="sxs-lookup"><span data-stu-id="2a23f-104">Testing your app on HoloLens</span></span>

<span data-ttu-id="2a23f-105">HoloLens のアプリケーションのテストは、Windows アプリケーションのテストとよく似ています。</span><span class="sxs-lookup"><span data-stu-id="2a23f-105">Testing HoloLens applications are very similar to testing Windows applications.</span></span> <span data-ttu-id="2a23f-106">(機能、相互運用性、パフォーマンス、セキュリティ、信頼性など) は、通常のすべての領域を検討してください。</span><span class="sxs-lookup"><span data-stu-id="2a23f-106">All the usual areas should be considered (functionality, interoperability, performance, security, reliability, etc.).</span></span> <span data-ttu-id="2a23f-107">ただし、特別な処理や PC または phone アプリでは、通常は確認されません詳細の確認が必要な一部の領域があります。</span><span class="sxs-lookup"><span data-stu-id="2a23f-107">There are, however, some areas that require special handling or attention to details that are not usually observed in PC or phone apps.</span></span> <span data-ttu-id="2a23f-108">Holographic アプリは、多様な環境でスムーズに実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a23f-108">Holographic apps need to run smoothly in a diverse set of environments.</span></span> <span data-ttu-id="2a23f-109">常にパフォーマンスとユーザーの快適性を維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a23f-109">They also need to maintain performance and user comfort at all times.</span></span> <span data-ttu-id="2a23f-110">これらの領域をテストするためのガイダンスはこのトピックで説明します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-110">Guidance for testing these areas is detailed in this topic.</span></span>

## <a name="performance"></a><span data-ttu-id="2a23f-111">パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="2a23f-111">Performance</span></span>

<span data-ttu-id="2a23f-112">Holographic アプリは、多様な環境でスムーズに実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a23f-112">Holographic apps need to run smoothly in a diverse set of environments.</span></span> <span data-ttu-id="2a23f-113">常にパフォーマンスとユーザーの快適性を維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a23f-113">They also need to maintain performance and user comfort at all times.</span></span> <span data-ttu-id="2a23f-114">パフォーマンスが非常に重要なトピック、全体をある Holographic アプリでユーザーのエクスペリエンスにします。</span><span class="sxs-lookup"><span data-stu-id="2a23f-114">Performance is so important to the user's experience with a Holographic app that we have an entire topic devoted to it.</span></span> <span data-ttu-id="2a23f-115">次のことを確認してください、 [for Mixed Reality パフォーマンスを理解](understanding-performance-for-mixed-reality.md)</span><span class="sxs-lookup"><span data-stu-id="2a23f-115">Please make sure you read and follow the [Understanding Performance for Mixed Reality](understanding-performance-for-mixed-reality.md)</span></span>

## <a name="testing-3d-in-3d"></a><span data-ttu-id="2a23f-116">3D で 3D のテスト</span><span class="sxs-lookup"><span data-stu-id="2a23f-116">Testing 3D in 3D</span></span>
1. <span data-ttu-id="2a23f-117">**できるだけ多くのさまざまなスペースでアプリをテストします。**</span><span class="sxs-lookup"><span data-stu-id="2a23f-117">**Test your app in as many different spaces as possible.**</span></span> <span data-ttu-id="2a23f-118">ビッグ ルーム、小規模のルーム、浴室、設備、ベッドルーム、オフィスなどでお試しください。非縦方向の壁、曲線の壁、水平方向以外シーリングなどの非標準の機能と考慮事項のルームを考慮します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-118">Try in big rooms, small rooms, bathrooms, kitchens, bedrooms, offices, etc. Also take into consideration rooms with non standard features such as non vertical walls, curved walls, non-horizontal ceilings.</span></span> <span data-ttu-id="2a23f-119">動作のルームの間で遷移、ときにも現場、廊下や階段を通過しますか?</span><span class="sxs-lookup"><span data-stu-id="2a23f-119">Does it work well when transitioning between rooms, floors, going through hallways or stairs?</span></span>
2. <span data-ttu-id="2a23f-120">**さまざまな照明条件では、アプリをテストします。**</span><span class="sxs-lookup"><span data-stu-id="2a23f-120">**Test your app in different lighting conditions.**</span></span> <span data-ttu-id="2a23f-121">適切に応答ライティング、黒い画面、透過的/反射サーフェス (ミラー、ガラス壁など) などのさまざまな環境条件。</span><span class="sxs-lookup"><span data-stu-id="2a23f-121">Does it respond properly to different environmental conditions such as lighting, black surfaces, transparent/reflective surfaces such as mirrors, glass walls, etc.</span></span>
3. <span data-ttu-id="2a23f-122">**異なる動作条件では、アプリをテストします。**</span><span class="sxs-lookup"><span data-stu-id="2a23f-122">**Test your app in different motion conditions.**</span></span> <span data-ttu-id="2a23f-123">デバイス上に配置して、モーションのさまざまな状態で、シナリオを再試行してください。</span><span class="sxs-lookup"><span data-stu-id="2a23f-123">Put on device and try your scenarios in various states of motion.</span></span> <span data-ttu-id="2a23f-124">適切に応答異なる移動または安定した状態ですか。</span><span class="sxs-lookup"><span data-stu-id="2a23f-124">Does it respond properly to different movement or steady state?</span></span>
4. <span data-ttu-id="2a23f-125">**さまざまな角度から、アプリの動作をテストします。**</span><span class="sxs-lookup"><span data-stu-id="2a23f-125">**Test how your app works from different angles.**</span></span> <span data-ttu-id="2a23f-126">ロックされている世界ホログラムがある場合は、その背後にある場合は、ユーザーとどうなりますか。</span><span class="sxs-lookup"><span data-stu-id="2a23f-126">If you have a world locked hologram, what happens if your user walks behind it?</span></span> <span data-ttu-id="2a23f-127">ユーザーと、ホログラムの間には何かするとどうなりますか。</span><span class="sxs-lookup"><span data-stu-id="2a23f-127">What happens if something comes between the user and the hologram?</span></span> <span data-ttu-id="2a23f-128">場合、ユーザーを見てから上または下ホログラムでしょうか。</span><span class="sxs-lookup"><span data-stu-id="2a23f-128">What if the user looks at the hologram from above or below?</span></span>
5. <span data-ttu-id="2a23f-129">**空間およびオーディオ キューを使用します。** アプリでは、これらを使用して、ユーザーが紛失するを防ぐことを確認します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-129">**Use spatial and audio cues.** Make sure your app uses these to prevent the user from getting lost.</span></span>
6. <span data-ttu-id="2a23f-130">**周囲のノイズのさまざまなレベルでアプリをテストします。**</span><span class="sxs-lookup"><span data-stu-id="2a23f-130">**Test your app at different levels of ambient noise.**</span></span> <span data-ttu-id="2a23f-131">音声コマンドを実装したら、周囲のノイズのさまざまなレベルでの呼び出しを再試行してください。</span><span class="sxs-lookup"><span data-stu-id="2a23f-131">If you've implemented voice commands, try invoking them with varying levels of ambient noise.</span></span>
7. <span data-ttu-id="2a23f-132">**取り付けられているアプリと永続的なテスト**します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-132">**Test your app seated and standing**.</span></span> <span data-ttu-id="2a23f-133">座席と永続的な位置の両方からテストを確認します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-133">Make sure to test from both seating and standing positions.</span></span>
8. <span data-ttu-id="2a23f-134">**別の距離からアプリをテスト**します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-134">**Test your app from different distances**.</span></span> <span data-ttu-id="2a23f-135">UI 要素の読み取りし、遠くから対話しますか。</span><span class="sxs-lookup"><span data-stu-id="2a23f-135">Can UI elements be read and interacted with from far away?</span></span> <span data-ttu-id="2a23f-136">アプリに react をユーザーに近すぎるを取得するには、ホログラムでしょうか。</span><span class="sxs-lookup"><span data-stu-id="2a23f-136">Does your app react to users getting too close to your holograms?</span></span>
9. <span data-ttu-id="2a23f-137">**アプリ バーの一般的な対話に対してアプリをテスト**します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-137">**Test your app against common app bar interactions**.</span></span> <span data-ttu-id="2a23f-138">すべてのアプリのタイルと 2D のユニバーサル アプリが、[アプリ バー](navigating-the-windows-mixed-reality-home.md#moving-and-adjusting-apps)混在環境でアプリを配置する方法を制御することができます。</span><span class="sxs-lookup"><span data-stu-id="2a23f-138">All app tiles and 2D universal apps have a [app bar](navigating-the-windows-mixed-reality-home.md#moving-and-adjusting-apps) that allows you to control how the app is positioned in the Mixed World.</span></span> <span data-ttu-id="2a23f-139">アプリのプロセスが正常に終了します削除 をクリックし、2 D のユニバーサル アプリのコンテキスト内で、戻る ボタンがサポートされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2a23f-139">Make sure clicking Remove terminates your app process gracefully and that the Back button is supported within the context of your 2D universal app.</span></span> <span data-ttu-id="2a23f-140">Try のスケーリングとのアプリの移動[調整モード](navigating-the-windows-mixed-reality-home.md#moving-and-adjusting-apps)が中断されているアプリのタイルとの両方が、アクティブな。</span><span class="sxs-lookup"><span data-stu-id="2a23f-140">Try scaling and moving your app in [Adjust mode](navigating-the-windows-mixed-reality-home.md#moving-and-adjusting-apps) both while it is active, and while it is a suspended app tile.</span></span>

### <a name="environmental-test-matrix"></a><span data-ttu-id="2a23f-141">環境のテストのマトリックス</span><span class="sxs-lookup"><span data-stu-id="2a23f-141">Environmental Test Matrix</span></span>

![HoloLens アプリの開発環境のテストのマトリックス](images/environment-matrix-600px.png)

## <a name="comfort"></a><span data-ttu-id="2a23f-143">快適性</span><span class="sxs-lookup"><span data-stu-id="2a23f-143">Comfort</span></span>
1. <span data-ttu-id="2a23f-144">**平面をクリップします。**</span><span class="sxs-lookup"><span data-stu-id="2a23f-144">**Clip planes.**</span></span> <span data-ttu-id="2a23f-145">Where に注意深いする[ホログラムがレンダリングされる](hologram-stability.md#hologram-render-distances)します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-145">Be attentive to where [holograms are rendered](hologram-stability.md#hologram-render-distances).</span></span>
2. <span data-ttu-id="2a23f-146">**仮想移動実際ヘッドの移動と矛盾しないようにします。**</span><span class="sxs-lookup"><span data-stu-id="2a23f-146">**Avoid virtual movement inconsistent with actual head movement.**</span></span> <span data-ttu-id="2a23f-147">ユーザーの実際の動きの代表者でない方法で、カメラを移動しないでください。</span><span class="sxs-lookup"><span data-stu-id="2a23f-147">Avoid moving the camera in a way that is not representative of the user's actual motion.</span></span> <span data-ttu-id="2a23f-148">アプリでは、シーンを使用して、ユーザーを移動する必要がある場合は、動きを予測可能なことしの高速化を最小限に抑えるにより、ユーザーの動きを制御できます。</span><span class="sxs-lookup"><span data-stu-id="2a23f-148">If your app requires moving the user through a scene, make the motion predictable, minimize acceleration, and let the user control the movement.</span></span>
3. <span data-ttu-id="2a23f-149">**ホログラム品質ガイドラインに従います。**</span><span class="sxs-lookup"><span data-stu-id="2a23f-149">**Follow the hologram quality guidelines.**</span></span> <span data-ttu-id="2a23f-150">パフォーマンスの高いアプリを実装する、[ホログラム品質ガイダンス](hologram-stability.md)ユーザーの不安が発生する可能性が低い。</span><span class="sxs-lookup"><span data-stu-id="2a23f-150">Performant apps that implement the [hologram quality guidance](hologram-stability.md) are less likely to result in user discomfort.</span></span>
4. <span data-ttu-id="2a23f-151">**垂直方向にではなく水平方向にホログラムを配布します。**</span><span class="sxs-lookup"><span data-stu-id="2a23f-151">**Distribute holograms horizontally rather than vertically.**</span></span> <span data-ttu-id="2a23f-152">強制的に使用権をプレゼント ユーザーは検索時間の期間を拡張またはダウンの足部の疲労につながることができます。</span><span class="sxs-lookup"><span data-stu-id="2a23f-152">Forcing the user to spend extended periods of time looking up or down can lead to fatigue in the neck.</span></span>

## <a name="input"></a><span data-ttu-id="2a23f-153">入力</span><span class="sxs-lookup"><span data-stu-id="2a23f-153">Input</span></span>

### <a name="gaze-and-gestures"></a><span data-ttu-id="2a23f-154">視線、ジェスチャ</span><span class="sxs-lookup"><span data-stu-id="2a23f-154">Gaze and Gestures</span></span>

<span data-ttu-id="2a23f-155">[視線](gaze.md)入力に照準を合わせますホログラムと環境でユーザーを有効にする HoloLens での基本的な形式です。</span><span class="sxs-lookup"><span data-stu-id="2a23f-155">[Gaze](gaze.md) is a basic form of input on HoloLens that enable users to aim at holograms and the environment.</span></span> <span data-ttu-id="2a23f-156">視覚的に確認できます、視線の先を対象とする、カーソルの位置に基づいています。</span><span class="sxs-lookup"><span data-stu-id="2a23f-156">You can visually see where your gaze is targeting based on the cursor position.</span></span> <span data-ttu-id="2a23f-157">マウス カーソルを注視カーソルを関連付けるには一般的です。</span><span class="sxs-lookup"><span data-stu-id="2a23f-157">It's common to associate the gaze cursor with a mouse cursor.</span></span>

<span data-ttu-id="2a23f-158">[ジェスチャ](gestures.md)はマウスのクリックなどのホログラムと対話する方法。</span><span class="sxs-lookup"><span data-stu-id="2a23f-158">[Gestures](gestures.md) are how you interact with holograms, like a mouse click.</span></span> <span data-ttu-id="2a23f-159">ほとんどの場合、マウス、タッチの動作は同じですが理解し、検証と異なる場合に重要です。</span><span class="sxs-lookup"><span data-stu-id="2a23f-159">Most of the time the mouse and touch behaviors are the same, but it's important to understand and validate when they differ.</span></span>

<span data-ttu-id="2a23f-160">**アプリがマウス、タッチとは異なる動作を検証します。**</span><span class="sxs-lookup"><span data-stu-id="2a23f-160">**Validate when your app has a different behavior with mouse and touch.**</span></span> <span data-ttu-id="2a23f-161">矛盾をユーザーのより自然なエクスペリエンスを実現する設計上の決定を支援します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-161">This will identify inconsistencies and help with design decisions to make the experience more natural for users.</span></span> <span data-ttu-id="2a23f-162">たとえば、ホバーに基づいてアクションをトリガーします。</span><span class="sxs-lookup"><span data-stu-id="2a23f-162">For example, triggering an action based on hover.</span></span>

> [!NOTE]
> <span data-ttu-id="2a23f-163">HoloLens 2 に固有のガイダンスについて[近日](index.md#news-and-notes)します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-163">More guidance specific to HoloLens 2 [coming soon](index.md#news-and-notes).</span></span>

### <a name="custom-voice-commands"></a><span data-ttu-id="2a23f-164">カスタムの音声コマンド</span><span class="sxs-lookup"><span data-stu-id="2a23f-164">Custom Voice Commands</span></span>

<span data-ttu-id="2a23f-165">[音声入力](voice-input.md)相互作用の自然な形式です。</span><span class="sxs-lookup"><span data-stu-id="2a23f-165">[Voice input](voice-input.md) is a natural form of interaction.</span></span> <span data-ttu-id="2a23f-166">ユーザー エクスペリエンスは魔法のようなまたはコマンドおよび公開する方法の好みに応じてわかりづらいにできます。</span><span class="sxs-lookup"><span data-stu-id="2a23f-166">The user experience can be magical or confusing depending on your choice of commands and how you expose them.</span></span> <span data-ttu-id="2a23f-167">原則として、カスタム コマンドとして"Select"」や「コルタナさん」などのシステム音声コマンドを使用する必要がありますできません。</span><span class="sxs-lookup"><span data-stu-id="2a23f-167">As a rule, you should not use system voice commands such as "Select" or "Hey Cortana" as custom commands.</span></span> <span data-ttu-id="2a23f-168">考慮すべきいくつかの点を次に示します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-168">Here are a few points to consider:</span></span>
1. <span data-ttu-id="2a23f-169">**類似したコマンドを使用しないでください。**</span><span class="sxs-lookup"><span data-stu-id="2a23f-169">**Avoid using commands that sound similar.**</span></span> <span data-ttu-id="2a23f-170">これにより、誤ったコマンドが可能性のあるトリガーします。</span><span class="sxs-lookup"><span data-stu-id="2a23f-170">This can potentially trigger the incorrect command.</span></span>
2. <span data-ttu-id="2a23f-171">**可能であれば、発音の豊富な単語を選択します。**</span><span class="sxs-lookup"><span data-stu-id="2a23f-171">**Choose phonetically rich words when possible.**</span></span> <span data-ttu-id="2a23f-172">最小限に抑えるか、false のアクティブ化を回避これは。</span><span class="sxs-lookup"><span data-stu-id="2a23f-172">This will minimize and/or avoid false activations.</span></span>

### <a name="peripherals"></a><span data-ttu-id="2a23f-173">周辺機器</span><span class="sxs-lookup"><span data-stu-id="2a23f-173">Peripherals</span></span>

<span data-ttu-id="2a23f-174">アプリケーションをユーザーが操作できる[周辺機器](hardware-accessories.md)します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-174">Users can interact with your App through [peripherals](hardware-accessories.md).</span></span> <span data-ttu-id="2a23f-175">アプリが確認すべき点があります、その機能を活用するために特別な処理は必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2a23f-175">Apps don't need to do anything special to take advantage of that capability, however there are a couple things worth checking.</span></span>
1. <span data-ttu-id="2a23f-176">**カスタムの相互作用を検証します。**</span><span class="sxs-lookup"><span data-stu-id="2a23f-176">**Validate custom interactions.**</span></span> <span data-ttu-id="2a23f-177">アプリのカスタムのキーボード ショートカットはその一例です。</span><span class="sxs-lookup"><span data-stu-id="2a23f-177">Things like custom keyboard shortcuts for your app.</span></span>
2. <span data-ttu-id="2a23f-178">**入力の種類の切り替えを検証します。**</span><span class="sxs-lookup"><span data-stu-id="2a23f-178">**Validate switching input types.**</span></span> <span data-ttu-id="2a23f-179">複数の入力メソッドを使用して、音声、ジェスチャ、マウス、および同じシナリオですべてのキーボードなどのタスクを完了しようとしています。</span><span class="sxs-lookup"><span data-stu-id="2a23f-179">Attempting to use multiple input methods to complete a task, such as voice, gesture, mouse, and keyboard all in the same scenario.</span></span>

## <a name="system-integration"></a><span data-ttu-id="2a23f-180">システムの統合</span><span class="sxs-lookup"><span data-stu-id="2a23f-180">System Integration</span></span>

### <a name="battery"></a><span data-ttu-id="2a23f-181">バッテリー</span><span class="sxs-lookup"><span data-stu-id="2a23f-181">Battery</span></span>

<span data-ttu-id="2a23f-182">バッテリをお払い箱にどの程度の速度を理解するのに接続されている電源ソースを使用せず、アプリケーションをテストします。</span><span class="sxs-lookup"><span data-stu-id="2a23f-182">Test your application without a power source connected to understand how quickly it drains the battery.</span></span> <span data-ttu-id="2a23f-183">バッテリの状態は、電源 LED の測定値を調べることで 1 つ簡単に理解できます。</span><span class="sxs-lookup"><span data-stu-id="2a23f-183">One can easily understand the battery state by looking at Power LED readings.</span></span> ![バッテリ電源を示す LED の状態](images/batterypowerledindication-500px.png)

### <a name="power-state-transitions"></a><span data-ttu-id="2a23f-185">電源の状態遷移</span><span class="sxs-lookup"><span data-stu-id="2a23f-185">Power State Transitions</span></span>

<span data-ttu-id="2a23f-186">電源の状態間を遷移するときに期待どおりには、主要なシナリオの作業を検証します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-186">Validate key scenarios work as expected when transitioning between power states.</span></span> <span data-ttu-id="2a23f-187">アプリケーションは、元の位置にあるなど、残りますか。</span><span class="sxs-lookup"><span data-stu-id="2a23f-187">For example, does the application remain at its original position?</span></span> <span data-ttu-id="2a23f-188">正しく持続するための状態ですか。</span><span class="sxs-lookup"><span data-stu-id="2a23f-188">Does it correctly persist its state?</span></span> <span data-ttu-id="2a23f-189">正常に動作は、続行しますか。</span><span class="sxs-lookup"><span data-stu-id="2a23f-189">Does it continue to function as expected?</span></span>
1. <span data-ttu-id="2a23f-190">**スタンバイ/再開します。**</span><span class="sxs-lookup"><span data-stu-id="2a23f-190">**Stand-by / Resume.**</span></span> <span data-ttu-id="2a23f-191">スタンバイを入力するには、いずれかのキーを押し、電源ボタンを直ちに解放します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-191">To enter standby, one can press and release the power button immediately.</span></span> <span data-ttu-id="2a23f-192">デバイスは、3 分間続いた後に自動的にスタンバイが入力されます。</span><span class="sxs-lookup"><span data-stu-id="2a23f-192">The device also will enter standby automatically after 3 minutes of inactivity.</span></span> <span data-ttu-id="2a23f-193">スタンバイから再開するにいずれかのキーを押してし、電源ボタンを直ちに解放します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-193">To resume from standby, one can press and release the power button immediately.</span></span> <span data-ttu-id="2a23f-194">接続または電源から切断した場合にも、デバイスが再開されます。</span><span class="sxs-lookup"><span data-stu-id="2a23f-194">The device will also resume if you connect or disconnect it from a power source.</span></span>
2. <span data-ttu-id="2a23f-195">**シャット ダウン/再起動します。**</span><span class="sxs-lookup"><span data-stu-id="2a23f-195">**Shutdown / Restart.**</span></span> <span data-ttu-id="2a23f-196">シャット ダウン、キーを押すし、6 秒の電源ボタンを継続的に保持します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-196">To shutdown, press and hold the power button continuously for 6 seconds.</span></span> <span data-ttu-id="2a23f-197">を再起動するには、電源ボタンを押します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-197">To restart, press the power button.</span></span>

### <a name="multi-app-scenarios"></a><span data-ttu-id="2a23f-198">マルチ アプリ シナリオ</span><span class="sxs-lookup"><span data-stu-id="2a23f-198">Multi-App Scenarios</span></span>

<span data-ttu-id="2a23f-199">バック グラウンド タスクを実装している場合は特に、アプリ間で切り替えるとコア アプリの機能を検証します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-199">Validate core app functionality when switching between apps, especially if you've implemented a background task.</span></span> <span data-ttu-id="2a23f-200">コピー/貼り付けと Cortana の統合もチェックに値する該当する場合。</span><span class="sxs-lookup"><span data-stu-id="2a23f-200">Copy/Paste and Cortana integration are also worth checking where applicable.</span></span>

## <a name="telemetry"></a><span data-ttu-id="2a23f-201">利用統計情報</span><span class="sxs-lookup"><span data-stu-id="2a23f-201">Telemetry</span></span>

<span data-ttu-id="2a23f-202">テレメトリと分析を使用して、参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a23f-202">Use telemetry and analytics to guide you.</span></span> <span data-ttu-id="2a23f-203">分析をアプリに統合するベータ テスターとエンドユーザーからアプリに関する詳細情報を取得する際に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2a23f-203">Integrating analytics into your app will help you get insights about your app from your Beta testers and end-users.</span></span> <span data-ttu-id="2a23f-204">このデータは、今後の更新プログラムと、ストアを送信する前に、アプリを最適化するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="2a23f-204">This data can be used to help optimize your app before submission to the Store and for future updates.</span></span> <span data-ttu-id="2a23f-205">多くの分析のオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="2a23f-205">There are many analytics options out there.</span></span> <span data-ttu-id="2a23f-206">開始する場所がわからない場合はチェック アウト[App Insights](https://www.visualstudio.com/products/application-insights-vs.aspx)します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-206">If you're not sure where to start, check out [App Insights](https://www.visualstudio.com/products/application-insights-vs.aspx).</span></span>

<span data-ttu-id="2a23f-207">考慮すべき質問:</span><span class="sxs-lookup"><span data-stu-id="2a23f-207">Questions to consider:</span></span>
1. <span data-ttu-id="2a23f-208">ユーザーは、領域をどのように使用されてですか。</span><span class="sxs-lookup"><span data-stu-id="2a23f-208">How are users using the space?</span></span>
2. <span data-ttu-id="2a23f-209">どのようにアプリを配置するオブジェクトを世界で検出するには問題でしょうか。</span><span class="sxs-lookup"><span data-stu-id="2a23f-209">How is the app placing objects in the world - can you detect problems?</span></span>
3. <span data-ttu-id="2a23f-210">どれだけ時間、アプリケーションのさまざまな段階にかかるコストの操作を行いますか?</span><span class="sxs-lookup"><span data-stu-id="2a23f-210">How much time do they spend on different stages of the application?</span></span>
4. <span data-ttu-id="2a23f-211">時間の時間を費やしてアプリですか?</span><span class="sxs-lookup"><span data-stu-id="2a23f-211">How much time do they spend in the app?</span></span>
5. <span data-ttu-id="2a23f-212">最も一般的な使用状況のパス、ユーザーとはしようとしているでしょうか。</span><span class="sxs-lookup"><span data-stu-id="2a23f-212">What are the most common usage paths the users are trying?</span></span>
6. <span data-ttu-id="2a23f-213">予期しない状態やエラーに達したユーザーですか。</span><span class="sxs-lookup"><span data-stu-id="2a23f-213">Are users hitting unexpected states and/or errors?</span></span>

## <a name="emulator-and-simulated-input"></a><span data-ttu-id="2a23f-214">エミュレーターとシミュレートされた入力</span><span class="sxs-lookup"><span data-stu-id="2a23f-214">Emulator and Simulated Input</span></span>

<span data-ttu-id="2a23f-215">[HoloLens のエミュレーター](using-the-hololens-emulator.md) Holographic シミュレートされたユーザーの特性とスペースのさまざまなアプリを効率的にテストする優れた方法です。</span><span class="sxs-lookup"><span data-stu-id="2a23f-215">The [HoloLens emulator](using-the-hololens-emulator.md) is a great way to efficiently test your Holographic app with a variety of simulated user characteristics and spaces.</span></span> <span data-ttu-id="2a23f-216">効果的にエミュレーターを使用してアプリをテストする推奨事項を次に示します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-216">Here are some suggestions for effectively using the emulator to test your app:</span></span>
1. <span data-ttu-id="2a23f-217">**エミュレーターの仮想ルームを使用して、展開、テストします。**</span><span class="sxs-lookup"><span data-stu-id="2a23f-217">**Use the emulator's virtual rooms to expand your testing.**</span></span> <span data-ttu-id="2a23f-218">さらに多くの環境でアプリをテストに使用できる仮想ルームのセットに、エミュレーターが付属します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-218">The emulator comes with a set of virtual rooms that you can use to test your app in even more environments.</span></span>
2. <span data-ttu-id="2a23f-219">**エミュレーターを使用すると、すべての角度からアプリを確認します。**</span><span class="sxs-lookup"><span data-stu-id="2a23f-219">**Use the emulator to look at your app from all angles.**</span></span> <span data-ttu-id="2a23f-220">PageUp/PageDn キー サイズを垂直方向は、シミュレートされたユーザーになります。</span><span class="sxs-lookup"><span data-stu-id="2a23f-220">The PageUp/PageDn keys will make your simulated user taller or shorter.</span></span>
3. <span data-ttu-id="2a23f-221">**実際、HoloLens を使用してアプリをテストします。**</span><span class="sxs-lookup"><span data-stu-id="2a23f-221">**Test your app with a real HoloLens.**</span></span> <span data-ttu-id="2a23f-222">HoloLens のエミュレーターは、すぐに始めるための優れたツールのアプリで反復処理して、新しいバグの検出が、Windows ストアに送信する前に、また物理 HoloLens でテストすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2a23f-222">The HoloLens Emulator is a great tool to help you quickly iterate on an app and catch new bugs, but make sure you also test on a physical HoloLens before submitting to the Windows Store.</span></span> <span data-ttu-id="2a23f-223">これは、パフォーマンスとエクスペリエンスが優れたを実際のハードウェアであることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2a23f-223">This is important to ensure that the performance and experience are great on real hardware.</span></span>

## <a name="automated-testing-with-perception-simulation"></a><span data-ttu-id="2a23f-224">Perception シミュレーションによるテストの自動化</span><span class="sxs-lookup"><span data-stu-id="2a23f-224">Automated testing with Perception Simulation</span></span>

<span data-ttu-id="2a23f-225">アプリ開発者によっては、それぞれのアプリのテストを自動化する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2a23f-225">Some app developers might want to automate testing of their apps.</span></span> <span data-ttu-id="2a23f-226">単純な単体テスト、を超えて使用することができます、 [perception シミュレーション](perception-simulation.md)をアプリに人間と世界中の入力を自動化する HoloLens のスタック。</span><span class="sxs-lookup"><span data-stu-id="2a23f-226">Beyond simple unit tests, you can use the [perception simulation](perception-simulation.md) stack in HoloLens to automate human and world input to your app.</span></span> <span data-ttu-id="2a23f-227">Perception シミュレーションの API は、HoloLens のエミュレーターまたは物理 HoloLens のシミュレートされた入力を送信できます。</span><span class="sxs-lookup"><span data-stu-id="2a23f-227">The perception simulation API can send simulated input to either the HoloLens emulator or a physical HoloLens.</span></span>

## <a name="windows-app-certification-kit"></a><span data-ttu-id="2a23f-228">Windows アプリ認定キット</span><span class="sxs-lookup"><span data-stu-id="2a23f-228">Windows App Certification Kit</span></span>

<span data-ttu-id="2a23f-229">アプリを最良の確率の指定に[Windows ストアで公開されている](submitting-an-app-to-the-microsoft-store.md)、検証、および証明書を送信する前にローカルでテストします。</span><span class="sxs-lookup"><span data-stu-id="2a23f-229">To give your app the best chance of being [published on the Windows Store](submitting-an-app-to-the-microsoft-store.md), validate and test it locally before you submit it for certification.</span></span> <span data-ttu-id="2a23f-230">アプリの対象 Windows.Holographic デバイス ファミリの場合、 [Windows アプリ認定キット](https://msdn.microsoft.com/library/windows/apps/xaml/mt186449.aspx)PC でローカルの静的分析テストだけが実行されます。</span><span class="sxs-lookup"><span data-stu-id="2a23f-230">If your app targets the Windows.Holographic device family, the [Windows App Certification Kit](https://msdn.microsoft.com/library/windows/apps/xaml/mt186449.aspx) will only run local static analysis tests on your PC.</span></span> <span data-ttu-id="2a23f-231">HoloLens のテストは実行されません。</span><span class="sxs-lookup"><span data-stu-id="2a23f-231">No tests will be run on your HoloLens.</span></span>

## <a name="see-also"></a><span data-ttu-id="2a23f-232">関連項目</span><span class="sxs-lookup"><span data-stu-id="2a23f-232">See also</span></span>
* [<span data-ttu-id="2a23f-233">Windows ストア アプリの提出</span><span class="sxs-lookup"><span data-stu-id="2a23f-233">Submitting an app to the Windows Store</span></span>](submitting-an-app-to-the-microsoft-store.md)