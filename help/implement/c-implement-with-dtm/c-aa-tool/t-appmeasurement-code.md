---
description: Insert AppMeasurement code when manually deploying Dynamic Tag Management in Adobe Analytics.
keywords: Dynamic Tag Management;linked accounts;linking accounts;edit code;appmeasurement;appmeasurement code
seo-description: Insert AppMeasurement code when manually deploying Dynamic Tag Management in Adobe Analytics.
seo-title: Insert core AppMeasurement code
solution: Marketing Cloud,Analytics,Target,Dynamic Tag Management
title: Insert core AppMeasurement code
uuid: 51d4c37e-cbde-4fa5-b2ae-2822c7937ef0
index: y
internal: n
snippet: y
---

# Insert core AppMeasurement code

Insert AppMeasurement code when manually deploying Dynamic Tag Management in Adobe Analytics.

1. On the [!DNL Adobe Analytics] tool page, expand the **[!UICONTROL General]** section, then click **[!UICONTROL Open Editor]**.
1. Unzip the [!DNL AppMeasurement_JavaScript*.zip] file you downloaded in [deploy Adobe Analytics](../../../implement/c-implement-with-dtm/t-analytics-deploy.md#task_3A00639CADF14C9C844F962222077E4E).

   If you opt for custom library, when you open the window it will already have the most recent code version present. There is no need to download the zip from the Admin Console. 
1. Open [!DNL AppMeasurement.js] in a text editor.
1. Copy and paste the contents into the **[!UICONTROL Edit Code]** window.

   ![](assets/edit-code.png)

1. Adobe recommends adding the following code above the *`Do Not Alter Anything Below This Line`*:

   ```
   var s_account="INSERT-RSID-HERE"
   var s=s_gi(s_account)
   
   ```

   >[!IMPORTANT]
   >
   >If you add this code, it is recommended that you also select the **[!UICONTROL Set report suites using custom code below]** checkbox in the overall library settings.

1. Click **[!UICONTROL Save and Close]**.

   If you are using the Media Module, Integrate Module, or implementation plug-ins, you can copy them into the code section as well. The managed code in Dynamic Tag Management can be configured exactly like the JavaScript file in a typical implementation. 
