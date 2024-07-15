---
title: '[!DNL Walmart] krav'
description: '''Verifiera att du har den information och de resurser som krävs för att integrera med Channel Manager.'' [!DNL Walmart Marketplace]'
role: Leader, Admin, Developer
feature: Sales Channels, Install, User Account, Tools and External Services
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# Krav för [!DNL Walmart]

[!DNL Channel Manager] kräver följande resurser och information för att konfigurera en [!DNL Commerce]-försäljningskanal för [!DNL Walmart Marketplace.]

* Ett [!DNL Walmart]-säljarkonto

* En API-nyckel för att ansluta Adobe Commerce eller Magento Open Source till [!DNL Walmart Marketplace]

  API-nyckeln [!DNL Walmart Marketplace] gör det möjligt att integrera [!DNL Channel Manager] för Adobe [!DNL Commerce] eller Magento Open Source och Walmart Marketplace. Konfigurera API-nyckeln i Seller Central innan du startar Channel Manager-introduktionsprocessen.

## Konfigurera ett [!DNL Walmart Seller]-konto

Gå till [!DNL Walmart Seller Center] för att konfigurera ditt [Walmart Seller-konto](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

## Generera en [!DNL Walmart Marketplace]-produktions-API-nyckel

1. Gå till [!DNL Walmart Marketplace] om du vill generera en [API-nyckel för lösningsproviderproduktion för Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. Skapa nyckeln och konfigurera behörigheter:

   * Välj Adobe som lösningsleverantör.

   * Ange de behörigheter som visas i följande tabell. Mer information finns i [API-autentiseringsuppgifter](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) i hjälpen för _Walmart Marketplace-säljaren_.

   **Adobe API-nyckelkonfiguration för Walmart**

   | **Behörighet** | **Inställning** |
   |----------------|-------------|
   | Innehåll | Fullständig åtkomst |
   | Hämta feeds | Visa endast |
   | Lager | Fullständig åtkomst |
   | Objekt | Fullständig åtkomst |
   | Sena tiden | Fullständig åtkomst |
   | Beställning | Fullständig åtkomst |
   | Pris | Fullständig åtkomst |
   | Rapporter | Visa endast |
   | Returnerar | Fullständig åtkomst |
   | Regler | Fullständig åtkomst |
   | Leverans | Fullständig åtkomst |

## [!DNL Walmart Marketplace] Butiksstatus

När du ansluter produkter till Marketplace beror tillgängligheten på statusen för dina [!DNL Walmart Marketplace]-butiker:

* För livebutiker listas dina produkterbjudanden och är tillgängliga för försäljning när matchningen är klar.

* För butiker som inte är direktsända är era erbjudanden testade och inte synliga för kunderna. När [!DNL Walmart Marketplace]-butiken blir aktiv skickas mellanlagrade listor automatiskt till live-butiken.

![[!DNL Walmart Seller Central] mellanlagrade produkter](assets/walmart-seller-central-staged.png){width="600" zoomable="yes"}

>[!IMPORTANT]
>
>När [!DNL Channel Manager] har installerats och konfigurerats synkroniseras alla lager-, pris- och orderuppdateringar automatiskt. Anslut inte [!DNL Channel Manager] till ett live Walmart Marketplace-arkiv förrän du har inaktiverat andra integreringar som uppdaterar produkten och beställer data. Om du har konfigurerat andra integreringar kontrollerar du att artikelkvantiteten och priserna i [!DNL Commerce] matchar kvantiteterna i [!DNL Walmart Marketplace] innan du ansluter till en live-butik.

