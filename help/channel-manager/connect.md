---
title: '''Anslut till [!DNL Commerce] Tjänster'
description: Ansluta kanalhanteraren till [!DNL Commerce] tjänster för att möjliggöra datasynkronisering och kommunikation mellan [!DNL Commerce] -instans, Channel Manager och andra stödtjänster.'
role: User
level: Intermediate
exl-id: 97da2142-ecef-44dc-91d8-5dc55c713d31
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---


# Anslut till [!DNL Commerce] Tjänster

The [!DNL Commerce Services Connector] integrerar Channel Manager-tjänsten med instanser från Adobe Commerce och Magento Open Source. Kopplingen möjliggör datasynkronisering och kommunikation mellan [!DNL Commerce] instans, [!DNL Channel Manager]och andra stödtjänster.

[!DNL Commerce Services Connector] installation är en engångsprocess som krävs för att använda [Adobe Commerce SaaS-tjänster](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html){target="_blank"} som [!DNL Channel Manager], [!DNL Live Search]och [!DNL Product Recommendations]. Om du redan har konfigurerat anslutningen för en annan tjänst hoppar du över det här steget.

## Krav

- **Handelskonto**-Installera programvaran på [!DNL Commerce] -instanser måste du ha ett konto med ägar- eller administratörsåtkomst till [!DNL Commerce] plattform.

   Kontoägare och superanvändare kan skapa administratörskonton från [!DNL Commerce] -instans eller från kommandoraden med [!DNL Commerce] CLI, kommando `admin:user:create`.

- **Adobe Commerce Production API Key**-Den [key](https://docs.magento.com/user-guide/system/saas.html#apikey){target="_blank"} aktiverar API-åtkomst till tjänster som krävs av Channel Manager. Du behöver offentliga och privata autentiseringsuppgifter för den här nyckeln.

>[!TIP]
>
>Om du vill ange inloggningsuppgifterna [!DNL Commerce] licensinnehavare eller kontoägare har möjlighet att [dela åtkomst](https://docs.magento.com/user-guide/magento/magento-account-share.html){target="_blank"}, or give the [API Key](https://docs.magento.com/user-guide/system/saas.html#apikey){target="_blank"} autentiseringsuppgifter för en betrodd utvecklare.

## Konfigurera [!DNL Commerce Services Connector]

1. Öppna Store Services Configuration.

   - Välj **[!UICONTROL Stores]**.

   - Under *[!UICONTROL Settings]*, markera **[!UICONTROL Configuration]**.

   - Expandera **[!UICONTROL Services]** och markera **[!UICONTROL Commerce Services Connector]**.

1. Lägg till autentiseringsuppgifter för Production API-nyckel från ditt Adobe Commerce-konto.

   ![[!DNL Commerce Services Connector] i [!DNL Admin] visa](assets/commerce-services-connector-admin-service-view.png)


   >[!NOTE]
   >
   > Om [!DNL Commerce] instansen har en annan [!DNL Adobe Commerce] tjänster som [!DNL Live Search] eller [!DNL Product Recommendations] har installerats, inloggningsuppgifterna visas i gränssnittet och ingen ytterligare konfiguration krävs.

1. Konfigurera SaaS-projektet och dataområdet så att Commerce Services kan skicka data till Channel Manager-tjänsten.

   ![[!DNL Commerce Services Connector] Konfiguration av SaaS-identifierare i [!DNL Admin] visa](assets/commerce-services-connector-saas-config.png)

