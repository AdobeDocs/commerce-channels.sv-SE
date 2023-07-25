---
title: '''[!DNL Walmart] Krav'
description: '''Verifiera att du har rätt [!DNL Walmart Marketplace]information och resurser som kan integreras med Channel Manager."'
role: Leader, Admin, Developer
feature: Sales Channels, Install, User Account, Tools and External Services
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# [!DNL Walmart] Krav

[!DNL Channel Manager] kräver följande resurser och information för att konfigurera en [!DNL Commerce] försäljningskanal för [!DNL Walmart Marketplace.]

* A [!DNL Walmart] Säljarkonto

* En API-nyckel för att ansluta Adobe Commerce eller Magento Open Source till [!DNL Walmart Marketplace]

  The [!DNL Walmart Marketplace] API-nyckeln möjliggör integrering mellan [!DNL Channel Manager] för Adobe [!DNL Commerce] eller Magento Open Source och Walmart Marketplace. Konfigurera API-nyckeln i Seller Central innan du startar Channel Manager-introduktionsprocessen.

## Konfigurera en [!DNL Walmart Seller] konto

Gå till [!DNL Walmart Seller Center] för att konfigurera [Walmart Seller-konto](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

## Generera en [!DNL Walmart Marketplace] Production API-nyckel

1. Gå till [!DNL Walmart Marketplace] för att generera [API-nyckel för lösningsleverantörsproduktion för Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

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

## [!DNL Walmart Marketplace] Butiksstatus

När du kopplar produkter till marknadsplatsen beror listningstillgängligheten på din status [!DNL Walmart Marketplace] butiker:

* För livebutiker listas dina produkterbjudanden och är tillgängliga för försäljning när matchningen är klar.

* För butiker som inte är direktsända är era erbjudanden testade och inte synliga för kunderna. När [!DNL Walmart Marketplace] butiken publiceras, mellanlagrade listor skickas automatiskt till livebutiken.

![[!DNL Walmart Seller Central] mellanlagrade produkter](assets/walmart-seller-central-staged.png){width="600" zoomable="yes"}

>[!IMPORTANT]
>
>Efter [!DNL Channel Manager] installeras och konfigureras, synkroniseras alla lager-, pris- och orderuppdateringar automatiskt. Anslut inte [!DNL Channel Manager] till en live Walmart Marketplace-butik tills du har inaktiverat andra integreringar som uppdaterar produkt- och orderdata. Om du har konfigurerat andra integreringar kontrollerar du att artikelkvantiteten och priserna [!DNL Commerce] matchar kvantiteterna i [!DNL Walmart Marketplace] innan du ansluter till en livebutik.

