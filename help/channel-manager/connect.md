---
title: Anslut till Commerce Services
description: Anslut Channel Manager-instans till [!DNL Commerce services] för att möjliggöra datasynkronisering och kommunikation mellan Commerce-instansen, Channel Manager och andra stödtjänster.
role: User
level: Intermediate
source-git-commit: ec950579a9b2220f9ec106b616779fc3503f3add
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# Anslut till Commerce Services

Commerce Services Connector integrerar Channel Manager-tjänsten med instanser i Adobe Commerce och Magento Open Source. Kopplingen möjliggör datasynkronisering och kommunikation mellan [!DNL Commerce] instans, [!DNL Channel Manager]och andra stödtjänster.

Konfigurationen av Commerce Services Connector är en engångsprocess som krävs för att använda Adobe [Commerce SaaS-tjänster](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html){target=&quot;_blank&quot;} gillar [!DNL Channel Manager], [!DNL Live Search]och [!DNL Product Recommendations]. Om du redan har konfigurerat kopplingen för en annan tjänst kan du hoppa över det här steget.

## Förutsättningar

- **Handelskonto med [Administratörsåtkomst](https://docs.magento.com/user-guide/stores/admin.html){target=&quot;_blank&quot;}** till din Commerce-instans**-Kontoägare och Admin-användare kan konfigurera användarkonton från Commerce-instansen eller från kommandoraden med [!DNL Commerce] CLI, kommando `admin:user:create`.

- **Adobe Commerce [API-nycklar för produktion](https://docs.magento.com/user-guide/system/saas.html#apikey){target=&quot;_blank&quot;}**-Aktivera API-åtkomst till tjänster som krävs av Channel Manager

   En innehavare av en Commerce-licens eller kontoägare har möjlighet att ange inloggningsuppgifterna
   [dela åtkomst](https://docs.magento.com/user-guide/magento/magento-account-share.html){target=&quot;_blank&quot;}, eller ge [API-nyckel](https://docs.magento.com/user-guide/system/saas.html#apikey){target=&quot;_blank&quot;} autentiseringsuppgifter för en betrodd utvecklare.

## Konfigurera Commerce Services Connector

1. Öppna Store Services Configuration.

   - Välj [!UICONTROL Stores].

   - Under *Inställningar*, markera [!UICONTROL Configuration].

   - På [!UICONTROL Configuration] sida, expandera [!UICONTROL Services] och markera [!UICONTROL Commerce Services Connector].

1. Lägg till API-nycklar för produktion från ditt Adobe Commerce-konto.

   ![[!DNL Commerce Service Connector] i [!DNL Admin] visa](assets/commerce-services-connector-admin-service-view.png)


   >[!NOTE]
   >
   > Om [!DNL Commerce] instansen har en annan [!DNL Adobe Commerce] tjänster som [!DNL Live Search] eller [!DNL Product Recommendations] har installerats, inloggningsuppgifterna visas i gränssnittet och ingen ytterligare konfiguration krävs.

1. Konfigurera SaaS-projektet och dataområdet så att Commerce Services kan skicka data till Channel Manager-tjänsten.

   ![[!DNL Commerce Service Connector] Konfiguration av SaaS-identifierare i [!DNL Admin] visa](assets/commerce-services-connector-saas-config.png)

