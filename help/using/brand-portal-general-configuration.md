---
title: 管理一般租使用者組態
description: 設定加速下載、建立公開智慧型集合、建立公開集合，以及讓管理員使用者刪除租使用者上的資產。
contentOwner: mgulati
topic-tags: administration
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
role: Admin
exl-id: 5607be8e-0a7f-4692-b71b-5f66eb9ac5ee
source-git-commit: 32a67abf466dd3bf635b851b02377ed23591915e
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# 管理一般租使用者組態 {#administer-general-tenant-configurations}

Experience Manager Assets Brand Portal可讓組織為特定租使用者設定下列功能：

* 管理員刪除資產
* 非管理員使用者建立的公開集合
* 非管理員使用者建立的公開智慧型集合
* 非管理員使用者可看見共用資料夾的父階層

這些設定已在管理工具面板中作為&#x200B;**[!UICONTROL 一般設定]**&#x200B;設定提供。

![](assets/general-config.png)

**A** — 可讓系統管理員從Brand Portal刪除資產的設定。 （預設為啟用）

**B** — 可讓非管理員使用者建立公開集合的設定。 （預設為啟用）

**C** — 可讓非管理員使用者建立公開智慧型集合的設定。 （預設為啟用）

**D** — 設定可顯示共用資料夾的資料夾階層（從根目錄）給非管理員使用者（編輯者、檢視者、訪客使用者）。 （預設為停用）

## 啟用或停用一般設定 {#enable-disable-general-configurations}

若要啟用或停用這些設定，請執行下列動作：

1. 以管理員許可權登入。
1. 選取Experience Manager標誌以從頂部的工具列存取管理工具。
1. 從系統管理工具面板，選取&#x200B;**[!UICONTROL 一般]**&#x200B;以開啟&#x200B;**[!UICONTROL 一般設定]**&#x200B;頁面。
1. 使用各自的切換開關來啟用或停用任何「一般」設定。
1. **[!UICONTROL 儲存]**&#x200B;變更。
1. 登出，變更即可生效。

## 允許管理員使用者從Brand Portal刪除資產 {#allow-admin-users-to-delete-assets-from-brand-portal}

**[!UICONTROL 允許使用者刪除]**&#x200B;設定可讓組織允許（或限制）具有管理員許可權的使用者從Brand Portal中刪除資產和資料夾。

## 允許非管理員建立公開集合 {#allow-public-collections-creation-by-non-admins}

[[!UICONTROL 允許建立公開集合]](../using/brand-portal-share-collection.md#main-pars-text-1915052376)組態控制非系統管理員是否可以在Brand Portal上建立公開集合。 此設定預設為啟用。 透過停用設定，組織可以防止在其入口網站上有許多公開集合，以便節省系統空間。

## 允許非管理員建立公開的智慧型集合 {#allow-public-smart-collections-creation-by-non-admins}

[[!UICONTROL 允許建立公開的智慧型集合]](../using/brand-portal-searching.md#main-pars-header-500620467)設定控制非系統管理員是否可以將搜尋儲存為智慧型集合，並為該租使用者公開。 此設定預設為啟用。 透過停用設定，組織可以避免非管理員使用者在組織的Brand Portal上建立大量公開的智慧型集合。

<!-- 
## Allow download acceleration {#allow-download-acceleration}

[[!UICONTROL Allow download acceleration]](../using/accelerated-download.md) configuration lets the organizations to allow accelerated downloads of assets from Brand Portal and shared links, by integrating with IBM Aspera Connect that is an install-on-demand application. The application uses proprietary technology to remove TCP overheads.
-->

## 啟用資料夾階層 {#enable-folder-hierarchy}

[[!UICONTROL 啟用資料夾階層]](../using/brand-portal-sharing-folders.md#non-admin-user-access-to-shared-folders)設定可讓管理員控制非管理員使用者（編輯者、檢視者和訪客使用者）在登入後檢視共用資料夾的方式。
