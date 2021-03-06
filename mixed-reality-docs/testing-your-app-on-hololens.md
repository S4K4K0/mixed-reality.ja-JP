---
title: HoloLens でのアプリのテスト
description: HoloLens アプリのテストに関するガイダンスと提案
author: jonmlyons
ms.author: jlyons
ms.date: 02/24/2019
ms.topic: article
keywords: HoloLens, テスト
ms.openlocfilehash: 3ab5eeec4046b81dc41db51ae138eb9d1069d1ff
ms.sourcegitcommit: d6ac8f1f545fe20cf1e36b83c0e7998b82fd02f8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2020
ms.locfileid: "81277590"
---
# <a name="testing-your-app-on-hololens"></a>HoloLens でのアプリのテスト

HoloLens アプリケーションのテストは、Windows アプリケーションのテストとよく似ています。 通常のすべての領域 (機能、相互運用性、パフォーマンス、セキュリティ、信頼性など) を考慮する必要があります。 ただし、PC や電話のアプリでは通常見られない特別な処理や詳細への対処が必要な領域もあります。 Holographic アプリは、さまざまな環境のセットでスムーズに実行する必要があります。 また、パフォーマンスとユーザーの快適さを常に維持する必要もあります。 これらの領域のテストに関するガイダンスについては、このトピックで詳しく説明します。

## <a name="performance"></a>パフォーマンス テスト

Holographic アプリは、さまざまな環境のセットでスムーズに実行する必要があります。 また、パフォーマンスとユーザーの快適さを常に維持する必要もあります。 Holographic アプリのユーザーエクスペリエンスにとってパフォーマンスが非常に重要です。これには、トピック全体が含まれています。 [Mixed Reality のパフォーマンスを理解](understanding-performance-for-mixed-reality.md)し、それに従っていることを確認してください。

## <a name="testing-3d-in-3d"></a>3D でのテスト
1. **できるだけ多くの異なるスペースでアプリをテストします。** 大規模な部屋、小さな部屋、bathrooms、kitchens、ベッドルーム、オフィスなどで試してみてください。また、縦棒以外の壁面、曲線の壁面、水平でない雲など、標準以外の機能を備えたルームも考慮してください。 部屋、フロア、廊下または階段間を移行するときにうまく機能しますか。
2. **さまざまな照明条件でアプリをテストします。** 照明、黒い表面、反射/反射の面 (鏡など)、ガラスの壁など、さまざまな環境に適切に対応します。
3. **さまざまな動作条件でアプリをテストします。** デバイスに配置して、さまざまな動作の状態でシナリオを試すことができます。 異なる移動や安定した状態に対応していますか。
4. **さまざまな角度からアプリがどのように動作するかをテストします。** 世界でロックされているホログラムを使用している場合、ユーザーがその背後にいるとどうなりますか。 ユーザーとホログラムの間に何かがあるとどうなりますか。 ユーザーがホログラムを上または下から見た場合はどうなるでしょうか。
5. **空間およびオーディオキューを使用します。** ユーザーが紛失するのを防ぐために、アプリでこれらを使用するようにしてください。
6. **さまざまなレベルのアンビエントノイズでアプリをテストします。** 音声コマンドを実装している場合は、さまざまなレベルのアンビエントノイズで呼び出します。
7. アプリが取り付けられて**いることをテスト**します。 座席と地位の両方からテストするようにしてください。
8. **さまざまな距離からアプリをテスト**します。 UI 要素を遠く離れた場所から読み取ることができますか。 アプリは、ホログラムに近すぎるユーザーに反応しますか。
9. アプリを**共通のアプリバーとの対話に対してテスト**します。 すべてのアプリタイルと2D ユニバーサルアプリには、アプリが混合世界でどのように配置されるかを制御できる[アプリバー](navigating-the-windows-mixed-reality-home.md#moving-and-adjusting-apps)があります。 [削除] をクリックすると、アプリプロセスが正常に終了し、[戻る] ボタンが2D ユニバーサルアプリのコンテキスト内でサポートされていることを確認します。 アクティブになっている間、およびアプリが中断されたアプリのタイルである間は、[調整モード](navigating-the-windows-mixed-reality-home.md#moving-and-adjusting-apps)でアプリケーションをスケーリングして移動してみてください。

### <a name="environmental-test-matrix"></a>環境テストマトリックス

![HoloLens アプリ開発のための環境テストマトリックス](images/environment-matrix-600px.png)

## <a name="comfort"></a>快適性
1. **クリッププレーン。** [ホログラムがレンダリング](hologram-stability.md#hologram-render-distances)される場所に attentive してください。
2. **仮想移動は、実際のヘッド移動と矛盾しないようにしてください。** ユーザーの実際の動きを代表しない方法でカメラを移動しないようにします。 アプリでシーンを通じてユーザーを移動する必要がある場合は、動きを予測可能にし、加速を最小化して、ユーザーが移動を制御できるようにします。
3. **ホログラムの品質ガイドラインに従います。** [ホログラム品質ガイダンス](hologram-stability.md)を実装する高性能アプリでは、ユーザー不快感が発生する可能性が低くなります。
4. **ホログラムを垂直方向ではなく水平方向に分散します。** ユーザーが長時間にわたって長い期間を使用するように強制すると、ネックの疲労につながる可能性があります。


## <a name="input"></a>入力

### <a name="interaction-models"></a>操作モデル

ホログラムの相互作用が、選択した[相互作用モデル](interaction-fundamentals.md)と連携していることを確認します。
また、ユーザー補助機能をサポートするためにこれらのアクセサリが必要な場合は、マウスやキーボードなどのさまざまなアクセサリで検証することをお勧めします。

**アプリの動作がマウスとタッチで異なる場合に検証します。** これにより、不整合が特定され、ユーザーにより自然なエクスペリエンスを実現するための設計上の決定に役立ちます。 たとえば、ホバーに基づいてアクションをトリガーします。


### <a name="custom-voice-commands"></a>カスタム音声コマンド

[音声入力](voice-input.md)は、自然な形でやり取りされます。 ユーザーエクスペリエンスは、選択したコマンドとそれらを公開する方法によって、魔法または混乱を招く可能性があります。 ルールとして、"Select" や "Cortana" などのシステム音声コマンドをカスタムコマンドとして使用しないでください。 次に、考慮すべき点をいくつか示します。
1. **類似していると思われるコマンドは使用しないでください。** これにより、正しくないコマンドがトリガーされる可能性があります。
2. **可能な場合は、発音豊富な単語を選択します。** これにより、誤ライセンス認証が最小化または回避されます。

### <a name="peripherals"></a>周辺機器

ユーザーは、[周辺機器](hardware-accessories.md)を使用してアプリと対話できます。 アプリでは、その機能を利用するために特別な操作を行う必要はありませんが、いくつかの点を確認する必要があります。
1. **カスタムの相互作用を検証します。** アプリのカスタムキーボードショートカットのようなものです。
2. **入力の種類の切り替えを検証します。** 同じシナリオで、複数の入力方法を使用して、音声、ジェスチャ、マウス、キーボードなどのタスクを完了しようとしています。

## <a name="system-integration"></a>システム統合

### <a name="battery"></a>バッテリー

電源が接続されていない状態でアプリケーションをテストし、バッテリの消費速度を把握します。 電源 LED の測定を見ることで、バッテリの状態を簡単に把握できます。 

![バッテリ電源を示す LED の状態](images/batterypowerledindication-500px.png)<br>

*バッテリ電源を示す LED の状態*

### <a name="power-state-transitions"></a>電源状態の移行

電源状態間の移行時に、キーシナリオの検証が期待どおりに動作することを確認します。 たとえば、アプリケーションは元の位置に残りますか。 状態が正常に保持されていますか。 予期したとおりに機能しますか。
1. **[スタンバイ/再開]。** スタンバイに入るには、すぐに電源ボタンを押して離すことができます。 デバイスは、非アクティブな状態が3分続くと自動的にスタンバイ状態になります。 スタンバイから再開するには、すぐに電源ボタンを押して離すことができます。 デバイスは電源に接続するか、電源を切断した場合にも再開されます。
2. **[シャットダウン/再起動]。** シャットダウンするには、電源ボタンを6秒間連続して押したままにします。 再起動するには、電源ボタンを押します。

### <a name="multi-app-scenarios"></a>複数アプリのシナリオ

特にバックグラウンドタスクが実装されている場合は、アプリ間を切り替えるときにアプリのコア機能を検証します。 コピー/貼り付けと Cortana 統合は、該当する場合にも確認する価値があります。

## <a name="telemetry"></a>製品利用統計情報

テレメトリと分析を使用してガイドを作成できます。 Analytics をアプリに統合することで、ベータテスターやエンドユーザーからアプリに関する洞察を得ることができます。 このデータを使用して、ストアに送信する前にアプリを最適化したり、将来の更新に使用したりできます。 分析オプションは多数あります。 どこから始めるかわからない場合は、「 [App Insights](https://www.visualstudio.com/products/application-insights-vs.aspx)」をご覧ください。

考慮すべき質問:
1. ユーザーはどのようにスペースを使用していますか。
2. アプリがどのように世界中にオブジェクトを配置しているか。問題を検出できますか。
3. アプリケーションのさまざまな段階にどれくらいの時間がかかっていますか。
4. アプリにはどのくらいの時間がかかるのでしょうか。
5. ユーザーが実行しようとしている最も一般的な使用パスは何ですか。
6. ユーザーは予期しない状態やエラーに達していますか。

## <a name="emulator-and-simulated-input"></a>エミュレーターとシミュレートされた入力

[HoloLens emulator](using-the-hololens-emulator.md)は、シミュレートされたさまざまなユーザー特性とスペースを使用して Holographic アプリを効率的にテストするための優れた方法です。 アプリをテストするためにエミュレーターを効果的に使用するための推奨事項を次に示します。
1. **エミュレーターの仮想ルームを使用して、テストを拡張します。** エミュレーターには、さらに多くの環境でアプリをテストするために使用できる一連の仮想ルームが付属しています。
2. **エミュレーターを使用して、あらゆる角度からアプリを確認します。** Pageup キー/PageDn キーを使用すると、シミュレートされたユーザーの高さが高くなります。
3. **実際の HoloLens でアプリをテストします。** HoloLens エミュレーターは、アプリを迅速に反復処理し、新しいバグをキャッチするのに役立つ優れたツールですが、Windows ストアに送信する前に、物理 HoloLens でもテストするようにしてください。 これは、実際のハードウェアでパフォーマンスとエクスペリエンスが優れていることを確認するために重要です。

## <a name="automated-testing-with-perception-simulation"></a>知覚シミュレーションによる自動テスト

アプリ開発者によっては、アプリのテストを自動化することが必要になる場合があります。 単純な単体テスト以外に、HoloLens の[知覚シミュレーション](perception-simulation.md)スタックを使用して、アプリへの人間と世界の入力を自動化できます。 認識シミュレーション API は、HoloLens エミュレーターまたは物理 HoloLens のいずれかにシミュレートされた入力を送信できます。

## <a name="windows-app-certification-kit"></a>Windows アプリ認定キット

アプリを[Windows ストアで公開](submitting-an-app-to-the-microsoft-store.md)する機会を与えるには、証明書を送信する前に、ローカルで検証してテストします。 アプリが Holographic デバイスファミリを対象としている場合、 [Windows アプリ認定キット](https://msdn.microsoft.com/library/windows/apps/xaml/mt186449.aspx)では、ローカルの静的分析テストのみが PC 上で実行されます。 HoloLens ではテストは実行されません。

## <a name="see-also"></a>参照
* [Windows ストアへのアプリの送信](submitting-an-app-to-the-microsoft-store.md)
