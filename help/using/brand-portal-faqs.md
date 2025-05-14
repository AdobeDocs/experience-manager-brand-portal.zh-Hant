---
title: 常見問題
description: 深入了解 Adobe Experience Manager Assets Brand Portal 的常見問題。
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: frequently-asked-questions
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
exl-id: 4a8f7fbd-7485-421d-a8db-755324d2dbef
source-git-commit: 32a67abf466dd3bf635b851b02377ed23591915e
workflow-type: ht
source-wordcount: '1500'
ht-degree: 100%

---

# 常見問題 {#frequently-asked-questions}

Brand Portal 常見問題著重於一般使用者在使用最新的 Experience Manager Assets Brand Portal 6.4.6 版本或更早版本時提出的查詢和可能遇到的問題。


## Brand Portal 6.4.6 常見問題 {#faqs-bp646}

**問題：現有的舊版 OAuth 端點 (`https://legacy-oauth.cloud.adobe.io/login`) 無法作用。可能的原因是什麼？**

**回答：**&#x200B;舊版 OAuth 設定已棄用。將 Experience Manager Assets 作者實例升級到最新 Service Pack，並透過 Adobe Developer Console 進行設定。詳細資訊請參閱[設定 Experience Manager Assets 與 Brand Portal 搭配使用](configure-aem-assets-with-brand-portal.md)。不過，為了讓舊版 OAuth 設定在升級之前能夠正常運作，請將舊版 OAuth 端點更新為 `https://hypnosisprod.ethos11-prod-or1.ethos.adobe.net/`。

**問題：升級到 Adobe Developer Console 後，我無法將貢獻資料夾的資產從 Brand Portal 發佈至 Experience Manager Assets。我的作者實例在 Experience Manager Assets 6.5.4 上。可能的原因是什麼？**

**回答：**&#x200B;是的，透過 Adobe Developer Console 將貢獻資料夾的資產發佈至 Experience Manager Assets 6.5.4 存在一個已知問題。

此問題已在 Experience Manager Assets 6.5.5 中修正。您可以將 Experience Manager Assets 執行個體升級到最新 Service Pack，並在 Adobe Developer Console 上[升級您的設定](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal#upgrade-integration-65)。


**問題：我在 Experience Manager Assets 中沒有看到從 Brand Portal 發佈的貢獻資料夾內容。可能的原因是什麼？**

**回答：**&#x200B;請聯絡您的 Experience Manager Assets 管理員以驗證設定，並確保您的 Brand Portal 租用戶僅設定一個 Experience Manager Assets 作者實例。

當您在多個 Experience Manager Assets 作者實例上設定 Brand Portal 租用戶時，可能會發生此問題。例如，管理員在中繼和生產環境的 Experience Manager Assets 作者實例上設定相同的 Brand Portal 租用戶。在這種情況下，雖會在 Brand Portal 中觸發資產發佈，但 Experience Manager Assets 作者實例無法匯入資產，因為複寫代理程式並未收到請求權杖。


**問題：我無法將資產從 Experience Manager Assets 發佈至 Brand Portal。複寫記錄顯示連線逾時。有快速修正的方法嗎？**

**回答：**&#x200B;如果複寫佇列中有多個待處理的請求，發佈通常會失敗並出現逾時錯誤。若要解決此問題，請確保複寫代理程式已設定為避免逾時。

執行下列步驟來設定複寫代理程式：

1. 登入您的 Experience Manager Assets 作者實例。
1. 從「**工具**」面板，導覽至「**[!UICONTROL 部署]** > **[!UICONTROL 複寫]**」。
1. 在「複寫」頁面中，按一下「**[!UICONTROL `Agents on author`]**」。您可以看到 Brand Portal 租用戶的四個複寫代理程式。
1. 按一下複寫代理程式 URL，開啟代理程式詳細資料。
1. 按一下「**[!UICONTROL 編輯]**」，編輯複寫代理程式設定。
1. 在代理程式設定中，按一下「**[!UICONTROL 擴充]**」索引標籤。
1. 選取「**[!UICONTROL 關閉連線]**」核取方塊。
1. 重複步驟 4 到 7，設定所有四個複寫代理程式。
1. 重新啟動伺服器並驗證連線。


## Brand Portal 6.4.5 常見問題 {#faqs-bp645}

**問題：Brand Portal 6.4.5 版本的主要變更是什麼？**

**回答：** Experience Manager Assets Brand Portal 6.4.5 讓使用者能夠直接從 Brand Portal 上傳內容，並將貢獻資料夾發佈回 Experience Manager Assets 中，而無需管理員權限。如需詳細資訊，請參閱 [Brand Portal 中的資產來源](brand-portal-asset-sourcing.md)。



**問題：我是否無法再存取我所建立的任何現有資產、功能或設定？**

**回答：**&#x200B;您所有現有的功能和設定均維持不變。您的一般使用者不會受到影響，並且您的內容保持完整。



**問題：我什麼時候可以移轉到新版本的 Brand Portal？**

**回答：**Brand Portal 6.4.5 於 2019 年 10 月發佈到生產環境。下一個 Brand Portal 版本預計將於 2020 年 3 月發佈。
關於更新和版本變更，Adobe 建議您追蹤[發行說明](brand-portal-release-notes.md)和 [Brand Portal 新增功能](whats-new.md)。



**問題：我的使用者會受到影響嗎？**

**回答：** Brand Portal 6.4.5 版本僅在 Brand Portal 內部發佈，因此不會對您的一般使用者產生影響。



**問題：做為 Brand Portal 使用者，我需要採取什麼動作嗎？**

**回答：** Brand Portal 6.4.5 版本具有一項名為「資產來源」的新功能。管理員必須在 Experience Manager Assets 中設定資產來源功能，才能為 Brand Portal 使用者啟用該功能。如需詳細資訊，請參閱[啟用資產來源](brand-portal-asset-sourcing.md)。



**問題：誰可以建立貢獻資料夾？**

**回答：**&#x200B;任何有權在 Experience Manager Assets 中建立資料夾的 Experience Manager Assets 使用者，都可以建立「**貢獻**」資料夾。若要建立「**貢獻**」資料夾，請建立類型為「**資產貢獻**」的資料夾。
此資料夾會與使用中的 Brand Portal 使用者共用，以便進行貢獻。



**問題：「貢獻」資料夾內包含什麼？**

**回答：**「**貢獻**」資料夾包含兩個子資料夾，「**NEW**」和「**SHARED**」。最初，「NEW」資料夾是空白的，而「SHARED」資料夾包含提供予 Brand Portal 使用者的參考內容 (可重複使用的資產)。
Brand Portal 使用者可以存取「**貢獻**」資料夾，並上傳內容到「**NEW**」資料夾。



**問題：我可以修改現有「貢獻」資料夾的名稱嗎？**

**回答：****不可以**，您不能修改現有「**貢獻**」資料夾的名稱。



**問題：相對於貢獻，資產要求是什麼？**

**回答：**「**貢獻**」資料夾內的&#x200B;**簡介**&#x200B;文件和「**SHARED**」資料夾內的參考內容，可以協助 Brand Portal 使用者了解貢獻需求和期望。兩者統稱為資產要求。

**問題：我可以將資產上傳到任何允許的資料夾嗎？**

**回答：**&#x200B;並非所有允許的資料夾都可以。Brand Portal 使用者只能將內容上傳到 Experience Manager Assets 或 Brand Portal 管理員共用的「**貢獻**」資料夾。



**問題：如何存取「貢獻」資料夾？**

**回答：**&#x200B;唯有「**貢獻**」資料夾與您共用時，您才能存取。每當有人與您共用「貢獻」資料夾時，您都會收到電子郵件/即時簡短通知。您可以透過電子郵件中共用的連結存取「貢獻」資料夾。或者，您可以登入您的 Brand Portal 實例，並導覽至鈴鐺圖示以讀取通知，進而存取「貢獻」資料夾。

>[!NOTE]
>
>如果您不是 Brand Portal 使用者，需請求 Experience Manager Assets 管理員在 Admin Console 中建立您的使用者。然後，將您的基本資料新增至 Brand Portal 使用者清單中的使用者設定檔案中。


**問題：使用者匯入 CSV 檔案的格式是什麼？**

**回答：**&#x200B;此格式與 Admin Console 支援之大量使用者匯入格式相符。電子郵件、名字和姓氏為必填。



**問題：資產貢獻使用者下拉選單中的使用者清單 (Brand Portal 貢獻者) 會填入什麼？**

**回答：**&#x200B;下拉式選單中的使用者來自上傳至 Experience Manager Assets 的 Brand Portal 使用者設定 (.csv) 檔案。



**問題：在哪裡可以查看匯入和發佈工作的狀態？**

**回答：**&#x200B;在 Experience Manager Assets 中，您可以在&#x200B;**非同步**&#x200B;工作頁面看到匯入狀態。在 Brand Portal 中，您可以在「**[!UICONTROL 工具 > 資產貢獻狀態]**」查看發佈工作的狀態。



**問題：Experience Manager 中定期執行之匯入工作的頻率為何？**

**回答：**&#x200B;在 Experience Manager Assets 中，每五分鐘執行一次輪詢。



**問題：一個資料夾從 Brand Portal 發佈至 Experience Manager Assets 的次數是否有限制？**

**回答：**&#x200B;沒有，「**NEW**」資料夾的所有資產都會發佈至 Experience Manager Assets，無論其之前是否發佈過。每次「**貢獻**」資料夾從 Brand Portal 發佈至 Experience Manager Assets 後，便會取代「**NEW**」資料夾的內容。



**問題：如何在「貢獻」資料夾內上傳新資產？**

**回答：**&#x200B;請參閱[將資產上傳到「貢獻」資料夾](brand-portal-publish-contribution-folder-to-brand-portal.md)的詳細文件。



**問題：我無法看到上傳至「NEW」資料夾的資產之縮圖或預覽。**

**回答：**&#x200B;此為正常現象，因為在 Brand Portal 這一端沒有執行工作流程。



**問題：如果將一個資料夾從 Experience Manager Assets 發佈至 Brand Portal，但該資料夾持續變更，會發生什麼情況？**

**回答：**&#x200B;在 Experience Manager Assets 中，每次將資料夾發佈至 Brand Portal 時都會保留記錄。發佈時，所有未發佈至 Brand Portal 的資產都會加入到複寫佇列中。發佈工作觸發後新增至資料夾的任何資產，都不會發佈至 Brand Portal。當 Experience Manager Assets 使用者再次發佈資料夾時，只有先前未發佈的資產 (存在於複寫佇列中) 才會發佈至 Brand Portal。此程序適用於任何從 Experience Manager Assets 發佈至 Brand Portal 的資料夾，以及「貢獻」資料夾內的「SHARED」資料夾。

**問題：如果我有問題該聯絡誰？**

**回答：**&#x200B;請聯絡您的 Adobe 客戶經理或客戶支援。

>[!NOTE]
>
>發佈排程是暫定的，可能會有所變更。請聯絡您的 Adobe 客戶經理或客戶支援，取得更新的發佈排程。


## 產品存取和支援 (受限網站) {#product-access-and-support-restricted-sites}

這些網站僅適用於客戶。如果您是客戶並且需要存取權，請聯絡您的 Adobe 客戶經理。

<!--
* [](https://daycare.day.com) [Product Access](https://login.marketing.adobe.com)

* [Adobe Customer Support]()
-->
