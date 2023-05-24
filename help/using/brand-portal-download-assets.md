---
title: 下載資產
seo-title: Download assets
description: 所有使用者都可以同時下載他們可存取的資產和資料夾。 如此一來，核准的品牌資產就能安全地散發，以供離線使用。
seo-description: All users can simultaneously download assets and folders accessible to them. This way, approved brand assets can be securely distributed for offline use.
uuid: 4b57118e-a76e-4d8a-992a-cb3c3097bc03
content-type: reference
contentOwner: Vishabh Gupta
products: SG_EXPERIENCEMANAGER/Brand_Portal
topic-tags: download, download-install, download assets
discoiquuid: f90c2214-beea-4695-9102-8b952bc9fd17
exl-id: be264b1c-38d9-4075-b56a-113f34a2c6bf
source-git-commit: fe6677df928a4125185051d80ae3055afb479369
workflow-type: tm+mt
source-wordcount: '1921'
ht-degree: 3%

---

# 下載資產 {#download-assets-from-bp}

Adobe Experience Manager Assets Brand Portal可讓使用者同時下載可從Brand Portal存取的資產和資料夾，藉此增強下載體驗。 如此一來，核准的品牌資產就能安全地散發，以供離線使用。 請閱讀下文，瞭解如何從Brand Portal下載資產（已核准資產），以及期望 [下載效能](#expected-download-performance).


>[!NOTE]
>
>在Brand Portal 2020.10.0 （及更高版本）中， **[!UICONTROL 快速下載]** 預設會啟用此設定，使用IBM Aspera Connect加速下載資產。 安裝IBM Aspera Connect 3.9.9 (`https://www.ibm.com/docs/en/aspera-connect/3.9.9`)，然後再從Brand Portal下載資產。 如需詳細資訊，請參閱 [加速從Brand Portal下載的指南](../using/accelerated-download.md).
>
>如果您不想使用IBM Aspera Connect並繼續正常下載程式，請聯絡Brand Portal管理員以關閉 **[!UICONTROL 快速下載]** 設定。

## 設定資產下載 {#configure-download}

Brand Portal管理員可以為Brand Portal使用者設定資產下載和使用者群組設定，好讓他們從Brand Portal介面存取和下載資產轉譯。

>[!NOTE]
>
>套用至使用者介面的下載設定有助於Brand Portal使用者獲得自助式體驗，以便輕鬆設定和下載資產轉譯。 它不會限制在應用程式層的資產下載，例如，使用者仍然可以存取和下載具有完整URL路徑的資產轉譯。

下列設定會定義從Brand Portal介面存取和下載資產轉譯：

* 啟用下載設定
* 設定使用者群組設定

### 啟用下載設定 {#enable-download-settings}

管理員可以啟用資產 **[!UICONTROL 下載設定]** 以定義Brand Portal使用者可存取以供下載的轉譯集。

可用的設定包括：

* **[!UICONTROL 快速下載]**

   它提供使用IBM Aspera Connect加速資產下載的功能。 根據預設， **[!UICONTROL 快速下載]** 中的設定已啟用 **[!UICONTROL 下載設定]**.

* **[!UICONTROL 自訂轉譯]**

   允許下載資產的自訂和（或）動態轉譯。

   除了原始資產和系統產生的轉譯之外，所有資產轉譯都稱為自訂轉譯。 其中包含可用於資產的靜態和動態轉譯。 任何使用者都可以在Experience Manager Assets中建立自訂靜態轉譯，但只有管理員才能建立自訂動態轉譯。 如需詳細資訊，請參閱 [如何套用影像預設集或動態轉譯](../using/brand-portal-image-presets.md).

* **[!UICONTROL 系統轉譯]**

   允許下載系統產生的資產轉譯。

   這些是根據「DAM更新資產」工作流程，在Experience Manager Assets中自動產生的縮圖。

* **[!UICONTROL 資產下載]**

   可讓您將轉譯下載到每個資產的個別檔案夾中。 此設定適用於資料夾、集合和大量下載資產（超過20個資產）。


以管理員身分登入您的Brand Portal租使用者，並導覽至 **[!UICONTROL 工具]** > **[!UICONTROL 下載]**.

管理員可以啟用Brand Portal使用者的任何設定組合，以存取和下載資產轉譯。

![](assets/download-settings-new.png)


>[!NOTE]
>
>只有管理員可以下載過期的資產。 如需過期資產的詳細資訊，請參閱 [管理資產的數位版權](../using/manage-digital-rights-of-assets.md).

### 設定使用者群組設定 {#configure-user-group-settings}

除了 **[!UICONTROL 下載設定]**，Brand Portal管理員可以進一步設定不同使用者群組的設定，以檢視和（或）下載原始資產及其轉譯。

以管理員身分登入您的Brand Portal租使用者，並導覽至 **[!UICONTROL 工具]** > **[!UICONTROL 使用者]**. 在 **[!UICONTROL 使用者角色]** 頁面，導覽至 **[!UICONTROL 群組]** 索引標籤來設定使用者群組的檢視和（或）下載設定。

![view-download-permission](assets/download-permissions.png)

>[!NOTE]
>
>如果將使用者新增到多個群組，並且其中一個群組具有限制，則該限制將套用至使用者。

根據設定，獨立資產、多個資產、包含資產的資料夾、已授權或未授權的資產，以及使用共用連結下載資產時，下載工作流程保持不變。

以下矩陣定義使用者是否有權存取轉譯，取決於 [下載設定](#configure-download)：

| **下載設定：自訂轉譯** | **下載設定：系統轉譯** | **使用者群組設定：下載原始檔案** | **使用者群組設定：下載轉譯** | **結果** |
|---|---|---|---|---|
| 開啟 | 開啟 | 開啟 | 開啟 | 檢視和下載所有轉譯 |
| 開啟 | 開啟 | 關閉 | 關閉 | 檢視原始資產 |
| 關閉 | 關閉 | 開啟 | 開啟 | 檢視和下載原始資產 |
| 開啟 | 關閉 | 開啟 | 開啟 | 檢視和下載原始資產和自訂轉譯 |
| 關閉 | 開啟 | 開啟 | 開啟 | 檢視和下載原始資產與系統轉譯 |
| 開啟 | 關閉 | 關閉 | 關閉 | 檢視原始資產 |
| 關閉 | 開啟 | 關閉 | 關閉 | 檢視原始資產 |
| 關閉 | 關閉 | 關閉 | 開啟 | 檢視原始資產 |
| 關閉 | 關閉 | 開啟 | 關閉 | 檢視和下載原始資產 |
| 關閉 | 關閉 | 關閉 | 關閉 | 檢視原始資產 |



## 下載資產 {#download-assets}

Brand Portal使用者可以從Brand Portal介面下載多個資產、包含資產的資料夾和集合。

>[!NOTE]
>
>如果您沒有存取或下載資產轉譯的許可權，請聯絡Brand Portal管理員。

如果使用者有權存取轉譯，則會為使用者提供增強功能 **[!UICONTROL 下載]** 對話方塊中的下列功能：

* 檢視下載清單中任何資產的所有可用轉譯。
* 排除不需要下載的資產轉譯。
* 按一下即可將相同的轉譯集套用至所有類似的資產型別。
* 針對不同的資產型別套用不同的轉譯集。
* 為每個資產建立個別的資料夾。
* 下載選取的資產及其轉譯。

![download-dialog](assets/download-dialog-box.png)

>[!NOTE]
>
>此 **[!UICONTROL 下載]** 對話方塊僅出現於 **[!UICONTROL 自訂轉譯]** 和（或） **[!UICONTROL 系統轉譯]** 在中啟用 **[!UICONTROL 下載設定]**.


### 下載資產的步驟 {#bulk-download}

以下是從Brand Portal介面下載資產或包含資產的資料夾的步驟：

1. 登入您的Brand Portal租使用者。 根據預設， **[!UICONTROL 檔案]** 檢視會開啟，其中包含所有已發佈的資產和資料夾。

   執行下列任一項作業：

   * 選取您要下載的資產或資料夾。 在頂端的工具列中，按一下 **[!UICONTROL 下載]** 圖示。

      ![select-multi-assets](assets/select-assets-new.png)

   * 若要下載資產的特定資產轉譯，請將指標暫留在資產上，然後按一下 **[!UICONTROL 下載]** 圖示供快速動作縮圖使用。

      ![select-asset](assets/select-asset.png)


      >[!NOTE]
      >
      >如果您是第一次下載資產，而且瀏覽器中未安裝IBM Aspera Connect，系統會提示您安裝Aspera下載加速器(`https://www.ibm.com/docs/en/aspera-connect/3.9.9`)。


      >[!NOTE]
      >
      >如果您要下載的資產也包含授權資產，系統會將您重新導向至 **[!UICONTROL 版權管理]** 頁面。 在此頁面中，選取資產，按一下 **[!UICONTROL 同意]**，然後按一下 **[!UICONTROL 下載]**. 如果您選擇不同意，授權資產將不會下載。
      > 
      >受授權保護的資產具有 [已附加授權合約](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/drm.html) ，這是透過設定資產的 [中繼資料屬性](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/drm.html) 在Experience Manager Assets中。


      ![licensed-asset](assets/licensed-asset-new.png)

1. 此 **[!UICONTROL 下載]** 列出所有選定資產的對話方塊隨即開啟。

   按一下任何資產以檢視可用的轉譯，並選取與您要下載的轉譯相對應的核取方塊。

   您可以手動選取或排除個別資產的轉譯，或按一下 **套用** 圖示可針對類似資產型別（此範例中的所有影像檔案）選取要下載的相同轉譯集。 在 **[!UICONTROL 全部套用]** 對話方塊，按一下 **[!UICONTROL 完成]** 將規則套用至所有類似資產。

   ![apply-all](assets/apply.png)

   您也可以按一下「 」，將資產從下載清單中移除（如有需要） **移除** 圖示。

   ![移除](assets/remove.png)

   若要在下載資產時保留Brand Portal資料夾階層，請選取 **[!UICONTROL 為每個資產建立個別的資料夾]** 核取方塊。

   下載按鈕會反映所選專案的計數。 套用完規則後，請按一下 **[!UICONTROL 下載專案]**.

   ![download-dialog](assets/download-dialog-box-new.png)

1. 根據預設 **[!UICONTROL 快速下載]** 中的設定已啟用 **[!UICONTROL 下載設定]**. 因此，確認方塊會顯示為允許使用IBM Aspera Connect加速下載。

   若要繼續使用 **[!UICONTROL 快速下載]**，按一下 **[!UICONTROL 允許]**. 所有選取的轉譯都會使用IBM Aspera Connect下載到zip資料夾中。

   如果您不想使用IBM Aspera Connect，請按一下 **[!UICONTROL 拒絕]**. 若 **[!UICONTROL 快速下載]** 被拒絕或失敗，系統會填入錯誤訊息。 按一下 **[!UICONTROL 一般下載]** 按鈕以繼續下載資產。

<!-- removed the known issue from step 2 as it is fixed in 2022.02.0 release.
   >[!CAUTION]
   >
   >(**Experience Manager Assets as a Cloud Service** only) The following known issue will be fixed in the upcoming release:
   >
   >The download dialog lists the smart crop renditions of the selected asset, however, the user cannot download the smart crop renditions.
-->

>[!NOTE]
>
>如果 **[!UICONTROL 快速下載]** 管理員會關閉此設定，系統不會使用IBM Aspera Connect，直接將選取的轉譯下載到zip資料夾中。

>[!NOTE]
>
>如果 **[!UICONTROL 資產下載]** 中的設定已啟用 **[!UICONTROL 下載設定]**，資產轉譯會下載到zip檔案夾內每個資產的個別檔案夾中。
>  
>如果資產是從共用連結下載，資產轉譯會針對zip資料夾內的每個資產下載到個別資料夾中。
>
>如果選取要下載的資料夾、集合或超過20個資產， **[!UICONTROL 下載]** 會略過對話方塊，而且使用者可存取的所有資產轉譯（動態轉譯除外）都會下載到zip資料夾中。

>[!NOTE]
>
>Brand Portal支援在混合模式和Scene 7模式下設定Dynamic Media。
>
>(*如果Experience Manager Assets編寫執行個體執行於&#x200B;**Dynamic Media混合模式***)
>
>若要預覽或下載資產的動態轉譯，請確定動態媒體已啟用，且資產的金字塔形轉譯存在於已發佈資產的Experience Manager Assets作者執行個體。 將資產從Experience Manager Assets發佈到Brand Portal時，也會發佈其Pyramid tiff轉譯。



如果您不是 [管理員已授權可存取原始轉譯](../using/brand-portal-adding-users.md#main-pars-procedure-202029708)，則不會下載所選資產的原始轉譯。

![no-access-message](assets/no-access-message.png)

<!-- This issue has been resolved, check with engineering.
>[!NOTE]
>
>Once you have downloaded the asset renditions, the **[!UICONTROL Download]** button is disabled to avoid creating duplicate copies of the renditions. To download more (missing or another copy of renditions), refresh the browser to re-enable the download button.
-->

### 從資產詳細資訊頁面下載資產 {#download-assets-from-asset-details-page}

除了下載工作流程外，還有另一種方法可直接從資產詳細資訊頁面下載個別資產的轉譯。

使用者可以預覽不同的資產轉譯、選取特定轉譯，並直接從以下來源下載資產轉譯： **[!UICONTROL 轉譯]** 面板，而不需開啟 **[!UICONTROL 下載]** 對話方塊。


以下是從資產詳細資訊頁面下載資產轉譯的步驟：

1. 登入您的Brand Portal租使用者，然後按一下資產以開啟資產詳細資訊頁面。
1. 按一下左側的覆蓋圖示，然後按一下 **[!UICONTROL 轉譯]**.

   ![節目導覽](assets/rendition-navigation.png)

1. 此 **[!UICONTROL 轉譯]** 面板會根據資產列出所有可存取的資產轉譯 [下載設定](#configure-download).

   選取您要下載的特定轉譯，然後按一下 **[!UICONTROL 下載專案]**.

   ![轉譯 — 面板](assets/renditions-panel.png)


1. 根據預設 **[!UICONTROL 快速下載]** 中的設定已啟用 **[!UICONTROL 下載設定]**. 因此，確認方塊會顯示為允許使用IBM Aspera Connect加速下載。

   若要繼續使用 **[!UICONTROL 快速下載]**，按一下 **[!UICONTROL 允許]**. 所有選取的轉譯都會使用IBM Aspera Connect下載到zip資料夾中。

   如果您拒絕使用 **[!UICONTROL 快速下載]**，系統會填入錯誤訊息。 按一下 **[!UICONTROL 一般下載]** 按鈕以繼續下載資產。

<!-- removed the known issue from step 3 as it is fixed in 2022.02.0 release.
   >[!CAUTION]
   >
   >(**Experience Manager Assets as a Cloud Service** only) The following known issues will be fixed in the upcoming release:
   >
   >The **[!UICONTROL Renditions]** panel does not list all the static renditions of the assets that are published to Brand Portal after December 16, 2021.
   >
   >The **[!UICONTROL Renditions]** panel lists the smart crop renditions of the asset, however, the user cannot preview or download the smart crop renditions.
-->

>[!NOTE]
>
>如果 **[!UICONTROL 快速下載]** 管理員會關閉此設定，系統不會使用IBM Aspera Connect，直接將選取的轉譯下載到zip資料夾中。


>[!NOTE]
>
>個別下載的資產會顯示在資產下載報表中。 不過，如果下載了包含資產的資料夾，則該資料夾和資產不會顯示在資產下載報表中。

<!--
>[!NOTE]
>
>Assets that are individually downloaded are visible in the assets download report. However, if a folder containing assets is downloaded, the folder and assets are not displayed in the assets download report.
-->

<!-- Backup of content before updating the new feature docs.
## Configure asset download {#configure-download}

The download configuration allows the Brand Portal administrators to define the set of renditions available to the Brand Portal users for downloading the assets. The administrator can configure the asset **[!UICONTROL Download]** settings from the Brand Portal interface. 

The available configurations are:

* **[!UICONTROL Fast Download]** 

  Enables high-speed download of the assets. To know more, see [guide to accelerate downloads from Brand Portal](../using/accelerated-download.md).

* **[!UICONTROL Custom Renditions]** 
  
  Download custom and (or) dynamic renditions of the assets. 
  All the asset renditions other than the original asset and system-generated renditions are called as custom renditions. It includes static as well as dynamic renditions available for the asset. Any user can create a custom static rendition in AEM Assets, whereas, only the AEM administrator can create custom dynamic renditions. To know more, see [how to apply image presets or dynamic renditions](../using/brand-portal-image-presets.md)

* **[!UICONTROL System Renditions]** 

  Download system-generated renditions of the assets. These are the thumbnails which are automatically generated in AEM Assets based on the "DAM update asset" workflow. 

Log in to your Brand Portal tenant as an administrator and navigate to **[!UICONTROL Tools]** > **[!UICONTROL Download]**. By default, the **[!UICONTROL Fast Download]** configuration is enabled in the **[!UICONTROL Download Settings]**. 

The administrators can enable any combination to configure the asset download process.

![](assets/download-configuration.png)


Based on the configuration, the download workflow remains constant for stand-alone assets, multiple assets, folders containing assets, licensed or unlicensed assets, and downloading assets using share link. 


* If both **[!UICONTROL Custom Renditions]** and **[!UICONTROL System Renditions]** configurations are turned-off, the original renditions of the assets are downloaded without any additional dialog being presented to the users.    


* If any of the **[!UICONTROL Custom Renditions]** or **[!UICONTROL System Renditions]** configuration is enabled, an additional **[!UICONTROL Download]** dialog box appears wherein you can choose whether to download the original asset along with its renditions, or download only specific renditions. 

>[!NOTE]
>
>Only the administrators can download the expired assets. For more information about expired assets, see [manage digital rights of assets](../using/manage-digital-rights-of-assets.md).

## Steps to download assets {#steps-to-download-assets}

Following are the steps to download assets or folders containing assets from Brand Portal:

1. From the Brand Portal interface, do one of the following:

   * Select the folders or assets you want to download. From the toolbar at the top, click the **[!UICONTROL Download]** icon.

     ![](assets/downloadassets-1.png)

   * To download a specific asset or folder, hover the pointer over the asset or folder and click the **[!UICONTROL Download]** icon available in the quick action thumbnails.

     ![](assets/downloadsingleasset-1.png)


     >[!NOTE]
     >
     >If you are downloading the assets for the first time and do not have IBM Aspera Connect installed in your browser, it will prompt you to install the Aspera download accelerator. 


     >[!NOTE]
     >
     >If the assets you are downloading also include licensed assets, you are redirected to the **[!UICONTROL Copyright Management]** page. In this page, select the assets, click **[!UICONTROL Agree]**, and then click **[!UICONTROL Download]**. If you choose to disagree, licensed assets are not downloaded. 
     > 
     >License-protected assets have [license agreement attached]() to them, which is done by setting asset's [metadata property]() in Experience Manager Assets.


     ![](assets/licensed-asset-download-1.png)

     
     >[!NOTE]
     >
     >Ensure to select all the required asset renditions while downloading them from the asset details page, and click **[!UICONTROL Download]**. The selected renditions are downloaded to your local machine.
     > 
     >Once you download, the **[!UICONTROL Download]** button is disabled to avoid creating duplicate copies of the downloaded renditions. To download more (missing or another copy of renditions), refresh the browser to re-enable the download button.

     If any of the **[!UICONTROL Custom Renditions]** or **[!UICONTROL System Renditions]** configuration is enabled in the **[!UICONTROL Download Settings]**, the **[!UICONTROL Download]** dialog appears with the **[!UICONTROL Asset(s)]** check box selected by default. If the **[!UICONTROL Fast Download]** configuration is enabled, the **[!UICONTROL Enable download acceleration]** check box is selected by default.

     ![](assets/download-dialog.png)

     >[!NOTE]
     >
     >If the downloading assets are image files, and you select only the **[!UICONTROL Asset(s)]** check box in the **[!UICONTROL Download]** dialog but are not [authorized by the administrator to have access to the original renditions of image files](../using/brand-portal-adding-users.md#main-pars-procedure-202029708) then no image files are downloaded and a notification appears, stating that you have been restricted by the administrator to access original renditions.

     ![](assets/restrictaccess-note.png)

1. To download the renditions in addition to the original assets, select the **[!UICONTROL Rendition(s)]** check box. However, if you want to download the system-generated renditions along with the custom renditions, clear the **[!UICONTROL Exclude System Renditions]** check box.

   ![](assets/download-system-rendition.png)

   * To download only the renditions, clear the **[!UICONTROL Asset(s)]** check box.

     >[!NOTE]
     >
     >By default, only the assets are downloaded. However, original renditions of image files are not downloaded if you are not [authorized by the administrator to have access to the original renditions of image files](../using/brand-portal-adding-users.md#main-pars-procedure-202029708).

    * To share the selected assets with other users through a link, select the **[!UICONTROL Email]** check box. An email notification is sent to the users with the download link. To know how to download assets from shared links, see [downloading assets from shared links](../using/brand-portal-link-share.md#main-pars-header-1703469193).  

      ![](assets/download-link.png)

      >[!NOTE]
      >
      >The download link on email notification expires after 45 days.
      >
      >The administrators can customize email messages, that is, logo, description, and footer, using the [Branding](../using/brand-portal-branding.md) feature.


    * You can select a predefined image preset or create a custom dynamic rendition from the **[!UICONTROL Download]** dialog box. 

      To apply a [custom image preset to the asset and its renditions](../using/brand-portal-image-presets.md#applyimagepresetswhendownloadingimages), select the **[!UICONTROL Dynamic Rendition(s)]** check box. Specify the image preset properties (such as size, format, color space, resolution, and image modifier) to apply the custom image preset while downloading the asset and its renditions. To download only the dynamic renditions, clear the **[!UICONTROL Asset(s)]** check box.

      ![](assets/dynamic-rendition.png)

      >[!NOTE]
      >
      >Brand Portal supports configuring Dynamic Media in both - Hybird and Scene 7 mode. 
      >
      >(*If AEM author instance is running on **Dynamic Media Hybrid mode***)
      >
      >To preview or download dynamic renditions of an asset, ensure that the dynamic media is enabled and the asset's Pyramid tiff rendition exists at the AEM Assets author instance from where the assets have been published. When an asset is published to Brand Portal, its Pyramid tiff rendition is also published.
      
  
    * To preserve the Brand Portal folder hierarchy while downloading assets, select the **[!UICONTROL Create separate folder for each asset]** check box. By default, the Brand Portal folder hierarchy is ignored and all the assets are downloaded in one folder in your local system.

1. Click **[!UICONTROL Download]**.

   The assets (and renditions if selected) are downloaded as a zip file to your local folder. However, no zip file is created if a single asset is downloaded without any of the renditions. 

   If you are not [authorized by the administrator to have access to the original renditions](../using/brand-portal-adding-users.md#main-pars-procedure-202029708), the original renditions of the selected assets are not downloaded. 

   >[!NOTE]
   >
   >Assets that are individually downloaded are visible in the assets download report. However, if a folder containing assets is downloaded, the folder and assets are not displayed in the assets download report.
-->

## 預期的下載效能 {#expected-download-performance}

根據本機網際網路連線和伺服器延遲等因素，不同使用者端位置的檔案下載體驗可能會有所不同。 在不同使用者端位置觀察到2 GB檔案的預期下載效能如下，其中位於美國奧勒岡州的Brand Portal伺服器為：

| 使用者端位置 | 使用者端與伺服器之間的延遲 | 預期下載速度 | 下載2-GB檔案所花的時間 |
|-------------------------|-----------------------------------|-------------------------|------------------------------------|
| 美國西部（北加州） | 18毫秒 | 7.68 MB/秒 | 4 分鐘 |
| 美國西部（奧勒岡州） | 42毫秒 | 3.84 MB/秒 | 9 分鐘 |
| 美國東部（維吉尼亞北部） | 85毫秒 | 1.61 MB/秒 | 21 分鐘 |
| APAC （東京） | 124毫秒 | 1.13 MB/秒 | 30 分鐘 |
| 野田 | 275毫秒 | 0.5 MB/秒 | 68 分鐘 |
| 雪梨 | 175毫秒 | 0.49 MB/秒 | 69 分鐘 |
| 倫敦 | 179毫秒 | 0.32 MB/秒 | 106 分鐘 |
| 新加坡 | 196毫秒 | 0.5 MB/秒 | 68 分鐘 |


>[!NOTE]
>
>在測試條件下會觀察到引述的資料，對於不同位置的使用者而言，這會因延遲和頻寬而異。
