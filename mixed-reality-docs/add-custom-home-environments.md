---
title: 独自のイマーシブ環境を設計する
description: 提供する Windows Mixed Reality ホーム環境に加えて、独自のを作成して使用することもできます。
author: thmignon
ms.author: thmignon
ms.date: 04/30/2018
ms.topic: article
keywords: Windows Mixed Reality、Mixed Reality、Virtual Reality、VR、MR、Home、Custom Environment、地名、崖ハウス、skyloft、user、create
ms.openlocfilehash: e133e1438410540592a51f54ed136aecd04c6244
ms.sourcegitcommit: 6bc6757b9b273a63f260f1716c944603dfa51151
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "73437073"
---
# <a name="design-your-own-immersive-environments"></a>独自のイマーシブ環境を設計する

>[!NOTE]
>これは試験的な機能です。 試してみてください。しかし、すべてが期待どおりに動作しない場合、驚かれることはありません。 この機能の有効性を評価し、それを使用することに関心があるので、[開発者フォーラム](https://forums.hololens.com/categories/custom-home-environments)で、経験 (および発見したバグ) についてご意見をお聞かせください。

[Windows 10 April 2018 update](release-notes-april-2018.md)以降では、 [windows Mixed Reality ホーム](navigating-the-windows-mixed-reality-home.md)として使用するカスタム環境を [スタート] メニューの [場所] ピッカーに追加できる実験的な機能が有効になりました。 Windows Mixed Reality には、2つの既定の環境 (崖家と Skyloft) があり、これをホームとして選択することができます。 カスタム環境を作成すると、独自の作成でそのリストを拡張できます。 これを早期の状態で使用できるようにして、作成者と開発者の関心を評価し、作成した世界の種類を確認し、さまざまな作成ツールの使用方法を理解します。

カスタム環境を使用すると、Skyloft が崖家やの場合と同じように、テレ移植、アプリとの対話、およびホログラムの配置が行われます。 Web を fantasy ランドスケープで閲覧したり、ホログラムを使用して futuristic の都市を埋めることができます。可能性は無限です。

## <a name="device-support"></a>デバイスのサポート

<table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <tr>
        <td><strong>機能</strong></td>
        <td><a href="hololens-hardware-details.md"><strong>HoloLens</strong></a></td>
        <td><a href="immersive-headset-hardware-details.md"><strong>イマーシブ ヘッドセット</strong></a></td>
    </tr>
     <tr>
        <td>カスタムホーム環境</td>
        <td>❌</td>
        <td>✔️</td>
    </tr>
</table>

## <a name="trying-a-sample-environment"></a>サンプル環境を試す

カスタムホーム環境の独創的な可能性を示すサンプル環境を作成しました。 次の手順に従って試してみてください。
1. [サンプル Fantasy アイランド環境](https://download.microsoft.com/download/B/2/5/B25C1AEF-40CD-4B03-A596-4BCA3D33035A/Fantasy_Island.exe)(自己解凍形式の実行可能ファイルへのリンクポイント) をダウンロードします。

    ![Fantasy アイランドのサンプル環境](images/FantasyLand.jpg)<br>
    *Fantasy 島のサンプル環境*<br>

2. ダウンロードした**Fantasy_Island**ファイルを実行します。

    > [!NOTE]
    > Web からダウンロードした .exe ファイルを実行しようとすると (この例のように)、"Windows で保護されている PC" ポップアップが表示されることがあります。 このポップアップから Fantasy_Island を実行するには、 **[詳細情報]** を選択し、 **[実行]** をクリックします。 このセキュリティ設定は、信頼しないファイルのダウンロードを防止するためのものであるため、ファイルのソースを信頼する場合にのみ、このオプションを選択してください。

3. **ファイルエクスプローラー**を開き、アドレスバーに次のように貼り付けて、環境 フォルダーに移動します。 `%LOCALAPPDATA%\Packages\EnvironmentsApp_cw5n1h2txyewy\LocalState` を参照してください。
4. ダウンロードしたサンプル環境をこのフォルダーにコピーします。
5. **Mixed Reality ポータル**を再起動します。 これにより、[場所の選択] の環境の一覧が更新されます。
6. ヘッドセットに配置します。 自宅にいる場合は、コントローラーで [Windows] ボタンを使用して [**スタート] メニュー**を開きます。
7. ピン留めされたアプリの一覧の上にある **[場所]** アイコンを選択して、ホーム環境を選択します。
8. ダウンロードした Fantasy アイランド環境が、場所の一覧に表示されます。 **[Fantasy 島]** を選択して、新しいカスタムホーム環境に入ります。

## <a name="creating-your-own-custom-environment"></a>独自のカスタム環境を作成する

このサンプル環境を使用するだけでなく、お好きな3D 編集ソフトウェアを使用して、独自のカスタム環境をエクスポートすることもできます。 

### <a name="modeling-guidelines"></a>モデリングガイドライン

環境をモデリングする場合は、次の推奨事項を考慮してください。 これにより、ユーザーが believably サイズの世界で正しい向きで生成されるようになります。

1. ユーザーは 0, 0, 0 で起動します。これにより、元の場所を中心にして目的の場所を作成できます。
2. 資産を世界規模で作成できるように、作業単位をメーターに設定する必要があります。
3. 上の軸を "Y" に設定する必要があります。
4. 資産は正の Z 軸に "進む" ようになります。
5. すべてのメッシュを結合する必要はありませんが、リソースを制限するデバイスを対象とする場合にお勧めします。

### <a name="exporting-your-environment"></a>環境のエクスポート

Windows Mixed Reality は、環境の資産配信形式としてバイナリ glTF (. glb) に依存しています。 glTF は、Khronos グループによって維持される、3D 資産配信用のロイヤリティフリーオープンスタンダードです。 GlTF は相互運用可能な3D コンテンツの業界標準として進化しているため、Microsoft は Windows アプリとエクスペリエンス全体の形式をサポートしています。

カスタムホーム環境として使用するアセットをエクスポートする最初の手順として、glTF 2.0 モデルが生成されます。 GlTF 作業グループは、[サポートされているエクスポーターとコンバーターの一覧](https://github.com/KhronosGroup/glTF/blob/master/README.md#converters-and-exporters)を保持し、gltf 2.0 モデルを作成します。 開始するには、このページに記載されているいずれかのプログラムを使用して、glTF 2.0 モデルを作成してエクスポートするか、サポートされているいずれかのコンバーターを使用して既存のモデルを変換します。

また、Blender と 3DS Max から直接、glTF モデルをエクスポートするための最先端のワークフローの概要については、こちらの[役に立つ記事](https://www.khronos.org/blog/art-pipeline-for-gltf)をご覧ください。 

### <a name="environment-limits"></a>環境の制限

すべての環境は 256 mbs < なければなりません。 256 mbs を超える環境では、ユーザーを囲む既定のスカイボックスのみを使用して、空の世界への読み込みとフォールバックが失敗します。 モデルの作成時には、このファイルサイズの制限に留意してください。 さらに、以下で説明するように WindowsMRAssetConverter を使用して環境を最適化する場合は、ファイルサイズが大きく、読み込みが高速になるテクスチャを作成するときにテクスチャサイズが増加することを cognizant してください。 

### <a name="optimizing-your-environment"></a>環境の最適化

Windows Mixed Reality では、環境の読み込み時間を大幅に短縮する、いくつかのオプションの最適化がサポートされています。 これは、多くのテクスチャを持つ環境では特に重要です。読み込み中にタイムアウトすることがあります。 一般に、すべての資産に対してこの手順をお勧めします。ただし、少数または低解像度のテクスチャを使用する小規模な環境では、常に必要になるとは限りません。 

このプロセスを簡単にするために、 [Windows Mixed Reality 資産コンバーター (GitHub で入手できます)](https://github.com/Microsoft/glTF-Toolkit/releases)を作成し、最適化を実行しました。 このツールでは、Microsoft glTF toolkit で利用できる一連のユーティリティを使用して、追加のテクスチャパッキング、圧縮、および解像度のスケールダウンを実行することで、標準の 2.0 glTF または glb を最適化します。 

現在、コンバーターでは、最適化の正確な動作を調整するための多数のフラグがサポートされています。 最良の結果を得るには、次のフラグを使用してを実行することをお勧めします。

Flag|推奨値|説明
---|---|---
-max-テクスチャ-サイズ|1024または2048| テクスチャの品質を向上させるためにこれを微調整します。既定値は512x512 です。 大きな値を指定すると、環境のファイルサイズに大きく影響するため、256 mb の制限を考慮してください。
-最小バージョン|1803|カスタム環境は、windows > = 1803 のバージョンでのみサポートされています。 このフラグは、古いバージョンのテクスチャを削除し、最終的な資産のファイルサイズを縮小します

次に、例を示します。

```cmd
WindowsMRAssetConverter FileToConvert.gltf -max-texture-size 1024 -min-version 1803
```

### <a name="testing-your-environment"></a>環境のテスト

Glb 環境が完成したら、ヘッドセットでテストする準備が整います。 カスタム環境を mixed reality ホームとして使用する場合は、 [「サンプル環境を試す」](#trying-a-sample-environment)セクションの手順2から開始します。 

## <a name="feedback"></a>Feedback

この試験的な機能を評価していますが、ここでは、カスタム環境の使用方法、発生する可能性があるすべてのバグ、および機能の好みについて説明します。 [開発者フォーラム](https://forums.hololens.com/categories/custom-home-environments)でカスタムホーム環境を作成および使用するためのすべてのフィードバックを共有してください。

## <a name="troubleshooting-and-tips"></a>トラブルシューティングとヒント

### <a name="how-do-i-change-the-name-of-the-environment"></a>環境の名前を変更操作方法には

[環境] フォルダー内のファイル名は、[場所の選択] で使用されます。 環境の名前を変更するには、環境のファイル名の名前を変更し、Mixed Reality ポータルを再起動します。

### <a name="how-do-i-remove-custom-environments-from-my-places-picker"></a>マイプレースピッカーからカスタム環境を削除操作方法には

カスタム環境を削除するには、PC の環境フォルダー (`%LOCALAPPDATA%\Packages\EnvironmentsApp_cw5n1h2txyewy\LocalState`) を開き、環境を削除します。 Mixed Reality ポータルを再起動すると、この環境は [場所の選択] に表示されなくなります。 

### <a name="how-do-i-default-to-my-favorite-custom-environment"></a>お気に入りのカスタム環境に既定操作方法しますか?

現在、既定の環境を変更することはできません。 Mixed Reality ポータルを再起動するたびに、崖ハウス環境に戻ります。 

### <a name="i-spawn-into-a-blank-space"></a>空のスペースを生成する

Windows Mixed Reality[では、256 mb を超える環境はサポートされていません](#environment-limits)。 環境がこの制限を超えると、モデルのない空のスカイボックスが表示されます。

### <a name="it-takes-a-long-time-to-load-my-environment"></a>環境の読み込みに時間がかかる

環境にオプションの最適化を追加して、読み込みを高速化することができます。 詳細については[、「環境の最適化」](#optimizing-your-environment)を参照してください。

### <a name="the-scale-of-my-environment-is-incorrect"></a>環境のスケールが正しくありません

Windows Mixed Reality は、環境の読み込み時に glTF units を1メートルに変換します。 環境で予期しないスケールが読み込まれる場合は、エクスポーターを再確認して、1メートルのスケールでモデル化されていることを確認します。 

### <a name="the-spawn-location-in-my-environment-is-incorrect"></a>環境内の生成場所が正しくありません

既定の生成場所は、環境内の0、0、0にあります。 現在、この場所をカスタマイズすることはできません。そのため、必要な生成ポイントに配置された元の環境をエクスポートして、生成ポイントを変更する必要があります。

### <a name="the-audio-doesnt-sound-correct-in-the-environment"></a>環境内のオーディオが正しく聞こえない

カスタム環境を作成すると、作成した物理空間に一致しない acoustics レンダリングシミュレーションが使用されます。 サウンドが間違った方向にある可能性があり、muffled が聞こえる可能性があります。 

## <a name="see-also"></a>関連項目
* [Windows Mixed Reality 資産コンバーター (GitHub)](https://github.com/Microsoft/glTF-Toolkit/releases)

