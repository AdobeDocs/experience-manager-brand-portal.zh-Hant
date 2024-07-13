---
title: 設定貢獻資料夾並從Experience Manager Assets發佈至Brand Portal
seo-title: Configure and publish contribution folder from Experience Manager Assets to Brand Portal
description: 深入瞭解如何從Experience Manager Assets設定貢獻資料夾並發佈至Brand Portal。
seo-description: Get an insight into configuring and publishing a contribution folder from Experience Manager Assets to Brand Portal.
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
exl-id: 9acad588-977a-45de-b544-f2cc8874ba12
source-git-commit: 3845d9fa17e75d59493383303ca0978349ca0401
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 0%

---

# 在Experience Manager Assets中設定貢獻資料夾 {#configure-contribution-folder}

針對合作資產來源，Experience Manager Assets使用者（具有許可權的管理員和非管理員使用者）可以建立&#x200B;**資產貢獻**&#x200B;型別的新資料夾，確保所建立的新資料夾可供Brand Portal使用者提交資產。  這會自動觸發工作流程，在新建立的&#x200B;**貢獻**&#x200B;資料夾中建立兩個額外的子資料夾，稱為&#x200B;**SHARED**&#x200B;和&#x200B;**NEW**。

Experience Manager Assets使用者接著定義資產需求，方法是上傳應新增至貢獻資料夾的資產型別簡介，以及一組基準資產，至&#x200B;**共用**&#x200B;資料夾，以確保Brand Portal使用者擁有他們需要的資訊。 然後，管理員可在將新建立的貢獻資料夾發佈至Brand Portal之前，先授予作用中Brand Portal使用者對貢獻資料夾的存取權。

下列影片示範如何在Experience Manager Assets中設定「貢獻」資料夾：

>[!VIDEO](https://video.tv.adobe.com/v/30547)

Experience Manager Assets使用者會在設定貢獻資料夾時執行下列活動：

* [建立貢獻資料夾](#create-contribution-folder)
* [上傳資產需求並指派參與者](#configure-contribution-folder-properties)
* [上傳基準資產](#uplad-new-assets-to-contribution-folder)
* [從Experience Manager Assets到Brand Portal的Publish貢獻資料夾](#publish-contribution-folder-to-brand-portal)

## 建立貢獻資料夾 {#create-contribution-folder}


Experience Manager Assets管理員與非管理員使用者若有建立新檔案夾的許可權，可以在Experience Manager Assets中建立「貢獻」檔案夾。
若要建立貢獻資料夾，請建立「資產貢獻」型別的新資料夾，以確保建立的新資料夾可供Brand Portal使用者提交資產。  這會自動觸發在貢獻資料夾中建立兩個額外子資料夾（稱為SHARED和NEW）的工作流程。


>[!NOTE]
>
>管理員可以在資料夾中建立多個資產貢獻資料夾。
>
>資產貢獻資料夾包含用於資產分佈和貢獻的NEW和SHARED資料夾。 請勿在貢獻資料夾中建立資產、資料夾或貢獻資料夾。


您可以在建立貢獻資料夾時，個別設定貢獻資料夾屬性。 在此範例中，我們分別設定屬性。

**若要建立貢獻資料夾：**

1. 登入您的Experience Manager Assets執行個體。

1. 導覽至&#x200B;**[!UICONTROL Assets]** > **[!UICONTROL 檔案]**。 其中列出Experience Manager Assets存放庫中的所有現有資料夾。

1. 按一下&#x200B;**[!UICONTROL 建立]**&#x200B;以建立新資料夾。 **[!UICONTROL 建立資料夾]**&#x200B;對話方塊開啟。

1. 輸入資料夾的&#x200B;**[!UICONTROL Title]**&#x200B;和&#x200B;**[!UICONTROL Name]**，然後選取&#x200B;**[!UICONTROL 資產貢獻]**核取方塊。
建議使用不含任何空格的小寫字母來命名資料夾。

1. 按一下「**[!UICONTROL 建立]**」。您會看到Experience Manager Assets存放庫中列出的貢獻資料夾。

   >[!NOTE]
   >
   >非管理員使用者可以建立和共用資產貢獻資料夾，但無法修改或刪除它。


   ![](assets/create-contribution-folder.png)

1. 按一下以開啟貢獻資料夾，您會看到兩個子資料夾 — **[!UICONTROL SHARED]**&#x200B;和&#x200B;**[!UICONTROL NEW]**&#x200B;在貢獻資料夾中自動建立。

   ![](assets/contribution-folder.png)


## 設定貢獻資料夾屬性 {#configure-contribution-folder-properties}

Experience Manager Assets管理員會在設定貢獻資料夾的屬性時執行下列活動。

* **新增說明**：提供貢獻資料夾的高層級說明。
* **上傳簡報**：上傳包含資產相關資訊的資產需求檔案。
* **新增貢獻者**：新增Brand Portal使用者，以授予他們貢獻資料夾的存取權。

資產需求是指管理員提供的詳細資訊，可協助貢獻者(Brand Portal使用者)瞭解貢獻資料夾的需求和需求。 管理員會上傳資產需求檔案，其中包含應新增至貢獻資料夾的資產型別簡介以及資產相關資訊，例如用途、影像型別、最大大小等。

**若要設定貢獻資料夾屬性：**

1. 登入您的Experience Manager Assets執行個體。

1. 導覽至&#x200B;**[!UICONTROL Assets >檔案]**，然後找出貢獻資料夾。
1. 選取貢獻資料夾並按一下&#x200B;**[!UICONTROL 屬性]**&#x200B;以開啟[資料夾屬性]視窗。

   ![](assets/properties.png)

   ![](assets/contribution-folder-property1.png)

1. 導覽至&#x200B;**[!UICONTROL 資產貢獻]**&#x200B;索引標籤。
1. 輸入貢獻資料夾的高階&#x200B;**[!UICONTROL 描述]**。
1. 按一下&#x200B;**[!UICONTROL 上傳簡報]**，從本機電腦瀏覽並上傳&#x200B;**資產需求檔案**。

   ![](assets/upload.png)

1. 在&#x200B;**[!UICONTROL 新增使用者]**&#x200B;欄位中，新增您要共用貢獻資料夾的Brand Portal使用者。 這些使用者可以使用Brand Portal介面存取內容並將其上傳至貢獻資料夾。
1. 按一下「**[!UICONTROL 儲存]**」。

   ![](assets/contribution-folder-property3.png)

>[!NOTE]
>
>搜尋結果以Experience Manager Assets中設定的Brand Portal使用者清單為基礎。 確定您擁有更新的Brand Portal使用者清單。

管理員可以從[!DNL Admin Console]下載`user.csv`檔案，並將其作為新增Brand Portal使用者的基礎範本。 移至[!UICONTROL 使用者]，然後按一下[!UICONTROL 將使用者清單匯出為csv]選項，即可下載`users.csv`檔案。 下列範例使用者列出新增使用者所需的屬性詳細資訊。 使用者專案的唯一必要屬性是`Email`，而所有其他屬性都是選用屬性。

[取得檔案](assets/users.csv)

## 將資產上傳至貢獻資料夾 {#uplad-new-assets-to-contribution-folder}

Experience Manager Assets使用者會將一組基準資產上傳至&#x200B;**共用**&#x200B;資料夾，以確保Brand Portal使用者獲得所需的資訊。

**若要上傳基準線資產：**

1. 登入您的Experience Manager Assets執行個體。

1. 導覽至&#x200B;**[!UICONTROL Assets >檔案]**，然後找出貢獻資料夾。

1. 選取貢獻資料夾，然後按一下以開啟它。

1. 按一下&#x200B;**[!UICONTROL 新增]**&#x200B;資料夾。

   ![](assets/upload-new-assets1.png)

1. 按一下[建立&#x200B;****] > [檔案&#x200B;****]，上傳包含多個資產的個別檔案或資料夾(.zip)。

   ![](assets/upload-new-assets2.png)

1. 瀏覽並上傳資產（檔案或資料夾）至&#x200B;**[!UICONTROL NEW]**&#x200B;資料夾。

   ![](assets/upload-asset4.png)

將所有資產或資料夾上傳至「新增」資料夾後，將貢獻資料夾發佈至Experience Manager Assets。


## Publish貢獻資料夾至Brand Portal {#publish-contribution-folder-to-brand-portal}

設定貢獻資料夾後，Experience Manager Assets使用者（管理員/非管理員使用者）可以從Experience Manager Assets將貢獻資料夾發佈到Brand Portal。 具有存取貢獻資料夾許可權的Brand Portal使用者將在發佈動作完成時收到電子郵件/脈衝通知。


**要發佈貢獻資料夾：**

1. 登入您的Experience Manager Assets執行個體。

1. 導覽至&#x200B;**[!UICONTROL Assets >檔案]**，並找出您要發佈至Brand Portal的貢獻資料夾。
1. 選取貢獻資料夾，然後按一下&#x200B;**[!UICONTROL 快速Publish]** > **[!UICONTROL Publish至Brand Portal]**。

   ![](assets/publish-contribution-folder-to-bp.png)

   貢獻資料夾發佈至Brand Portal後，您會收到一則成功訊息。

電子郵件/脈衝通知會傳送給指派至貢獻資料夾的Brand Portal使用者。 Brand Portal使用者可以存取貢獻資料夾並開始貢獻。 請參閱[將資產上傳至貢獻資料夾並發佈至Experience Manager Assets](brand-portal-publish-contribution-folder-to-aem-assets.md)。
