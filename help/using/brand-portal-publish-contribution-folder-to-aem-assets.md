---
title: 上傳資產，並將「貢獻」資料夾從Brand Portal發佈至Experience Manager Assets
description: 深入瞭解如何從Brand Portal上傳新資產以及將貢獻資料夾發佈至Experience Manager Assets。
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
exl-id: 7dcf445d-97ed-4fa5-959c-c4c48e325766
source-git-commit: 10f89ded6febb1a024cbe181fa48a290d90223f0
workflow-type: tm+mt
source-wordcount: '1470'
ht-degree: 0%

---

# Publish貢獻資料夾至Experience Manager Assets {#using-asset-souring-in-bp}

具有適當許可權的Brand Portal使用者可上傳多個資產或包含多個資產的檔案夾至貢獻檔案夾。 不過，Brand Portal使用者只能將資產上傳至&#x200B;**NEW**&#x200B;資料夾。 **共用**&#x200B;資料夾用於分發Brand Portal使用者在建立貢獻的新資產時所使用的基準資產（參考內容）。

擁有貢獻資料夾存取許可權的Brand Portal使用者可以執行下列活動：

* [下載資產需求](#download-asset-requirements)
* [將新資產上傳至貢獻資料夾](#uplad-new-assets-to-contribution-folder)
* [Publish貢獻資料夾至Experience Manager Assets](#publish-contribution-folder-to-aem)

## 下載資產需求 {#download-asset-requirements}

當Brand Portal使用者共用貢獻資料夾時，Experience Manager Assets使用者會自動收到電子郵件和脈衝通知。 此工作流程可讓他們從&#x200B;**共用**&#x200B;資料夾下載簡短（資產需求）檔案和基準資產（參考內容），以瞭解資產需求。

Brand Portal使用者會執行下列活動來下載資產需求：

* **下載簡介** — 下載附加至貢獻資料夾的簡介（資產需求檔案）。 它包含資產相關資訊，例如資產型別、用途、支援的格式、資產大小上限等。
* **下載基準線資產** — 下載基準線資產，其可用於瞭解所需的資產型別。 Brand Portal使用者可參照這些資產，以建立新的資產來貢獻。

Brand Portal儀表板會反映Brand Portal使用者允許的所有現有資料夾，以及新共用的貢獻資料夾。 在此範例中，Brand Portal使用者僅擁有新建立貢獻資料夾的存取權。 沒有其他現有資料夾與該使用者共用。

**若要下載資產需求：**

1. 登入您的Brand Portal執行個體。
1. 從Brand Portal儀表板選取貢獻資料夾。
1. 按一下&#x200B;**[!UICONTROL 屬性]**。 包含貢獻資料夾詳細資訊的「屬性」視窗隨即開啟。

   ![](assets/properties.png)

   ![](assets/download-asset-requirement2.png)

1. 按一下&#x200B;**[!UICONTROL 下載簡報]**&#x200B;選項，將資產需求檔案下載到您的本機電腦上。

   ![](assets/download.png)

1. 返回Brand Portal控制面板。
1. 按一下貢獻資料夾以開啟它。 您可以在貢獻資料夾中看到兩個子資料夾： **[!UICONTROL SHARED]**&#x200B;和&#x200B;**[!UICONTROL NEW]**。 共用資料夾包含管理員共用的所有基準資產（參考內容）。
1. 您可以下載包含本機電腦上所有基準資產的&#x200B;**[!UICONTROL SHARED]**資料夾。
或者，您可以開啟**[!UICONTROL 共用]**&#x200B;資料夾，然後按一下&#x200B;**下載**&#x200B;圖示來下載個別檔案/資料夾。

   ![](assets/download.png)

   ![](assets/download-asset-requirement5.png)

瀏覽簡報（資產需求檔案），並參閱基準資產，以瞭解資產需求。 現在，您可以建立新的貢獻資產，並將其上傳至貢獻資料夾。

## 將資產上傳至貢獻資料夾 {#upload-new-assets-to-contribution-folder}

處理完資產需求後，Brand Portal使用者可以為貢獻建立新資產，並將這些資產上傳至貢獻資料夾中的新資料夾。 使用者可將多個資產上傳至資產貢獻資料夾。 不過，一次只能建立一個資料夾。

>[!NOTE]
>
>Brand Portal使用者可將資產（每個檔案大小最多2 GB）上傳至NEW資料夾。
>
>任何Brand Portal租使用者的最大上傳限製為10 GB，會累計套用至所有貢獻資料夾。
>
>上傳至Brand Portal的資產不會處理轉譯，也不會包含預覽。

>[!NOTE]
>
>Adobe建議您在發佈貢獻資料夾至Experience Manager Assets後發佈上傳空間，以供其他Brand Portal使用者貢獻內容。
>
>如果需要將Brand Portal租使用者的上傳限制延長到&#x200B;**10** GB以上，請聯絡客戶支援服務，指定需求。


**若要上傳新資產：**

1. 登入您的Brand Portal執行個體。
Brand Portal儀表板會反映Brand Portal使用者允許的所有現有資料夾，以及新共用的貢獻資料夾。

1. 選取貢獻資料夾，然後按一下以開啟它。 貢獻資料夾包含兩個子資料夾 — **[!UICONTROL 共用]**&#x200B;和&#x200B;**[!UICONTROL 新增]**。

1. 按一下&#x200B;**[!UICONTROL 新增]**&#x200B;資料夾。

   ![](assets/upload-new-assets4.png)

1. 按一下[建立&#x200B;****] > [檔案&#x200B;****]，上傳包含多個資產的個別檔案或資料夾(.zip)。

   ![](assets/upload-new-assets5.png)

1. 瀏覽並上傳資產（檔案或資料夾）至&#x200B;**[!UICONTROL NEW]**&#x200B;資料夾。

   ![](assets/upload-asset4.png)

將所有資產或資料夾上傳至「新增」資料夾後，將貢獻資料夾發佈至Experience Manager Assets。


## Publish貢獻資料夾至Experience Manager Assets {#publish-contribution-folder-to-aem}

Brand Portal使用者可以將「貢獻」資料夾發佈到Experience Manager Assets，而不需要存取Experience Manager作者例項。

確保您已通過資產要求，並在貢獻資料夾內的&#x200B;**NEW**&#x200B;資料夾中上傳新建立的資產。

**若要發佈貢獻資料夾：**

1. 登入您的Brand Portal執行個體。

1. 從Brand Portal儀表板選取貢獻資料夾。
1. 按一下&#x200B;**[!UICONTROL Publish到AEM]**。

   ![](assets/export.png)

   ![](assets/publish-contribution-folder-to-aem1.png)

在發佈工作流程的不同階段中，會傳送電子郵件/脈衝通知給Brand Portal使用者和管理員：

1. **已排入佇列** — 在Brand Portal中觸發發佈工作流程時，會傳送通知給Brand Portal使用者和Brand Portal管理員。

1. **完成** — 當貢獻資料夾成功發佈至Brand Portal時，會傳送通知給Experience Manager Assets使用者和Brand Portal管理員。

將新建立的資產發佈到Experience Manager Assets後，Brand Portal使用者可以將其從「新增」資料夾中刪除。 不過，Brand Portal管理員可以從「新增」和「共用」資料夾中刪除資產。

一旦達到建立貢獻資料夾的目標，Brand Portal管理員可以刪除貢獻資料夾，以釋出上傳空間給其他使用者。

## 發佈工作狀態 {#publishing-job-status}

管理員可以使用兩個報表，檢視從Brand Portal發佈至Experience Manager Assets的資產貢獻資料夾狀態。

* 在Brand Portal中，導覽至&#x200B;**[!UICONTROL 工具]** > **[!UICONTROL 資產貢獻狀態]**。 此報表會反映發佈工作流程不同階段的所有發佈工作狀態。

  ![](assets/contribution-folder-status-v2.png)

* 在Experience Manager Assets （內部部署或受管理的服務）中，導覽至&#x200B;**[!UICONTROL Assets]** > **[!UICONTROL 工作]**。 此報表可反映所有發佈工作的最終狀態（成功或錯誤）。

  ![](assets/publishing-status.png)

* 在Experience Manager Assetsas a Cloud Service中，導覽至&#x200B;**[!UICONTROL Assets]** > **[!UICONTROL 工作]**。

  或者，您可以從全域導覽直接導覽至&#x200B;**[!UICONTROL 工作]**。

  此報表可反映所有發佈工作的最終狀態（成功或錯誤），包括從Brand Portal將資產匯入Experience Manager Assetsas a Cloud Service。

  ![](assets/cloud-service-job-status.png)

<!--
>[!NOTE]
>
>Currently, no report is generated in AEM Assets as a Cloud Service for the Asset Sourcing workflow. 
-->

## 從「貢獻」資料夾自動刪除發佈至Experience Manager Assets的資產 {#automatically-delete-published-assets-from-contribution-folder}

Brand Portal現在每十二小時執行一次自動作業，以掃描所有「貢獻」資料夾並刪除發佈至AEM的所有資產。 因此，您不需要手動刪除「貢獻」資料夾中的資產，以使資料夾大小低於[臨界值限制](#upload-new-assets-to-contribution-folder)。 您也可以監視過去七天內自動執行的刪除作業的狀態。 工作的報表提供下列詳細資訊：

* 工作開始時間
* 工作結束時間
* 工作狀態
* 工作中包含的資產總數
* 在工作中成功刪除的資產總數
* 因工作執行而可供使用的總儲存空間

  ![刪除報告](assets/deletion-reports.png)

您也可以進一步向下展開，以檢視刪除工作中每個資產的詳細資訊。 資產標題、大小、作者、刪除狀態和刪除時間等詳細資料會納入報告中。

![詳細刪除報告](assets/deletion-reports-detailed.png)

>[!NOTE]
>
> * 客戶可以要求Adobe客戶支援停用及重新啟用自動刪除工作功能，或變更其執行頻率。
> * Experience Manager 6.5.13.0和更新版本皆提供此功能。

### 檢視和下載刪除報告 {#view-delete-jobs}

若要檢視及下載刪除工作的報表：

1. 在Brand Portal中，導覽至&#x200B;**[!UICONTROL 工具]**>**[!UICONTROL 資產貢獻狀態]**>**[!UICONTROL 刪除報告]**&#x200B;選項。

1. 選取工作並按一下[檢視] **[!UICONTROL 檢視報告]**。

   檢視刪除工作中每個資產的詳細資訊。 資產標題、大小、作者、刪除狀態和刪除時間等詳細資料會納入報告中。 按一下「下載&#x200B;****」，以CSV格式下載工作的報告。

   報表中資產的刪除狀態可能具有以下值：

   * **已刪除** — 已成功從「貢獻」資料夾中刪除資產。

   * **找不到** - Brand Portal在「貢獻」資料夾中找不到資產。 資產已手動從資料夾中刪除。

   * **已略過** - Brand Portal已略過資產刪除，因為「貢獻」資料夾中有新版本可供資產使用，但尚未發佈至Experience Manager。

   * **失敗** - Brand Portal無法刪除資產。 刪除狀態為`Failed`之資產的重試次數有三次。 如果資產第三次重試刪除嘗試失敗，您需要手動刪除資產。

### 刪除報告

Brand Portal也可讓您選取一或多個報表，然後手動將其刪除。

若要刪除報告：

1. 瀏覽至&#x200B;**[!UICONTROL 工具]**>**[!UICONTROL 資產貢獻狀態]**>**[!UICONTROL 刪除報告]**&#x200B;選項。

1. 選取一或多個報告並按一下&#x200B;**[!UICONTROL 刪除]**。


