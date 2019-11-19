---
title: 品牌入口網站中的資產採購
seo-title: 品牌入口網站中的資產採購
description: 深入瞭解Adobe Experience Manager Assets品牌入口網站中發佈的資產來源補充功能。
seo-description: 深入瞭解Adobe Experience Manager Assets品牌入口網站中發佈的資產來源補充功能。
uuid: null
content-type: reference
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
product: experience-manager
sub-product: assets
feature: brand-portal
topics: collaboration, content-velocity, sharing
doc-type: feature-video
activity: use
audience: author, marketer
version: 6.5
kt: 3838
translation-type: tm+mt
source-git-commit: f8d95ab1e1c17ef2cf86d0206a36134996e4fe07

---


# 資產來源補充概述 {#overview-asset-sourcing-in-bp}

**Asset Sourcing****** 允許AEM使用者（管理員／非管理員使用者）建立新資料夾，並附加「資產貢獻」屬性，以確保建立的新資料夾可供Brand Portal使用者提交資產。 這會自動觸發在新建立的「貢獻」檔案夾中建立另外兩個子檔案夾( **SHARED** 和 **NEW**)的 **** 工作流程。 然後，AEM管理員會將應新增至貢獻檔案夾的資產類型以及一組基準資產上傳至 **SHARED** 檔案夾，以確保BP使用者擁有所需的參考資訊，借此定義需求。 然後，管理員可以先授與作用中的品牌入口網站使用者對貢獻資料夾的存取權，再將新建立的 **貢獻資料夾發佈至品牌入口網站** 。 當使用者在「 **NEW** 」檔案夾中新增內容後，就可以將貢獻檔案夾發佈回AEM作者環境。 請注意，完成匯入並反映AEM Assets中新發佈的內容可能需要幾分鐘的時間。

此外，所有現有功能都保持不變。 品牌入口網站使用者可從貢獻資料夾以及其他許可的資料夾檢視、搜尋及下載資產。 此外，管理員還可以進一步共用貢獻資料夾、修改屬性並將資產新增至系列。

>[!VIDEO](https://video.tv.adobe.com/v/29365/?quality=12&captions=chi_hant)

>[!NOTE]
>
>AEM 6.5.2.0和更新版本支援品牌入口網站中的資產採購。
>
>舊版不支援此功能- AEM 6.3和AEM 6.4。
>
>請連絡Adobe支援，將您的AEM實例升級至最新支援的AEM版本。

![品牌入口網站資產來源補充](assets/asset-sourcing.png)

## 必備條件 {#prerequisites}

* AEM 6.5.0.2或更新版本。
* 請確定您的AEM Assets實例已與品牌入口網站整合。 請參閱「 [設定AEM資產與品牌入口網站的整合」](https://helpx.adobe.com/experience-manager/6-5/assets/using/brand-portal-configuring-integration.html)。

## 另請參閱 {#reference-articles}

**針對管理員**

* [在AEM中設定資產來源補充](brand-portal-configure-asset-sourcing.md)
* [上傳品牌入口網站使用者清單](brand-portal-configure-asset-sourcing.md)
* [設定貢獻資料夾](brand-portal-contribution-folder.md)
* [將基準資產上傳至貢獻資料夾](brand-portal-upload-baseline-assets.md)
* [將貢獻資料夾發佈至品牌入口網站](brand-portal-publish-contribution-folder-to-brand-portal.md)

**針對品牌入口網站使用者**

* [下載資產需求](brand-portal-download-asset-requirements.md)
* [將新資產上傳至貢獻檔案夾](brand-portal-upload-assets-to-contribution-folder.md)
* [將貢獻資料夾發佈至AEM Assets](brand-portal-publish-contribution-folder-to-aem-assets.md)