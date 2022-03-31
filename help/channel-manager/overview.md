---
title: Om [!DNL Channel Manager]
description: Lär dig hur du installerar och använder [!DNL Channel Manager] att integrera Adobe Commerce och Magento Open Source butiker med marknadsplatser från tredje part och skapa en försäljningskanal för att hantera marknadsplatslistor, priser, lager och försäljning smidigt från er Commerce Admin.
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: ac084bf968a262dd4e7f6b6040aea2e6dc6197c2
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---

# Översikt

Channel Manager för Adobe Commerce och Magento Open Source har en smidig arbetsyta i Admin för att hantera kanalförsäljning på tredjepartsplatser som Walmart, Amazon och eBay. Öka försäljningen och utöka den till nya marknader samtidigt som ni hanterar säljkanalsåtgärder sömlöst från er Commerce Admin.

![[!DNL Channel Manager] tilläggsadministratörsvy](assets/channel-manager-admin-entry-page.png)

## Betaversion - översikt

Betaversionen av Channel Manager stöder Adobe Commerce- och Magento Open Source-säljare som vill erbjuda produkter på Walmart Marketplace.

Den här versionen har stöd för följande funktioner för att hantera åtgärder för försäljningskanaler:

* Upprätta en API-anslutning mellan Adobe Commerce eller Magento Open Source och Walmart Marketplace

* Publicera produkter från Channel Manager till Walmart med produktmatchning

* Visa produktliststatus i t.ex. Channel Manager *utkast*, *bearbetning*, *matchad*, *fel*.

* Synkronisera lagerkvantiteter för matchade produkter från Commerce till Walmart

* Synkronisera katalogpriser för matchade produkter från Commerce till Walmart

* Ta emot beställningar från Walmart Marketplace och se dem i [!DNL Commerce] kontrollpanel för order

### Förväntad fördröjning för kanalhanteraråtgärder

Datasynkroniseringsprocesserna mellan [!DNL Channel Manager] och en länkad [!DNL Walmart Marketplace] butiken behöver lite tid för att slutföra. Granska den förväntade bearbetningstiden för [!DNL Channel Manager] åtgärder för att planera säljkanalsåtgärder.

**Beräknad fördröjning för kanalhanteraråtgärder**

| **Åtgärd** | **Beskrivning** | **Förväntad fördröjning** |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Lägg till produkter i Channel Manager | Välj produkter i Commerce-produktkatalogen och importera dem till Channel Manager. | **Upp till 5 minuter**-Om du väljer många produkter, till exempel en hel produktkatalog, tar importen längre tid. |
| Matcha produkter på Walmart Marketplace | Välj produktlistor i Channel Manager och skicka till Walmart för matchning. | **Upp till 30 minuter**-Om du väljer många produkter tar matchningsprocessen längre tid beroende på vald kvantitet. |
| Lageruppdateringar | När lagerkvantiteten ändras i Commerce. Channel Manager synkroniserar uppdateringen till Walmart. | **Upp till 10 minuter** |
| Prisuppdateringar | När ett produktpris ändras synkroniserar Channel Manager uppdateringen till Walmart. | **Upp till 5 minuter** |
| Beställa synkroniseringar från Walmart till Commerce | Kunden beställer en Commerce-produkt på Walmart Marketplace. Walmart skickar beställningen till kanalhanteraren. Ordningen visas på orderkontrollpanelen. | **Upp till 30 minuter** |
| Ordern har skapats i Hantering av handelsorder | Kanalhanteraren skapar handelsordern från Walmart-ordern och uppdaterar orderkontrollpanelen så att den innehåller handelsordernumret. | **Upp till 5 minuter** |

## Krav på genomgång

Du behöver följande information från Walmart för att kunna integrera Commerce med Walmart Marketplace:

* Godkännande att sälja på Walmart och inloggningsuppgifter för att logga in på det registrerade Marketplace-säljarkontot

* En API-nyckel för att ansluta Adobe Commerce eller Magento Open Source till Walmart Marketplace

   API-nyckeln Walmart Marketplace gör det möjligt att integrera kanalhanteraren för Adobe Commerce eller Magento Open Source och Walmart Marketplace. Konfigurera API-nyckeln i Seller Central innan du startar Channel Manager-introduktionsprocessen.

### Konfigurera ett Marketplace-säljarkonto

1. [Skicka in din Walmart Seller-app](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI)
2. Efter godkännande från Walmart, [konfigurera ditt Walmart Seller-konto](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

### Generera en Walmart Marketplace-API-nyckel

1. Gå till Walmart Marketplace för att generera en [API-nyckel för lösningsleverantörsproduktion för Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. Skapa nyckeln och konfigurera behörigheter:

   * Välj Adobe som lösningsleverantör.

   * Ange de behörigheter som visas i följande tabell. Mer information finns i [API-autentiseringsuppgifter](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) i *Hjälp för Walmart Marketplace Seller*.

   **Adobe API-nyckelkonfiguration för Walmart**

   | **Behörighet** | **Inställning** |
   |----------------|-------------|
   | Innehåll | Fullständig åtkomst |
   | Hämta feeds | Visa endast |
   | Lager | Fullständig åtkomst |
   | Objekt | Fullständig åtkomst |
   | Sena tiden | Fullständig åtkomst |
   | Order | Fullständig åtkomst |
   | Pris | Fullständig åtkomst |
   | Rapporter | Visa endast |
   | Returnerar | Fullständig åtkomst |
   | Regler | Fullständig åtkomst |
   | Leverans | Fullständig åtkomst |

## Status för Walmart Marketplace Store

När du publicerar produkter på Walmart Marketplace beror tillgängligheten på status för dina Walmart Marketplace-butiker:

* För livebutiker listas dina erbjudanden och kan köpas så snart matchningen är klar.

* För butiker som inte är direktsända är era erbjudanden testade och inte synliga för kunderna. Så snart butiken blir offentlig skickas alla mellanlagrade listor automatiskt till den publicerade butiken.


![[!DNL Walmart Seller Central] mellanlagrade produkter](assets/walmart-seller-central-staged.png)
