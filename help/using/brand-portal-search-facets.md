---
title: 使用自訂搜尋 Facet
seo-title: Use custom search facets
description: 管理員可以將搜尋述詞新增至「篩選器」面板，以自訂搜尋，並讓搜尋功能變得通用。
seo-description: Administrators can add search predicates to the Filters panel to customize search and make the search functionality versatile.
uuid: 986fba5a-fac5-4128-ac75-d04da5b52d45
content-type: reference
topic-tags: administration
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: 19faa028-246b-42c7-869f-97c95c7a1349
role: Admin
exl-id: c07e1268-2c83-40ba-8dcd-5dade3a10141
source-git-commit: 955cd8afe939ff47e9f08f312505e230e2f38495
workflow-type: tm+mt
source-wordcount: '1279'
ht-degree: 8%

---

# 使用自訂搜尋 Facet {#use-custom-search-facets}

管理員可以將搜尋述詞新增至[!UICONTROL 篩選器]面板，以自訂搜尋並讓搜尋功能通用。

Brand Portal支援[多面搜尋](../using/brand-portal-searching.md#search-using-facets-in-filters-panel)以精細搜尋已核准的品牌資產，這可能是因為&#x200B;[**篩選器**&#x200B;面板](../using/brand-portal-searching.md#search-using-facets-in-filters-panel)所致。 透過管理工具的&#x200B;**[!UICONTROL 搜尋表單]**，可在「篩選器」面板上使用搜尋Facet。 管理工具的「搜尋Forms」頁面中存在名為「資產管理搜尋邊欄」的預設搜尋表單。 不過，管理員可以借由新增、修改或移除搜尋述詞，編輯預設的搜尋表單（資產管理搜尋邊欄），來自訂預設的「篩選器」面板，進而讓搜尋功能變得通用。

您可以使用各種搜尋述詞來自訂&#x200B;**[!UICONTROL 篩選器]**&#x200B;面板。 例如，新增屬性述詞以搜尋符合您在此述詞中指定之單一屬性的資產。 新增選項述詞，以搜尋符合您為特定屬性所指定之一或多個值的資產。 新增日期範圍述詞，以搜尋在指定日期範圍內建立的資產。

>[!NOTE]
>
>Experience Manager資產可讓組織[將自訂的搜尋表單從AEM作者](../using/publish-schema-search-facets-presets.md#publish-search-facets-to-brand-portal)發佈至Brand Portal，而非在Brand Portal上重新建立相同的表單。

## 新增搜尋述詞 {#add-a-search-predicate}

要將搜索謂詞添加到&#x200B;**[!UICONTROL 篩選器]**&#x200B;面板：

1. 若要存取管理工具，請按一下頂端工具列中的Experience Manager標誌。

   ![](assets/aemlogo.png)

1. 在管理工具面板中，按一下&#x200B;**[!UICONTROL 搜尋Forms]**。

   ![](assets/navigation-panel-1.png)

1. 在&#x200B;**[!UICONTROL 搜尋Forms]**&#x200B;頁面中，選取&#x200B;**[!UICONTROL 資產管理搜尋邊欄]**。

   ![](assets/search-forms-page.png)

1. 在頂部顯示的工具欄上，按一下「編輯」(**[!UICONTROL Edit)]**&#x200B;以開啟編輯搜索表單。

   ![](assets/edit-search-form-1.png)

1. 在[!UICONTROL 編輯搜索表單]頁中，將謂詞從[!UICONTROL 選擇謂詞]頁簽拖動到主窗格。 例如，拖曳&#x200B;**[!UICONTROL 屬性述詞]**。

   主窗格中會顯示&#x200B;**[!UICONTROL Property]**&#x200B;欄位，右側的&#x200B;**[!UICONTROL Settings]**&#x200B;標籤會顯示屬性謂語。

   ![](assets/partial-prop-predicate.png)

   >[!NOTE]
   >
   >**[!UICONTROL Settings]**&#x200B;標籤中的標題標籤標識您選擇的謂詞類型。

1. 在&#x200B;**[!UICONTROL Settings]**&#x200B;標籤中，輸入屬性謂語的標籤、佔位符文本和說明。

   * 如果您想要根據指定的屬性值，允許資產的部分片語搜尋（和萬用字元搜尋），請選取「**[!UICONTROL 部分搜尋]**」。 預設情況下，謂語支援全文搜索。
   * 如果您希望根據屬性值進行資產搜尋時不區分大小寫，請選取「**[!UICONTROL 忽略大小寫]**」。 依預設，在「搜尋篩選器」中搜尋屬性值會區分大小寫。

   >[!NOTE]
   >
   >選中&#x200B;**[!UICONTROL 部分搜索]**&#x200B;複選框時，預設選中&#x200B;**[!UICONTROL 忽略大小寫]**。

1. 在&#x200B;**[!UICONTROL 屬性名稱]**&#x200B;欄位中，開啟屬性選擇器，並根據其選擇執行搜索的屬性。 或者，輸入屬性的名稱。 例如，輸入 `  jcr :content/metadata/dc:title` 或 `./jcr:content/metadata/dc:title`。

   >[!NOTE]
   >
   >在Brand Portal中，預設會對`dam:asset`的`jcrcontent/metadata`中的所有屬性（以`xmp`開頭的屬性除外）進行索引。
   >
   >建立屬性述詞時，可以使用任何已編列索引的屬性。 如果配置了任何非索引屬性，則未索引屬性上的搜索查詢可能不提供任何搜索結果。

   ![](assets/title-prop.png)

1. 按一下&#x200B;**[!UICONTROL Done]**&#x200B;以儲存設定。
1. 從[!UICONTROL Assets]使用者介面，按一下覆蓋圖示並選擇&#x200B;**[!UICONTROL Filter]**&#x200B;以導覽至&#x200B;**[!UICONTROL Filters]**&#x200B;面板。 The **[!UICONTROL Property]** predicate is added to the panel.

   ![](assets/property-filter-panel.png)

1. 在&#x200B;**[!UICONTROL Property]**&#x200B;文字方塊中輸入要搜尋的資產標題。 例如，「Adobe」。 執行搜尋時，標題符合「Adobe」的資產會顯示在搜尋結果中。

## 搜索謂詞清單 {#list-of-search-predicates}

與新增&#x200B;**[!UICONTROL Property]**&#x200B;述詞的方式類似，您可以將下列述詞新增至&#x200B;**[!UICONTROL Filters]**&#x200B;面板：

| **謂語名稱** | **說明** | **屬性** |
|-------|-------|----------|
| **[!UICONTROL 路徑瀏覽器]** | 搜尋述詞以搜尋特定位置的資產。 **注意：** *對於登入的使用者，「篩選」上的路徑瀏覽器只會顯示與使用者共用之資料夾（及其祖先）的內容結構。* <br> 管理員使用者可使用路徑瀏覽器導覽至任何資料夾，以搜尋該資產。<br> 然而，非管理員使用者可以在路徑瀏覽器中導覽至該資料夾，以在資料夾中搜尋資產（可供他們存取）。 | <ul><li>欄位標籤</li><li>路徑</li><li>說明</li></ul> |
| **[!UICONTROL 屬性]** | 根據特定中繼資料屬性搜尋資產。 **注意：** *選取「部分搜尋」時，預設會選取「忽略大小寫」*。 | <ul><li>欄位標籤</li><li>預留位置</li><li>屬性名稱</li><li>部分搜尋</li><li>忽略大小寫</li><li> 說明</li></ul> |
| **[!UICONTROL 多值屬性]** | 與屬性述詞類似，但允許多個輸入值，由分隔字元分隔（預設值為COMMA[,]），在結果中返回與任何輸入值匹配的資產。 | <ul><li>欄位標籤</li><li>預留位置</li><li>屬性名稱</li><li>分隔符號支援</li><li>忽略大小寫</li><li>說明</li></ul> |
| **[!UICONTROL 標記]** | 搜尋述詞以根據標籤來搜尋資產。 您可以設定「路徑」屬性，以填入「標籤」清單中的各種標籤。 *注意：如果管理員從AEM發佈搜尋表單，其中路徑不包含租用戶資訊，例如[!UICONTROL `/etc/tags/<custom_tag_namespace>`]，則可能需要變更路徑值，例如[!UICONTROL `/etc/tags/mac/<tenant_id>/<custom_tag_namespace>`]。 | <ul><li>欄位標籤</li><li>屬性名稱</li><li>路徑</li><li>說明</li></ul> |
| **[!UICONTROL 路徑]** | 搜尋述詞以搜尋特定位置的資產。 | <ul><li>欄位標籤</li><li>路徑</li><li>說明</li></ul> |  |
| **[!UICONTROL 相對日期]** | 搜尋述詞，以根據資產建立的相對日期來搜尋資產。 | <ul><li>欄位標籤</li><li>屬性名稱</li><li>相對日期</li></ul> |
| **[!UICONTROL 範圍]** | 搜尋述詞，以搜尋位於指定屬性值範圍內的資產。 在「篩選器」面板中，您可以指定範圍的最小和最大屬性值。 | <ul><li>欄位標籤</li><li>屬性名稱</li><li>說明</li></ul> |
| **[!UICONTROL 日期範圍]** | 搜尋述詞，以搜尋在日期屬性的指定範圍內建立的資產。 在「篩選」面板中，您可以指定「開始」和「結束」日期。 | <ul><li>欄位標籤</li><li>預留位置</li><li>屬性名稱</li><li>範圍文字（開始日期）</li><li>範圍文字（至）</li><li>說明</li></ul> |
| **[!UICONTROL 日期]** | 根據日期屬性，以滑桿式搜尋資產時的搜尋述詞。 | <ul><li>欄位標籤</li><li>屬性名稱</li><li>說明</li></ul> |
| **[!UICONTROL 檔案大小]** | 搜尋述詞以根據資產大小來搜尋資產。 | <ul><li>欄位標籤</li><li>屬性名稱</li><li>路徑</li><li>說明</li></ul> |
| **[!UICONTROL 上次修改的資產]** | 搜尋述詞，以根據上次修改的日期搜尋資產。 | <ul><li>欄位標籤</li><li>屬性名稱</li><li>說明</li></ul> |
| **[!UICONTROL 核准狀態]** | 搜尋述詞，以根據核准中繼資料屬性搜尋資產。 預設屬性名稱為&#x200B;**dam:status**。 | <ul><li>欄位標籤</li><li>屬性名稱</li><li>說明</li></ul> |
| **[!UICONTROL 簽出狀態]** | 搜尋述詞，以從AEM Assets發佈資產時，根據資產的結帳狀態來搜尋資產。 | <ul><li>欄位標籤</li><li>屬性名稱</li><li>說明</li></ul> |
| **[!UICONTROL 簽出者]** | 搜尋述詞，以根據已結帳資產的使用者來搜尋資產。 | <ul><li>欄位標籤</li><li>屬性名稱</li><li>說明</li></ul> |
| **[!UICONTROL 到期狀態]** | 搜尋述詞，以根據到期狀態搜尋資產。 | <ul><li>欄位標籤</li><li>屬性名稱</li><li>說明</li></ul> |
| **[!UICONTROL 集合成員]** | 搜尋述詞，以根據資產是否屬於集合的一部分來搜尋資產。 | 說明 |
| **[!UICONTROL 隱藏]** | 此述詞不明確顯示給一般使用者，且用於任何隱藏的限制，通常用於將搜尋結果類型限制為&#x200B;**dam:Asset**。 | <ul><li>欄位標籤</li><li>屬性名稱</li><li>說明</li></ul> |

>[!NOTE]
>
>請勿使用&#x200B;**[!UICONTROL 選項述詞]**、**[!UICONTROL 發佈狀態述詞]**&#x200B;和&#x200B;**[!UICONTROL 評等述詞]**，因為這些述詞在Brand Portal中無法運作。

## 刪除搜索謂詞 {#delete-a-search-predicate}

要刪除搜索謂詞，請執行以下步驟：

1. 按一下Adobe標誌以存取管理工具。

   ![](assets/aemlogo.png)

1. 在管理工具面板中，按一下&#x200B;**[!UICONTROL 搜尋Forms]**。

   ![](assets/navigation-panel-2.png)

1. 在&#x200B;**[!UICONTROL 搜尋Forms]**&#x200B;頁面中，選取&#x200B;**[!UICONTROL 資產管理搜尋邊欄]**。

   ![](assets/search-forms-page.png)

1. 在頂部顯示的工具欄上，按一下「編輯」(**[!UICONTROL Edit)]**&#x200B;以開啟編輯搜索表單。

   ![](assets/edit-search-form-2.png)

1. 在[!UICONTROL 編輯搜索表單]頁中，從主窗格中，選擇要刪除的謂詞。 例如，選擇&#x200B;**[!UICONTROL 屬性謂詞]**。

   右側的&#x200B;**[!UICONTROL Settings]**&#x200B;頁簽顯示屬性謂詞欄位。

1. 若要刪除屬性述詞，請按一下bin圖示。 在&#x200B;**[!UICONTROL 刪除欄位]**&#x200B;對話框中，按一下&#x200B;**[!UICONTROL 刪除]**&#x200B;以確認刪除操作。

   從主窗格中刪除&#x200B;**[!UICONTROL 屬性謂詞]**&#x200B;欄位，並且&#x200B;**[!UICONTROL 設定]**&#x200B;頁簽變為空。

   ![](assets/search-form-delete-predicate.png)

1. 要保存更改，請按一下工具欄中的&#x200B;**[!UICONTROL Done]**。
1. 從&#x200B;**[!UICONTROL Assets]**&#x200B;使用者介面，按一下覆蓋圖示並選擇&#x200B;**[!UICONTROL Filter]**&#x200B;以導覽至&#x200B;**[!UICONTROL Filters]**&#x200B;面板。 **[!UICONTROL 屬性]**&#x200B;述詞已從面板中移除。

   ![](assets/property-predicate-removed.png)
