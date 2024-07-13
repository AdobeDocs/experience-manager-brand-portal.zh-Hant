---
title: 使用Brand Portal設定Experience Manager Assets
seo-title: Configure Experience Manager Assets with Brand Portal
description: 深入瞭解如何使用Brand Portal設定Experience Manager Assets。
seo-description: Get an insight into configuring Experience Manager Assets with Brand Portal.
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
role: Admin
exl-id: 261c0e84-6b3d-459c-b6b9-a9af106d6943
source-git-commit: 454b05c05359a2068cc29124f826d5bd25a1bad1
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 2%

---

# 使用Brand Portal設定Experience Manager Assets {#configure-integration}

使用Brand Portal設定Adobe Experience Manager Assets可為Brand Portal使用者啟用資產發佈、資產發佈和資產貢獻功能。 它可讓Experience Manager Assets使用者與Brand Portal使用者一起發佈和發佈資產。 Brand Portal使用者可以存取共用資產，並透過將新資產上傳至資產貢獻資料夾並將其發佈回Experience Manager Assets來貢獻資產。

支援使用Brand Portal設定Experience Manager Assets的平台：

* Experience Manager Assetsas a Cloud Service
* Experience Manager Assets （內部部署和託管服務） 6.5和更高版本

從Cloud Manager啟用Experience Manager Assets，便會自動使用Brand Portal設定Brand Portal as a Cloud Service。 啟動工作流程會在後端建立所需的設定，並在與Experience Manager Assetsas a Cloud Service執行個體相同的IMS組織上啟動Brand Portal。

然而，Experience Manager Assets （內部部署和託管服務）是使用Adobe Developer Console以Brand Portal手動設定，這會取得AdobeIdentity Management Services (IMS) Token以授權Brand Portal租使用者。

>[!NOTE]
>
>適用於Experience Manager Assets 6.5及更高版本的&#x200B;******
>
>之前，Brand Portal是透過舊版OAuth閘道在傳統介面中設定，該介面使用JSON Web權杖(JWT)交換取得IMS權杖以授權。
>
>自2020年4月6日起，不再支援透過舊版OAuth進行設定，而改為透過Adobe Developer Console進行設定。


>[!TIP]
>
>***僅針對現有客戶（內部部署和受管理的服務）***
>
>舊版OAuth閘道設定將繼續適用於現有客戶。
>
>如果您遇到舊版OAuth閘道設定問題，請刪除現有設定，並透過Adobe Developer Console建立新設定。

使用Brand Portal設定AEM Assets的步驟因您的AEM版本，以及您是第一次設定還是升級現有設定而異：

| **AEM版本** | **新組態** | **升級組態** |
|---|---|---|
| **AEM Assets as a Cloud Service** | [啟動Brand Portal](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html) | - |
| **AEM 6.5 （6.5.4.0和更新版本）** | [建立設定](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html) | [升級組態](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65) |
