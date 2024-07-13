---
title: 共用集合
seo-title: Share a collection
description: Experience Manager Assets Brand Portal管理員可與授權使用者共用和取消共用集合或智慧型集合。 編輯者只能檢視和共用他們建立、與他們共用的收藏集和公開收藏集。
seo-description: Experience Manager Assets Brand Portal Administrators can share and unshare a collection or a smart collection with authorized users. Editors can view and share only the collections created by them, shared with them, and public collections.
uuid: 965f39cd-1378-42c1-a58a-01e1bf825aa3
contentOwner: Vishabh Gupta
content-type: reference
topic-tags: sharing
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: f053013e-5981-419f-927e-b5bb1d47eae2
exl-id: 29b877f6-4200-4299-9b8d-81d88f4e8221
source-git-commit: 26c16668224d22f133419c13ea5fe4e24335a22f
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 0%

---

# 共用集合 {#share-collections}

集合代表儲存在Adobe Experience Manager Assets Brand Portal中一組相關資產。 使用者可以透過[套用Omnisearch或Facet搜尋來建立智慧型集合，以篩選掉相關資產](brand-portal-searching.md)並將它們儲存在一起，以便輕鬆存取並進一步與其他Brand Portal使用者共用。

<!--The administrators can share and unshare a collection with the authorized Brand Portal users. Editors and viewers can view and share the collections created by them, shared with them, and public collections.-->

收藏集會透過電子郵件以連結形式分享。 有權存取共用連結的每個人都可以開啟集合，而共用的電子郵件可以轉寄給任何人。 此外，[共用連結](https://experienceleague.adobe.com/docs/experience-manager-brand-portal/using/share/brand-portal-link-share.html?lang=en)是暫時性的，僅可在有限期間存取。 或者，也可以邀請使用者成為集合的永久成員。 集合有下列使用者型別：

* **管理員**&#x200B;可以與授權的Brand Portal使用者共用或取消共用集合。 他們可以邀請其他使用者加入特定的集合，並定義他們在該集合中的角色。 此外，管理員可以建立公開集合。

* 允許&#x200B;**編輯器**&#x200B;建立和共用集合。 他們可以邀請其他使用者加入特定的集合，並定義他們在該集合中的角色。 此外，如果他們受邀以編輯者或擁有者的身分加入集合，則他們也可以共用集合。

* **檢視者**&#x200B;只能建立私人集合。 即使他們受邀成為擁有者，仍不可共用集合。

>[!NOTE]
>
>編輯者無法將公用集合變更為非公用集合，因此在&#x200B;**[!UICONTROL 集合設定]**&#x200B;對話方塊中沒有&#x200B;**[!UICONTROL 公用集合]**&#x200B;核取方塊。

## 共用集合 {#share-collection}

以下是和授權的Brand Portal使用者共用集合的步驟：

1. 登入您的Brand Portal租使用者。 依預設，**[!UICONTROL 檔案]**&#x200B;檢視會開啟，其中包含所有已發佈的資產和資料夾。

1. 從頂端的快速導覽中，按一下&#x200B;**[!UICONTROL 集合]**。

1. 從&#x200B;**[!UICONTROL 集合]**&#x200B;主控台，執行下列其中一項作業：

   * 將指標暫留在您要共用的集合上。 在集合可用的快速動作縮圖中，按一下&#x200B;**[!UICONTROL 設定]**&#x200B;圖示。

     ![](assets/settings-icon.png)

   * 選取您要共用的集合。 從頂端的工具列按一下&#x200B;**[!UICONTROL 設定]**。

     ![](assets/collection-console.png)

1. 在&#x200B;**[!UICONTROL 集合設定]**&#x200B;對話方塊中，選取您要共用集合的使用者，並選取符合其全域角色的使用者角色。 例如，將編輯者角色指派給全域編輯者，將檢視者角色指派給全域檢視者。

   或者，若要讓集合可供所有使用者使用，而不論其群組成員資格與角色為何，請選取&#x200B;**[!UICONTROL 公用集合]**&#x200B;核取方塊以將其設為公用。

   >[!NOTE]
   >
   >但是，非管理員使用者可以限制建立公開收藏集，以避免具有大量公開收藏集，從而可以節省系統空間。 組織可以停用管理工具面板中可用之&#x200B;**[!UICONTROL 一般]**&#x200B;設定中的&#x200B;**[!UICONTROL 允許建立公開集合]**&#x200B;設定。

   ![](assets/collection_sharingadduser.png)

   編輯器無法將公用集合變更為非公用集合，因此在&#x200B;**[!UICONTROL 集合設定]**&#x200B;對話方塊中沒有&#x200B;**[!UICONTROL 公用集合]**&#x200B;核取方塊。

   ![](assets/collection-setting-editor.png)

1. 按一下&#x200B;**[!UICONTROL 新增]**&#x200B;按鈕以新增使用者，然後按一下&#x200B;**[!UICONTROL 儲存]**。 系列會與使用者共用。

   >[!NOTE]
   >
   >使用者的角色可控制對集合內資產和資料夾的存取權。 如果使用者無權存取資產，則會與使用者共用空白集合。 此外，使用者的角色會控制可用於集合的動作。

## 取消共用集合 {#unshare-a-collection}

若要取消共用先前共用的集合，請執行下列動作：

1. 從&#x200B;**[!UICONTROL 集合]**&#x200B;主控台，選取您要取消共用的集合。

   從頂端的工具列按一下&#x200B;**[!UICONTROL 設定]**。

   ![](assets/collection_settings.png)

1. 在&#x200B;**[!UICONTROL 集合設定]**&#x200B;對話方塊的&#x200B;**[!UICONTROL 成員]**&#x200B;區段下，按一下使用者旁的&#x200B;**[!UICONTROL x]**&#x200B;符號，以將他們從擁有集合存取權的使用者清單中移除。

   ![](assets/unshare_collection.png)

1. 警告訊息隨即出現。 按一下&#x200B;**[!UICONTROL 確認]**&#x200B;以取消共用集合。

1. 按一下[儲存]以套用變更。****

   一旦從共用清單移除使用者，非共用集合就會從使用者的&#x200B;**[!UICONTROL 集合]**&#x200B;主控台移除。

<!--
1. Click the overlay icon on the left, and choose **[!UICONTROL Navigation]**.

   ![](assets/contenttree-1.png)

1. From the siderail on the left, click **[!UICONTROL Collections]**.

   ![](assets/access_collections.png)

1. From the **[!UICONTROL Collections]** console, do one of the following:

    * Hover the pointer over the collection you want to share. From the quick action thumbnails available for the collection, click the **[!UICONTROL Settings]** icon.

   ![](assets/settings_thumbnail.png)

    * Select the collection you want to share. From the toolbar at the top, click **[!UICONTROL Settings]**.
    
   ![](assets/collection-sharing.png)

1. In the [!UICONTROL Collection Settings] dialog box, select the users or groups with whom you want to share the collection and select the role for a user or a group to match their global role. For example, assign the Editor role to a global editor, the Viewer role to a global viewer.

   Alternatively, to make the collection available to all users irrespective of their group membership and role, make it public by selecting the **[!UICONTROL Public Collection]** check-box.

   >[!NOTE]
   >
   >However, non-admin users can be restricted from creating public collections, to avoid having numerous public collections so that system space can be saved. Organizations can disable the **[!UICONTROL Allow public collections creation]** configuration from [!UICONTROL General] settings available in admin tools panel.

   ![](assets/collection_sharingadduser.png)

   Editors cannot change a public collection to a non-public collection and, therefore, do not have **[!UICONTROL Public Collection]** check-box available in **[!UICONTROL Collection Settings]** dialog.

   ![](assets/collection-setting-editor.png)

1. Select **[!UICONTROL Add]**, and then **[!UICONTROL Save]**. The collection is shared with the chosen users.

   >[!NOTE]
   >
   >A user's role governs access to the assets and folders inside a collection. If a user does not have access to assets, an empty collection is shared with the user. Also, a user's role governs the actions available for collections.

## Unshare a collection {#unshare-a-collection}

To unshare a previously shared collection, do the following:

1. From the **[!UICONTROL Collections]** console, select the collection you want to unshare.

   In the toolbar, click **[!UICONTROL Settings]**.

   ![](assets/collection_settings.png)

1. On the **[!UICONTROL Collection Settings]** dialog box, under **[!UICONTROL Members]**, click the **[!UICONTROL x]** symbol next to users or groups to remove them from the list of users you shared the collection with.

   ![](assets/unshare_collection.png)

1. In the warning message box, click **[!UICONTROL Confirm]** to confirm unshare.

   Click **[!UICONTROL Save]**.

1. Log in to Brand Portal with the credentials of the user you removed from the shared list. The collection is removed from the **[!UICONTROL Collections]** console.
-->
