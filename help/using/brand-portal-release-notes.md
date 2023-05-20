---
title: 發行說明
seo-title: Release Notes
description: 深入瞭解Adobe Experience Manager Assets Brand Portal版中的功能、增強功能、已修復的關鍵問題和已知2023.05.0題。
seo-description: Get an insight into the enhancements, critical issues fixed, and known issues in the Adobe Experience Manager Assets Brand Portal 2023.05.0 release.
uuid: 3d6ffb6f-4608-4e83-8486-5c90e06cdb43
content-type: reference
contentOwner: Kirandeep Kour
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: 79ebb9fc-385c-48a8-979e-374f42517988
exl-id: e4e89080-9863-4857-8f3a-fcd516ef3271
source-git-commit: 78168800e22dc1bd18d77b958d1dec4892dc4d2d
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 3%

---

# 發行說明 {#release-notes}

深入瞭解Adobe Experience Manager Assets Brand Portal版中的新功能、增強功能、已修復的關鍵問題和已知2023.05.0題。

## 發行資訊 {#release-information}

| 產品 | Adobe Experience Manager Assets Brand Portal |
|---|---|
| 版本 | 2023.05.0 |
| 日期 | 2023年5月 |

## 概觀 {#overview}

Adobe Experience Manager(AEM)Assets Brand Portal幫助您輕鬆獲得、控制和安全地將經批准的創意資產分散給外部各方和跨設備的內部業務用戶。 它有助於提高資產共用的效率，加快資產上市的時間，並降低不遵守法規和未經授權的訪問的風險。 Brand Portal允許用戶隨時隨地以公司批准的格式瀏覽、搜索、預覽、下載和導出資產。

## 2023.05.0中的新增功能 {#whats-new-in-2023.05.0}

### 關鍵問題已修復 {#critical-issues-fixed}

#### 錯誤修正 {#bug-fixes}

此版本包括對以下關鍵問題的修復：
* 如果從共用連結下載資產時出錯， `Notice` 和 `Close` 錯誤提示的標籤未本地化。
* Brand Portal **請求標題欄位太大** 訪問搜索篩選器時出錯 `Filter` 的子菜單。

### 已知問題 {#known-issues}

此版本包括以下已知問題：

* 資產來源補充報表內容中的部分本地化。
* 用戶配置檔案中很少有欄位不可編輯。

## 以前的版本

### 2023年2月發行 {#feb-2023}

**錯誤修正**

此版本包括對以下關鍵問題的修復：
* 無法在Brand Portal上更新配置檔案圖片。
* 內容樹窗格不可調整大小。 如果檔案名長於內容樹的預設寬度，則不能水準和垂直拖動內容樹。 因此，長檔案名不可讀。
* 搜索表單中兩次使用的同一屬性謂詞的搜索結果不一致。
* 中間登錄頁上的文本不是所有語言的本地化文本。

**增強功能**

此版本包括以下增強功能：
* 現在，新的現代PDF觀看器可用於改進PDF資產的預覽。
* 現在，您可以選擇啟用或禁用管理員的資產來源補充通知。 導航到 [!UICONTROL 常規設定] 然後啟用或禁用 [!UICONTROL `Notify Administrator of asset contribution`]。

   ![通知管理員資產貢獻](assets/notify-admin.png)

* 如果禁用了請求訪問，則未經授權的用戶無法請求訪問Brand Portal。
* 僅為Brand Portal設定的組織在配置檔案選取器清單中可見。

**已知問題**

此版本包括以下已知問題：

* 資產來源補充報表內容中的部分本地化。
* 用戶配置檔案中很少有欄位不可編輯。

### 2022年10月發行 {#oct-2022}

**關鍵問題已修復**

此版本包括對以下關鍵問題的修復：
* 將大檔案從Brand Portal複製到第三方工具時響應速度較慢。
* 選中格式副本計數複選框時，將禁用用於選擇單個格式副本的複選框。
* 搜索響應時間較慢。

>[!IMPORTANT]
>
>AEM Assets Brand Portal的脈搏通知將從2022年12月1日起停止。 您將繼續接收以下事件的電子郵件通知，而不是Pulse通知：
>* 通過連結共用資產
>* 請求訪問工作流
>* 共用稿件夾
>* 正在啟動導出AEM至
>* 已完成導出AEM到
>


### 2022年8月發行 {#aug-2022}

**關鍵問題已修復**

此版本包括對以下關鍵問題的修復：
* 當NUI無法處理Experience Manager中的資產時，Brand Portal顯示不準確的資產導入狀態。
* 當預覽操作失敗時，沒有通知來通知失敗。
* 每個資產的totalUploadedSize屬性的值不準確。
* 按一下 **下載所有項目** 而且有大量格式副本可用於某項資產，Brand Portal會下載一個無效的.ZIP檔案。
* 某些字串的翻譯在Brand Portal用戶介面上被截斷。

### 2022年5月發行 {#may-2022}

**新功能**

Brand Portal現在每12小時執行一次自動作業，以刪除發佈到的所有Brand Portal資AEM產。 因此，您不需要手動刪除「貢獻」資料夾中的資產，以使資料夾大小低於閾值限制。

**關鍵問題已修復**

此版本包括對以下關鍵問題的修復：

* 下載包含帶有顏色標籤的資產的資料夾或集合時，也會下載XML檔案。
* 下載包含格式副本的視頻時，Brand Portal會建立一個無效的.ZIP檔案。
* 當您在作者上建立預設和資AEM產並將其發佈到Brand Portal，然後在下載資產時選擇動態格式副本時，無法提取下載的.ZIP檔案。
* 從Brand Portal上可用的某些資料夾下載視頻資產時出現問題。
* 使用電子郵件共用「貢獻」資料夾的URL時，查看器和編輯器角色在使用breadcrumb訪問其父資料夾時遇到問題。
* 來源補充發佈報告顯示的作業開始時間不正確。

### 2022年2月發行 {#feb-2022}

**新功能**

* 來賓用戶的會話超時閾值已從2小時減少到15分鐘。
* 其他 **[!UICONTROL 查看頁面]** 已刪除多頁PDF的選項，因為用戶現在可以從Adobe Document Cloud查看器查看PDF頁。
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

* The users are unable to search, navigate, or open folders. The user interface reflects the error message: `Failed to load data`. 
* The **[!UICONTROL Renditions]** panel does not list all the static renditions of the assets that are published to Brand Portal.
* The **[!UICONTROL Renditions]** panel lists the smart crop renditions of the asset, however, the user cannot preview or download the smart crop renditions.
* The download dialog lists the smart crop renditions of the selected asset, however, the user cannot download the smart crop renditions. 
* A non-admin user is getting only the original asset rendition when downloading an asset. The system and custom renditions are not downloaded.  
* When applying search filter to download an asset, the `Download` button is disabled in the download dialog and does not allows the user to download the asset.
* If `Smart Tags` and (or) `Color Tags` are enabled, the download dialog lists the `json` files as renditions and downloads these `json` files in the archived zip folder.
* The anonymous users are unable to download assets using a shared link because the link redirects to the Brand Portal login page. 
* The system is not reflecting the correct value for the number of active concurrent users.
-->

<!--
### New features {#new-features}

Brand Portal now executes automatic jobs every twelve hours to delete all Brand Portal assets that are published to AEM. As a result, you do not need to delete the assets in the Contribution folder manually to keep the folder size below the threshold limit. See [What's new in Experience Manager Assets Brand Portal](whats-new.md).
-->

<!--
This release includes fixes to the following critical issues:

* When you download a folder or a collection that includes assets with color tags, an XML file gets downloaded as well.

* When you download a video that includes renditions, Brand Portal creates an invalid .ZIP file.

* When you create presets and assets on AEM author and publish them to Brand Portal and then select dynamic renditions while downloading the assets, you cannot extract the downloaded .ZIP file.

* Issues while downloading video assets from certain folders available on Brand Portal.

* When you share the Contribution folder’s URL using an email, Viewer and Editor roles face issues while accessing its parent folder using the breadcrumb.

* Sourcing published report displays an incorrect job start time.
>
 
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

* Advances in the asset download process which improves the Brand Portal user experience while [downloading assets from Brand Portal](brand-portal-download-assets.md). Brand Portal administrators can configure **[!UICONTROL Fast Download]**, **[!UICONTROL Custom Renditions]**, and **[!UICONTROL System Renditions]** from the **[!UICONTROL Download]** settings. 

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
