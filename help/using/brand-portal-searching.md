---
title: 在Brand Portal上搜尋資產
description: Brand Portal搜尋功能可讓您使用Omnisearch快速搜尋相關資產，而搜尋篩選器可協助您進一步縮小搜尋範圍。 將搜尋儲存為智慧型系列，以供日後使用。
contentOwner: bdhar
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
topic-tags: SearchandPromote
exl-id: 7297bbe5-df8c-4d0b-8204-218a9fdc2292
source-git-commit: 32a67abf466dd3bf635b851b02377ed23591915e
workflow-type: tm+mt
source-wordcount: '1343'
ht-degree: 0%

---

# 在Brand Portal上搜尋資產 {#search-assets-on-brand-portal}

Brand Portal搜尋功能可讓您使用Omnisearch快速搜尋相關資產，以及使用篩選器的多面向搜尋，協助您進一步縮小搜尋範圍。 您可以在檔案或資料夾層級搜尋資產，並將搜尋結果儲存為智慧型收集。

>[!NOTE]
>
>Brand Portal不支援使用Omnisearch進行集合搜尋。
>
>不過，您可以使用[搜尋篩選器來取得相關集合](#search-collection)的清單。

## 使用Omnisearch搜尋資產 {#search-assets-using-omnisearch}

若要在Brand Portal上搜尋資產：

1. 在工具列中按一下&#x200B;**[!UICONTROL 搜尋]**&#x200B;圖示，或按下&#x200B;**[!UICONTROL /]** （正斜線）鍵以啟動Omnisearch。

   ![](assets/omnisearchicon-1.png)

1. 在搜尋方塊中，輸入您要搜尋之資產的關鍵字。

   ![](assets/omnisearch.png)

   >[!NOTE]
   >
   >* Omnisearch中至少需要3個字元，才會顯示搜尋建議。
   >* 搜尋`mountain biking`時，Omnisearch會在搜尋結果中傳回中繼資料欄位中同時有`mountain`和`biking`可用的所有資產。 例如，`Title`欄位中的`mountain`和`Description`欄位中的`biking`。 這兩個字詞都必須在中繼資料欄位中可用，才能顯示在搜尋結果中。 不過，Omnisearch會在搜尋結果中傳回資產，即便智慧型標籤中繼資料欄位中只有兩個辭彙可供使用。 例如，假設某個資產將`mountain`當作智慧標籤，但在任何其他中繼資料欄位中缺少`biking`。 接著您搜尋`mountain biking`。 Omnisearch仍會在搜尋結果中傳回資產。 此工作流程可確保不會遺漏具有相關標籤的資產。

1. 從下拉式清單中顯示的相關建議中選取，以快速存取相關資產。

   ![](assets/assets-search-result.png)

   *使用Omnisearch搜尋資產*

若要進一步瞭解使用智慧標籤資產的搜尋行為，請移至[瞭解搜尋結果和行為](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-65/content/assets/using/search-assets)。

## 在「篩選器」面板中使用Facet進行搜尋 {#search-using-facets-in-filters-panel}

「篩選器」面板中的搜尋Facet可為您的搜尋體驗增加精細度，並讓搜尋功能更有效率。 搜尋Facet會使用多個維度（述詞），讓您執行複雜的搜尋。 您可以輕鬆向下展開至所需的詳細資訊層級，以更集中地搜尋。

例如，如果您要尋找影像，您可以選擇您要點陣圖或向量影像。 您可以在「檔案型別」搜尋Facet中指定影像的MIME型別，進一步縮小搜尋範圍。 同樣地，在搜尋檔案時，您可以指定格式，例如PDF或MS® Word格式。

Brand Portal中的![篩選器面板](assets/file-type-search.png "Brand Portal中的篩選器面板")

**[!UICONTROL 篩選器]**&#x200B;面板包含幾個標準Facet，例如 — **[!UICONTROL 路徑瀏覽器]**、**[!UICONTROL 檔案型別]**、**[!UICONTROL 檔案大小]**、**[!UICONTROL 狀態]**&#x200B;以及&#x200B;**[!UICONTROL 方向]**。
不過，您可以[新增自訂搜尋Facet](../using/brand-portal-search-facets.md)，或從&#x200B;**[!UICONTROL 篩選器]**&#x200B;面板中移除特定的Facet。 只需編輯基礎搜尋表單中的述詞。 檢視Brand Portal](../using/brand-portal-search-facets.md#list-of-search-predicates)上可用和可用的[搜尋述詞清單。

若要將篩選器套用至您的搜尋，請使用可用的[搜尋Facet](../using/brand-portal-search-facets.md)：

1. 按一下覆蓋圖示並選取&#x200B;**[!UICONTROL 篩選器]**。

   ![](assets/selectorrail.png)

1. 從左側的&#x200B;**[!UICONTROL 篩選器]**面板中，選取適當的選項以套用相關的篩選器。
例如，使用下列標準篩選器：

   * **[!UICONTROL 路徑瀏覽器]**&#x200B;以搜尋特定目錄中的資產。 路徑瀏覽器的述詞預設搜尋路徑為`/content/dam/mac/<tenant-id>/`，可透過編輯預設搜尋表單進行設定。

   >[!NOTE]
   >
   >對於非管理員使用者，[!UICONTROL 篩選器]面板中的[!UICONTROL 路徑瀏覽器]只會顯示與他們共用的資料夾（及其上級資料夾）的內容結構。\
   >若是管理員使用者，路徑瀏覽器可讓您導覽至Brand Portal中的任何資料夾。

   * **[!UICONTROL 檔案型別]**&#x200B;以指定您要尋找的資產檔案型別（影像、檔案、多媒體、封存）。 此外，您可以縮小搜尋範圍，例如，為影像或檔案格式(PDF或MS® Word)指定MIME型別（Tiff、點陣圖、GIMP影像）。
   * **[!UICONTROL 檔案大小]**&#x200B;以根據資產大小來搜尋資產。 您可以指定大小範圍的上限和下限，以縮小搜尋範圍，並指定要搜尋的度量單位。
   * **[!UICONTROL 狀態]**&#x200B;以根據資產狀態來搜尋資產，例如核准（已核准、已要求變更、已拒絕、擱置中）和到期。
   * **[!UICONTROL 平均評分]**，以根據資產的評分搜尋資產。
   * **[!UICONTROL 方向]**，根據資產的方向（水準、垂直、正方形）搜尋資產。
   * **[!UICONTROL 樣式]**&#x200B;以根據資產的樣式（彩色、單色）搜尋資產。
   * **[!UICONTROL 視訊格式]**，依據其格式(DVI、Flash、MPEG4、MPEG、OGG Theora、QuickTime、Windows Media、WebM)搜尋視訊資產。

   您可以編輯基礎搜尋表單，以使用「篩選器」面板中的[自訂搜尋Facet](../using/brand-portal-search-facets.md)。

   * **[!UICONTROL 屬性述詞]**&#x200B;若用於搜尋表單，可讓您搜尋符合述詞對應之中繼資料屬性的資產。\
     例如，如果「屬性述詞」對應至`jcr:content/metadata/dc:title`，您可以根據資產的標題來搜尋資產。\
     [!UICONTROL 屬性述詞]支援下列文字搜尋：

     **部分片語**
若要允許使用屬性述詞中的部分詞語來搜尋資產，請啟用「搜尋表單」中的**[!UICONTROL 部分搜尋]**&#x200B;核取方塊。 此方法可讓您搜尋所需的資產，即使您未指定資產中繼資料中使用的確切字詞或片語。

     >[!NOTE]
     >
     > Brand Portal支援下列「部分搜尋」欄位：
     >
     >* `jcr:content/metadata/dc:title`
     >* `jcr:content/jcr:title`
     >* `jcr:content/metadata/dc:format`

     您可以：
      * 在「篩選器」面板的Facet中，指定搜尋片語中的單字。 例如，如果您搜尋字詞&#x200B;**climb** （且「屬性述詞」對應至`dc:title`屬性），則系統會傳回標題片語中包含&#x200B;**climb**&#x200B;字的所有資產。
      * 指定搜尋片語中單字的一部分，並以萬用字元(&#42;)填滿空隙。
例如，搜尋：
         * **climb&#42;**&#x200B;傳回標題片語中字元開頭為「climb」的所有資產。
         * **&#42;climb**&#x200B;傳回標題片語中字詞結尾為&quot;climb&quot;的所有資產。
         * **&#42;climb&#42;**&#x200B;傳回標題片語中包含「climb」字元的所有資產。

     **不區分大小寫的文字**
您可以在屬性述詞中允許不區分大小寫的搜尋。 只需啟用[搜尋表單]中的**[!UICONTROL 忽略大小寫]**&#x200B;核取方塊。 依預設，「屬性述詞」中的文字搜尋會區分大小寫。

   >[!NOTE]
   >
   >選取&#x200B;**[!UICONTROL 部分搜尋]**&#x200B;核取方塊時，預設會選取&#x200B;**[!UICONTROL 忽略大小寫]**。

   ![](assets/wildcard-prop-1.png)

   搜尋結果會根據套用的篩選器以及搜尋結果計數顯示。

   ![](assets/omnisearch-with-filters.png)

   具有搜尋結果計數的資產搜尋結果。

1. 您可以從搜尋結果輕鬆導覽至某個專案，並使用瀏覽器中的「上一步」按鈕返回相同的搜尋結果，而無需重新執行搜尋查詢。

## 將搜尋儲存為智慧型集合 {#save-your-searches-as-smart-collection}

您可以將搜尋設定儲存為智慧型集合，以便能夠快速重複相同的搜尋，而無需稍後重做相同的設定。 不過，您無法在集合中套用搜尋篩選器。

若要將搜尋設定儲存為智慧型集合：

1. 按一下&#x200B;**[!UICONTROL 儲存智慧型集合]**，並提供智慧型集合的名稱。

   若要讓所有使用者都能存取智慧型集合，請選取&#x200B;**[!UICONTROL 公用]**。 系統會顯示訊息，確認智慧型系列已建立，並已新增至您已儲存的搜尋清單。

   >[!NOTE]
   >
   >您可以限制非管理員使用者將智慧型集合設為公開，以避免非管理員使用者在組織的Brand Portal上建立大量公開的智慧型集合。 組織可以從管理工具面板中可用的&#x200B;**[!UICONTROL 一般]**&#x200B;設定中停用&#x200B;**[!UICONTROL 允許公用智慧型集合建立]**&#x200B;設定。

   ![](assets/save_smartcollectionui.png)

1. 若要以不同的名稱儲存智慧型集合，並選取或清除&#x200B;**[!UICONTROL 公用]**&#x200B;核取方塊，請按一下&#x200B;**[!UICONTROL 編輯智慧型集合]**。

   ![](assets/edit_smartcollection.png)

1. 在&#x200B;**[!UICONTROL 編輯智慧型集合]**&#x200B;對話方塊中，選取&#x200B;**[!UICONTROL 另存新檔]**&#x200B;並輸入智慧型集合的名稱。 按一下「**[!UICONTROL 儲存]**」。

   ![](assets/saveas_smartsearch.png)


## 搜尋集合 {#search-collection}

集合不支援Omnisearch。 不過，您可以套用搜尋篩選器，以列出[!UICONTROL 集合]介面內的相關集合。

從[!UICONTROL 集合]介面，按一下覆蓋圖示以開啟左側邊欄中的篩選面板。 從可用的篩選器（`modified date`、`access type`和`tags`）套用單一或多個搜尋篩選器。 它會根據套用的篩選器列出最相關的集合集。

![](assets/collection-search.png)
