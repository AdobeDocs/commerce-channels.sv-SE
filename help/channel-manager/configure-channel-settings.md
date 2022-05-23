---
title: Konfigurera kanalinställningar
description: Konfigurera kanalhanteraren och inställningarna för försäljningskanal för autentisering, mappa katalogattribut och transportföretag som krävs för att koordinera säljåtgärder mellan [!DNL Commerce] och [!DNL Walmart Marketplace].
source-git-commit: d819af5c0b03094fe208c5e8e95d524ebdac7aa9
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# Konfigurera inställningar för försäljningskanal

Försäljningskanalsinställningarna möjliggör kommunikation och datasynkronisering mellan [!DNL Commerce] och [!DNL Walmart Marketplace] så att du kan hantera Walmart Marketplace-säljåtgärder från [!DNL Commerce] Administratör:

I [!DNL Channel Manager]konfigurerar du vissa inställningar för försäljningskanaler under introduktionsprocessen. Efter introduktionen kan du visa och hantera konfigurationen av inställningarna på *Inställningar* sida.

* **[Mappa unika identifierare](map-catalog-attributes.md)**-Innan du publicerar listor från [!DNL Commerce] till [!DNL Walmart Marketplace]mappa minst en unik identifierare från [!DNL Commerce] katalog till motsvarande identifierare från Walmart. Det här steget krävs för att matcha [!DNL Commerce] produkter till befintliga [!DNL Walmart] listor och synkronisera produktdata mellan [!DNL Commerce] och [!DNL Walmart].

* **[Kartlägg transportföretag](map-shipping-carriers.md)**-Innan du bearbetar [!DNL Walmart Marketplace] order från [!DNL Commerce]ser du till att kartlägga fraktföretag från [!DNL Commerce] instans till motsvarande bärare på [!DNL Walmart Marketplace].

* **WWART API-autentiseringsuppgifter**-Under [!DNL Channel Manager] introduktionsprocessen, du anger [Walmart API-autentiseringsuppgifter](walmart-prerequisites.md#generate-a-walmart-marketplace-production-api-key) från ditt Walmart Marketplace-säljarkonto för att ansluta [!DNL Commerce] till [!DNL Walmart Marketplace] för kommunikation och datasynkronisering. Om det behövs kan du uppdatera dessa uppgifter från *Inställningar* sida.
