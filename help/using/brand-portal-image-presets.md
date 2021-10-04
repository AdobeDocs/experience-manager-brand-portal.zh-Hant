---
title: 套用影像預設集或動態轉譯
seo-title: Apply image presets or dynamic renditions
description: '像宏一樣，影像預設集是儲存在名稱下的大小調整和格式設定命令的預定義集合。 影像預設集可讓Experience ManagerAssets Brand Portal以動態方式傳送不同大小、格式和屬性的影像。 '
seo-description: Like a macro, an image preset is a predefined collection of sizing and formatting commands saved under a name. Image presets enable Experience Manager Assets Brand Portal to dynamically deliver images of different sizes, formats, and properties.
uuid: a3c8705c-5fbd-472c-8b61-f65b3e552c1b
content-type: reference
topic-tags: administration
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: a512dfa0-fef3-4c3f-a389-a0a3a7415bac
role: Admin
exl-id: 212a1b3a-686f-4250-be06-b679b6039887
source-git-commit: 955cd8afe939ff47e9f08f312505e230e2f38495
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 3%

---

# 套用影像預設集或動態轉譯 {#apply-image-presets-or-dynamic-renditions}

像宏一樣，影像預設集是儲存在名稱下的大小調整和格式設定命令的預定義集合。 影像預設集可讓Experience ManagerAssets Brand Portal以動態方式傳送不同大小、格式和屬性的影像。

影像預設集可用來產生可預覽及下載之影像的動態轉譯。 預覽影像及其轉譯時，您可以選擇預設集，將影像重新格式化為管理員設定的規格。

(*如果「Experience Manager資產」製作例項在&#x200B;**Dynamic Media混合模式***上執行)若要在Brand Portal中檢視資產的動態轉譯，請確定其Tiff金字塔轉譯存在於您發佈至Brand Portal的「Experience Manager資產」製作例項中。 當您發佈資產時，其PTIFF轉譯也會發佈至Brand Portal。

>[!NOTE]
>
>下載影像及其轉譯時，沒有選項可從現有的預設集中選擇。 您可以改為指定自訂影像預設集的屬性。 如需詳細資訊，請參閱下載影像時套用影像預設集](../using/brand-portal-image-presets.md#main-pars-text-1403412644) 。[


有關建立影像預設集時所需參數的詳細資訊，請參閱[管理影像預設集](../using/brand-portal-image-presets.md)。

## 建立影像預設集 {#create-an-image-preset}

Experience Manager資產管理員可以建立影像預設集，這些預設集在資產詳細資料頁面上顯示為動態轉譯。 您可以從草稿開始建立影像預設集，或以新名稱儲存現有的預設集。 建立影像預設集時，請選擇影像傳送的大小和格式命令。 當傳送影像以供檢視時，其外觀根據所選命令而最佳化。

>[!NOTE]
>
>使用影像的金字塔TIFF建立影像的動態轉譯。 如果金字塔TIFF無法用於任何資產，則無法在Brand Portal中擷取該資產的動態轉譯。
>
>如果「Experience Manager資產」製作例項在&#x200B;**Dynamic Media混合模式**&#x200B;上執行，則會建立影像資產的金字塔TIFF轉譯並儲存在「Experience Manager資產」存放庫中。
>
>然而，如果「Experience Manager資產」製作例項在&#x200B;**Dynamic Media場景7模式**&#x200B;上執行，則「場景7」伺服器上存在影像資產的金字塔TIFF轉譯。
>
>將這些資產發佈至brand portal時，會套用影像預設集並顯示動態轉譯。


1. 在頂端的工具列中，按一下Experience Manager標誌以存取管理工具。

1. 在管理工具面板中，按一下「影像預設集」]**。**[!UICONTROL 

   ![](assets/admin-tools-panel-4.png)

1. 在影像預設集頁面中，按一下「**[!UICONTROL 建立]**」。

   ![](assets/image_preset_homepage.png)

1. 在&#x200B;**[!UICONTROL 編輯影像預設集]**&#x200B;頁中，根據需要在&#x200B;**[!UICONTROL Basic]**&#x200B;和&#x200B;**[!UICONTROL Advanced]**&#x200B;標籤中輸入值，包括名稱。 預設集會出現在左窗格中，並可與其他資產一起即時使用。

   ![](assets/image_preset_create.png)

   >[!NOTE]
   >
   >您也可以使用「**[!UICONTROL 編輯影像預設集]**」頁面來編輯現有影像預設集的屬性。 若要編輯影像預設集，請從影像預設集頁面中選取該影像預設集，然後按一下「編輯」****。

1. 按一下「**[!UICONTROL 儲存]**」。影像預設集會建立並顯示在影像預設集頁面上。
1. 若要刪除影像預設集，請從影像預設集頁面中選取該影像預設集，然後按一下&#x200B;**[!UICONTROL Delete]**。 在確認頁面中，按一下&#x200B;**[!UICONTROL Delete]**&#x200B;以確認刪除。 影像預設集將從影像預設集頁面中移除。

## 預覽影像時套用影像預設集  {#apply-image-presets-when-previewing-images}

預覽影像及其轉譯時，從現有預設集中選擇，以將影像重新格式化為管理員設定的規格。

1. 在Brand Portal介面中，按一下影像以開啟。
1. 按一下左側的覆蓋圖示，然後選擇&#x200B;**[!UICONTROL 轉譯]**。

   ![](assets/image-preset-previewrenditions.png)

1. 從&#x200B;**[!UICONTROL 轉譯]**&#x200B;清單中，選取適當的動態轉譯，例如&#x200B;**[!UICONTROL 縮圖]**。 預覽影像會根據您選擇的轉譯來呈現。

   ![](assets/image-preset-previewrenditionthumbnail.png)

## 下載影像時套用影像預設集 {#apply-image-presets-when-downloading-images}

從Brand Portal下載影像及其轉譯時，無法從現有的影像預設集中選擇。 不過，您可以根據要重新格式化影像的屬性來自訂影像預設集屬性。

1. 從Brand Portal介面，執行下列其中一項操作：

   * 將指標暫留在您要下載的影像上。 從可用的快速操作縮圖中，按一下&#x200B;**[!UICONTROL Download]**&#x200B;表徵圖。

   ![](assets/downloadsingleasset.png)

   * 選取您要下載的影像。 從頂端的工具列按一下&#x200B;**[!UICONTROL Download]**&#x200B;圖示。

   ![](assets/downloadassets.png)

1. 在&#x200B;**[!UICONTROL 下載]**&#x200B;對話方塊中，根據您要下載包含或不包含其轉譯的資產，選取所需選項。

   ![](assets/donload-assets-dialog.png)

1. 若要下載資產的動態轉譯，請選取「**[!UICONTROL 動態轉譯」]**&#x200B;選項。
1. 根據您要在下載期間動態重新格式化影像及其轉譯的影像預設集屬性，自訂影像預設集屬性。 指定大小、格式、顏色空間、解析度和影像修飾符。

   ![](assets/dynamicrenditions.png)

1. 按一下「**[!UICONTROL 下載]**」。 自訂動態轉譯會以ZIP檔案下載，並附上您選擇下載的影像和轉譯。 不過，如果下載了單一資產，則不會建立任何zip檔案，如此可確保快速下載。
