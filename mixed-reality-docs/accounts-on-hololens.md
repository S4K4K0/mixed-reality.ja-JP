---
title: HoloLens のアカウント
description: HoloLens でアカウントを設定して、ユーザーを管理する方法。
author: ''
ms.author: toddly
ms.date: 03/21/2018
ms.topic: article
keywords: HoloLens, user, account, aad, adfs, microsoft account, msa, credentials
ms.openlocfilehash: 14f43b08b6ccb396bcf39c4082c840c65ac78cf9
ms.sourcegitcommit: 384b0087899cd835a3a965f75c6f6c607c9edd1b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/12/2019
ms.locfileid: "59599831"
---
# <a name="accounts-on-hololens"></a><span data-ttu-id="7fc26-104">HoloLens のアカウント</span><span class="sxs-lookup"><span data-stu-id="7fc26-104">Accounts on HoloLens</span></span>

<span data-ttu-id="7fc26-105">HoloLens の初期セットアップ中には、デバイスで使用するアカウントでサインインするユーザーが必要です。</span><span class="sxs-lookup"><span data-stu-id="7fc26-105">During initial HoloLens setup, users are required to sign in with the account they want to use on the device.</span></span> <span data-ttu-id="7fc26-106">このアカウントは、コンシューマー Microsoft アカウントまたは Azure Active Directory (AAD) または Active Directory フェデレーション サービス (ADFS) で構成されているエンタープライズ アカウントのいずれかにできます。</span><span class="sxs-lookup"><span data-stu-id="7fc26-106">This account can be either a consumer Microsoft account or an enterprise account that has been configured in Azure Active Directory (AAD) or Active Directory Federation Services (ADFS).</span></span>

<span data-ttu-id="7fc26-107">セットアップ中にこのアカウントにサインインをユーザーが使用できるデバイスでユーザー プロファイルが作成、サインインするすべてのアプリのデータの格納とします。</span><span class="sxs-lookup"><span data-stu-id="7fc26-107">Signing into this account during setup creates a user profile on the device which the user can use to sign-in, and against which all apps will store their data.</span></span> <span data-ttu-id="7fc26-108">この同じアカウントは、Edge、または Windows アカウント マネージャー Api を使用して、Skype などのアプリのシングル サインオンも提供します。</span><span class="sxs-lookup"><span data-stu-id="7fc26-108">This same account also provides Single Sign On for apps such as Edge or Skype via the Windows Account Manager APIs.</span></span>

<span data-ttu-id="7fc26-109">さらに、エンタープライズまたはデバイス上の組織のアカウントをサインインするときに可能性がありますもモバイル デバイス管理 (MDM) ポリシーを適用する、IT 管理者によって構成されている場合</span><span class="sxs-lookup"><span data-stu-id="7fc26-109">Additionally, when signing into an enterprise or organizational account on the device, it may also apply Mobile Device Management (MDM) policy, if configured by your IT Admin.</span></span>

<span data-ttu-id="7fc26-110">デバイスが再起動またはスタンバイから再開、されるたびに、このアカウントの資格情報は、もう一度サインインに使用されます。</span><span class="sxs-lookup"><span data-stu-id="7fc26-110">Whenever the device restarts or resumes from standby, the credentials for this account are used to sign-in again.</span></span> <span data-ttu-id="7fc26-111">設定で、明示的なサインインを適用するオプションが有効な場合、ユーザーが自分の資格情報をもう一度入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7fc26-111">If the option enforcing an explicit sign-in is enabled in Settings, the user will be required to type in their credentials again.</span></span> <span data-ttu-id="7fc26-112">デバイスが再起動を受信し、OS の更新プログラムを適用した後、いつでも、明示的なサインインが必要です。</span><span class="sxs-lookup"><span data-stu-id="7fc26-112">Anytime the device restarts after receiving and applying an OS update, an explicit sign-in is required.</span></span>

## <a name="multi-user-support"></a><span data-ttu-id="7fc26-113">マルチ ユーザー サポート</span><span class="sxs-lookup"><span data-stu-id="7fc26-113">Multi-user support</span></span>

>[!NOTE]
><span data-ttu-id="7fc26-114">これはマルチ ユーザー サポートは、商用のスイートが必要です、 [Windows Holographic for Business](https://docs.microsoft.com/hololens/hololens-upgrade-enterprise)機能します。</span><span class="sxs-lookup"><span data-stu-id="7fc26-114">Multi-user support requires the Commercial Suite, as this is a [Windows Holographic for Business](https://docs.microsoft.com/hololens/hololens-upgrade-enterprise) feature.</span></span>

<span data-ttu-id="7fc26-115">以降では、 [Windows 10 April 2018 Update](release-notes-april-2018.md)HoloLens、同じ AAD テナント内から複数のユーザーをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7fc26-115">Starting with the [Windows 10 April 2018 Update](release-notes-april-2018.md), HoloLens supports multiple users from within the same AAD tenant.</span></span> <span data-ttu-id="7fc26-116">これを使用するには、お客様の組織に属しているアカウントを使用して最初にデバイスを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7fc26-116">To use this you must set up the device initially with an account that belongs to your organization.</span></span> <span data-ttu-id="7fc26-117">その後、同じテナントから他のユーザーは、既存のユーザーをサインアウトするサインイン画面から、または [スタート] パネルのユーザー タイルをタップして、デバイスにサインインすることになります。</span><span class="sxs-lookup"><span data-stu-id="7fc26-117">Subsequently, other users from the same tenant will be able to sign into the device from the sign-in screen or by tapping the user tile on the Start panel to sign out the existing user.</span></span> 

<span data-ttu-id="7fc26-118">その他のすべてのユーザーに利用できるデバイスにインストールされているアプリしますが、それぞれ独自のアプリのデータと設定。</span><span class="sxs-lookup"><span data-stu-id="7fc26-118">Apps installed on the device will be available to all other users, but each will have their own app data and preferences.</span></span> <span data-ttu-id="7fc26-119">アプリを削除するも削除されますが他のすべてのユーザーが。</span><span class="sxs-lookup"><span data-stu-id="7fc26-119">Removing an app will also remove it for all other users though.</span></span> 

<span data-ttu-id="7fc26-120">デバイスのユーザーを削除するには設定に移動して領域を再利用するデバイスから > アカウント > 他のユーザー。</span><span class="sxs-lookup"><span data-stu-id="7fc26-120">You can remove device users from the device to reclaim space by going to Settings > Accounts > Other people.</span></span> <span data-ttu-id="7fc26-121">また、デバイスからすべての他のユーザーのアプリ データこれも削除されます。</span><span class="sxs-lookup"><span data-stu-id="7fc26-121">This will also remove all of the other users' app data from the device.</span></span> 

## <a name="linked-accounts"></a><span data-ttu-id="7fc26-122">リンクされたアカウント</span><span class="sxs-lookup"><span data-stu-id="7fc26-122">Linked accounts</span></span>

<span data-ttu-id="7fc26-123">(ストア) などのアプリ内で簡単にアクセスするために、追加の web アカウントの資格情報をリンクする、1 つのデバイス アカウント内または個人と職場のリソース、Windows のデスクトップ バージョンのようなへのアクセスを結合します。</span><span class="sxs-lookup"><span data-stu-id="7fc26-123">Within a single device account, users can link additional web account credentials for the purpose of the easier access within apps (such as the Store) or to combine access to personal and work resources, similar to the Desktop version of Windows.</span></span> <span data-ttu-id="7fc26-124">この方法で追加のアカウントにサインインは、イメージなど、デバイスで作成されたユーザー データを分離しないまたはダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7fc26-124">Signing into an additional account in this way does not separate the user data created on the device, such as images or downloads.</span></span> <span data-ttu-id="7fc26-125">アプリを作成できるアカウントをデバイスに接続すると、アプリごとに個別にサインインすることを削減する、アクセス許可を持つことの使用します。</span><span class="sxs-lookup"><span data-stu-id="7fc26-125">Once an account has been connected to a device, apps can make use of it with your permission to reduce having to sign into each app individually.</span></span>

## <a name="using-single-sign-on-within-an-app"></a><span data-ttu-id="7fc26-126">アプリ内でのシングル サインオンを使用してください。</span><span class="sxs-lookup"><span data-stu-id="7fc26-126">Using single sign-on within an app</span></span>

<span data-ttu-id="7fc26-127">アプリ開発者の場合での HoloLens で接続されている id を格納する利点を行う、 [Windows アカウント マネージャー Api](https://msdn.microsoft.com/library/windows/apps/xaml/windows.security.authentication.web.core.aspx)上の他の Windows デバイスの場合と同様、します。</span><span class="sxs-lookup"><span data-stu-id="7fc26-127">As an app developer, you can take advantage of having a connected identity on HoloLens with the [Windows Account Manager APIs](https://msdn.microsoft.com/library/windows/apps/xaml/windows.security.authentication.web.core.aspx), just as you would on other Windows devices.</span></span> <span data-ttu-id="7fc26-128">これらの Api のいくつかのコード サンプルは[ここ](http://go.microsoft.com/fwlink/p/?LinkId=620621)します。</span><span class="sxs-lookup"><span data-stu-id="7fc26-128">Some code samples for these APIs are available [here](http://go.microsoft.com/fwlink/p/?LinkId=620621).</span></span>

<span data-ttu-id="7fc26-129">アカウント情報の要求元のユーザーなどになる可能性があるアカウント割り込みに同意するものをアプリは、認証トークンを要求すると、2 要素認証などを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7fc26-129">Any account interrupts that may occur such as requesting user consent for account information, two-factor authentication etc. must be handled when the app requests an authentication token.</span></span>

<span data-ttu-id="7fc26-130">アプリでは、以前にリンクされていない特定のアカウントの種類を必要とする場合、アプリは、1 つ追加するユーザー入力を求めるシステムを要求できます。</span><span class="sxs-lookup"><span data-stu-id="7fc26-130">If your app requires a specific account type that hasn't been linked previously, your app can ask the system to prompt the user to add one.</span></span> <span data-ttu-id="7fc26-131">これにより、アプリの子のモーダルとして起動されるようにアカウント設定 ウィンドウがトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="7fc26-131">This will trigger the account settings pane to be launched as a modal child of your app.</span></span> <span data-ttu-id="7fc26-132">2D アプリは、Unity アプリのアプリのセンター経由で直接このウィンドウを表示、この子ウィンドウが表示できるように、これについて簡単に holographic アプリからユーザーにかかるは。</span><span class="sxs-lookup"><span data-stu-id="7fc26-132">For 2D apps, this window will render directly over the center of your app and for Unity apps, this will briefly take the user out of your holographic app so that this child window can be rendered.</span></span> <span data-ttu-id="7fc26-133">コマンドおよびウィンドウでこの操作のカスタマイズが説明されている[ここ](https://msdn.microsoft.com/library/windows/apps/windows.ui.applicationsettings.webaccountcommand.aspx)します。</span><span class="sxs-lookup"><span data-stu-id="7fc26-133">Customizing the commands and actions on this pane is described [here](https://msdn.microsoft.com/library/windows/apps/windows.ui.applicationsettings.webaccountcommand.aspx).</span></span>

## <a name="enterprise-and-other-authentication"></a><span data-ttu-id="7fc26-134">Enterprise およびその他の認証</span><span class="sxs-lookup"><span data-stu-id="7fc26-134">Enterprise and other authentication</span></span>

<span data-ttu-id="7fc26-135">アプリが行う場合の他の種類の認証を使用して、NTLM、Basic、または Kerberos などを使用できます[Windows 資格情報の UI](https://msdn.microsoft.com/library/windows/apps/windows.security.credentials.ui.aspx)を収集、処理、およびユーザーの資格情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="7fc26-135">If your app makes use of other types of authentication, such as NTLM, Basic, or Kerberos, you can use [Windows Credential UI](https://msdn.microsoft.com/library/windows/apps/windows.security.credentials.ui.aspx) to collect, process, and store the user's credentials.</span></span> <span data-ttu-id="7fc26-136">これらの資格情報を収集するためのユーザー エクスペリエンスは現在アカウント割り込み駆動型の他のクラウドによく似ていますと 2D アプリ上に子アプリとして表示されます、または、UI を表示する Unity アプリを簡単に中断されます。</span><span class="sxs-lookup"><span data-stu-id="7fc26-136">The user experience for collecting these credentials is very similar to other cloud driven account interrupts and will appear as a child app on top of your 2D app or briefly suspend a Unity app to show the UI.</span></span>

## <a name="deprecated-apis"></a><span data-ttu-id="7fc26-137">非推奨の Api</span><span class="sxs-lookup"><span data-stu-id="7fc26-137">Deprecated APIs</span></span>

<span data-ttu-id="7fc26-138">デスクトップから HoloLens での開発の違いの 1 つは[OnlineIDAuthenticator](https://msdn.microsoft.com/library/windows/apps/windows.security.authentication.onlineid.onlineidauthenticator.aspx) API が完全にサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7fc26-138">One difference for developing on HoloLens from Desktop is that [OnlineIDAuthenticator](https://msdn.microsoft.com/library/windows/apps/windows.security.authentication.onlineid.onlineidauthenticator.aspx) API is not fully supported.</span></span> <span data-ttu-id="7fc26-139">などの割り込み優良、プライマリのアカウントがある場合、トークンが返されますが上記で説明した、ユーザーの UI は表示されませんしは、アカウントを正しく認証に失敗します。</span><span class="sxs-lookup"><span data-stu-id="7fc26-139">Although it will return a token if the primary account is in good-standing, interrupts such as those described above will not display any UI for the user, and will fail to correctly authenticate the account.</span></span>
