---
title: Koppla försäljningskanal till [!DNL Walmart Marketplace]
description: Konfigurera säljkanalen och anslut till Walmart Marketplace.
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
source-git-commit: e0b7f971f8eb4bc0827a7792ef94d88766adf82e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Koppla försäljningskanal till [!DNL Walmart Marketplace]

När du har installerat Channel Manager på din [!DNL Commerce] koppla en Commerce Store till Walmart Marketplace.

1. [Skapa försäljningskanalen](#create-the-sales-channel) genom att välja Commerce Store för produktlistor.

1. [Ansluta kanalen till [!DNL Walmart Marketplace] genom att lägga till Walmart API-autentiseringsuppgifter](#connect-the-channel-to-walmart-marketplace).

1. [Slutför konfiguration av försäljningskanal](#complete-store-setup) för att hantera listor, lager, priser och beställningar för produktsortiment på Walmart Marketplace.

## Skapa försäljningskanalen

1. Öppna [!DNL Channel Manager].

   - I Admin väljer du **[!UICONTROL Marketing** > _Kanaler _> **Channel Manager]**.

   - Välj **[!UICONTROL Connect New Store]**.

      ![Anslut Commerce Store till [!DNL Walmart Marketplace] från [!DNL Channel Manager]](assets/connect-commerce-store-to-marketplace.png)


1. Konfigurera arkivet och anslutningen:

   - Ange ett unikt **[!UICONTROL store name]**.

   - Välj **[!UICONTROL Adobe Commerce site]** för produktlistor.

   - Lägg till en **[!UICONTROL email address]** för att ta emot tjänstmeddelanden relaterade till [!DNL Channel Manager].

      ![Konfigurera anslutning mellan Commerce och [!DNL Walmart Marketplace] från [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png)

## Ansluta kanalen till Walmart Marketplace

1. Lägg till autentiseringsuppgifterna för [[!DNL Walmart Marketplace Adobe Production API key]](connect-marketplace.md#generate-a-walmart-marketplace-production-api-key) från [!DNL Walmart Marketplace Seller] konto.

   - Om du inte har inloggningsuppgifterna väljer du **[!UICONTROL Get API credentials]** för att få dem från [!DNL Walmart Marketplace Developer Portal].

      Välj region (USA och Kanada) och logga sedan in om du uppmanas till detta.

      ![[!DNL Walmart Marketplace] kontoinloggning](assets/walmart-marketplace-login-page.png)

   - Kopiera och spara API-nyckelformuläret **[!UICONTROL Client ID]** och **[!UICONTROL Client Secret]** värden för [!UICONTROL Adobe Inc Production API key] till en säker plats.

      ![[!DNL Walmart Marketplace API key] konfigurationssida](assets/walmart-api-key-management-form.png)

      >[!NOTE]
      >
      >Om [!DNL Adobe Inc] är inte listad i Developer Portal, välj **[!UICONTROL Add New Key for a Solution Provider]** för att konfigurera behörigheter och generera nyckeln. Konfigurationsinformation finns i [Generera en [!DNL Walmart Marketplace API Key]](walmart-prerequisites.md#generate-a-walmart-marketplace-api-key).

   - Återgå till [!DNL Channel Manager] för att lägga till inloggningsuppgifterna i **[!UICONTROL Walmart Connection]** information.

      När du lägger till autentiseringsuppgifter i [!DNL Channel Manager], döljer Adobe kundhemligheten och lagrar värdet i ett säkert valv.

1. Välj [!UICONTROL Save] för att tillämpa konfigurationen och ansluta till [!DNL Walmart marketplace].

Hantera kanalen från **[!UICONTROL Channel Manager > Marketplace Stores]**.

![[!DNL Walmart Marketplace API key] konfigurationssida](assets/manage-connected-stores.png)


### Felsöka anslutningsproblem

Om anslutningen till Walmart misslyckas, se [Frågor och svar om Walmart Marketplace](https://developer.walmart.com/faq/us/faq-auth/){target=&quot;_blank&quot;} för felsökningstips.

- Från [!DNL Walmart Developer Portal]kontrollerar du att du har kopierat rätt autentiseringsuppgifter för produktions-API-nyckeln för [!UICONTROL Adobe Inc.]

- Kontrollera att åtkomstkonfigurationen för Walmart Adobe API-nyckeln har rätt behörigheter. Se [Krav för Walmart](walmart-prerequisites.md##generate-a-walmart-marketplace-api-key).

- Bekräfta att [!DNL Walmart API] är tillgänglig från [WWART API-statussida](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target=&quot;_blank&quot;}.

## Slutför butiksinställning

När du har anslutit en Commerce Store till [!DNL Walmart Marketplace]kan du slutföra butiksinställningarna från [!DNL Channel Manager Stores] vy.

Så här slutför du butiksinställningarna:

1. Välj **[!UICONTROL Marketing** > **Kanalhanteraren**].

   ![[!DNL Walmart Marketplace API key] konfigurationssida](assets/connect-commerce-store-config.png)

1. Öppna en ansluten försäljningskanal genom att välja pennikonen i en butikspostrad.

1. Starta säljkanalsåtgärder.

   - [Lägg till produkter från din Commerce Catalog i Channel Manager](add-products-to-connected-channel.md)

   - [Publicera produkter på Walmart med produktmatchning](publish-listings-to-marketplace.md)

   - [Visa och hantera lager och priser](inventory-and-price-updates.md)

   - [Visa och hantera Walmart-order från Commerce Admin](manage-orders.md)
