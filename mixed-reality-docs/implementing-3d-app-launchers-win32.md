---
title: 3D アプリランチャーの実装 (Win32 アプリ)
description: Win32 VR アプリおよびゲーム用の3D アプリランチャーおよびロゴを作成する方法 (ストリームの外部に分散)。これらのアプリケーションは、Windows Mixed Reality の [スタート] メニューと [ホーム] 環境に表示されます。
author: thmignon
ms.author: thmignon
ms.date: 07/12/2018
ms.topic: article
keywords: 3D、ロゴ、アイコン、モデリング、ランチャー、3D ランチャー、タイル、live cube、win32
ms.openlocfilehash: 87eadfb5184f9fb5f8d513ab00a2a954e71df376
ms.sourcegitcommit: 6bc6757b9b273a63f260f1716c944603dfa51151
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "73438578"
---
# <a name="implement-3d-app-launchers-win32-apps"></a>3D アプリランチャーの実装 (Win32 アプリ)

> [!NOTE]
> この機能は、最新の[Windows Insider](https://insider.windows.com)便 (RS5)、ビルド17704以降を実行している pc でのみ使用できます。

[Windows Mixed Reality ホーム](navigating-the-windows-mixed-reality-home.md)は、アプリケーションを起動する前にユーザーが移動する開始点です。 既定では、イマーシブ Win32 VR アプリとゲームはヘッドセットの外部から起動する必要があり、Windows Mixed Reality の [スタート] メニューの [すべてのアプリ] の一覧には表示されません。 ただし、この記事の手順に従って3D アプリランチャーを実装することで、Windows Mixed Reality の [スタート] メニューと [ホーム] 環境からイマーシブ Win32 VR エクスペリエンスを起動できます。

これは、蒸気の外部で distributied の Win32 VR エクスペリエンスを使用する場合にのみ当てはまります。 [ストリームによって配布](updating-your-steamvr-application-for-windows-mixed-reality.md)される VR エクスペリエンスの場合、Windows [Mixed Reality For Steamvr Beta](https://steamcommunity.com/games/719950/announcements/detail/1687045485866139800)と最新の windows Insider RS5 フライトを更新しました。これにより、"すべてのアプリ" リストの windows Mixed reality の [スタート] メニューに steamvr タイトルが表示されます。既定のランチャーを自動的に使用します。 言い換えると、この記事で説明されている方法は SteamVR タイトルには不要であり、Windows Mixed Reality for SteamVR Beta 機能によって上書きされます。

## <a name="3d-app-launcher-creation-process"></a>3D アプリランチャー作成プロセス

3D アプリランチャーを作成するには、次の3つの手順を実行します。
1. [設計と concepting](3d-app-launcher-design-guidance.md)
2. [モデリングとエクスポート](creating-3d-models-for-use-in-the-windows-mixed-reality-home.md)
3. アプリケーションへの統合 (この記事)

アプリケーションのランチャーとして使用する3D アセットは、互換性を確保するために、 [Windows Mixed Reality オーサリングガイドライン](creating-3d-models-for-use-in-the-windows-mixed-reality-home.md)を使用して作成する必要があります。 このオーサリング仕様に合わなかった資産は、Windows Mixed Reality ホームではレンダリングされません。

## <a name="configuring-the-3d-launcher"></a>3D ランチャーの構成

Win32 アプリケーションは、Windows Mixed Reality の [スタート] メニューの [すべてのアプリ] の一覧に表示されます (3D アプリランチャーを作成した場合)。 これを行うには、次の手順に従って、3D アプリランチャーを参照する[ビジュアル要素マニフェスト](https://msdn.microsoft.com/library/windows/apps/dn393983.aspx)XML ファイルを作成します。

1. **3D アプリランチャー ASSET GLB ファイル**を作成します (「[モデリングとエクスポート](creating-3d-models-for-use-in-the-windows-mixed-reality-home.md)」を参照してください)。
2. アプリケーションの **[ビジュアル要素マニフェスト](https://msdn.microsoft.com/library/windows/apps/dn393983.aspx)** を作成します。
    1. [次のサンプル](#sample-visual-elements-manifest)から始めることができます。  詳細については、[ビジュアル要素](https://msdn.microsoft.com/library/windows/apps/dn393983.aspx)の完全なマニフェストに関するドキュメントを参照してください。
    2. アプリの PNG/JPG/GIF で**Square150x150Logo**と**Square70x70Logo**を更新します。
        * これらは、Windows Mixed Reality のすべてのアプリの一覧とデスクトップの [スタート] メニューのアプリの2D ロゴに使用されます。
        * ファイルパスは、ビジュアル要素マニフェストを含むフォルダーに対する相対パスです。
        * その場合でも、標準のメカニズムを使用して、アプリのデスクトップの [スタート] メニューアイコンを指定する必要があります。 これは、実行可能ファイルまたは作成したショートカット (IShellLink:: SetIconLocation など) に直接配置できます。
        * *省略可能:* MRT.DLL がさまざまな解像度スケールとハイコントラストテーマに対して複数のアセットサイズを提供する場合は、リソースの pri ファイルを使用できます。
    3. 3D アプリランチャーの GLB をポイントするように**MixedRealityModel パス**を更新します。
    4. "" という拡張子を持つ実行可能ファイルと同じ名前のファイルを保存します。Visualを Manifest.xml し、同じディレクトリに保存します。 たとえば、実行可能ファイル "al.exe" の場合、付随する XML ファイルの名前は "contoso. visual、.manifest" になります。
3. アプリケーションへの**ショートカットを**デスクトップの [スタート] メニューに追加します。 実装の例C++については、[次のサンプル](#sample-app-launcher-shortcut-creation)を参照してください。 
    * %ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs (machine) または%APPDATA%\Microsoft\Windows\Start Menu\Programs (user) で作成する
    * 更新によって、ビジュアル要素マニフェストまたはそれによって参照される資産が変更された場合、更新プログラムによって、マニフェストが再解析され、キャッシュされたアセットが更新されるようにショートカットが更新されます。
4. *省略可能:* デスクトップショートカットがアプリケーションの EXE を直接指していない場合 (たとえば、"myapp://" のようなカスタムプロトコルハンドラーが呼び出された場合)、[スタート] メニューでアプリの Visual要素のマニフェストファイルが自動的に検索されません。 これを解決するには、ショートカットで VisualElementsManifestHintPath () を使用して、ビジュアル要素マニフェストのファイルパスを指定する必要があります。 これは、System.AppUserModel.ID と同じ手法を使用して、ショートカットで設定できます。 System.AppUserModel.ID を使用する必要はありませんが、アプリケーションの明示的なアプリケーションユーザーモデル ID が使用されている場合に、そのショートカットに一致するように指定することもできます。  サンプルについては、後の「[サンプルアプリランチャーショートカットの作成](#sample-app-launcher-shortcut-creation)」セクションを参照してください。 C++

### <a name="sample-visual-elements-manifest"></a>ビジュアル要素マニフェストのサンプル

```xml
<Application xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance">
  <VisualElements
    ShowNameOnSquare150x150Logo="on"
    Square150x150Logo="YOUR_APP_LOGO_150X150.png"
    Square70x70Logo=" YOUR_APP_LOGO_70X70.png"
    ForegroundText="light"
    BackgroundColor="#000000">
    <MixedRealityModel Path="YOUR_3D_APP_LAUNCHER_ASSET.glb">
        <SpatialBoundingBox Center="0,0,0" Extents="Auto" />
    </MixedRealityModel>
  </VisualElements>
</Application>
```

### <a name="sample-app-launcher-shortcut-creation"></a>サンプルアプリランチャーショートカットの作成

次のサンプルコードは、でC++ショートカットを作成する方法を示しています。これには、ビジュアル要素マニフェスト XML ファイルへのパスのオーバーライドが含まれます。 注: このオーバーライドは、ショートカットがマニフェストに関連付けられている EXE を直接指していない場合にのみ必要です (例: ショートカットでは、"myapp://" のようなカスタムプロトコルハンドラーを使用します)。

#### <a name="sample-lnk-shortcut-creation-c"></a>サンプル.LNK ショートカットのC++作成 ()

```cpp
#include <windows.h>
#include <propkey.h>
#include <shlobj_core.h>
#include <shlwapi.h>
#include <propvarutil.h>
#include <wrl.h>

#include <memory>

using namespace Microsoft::WRL;

#define RETURN_IF_FAILED(x) do { HRESULT hr = x; if (FAILED(hr)) { return hr; } } while(0)
#define RETURN_IF_WIN32_BOOL_FALSE(x) do { DWORD res = x; if (res == 0) { return HRESULT_FROM_WIN32(GetLastError()); } } while(0)

int wmain()
{
    RETURN_IF_FAILED(CoInitializeEx(nullptr, COINIT_APARTMENTTHREADED));

    ComPtr<IShellLink> shellLink;
    RETURN_IF_FAILED(CoCreateInstance(__uuidof(ShellLink), nullptr, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&shellLink)));
    RETURN_IF_FAILED(shellLink->SetPath(L"MyLauncher://launch/app-identifier"));

    // It is also possible to use an icon file in another location. For example, "C:\Program Files (x86)\MyLauncher\assets\app-identifier.ico".
    RETURN_IF_FAILED(shellLink->SetIconLocation(L"C:\\Program Files (x86)\\MyLauncher\\apps\\app-identifier\\game.exe", 0 /*iIcon*/));

    ComPtr<IPropertyStore> propStore;
    RETURN_IF_FAILED(shellLink.As(&propStore));

    {
        // Optional: If the application has an explict Application User Model ID, then you should usually specify it in the shortcut.
        PROPVARIANT propVar;
        RETURN_IF_FAILED(InitPropVariantFromString(L"ExplicitAppUserModelID", &propVar));
        RETURN_IF_FAILED(propStore->SetValue(PKEY_AppUserModel_ID, propVar));
        PropVariantClear(&propVar);
    }

    {
        // A hint path to the manifest is only necessary if the target path of the shortcut is not a file path to the executable.
        // By convention the manifest is named <executable name>.VisualElementsManifest.xml and is in the same folder as the executable
        // (and resources.pri if applicable). Assets referenced by the manifest are relative to the folder containing the manifest.

        //
        // PropKey.h
        //
        //  Name:     System.AppUserModel.VisualElementsManifestHintPath -- PKEY_AppUserModel_VisualElementsManifestHintPath
        //  Type:     String -- VT_LPWSTR  (For variants: VT_BSTR)
        //  FormatID: {9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3}, 31
        //  
        //  Suggests where to look for the VisualElementsManifest for a Win32 app
        //
        // DEFINE_PROPERTYKEY(PKEY_AppUserModel_VisualElementsManifestHintPath, 0x9F4C2855, 0x9F79, 0x4B39, 0xA8, 0xD0, 0xE1, 0xD4, 0x2D, 0xE1, 0xD5, 0xF3, 31);
        // #define INIT_PKEY_AppUserModel_VisualElementsManifestHintPath { { 0x9F4C2855, 0x9F79, 0x4B39, 0xA8, 0xD0, 0xE1, 0xD4, 0x2D, 0xE1, 0xD5, 0xF3 }, 31 }

        PROPVARIANT propVar;
        RETURN_IF_FAILED(InitPropVariantFromString(L"C:\\Program Files (x86)\\MyLauncher\\apps\\app-identifier\\game.visualelementsmanifest.xml", &propVar));
        RETURN_IF_FAILED(propStore->SetValue(PKEY_AppUserModel_VisualElementsManifestHintPath, propVar));
        PropVariantClear(&propVar);
    }

    constexpr PCWSTR shortcutPath = L"%APPDATA%\\Microsoft\\Windows\\Start Menu\\Programs\\game.lnk";
    const DWORD requiredBufferLength = ExpandEnvironmentStrings(shortcutPath, nullptr, 0);
    RETURN_IF_WIN32_BOOL_FALSE(requiredBufferLength);

    const auto expandedShortcutPath = std::make_unique<wchar_t[]>(requiredBufferLength);
    RETURN_IF_WIN32_BOOL_FALSE(ExpandEnvironmentStrings(shortcutPath, expandedShortcutPath.get(), requiredBufferLength));

    ComPtr<IPersistFile> persistFile;
    RETURN_IF_FAILED(shellLink.As(&persistFile));
    RETURN_IF_FAILED(persistFile->Save(expandedShortcutPath.get(), FALSE));

    return 0;
}
```

#### <a name="sample-url-launcher-shortcut"></a>サンプル.URL ランチャーショートカット 

```
[{9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3}]
Prop31=C:\Program Files (x86)\MyLauncher\apps\app-identifier\game.visualelementsmanifest.xml
Prop5=ExplicitAppUserModelID

[{000214A0-0000-0000-C000-000000000046}]
Prop3=19,0

[InternetShortcut]
IDList=
URL=MyLauncher://launch/app-identifier
IconFile=C:\Program Files (x86)\MyLauncher\apps\app-identifier\game.exe
IconIndex=0
```

## <a name="see-also"></a>関連項目

* 3D アプリランチャーを含む[Mixed reality モデルサンプル](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/MixedRealityModel)。
* [3D アプリ起動ツールの設計ガイダンス](3d-app-launcher-design-guidance.md)
* [Windows Mixed Reality ホームで使用するための3D モデルの作成](creating-3d-models-for-use-in-the-windows-mixed-reality-home.md)
* [3D アプリランチャーの実装 (UWP アプリ)](implementing-3d-app-launchers.md)
* [Windows Mixed Reality ホームのナビゲーション](navigating-the-windows-mixed-reality-home.md)
