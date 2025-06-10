---
title: 設定 Experience Manager Assets 以便與 Brand Portal 搭配使用
description: 透過insight使用Brand Portal設定Experience Manager Assets。
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
role: Admin
exl-id: 261c0e84-6b3d-459c-b6b9-a9af106d6943
source-git-commit: f4add370fd3242f5506e5cc4d921362e2b14141a
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 18%

---

# 設定 Experience Manager Assets 以便與 Brand Portal 搭配使用 {#configure-integration}

使用Brand Portal設定Adobe Experience Manager Assets可為Brand Portal使用者啟用資產發佈、資產發佈和資產貢獻功能。 它可讓Experience Manager Assets使用者與Brand Portal使用者一起發佈和發佈資產。 Brand Portal使用者可以存取共用資產，並透過將新資產上傳至資產貢獻資料夾並將其發佈回Experience Manager Assets來貢獻資產。

支援使用Brand Portal設定Experience Manager Assets的平台：

* Experience Manager Assets as a Cloud Service
* Experience Manager Assets （內部部署和託管服務） 6.5和更高版本

Experience Manager Assets as a Cloud Service是透過Cloud Manager啟用Brand Portal來自動設定的Brand Portal。 啟動工作流程會在後端建立所需的設定，並在與Experience Manager Assets as a Cloud Service執行個體相同的IMS組織上啟動Brand Portal。

而Experience Manager Assets （內部部署和託管服務）是使用Adobe Developer Console以Brand Portal手動設定，這會取得Adobe Identity Management Services (IMS) Token以授權Brand Portal租使用者。

>[!NOTE]
>
>***適用於Experience Manager Assets、6.5及更高版本***
>
>之前，Classic介面是使用舊版OAuth閘道設定Brand Portal，該閘道採用JSON網頁權杖(JWT)交換來取得IMS權杖以授權。
>
>自2020年4月6日起，已不再支援透過舊版OAuth進行設定，而會變更為透過Adobe Developer Console進行設定。


>[!TIP]
>
>***僅針對現有客戶（內部部署和受管理的服務）***
>
>舊版OAuth閘道設定仍適用於現有客戶。
>
>如果您遇到舊版OAuth閘道設定問題，請刪除現有設定，並透過Adobe Developer Console建立新設定。

設定 AEM Assets 與 Brand Portal 搭配使用的步驟因 AEM 版本而異，也會因為您是首次設定或是升級現有設定而不同：

| **AEM 版本** | **新設定** | **升級設定** |
|---|---|---|
| **AEM Assets as a Cloud Service** | [啟動Brand Portal](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/assets/brand-portal/configure-aem-assets-with-brand-portal) | - |
| **AEM 6.5 (6.5.4.0 及更高版本)** | [建立設定](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal) | [升級設定](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal#upgrade-integration-65) |
