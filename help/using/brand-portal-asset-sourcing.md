---
title: Brand Portal 中的資產來源
description: 將insight帶入Adobe Experience Manager Assets Brand Portal中發佈的資產來源功能。
content-type: reference
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
sub-product: assets
topics: collaboration, content-velocity, sharing
doc-type: feature-video
activity: use
audience: author, marketer
version: Experience Manager 6.5
kt: 3838
exl-id: 2c132a7a-ed10-4856-8378-67939167ea60
source-git-commit: 9b8a415fa3a19e462ea797cfc9c3ea9b9323723e
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 11%

---

# 資產來源概觀 {#overview-asset-sourcing-in-bp}

**Asset Sourcing**&#x200B;可讓Experience Manager Assets使用者（管理員/非管理員使用者）使用額外的&#x200B;**資產貢獻**&#x200B;屬性來建立新資料夾，確保所建立的新資料夾可供Brand Portal使用者提交資產。 這會自動觸發工作流程，在新建立的&#x200B;**貢獻**&#x200B;資料夾中建立兩個額外的子資料夾，稱為&#x200B;**SHARED**&#x200B;和&#x200B;**NEW**。 管理員會上傳應新增至貢獻資料夾的資產型別簡介，以定義需求。 他們上傳一組基準資產至&#x200B;**共用**&#x200B;資料夾，為Brand Portal使用者提供必要的參考資訊。 然後，管理員可以在將新建立的&#x200B;**貢獻**&#x200B;資料夾發佈到Brand Portal之前，授予作用中Brand Portal使用者對貢獻資料夾的存取權。 當使用者完成在&#x200B;**NEW**&#x200B;資料夾中新增內容時，他們可以發佈貢獻資料夾回Experience Manager作者環境。 請注意，可能需要幾分鐘的時間來完成匯入，並在Experience Manager Assets中反映新發佈的內容。

此外，所有現有功能保持不變。 Brand Portal使用者可以從貢獻資料夾以及其他允許的資料夾中檢視、搜尋和下載資產。 而管理員可以進一步共用貢獻資料夾、修改屬性，以及將資產新增至集合中。

![Brand Portal資產來源](assets/asset-sourcing.png)

>[!VIDEO](https://video.tv.adobe.com/v/29365/?quality=12)

## 先決條件 {#prerequisites}

* Experience Manager Assets as a Cloud Service執行個體、Experience Manager Assets 6.5.2或更高版本。
* 確認您的Experience Manager Assets執行個體已使用Brand Portal進行設定。 請參閱[使用Brand Portal設定Experience Manager Assets](../using/configure-aem-assets-with-brand-portal.md)。

<!--
* Ensure that your Brand Portal tenant is configured with one AEM Assets author instance.
-->

>[!NOTE]
>
>Experience Manager Assets as a Cloud Service、Experience Manager Assets 6.5.9及更高版本上的「資產來源」功能預設為啟用。
>
>現有設定可在舊版上繼續運作。

>[!NOTE]
>
>Experience Manager Assets 6.5.4有一個已知問題。Brand Portal使用者升級至Adobe Developer Console時，無法將貢獻資料夾的資產發佈至Experience Manager Assets。
>
>此問題已在 Experience Manager Assets 6.5.5 中修正。您可以將 Experience Manager Assets 執行個體升級到最新 Service Pack，並在 Adobe Developer Console 上[升級您的設定](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal#upgrade-integration-65)。

<!--

>For immediate fix on AEM 6.5.4, it is recommended to [download the hotfix](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq650/hotfix/cq-6.5.0-hotfix-33041) and install on your author instance.
-->

<!--
## Configure Asset Sourcing {#configure-asset-sourcing}

**Asset Sourcing** is configured from within the AEM Assets author instance. The administrators can enable the Asset Sourcing feature flag configuration from the **AEM Web Console Configuration** and upload the active Brand Portal users list in **AEM Assets**.

>[!NOTE]
>
>Asset Sourcing is by default enabled on AEM Assets as a Cloud Service. The AEM administrator can directly upload the active Brand Portal users to allow them access to the Asset Sourcing feature.

>[!NOTE]
>
>Before you begin with the configuration, ensure that your AEM Assets instance is configured with Brand Portal. See, [Configure AEM Assets with Brand Portal](../using/configure-aem-assets-with-brand-portal.md). 

The following video demonstrates, how to configure Asset Sourcing on your AEM Assets author instance:

>[!VIDEO](https://video.tv.adobe.com/v/29771)
-->

<!--
### Enable Asset Sourcing {#enable-asset-sourcing}

AEM administrators can enable the Asset Sourcing feature flag from within the AEM Web Console Configuration (a.k.a Configuration Manager).

>[!NOTE]
>
>This step is not applicable for AEM Assets as a Cloud Service.


**To enable Asset Sourcing:**
1. Log in to your AEM Assets author instance and open Configuration Manager. 
Default URL: http:// localhost:4502/system/console/configMgr.
1. Search using the keyword **Asset Sourcing** to locate **[!UICONTROL Asset Sourcing Feature Flag Config]**.
1. Click **[!UICONTROL Asset Sourcing Feature Flag Config]** to open the configuration window.
1. Select the **[!UICONTROL feature.flag.active.status]** check box.
1. Click **[!UICONTROL Save]**.

![](assets/enable-asset-sourcing.png)
-->


### 上傳Brand Portal使用者清單 {#upload-bp-user-list}

Experience Manager Assets管理員可上傳包含Experience Manager Assets中有效Brand Portal使用者清單的Brand Portal使用者設定(.csv)檔案，以允許他們存取Asset Sourcing功能。

貢獻資料夾只能與使用者清單中定義的作用中Brand Portal使用者共用。 管理員也可以在設定檔案中新增使用者，並上傳修改的使用者清單。

>[!NOTE]
>
>確認您的Experience Manager Assets執行個體已使用Brand Portal進行設定。 請參閱[使用Brand Portal設定Experience Manager Assets](../using/configure-aem-assets-with-brand-portal.md)。

>[!NOTE]
>
>CSV檔案的格式與Admin Console對大量使用者匯入支援的格式相同。 電子郵件、名字和姓氏為必填。

管理員可以在Admin Console中新增使用者。 請移至[管理使用者](brand-portal-adding-users.md)以取得詳細資訊。 在Admin Console中新增使用者後，可將這些使用者新增至Brand Portal使用者設定檔，然後指派許可權以存取貢獻資料夾。

**若要上傳Brand Portal使用者清單：**

1. 登入您的Experience Manager Assets執行個體。
1. 從[!UICONTROL 工具]面板，瀏覽至&#x200B;**[!UICONTROL Assets]** > **[!UICONTROL Brand Portal使用者]**。

1. Brand Portal上傳貢獻者視窗隨即開啟。
從您的本機電腦瀏覽並上傳包含作用中Brand Portal使用者清單的&#x200B;**組態(.csv)檔案**。
1. 按一下&#x200B;**[!UICONTROL 儲存]**。

   ![](assets/upload-user-list2.png)

管理員可在設定貢獻資料夾時，從此使用者清單提供特定使用者的存取權。 只有指派給貢獻資料夾的使用者才能存取貢獻資料夾，並從Brand Portal將資產發佈到Experience Manager Assets。

## 另請參閱 {#reference-articles}

* [設定貢獻資料夾並發佈至Brand Portal](brand-portal-publish-contribution-folder-to-brand-portal.md)

* [將貢獻資料夾發佈至 Experience Manager Assets](brand-portal-publish-contribution-folder-to-aem-assets.md)
