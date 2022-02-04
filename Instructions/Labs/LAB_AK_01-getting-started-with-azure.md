---
lab:
    title: 'ラボ 01: Azure の使用を開始する'
    module: 'モジュール 1: IoT と Azure IoT Services サービスの概要'
---

# Azure の使用を開始する

## ラボ シナリオ

あなたは Contoso という名前のグルメ チーズ会社で働いています。同社の最高技術責任者は、IoT を実装するためのビジネス チャンスを評価し、Contoso は IoT ソリューションを実装することで大きなメリットを実現できると結論付けました。Contoso は、評価に基づいて Microsoft Azure IoT ツールを選択しました。

プロジェクトに割り当てられた個人の 1人として、Azure ツールに精通する必要があります。

## このラボでは

このラボでは、Azure portal に精通し、リソース グループを設定します。ラボには、次の演習が含まれます。

* Azure ortal をカスタマイズする
* Azure ダッシュボードとリソース グループの作成

## ラボの手順

### 演習 1: Azure portal とダッシュボードの詳細

Azure IoT サービスの使用を開始する前に、Azure 自体のしくみを理解しておくと便利です。

Azure は一般的に 'クラウド' と呼ばれていますが、実際には、単一の Web サイトから Azure リソースにアクセスできるように設計された Web ポータルです。すべての Azure は Azure portal を通してアクセスできます

#### タスク 1: Azure portal のホーム ページを確認する

1. Web ブラウザーで Azure portal を開くには、[portal.azure.com](http://portal.azure.com) に移動します。

    Azure にログインすると、Azure portal に移動します。Azure portal には、Azure リソースへのアクセスに使用できるカスタマイズ可能な UI が用意されています。

1. ポータル ウィンドウの左上隅で、Azure portal メニューを開き、ハンバーガー メニュー アイコンをクリックします。

    ポータル メニューの上部に、次の 4 つのメニュー オプションを含むセクションが表示されます。

    * 「**リソースの作成**」 ボタンにより、Azure Marketplace を通じて利用できるサービスを表示するページが開きます。その多くは無料オプションを提供します。サービスは "モノのインターネット" などのテクノロジ別にグループ化され、検索ボックスが提供されていることに注意してください。
    * 「**ホーム**」 ボタンにより、Azure サービス、最近アクセスしたサービス、およびその他のツールへのリンクを表示するカスタマイズされたページが開きます。
    * 「**ダッシュボード**」 ボタンにより、既定の (または最近使用した) ダッシュボードを表示するページが開きます。このラボの後半で、ダッシュボードを作成します。

    * 「**すべてのサービス**」 ボタンにより、上記の 「**リソースの作成**」 ボタンに似たページが開きます。

    ポータル メニューの下部セクションは 、お気に入りリソースまたは最も一般的に使用されるリソースを表示するようにカスタマイズできる**お気に入り**セクションです。このラボの後半では、この既定の一般的なサービスの一覧をカスタマイズして、独自のお気に入りの一覧にする方法を学習します。

1. Azure portal メニューで、**「ホーム」** をクリックします。

    「ホーム」 ページには、最近使用したリソースとサービスのカスタマイズされたビュー、およびその他の役立つリンクが表示されます。

1. 「ホーム」 ページの **「ツール」** で、**「Azure Monitor」** をクリックします。

    Azure Monitor は、Azure リソースの管理に役立つツールです。IoT ソリューションを補完するサービスを実装したときに、このコースの後半で Azure Monitor を使用することになります。

1. 左側の 「ナビゲーション」 メニューで、データ センター地域のマップを表示するには、**「サービスの正常性」** をクリックします。

    **「サブスクリプション」**、**「リージョン」**、および **「サービス」** のドロップダウンに注意してください。Azure でリソースを購読する場合は、デプロイ先のリージョンを選択します。Azure は、世界中に配置された一連のリージョンでサポートされています。

    このマップは、サブスクリプションに関連付けられているリージョンの現在の状態を示しています。緑色の円を使用して、サービスがそのリージョンで正常に実行されていることを示します。

    クラウド ベンダー(Azure、AWS、Google Cloud など) によっては、サービスが停止することがあります。Service Health マップ上のリージョンの横に青い 'i' が表示される場合は、そのリージョンで 1 つ以上のサービスに問題が発生していることを表しています。Azure では、異なるリージョンでアプリケーションの複数のコピーを実行することで、これらの問題を軽減します (*Geo 冗長性* と呼ばれるプラクティス)。特定のサービスにより、リージョンで問題が発生した場合、それらの要求は別のリージョンにロール オーバーされ、要求を満たします。これは、Azure クラウドでアプリをホストする大きな利点の 1 つです。Azure が問題を処理するため、問題を処理する必要はありません。

1. Azure portal の左上隅で、ホーム ページに戻る場合は、「**ホーム**」 をクリックします。

    ポータル メニューを使用して、簡単なナビゲーションを実行することもできます。ポータル ナビゲーションの一部のオプションをすぐに試すことができます。

#### タスク 2: Azure サービス オプションの詳細

1. Azure portal メニューを開き、「**すべてのサービス**」 をクリック します。

    「すべてのサービス」 ページには、Azure が提供するすべての PaaS、IaaS、および SaaS サービスへのいくつかの異なる表示オプションとアクセスが提供されます。初めて 「すべてのサービス」 ページを開くと、「概要」 ページが表示されます。このビューは、左側のメニューからアクセスできます。

    > **定義**: **PaaS** という用語は **Platformas a Service (サービスとしてのプラットフォーム)** の頭字語であり、**IaaS** という用語は **Infrastructure as a Service (サービスとしてのインフラストラクチャ)** の頭字語であり、**SaaS** という用語は **Software as a Service (サービスとしてのソフトウェア)** の頭字語です。

1. **「すべてのサービス」** ページの左側のメニューの **「カテゴリ」** で、**「すべて」** をクリックします。

    このビューには、各カテゴリに対応するグループに整理されたすべてのサービスが表示されます。上部の検索ボックスは非常に役立ちます。

1. 左側のメニューの 「**カテゴリ**」 で、「**モノのインターネット**」 をクリックします。

    サービスの一覧は、IoT ソリューションに直接関連するサービスに限定されるようになりました。

    Azure portal のサービス/リソース ページは、_ブレード_と呼ばれることもあります 。数ステップ前に Service Health ページを開いたとき、Service Health ブレードが開きました。

    Azure portal では、ブレードをナビゲーション パターンの一種として使用します。サービスの詳細を掘り下げるにつれて、新しいブレードが右に開きます。これにより、水平方向にナビゲートするときにパンくずナビゲーションの形式が提供され、Azure は、クリック可能なブレードの上部にファイル エクスプローラー スタイルのパスを提供します。例: 「ホーム」 > 「監視」 > 「サービス正常性」。しかし、すべてのページがブレードであるとは限りません。あなたはすぐにそれに慣れるでしょう。

1. **「すべてのサービス」** ページで、マウスポインターを **「IoT Hub」** に合わせます。

    ダイアログ ボックスが表示されます。右上隅に "星" の形が表示されます。星形が塗りつぶされると、サービスがお気に入りとして選択されます。ポータル ウィンドウの左側のナビゲーション メニューのお気に入りサービスの一覧に、お気に入りが表示されます。これにより、最も頻繁に使用するサービスに簡単にアクセスできます。お気に入り一覧は、最も使用するサービスを選択してカスタマイズできます。

1. 「IoT Hub」 ダイアログの右上隅で、お気に入りサービスの一覧に IoT Hub を追加するには、星形のアイコンをクリックします。

    これで星が塗りつぶされます。星が枠線として表示されている場合は、星のアイコンをもう一度クリックします。

    > **ヒント**: 新しい項目をお気に入り一覧に追加すると、Azure portal メニューのお気に入り一覧の最下部に配置されます。ドラッグ アンド ドロップ操作を使用して、お気に入りを希望の順序に並べ替えることができます。

1. 同じプロセスを使用して、お気に入りに次のサービスを追加します。**デバイス プロビジョニング サービス**、**論理アプリ**、**Stream Analytics ジョブ**、および **ストレージ アカウント**です。

    > **注**: 選択したサービスの星をクリックすると、お気に入りサービス一覧からサービスを削除できます。

1. 左側のメニューの 「**カテゴリ**」 で、「**全般**」 をクリックします。

1. 以下のサービスをお気に入りとして選択していることを確認します。

    * **サブスクリプション**
    * **リソース グループ**

    追加したお気に入りは、作業を開始するのに十分ですが、「モノのインターネット」 カテゴリを使用して、必要に応じてポータル メニューに追加のお気に入りを追加できます。

#### タスク 3: ツールバー メニューを確認する

1. ウィンドウの全幅を実行するポータルの上部にあるツールバーに注目してください。

    このツールバーの左端にあるハンバーガー メニュー アイコンに加えて、役に立つツール項目がいくつかあります。

    まず、特定のリソースをすばやく検索するために使用できる_検索リソース_ ツールがあることに注意してください。

    検索ツールの右側には、一般的なツールへのアクセスを提供するいくつかのボタンがあります。ボタンの上にマウス ポインターを合わせる、ボタン名が表示されます。

    * 「_Cloud Shell_」 ボタンにより、Azure リソースの管理に使用できる対話型の認証されたシェルがポータル ウィンドウに表示されます。Azure Cloud Shell は、Bash と PowerShell をサポートします。
    * 「_ディレクトリ + サブスクリプション_」 ボタンにより、Azure サブスクリプションとアカウント ディレクトリ (Azure Active Directory 認証メカニズム) の管理に使用できるウィンドウが開きます。
    * 通知ウィンドウを開く 「_通知_」 ボタン。通知ウィンドウは、長期プロセスを操作する場合に便利です。このコース全体でリソースを作成および構成する際に、通知を監視します。
    * 「*設定*」、「*ヘルプ*」、 および 「*フィードバック*」 用のボタンもあります。「*ヘルプ*」 ボタンには、ヘルプ ドキュメントへのリンクと、便利なキーボード ショートカットの一覧が含まれています。

    右端にはアカウント情報のボタンがあり、アカウントのパスワードや課金情報などにアクセスできます。

1. ツールバーで 「**ヘルプ**」 をクリックし、「**ヘルプとサポート**」 をクリックします

1. 「**ヘルプとサポート**」 ブレードで、「_はじめに_」 、「_ドキュメント_」、「_請求に関する FAQ_」、および 「_サポート プラン_」 の 4 つのタイルに注意してください。

    「ヘルプとサポート」 ブレードを使用すると、多くの優れたリソースにアクセスできます。後でこれに戻って、さらに詳しく見ることができます。

1. 「**ヘルプとサポート**」 ブレードで、「**請求に関する FAQ**」 をクリックします

    新しいブラウザー タブが開き、Azure の請求ドキュメントが表示されます。

1. **「Azure の請求とコスト管理で予期しない請求を防ぐ」** ページのコンテンツをスキャンしてください。 

    *ユーザー*が、有料の Azure サブスクリプションを使用していて、課金の責任がある場合 (アカウント管理者である場合) は、請求の管理に役立つコスト アラートを設定できます。

### 演習 2: Azure ダッシュボードとリソース グループの作成

Azure portal では、ダッシュボードを使用して、リソースのカスタマイズされたビューを表示します。情報は、便利な方法でリソースを整理するために配置およびサイズを設定することができるタイルを使用して表示されます。さまざまなビューを提供し、さまざまな目的を果たすさまざまなダッシュボードを作成できます。

ダッシュボードに配置した各タイルには、1 つ以上のリソースが表示されます。個々のリソースのデータを公開するタイルに加えて、リソース グループと呼ばれるもののタイルを作成できます。

リソース グループは、プロジェクトまたはアプリケーションに関連するリソースを含む論理グループです。リソース グループには、ソリューションのすべてのリソース、またはグループとして管理するリソースのみを含めることができます。組織に最も合ったものに基づいてリソース グループにリソースを割り当てる方法を決定します。通常は、同じライフサイクルを共有するリソースを同じリソース グループに追加して、グループとして簡単にデプロイ、更新、および削除できるようにします。

この演習では、次のことを行います。

* このコースで使用できるカスタム ダッシュボードを作成する
* リソース グループを作成し、ダッシュボードにリソース グループ タイルを追加する

#### タスク 1: ダッシュボードの作成

1. 必要に応じて、Web ブラウザーを開き、Azure portal に移動します。

    次のリンクを使用して、Azure portal を開けます。 [Azure portal](https://portal.azure.com)

1. Azure portal メニューで、**「ダッシュボード」** をクリックします。

1. 「**マイ ダッシュボード**」 ページで、「**+ 新しいダッシュボード**」 をクリックし、「**空白のダッシュボード**」 をクリックします。

    カスタム ダッシュボードを作成して、プロジェクトの Azure リソースを整理してアクセスできます。この場合、このコースのカスタム ダッシュボードを作成します。

1. 新しいダッシュボードに名前を付けるには、 **マイ ダッシュボード**を **AZ-220** に置き換えます。

    今後の手順では、手動でダッシュボードにタイルを追加します。別のオプションとして、ドラッグ アンド ドロップ操作を使用してタイル ギャラリーから提供されるスペースにタイルを追加する方法があります。

1. ダッシュボード エディターの上部で、「**カスタマイズの完了**」 をクリックします。

    この時点で、空のダッシュボードが表示されます。

#### タスク 2: リソース グループを作成し、ダッシュボードにリソース グループ タイルを追加する

1. Azure portal メニューで、「**リソース グループ**」 をクリックします。

    このブレードには、Azure サブスクリプションを使用して作成したすべてのリソース グループが表示されます。Azure を使い始めたばかりの場合は、リソース グループがまだない可能性があります。

1. 「**リソース グループ**」 ブレードの左上隅の領域で、「**+ 作成**」 をクリックします

    これにより、「リソース グループの作成」 という名前の新しいブレードが開きます。

1. 時間を割いて、「**リソース グループの作成**」 ブレードの内容を確認します。

    リソース グループがサブスクリプションとリージョンに関連付けられていることに注意してください。次の点について検討してください。

    * サブスクリプションをリソース グループに関連付けると、どのように役に立つか。
    * リソース グループにリージョンを関連付けることによって、リソース グループに含める内容にどのような影響が及ぶでしょうか?

1. 「**サブスクリプション**」 ドロップダウンで、このコースに使用する Azure サブスクリプションを選択します。

1. 「**リソース グループ**」 テキストボックスに、「**rg-az220**」と入力します

    リソース グループの名前は、サブスクリプション内で**一意**である必要があります。入力した名前がまだ使用されておらず、リソース グループの命名規則に適合する場合は、緑色のチェック マークが表示されます。

    > **ヒント**: Azure のドキュメントでは、すべての Azureの [命名規則と制限](https://docs.microsoft.com/ja-jp/azure/architecture/best-practices/resource-naming) について説明しています。

1. 「**リージョン**」 ドロップダウンで、近くにあるリージョンを選択します。  

    [すべてのリージョンが、すべてのサービスを提供しているわけではないので](https://azure.microsoft.com/ja-jp/global-infrastructure/services/)、講師にも確認する必要があります。

    リソース グループはリソースに関するメタデータを格納し、リソース グループ内の新しいリソースが作成される既定の場所として機能するため、リソース グループの場所を指定する必要があります。場合によっては、コンプライアンス上の理由から、そのメタデータが格納される場所を指定する必要があります。一般に、ほとんどのリソースが存在する場所を指定することをお勧めします。同じ場所を使用すると、リソースの管理に使用するテンプレートを簡単にできます。

1. 「**リソース グループの作成**」 ブレードの下部にある 「**Review + create**」 をクリックします。

    リソース グループの設定が正常に検証されたことを示すメッセージが表示されます。

1. リソース グループを作成するには、「**作成**」 をクリックします。

1. 「**リソース グループ**」 ブレードのトップ メニューで、新しいリソース グループを表示するには、「**更新**」 をクリックします。

    このコースを通じて、リソースの管理について詳しく学習します。

1. 名前付きリソース グループの一覧で、作成した **rg-az220** リソース グループの左側にあるボックスをクリックします。

    > **注**:  新しいブレードでリソース グループを開く必要はありません、それ (左側のチェック マーク) を選択するだけです。

1. 画面の右側で、リソース グループに対応する省略記号 (..) をクリックし、「**ダッシュボードにピン留めする**」 をクリックします。

1. 「**リソース グループ**」 ブレードを閉じます。

    ダッシュボードには空のリソースのタイルが含まれますが、心配はいりません。すぐに十分に入力されます。