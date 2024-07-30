---
title: 疑難排解平行發佈至Brand Portal的問題
description: 疑難排解平行發佈。
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
topic-tags: brand-portal
role: Admin
exl-id: 631beabc-b145-49ba-a8e4-f301497be6da
source-git-commit: ce3a7a5232f32c86b4930f9079bed5f04d001d8f
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 0%

---

# 疑難排解平行發佈至Brand Portal的問題 {#troubleshoot-issues-in-parallel-publishing-to-brand-portal}

Brand Portal已使用Experience Manager Assets設定，以核准從Experience Manager Assets製作例項無縫擷取（或發佈）品牌資產。 設定[後](../using/configure-aem-assets-with-brand-portal.md)，Experience Manager作者會使用復寫代理程式，將一或多個選取的資產復寫至Brand Portal雲端服務，以供Brand Portal使用者核准使用。 Experience Manager6.2 SP1-CFP5、Experience ManagerCFP 6.3.0.2及更高版本都使用多個復寫代理程式，以允許高速平行發佈。

>[!NOTE]
>
>為確保使用Experience Manager Assets成功設定Experience Manager Assets Brand Portal，Adobe建議升級至Experience Manager 6.4.1.0。Experience Manager 6.4的限制會在使用Brand Portal設定Experience Manager Assets時發生錯誤，且復寫失敗。

在&#x200B;**[!UICONTROL /etc/cloudservice]**&#x200B;下設定Brand Portal的雲端服務時，會自動產生所有必要的使用者和Token，並儲存在存放庫中。 雲端服務設定已建立，也建立了復寫和復寫內容復寫代理所需的服務使用者。 它會建立四個復寫代理。 因此，當您從Experience Manager發佈許多資產到Brand Portal時，資產會排入佇列，並透過循環配置資源在復寫代理程式之間分配。

不過，發佈可能會間歇性地失敗，原因包括：大型Sling工作、Experience Manager製作執行個體上的網路和&#x200B;**[!UICONTROL 磁碟I/O]**&#x200B;增加，或Experience Manager製作執行個體的效能降低。 Adobe建議您在開始發佈之前，先測試與一或多個復寫代理程式的連線。

![](assets/test-connection.png)

## 疑難排解首次發佈的失敗：驗證您的發佈設定 {#troubleshoot-failures-in-first-time-publishing-validating-your-publish-configuration}

若要驗證發佈設定：

1. 檢查錯誤記錄
1. 檢查是否已建立復寫代理
1. 測試連線

建立Cloud Service時有&#x200B;**尾記錄**

檢查尾部記錄。 檢查是否已建立復寫代理程式。 如果復寫代理程式建立失敗，請在雲端服務中進行微幅變更，以編輯雲端服務。 驗證並再次檢查復寫代理程式是否已建立。 如果沒有，請重新編輯服務。

如果重複編輯雲端服務時未正確設定，則報告Daycare票證。

**測試與復寫代理程式的連線**

檢視記錄檔（如果在復寫記錄檔中發現錯誤）：

1. 請聯絡客戶支援。

1. 重試[清理](../using/troubleshoot-parallel-publishing.md#clean-up-existing-config)，然後再次建立發佈設定。

<!--
Comment Type: remark
Last Modified By: Mini Gulati (mgulati)
Last Modified Date: 2018-06-21T22:56:21.256-0400
<p>?? check and compare public key. At times public key is different</p>
<p>?? another thing to check in /useradmin</p>
-->

## 清除現有的Brand Portal發佈設定 {#clean-up-existing-config}

發佈經常會因「401未獲授權」錯誤而失敗，因為使用者（例如`mac-<tenantid>-replication`）缺少最新的私密金鑰，而且復寫代理程式記錄檔中未回報任何其他錯誤。 您可能希望避免進行疑難排解，而改為建立設定。 為了讓新設定正常運作，請從Experience Manager作者設定中清理下列專案：

1. 移至`localhost:4502/crx/de/` （考慮您正在`localhost:4502:`上執行作者執行個體）
i.刪除`/etc/replication/agents.author/mp_replication`
二、 刪除`/etc/cloudservices/mediaportal/<config_name>`

1. 移至localhost：4502/useradmin：\
   i.搜尋使用者`mac-<tenantid>replication`
二、 刪除此使用者

現在系統已全部清除。 現在，您可以嘗試建立雲端服務設定，同時仍使用現有的JWT應用程式。 不需要建立應用程式，而是從新建立的雲端設定更新公開金鑰。

>[!NOTE]
>
>請勿修改任何自動產生的設定。


## Developer Connection JWT應用程式租使用者可見性問題 {#developer-connection-jwt-application-tenant-visibility-issue}

如果位於`https://legacy-oauth.cloud.adobe.io/`，則會列出目前使用者擁有系統管理員的所有組織（租使用者）。 如果您在這裡找不到組織名稱，或是您在這裡無法為必要的租使用者建立應用程式，請檢查您是否有足夠的（系統管理員）許可權。

此使用者介面有一個已知問題，即對於任何租使用者而言，只會顯示前十個應用程式。 建立應用程式時，請停留在頁面上並將URL加入書籤。 請勿移至應用程式的清單頁面，並尋找您建立的應用程式。 您可以直接點選此建立書籤的URL，並視需要更新或刪除應用程式。

JWT應用程式可能未正確列出。 因此，建議您在建立JWT應用程式時記下URL或將它加入書籤。

## 執行組態停止運作 {#running-configuration-stops-working}

<!--
Comment Type: draft

<p>If the running configuration stops working, either of the following two possibilities
<g class="gr_ gr_15 gr-alert gr_gramm gr_inline_cards gr_run_anim Grammar multiReplace" data-gr-id="15" id="15" style="font-size: 12px;">
are
</g> there:</p>
<p>1.
<g class="gr_ gr_14 gr-alert gr_gramm gr_inline_cards gr_run_anim Grammar only-ins doubleReplace replaceWithoutSep" data-gr-id="14" id="14">
Connection
</g> has failed, or</p>
<p>2. Publish has failed with permission to dam-replication-service denied, while connection has passed </p>
<p>If the connection has failed [1], the
<g class="gr_ gr_10 gr-alert gr_spell gr_inline_cards gr_run_anim ContextualSpelling ins-del multiReplace" data-gr-id="10" id="10">
fail safe
</g> way to fix it is to <a href="../using/troubleshoot-parallel-publishing.md#main-pars-header-1664955658">clean up</a> the existing Brand Portal publish configuration and recreate a publish configuration. </p>
<p>However, if the
<g class="gr_ gr_18 gr-alert gr_spell gr_inline_cards gr_run_anim ContextualSpelling" data-gr-id="18" id="18">
publish
</g> has failed with
<g class="gr_ gr_16 gr-alert gr_gramm gr_inline_cards gr_run_anim Grammar only-ins doubleReplace replaceWithoutSep" data-gr-id="16" id="16">
permission
</g> denied to dam-replication-service, raise a support ticket.</p>
-->

如果復寫代理程式(原本可順利發佈至Brand Portal)停止處理發佈工作，請檢查復寫記錄。 Experience Manager內建自動重試功能，因此如果特定資產發佈失敗，則會自動重試。 如果發生網路錯誤等間歇性問題，重試時可能會成功。

如果連續發佈失敗，且佇列被封鎖，請檢查&#x200B;**[!UICONTROL 測試連線]**。 嘗試解決正在報告的錯誤。

根據錯誤，建議您記錄支援票證，以便Brand Portal工程團隊可以幫助您解決問題。

## Brand Portal IMS設定權杖已到期 {#token-expired}

如果您的Brand Portal環境突然停止，IMS設定可能會無法正常運作。 系統會顯示不正常的IMS設定，並反映您的存取權杖已過期的錯誤訊息（類似以下內容）。

`com.adobe.granite.auth.oauth.AccessTokenProvider failed to get access token from authorization server status: 400 response: Unknown macro: {"error"}`

若要解決此問題，Adobe建議您手動儲存並關閉IMS設定，然後再次檢查健全狀態。 如果組態無法運作，請刪除現有組態並建立新組態。


## 設定復寫代理以避免連線逾時錯誤 {#connection-timeout}

如果復寫佇列中有多個擱置中的要求，發佈作業通常會因逾時錯誤而失敗。 若要解決此問題，請確保復寫代理已設定為避免逾時。

設定復寫代理程式：

1. 登入您的AEM Assets作者執行個體。
1. 從&#x200B;**工具**&#x200B;面板，瀏覽至&#x200B;**[!UICONTROL 部署]** > **[!UICONTROL 復寫]**。
1. 在[復寫]頁面中，按一下&#x200B;**[!UICONTROL `Agents on author`]**。 您可以看到Brand Portal租使用者的四個復寫代理。
1. 按一下復寫代理程式URL，然後按一下&#x200B;**[!UICONTROL 編輯]**。
1. 在[代理程式設定]中，按一下[**[!UICONTROL 延伸]**]索引標籤。
1. 選取&#x200B;**[!UICONTROL 關閉連線]**&#x200B;核取方塊。
1. 重複步驟4到7，設定所有四個復寫代理程式。
1. 重新啟動伺服器。
