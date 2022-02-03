---
title: Speed up the Brand Portal downloads
seo-title: Speed up the Brand Portal downloads
description: Enhance download performance from Brand Portal and the shared links.
seo-description: Enhance download performance from Brand Portal and the shared links.
uuid: 2871137e-6471-49a7-872a-841bd92543d1
contentOwner: Vishabh Gupta
topic-tags: download-install, download assets
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: 301f7a0b-5527-4aac-b731-bfc145fed0c0
exl-id: cf28df58-c6dd-4b12-8279-01351892009f
source-git-commit: 63b7bdd34ff185a96ea69560d2b94c2dc04129de
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 2%

---

# Speed up the Brand Portal downloads {#guide-to-accelerate-downloads-from-brand-portal}

Adobe Experience Manager Assets Brand Portal allows enhancing the download performance of large asset files by integrating with IBM Aspera Connect, which is an install-on-demand application. The application uses proprietary technology to remove TCP overheads and helps improve transfer speed of the asset files. This integration ensures enhanced download experience.

>[!NOTE]
>
>Download speed varies for users as it depends upon factors such as network bandwidth, server latency, and geographical location of clients.

****

![](assets/download-settings-new.png)

## Prerequisites to accelerate file download {#prerequisites-to-accelerate-file-download}

To download the files faster, ensure the following:

* ****************
* Ensure that port 33001 (both TCP and UDP) is open on the firewall. [](https://downloads.asperasoft.com/en/documentation/8)
* ****`https://www.ibm.com/docs/en/aspera-connect/3.9.9`
* [](https://www.asperasoft.com/company/support/transfer-clients/)

>[!NOTE]
>
>There is a known issue with IBM Aspera Connect. Fast download does not work with IBM Aspera Connect version 3.10 and above.

## Download domains {#download-domains}

Following are the download domains for different geographies:

| Region Code | 網域 |
|---|---|
| NA OR1 | downloads-na1.brand-portal.adobe.com |
| NA VA5 | downloads-na2.brand-portal.adobe.com |
| EMEA LON5 | downloads-emea1.brand-portal.adobe.com |
| APAC SIN2 | downloads-apac1.brand-portal.adobe.com |

## Sample download performance using file accelerator {#expected-download-performance-using-file-accelerator}

The following table shows download performance for 2 GB file using Aspera Connect file download accelerator:

**

| Client location | Latency between client and server (milliseconds) | Speed with Aspera Connect File Transfer Accelerator (MBps) | Time taken to download 2 GB file with  Aspera File Transfer Accelerator (seconds) |
|---------------------------|-----------------------------------|---------------------------------------------|-------------------------------------------------------------------------|
| U.S. West (N. California) | 18 | 36 | 57 |
| U.S. West (Oregon) | 42 | 36 | 57 |
| U.S. East (N. Virginia) | 85 | 35 | 58 |
| APAC (Tokyo) | 124 | 36 | 57 |
| Noida (India) | 275 | 13.36 | 153 |
| Sydney | 175 | 29 | 70 |
| 倫敦 | 179 | 35 | 58 |
| 新加坡 | 196 | 34 | 60 |

## 下載資產 {#download-assets}

To download assets faster from Brand Portal:

1. Log in to your Brand Portal tenant. ****

   Do one of the following:

   * Select the assets or folders you want to download. ****

      ![](assets/select-assets-new.png)

   * ****

      ![](assets/select-asset.png)

1. ****

   ****

   The download button reflects the count of the selected items. ****[](../using/download-assets.md#download-assets)

   ![](assets/download-dialog-box-new.png)

1. ******** Therefore, a confirmation box appears to download assets using IBM Aspera Connect.

   `https://www.ibm.com/docs/en/aspera-connect/3.9.9`

   ![](assets/aspera-not-launched.png)

1. ****

   To install IBM Aspera Connect client setup, run the setup from  .msi  file of IBM Aspera Connect client application and follow the installation wizard.

   ![](assets/aspera-download-1.png)

1. Once the client is successfully installed, refresh the browser page and initiate the download steps again.

1. ******** All the selected renditions are downloaded in a zip folder using IBM Aspera Connect.

   On successful completion of the download, a dialog box shows the location where assets are downloaded onto the user&#39;s system.

   ![](assets/aspera-download-2.png)

   ************

>[!NOTE]
>
>****

<!-- 
On successful completion of the download, a dialog box shows the location where assets are downloaded onto the user's system. If there is a failure, it shows error.

   >[!NOTE]
   >
   >There is a known limitation in Aspera Connect client application that no prompt to select download location appears if **[!UICONTROL Always ask me where to save downloaded files]** is enabled under the tab **[!UICONTROL Transfers]** within **[!UICONTROL Preferences]**. Before any download begins, provide the location in the text box **[!UICONTROL Save downloaded files to]**.


1. Log in to Brand Portal using a supported browser.
1. Browse and select the folders or assets you want to download. From the toolbar at the top, click the **[!UICONTROL Download]** icon. the **[!UICONTROL Download]** dialog appears with the **[!UICONTROL Asset(s)]** and **[!UICONTROL Enable download acceleration]** check boxes selected by default. 

   ![](assets/download-assetsbp.png)

   >[!NOTE]
   >
   >The functionality to send email notification with the link to download assets is presently not supported while faster downloads are enabled.

   ![](assets/fast-download-emailchk.png)

1. Click **[!UICONTROL Download]**.

   To speed up the download experience on your Brand Portal tenant account, you need to have Aspera Connect client application installed in your browser's extension.

1. **Download Aspera Connect Client**

   If Aspera Connect client is not installed on your system or the existing Aspera Connect client is out of date, a prompt is displayed on the browser page from where you can download the system-specific Aspera Connect client by selecting **[!UICONTROL Download Latest Version]**.

   ![](assets/aspera-not-launched.png)

   To download the latest version of Aspera Connect from [https://downloads.asperasoft.com/connect2/](https://downloads.asperasoft.com/connect2/), select **[!UICONTROL Download Now]** and follow the instructions.

1. **Install Aspera Connect Client**

   To install IBM Aspera Connect client setup, run the setup from  .msi  file of IBM Aspera Connect client application and follow the installation wizard.

1. Once the client is successfully installed, refresh the browser page and initiate the download steps again.

   When using Aspera Connect for the first time, the browser prompts to open the link using **[!UICONTROL IBM Aspera Connect]**. To skip this dialog in future, enable **[!UICONTROL Remember my choice for FASP links]**.

   >[!NOTE]
   >
   >This message is different on the different browsers.

1. A dialog box confirms whether to proceed the transfer or not. Select **[!UICONTROL Allow]** to begin.
To skip this dialog in future, enable **[!UICONTROL Use my choice for all connections with this host]**.
Download begins. A dialog box shows the progress of the download. Use the dialog box to **[!UICONTROL pause]**, **[!UICONTROL resume]**, or **[!UICONTROL cancel]** the download.
Aspera Connect application provides an Activity Window on the system where user can view and manage all transfer sessions. For more information, refer [Aspera Connect Client documentation](https://downloads.asperasoft.com/en/documentation/8).

![](assets/aspera-activity-window.png)

On successful completion of the download, a dialog box shows the location where assets are downloaded onto the user's system. If there is a failure, it shows error.

   >[!NOTE]
   >
   >There is a known limitation in Aspera Connect client application that no prompt to select download location appears if **[!UICONTROL Always ask me where to save downloaded files]** is enabled under the tab **[!UICONTROL Transfers]** within **[!UICONTROL Preferences]**. Before any download begins, provide the location in the text box **[!UICONTROL Save downloaded files to]**.
-->

## Using file accelerator on Microsoft Edge browser {#using-file-accelerator-on-microsoft-edge-browser}

Microsoft Edge runs in Enhanced Protected Mode (EPM) preventing communication with the Aspera Connect server, while on same private network or with a Trusted Site. Therefore, a pop- up shows up every time a connection with the server is being established.

![](assets/switchapps-msedge.png)

To use accelerated download functionality on Microsoft Edge, remove the Brand Portal site from the trusted site list.

1. ********
1. ************
1. ********
1. Remove Brand Portal site from the list.

## Aspera Connect client Preferences {#aspera-connect-client-preferences}

****

![](assets/download_assets_frombrandportalimg19.png)

You can set the default download location.

![](assets/aspera-preferences.png)

Also, the Aspera Connect client can be marked to automatically start on system startup so that the connect client is running and available for the download to begin faster.

![](assets/aspera-automaticallylaunch.png)

## Troubleshoot issues with download acceleration {#troubleshoot-issues-with-download-acceleration}

If download acceleration is not working for you, follow these steps to troubleshoot:

1. [](https://test-connect.asperasoft.com/)

   If ports are not OK, then reach out to your network team and ensure that Ports 33001 (both TCP &amp; UDP) are not blocked in the firewall.

1. [](https://www.speedtest.net/)

   If the bandwidth is a few (1-10 Mbps) or in Kbps, then use Aspera Preferences and try to limit the bandwidth equal to the available bandwidth.

1. [](https://demo.asperasoft.com/aspera/user)\
   (login:  asperaweb , password:  demoaspera )

1. If none of the above troubleshooting steps work, deselect the option Enable Download Acceleration and use the normal download.
