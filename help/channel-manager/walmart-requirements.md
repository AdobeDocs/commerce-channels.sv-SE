---
title: '"[!DNL Walmart] Krav"'
description: '"Kontrollera att du har rätt[!DNL Walmart Marketplace]information och resurser som kan integreras med Channel Manager."'
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: fffbdac54443b7b9bed8854eba8341446e78cc80
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# [!DNL Walmart] krav

[!DNL Channel Manager] kräver följande resurser och information för att konfigurera en [!DNL Commerce] försäljningskanal för [!DNL Walmart Marketplace.]

* Godkännande att sälja vidare [!DNL Walmart] och inloggningsuppgifter för det registrerade Marketplace-säljarkontot

* En API-nyckel för att ansluta Adobe Commerce eller Magento Open Source till [!DNL Walmart Marketplace]

   The [!DNL Walmart Marketplace] API-nyckeln möjliggör integrering mellan [!DNL Channel Manager] för Adobe Commerce eller Magento Open Source och Walmart Marketplace. Konfigurera API-nyckeln i Seller Central innan du startar Channel Manager-introduktionsprocessen.

## Konfigurera ett Marketplace-säljarkonto

1. [Skicka in din Walmart Seller-app](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI).
1. Efter godkännande från [!DNL Walmart], [konfigurera ditt Walmart Seller-konto](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

## Generera en [!DNL Walmart Marketplace] Production API-nyckel

1. Gå till [!DNL Walmart Marketplace]för att generera [API-nyckel för lösningsleverantörsproduktion för Adobe](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

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

När du publicerar produkter på marknaden beror listtillgängligheten på din status [!DNL Walmart Marketplace] butiker:

* För livebutiker listas dina produkterbjudanden och är tillgängliga för försäljning när matchningen är klar.

* För butiker som inte är direktsända är era erbjudanden testade och inte synliga för kunderna. När [!DNL Walmart Marketplace] butiken publiceras, mellanlagrade listor skickas automatiskt till livebutiken.

![[!DNL Walmart Seller Central] mellanlagrade produkter](assets/walmart-seller-central-staged.png)