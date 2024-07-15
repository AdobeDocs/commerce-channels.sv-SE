---
title: Inbyggt [!DNL Channel Manager]
description: 'Anslut instansen till tjänsten [!DNL Channel Manager] genom att slutföra några startsteg.'
level: Intermediate
role: Leader, Admin, Developer
feature: Sales Channels, Install
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---


# Inbyggt [!DNL Channel Manager]

När du är klar med Channel Manager-introduktionsprocessen kan du få åtkomst till, konfigurera och hantera kanalförsäljningsåtgärder på Walmart Marketplace från Adobe Commerce. Kanalhanteraren är tillgänglig från alternativet [!UICONTROL Channel Manager] på menyn [!UICONTROL Commerce Admin Marketing].

Alternativet ![[!DNL Channel Manager] i administratörsvyn ](assets/channel-manager-admin-view.png){width="500"}

## Krav

Granska kraven för att använda Channel Manager och samla in kontoinformation och autentiseringsuppgifter för att hämta, installera och konfigurera tillägget.

- **[Gå till Marketplace-krav](walmart-requirements.md)**-Verifiera att du uppfyller kraven för att integrera med Channel Manager, inklusive [att konfigurera ditt säljarkonto](https://sellerhelp.walmart.com/seller/s/guide?article=000008219) och generera API-nyckeln för att aktivera integreringen.

- **Commerce-kontoinformation**-Hämtning och installation av [!DNL Channel Manager] kräver ett [Commerce-konto](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-create.html). Du behöver ett konto-ID och autentiseringsuppgifter med ägar- eller administratörsåtkomst till instansen [!DNL Adobe Commerce] eller [!DNL Magento Open Source].

   - **MAGE ID**-[Logga in](https://account.magento.com/customer/account/login/) på [!DNL Commerce]-kontot för att hämta ID:t från **[!UICONTROL My Account - Magento settings]**.

     ![[!DNL MAGEID] på [!DNL Commerce] kontoinställningar ](assets/mageid-my-commerce-account.png){width="250"}

   - **Åtkomstnycklar-** Hämta autentiseringsnycklar för att hämta [!DNL Commerce] tillägg från [!DNL Commerce] Composer-databasen `([!DNL repo.magento.com]`).

     ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png){width="400"}

     I Adobe Commerce- och Magento Open Source-projekt kan ägaren konfigurera [delad åtkomst](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html) så att betrodda medarbetare och tjänsteleverantörer kan hämta tillägg med hjälp av autentiseringsuppgifter från ägar- eller licenshållarkontot.

     För [!DNL Adobe Commerce] i molninfrastrukturprojekt måste programinstallerare ha följande åtkomst till instansen [!DNL Commerce]:

      - Superanvändaråtkomst till Cloud-projektet
      - Administratörsåtkomst till en viss miljö
      - ett [!DNL Adobe Commerce]-konto med behörighet att komma åt Composer-databasen

     Se [Hantera användaråtkomst](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) i *Commerce on Cloud Infrastructure Guide*.

- **Använd Composer och[!DNL Commerce CLI]**-See [Installera ett tillägg](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) i *installationshandboken* om du vill ha information om hur du använder verktygen för att installera och hantera tillägg på [!DNL Adobe Commerce] - eller [!DNL Magento Open Source]-plattformar.

- **[[!DNL Amazon Sales Channel] version 4.4.2 eller senare](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)**-Om du aktiverade [!DNL Amazon Sales Channel] för dina [!DNL Commerce]-platser kontrollerar du att version 4.4.2 eller senare för din [!DNL Commerce]-plattform är installerad innan du installerar [!DNL Channel Manager].

- **[!DNL Inventory Management]-tillägg för Adobe Commerce och Magento Open Source**

  Om du tänker använda Channel Manager för lager- och orderhantering måste du ha Inventory management-tillägget installerat och aktiverat på din Adobe Commerce- och Magento Open Source-instans. Det här tillägget installeras och aktiveras som standard i Adobe Commerce och [!DNL Magento Open Source] 2.3.x och senare.

  Om du har uppgraderat Commerce från 2.2.x eller om du har inaktiverat Inventory management ska du uppdatera din installation så att den innehåller de moduler som krävs. Se [Installera Inventory management](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html) i *Inventory management-handboken*.

### Systemkrav

- [Adobe Commerce 2.4.x](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html)
- [PHP 7.3/7.4](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html)
- [Composer 1.x eller senare](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/overview.html)
- [[!DNL Amazon Sales Channel] version 4.4.2 eller senare](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)-Om du har aktiverat [!DNL Amazon Sales Channel] för dina [!DNL Commerce] -platser kontrollerar du att version 4.4.2 för din [!DNL Commerce]-plattform är installerad innan du installerar [!DNL Channel Manager].
- [[!DNL Inventory Management]](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html)

### Plattformar som stöds

- Adobe Commerce on Cloud (ECE): 2.4.x
- Adobe Commerce lokalkontor: 2.4.x
- Magento Open Source 2.4.x

## Onboarding-steg

1. [Konfigurera ditt Walmart Seller-konto](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

1. [Installera  [!DNL Channel Manager] tillägget](install.md).

1. [Anslut till Commerce Services](connect.md) om du vill integrera Channel Manager med Commerce-instansen och andra stödtjänster.

1. [Anslut din [!DNL Commerce] butik till [!DNL Walmart Marketplace]](connect-marketplace.md).

1. [Slutför butikskonfiguration](complete-sales-channel-store-setup.md).
