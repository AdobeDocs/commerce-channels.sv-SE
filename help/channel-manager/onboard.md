---
title: Inbyggt [!DNL Channel Manager]
description: '''Anslut instansen till [!DNL Channel Manager] genom att slutföra några startsteg."'
level: Intermediate
role: Leader, Admin, Developer
feature: Sales Channels, Install
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---


# Inbyggt [!DNL Channel Manager]

När du är klar med Channel Manager-introduktionsprocessen kan du få åtkomst till, konfigurera och hantera kanalförsäljningsåtgärder på Walmart Marketplace från Adobe Commerce. Kanalhanteraren är tillgänglig från [!UICONTROL Channel Manager] på [!UICONTROL Commerce Admin Marketing] -menyn.

![[!DNL Channel Manager] i administrationsvyn](assets/channel-manager-admin-view.png){width="500"}

## Krav

Granska kraven för att använda Channel Manager och samla in kontoinformation och autentiseringsuppgifter för att hämta, installera och konfigurera tillägget.

- **[Krav på Walmart Marketplace](walmart-requirements.md)**-Verifiera att ni uppfyller kraven för att integrera med Channel Manager, inklusive [konfigurera ditt säljarkonto](https://sellerhelp.walmart.com/seller/s/guide?article=000008219) och generera API-nyckeln för att aktivera integreringen.

- **Information om handelskonto**-Hämta och installera [!DNL Channel Manager] kräver [Handelskonto](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-create.html). Du behöver ett konto-ID och autentiseringsuppgifter med ägar- eller administratörsåtkomst till [!DNL Adobe Commerce] eller [!DNL Magento Open Source] -instans.

   - **BILD-ID**-[Logga in](https://account.magento.com/customer/account/login/) till [!DNL Commerce] konto att hämta ID från **[!UICONTROL My Account - Magento settings]**.

     ![[!DNL MAGEID] på [!DNL Commerce] kontoinställningar](assets/mageid-my-commerce-account.png){width="250"}

   - **Åtkomstnycklar-** Hämta autentiseringsnycklar att hämta [!DNL Commerce] tillägg från [!DNL Commerce] Dispositionsdatabas `([!DNL repo.magento.com]`).

     ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png){width="400"}

     I Adobe Commerce- och Magento Open Source-projekt kan ägaren konfigurera [Delad åtkomst](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html) för att tillåta betrodda anställda och tjänsteleverantörer att hämta tillägg med hjälp av autentiseringsuppgifter från ägar- eller licenshållarkontot.

     För [!DNL Adobe Commerce] i molninfrastrukturprojekt måste programinstallerare ha följande åtkomst till [!DNL Commerce] instans:

      - Superanvändaråtkomst till Cloud-projektet
      - Administratörsåtkomst till en viss miljö
      - en [!DNL Adobe Commerce] konto med behörighet att komma åt Composer-databasen

     Se [Hantera användaråtkomst](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) i *Handbok för Commerce on Cloud Infrastructure*.

- **Upplevelse med Composer och[!DNL Commerce CLI]**-See [Installera ett tillägg](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) i *Installationshandbok* om du vill ha information om hur du använder verktygen för att installera och hantera tillägg på [!DNL Adobe Commerce] eller [!DNL Magento Open Source] -plattformar.

- **[[!DNL Amazon Sales Channel] version 4.4.2 eller senare](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)**-Om du har aktiverat [!DNL Amazon Sales Channel] för [!DNL Commerce] webbplatser, verifiera att [!DNL Commerce] har version 4.4.2 eller senare installerad innan du installerar [!DNL Channel Manager].

- **[!DNL Inventory Management]tillägg för Adobe Commerce och Magento Open Source**

  Om du tänker använda Channel Manager för lager- och orderhantering måste du ha Inventory management-tillägget installerat och aktiverat på din Adobe Commerce- och Magento Open Source-instans. Tillägget installeras och aktiveras som standard i Adobe Commerce och [!DNL Magento Open Source] 2.3.x och senare.

  Om du har uppgraderat Commerce från 2.2.x eller om du har inaktiverat Inventory management ska du uppdatera din installation så att den innehåller de moduler som krävs. Se [Installera Inventory management](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html) i *Inventory management Guide*.

### Systemkrav

- [Adobe Commerce 2.4.x](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html)
- [PHP 7.3/7.4](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html)
- [Composer 1.x eller senare](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/overview.html)
- [[!DNL Amazon Sales Channel] version 4.4.2 eller senare](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)-Om du har aktiverat [!DNL Amazon Sales Channel] för [!DNL Commerce] webbplatser, verifiera att [!DNL Commerce] har version 4.4.2 installerad innan du installerar [!DNL Channel Manager].
- [[!DNL Inventory Management]](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html)

### Plattformar som stöds

- Adobe Commerce on Cloud (ECE): 2.4.x
- Adobe Commerce lokalkontor: 2.4.x
- Magento Open Source 2.4.x

## Inledande steg

1. [Konfigurera ditt Walmart Seller-konto](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

1. [Installera [!DNL Channel Manager] extension](install.md).

1. [Anslut till Commerce Services](connect.md) för att integrera kanalhanteraren med handelsinstansen och andra stödtjänster.

1. [Koppla samman [!DNL Commerce] lagra till [!DNL Walmart Marketplace]](connect-marketplace.md).

1. [Slutför butiksinställning](complete-sales-channel-store-setup.md).
