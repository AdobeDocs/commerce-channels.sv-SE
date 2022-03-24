---
title: 'Anslut Sales Channel till [!DNL Walmart Marketplace] '
description: Konfigurera säljkanalen och anslut till Walmart Marketplace.
source-git-commit: ff87f31fec7a689385a93b8cab260fd93ff15f90
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# Anslut till [!DNL Walmart Marketplace]

När du har installerat Channel Manager på din [!DNL Commerce] koppla en Commerce Store till Walmart Marketplace.

1. Skapa försäljningskanalen med [välja Commerce Store för produktlistor](#select-the-commerce-store-for-the-sales-channel).

1. [Ansluta kanalen till [!DNL Walmart Marketplace] genom att lägga till Walmart API-autentiseringsuppgifter](#connect-the-channel-to-walmart-marketplace).

1. [Slutför konfiguration av försäljningskanal](#complete-store-setup) så att ni kan hantera listor, lager, priser och försäljning från Channel Manager.

## Skapa försäljningskanalen

1. Öppna kanalhanteraren.

   - I Admin väljer du **[!UICONTROL Marketing** > _Kanaler _> **Channel Manager]**.

   - Välj **[!UICONTROL Connect New Store]**.

      ![Anslut Commerce Store till [!DNL Walmart Marketplace] från [!DNL Channel Manager]](assets/connect-commerce-store-to-marketplace.png)


1. Konfigurera arkivet och anslutningen:

   - Ange ett unikt **[!UICONTROL store name]**.

   - Välj **[!UICONTROL Adobe Commerce site]** för produktlistor.

   - Lägg till en **[!UICONTROL email address]** för att ta emot tjänstmeddelanden relaterade till [!DNL Channel Manager].

      ![Konfigurera anslutning mellan Commerce och [!DNL Walmart Marketplace] från [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png)


## Ansluta kanalen till Walmart Marketplace

1. Lägg till autentiseringsuppgifterna för [!DNL Walmart Marketplace Adobe Production API key] från [!DNL Walmart Marketplace Seller] konto.

   - Om du inte har inloggningsuppgifterna väljer du **[!UICONTROL Get API credentials]** för att få dem från [!DNL Walmart Marketplace Developer Portal].

      Välj region (USA och Kanada) och logga sedan in om du uppmanas till detta.

      ![[!DNL Walmart Marketplace] kontoinloggning](assets/walmart-marketplace-login-page.png)

   - Kopiera och spara API-nyckelformuläret **[!UICONTROL Client ID]** och **[!UICONTROL Client Secret]** värden för [!UICONTROL Adobe Inc Production API key] till en säker plats.

      ![[!DNL Walmart Marketplace API key] konfigurationssida](assets/walmart-api-key-management-form.png)

      >[!NOTE]
      >
      >Om du inte ser en [!DNL Adobe Inc] på Developer Portal väljer du **[!UICONTROL Add New Key for a Solution Provider]** för att konfigurera behörigheter och generera nyckeln. Konfigurationsinformation finns i [Generera en [!DNL Walmart Marketplace API Key]](overview.md#generate-a-walmart-marketplace-api-key).

   - Återgå till [!DNL Channel Manager] för att lägga till inloggningsuppgifterna i **[!UICONTROL Walmart Connection]** information.

      När du lägger till autentiseringsuppgifter i [!DNL Channel Manager], döljer Adobe kundhemligheten och lagrar värdet i ett säkert valv.

1. [!UICONTROL Save] konfigurationen för att upprätta anslutningen.

   Hantera kanalen från **[!UICONTROL Channel Manager > Marketplace Stores]**.

   ![[!DNL Walmart Marketplace API key] konfigurationssida](assets/manage-connected-stores.png)


### Felsöka anslutningsproblem

Om anslutningen till Walmart misslyckas, se [Frågor och svar om Walmart Marketplace](https://developer.walmart.com/faq/us/faq-auth/){target=&quot;_blank&quot;} för felsökningstips.

- Från [!DNL Walmart Developer Portal]kontrollerar du att du har kopierat rätt autentiseringsuppgifter för produktions-API-nyckeln för [!UICONTROL Adobe Inc.]

- Kontrollera att åtkomstkonfigurationen för Walmart Adobe API-nyckeln har rätt behörigheter. Se [Krav för Walmart](overview.md#walmart-prerequisites).

- Bekräfta att Walmart API-tjänsten är tillgänglig från [WWART API-statussida](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target=&quot;_blank&quot;}.


## Slutför butiksinställning

När du har anslutit en Commerce Store till [!DNL Walmart Marketplace]kan du slutföra butiksinställningarna från [!DNL Channel Manager Stores] vy.

Så här slutför du butiksinställningarna:

1. Välj **[!UICONTROL Marketing** > **Kanalhanteraren**].

   ![[!DNL Walmart Marketplace API key] konfigurationssida](assets/connect-commerce-store-config.png)

1. Öppna en ansluten försäljningskanal genom att välja pennikonen i en butikspostrad.

1. Starta säljkanalsåtgärder.

   - Lägg till produkter från din Commerce Catalog i Channel Manager

   - Publicera produkter på Walmart med produktmatchning

   - Visa och hantera lager och priser

   - Visa och hantera Walmart-order från Commerce Admin
