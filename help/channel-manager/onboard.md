---
title: '"Inbyggt [!DNL Channel Manager]"'
description: Anslut instansen till [!DNL Channel Manager] genom att utföra några steg.
role: User
level: Intermediate
source-git-commit: ff87f31fec7a689385a93b8cab260fd93ff15f90
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Inbyggt [!DNL Channel Manager]

Anmäl kanalhanteraren genom att installera Channel Manager-tillägget på din [!DNL Commerce] instansen och konfigurationen av API-anslutningar för att aktivera kommunikation och datasynkronisering mellan din Commerce-instans och Walmart Marketplace.

När du är klar med introduktionen kan du konfigurera och hantera säljkanalsåtgärder från [!UICONTROL Channel Manager] på [!UICONTROL Commerce Admin Marketing] -menyn.

![[!DNL Channel Manager] i administrationsvyn](assets/channel-manager-admin-view.png)

## Översikt över introduktion

1. [Installera [!DNL Channel Manager] extension](install.md).

1. [Konfigurera [!DNL Commerce Services Connector]](connect.md) för att integrera kanalhanteraren med handelsinstansen och andra stödtjänster.

1. [Koppla samman [!DNL Commerce] lagra till [!DNL Walmart Marketplace]](connect.md).

## Förutsättningar

- Verifiera att du har Walmart Marketplace Seller AccountWalmart-krav för försäljning på Walmart Marketplace

- **Information om handelskonto**-Hämta och installera [!DNL Channel Manager] kräver ett ID och autentiseringsuppgifter från en [Handelskonto](https://docs.magento.com/user-guide/magento/magento-account.html){target=&quot;_blank&quot;} med ägaråtkomst till [!DNL Adobe Commerce] eller [!DNL Magento Open Source] -instans.

   - **BILD-ID**-[Logga in](https://account.magento.com/customer/account/login/) till Commerce-kontot för att hämta ID:t från [!UICONTROL My Account - Magento settings]. Du behöver detta ID för att registrera dig för [!DNL Channel Manager] betaprogram.

      ![[!DNL MAGEID] på inställningar för Commerce-konto](assets/mageid-my-commerce-account.png)

   - **Åtkomstnycklar-** Hämta autentiseringsnycklar för att hämta Commerce-tillägg från Commerce Composer-databasen ([!DNL repo.magento.com]).

      ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png)

      I Adobe Commerce- och Magento Open Source-projekt kan ägaren konfigurera [Delad åtkomst](https://docs.magento.com/user-guide/magento/magento-account-share.html) för att tillåta betrodda anställda och tjänsteleverantörer att hämta tillägg med hjälp av autentiseringsuppgifter från ägar- eller licenshållarkontot.

      På [!DNL Adobe Commerce] i molninfrastrukturprojekt måste användarna ha följande behörigheter för att installera programvara i [!DNL Commerce] instans:

      - Superanvändaråtkomst till Cloud-projektet
      - Administratörsåtkomst till en viss miljö
      - en [!DNL Adobe Commerce] eller [!DNL Magento Open Source] konto med behörighet att komma åt Composer-databasen. Se [Hantera användaråtkomst](https://devdocs.magento.com/cloud/project/user-admin.html).

- **Behörighet att hämta Channel Manager Composer-paketet**-Tillhandahåll MAGE-ID från det Commerce-konto som används för att hantera tjänsten till den Adobe-representant som koordinerar betaprogrammet för din organisation.
- **Upplevelse med Composer och[!DNL Commerce CLI]** -See [Allmän CLI-installation](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;} om du vill ha information om hur du använder verktygen för att installera och hantera tillägg på A[!DNL Adobe Commerce] eller [!DNL Magento Open Source] -plattformar.
- För Commerce-instanser som har Amazon Sales Channel installerat måste du kontrollera att [Amazon Sales Channel version 4.4.2 eller senare](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html) installeras innan Channel Manager installeras.


### Krav

- [Adobe Commerce 2.4.x](https://devdocs.magento.com/release/released-versions.html)
- [PHP 7.3/7.4](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)
- [Composer 1.x eller senare](https://devdocs.magento.com/cloud/reference/cloud-composer.html)


### Plattformar som stöds

- Adobe Commerce on Cloud (ECE): 2.4.x
- Adobe Commerce lokalkontor: 2.4.x
- Magento Open Source 2.4.x
