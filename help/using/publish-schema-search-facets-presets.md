---
title: Publish預設集、結構和Brand Portal的Facet
description: 瞭解如何將預設集、結構和Facet發佈至Brand Portal。
topic-tags: publish
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
exl-id: 9b585606-6538-459b-87a9-2e68df0087b3
source-git-commit: 4d9d7afa2cd45ea68c2e15338c92aa29ecf09f91
workflow-type: tm+mt
source-wordcount: '1116'
ht-degree: 0%

---

# Publish預設集、結構和Brand Portal的Facet {#publish-presets-schema-and-facets-to-brand-portal}

本文深入探討如何從AEM製作例項將影像預設集、中繼資料結構以及自訂搜尋Facet發佈至Brand Portal。 發佈功能可讓組織重複使用在AEM作者執行個體上建立或編輯的影像預設集、中繼資料結構以及搜尋Facet。 此方法可減少重複工作。

>[!NOTE]
>
>從AEM 6.2 SP1-CFP7和AEM 6.3 SP 1-CFP 1 (6.3.1.1)開始，您就可以從AEM製作執行個體將影像預設集、中繼資料結構和Search Facet發佈至Brand Portal。

## Publish影像預設集至Brand Portal {#publish-image-presets-to-brand-portal}

影像預設集是在影像傳送時套用至影像的一組大小調整和格式命令。 影像預設集可在Brand Portal中建立和修改。 或者，如果AEM Author例項以Dynamic Media模式執行，使用者可以在AEM Author中建立預設集，並將其發佈至AEM Assets Brand Portal。 此方法可避免在Brand Portal中重新建立相同的預設集。
預設集建立後，會在資產詳細資料轉譯邊欄和下載對話方塊中列為動態轉譯。

>[!NOTE]
>
>如果AEM Author執行個體不是在&#x200B;**[!UICONTROL Dynamic Media模式]**&#x200B;中執行(客戶尚未購買Dynamic Media)，則上傳時不會建立資產的&#x200B;**[!UICONTROL 金字塔TIFF]**&#x200B;轉譯。 影像預設集或動態轉譯可在資產的&#x200B;**[!UICONTROL 金字塔TIFF]**&#x200B;上運作。 因此，如果&#x200B;**[!UICONTROL 金字塔TIFF]**&#x200B;無法在AEM Author執行個體上使用，則無法在Brand Portal上使用。 因此，資產詳細資訊頁面和下載對話方塊的轉譯邊欄中不會出現動態轉譯。

若要將影像預設集發佈至Brand Portal：

1. 在AEM Author執行個體中，按一下AEM標誌以存取全域導覽主控台，然後按一下「工具」圖示並導覽至&#x200B;**[!UICONTROL Assets >影像預設集]**。
1. 從影像預設集清單中選取影像預設集或多個影像預設集，然後按一下&#x200B;**[!UICONTROL Publish至Brand Portal]**。

![](assets/publishpreset.png)

>[!NOTE]
>
>當使用者按一下&#x200B;**[!UICONTROL Publish到Brand Portal]**&#x200B;時，影像預設集會排入佇列等候發佈。 建議使用者監視復寫代理程式的記錄檔，以確認發佈是否成功。

若要從Brand Portal取消發佈影像預設集：

1. 在AEM Author執行個體中，按一下AEM標誌以存取全域導覽主控台，然後按一下&#x200B;**[!UICONTROL 工具]**&#x200B;圖示並導覽至&#x200B;**[!UICONTROL Assets >影像預設集]**。
1. 選取影像預設集，並從上方的可用選項中選取&#x200B;**[!UICONTROL 從Brand Portal移除]**。

## Publish中繼資料結構至Brand Portal {#publish-metadata-schema-to-brand-portal}

中繼資料結構描述在資產/集合的屬性頁面上顯示的版面和屬性。

![](assets/metadata-schema-editor.png) ![](assets/asset-properties-1.png)

如果使用者在AEM Author例項上編輯了預設結構，並且他們想要使用與Brand Portal上的預設結構相同的結構，請將中繼資料結構表單發佈到Brand Portal。 在這種情況下，從AEM編寫執行個體發佈的預設結構描述會覆寫Brand Portal的預設結構描述。

如果使用者已在AEM Author例項上建立自訂結構，可將自訂結構描述發佈至Brand Portal，而非在那裡重新建立相同的自訂結構。 之後，使用者可以將此自訂結構描述套用至Brand Portal中的任何資料夾/集合。

>[!NOTE]
>
>如果預設結構描述在AEM執行個體上鎖定，則無法將其發佈到Brand Portal。 也就是說，這些檔案並不會被編輯。

![](assets/default-schema-form.png)

>[!NOTE]
>
>如果資料夾在AEM Author例項上套用了結構描述，Brand Portal上也必須存在相同的結構描述。 這麼做有助於維護AEM Author和Brand Portal上資產屬性頁面的一致性。

若要將中繼資料結構從AEM作者例項發佈至Brand Portal：

1. 在AEM Author執行個體中，按一下AEM標誌以存取全域導覽主控台，然後按一下「工具」圖示並導覽至&#x200B;**[!UICONTROL Assets >中繼資料結構]**。
1. 選取中繼資料結構描述，並從上方的可用選項中選取&#x200B;**[!UICONTROL Publish to Brand Portal]**。

>[!NOTE]
>
>當使用者按一下&#x200B;**[!UICONTROL Publish到Brand Portal]**&#x200B;時，中繼資料結構會排入發佈佇列。 建議使用者監視復寫代理程式的記錄檔，以確認發佈是否成功。

若要從Brand Portal取消發佈中繼資料結構：

1. 在AEM Author執行個體中，按一下AEM標誌以存取全域導覽主控台，然後按一下「工具」圖示並導覽至&#x200B;**[!UICONTROL Assets >中繼資料結構]**。
1. 選取中繼資料結構描述，並從上方的可用選項中選取&#x200B;**[!UICONTROL 從Brand Portal移除]**。

## Publish搜尋Facet至Brand Portal {#publish-search-facets-to-brand-portal}

搜尋表單為Brand Portal上的使用者提供[多面向搜尋](../using/brand-portal-search-facets.md)的功能。 搜尋Facet可為Brand Portal上的搜尋提供更精細的粒度。 搜尋表單中新增的所有[述詞](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-65/content/assets/administer/search-facets)都可供使用者作為搜尋篩選中的搜尋Facet。

![](assets/property-predicate-removed.png)
![](assets/search-form.png)

若要在AEM Author執行個體的&#x200B;**[!UICONTROL Assets管理搜尋邊欄]**&#x200B;上使用自訂搜尋表單，請直接將其發佈至Brand Portal，而非重新建立。

>[!NOTE]
>
>若要從AEM Assets在&#x200B;**[!UICONTROL Assets管理搜尋邊欄]**&#x200B;上發佈鎖定的搜尋表單至Brand Portal，您必須先編輯它。 編輯和發佈後，此搜尋表單會覆寫Brand Portal上現有的搜尋表單。

若要將已編輯的搜尋Facet從AEM作者例項發佈至Brand Portal：

1. 按一下AEM標誌，然後前往&#x200B;**[!UICONTROL 工具>一般>搜尋Forms]**。
1. 選取已編輯的搜尋表單，然後選取&#x200B;**[!UICONTROL Publish至Brand Portal]**。

   >[!NOTE]
   >
   >當使用者按一下&#x200B;**[!UICONTROL Publish到Brand Portal]**&#x200B;時，搜尋Facet會排入佇列等候發佈。 建議使用者監視復寫代理程式的記錄檔，以確認發佈是否成功。

若要從Brand Portal取消發佈搜尋表單：

1. 在AEM Author執行個體中，按一下AEM標誌以存取全域導覽主控台，然後按一下「工具」圖示並導覽至&#x200B;**[!UICONTROL 一般>搜尋Forms]**。
1. 選取搜尋表單，並從上方的可用選項中選取&#x200B;**[!UICONTROL 從Brand Portal移除]**。

>[!NOTE]
>
>從Brand Portal **取消發佈**&#x200B;動作會保留Brand Portal上的預設搜尋表單，不會還原為發佈前使用的最後一個搜尋表單。

### 限制 {#limitations}

1. 少數搜尋述詞不適用於Brand Portal上的搜尋篩選器。 當這些搜尋述詞作為搜尋表單的一部分從AEM Author執行個體發佈到Brand Portal時，即會被篩選掉。 因此，使用者可以在Brand Portal上看到較少已發佈表單中的述詞數量。 檢視Brand Portal[&#128279;](../using/brand-portal-search-facets.md#list-of-search-predicates)上適用於篩選器的搜尋述詞。

1. 對於[!UICONTROL 選項述詞]，如果使用者使用任何自訂路徑來讀取AEM Author執行個體上的選項，則它無法在Brand Portal上運作。 這些額外的路徑和選項沒有透過搜尋表單發佈至Brand Portal。 在此情況下，使用者可以在&#x200B;**[!UICONTROL 選項述詞]**&#x200B;內的&#x200B;**[!UICONTROL 新增選項]**&#x200B;中選取&#x200B;**[!UICONTROL 手動]**&#x200B;選項，以在Brand Portal中手動新增這些選項。

![](assets/options-predicate-manual.png)
