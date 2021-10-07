---
title: 共用資料夾
seo-title: Share folders
description: Brand Portal不支援資產擷取，因此必須從預先設定的Experience Manager Assets Author例項將資產發佈至Brand Portal。 Brand Portal的非管理員使用者無法存取已發佈的資產，除非在使用Experience Manager例項設定復寫時已設定，且必須與他們共用。
seo-description: Brand Portal does not support asset ingestion so assets must be published to Brand Portal from a pre-configured Experience Manager Assets Author instance. Published assets are not accessible to non-admin users of Brand Portal, unless configured while configuring replication with Experience Manager instance, and need to be shared with them.
uuid: 340d0a49-b708-4f0e-9fb8-99c824942f34
content-type: reference
topic-tags: sharing
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: 2332c16f-40be-4673-8cc6-2360d5b74116
exl-id: d28cf927-60e8-437e-9cba-92f7e19020e7
source-git-commit: 4caa4263bd74b51af7504295161c421524e51f0c
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 1%

---

# 在Brand Portal上共用資料夾 {#share-folders}

資產必須從預先設定的「Experience Manager作者」例項發佈至Brand Portal，因為Brand Portal不支援資產擷取。

## Brand Portal中的資料夾共用工作流程 {#folder-sharing-workflow-in-brand-portal}

以下說明資料夾共用工作流程和使用者存取：

* 依預設，從Experience Manager Assets發佈至Brand Portal的所有資料夾都只會顯示給Brand Portal管理員，除非在設定復寫時標示為公用。
* 管理員使用&#x200B;**[!UICONTROL 資料夾屬性]**&#x200B;控制台與選擇性用戶或組共用資料夾。 只有共用資料夾的使用者或群組在登入Brand Portal後，才能看到資料夾。 其他使用者看不到該資料夾。
* 管理員還可以通過&#x200B;**[!UICONTROL 資料夾屬性]**&#x200B;控制台中的&#x200B;**[!UICONTROL 公用資料夾]**&#x200B;複選框，將資料夾設為公用。 所有使用者都可看到公用資料夾。

* 無論使用者角色和權限為何，當使用者登入Brand Portal時，都會看到所有公用資料夾，以及直接與他們共用的資料夾，或與他們所屬的群組共用的資料夾。 私人資料夾或與其他使用者共用的資料夾不會顯示給所有使用者。

### 在Brand Portal上與使用者群組共用資料夾 {#sharing-folders-with-user-groups-on-brand-portal}

資料夾資產的存取權限取決於其父資料夾的存取權限，而不考慮子資料夾的設定。 在AEM中，此行為受[ACL](https://experienceleague.adobe.com/docs/experience-manager-65/administering/security/security.html)控制，因為子資料夾會從其父資料夾繼承ACL。 例如，如果資料夾A包含包含資料夾C的資料夾B，則對資料夾A具有訪問權限的用戶組（或用戶）對資料夾B和資料夾C也具有相同的訪問權限。資料夾B是A的子資料夾，會繼承其ACL，而資料夾C是B的子資料夾，會繼承其ACL。

同樣地，具有僅訪問資料夾B權限的用戶組（或用戶）對資料夾C具有相同的訪問權限，但對資料夾A則不具有訪問權限。因此，建議組織排列其內容，以便將大多數公開的資產放在子資料夾中，並可以限制從子資料夾到根資料夾的訪問。

### 發佈公用資料夾 {#public-folder-publish}

除非在設定Brand Portal復寫時選取&#x200B;**[!UICONTROL 公用資料夾發佈]**&#x200B;選項，否則非管理員使用者（例如編輯器和檢視器）無法存取從AEM Assets發佈至Brand Portal的資產。

![](assets/assetbpreplication.png)

如果停用「**[!UICONTROL 公用資料夾發佈]**」選項，管理員需要使用共用功能，特別與非管理員使用者共用這些資產。

>[!NOTE]
>
>啟用&#x200B;**[!UICONTROL 公用資料夾發佈]**&#x200B;的選項可在AEM 6.3.2.1以後使用。

## 對共用資料夾的存取 {#access-to-shared-folders}

下列矩陣會討論不同使用者角色共用/取消共用資產的存取權限和權限：

|  | 存取從AEM Assets發佈至Brand Portal的所有資料夾 | 對共用資料夾的存取 | 共用/取消共用資料夾權限 |
|---------------|-----------|-----------|------------|
| 管理員 | 是 | 是 | 是 |
| 編輯者 | 否* | 是，只有在與他們共用或與他們所屬的群組共用時 | 是，僅適用於與其共用的資料夾，或與其所屬群組共用的資料夾 |
| 檢視者 | 否* | 是，只有在與他們共用或與他們所屬的群組共用時 | 否 |
| 訪客使用者 | 否* | 是，只有在與他們共用或與他們所屬的群組共用時 | 否 |

>[!NOTE]
>
>依預設，使用AEM作者設定Brand Portal復寫時，會停用&#x200B;**[!UICONTROL 公用資料夾發佈]**&#x200B;選項。 如果已啟用選項，則所有使用者（非管理員使用者）都可依預設存取發佈至Brand Portal的資料夾。

### 非管理員使用者存取共用資料夾 {#non-admin-user-access-to-shared-folders}

非管理員使用者只能存取在Brand Portal上與他們共用的資料夾。 但是，這些資料夾在登入時在入口上的顯示方式取決於&#x200B;**[!UICONTROL 啟用資料夾階層]**&#x200B;組態的設定。

**如果已停用設定**

非管理員使用者在登入Brand Portal時，會在登陸頁面上看見與他們共用的所有資料夾。

![](assets/disabled-folder-hierarchy1-1.png)

**如果已啟用設定**

非管理員使用者在登入Brand Portal時，會看見資料夾樹狀結構（從根資料夾開始）和排列在其個別父資料夾中的共用資料夾。

這些父資料夾是虛擬資料夾，不能對其執行任何操作。 您可以使用鎖表徵圖識別這些虛擬資料夾。

暫留或在&#x200B;**[!UICONTROL 卡片檢視]**&#x200B;中選取時，不會顯示任何動作任務，這點與共用資料夾不同。 **** 在「欄檢視」和「清單檢視」中選取虛擬資料 **[!UICONTROL 夾時]** 會顯示 **[!UICONTROL 「概觀」按鈕]**。

>[!NOTE]
>
>請注意，虛擬資料夾的預設縮圖是第一個共用資料夾的縮圖影像。

![](assets/enabled-hierarchy1-1.png) ![](assets/hierarchy1-nonadmin-1.png) ![](assets/hierarchy-nonadmin-1.png) ![](assets/hierarchy2-nonadmin-1.png)

## 共用資料夾 {#how-to-share-folders}

若要與Brand Portal上的使用者共用資料夾，請執行下列步驟：

1. 按一下左側的覆蓋圖示，然後選擇&#x200B;**[!UICONTROL Navigation]**。

   ![](assets/selectorrail.png)

1. 從左側的脫軌中，選擇&#x200B;**[!UICONTROL 檔案]**。

   ![](assets/access_files.png)

1. 從Brand Portal介面中，選取您要共用的資料夾。

   ![](assets/share-folders.png)

1. 從頂部工具欄中，選擇&#x200B;**[!UICONTROL 共用]**。

   ![](assets/share_icon.png)

   將顯示[!UICONTROL 資料夾屬性]控制台。

   ![](assets/folder_properties.png)

1. 在&#x200B;**[!UICONTROL 資料夾屬性]**&#x200B;控制台中，如果不希望向用戶顯示預設名稱，請在&#x200B;**[!UICONTROL 資料夾標題]**&#x200B;欄位中指定資料夾標題。
1. 從&#x200B;**[!UICONTROL 添加用戶]**&#x200B;清單中，選擇要與其共用資料夾的用戶或組，然後按一下&#x200B;**[!UICONTROL 添加]**。
要僅與來賓用戶共用資料夾，而不要與其他用戶共用資料夾，請從**[!UICONTROL 成員]**&#x200B;下拉清單中選擇&#x200B;**[!UICONTROL 匿名用戶]**。

   ![](assets/only-anonymous.png)

   >[!NOTE]
   >
   >要使資料夾可供所有用戶使用（無論其組成員資格和角色如何），請選中&#x200B;**[!UICONTROL 公用資料夾]**&#x200B;複選框將其設為公用。

1. 如有必要，按一下「**[!UICONTROL 更改縮略圖]**」以修改資料夾的縮略圖。
1. 按一下「**[!UICONTROL 儲存]**」。

1. 若要存取共用資料夾，請使用您共用資料夾之使用者的憑證登入Brand Portal。 在介面中檢閱共用資料夾。

## 取消共用資料夾 {#unshare-the-folders}

若要取消共用先前共用的資料夾，請執行下列步驟：

1. 從Brand Portal介面中，選取您要取消共用的資料夾。

   ![](assets/share-folders-1.png)

1. 從頂端的工具列按一下&#x200B;**[!UICONTROL 共用]**。
1. 在&#x200B;**[!UICONTROL 資料夾屬性]**&#x200B;控制台的&#x200B;**[!UICONTROL 成員]**&#x200B;下，按一下用戶旁的&#x200B;**[!UICONTROL x]**&#x200B;符號，從與共用資料夾的用戶清單中刪除它們。

   ![](assets/folder_propertiesunshare.png)

1. 在警告訊息方塊中，按一下&#x200B;**[!UICONTROL Confirm]**以確認取消共用。
按一下「**[!UICONTROL 儲存]**」。

1. 以您從共用清單中移除之使用者的認證登入Brand Portal。 該資料夾不再適用於使用者的Brand Portal介面。
