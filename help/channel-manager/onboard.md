---
title: Inbyggt [!DNL Channel Manager]
description: '''Anslut instansen till [!DNL Channel Manager] genom att slutföra några startsteg."'
role: User
level: Intermediate
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: 738c48b8b8075e7c8bbf883c58cc8de39bca355c
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---


# Inbyggt [!DNL Channel Manager]

När du är klar med Channel Manager-introduktionsprocessen kan du få åtkomst till, konfigurera och hantera kanalförsäljningsåtgärder på Walmart Marketplace från Adobe Commerce. Kanalhanteraren är tillgänglig från [!UICONTROL Channel Manager] på [!UICONTROL Commerce Admin Marketing] -menyn.

![[!DNL Channel Manager] i administrationsvyn](assets/channel-manager-admin-view.png)

## Krav

Granska kraven för att använda Channel Manager och samla in kontoinformation och autentiseringsuppgifter för att hämta, installera och konfigurera tillägget.

- **[Krav på Walmart Marketplace](walmart-requirements.md)**-Verifiera att ni uppfyller kraven för att integrera med Channel Manager, inklusive [konfigurera ditt säljarkonto](https://sellerhelp.walmart.com/seller/s/guide?article=000008219) och generera API-nyckeln för att aktivera integreringen.

- **Information om handelskonto**-Hämta och installera [!DNL Channel Manager] kräver [Handelskonto](https://docs.magento.com/user-guide/magento/magento-account.html){target=&quot;_blank&quot;}. Du behöver ett konto-ID och autentiseringsuppgifter med ägar- eller administratörsåtkomst till [!DNL Adobe Commerce] eller [!DNL Magento Open Source] -instans.

   - **BILD-ID**-[Logga in](https://account.magento.com/customer/account/login/) till [!DNL Commerce] konto att hämta ID från **[!UICONTROL My Account - Magento settings]**.

      ![[!DNL MAGEID] på [!DNL Commerce] kontoinställningar](assets/mageid-my-commerce-account.png)

   - **Åtkomstnycklar-** Hämta autentiseringsnycklar att hämta [!DNL Commerce] tillägg från [!DNL Commerce] Dispositionsdatabas `([!DNL repo.magento.com]`).

      ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png)

      I Adobe Commerce- och Magento Open Source-projekt kan ägaren konfigurera [Delad åtkomst](https://docs.magento.com/user-guide/magento/magento-account-share.html) för att tillåta betrodda anställda och tjänsteleverantörer att hämta tillägg med hjälp av autentiseringsuppgifter från ägar- eller licenshållarkontot.

      För [!DNL Adobe Commerce] i molninfrastrukturprojekt måste programinstallerare ha följande åtkomst till [!DNL Commerce] instans:

      - Superanvändaråtkomst till Cloud-projektet
      - Administratörsåtkomst till en viss miljö
      - en [!DNL Adobe Commerce] konto med behörighet att komma åt Composer-databasen

      Se [Hantera användaråtkomst](https://devdocs.magento.com/cloud/project/user-admin.html).


- **Upplevelse med Composer och[!DNL Commerce CLI]**-See [Allmän CLI-installation](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;} om du vill ha information om hur du använder verktygen för att installera och hantera tillägg på [!DNL Adobe Commerce] eller [!DNL Magento Open Source] -plattformar.

- **[[!DNL Amazon Sales Channel] version 4.4.2 eller senare](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)**-Om du har aktiverat [!DNL Amazon Sales Channel] för [!DNL Commerce] webbplatser, verifiera att [!DNL Commerce] har version 4.4.2 eller senare installerad innan du installerar [!DNL Channel Manager].

- **[!DNL Inventory Management]tillägg för Adobe Commerce och Magento Open Source**

   Om du tänker använda Channel Manager för lager- och orderhantering måste du ha Inventory management-tillägget installerat och aktiverat på din Adobe Commerce- och Magento Open Source-instans. Tillägget installeras och aktiveras som standard i Adobe Commerce och [!DNL Magento Open Source] 2.3.x och senare.

   Om du har uppgraderat Commerce från 2.2.x eller om du har inaktiverat Inventory management ska du uppdatera din installation så att den innehåller de moduler som krävs. Se [Installera Inventory management](https://devdocs.magento.com/extensions/inventory-management/) i Adobe Commerce Developer-dokumentationen.

### Systemkrav

- [Adobe Commerce 2.4.x](https://devdocs.magento.com/release/released-versions.html)
- [PHP 7.3/7.4](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)
- [Composer 1.x eller senare](https://devdocs.magento.com/cloud/reference/cloud-composer.html)
- [[!DNL Amazon Sales Channel] version 4.4.2 eller senare](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)-Om du har aktiverat [!DNL Amazon Sales Channel] för [!DNL Commerce] webbplatser, verifiera att [!DNL Commerce] har version 4.4.2 installerad innan du installerar [!DNL Channel Manager].
- [[!DNL Inventory Management]](https://devdocs.magento.com/extensions/inventory-management/)

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
