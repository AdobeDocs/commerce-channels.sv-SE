---
title: Anslut [!DNL Channel Manager] till [!DNL Walmart Marketplace]
description: "Anslut en Commerce-butiksvy till  [!DNL Walmart Marketplace] för att skapa en försäljningskanal för att hantera Commerce produktlistor, lager, pris och order för Walmart Marketplace-försäljning."
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
role: Admin, Developer
feature: Sales Channels, Install, Integration
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Anslut [!DNL Channel Manager] till [!DNL Walmart Marketplace]

När du har installerat Channel Manager på din [!DNL Commerce]-instans skapar du en försäljningskanal i Channel Manager och konfigurerar autentiseringsuppgifterna för att ansluta [!DNL Channel Manager] till [!DNL Walmart Marketplace].

1. [Skapa försäljningskanalen](#create-the-sales-channel) genom att välja butiken [!DNL Commerce] för produktlistor.

1. [Anslut kanalen till  [!DNL Walmart Marketplace] genom att lägga till [!UICONTROL Walmart API credentials]](#connect-the-channel-to-walmart-marketplace).

1. [Slutför konfigurationen av försäljningskanalen](#complete-sales-channel-store-setup) för att hantera listor, lager, priser och order för din [!DNL Walmart Marketplace] produktsortiment.

>[!NOTE]
>
>Channel Manager kräver en 1:1-anslutning mellan ett Walmart-konto och en [!DNL Commerce]-butiksvy. Du kan inte ansluta samma butiksvy till flera Walmart-konton.

## Skapa försäljningskanalen

1. Öppna [!DNL Channel Manager] från Admin genom att välja **[!UICONTROL Marketing** > _Kanaler _> **Kanalhanteraren]**.

1. Välj **[!UICONTROL Get Started]** i avsnittet **[!UICONTROL Marketplaces available to connect]**.

   ![Anslut en ny [!DNL Walmart]-butik till [!DNL Channel Manager]](assets/channel-manager-home.png){width="700" zoomable="yes"}

1. Konfigurera ditt [!DNL Walmart Marketplace Seller]-konto om det behövs.

1. Konfigurera arkivet och anslutningen:

   - Välj **[!UICONTROL Add Credentials]**.

   - Välj butiksvyn [!DNL Commerce] som erbjuder de produkter du vill sälja på marknadsplatsen.

     ![Konfigurera anslutning mellan [!DNL Commerce] och [!DNL Walmart Marketplace] från [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png){width="500" zoomable="yes"}

   - Ange en unik **[!UICONTROL store name]**.

   - Välj **[!UICONTROL Adobe [!DNL Commerce] site]** för produktlistor och orderbearbetning.

   - Om du vill få meddelanden relaterade till [!DNL Channel Manager] lägger du till en **[!UICONTROL email address]**.

1. Anslut kanalen till [!DNL Walmart Marketplace].

   - Lägg till autentiseringsuppgifterna för [[!DNL Walmart Marketplace Adobe Production API key]](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) från ditt [!DNL Walmart Marketplace Seller]-konto.

   - Om du inte har autentiseringsuppgifterna kan du hämta dem från [!DNL Walmart Marketplace Developer Portal] genom att välja **[!UICONTROL Get API credentials]**.

     På Developer Portal väljer du region (USA och Kanada) och loggar sedan in.

     ![[!DNL Walmart Marketplace]-kontoinloggning](assets/walmart-marketplace-login-page.png){width="600"}

   - Kopiera och spara värdena **[!UICONTROL Client ID]** och **[!UICONTROL Client Secret]** för [!UICONTROL Adobe Inc Production API key] på API-nyckelformuläret till en säker plats.

     ![[!DNL Walmart Marketplace API key] konfigurationssida ](assets/walmart-api-key-management-form.png){width="600" zoomable="yes"}

     >[!NOTE]
     >
     >Om nyckeln [!DNL Adobe Inc] inte finns med i listan på utvecklarportalen väljer du **[!UICONTROL Add New Key for a Solution Provider]** för att konfigurera behörigheter och generera nyckeln. Mer konfigurationsinformation finns i [Skapa en [!DNL Walmart Marketplace API Key]](walmart-requirements.md#generate-a-walmart-marketplace-api-key).

   - Återgå till [!DNL Channel Manager] om du vill lägga till autentiseringsuppgifterna i informationen **[!UICONTROL Walmart Connection]**.

     När du lägger till autentiseringsuppgifter döljer Adobe klienthemligheten och lagrar värdet i ett säkert valv.

1. Välj **[!UICONTROL Save Store]** om du vill använda konfigurationen och ansluta till [!DNL Walmart marketplace].

1. När anslutningen lyckades [slutförde butiksinställningarna](complete-sales-channel-store-setup.md) från butikssidan **[!UICONTROL Channel Manager]**.

![Konfigurera första arkivet](assets/channel-manager-setup-first-store.png){width="500" zoomable="yes"}

### Felsöka anslutningsproblem

Om anslutningen till [!DNL Walmart] misslyckas finns felsökningstips i [Walmart Marketplace FAQ](https://developer.walmart.com/faq/us/faq-auth/){target="_blank"}.

- Verifiera från [!DNL Walmart Developer Portal] att du har kopierat rätt autentiseringsuppgifter för produktions-API-nyckeln för [!UICONTROL Adobe Inc.]

- Kontrollera att åtkomstkonfigurationen för [!UICONTROL Walmart Adobe API key] har rätt behörigheter. Se [[!DNL Walmart Requirements]](walmart-requirements.md##generate-a-walmart-marketplace-api-key).

- Bekräfta att tjänsten [!DNL Walmart API] är tillgänglig från [Walmart API-statussidan](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target="_blank"}.
