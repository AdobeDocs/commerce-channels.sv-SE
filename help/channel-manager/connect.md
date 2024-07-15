---
title: Anslut till  [!DNL Commerce] tjänster
description: 'Anslut kanalhanteraren till  [!DNL Commerce] tjänster för att aktivera datasynkronisering och kommunikation mellan  [!DNL Commerce] instansen, kanalhanteraren och andra stödtjänster.'
role: Admin, Developer
level: Intermediate
feature: Sales Channels, Install, Integration
exl-id: 97da2142-ecef-44dc-91d8-5dc55c713d31
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---


# Anslut till [!DNL Commerce]-tjänster

[!DNL Commerce Services Connector] integrerar Channel Manager-tjänsten med instanser från Adobe Commerce och Magento Open Source. Kopplingen möjliggör datasynkronisering och kommunikation mellan [!DNL Commerce]-instansen, [!DNL Channel Manager] och andra stödtjänster.

Installationsprogrammet för [!DNL Commerce Services Connector] är en engångsprocess som krävs för att använda [Adobe Commerce SaaS-tjänster](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) som [!DNL Channel Manager], [!DNL Live Search] och [!DNL Product Recommendations]. Om du redan har konfigurerat anslutningen för en annan tjänst hoppar du över det här steget.

## Krav

- **Commerce-konto**-Om du vill installera program på [!DNL Commerce] instanser måste du ha ett konto med ägar- eller administratörsåtkomst till [!DNL Commerce]-plattformen.

  Kontoägare och superanvändare kan skapa administratörskonton från instansen [!DNL Commerce] eller från kommandoraden med hjälp av kommandot [!DNL Commerce] CLI `admin:user:create`.

- **Adobe Commerce Production API Key**-This [key](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#genapikey) enable API access to services required by Channel Manager. Du behöver offentliga och privata autentiseringsuppgifter för den här nyckeln.

>[!TIP]
>
>En [!DNL Commerce]-licensinnehavare eller kontoägare kan välja att [dela åtkomst](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html) eller ge [API-nyckeln](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html)-autentiseringsuppgifterna till en betrodd utvecklare för att kunna tillhandahålla autentiseringsuppgifterna.

## Konfigurera [!DNL Commerce Services Connector]

1. Öppna konfigurationen för Store-tjänster.

   - Välj **[!UICONTROL Stores]** i Admin.

   - Välj **[!UICONTROL Configuration]** under *[!UICONTROL Settings]*.

   - Expandera **[!UICONTROL Services]** och välj **[!UICONTROL Commerce Services Connector]**.

1. Lägg till autentiseringsuppgifter för Production API-nyckel från ditt Adobe Commerce-konto.

   ![[!DNL Commerce Services Connector]-tjänsten i [!DNL Admin] view ](assets/commerce-services-connector-admin-service-view.png){width="600" zoomable="yes"}


   >[!NOTE]
   >
   > Om din [!DNL Commerce]-instans har andra [!DNL Adobe Commerce]-tjänster som [!DNL Live Search] eller [!DNL Product Recommendations] installerade, visas inloggningsinformationen i gränssnittet och ingen ytterligare konfiguration krävs.

1. Konfigurera SaaS-projektet och dataområdet så att Commerce Services kan skicka data till Channel Manager-tjänsten.

   ![[!DNL Commerce Services Connector] SaaS-identifierarkonfiguration i [!DNL Admin] view ](assets/commerce-services-connector-saas-config.png){width="600" zoomable="yes"}

