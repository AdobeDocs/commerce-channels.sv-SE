---
title: Krav för Walmart
description: Kontrollera att du har den Walmart Marketplace-information och de resurser du behöver för att integrera med Channel Manager.
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: e6368d30e16ccffcb1dfc64bdd56561116934b54
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Krav på genomgång

Channel Manager kräver följande resurser och information för att konfigurera en Commerce-försäljningskanal för Walmart Marketplace.

* Godkännande att sälja på Walmart och inloggningsuppgifter för att logga in på det registrerade Marketplace-säljarkontot

* En API-nyckel för att ansluta Adobe Commerce eller Magento Open Source till Walmart Marketplace

   API-nyckeln Walmart Marketplace gör det möjligt att integrera kanalhanteraren för Adobe Commerce eller Magento Open Source och Walmart Marketplace. Konfigurera API-nyckeln i Seller Central innan du startar Channel Manager-introduktionsprocessen.

## Konfigurera ett Marketplace-säljarkonto

1. [Skicka in din Walmart Seller-app](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI).
1. Efter godkännande från Walmart, [konfigurera ditt Walmart Seller-konto](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

## Generera en Walmart Marketplace Production API-nyckel

1. Gå till Walmart Marketplace för att generera en [API-nyckel för lösningsleverantörsproduktion för Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. Skapa nyckeln och konfigurera behörigheter:

   * Välj Adobe som lösningsleverantör.

   * Ange de behörigheter som visas i följande tabell. Mer information finns i [API-autentiseringsuppgifter](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) i _Hjälp för Walmart Marketplace Seller_.

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

* För livebutiker listas dina produkterbjudanden och är tillgängliga för försäljning när matchningen är klar.

* För butiker som inte är direktsända är era erbjudanden testade och inte synliga för kunderna. När butiken publiceras skickas alla mellanlagrade listor automatiskt till den aktiva butiken.

![[!DNL Walmart Seller Central] mellanlagrade produkter](assets/walmart-seller-central-staged.png)
