---
title: HoloTour 空間設計のケース スタディ
description: Microsoft HoloLens の本当に魅力的な 3D バーチャル ツアーを作成するには、パノラマ ビデオおよび holographic 風景は、数式の一部に過ぎません。
author: JSyltebo
ms.author: jsylte
ms.date: 03/21/2018
ms.topic: article
keywords: Windows Mixed Reality、HoloLens、HoloTour、空間のサウンド、ケース スタディ
ms.openlocfilehash: eca675534dba12dd65a20fb9d85e4df57f725288
ms.sourcegitcommit: 384b0087899cd835a3a965f75c6f6c607c9edd1b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/12/2019
ms.locfileid: "59603642"
---
# <a name="case-study---spatial-sound-design-for-holotour"></a><span data-ttu-id="80f6c-104">HoloTour 空間設計のケース スタディ</span><span class="sxs-lookup"><span data-stu-id="80f6c-104">Case study - Spatial sound design for HoloTour</span></span>

<span data-ttu-id="80f6c-105">Microsoft HoloLens の本当に魅力的な 3D バーチャル ツアーを作成するには、パノラマ ビデオおよび holographic 風景は、数式の一部に過ぎません。</span><span class="sxs-lookup"><span data-stu-id="80f6c-105">To create a truly immersive 3D virtual tour for Microsoft HoloLens, the panoramic videos and holographic scenery are only part of the formula.</span></span> <span data-ttu-id="80f6c-106">Jason Syltebo ではサウンド方法について説明するオーディオ デザイナーがキャプチャされ、HoloTour 内の場所のそれぞれで実際にいる気分に処理されます。</span><span class="sxs-lookup"><span data-stu-id="80f6c-106">Audio designer Jason Syltebo talks about how sound was captured and processed to make you feel like you're actually in each of the locations in HoloTour.</span></span>

## <a name="the-tech"></a><span data-ttu-id="80f6c-107">技術者</span><span class="sxs-lookup"><span data-stu-id="80f6c-107">The tech</span></span>

<span data-ttu-id="80f6c-108">美しい画像および HoloTour 『 holographic のシーンは、かぎり複合現実エクスペリエンスを作成する 1 つだけの一部です。</span><span class="sxs-lookup"><span data-stu-id="80f6c-108">The beautiful imagery and holographic scenes you see in HoloTour are only one part of creating a believable mixed reality experience.</span></span> <span data-ttu-id="80f6c-109">ユーザーの前にホログラムが視覚的にのみ表示されます、[空間サウンド](spatial-sound.md)HoloLens の機能により、すべての方向に由来するオーディオより完全な感覚エクスペリエンスをユーザーに提供します。</span><span class="sxs-lookup"><span data-stu-id="80f6c-109">While holograms can only appear visually in front of a user, the [spatial sound](spatial-sound.md) feature of HoloLens allows audio to come from all directions, which gives the user a more complete sensory experience.</span></span>

<span data-ttu-id="80f6c-110">空間のサウンドを使用して、またはユーザーがその領域内を参照するように複数のホログラムがあることに、ユーザーが有効にする方向を示すオーディオ キューを提供できます。</span><span class="sxs-lookup"><span data-stu-id="80f6c-110">Spatial sound allows us to give audio cues to indicate a direction in which the user should turn, or to let the user know there are more holograms for them to see within their space.</span></span> <span data-ttu-id="80f6c-111">方向と距離ホログラムはサウンドがそのオブジェクトから直接送信されるかのように見えますが、ユーザーからの継続的に更新を直接ホログラムにサウンドを添付することもできます。</span><span class="sxs-lookup"><span data-stu-id="80f6c-111">We can also attach a sound directly to a hologram and continually update the direction and distance the hologram is from a user to make it seem as if the sound is coming directly from that object.</span></span>

<span data-ttu-id="80f6c-112">HoloTour で特定の場所の sonic 重要なポイントを表示するビデオと同期して、360 度アンビエント環境を作成する、HoloLens のサウンドの空間機能を活用するために考えました。</span><span class="sxs-lookup"><span data-stu-id="80f6c-112">With HoloTour, we wanted to take advantage of the spatial sound capabilities of HoloLens to create a 360-degree ambient environment, synchronized with the video to reveal the sonic highlights of specific locations.</span></span>

## <a name="behind-the-scenes"></a><span data-ttu-id="80f6c-113">しくみ</span><span class="sxs-lookup"><span data-stu-id="80f6c-113">Behind the scenes</span></span>

<span data-ttu-id="80f6c-114">2 つの場所の HoloTour エクスペリエンスを作成しました。ローマ マチュピチュ.</span><span class="sxs-lookup"><span data-stu-id="80f6c-114">We created HoloTour experiences of two different locations: Rome and Machu Picchu.</span></span> <span data-ttu-id="80f6c-115">本物であり、説得力のあると思われるこれらのツアーを作成するには、一般的なサウンドを使用しないようにして代わりに場所映画された場所から直接オーディオをキャプチャする考えました。</span><span class="sxs-lookup"><span data-stu-id="80f6c-115">To make these tours feel authentic and compelling we wanted to avoid using generic sounds and instead capture audio directly from the locations where we were filming.</span></span>

### <a name="capturing-the-audio"></a><span data-ttu-id="80f6c-116">オーディオのキャプチャ</span><span class="sxs-lookup"><span data-stu-id="80f6c-116">Capturing the audio</span></span>

<span data-ttu-id="80f6c-117">[HoloTour のビジュアルのコンテンツをキャプチャする方法についてのケース スタディ](case-study-capturing-and-creating-content-for-holotour.md)は、カメラのリモート テスト マシン群のカスタム デザインについて説明しました。</span><span class="sxs-lookup"><span data-stu-id="80f6c-117">In our [case study about capturing the visual content for HoloTour](case-study-capturing-and-creating-content-for-holotour.md), we talked about the custom design of our camera rig.</span></span> <span data-ttu-id="80f6c-118">3D 印刷の住宅費に含まれている 14 の GoPro カメラで構成されている、三脚の特定の大きさに設計されています。</span><span class="sxs-lookup"><span data-stu-id="80f6c-118">It consisted of 14 GoPro cameras contained in a 3D-printed housing, designed to the specific dimensions of the tripod.</span></span> <span data-ttu-id="80f6c-119">このリモート テスト マシン群のオーディオをキャプチャするには、カメラでは、三脚の下部に座って compact 4 チャネル記録単位にフィードの下にクアッド マイク配列を追加しました。</span><span class="sxs-lookup"><span data-stu-id="80f6c-119">To capture audio from this rig, we added a quad-microphone array beneath the cameras, which fed into a compact 4-channel recording unit that sat at the base of the tripod.</span></span> <span data-ttu-id="80f6c-120">選択したマイク、実行するだけでなく、非常に小さなフット プリント、カメラの視野がないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="80f6c-120">We chose microphones that not only performed well, but which had a very small footprint, so as to not occlude the view of the camera.</span></span>

<span data-ttu-id="80f6c-121">![カスタム カメラとマイク リモート テスト マシン群](images/camera-rig-microphones-300px.png)</span><span class="sxs-lookup"><span data-stu-id="80f6c-121">![Custom camera and microphone rig](images/camera-rig-microphones-300px.png)</span></span><br>
<span data-ttu-id="80f6c-122">*カスタム カメラとマイク リモート テスト マシン群*</span><span class="sxs-lookup"><span data-stu-id="80f6c-122">*Custom camera and microphone rig*</span></span>

<span data-ttu-id="80f6c-123">このセットアップでは、空間のサウンドは、後で同期する 360 度のビデオでしたを使用して 3D 聴覚的なパノラマを再作成するのに十分な情報を提供することで、カメラの正確な場所から 4 方向のサウンドをキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="80f6c-123">This setup captured sound in four directions from the precise location of our camera, giving us enough information to re-create a 3D aural panorama using spatial sound, which we could later synchronize to the 360-degree video.</span></span>

<span data-ttu-id="80f6c-124">カメラの配列のオーディオに関する課題の 1 つは、キャプチャ時に記録内容が制御しています。</span><span class="sxs-lookup"><span data-stu-id="80f6c-124">One of the challenges with the camera array audio is that you are at the mercy of what is recorded at the time of capture.</span></span> <span data-ttu-id="80f6c-125">ビデオのキャプチャが正常な場合でもサウンドのキャプチャは問題のあるカメラからのサウンド sirens、飛行機、強風などが原因になります。</span><span class="sxs-lookup"><span data-stu-id="80f6c-125">Even if the video capture is good, the sound capture can become problematic due to off-camera sounds such as sirens, airplanes, or high winds.</span></span> <span data-ttu-id="80f6c-126">ようにする必要があるすべての要素には、一連のモバイルの記録をステレオと mono のユニットを使用して、各場所で関心のある特定の時点で非同期のアンビエント要素を取得しました。</span><span class="sxs-lookup"><span data-stu-id="80f6c-126">To assure we had all the elements we need, we used a series of stereo and mono mobile recording units to get asynchronous, ambient elements at specific points of interest in each location.</span></span> <span data-ttu-id="80f6c-127">このキャプチャは、サウンドのデザイナーには関心を作って方向性をさらに追加後の運用環境で使用できるクリーンで使用可能なコンテンツをシーク機能を提供するので重要です。</span><span class="sxs-lookup"><span data-stu-id="80f6c-127">This capture is important as it gives the sound designer the ability to seek out clean and usable content that can be used in post-production to craft interest and add further directionality.</span></span>

<span data-ttu-id="80f6c-128">指定されたキャプチャの日では、多数のファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="80f6c-128">Any given capture day would generate a large number of files.</span></span> <span data-ttu-id="80f6c-129">追跡するために特定の場所またはカメラ ショット対応、ファイル システムを開発する重要でした。</span><span class="sxs-lookup"><span data-stu-id="80f6c-129">It was important to develop a system to track which files correspond to a particular location or camera shot.</span></span> <span data-ttu-id="80f6c-130">日付で弊社の記録の単位が自動名前のファイルをセットアップし、take の数値と私たちはこれらをバックアップ、1 日の最後に外部ドライブにします。</span><span class="sxs-lookup"><span data-stu-id="80f6c-130">Our recording unit was set up to auto-name files by date and take number and we would back these up at the end of the day to external drives.</span></span> <span data-ttu-id="80f6c-131">少なくとも、スレート口頭でオーディオ録音の開始が重要なは、ファイル名が問題になる必要があります、コンテンツのコンテキスト id を簡単にします。</span><span class="sxs-lookup"><span data-stu-id="80f6c-131">At the very least, verbally slating the beginning of audio recordings was important as this allows easy contextual identification of the content should filenames become a problem.</span></span> <span data-ttu-id="80f6c-132">ビデオとオーディオが別のメディアとして記録し、post 中に同期するために必要なカメラ リモート テスト マシン群のキャプチャを視覚的にスレートに重要でした。</span><span class="sxs-lookup"><span data-stu-id="80f6c-132">It was also important for us to visually slate the camera rig capture as the video and audio were recorded as separate media and needed to be synchronized during post.</span></span>

### <a name="editing-the-audio"></a><span data-ttu-id="80f6c-133">オーディオの編集</span><span class="sxs-lookup"><span data-stu-id="80f6c-133">Editing the audio</span></span>

<span data-ttu-id="80f6c-134">キャプチャ トリップした後、studio に戻り、方向、没入型の聴覚的なエクスペリエンスをアセンブルする最初の手順は、すべての場所、最善の受け取りを取り出すと、独創的な時に適用できる主なトピックを識別するオーディオ キャプチャの確認統合します。</span><span class="sxs-lookup"><span data-stu-id="80f6c-134">Back at the studio after the capture trip, the first step in assembling a directional and immersive aural experience is to review all of the audio capture for a location, picking out the best takes and identifying any highlights that could be applied creatively during integration.</span></span> <span data-ttu-id="80f6c-135">オーディオを編集し、クリーンアップはします。</span><span class="sxs-lookup"><span data-stu-id="80f6c-135">The audio is then edited and cleaned up.</span></span> <span data-ttu-id="80f6c-136">など大きな車警報継続期間が 1 秒と、数回の繰り返しを交換およびと同じキャプチャからの通知の停止、アンビエント オーディオのセクションを使用して合成します。</span><span class="sxs-lookup"><span data-stu-id="80f6c-136">For example, a loud car horn lasting a second or so and repeating a few times, can be replaced and stitched in with sections of quiet, ambient audio from the same capture.</span></span>

<span data-ttu-id="80f6c-137">場所のビデオ編集が確立されると、サウンドのデザイナーは、対応するオーディオを同期できます。</span><span class="sxs-lookup"><span data-stu-id="80f6c-137">Once the video edit for a location has been established the sound designer can synchronize the corresponding audio.</span></span> <span data-ttu-id="80f6c-138">この時点でカメラのリモート テスト マシン群のキャプチャとどのような要素、または組み合わせ、没入型のオーディオ シーンを構築する動作を決定するモバイルのキャプチャの両方に取り組みました。</span><span class="sxs-lookup"><span data-stu-id="80f6c-138">At this point we worked with both camera rig capture and mobile capture to decide what elements, or combination thereof, will work to build an immersive audio scene.</span></span> <span data-ttu-id="80f6c-139">見つかりました便利な技法は、サウンドのすべての要素をオーディオ エディターとビルド クイック線形モック ups をさまざまな組み合わせのアイデアを実験に追加するがあります。</span><span class="sxs-lookup"><span data-stu-id="80f6c-139">A technique we found useful was to add all the sound elements into an audio editor and build quick linear mock ups to experiment with different mix ideas.</span></span> <span data-ttu-id="80f6c-140">これにより、形式でアイデアをより実際 HoloTour シーンを構築するとき。</span><span class="sxs-lookup"><span data-stu-id="80f6c-140">This gave us better formed ideas when it came time to build the actual HoloTour scenes.</span></span>

### <a name="assembling-the-scene"></a><span data-ttu-id="80f6c-141">シーンのアセンブル</span><span class="sxs-lookup"><span data-stu-id="80f6c-141">Assembling the scene</span></span>

<span data-ttu-id="80f6c-142">アンビエントの 3D シーンを構築する最初の手順では、シーン内の他の機能とサウンドの対話型の要素をサポートする一般的なバック グラウンド アンビエント ループ サウンドのベッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="80f6c-142">The first step to building a 3D ambient scene is to create a bed of general background ambient looping sounds that will support other features and interactive sound elements in a scene.</span></span> <span data-ttu-id="80f6c-143">そのため、特定のニーズと、特定のシーンの設計基準によって決定別の実装テクニックに対する包括的なアプローチをしました。</span><span class="sxs-lookup"><span data-stu-id="80f6c-143">In doing so, we took a holistic approach towards different implementation techniques determined by the specific needs and design criteria of any particular scene.</span></span> <span data-ttu-id="80f6c-144">いくつかのシーンは、HoloTour より映画のような瞬間のサウンド、対話型の要素と音楽とサウンド効果がより個別を使用するより選別された方法に配置が必要ですが、同期のカメラ キャプチャを使用したインデックス可能性があります。</span><span class="sxs-lookup"><span data-stu-id="80f6c-144">Some scenes might index towards using the synchronized camera capture, whereas others might require a more curated approach that uses more discretely placed sounds, interactive elements and music and sound effects for the more cinematic moments in HoloTour.</span></span>

<span data-ttu-id="80f6c-145">空間サウンドが有効なアンビエント オーディオ エミッタ north カメラのビューを北マイクからオーディオ再生されるように、カメラの向きの方向の座標に対応する配置しましたカメラ キャプチャ オーディオの使用にインデックスを付ける場合と同様に。その他の基本的な方向です。</span><span class="sxs-lookup"><span data-stu-id="80f6c-145">When indexing on the use of the camera capture audio, we placed spatial sound-enabled ambient audio emitters corresponding to the directional coordinates of the camera orientation such that the north camera view plays audio from the north microphone and likewise for the other cardinal directions.</span></span> <span data-ttu-id="80f6c-146">これらの発信機にはその場所での継続のサウンドを効率的にモデリングつまりユーザーは、これらの発信機に対する自分の頭に自由を有効にして、サウンドが変わります world ロックです。</span><span class="sxs-lookup"><span data-stu-id="80f6c-146">These emitters are world-locked, meaning the user can freely turn their head in relation to these emitters and the sound will change accordingly, effectively modeling the sound of standing at that location.</span></span> <span data-ttu-id="80f6c-147">カメラ キャプチャされたオーディオの適切な組み合わせを使用して、シーンの例については、Piazza Navona または Pantheon をリッスンします。</span><span class="sxs-lookup"><span data-stu-id="80f6c-147">Listen to Piazza Navona or The Pantheon for examples of scenes that use a good mix of camera captured audio.</span></span>

<span data-ttu-id="80f6c-148">別のアプローチでは、ボリューム、ピッチ、およびトリガーの頻度の観点からはランダム化を 1 回限りのサウンドの再生、シーンの周囲に配置する空間のサウンド エミッタを組み合わせてループ ステレオ アンビエンスの再生に関与します。</span><span class="sxs-lookup"><span data-stu-id="80f6c-148">A different approach involved playing a looping stereo ambience in conjunction with spatial sound emitters placed around the scene playing one-off sounds that are randomized in terms of volume, pitch and trigger frequency.</span></span> <span data-ttu-id="80f6c-149">これには、方向性の強化、理解、アンビエンスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="80f6c-149">This creates an ambience with an enhanced sense of directionality.</span></span> <span data-ttu-id="80f6c-150">Aguas Calientes でなどをリッスンできる方法パノラマの各作業領域が特定の発信機を意図的に、geography が全体的な没入型のアンビエンスを作成するための作業の特定の領域を強調します。</span><span class="sxs-lookup"><span data-stu-id="80f6c-150">In Aguas Calientes, for example, you can listen to how each quadrant of the panorama has specific emitters that intentionally highlight specific areas of the geography, but work together to create an overall immersive ambience.</span></span>

## <a name="tips-and-tricks"></a><span data-ttu-id="80f6c-151">ヒントとテクニック</span><span class="sxs-lookup"><span data-stu-id="80f6c-151">Tips and tricks</span></span>

<span data-ttu-id="80f6c-152">一緒に配置しているときに、シーンのオーディオ、メソッドがあるいくつか追加 HoloLens サウンドの空間機能の使用をさらに方向性と immersion、強調表示に使用できます。</span><span class="sxs-lookup"><span data-stu-id="80f6c-152">When you're putting together audio for a scene, there are some additional methods you can use to further highlight directionality and immersion, making full use of the spatial sound capabilities of HoloLens.</span></span> <span data-ttu-id="80f6c-153">以下のいくつか用意されています: HoloTour しようとする、次回そのリッスンします。</span><span class="sxs-lookup"><span data-stu-id="80f6c-153">We've provided a list of some below—listen for them the next time you try HoloTour.</span></span>
* <span data-ttu-id="80f6c-154">**ターゲットの検索**:これらは、特定のオブジェクトまたは holographic のフレームの領域で検索する場合にのみトリガーするサウンドです。</span><span class="sxs-lookup"><span data-stu-id="80f6c-154">**Look Targets**: These are sounds that trigger only when you are looking at a specific object or area of the holographic frame.</span></span> <span data-ttu-id="80f6c-155">たとえば、ローマの Piazza Navona で street 側カフェの方向に検索しても、ビジー状態のレストランのサウンドにはトリガー微妙です。</span><span class="sxs-lookup"><span data-stu-id="80f6c-155">For example, looking in the direction of the street-side café in Rome's Piazza Navona will subtly trigger the sounds of a busy restaurant.</span></span>
* <span data-ttu-id="80f6c-156">**ローカルのビジョン**:旅は、HoloTour ツアーのガイドで、特定の beats 含まれていますが、ホログラムによって支援されています学びます詳細なトピック。</span><span class="sxs-lookup"><span data-stu-id="80f6c-156">**Local Vision**: The journey though HoloTour contains certain beats where your tour guide, aided by holograms, will explore a topic in-depth.</span></span> <span data-ttu-id="80f6c-157">たとえば、ように、Pantheon のファサードを表示、oculus ディゾルブ、reverberating オーディオは、Pantheon の内側から 3D エミッタ内部モデルを調べるためのユーザーを採用するように配置されます。</span><span class="sxs-lookup"><span data-stu-id="80f6c-157">For instance, as the façade of the Pantheon dissolves to reveal the oculus, reverberating audio placed as a 3D emitter from the inside of the Pantheon encourages the user to explore the interior model.</span></span>
* <span data-ttu-id="80f6c-158">**方向性を強化**:多くのシーン内で、方向に追加するさまざまな方法でサウンドを配置します。</span><span class="sxs-lookup"><span data-stu-id="80f6c-158">**Enhanced directionality**: Within many scenes, we placed sounds in various ways to add to the directionality.</span></span> <span data-ttu-id="80f6c-159">Pantheon のシーンでなど、噴水のサウンドが配置 'sonic 視差' のプレイ領域を歩いていたアクセスできるようにユーザーに十分な独立したエミッタ閉じます。</span><span class="sxs-lookup"><span data-stu-id="80f6c-159">In the Pantheon scene, for example, the sound of the fountain was placed as a separate emitter close enough to the user so that they could get a sense of ‘sonic parallax’ as they walked around the play space.</span></span> <span data-ttu-id="80f6c-160">ペルーの Salinas de Maras シーンでは、ほとんどのストリームの一部の個々 のパースペクティブは、その場所の音声を認証でユーザーを囲む没入感が向上のアンビエント環境を構築する個別の発信機として配置されていた。</span><span class="sxs-lookup"><span data-stu-id="80f6c-160">In Peru's Salinas de Maras scene, the individual perspective of some of the little streams were placed as separate emitters to build a more immersive ambient environment, surrounding the user with the authentic sounds of that location.</span></span>
* <span data-ttu-id="80f6c-161">**スプライン エミッタ**:この特別な空間サウンド エミッタは、3 D 空間にアタッチされているオブジェクトのビジュアルの位置を基準に移動します。</span><span class="sxs-lookup"><span data-stu-id="80f6c-161">**Spline emitter**: This special spatial sound emitter moves in 3D space relative to the visual position of the object it's attached to.</span></span> <span data-ttu-id="80f6c-162">この例では、方向性と移動の個別感を与えるのスプライン エミッタ使いましたマチュピチュでトレーニングをしました。</span><span class="sxs-lookup"><span data-stu-id="80f6c-162">An example of this was the train in Machu Picchu, where we used a spline emitter to give a distinct sense of directionality and movement.</span></span>
* <span data-ttu-id="80f6c-163">**音楽と SFX**:その図案化された場合、または映画のようなアプローチを表す HoloTour の特定の側面は、感情的な影響を強化するために、音楽とサウンド効果を使用します。</span><span class="sxs-lookup"><span data-stu-id="80f6c-163">**Music and SFX**: Certain aspects of HoloTour that represent a more stylized or cinematic approach use music and sound effects to heighten the emotional impact.</span></span> <span data-ttu-id="80f6c-164">ローマ ツアーの最後に gladiator 戦い、whooshes または stingers など、特殊効果は、シーンに表示されるラベルの効果を強化するために使用されていました。</span><span class="sxs-lookup"><span data-stu-id="80f6c-164">In the gladiator battle at the end of the Rome tour, special effects like whooshes or stingers were used to help strengthen the effect of labels appearing in scenes.</span></span>

## <a name="about-the-author"></a><span data-ttu-id="80f6c-165">執筆者紹介</span><span class="sxs-lookup"><span data-stu-id="80f6c-165">About the author</span></span>

<table style="border-collapse:collapse">
<tr>
<td style="border-style: none" width="60px"><img alt="Picture of Jason Syltebo" width="60" height="60" src="images/syltebo.png"></td>
<td style="border-style: none"><span data-ttu-id="80f6c-166"><b>Jason Syltebo</b></span><span class="sxs-lookup"><span data-stu-id="80f6c-166"><b>Jason Syltebo</b></span></span><br><span data-ttu-id="80f6c-167">オーディオのデザイナー @Microsoft</span><span class="sxs-lookup"><span data-stu-id="80f6c-167">Audio Designer @Microsoft</span></span></td>
</tr>
</table>

## <a name="see-also"></a><span data-ttu-id="80f6c-168">関連項目</span><span class="sxs-lookup"><span data-stu-id="80f6c-168">See also</span></span>
* [<span data-ttu-id="80f6c-169">空間のサウンド</span><span class="sxs-lookup"><span data-stu-id="80f6c-169">Spatial sound</span></span>](spatial-sound.md)
* [<span data-ttu-id="80f6c-170">サウンドの空間の設計</span><span class="sxs-lookup"><span data-stu-id="80f6c-170">Spatial sound design</span></span>](spatial-sound-design.md)
* [<span data-ttu-id="80f6c-171">Unity での空間のサウンド</span><span class="sxs-lookup"><span data-stu-id="80f6c-171">Spatial sound in Unity</span></span>](spatial-sound-in-unity.md)
* [<span data-ttu-id="80f6c-172">MR 空間 220</span><span class="sxs-lookup"><span data-stu-id="80f6c-172">MR Spatial 220</span></span>](holograms-220.md)
* [<span data-ttu-id="80f6c-173">ビデオ:Microsoft HoloLens の場合:HoloTour</span><span class="sxs-lookup"><span data-stu-id="80f6c-173">Video: Microsoft HoloLens: HoloTour</span></span>](https://www.youtube.com/watch?v=pLd9WPlaMpY)

 