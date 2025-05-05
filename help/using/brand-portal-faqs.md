---
title: 常見問題
description: 深入瞭解Adobe Experience Manager Assets Brand Portal的常見問題集。
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: frequently-asked-questions
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
exl-id: 4a8f7fbd-7485-421d-a8db-755324d2dbef
source-git-commit: 32a67abf466dd3bf635b851b02377ed23591915e
workflow-type: tm+mt
source-wordcount: '1500'
ht-degree: 0%

---

# 常見問題 {#frequently-asked-questions}

Brand Portal常見問題集專注於使用者在使用最新Experience Manager Assets Brand Portal 6.4.6版本或更早版本時可能會遇到的查詢和問題。


## Brand Portal 6.4.6常見問題集 {#faqs-bp646}

**問題：現有的舊版OAuth端點(`https://legacy-oauth.cloud.adobe.io/login`)無法運作。 可能的原因是什麼？**

**答案：**&#x200B;已棄用舊版OAuth設定。 將Experience Manager Assets編寫執行個體升級至最新的Service Pack，並透過Adobe Developer Console進行設定。 如需詳細資訊，請參閱[使用Brand Portal設定Experience Manager Assets](configure-aem-assets-with-brand-portal.md)。 不過，若要讓舊版OAuth設定在升級前繼續運作，請將舊版OAuth端點更新為`https://hypnosisprod.ethos11-prod-or1.ethos.adobe.net/`。

**問題：升級至Adobe Developer Console後，我無法將貢獻資料夾中的資產從Brand Portal發佈至Experience Manager Assets。 我的編寫執行個體在Experience Manager Assets 6.5.4上。可能的原因是什麼？**

**答案：**&#x200B;是，透過Adobe Developer Console將貢獻資料夾的資產發佈至Experience Manager Assets 6.5.4時，出現已知問題。

Experience Manager Assets 6.5.5已修正此問題。您可以將您的Experience Manager Assets執行個體升級至最新的Service Pack，並在Adobe Developer Console上[升級您的設定](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal#upgrade-integration-65)。


**問題：我在Experience Manager Assets中看不到從Brand Portal發佈的貢獻資料夾內容。 可能的原因是什麼？**

**回答：**&#x200B;請連絡您的Experience Manager Assets管理員以驗證設定，並確定您的Brand Portal租使用者只設定了一個Experience Manager Assets作者執行個體。

當您在多個Brand Portal作者執行個體上設定Experience Manager Assets租使用者時，可能會發生此問題。 例如，管理員會在預備和生產環境的Brand Portal製作例項上設定相同的Experience Manager Assets租使用者。 在這種情況下，資產發佈會在Brand Portal中觸發，但Experience Manager Assets製作例項無法匯入資產，因為復寫代理程式未收到請求權杖。


**問題：我無法從Experience Manager Assets發佈資產到Brand Portal。 復寫記錄檔指出連線逾時。 有快速修正嗎？**

**回答：**&#x200B;如果復寫佇列中有多個擱置的要求，則發佈通常會因逾時錯誤而失敗。 若要解決此問題，請確保復寫代理已設定為避免逾時。

執行以下步驟來設定復寫代理程式：

1. 登入您的Experience Manager Assets作者執行個體。
1. 從&#x200B;**工具**&#x200B;面板，瀏覽至&#x200B;**[!UICONTROL 部署]** > **[!UICONTROL 復寫]**。
1. 在[復寫]頁面中，按一下&#x200B;**[!UICONTROL `Agents on author`]**。 您可以看到您的Brand Portal租使用者的四個復寫代理。
1. 按一下復寫代理程式URL以開啟代理程式詳細資訊。
1. 按一下&#x200B;**[!UICONTROL 編輯]**&#x200B;以編輯復寫代理程式設定。
1. 在代理程式設定中，按一下&#x200B;**[!UICONTROL 延伸]**&#x200B;索引標籤。
1. 選取&#x200B;**[!UICONTROL 關閉連線]**&#x200B;核取方塊。
1. 重複步驟4到7，設定所有四個復寫代理程式。
1. 重新啟動伺服器並驗證連線。


## Brand Portal 6.4.5常見問題集 {#faqs-bp645}

**問題： Brand Portal 6.4.5版有哪些主要變更？**

**答案：** Experience Manager Assets Brand Portal 6.4.5可讓使用者上傳內容，並直接從Brand Portal將「貢獻」資料夾發佈回Experience Manager Assets，不需要系統管理員許可權。 如需詳細資訊，請參閱[Brand Portal中的Asset Sourcing ](brand-portal-asset-sourcing.md)。



**問題：我是否無法存取任何我已建立的現有資產、功能或設定？**

**回答：**&#x200B;您所有現有的功能和設定都會維持不變。 您的使用者不受影響，內容保持不變。



**問題：何時要移至新版Brand Portal？**

**答案：** Brand Portal 6.4.5已於2019年10月發佈至生產環境。 下一版Brand Portal預計於2020年3月推出。
如需更新和版本變更，Adobe建議您追蹤[發行說明](brand-portal-release-notes.md)和[Brand Portal的新功能](whats-new.md)。



**問題：我的使用者是否會受到影響？**

**回答：** Brand Portal 6.4.5版本僅在Brand Portal中提供，因此不會影響您的一般使用者。



**問題：我身為Brand Portal使用者是否需要任何動作？**

**回答：** Brand Portal 6.4.5版本隨附名為Asset Sourcing的新功能。 管理員必須在Experience Manager Assets中設定Asset Sourcing功能，才能為Brand Portal使用者啟用此功能。 如需詳細資訊，請參閱[啟用資產來源](brand-portal-asset-sourcing.md)。



**問題：誰可以建立「貢獻」資料夾？**

**回答：**&#x200B;任何有權在Experience Manager Assets中建立資料夾的Experience Manager Assets使用者都可以建立&#x200B;**貢獻**&#x200B;資料夾。 若要建立&#x200B;**貢獻**&#x200B;資料夾，請建立&#x200B;**資產貢獻**&#x200B;型別的資料夾。
此資料夾會與作用中的Brand Portal使用者共用，以獲得貢獻。



**問題：「貢獻」資料夾包含什麼？**

**答案：** **貢獻**&#x200B;資料夾包含兩個子資料夾&#x200B;**NEW**&#x200B;和&#x200B;**SHARED**。 最初，NEW資料夾是空白的，而SHARED資料夾則包含Brand Portal使用者的參考內容（可重複使用的資產）。
Brand Portal使用者存取&#x200B;**貢獻**&#x200B;資料夾，並上傳&#x200B;**新增**&#x200B;資料夾的內容。



**問題：我可以修改現有「貢獻」資料夾的名稱嗎？**

**答案：** **否**，您無法修改現有&#x200B;**貢獻**&#x200B;資料夾的名稱。



**問題： w.r.t.貢獻的資產需求為何？**

**回答：** **貢獻**&#x200B;資料夾中的&#x200B;**簡介**&#x200B;檔案與&#x200B;**共用**&#x200B;資料夾中的參考內容可協助Brand Portal使用者瞭解貢獻需求和期望。 這些需求統稱為資產需求。

**問題：我可以將資產上傳到任何允許的資料夾嗎？**

**回答：**&#x200B;並非所有允許的資料夾。 Brand Portal使用者只能將內容上傳到Experience Manager Assets或Brand Portal管理員共用的&#x200B;**貢獻**&#x200B;資料夾。



**問題：如何取得貢獻資料夾的存取權？**

**回答：**&#x200B;您必須先與您共用&#x200B;**貢獻**&#x200B;資料夾，才能加以存取。 每當「貢獻」資料夾與您共用時，您都會收到電子郵件/脈衝通知。 您可以透過電子郵件中分享的連結來存取「貢獻」資料夾。 或者，您可以登入Brand Portal執行個體，並導覽至鈴鐺圖示，即可存取「貢獻」資料夾。

>[!NOTE]
>
>如果您不是Brand Portal使用者，請要求Experience Manager Assets管理員在Admin Console中建立您的使用者。 然後，將您的設定檔新增到Brand Portal使用者清單中的使用者設定檔。


**問題：使用者匯入的CSV檔案格式為何？**

**回答：**&#x200B;格式符合大量使用者匯入所支援的Admin Console。 電子郵件、名字和姓氏為必填欄位。



**問題：什麼會填入「資產貢獻」使用者下拉式清單中的使用者(Brand Portal貢獻者)清單？**

**回答：**&#x200B;下拉式清單中的使用者是從Experience Manager Assets中上傳的Brand Portal使用者設定(.csv)檔案填入的。



**問題：我可以在哪裡檢視匯入和發佈工作的狀態？**

**回答：**&#x200B;在Experience Manager Assets中，您可以在&#x200B;**非同步**&#x200B;工作頁面中看到匯入的狀態。 在Brand Portal中，您可以在&#x200B;**[!UICONTROL 工具>資產貢獻狀態]**&#x200B;中檢視發佈工作的狀態。



**問題：在Experience Manager中定期執行的匯入工作的頻率為何？**

**回答：**&#x200B;在Experience Manager Assets中，每五分鐘會執行輪詢。



**問題：資料夾從Brand Portal發佈至Experience Manager Assets的次數是否有臨界值？**

**回答：**&#x200B;否，**NEW**&#x200B;資料夾中的所有資產皆已發佈至Experience Manager Assets，無論這些資產先前是否發佈。 每次從Brand Portal將&#x200B;**貢獻**&#x200B;資料夾發佈到Experience Manager Assets時，都會取代&#x200B;**NEW**&#x200B;資料夾的內容。



**問題：如何在「貢獻」資料夾中上傳新資產？**

**答案：**&#x200B;請參閱有關[將資產上傳至「貢獻」資料夾](brand-portal-publish-contribution-folder-to-brand-portal.md)的詳細檔案。



**問題：我看不到上傳至NEW資料夾之資產的縮圖或預覽。**

**回答：**&#x200B;設計如常，因為沒有工作流程在Brand Portal端執行。



**問題：如果將資料夾從Experience Manager Assets發佈到變動中的Brand Portal，會發生什麼情況？**

**答案：**&#x200B;在Experience Manager Assets中，每次將資料夾發佈到Brand Portal時都會維護記錄。 發佈時，所有未發佈至Brand Portal的資產都會新增至復寫佇列。 觸發發佈工作後新增至資料夾的任何資產都不會發佈至Brand Portal。 當Experience Manager Assets使用者再次發佈資料夾時，只有先前未發佈的資產（存在於復寫佇列中）會發佈至Brand Portal。 從Experience Manager Assets發佈至Brand Portal的任何資料夾，以及「貢獻」資料夾內的「共用」資料夾，都會執行此程式。

**問題：我要聯絡誰來提出問題？**

**回答：**&#x200B;請連絡您的Adobe客戶經理或客戶支援。

>[!NOTE]
>
>發行排程為暫定，可能會有變動。 請聯絡您的Adobe客戶經理或客戶支援，以取得更新的發行排程。


## 產品存取與支援（受限制的網站） {#product-access-and-support-restricted-sites}

這些網站僅供客戶使用。 如果您是客戶且需要存取權，請聯絡您的Adobe客戶經理。

<!--
* [](https://daycare.day.com) [Product Access](https://login.marketing.adobe.com)

* [Adobe Customer Support]()
-->
