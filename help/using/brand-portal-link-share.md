---
title: 以連結形式共用資產
description: 瞭解Adobe Experience Manager Assets Brand Portal管理員如何與授權的內部使用者和外部實體（包括合作夥伴和廠商）共用多個資產的連結。 編輯者只能檢視和共用他們共用的資產。
contentOwner: bdhar
content-type: reference
topic-tags: sharing
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: f3573219-3c58-47ba-90db-62b003d8b9aa
exl-id: 9d254e95-a4fc-468d-ae1f-9690ddd3b4a1
source-git-commit: 32a67abf466dd3bf635b851b02377ed23591915e
workflow-type: tm+mt
source-wordcount: '1063'
ht-degree: 6%

---

# 以連結形式共用資產 {#share-assets-as-a-link}

Adobe Experience Manager Assets Brand Portal管理員可與已獲授權的內部使用者和外部實體（包括合作夥伴和廠商）共用多個資產的連結。 編輯者只能檢視和共用他們共用的資產。

透過連結共用資產是一種便利的方式，可供外部對象使用，因為接收者不必登入Brand Portal即可存取資產。

<!-- Link sharing access is restricted to editors and administrators. 
-->

如需詳細資訊，請參閱[管理使用者、群組和使用者角色](../using/brand-portal-adding-users.md#manage-user-roles)。


以下是以連結形式共用資產的步驟：

1. 登入您的Brand Portal租使用者。 依預設，**[!UICONTROL 檔案]**&#x200B;檢視會開啟，其中包含所有已發佈的資產和資料夾。

1. 選取要共用的資產或資料夾，或導覽至&#x200B;**[!UICONTROL 集合]**&#x200B;檢視以共用您已建立的集合。

   ![select-multiple-assets](assets/select-assets-new.png)

1. 從頂端的工具列按一下&#x200B;**[!UICONTROL 共用連結]**&#x200B;圖示。

   **[!UICONTROL 連結共用]**&#x200B;對話方塊就會顯示。

   ![](assets/link-sharing.png)

   * 在電子郵件地址方塊中，輸入您要共用連結之使用者的電子郵件ID。 您可以與多位使用者共用連結。 如果使用者是您組織的成員，請從下拉式清單中顯示的建議中選取其電子郵件ID。 如果使用者是外部使用者，請輸入完整的電子郵件識別碼，然後按&#x200B;**[!UICONTROL Enter]**；電子郵件識別碼會新增至使用者清單。

     ![](assets/link-sharing-text.png)

   * 在&#x200B;**[!UICONTROL 主旨]**&#x200B;方塊中，輸入您要共用之資產的主旨。
   * 在&#x200B;**[!UICONTROL 訊息]**&#x200B;方塊中，視需要輸入訊息。
   * 在&#x200B;**[!UICONTROL 到期]**&#x200B;欄位中，使用日期選擇器來指定連結的到期日期和時間。 依預設，到期日設為您共用連結當日起的7天。
   * 啟用&#x200B;**[!UICONTROL 允許下載原始檔案]**&#x200B;核取方塊，允許收件者下載原始轉譯。

   透過連結共用的資產在超過&#x200B;**[!UICONTROL 過期]**&#x200B;欄位中指定的日期和時間後過期。 如需Brand Portal中過期的資產行為與角色型活動變更的詳細資訊，請參閱[管理資產的數位版權](../using/manage-digital-rights-of-assets.md#asset-expiration)。

   >[!NOTE]
   >
   >連結的預設到期時間為7天。 連結必須透過電子郵件傳送給使用&#x200B;**[!UICONTROL 連結共用]**&#x200B;對話方塊的使用者，請勿分別複製和共用連結。

1. 按一下&#x200B;**[!UICONTROL 共用]**。 訊息會確認此連結已與使用者共用。 使用者會收到包含共用連結的電子郵件。

   ![](assets/link-share-email.png)

   >[!NOTE]
   >
   >管理員可以自訂電子郵件訊息，包括使用[品牌](../using/brand-portal-branding.md)功能自訂標誌、說明和頁尾。

## 從共用連結下載資產 {#download-assets-from-shared-links}

按一下電子郵件中的連結以存取共用資產。 「AEM連結共用」頁面隨即開啟。

若要下載共用資產：

1. 按一下資產或資料夾，然後從工具列按一下&#x200B;**[!UICONTROL 下載]**&#x200B;圖示。

   ![](assets/download-share-link.png)

   >[!NOTE]
   >
   >目前，您只能根據檔案格式，為特定資產產生預覽和縮圖。 如需支援的檔案格式詳細資訊，請參閱[資產格式的預覽和縮圖支援](#preview-thumbnail-support)。

1. **[!UICONTROL 下載]**&#x200B;對話方塊就會顯示。

   ![下載對話方塊](assets/download-dialog-box-new.png)

1. 預設會在&#x200B;**[!UICONTROL 下載設定]**&#x200B;中啟用&#x200B;**[!UICONTROL 快速下載]**&#x200B;設定。 因此，會顯示確認方塊，以繼續使用IBM® Aspera Connect下載。

   若要繼續使用&#x200B;**[!UICONTROL 快速下載]**，請按一下&#x200B;**[!UICONTROL 允許]**。

   所有選取的轉譯都會下載到包含每個資產個別資料夾的zip資料夾中。

   >[!NOTE]
   >
   >從共用連結下載資產時，會為每個資產建立個別的資料夾。
   >
   >如果選取了資料夾、集合或超過20個資產，則會略過&#x200B;**[!UICONTROL 下載]**&#x200B;對話方塊。 此外，所有可存取的資產轉譯（動態資產除外）都會下載到zip資料夾中，每個資產會有個別資料夾。

   >[!NOTE]
   >
   >如果管理員未授權使用者共用資產，則共用連結不會下載原始轉譯。 另請參閱管理員授權的[原始轉譯](../using/brand-portal-adding-users.md#manage-group-roles-and-privileges)的存取權。


>[!NOTE]
>
>Brand Portal會限制使用連結共用下載超過5 GB的資料夾或資產。

<!--
1. The **[!UICONTROL Download]** dialog box appears.

   ![](assets/download-linkshare.png)

    * To speed up the download of asset files shared as the link, select **[!UICONTROL Enable download acceleration]** option and [follow the wizard](../using/accelerated-download.md#download-workflow-using-file-accelerator). To know more about the fast download of assets on Brand Portal refer [Guide to accelerate downloads from Brand Portal](../using/accelerated-download.md).
    
1. To download the renditions of assets in addition to the assets from the shared link, select **[!UICONTROL Rendition(s)]** option. When you do so, **[!UICONTROL Exclude System Renditions]** option appears that is selected by default. This prevents the download of out-of-the-box renditions along with approved assets or their custom renditions.

   However, to allow auto-generated renditions to download along with custom renditions, deselect the **[!UICONTROL Exclude System Renditions]** option.

   >[!NOTE]
   >
   >Original renditions are not downloaded using the shared link if the user who shared the assets as a link is not [authorized by the administrator to have access to the original renditions](../using/brand-portal-adding-users.md#manage-group-roles-and-privileges).

   ![](assets/download-linkshare-autoren.png)

1. Click **[!UICONTROL Download]**. The assets (and renditions if selected) are downloaded as a ZIP file to your local folder. However, no zip file is created if a single asset is downloaded without any of the renditions, thereby ensuring speedy download.

-->

## 資產格式的預覽和縮圖支援 {#preview-thumbnail-support}

下表列出Brand Portal支援縮圖和預覽的資產格式：

| 資產格式 | 縮圖支援 | 預覽支援 |
|--------------|-------------------|-----------------|
| PNG | ✓ | ✓ |
| GIF | ✓ | ✓ |
| TIFF | ✓ | ✕ (A) |
| JPEG | ✓ | ✓ |
| BMP | ✓ | ✕ (A) |
| PNM* | 不適用 | 不適用 |
| PGM* | 不適用 | 不適用 |
| PBM* | 不適用 | 不適用 |
| PPM* | 不適用 | 不適用 |
| PSD | ✓ | ✕ (A) |
| EPS | 不適用 | ✕ (A) |
| DNG | ✓ | ✕ (A) |
| PICT | ✓ | ✕ (A) |
| PSB* | ✓ | ✕ (A) |
| JPG | ✓ | ✓ |
| AI | ✓ | ✕ (A) |
| DOC | ✕ (A) | ✕ (A) |
| DOCX | ✕ (A) | ✕ (A) |
| ODT* | ✕ (A) | ✕ (A) |
| PDF | ✓ | ✕ (A) |
| HTML | ✕ (A) | ✕ (A) |
| RTF | ✕ (A) | ✕ (A) |
| TXT | ✓ | ✕ (A) |
| XLS | ✕ (A) | ✕ (A) |
| XLSX | ✕ (A) | ✕ (A) |
| ODS | ✕ (A) | ✕ (A) |
| PPT | ✓ | ✕ (A) |
| PPTX | ✕ (A) | ✕ (A) |
| ODP | ✕ (A) | ✕ (A) |
| INDD | ✓ | ✕ (A) |
| PS | ✕ (A) | ✕ (A) |
| QXP | ✕ (A) | ✕ (A) |
| ePub | ✓ | ✕ (A) |
| AAC | ✕ (A) | ✕ (A) |
| MIDI | ✕ (A) | ✕ (A) |
| 3GP | ✕ (A) | ✕ (A) |
| MP3 | ✕ (A) | ✕ (A) |
| MP4 | ✕ (A) | ✕ (A) |
| OGA | ✕ (A) | ✕ (A) |
| OGG | ✕ (A) | ✕ (A) |
| RA | ✕ (A) | ✕ (A) |
| WAV | ✕ (A) | ✕ (A) |
| WMA | ✕ (A) | ✕ (A) |
| DVI | ✕ (A) | ✕ (A) |
| FLV | ✕ (A) | ✕ (A) |
| M4V | ✕ (A) | ✕ (A) |
| MPG | ✕ (A) | ✕ (A) |
| OGV | ✕ (A) | ✕ (A) |
| MOV | ✕ (A) | ✕ (A) |
| WMV | ✕ (A) | ✕ (A) |
| SWF | ✕ (A) | ✕ (A) |
| TGZ | 不適用 | ✕ (A) |
| JAR | ✓ | ✕ (A) |
| RAR | 不適用 | ✕ (A) |
| TAR | 不適用 | ✕ (A) |
| ZIP | ✓ | ✕ (A) |

下列圖例說明矩陣中使用的符號：

| 符號 | 含義 |
|---|---|
| ✓ | 此檔案格式支援此功能 |
| ✕ (A) | 此檔案格式不支援此功能 |
| 不適用 | 此功能不適用於此檔案格式 |
| &#42; | 此功能需要在AEM製作例項上提供此檔案格式的附加支援，但在資產發佈至Brand Portal後則不需要在Brand Portal上提供 |

## 取消共用連結資產 {#unshare-assets-shared-as-a-link}

若要以連結形式取消共用先前共用的資產，請執行以下操作：

1. 當您登入Brand Portal時，**[!UICONTROL 檔案]**&#x200B;檢視會依預設開啟。 若要檢視您以連結形式共用的資產，請導覽至&#x200B;**[!UICONTROL 共用連結]**&#x200B;檢視。

1. 從顯示的清單中檢閱您共用的連結。

   ![](assets/shared-links.png)

1. 若要從清單中取消共用連結，請選取該連結，然後按一下頂端工具列中的&#x200B;**[!UICONTROL 取消共用]**&#x200B;圖示。

   ![](assets/unshare-asset.png)

   >[!NOTE]
   >
   >顯示共用連結的方式因使用者而異。 此功能未顯示租使用者所有使用者共用的所有連結。

1. 在警告訊息方塊中，按一下&#x200B;**[!UICONTROL 繼續]**&#x200B;以確認取消共用。 連結的專案會從共用連結清單中移除。
