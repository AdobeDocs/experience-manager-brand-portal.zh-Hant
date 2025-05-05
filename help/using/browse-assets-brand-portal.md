---
title: 在Brand Portal上瀏覽資產
description: 使用Brand Portal上的不同檢視選項和UI元素，瀏覽資產、周游資產階層以及搜尋資產。
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
topic-tags: introduction
exl-id: 405d7861-a140-44b1-ae1f-4f0839f05033
source-git-commit: 4d9d7afa2cd45ea68c2e15338c92aa29ecf09f91
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 3%

---

# 在Brand Portal上瀏覽資產 {#browsing-assets-on-brand-portal}

Experience Manager Assets Brand Portal提供各種功能和使用者介面元素，讓您使用不同的檢視選項輕鬆瀏覽資源、導覽資產階層及搜尋資產。

頂端工具列中的Experience Manager標誌可方便管理員使用者存取管理工具面板。

![](assets/aemlogo.png)

![](assets/admin-tools-panel-2.png)

![](assets/bp_subheader.png)

Brand Portal左上角的邊欄選擇器下拉式清單，可顯示導覽至資產階層的選項、簡化搜尋並顯示資源。

![](assets/siderail-1.png)

您可以使用Brand Portal檢視選擇器中的任何可用檢視（卡片、欄和清單）來檢視、導覽和選取資產。

![](assets/viewselector.png)

## 檢視和選擇資源 {#viewing-and-selecting-resources}

從概念上講，所有檢視中檢視、導覽和選取每個檢視的方式都相同，只是處理方式根據您使用的檢視而略有差異。

您可以透過任何可用檢視檢視、瀏覽及選取（供進一步動作）您的資源：

* 欄檢視
* 卡片檢視
* 清單檢視

### 卡片檢視

![](assets/card-view.png)

卡片檢視會顯示目前層級中每個專案的資訊卡片。 這些卡片提供下列詳細資訊：

* 資產/資料夾的視覺化表示法。
* 類型
* 標題
* 名稱
* 從AEM將資產發佈到Brand Portal的日期和時間
* 大小
* 尺寸

您可以按一下卡片來向下瀏覽階層（注意避免快速動作），或使用標頭[&#128279;](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/authoring/essentials/basic-handling)中的階層連結來再次向上瀏覽。

![](assets/cardquickactions.png)

#### 非管理員使用者的卡片檢視

資料夾卡片在卡片檢視中，向非管理員使用者（編輯者、檢視者和訪客使用者）顯示資料夾階層資訊。 此功能可讓使用者知道他們存取的資料夾位置（相對於父階層）。

資料夾階層資訊對於區分名稱類似其他資料夾的資料夾和不同的資料夾階層特別有用。 如果非管理員使用者不知道與他們共用資產的資料夾結構，則名稱類似的資產/資料夾看起來會令人困惑。

* 個別卡片上顯示的路徑會遭截斷，以符合卡片大小。 不過，使用者可以將滑鼠游標停留在截斷的路徑上，將完整路徑視為工具提示。

![](assets/folder-hierarchy1.png)

**檢視資產屬性的概觀選項**

非管理員使用者（編輯器、檢視者、訪客使用者）可使用「概述」選項來檢視所選資產/資料夾的資產屬性。 「概述」選項隨即顯示：

* 在工具列的頂端，選取資產/資料夾時。
* 在下拉式清單中選取邊欄選取器時。

在選取資產/資料夾時選取&#x200B;**[!UICONTROL 總覽]**&#x200B;選項時，使用者可以看到資產建立的標題、路徑和時間。 而在資產詳細資訊頁面上，選取概述選項可讓使用者檢視資產的中繼資料。

![](assets/overview-option.png)

![](assets/overview-rail-selector.png)

#### 在卡片檢視中檢視設定

從檢視選擇器選取&#x200B;**[!UICONTROL 檢視設定]**，即可開啟&#x200B;**[!UICONTROL 檢視設定]**&#x200B;對話方塊。 它可讓您在「卡片檢視」中調整資產縮圖的大小。 如此一來，您便可個人化檢視並控制顯示的縮圖數目。

![](assets/cardviewsettings.png)

### 清單檢視

![](assets/list-view.png)

清單檢視會顯示目前層次中每個資源的資訊。 「清單」檢視提供下列詳細資訊：

* 資產的縮圖影像
* 名稱
* 標題
* 語系設定
* 類型
* 維度
* 大小
* 評等
* 顯示資產階層的資料夾路徑
* 在Brand Portal上發佈資產的日期

路徑欄可讓您輕鬆識別資料夾階層中的資產位置。 您可以按一下資源名稱來向下瀏覽階層，然後使用標頭[&#128279;](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/authoring/essentials/basic-handling)中的階層連結來向上瀏覽。

<!--
Comment Type: draft lastmodifiedby="mgulati" lastmodifieddate="2018-08-17T03:12:05.096-0400" type="annotation">Removed:- "Selecting assets in list view To select all items in the list, use the checkbox at the upper left of the list. When all items in the list are selected, this check box appears checked. To deselect all, click the checkbox. When only some items are selected, it appears with a minus sign. To select all, click the checkbox. To deselect all, click the checkbox again. You can change the order of items using the dotted vertical bar at the far right of each item in the list. Click the vertical selection bar and drag the item to a new position in the list."
 -->

### 在清單檢視中檢視設定

清單檢視預設會將資產&#x200B;**[!UICONTROL Name]**&#x200B;顯示為第一欄。 也會顯示其他資訊，例如資產&#x200B;**[!UICONTROL 標題]**、**[!UICONTROL 地區設定]**、**[!UICONTROL 型別]**、**[!UICONTROL Dimension]**、**[!UICONTROL 大小]**、**[!UICONTROL 評等]**、發佈狀態。 不過，您可以使用&#x200B;**[!UICONTROL 檢視設定]**&#x200B;來選取要顯示的資料行。

![](assets/list-view-setting.png)

### 欄檢視

![](assets/column-view.png)

使用欄檢視來瀏覽一連串重疊欄的內容樹狀結構。 此檢視可協助您視覺化並周游資產階層。

在第一欄（最左側）中選取資源，會在右側的第二欄中顯示子資源。 在第二欄中選取資源，會在右側的第三欄中顯示子資源，依此類推。

您可以在樹狀結構中向上和向下瀏覽。 按一下資源名稱或資源名稱右側的>形箭號。

* 按一下時，資源名稱和>形箭號會醒目提示。
* 點選或按一下縮圖可選取資源。
* 選取時，縮圖上會覆蓋勾號，且資源名稱會反白顯示。
* 所選資源的詳細資訊會顯示在最後一欄。

在欄檢視中選取資產時，資產的視覺化表示會連同下列詳細資料一起顯示在最後一欄：

* 標題
* 名稱
* 尺寸
* 從AEM將資產發佈到Brand Portal的日期和時間
* 大小
* 類型
* 前往資產詳細資訊頁面的更多詳細資訊選項

<!--
Comment Type: draft

<h3>Selecting Resources</h3>
-->

<!--
Comment Type: draft

<p>Selecting a specific resource depends on a combination of the view and the device:</p>
-->

<!--
Comment Type: draft

<table border="1" cellpadding="1" cellspacing="0" width="100%">
<tbody>
<tr>
<td> </td>
<td>Select</td>
<td>Deselect</td>
</tr>
<tr>
<td>Column View<br /> </td>
<td>
<ul>
<li>Desktop:<br /> Mouseover, then use the check mark quick action</li>
<li>Mobile device:<br /> Tap the thumbnail</li>
</ul> </td>
<td>
<ul>
<li>Desktop:<br /> Click the thumbnail</li>
<li>Mobile device:<br /> Tap the thumbnail</li>
</ul> </td>
</tr>
<tr>
<td>Card View<br /> </td>
<td>
<ul>
<li>Desktop:<br /> Mouseover, then use the check mark quick action</li>
<li>Mobile device:<br /> Tap-and-hold the card</li>
</ul> </td>
<td>
<ul>
<li>Desktop:<br /> Click the card</li>
<li>Mobile device:<br /> Tap the card</li>
</ul> </td>
</tr>
<tr>
<td>List View</td>
<td>
<ul>
<li>Desktop:<br /> Mouseover, then use the check mark quick action</li>
<li>Mobile device:<br /> Tap the thumbnail</li>
</ul> </td>
<td>
<ul>
<li>Desktop:<br /> Click the thumbnail</li>
<li>Mobile device:<br /> Tap the thumbnail</li>
</ul> </td>
</tr>
</tbody>
</table>
-->

<!--
Comment Type: draft

Deselecting All
-->

<!--
Comment Type: draft

<p>In all cases, as you select items the count of the items selected is displayed at the upper right of the toolbar.</p>
<p>You can deselect all items and exit selection mode by clicking the X next to the count.</p>
-->

<!--
Comment Type: draft

<p>In all views, all items can be deselected by clicking escape on the keyboard if you are using a desktop device.</p>
-->

## 內容樹狀結構 {#content-tree}

除了這些檢視之外，當您檢視並選取想要的資產或資料夾時，還可以使用樹狀檢視向下鑽研資產階層。

若要開啟樹狀檢視，請按一下左上方的邊欄選取器，然後從功能表中選取&#x200B;**[!UICONTROL 內容樹狀結構]**。

![](assets/contenttree.png)

從內容階層中，導覽至所需的資產。

![](assets/content-tree.png)

## 資產詳細資料 {#asset-details}

資產詳細資訊頁面可讓您檢視資產、下載、共用資產的連結、將其移至收藏集，或檢視其屬性頁面。 它也可讓您連續導覽相同資料夾中其他資產的詳細資訊頁面。

![](assets/asset-detail.png)

若要檢視資產的中繼資料或檢視其各種轉譯，請使用資產詳細資料頁面上的邊欄選取器。

![](assets/asset-overview.png)

您可以在資產詳細資訊頁面上檢視資產的所有可用轉譯，並從&#x200B;**[!UICONTROL 轉譯]**&#x200B;面板選取轉譯以進行預覽。

![](assets/renditions.png)

<!-- removed as it is fixed in 2022.02.0 release
>[!CAUTION]
>
>(**Experience Manager Assets as a Cloud Service** only) The following known issues will be fixed in the upcoming release:
>
>The **[!UICONTROL Renditions]** panel does not list all the static renditions of the assets that are published to Brand Portal after December 16, 2021.
>
>The **[!UICONTROL Renditions]** panel lists the smart crop renditions of the asset, however, the user cannot preview or download the smart crop renditions.
-->

若要開啟資產屬性頁面，請使用頂端列中的&#x200B;**[!UICONTROL 屬性(p)]**&#x200B;選項。

![](assets/asset-properties.png)

您也可以在資產的屬性頁面上檢視其所有相關資產(AEM上的來源或衍生資產)的清單，因為資產關係也會從AEM發佈至Brand Portal。
