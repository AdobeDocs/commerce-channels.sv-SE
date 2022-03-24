---
title: Inbyggt [!DNL Channel Manager]
description: Anslut instansen till [!DNL Channel Manager] genom att utföra några steg.
role: User
level: Intermediate
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: f57c6db4c0314272d10bb5483d2c8a0ae396a9fc
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---

# Inbyggt [!DNL Channel Manager]

Anmäl kanalhanteraren genom att installera Channel Manager-tillägget på din [!DNL Commerce] instans och konfiguration av API-anslutningar. Dessa anslutningar möjliggör kommunikation och datasynkronisering mellan din Commerce-instans och Walmart Marketplace.

När du är klar med introduktionen konfigurerar och hanterar du säljkanalsåtgärder från [!UICONTROL Channel Manager] på [!UICONTROL Commerce Admin Marketing] -menyn.

![[!DNL Channel Manager] i administrationsvyn](assets/channel-manager-admin-view.png)

## Översikt över introduktion

1. [Installera [!DNL Channel Manager] extension](install.md).

1. [Konfigurera [!DNL Commerce Services Connector]](connect.md) för att integrera kanalhanteraren med handelsinstansen och andra stödtjänster.

1. [Koppla samman [!DNL Commerce] lagra till [!DNL Walmart Marketplace]](connect.md).

1. [Slutför butiksinställning](complete-store-setup.md).

## Förutsättningar

- Kontrollera att du har rätt [Krav på Walmart Marketplace](walmart-prerequisites.md) för integrering med Channel Manager.

- **Information om handelskonto**-Hämta och installera [!DNL Channel Manager] kräver [Handelskonto](https://docs.magento.com/user-guide/magento/magento-account.html){target=&quot;_blank&quot;}. Du behöver ett konto-ID och autentiseringsuppgifter med ägar- eller administratörsåtkomst till [!DNL Adobe Commerce] eller [!DNL Magento Open Source] -instans.

   - **BILD-ID**-[Logga in](https://account.magento.com/customer/account/login/) till Commerce-kontot för att hämta ID:t från **[!UICONTROL My Account - Magento settings]**. Du behöver detta ID för att registrera dig för [!DNL Channel Manager] betaprogram.

      ![[!DNL MAGEID] på inställningar för Commerce-konto](assets/mageid-my-commerce-account.png)

   - **Åtkomstnycklar-** Hämta autentiseringsnycklar för att hämta Commerce-tillägg från Commerce Composer-databasen `([!DNL repo.magento.com]`).

      ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png)

      I Adobe Commerce- och Magento Open Source-projekt kan ägaren konfigurera [Delad åtkomst](https://docs.magento.com/user-guide/magento/magento-account-share.html) för att tillåta betrodda anställda och tjänsteleverantörer att hämta tillägg med hjälp av autentiseringsuppgifter från ägar- eller licenshållarkontot.

      På [!DNL Adobe Commerce] i molninfrastrukturprojekt måste programinstallerare ha följande åtkomst till [!DNL Commerce] instans:

      - Superanvändaråtkomst till Cloud-projektet
      - Administratörsåtkomst till en viss miljö
      - en [!DNL Adobe Commerce] eller [!DNL Magento Open Source] konto med behörighet att komma åt Composer-databasen.

      Se [Hantera användaråtkomst](https://devdocs.magento.com/cloud/project/user-admin.html).


- **Behörighet att hämta Channel Manager Composer-paketet**-Tillhandahåll MAGE-ID från det Commerce-konto som används för att hantera tjänsten till den Adobe-representant som koordinerar betaprogrammet för din organisation.
- **Upplevelse med Composer och[!DNL Commerce CLI]** -See [Allmän CLI-installation](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;} om du vill ha information om hur du använder verktygen för att installera och hantera tillägg på [!DNL Adobe Commerce] eller [!DNL Magento Open Source] -plattformar.
- **[Amazon Sales Channel version 4.4.2 eller senare](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)-Om du har aktiverat Amazon Sales Channel för dina Commerce-webbplatser måste du kontrollera att din Commerce-plattform har version 4.42 installerad innan du installerar Channel Manager.


### Krav

- [Adobe Commerce 2.4.x](https://devdocs.magento.com/release/released-versions.html)
- [PHP 7.3/7.4](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)
- [Composer 1.x eller senare](https://devdocs.magento.com/cloud/reference/cloud-composer.html)


### Plattformar som stöds

- Adobe Commerce on Cloud (ECE): 2.4.x
- Adobe Commerce lokalkontor: 2.4.x
- Magento Open Source 2.4.x
