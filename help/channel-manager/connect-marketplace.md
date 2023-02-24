---
title: 'Anslut [!DNL Channel Manager] till [!DNL Walmart Marketplace]'
description: "Anslut en Commerce Store-vy till [!DNL Walmart Marketplace] för att skapa en försäljningskanal för att hantera Commerce-produktlistor, lager, pris och order för Walmart Marketplace-försäljning."
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Anslut [!DNL Channel Manager] till [!DNL Walmart Marketplace]

När du har installerat Channel Manager på din [!DNL Commerce] skapa en försäljningskanal i Channel Manager och konfigurera autentiseringsuppgifterna för att ansluta [!DNL Channel Manager] till [!DNL Walmart Marketplace].

1. [Skapa försäljningskanalen](#create-the-sales-channel) genom att välja [!DNL Commerce] lagra produktlistor.

1. [Ansluta kanalen till [!DNL Walmart Marketplace] genom att lägga till [!UICONTROL Walmart API credentials]](#connect-the-channel-to-walmart-marketplace).

1. [Slutför konfiguration av försäljningskanal](#complete-sales-channel-store-setup) för att hantera listor, lager, priser och beställningar för [!DNL Walmart Marketplace] produktsortiment.

>[!NOTE]
>
>Channel Manager kräver en 1:1-anslutning mellan ett Walmart-konto och ett [!DNL Commerce] butiksvy. Du kan inte ansluta samma butiksvy till flera Walmart-konton.

## Skapa försäljningskanalen

1. Öppna från Admin [!DNL Channel Manager] genom att välja **[!UICONTROL Marketing** > _Kanaler _> **Channel Manager]**.

1. I **[!UICONTROL Marketplaces available to connect]** avsnitt, markera **[!UICONTROL Get Started]**.

   ![Anslut nytt [!DNL Walmart] lagra till [!DNL Channel Manager]](assets/channel-manager-home.png)

1. Konfigurera [!DNL Walmart Marketplace Seller] konto.

1. Konfigurera arkivet och anslutningen:

   - Välj **[!UICONTROL Add Credentials]**.

   - Välj [!DNL Commerce] butiksvy som erbjuder de produkter du vill sälja på marknaden.

      ![Konfigurera anslutning mellan [!DNL Commerce] och [!DNL Walmart Marketplace] från [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png)

   - Ange ett unikt **[!UICONTROL store name]**.

   - Välj **[!UICONTROL Adobe [!DNL Commerce] site]** för produktlistor och orderhantering.

   - Att ta emot meddelanden relaterade till [!DNL Channel Manager], lägga till **[!UICONTROL email address]**.

1. Ansluta kanalen till [!DNL Walmart Marketplace].

   - Lägg till autentiseringsuppgifterna för [[!DNL Walmart Marketplace Adobe Production API key]](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) från [!DNL Walmart Marketplace Seller] konto.

   - Om du inte har inloggningsuppgifterna hämtar du dem från [!DNL Walmart Marketplace Developer Portal] genom att välja **[!UICONTROL Get API credentials]**.

      På Developer Portal väljer du region (USA och Kanada) och loggar sedan in.

      ![[!DNL Walmart Marketplace] kontoinloggning](assets/walmart-marketplace-login-page.png)

   - Kopiera och spara API-nyckelformuläret **[!UICONTROL Client ID]** och **[!UICONTROL Client Secret]** värden för [!UICONTROL Adobe Inc Production API key] till en säker plats.

      ![[!DNL Walmart Marketplace API key] konfigurationssida](assets/walmart-api-key-management-form.png)

      >[!NOTE]
      >
      >Om [!DNL Adobe Inc] är inte listad i Developer Portal, välj **[!UICONTROL Add New Key for a Solution Provider]** för att konfigurera behörigheter och generera nyckeln. Konfigurationsinformation finns i [Generera en [!DNL Walmart Marketplace API Key]](walmart-requirements.md#generate-a-walmart-marketplace-api-key).

   - Återgå till [!DNL Channel Manager] för att lägga till inloggningsuppgifterna i **[!UICONTROL Walmart Connection]** information.

      När du lägger till autentiseringsuppgifter döljer Adobe klienthemligheten och lagrar värdet i ett säkert valv.

1. Välj **[!UICONTROL Save Store]** för att tillämpa konfigurationen och ansluta till [!DNL Walmart marketplace].

1. När anslutningen har slutförts [fullständig butiksinställning](complete-sales-channel-store-setup.md) från **[!UICONTROL Channel Manager]** butikssida.

![Konfigurera första butik](assets/channel-manager-setup-first-store.png)

### Felsöka anslutningsproblem

Om anslutningen till [!DNL Walmart] misslyckas, se [Frågor och svar om Walmart Marketplace](https://developer.walmart.com/faq/us/faq-auth/){target="_blank"} för felsökningstips.

- Från [!DNL Walmart Developer Portal]kontrollerar du att du har kopierat rätt autentiseringsuppgifter för produktions-API-nyckeln för [!UICONTROL Adobe Inc.]

- Verifiera att åtkomstkonfigurationen för [!UICONTROL Walmart Adobe API key] har rätt behörigheter. Se [[!DNL Walmart Requirements]](walmart-requirements.md##generate-a-walmart-marketplace-api-key).

- Bekräfta att [!DNL Walmart API] är tillgänglig från [WWART API-statussida](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target="_blank"}.
