---
title: 發行說明
seo-title: Release Notes
description: 深入瞭解Adobe Experience Manager Assets Brand Portal版中的功能、增強功能、已修復的關鍵問題和已知2022.02.0題。
seo-description: Get an insight into the enhancements, critical issues fixed, and known issues in the Adobe Experience Manager Assets Brand Portal 2022.02.0 release.
uuid: 3d6ffb6f-4608-4e83-8486-5c90e06cdb43
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: 79ebb9fc-385c-48a8-979e-374f42517988
exl-id: e4e89080-9863-4857-8f3a-fcd516ef3271
source-git-commit: 12187c4a98e1541be27b06eefedb1b654c5fb083
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 5%

---

# 發行說明 {#release-notes}

深入瞭解Adobe Experience Manager Assets Brand Portal版中的新功能、增強功能、已修復的關鍵問題和已知2022.02.0題。

## 發行資訊 {#release-information}

| 產品 | Adobe Experience Manager Assets Brand Portal |
|---|---|
| 版本 | 2022.02.0 |
| 日期 | 2022年2月 |

## 概覽 {#overview}

Adobe Experience Manager(AEM)Assets Brand Portal幫助您輕鬆獲得、控制和安全地將經批准的創意資產分散給外部各方和跨設備的內部業務用戶。 它有助於提高資產共用的效率，加快資產的上市時間，並降低不遵守法規和未經授權的訪問的風險。 Brand Portal允許用戶隨時隨地以公司批准的格式瀏覽、搜索、預覽、下載和導出資產。

## 2022.02.0中的新增功能 {#whats-new-in-2022.02.0}

<!--
### New Features {#new-features}

This release includes the following new features:

* AEM Assets as a Cloud Service is now entitled to have a pre-configured Brand Portal instance. The Cloud Manager user can activate Brand Portal on the AEM Assets as a Cloud Service instance.

* Asset Sourcing feature is now available on AEM Assets as a Cloud Service. It allows the Brand Portal users to upload assets to the permitted contribution folders and publish the contribution folder from Brand Portal to AEM Assets as a Cloud Service instance. 

* An additional **[!UICONTROL Asset Download]** setting has been introduced under the **[!UICONTROL Download Settings]**. It creates a separate folder for each asset while downloading the folders, collections, or bulk download of assets. 
-->
<!-- 
* The **[!UICONTROL Download]** dialog is revamped in a list view with additional options to exclude the renditions which are not required, apply the same set of rules for similar asset types, and download the selected asset renditions.
-->

<!--
* The new **[!UICONTROL Download]** dialog now appears with all the renditions of the selected assets or folders containing assets in a list view, wherein the Brand Portal users can apply same set of renditions for similar asset types and download the selected asset renditions. 
-->

<!-- 
* Navigation to the **[!UICONTROL Files]**, **[!UICONTROL Collections]**, and **[!UICONTROL Shared Links]** is now possible from all the Brand Portal pages in one-click.  

* The **[!UICONTROL Renditions]** panel in the asset details page now allows the Brand Portal users to select the original asset and (or) specific asset renditions, and directly download them from the **[!UICONTROL Renditions]** panel without having to open the **[!UICONTROL Download]** dialog.
-->

<!--
Brand Portal users can exclude specific renditions which are not required and directly download the original asset and its renditions from the **[!UICONTROL Renditions]** panel on the asset details page. 
-->

<!-- 
* In addition to the existing **[!UICONTROL Download]** configurations, the Brand Portal administrators can also [configure permissions for different group of users]() to view and (or) download the original asset and its renditions from the asset details page. These configurations will define who can access and (or) download the asset renditions.
-->

<!--
### Enhancements {#enhancements}

Brand Portal 2021.08.0 is an internal release that introduces Business profiles for enterprise and teams customers to give organizations better control over their assets. 

This release includes the following enhancements:

* The users now have organization-specific entitlement on the new and migrated organizations. If a user is entitled to multiple organizations, the user has to select the organization at the time of login.

* The new users that are added in Admin Console must **Join Team** to get entitled to the organization. 

>[!NOTE]
>
>Business profiles are currently applicable for the new organizations that are created after August 16, 2021. 
>
>Until your organization is migrated, you can continue to use Adobe ID, Enterprise ID, or Federated ID types to access the organization.   
-->

<!-- 
* For folder download, a separate folder is created for each asset using share link irrespective of the **[!UICONTROL Download Settings]**. 
* The Brand Portal **[!UICONTROL Usage Report]** has been modified to reflect only the active Brand Portal users.
-->

<!--
* The threshold of session timeout for the guest users has been reduced from 2 hours to 15 minutes.
* The additional **[!UICONTROL View pages]** option has been removed for multi-page PDFs as the user can now view the PDF pages from the Adobe Document Cloud Viewer.
-->


### 關鍵問題已修復 {#critical-issues-fixed}

此版本包括對以下關鍵問題的修復：

* 用戶無法搜索、導航或開啟資料夾。 用戶介面反映錯誤消息： `Failed to load data`。
* 的 **[!UICONTROL 格式副本]** 面板不列出發佈到Brand Portal的資產的所有靜態格式副本。
* 的 **[!UICONTROL 格式副本]** 面板列出了資產的智慧裁剪格式副本，但用戶無法預覽或下載智慧裁剪格式副本。
* 下載對話框列出選定資產的智慧裁剪格式副本，但用戶無法下載智慧裁剪格式副本。
* 非管理員用戶在下載資產時只獲取原始資產格式副本。 系統和自定義格式副本不會下載。
* 應用搜索篩選器下載資產時， `Download` 按鈕在下載對話框中禁用，不允許用戶下載資產。
* 如果 `Smart Tags` 和（或） `Color Tags` 啟用，下載對話框列出 `json` 檔案作為格式副本並下載 `json` 檔案。
* 匿名用戶無法使用共用連結下載資產，因為該連結重定向到Brand Portal登錄頁。
* 系統未反映活動併發用戶數的正確值。


<!--
* Asset Sourcing email notifications are not delivered for some organizations. 

* Video files with extension `.mov` are not running on Brand Portal. 

* In the **[!UICONTROL Smart Collections]** dropdown list, only ten saved collections are visible. 
-->
<!--
* *_deleted tenants are listed as valid tenant which fails during the execution of TenantCustomizers/TenantUpdates where tenant id is returned as /etc/tenants/`<nodename>`.
-->

<!--
In case only the original assets are downloaded, the asset reflects its own extension and does not open until the extension is manually changed to zip. 
* The user interface of the collection folder does not respond on clicking the navigation arrow. 
* **[!UICONTROL Create]** button is visible in the **[!UICONTROL Column]** view even when the folders are empty.
* **[!UICONTROL Omni search]** fails with a 414 error message (Request-URI Too Long) if the dispatcher is bypassed while accessing the Brand Portal instance.
* An empty zip folder is downloaded if the asset contains a comma (`,`) in the file name.
* The viewer users get the option to add users to the collection they have created. 
* Inconsistent behavior is experienced when an asset (thumbnail or web rendition) is downloaded using share link.

See [what's new in Brand Portal 2021.02.0](whats-new.md).
-->


### 已知問題 {#known-issues}

此版本包括以下已知問題：

* 用戶在遷移其現有組織期間無法登錄Brand Portal。

   但是，登錄到Brand Portal的活動用戶可以繼續工作，直到其當前會話過期。

* 從Brand Portal導航到Admin Console時，管理員可能會看到一個額外的螢幕來選擇組織。

* 如果 `Color Tags` 啟用並用戶下載資料夾或集合， `xml` 檔案將針對存檔的zip資料夾中的資料夾（或集合）的每個資產下載。


<!--
### Known Issues {#known-issues}

This release includes the following known issue:

* Search on the **[!UICONTROL Asset Reports]** shows processing on the product interface with no search result.
* The video DM encodes are not visible to the non-admin users on the asset details page.
* The alignment of the size of individual asset renditions and total download size is distorted in the Download dialog.
-->


<!--
* Download Settings configuration to configure asset download from Brand Portal. Fast download, custom renditions, and system renditions are the available configurations. 
-->

<!--
* Document Viewer has been introduced to enhance the PDF viewing experience. New options are available for viewing the PDF files in Brand Portal.

* Advances in the asset download process which improves the Brand Portal user experience while [downloading assets from Brand Portal](download-assets.md). Brand Portal administrators can configure **[!UICONTROL Fast Download]**, **[!UICONTROL Custom Renditions]**, and **[!UICONTROL System Renditions]** from the **[!UICONTROL Download]** settings. 

For details, see [what's new in Brand Portal 6.4.7](whats-new.md). 

### Critical Issues Fixed {#critical-issues-fixed-647}

This release includes fixes to the following critical issues:

* The viewer users are not permitted to share link for collections but the option to share is visible to them on the product interface.

* The **[!UICONTROL Download]** button on the options bar does not list all the licensed assets of the selected folder.

* The search takes longer to show the results for certain keywords.

* The **[!UICONTROL Agree]** and **[!UICONTROL Disagree]** check boxes does not appear on bulk selection of licensed and unlicensed assets during download.

* Filter-based search shows processing on the product interface with no search result. 

* The assets do not download from share link if the shared folder contains numerous and large assets.


### Known Issues {#known-issues-647}

This release includes the following known issues:

* If multiple assets are selected, license text does not appear on clicking Terms and Conditions on the license agreement page during download using share link.   

-->

## 語言 {#languages}

Brand Portal用戶介面以下列語言提供：

* 英文
* 德文
* 法文
* 西班牙文
* 義大利文
* 巴西葡萄牙語
* 日文
* 簡體中文
* 韓文

## 認證平台 {#certified-platforms}

要確定哪些平台經認證可隨本版Brand Portal一起運行，請參閱 **支援觸控優化的UI** 列 **創作用戶介面支援的瀏覽器** 部分 [技術要求](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/introduction/technical-requirements.html)。

## 連結 {#links}

* [Adobe Experience ManagerAdobe.com上的產品頁](https://business.adobe.com/in/products/experience-manager/adobe-experience-manager.html)
* [Assets Brand Portal文檔](https://experienceleague.adobe.com/docs/experience-manager-brand-portal/using/home.html)

## 產品訪問和支援（受限站點） {#product-access-and-support-restricted-sites}

這些站點僅可供客戶使用。 如果您是客戶並需要訪問，請與Adobe客戶經理聯繫。

<!--
* [https://daycare.day.com](https://daycare.day.com) 
-->

<!--
* [Customer Support]()
-->
