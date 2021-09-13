---
title: Om Amazon och Commerce Catalog
description: Amazon försäljningskanal importerar dina Amazon-listor till din Commerce-server och synkroniserar dem kontinuerligt med produkter och försäljning.
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 0%

---

# Om Amazon och katalogen [!DNL Commerce]

Din Adobe Commerce eller Magento Open Source backend innehåller en katalog med alla produkter och tillhörande inställningar och information (bilder, alternativ, priser med mera) samt beställnings- och leveranskonfigurationer. Ditt [!DNL Amazon Seller Central]-konto har också en katalog- och orderkonfiguration som strikt följer din försäljning via [!DNL Amazon Marketplace].

För att hantera och granska produktkatalogen och försäljningen på ett och samma ställe importerar Amazon säljkanal dina Amazon-listor till din [!DNL Commerce]-server, synkroniserar kontinuerligt med produkter och försäljning samt rapporterar problem och trender. Det stöder integreringar med flera [!DNL Amazon Seller Central]-konton och spårar alla data via ett enda gränssnitt för flera butiker.

## Produktattribut

Adobe Commerce och Magento Open Source hanterar katalogsynkroniseringar med hjälp av [attribut](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} för att definiera produktinställningar och data. Amazon använder också attribut som mappas via onboarding. Under [förinställningsuppgifter](./amazon-pre-setup-tasks.md) för Amazon försäljningskanal definierar du ytterligare Amazon-attribut (om det behövs) för att säkerställa korrekta produktmappningar när du importerar dina Amazon-listor till din [!DNL Commerce]-katalog. Dessa attribut omfattar UPC, EAN, ISBN och ASIN ([!DNL Amazon Standard Identification Number]). Genom introduktionen kan du synkronisera produkter mellan Amazon och [!DNL Commerce]-kataloger med dina attribut. Korrekt mappning av dina [!DNL Commerce]- och Amazon-produkter säkerställer en kontinuerlig synkronisering av produktinformation, order och lager.

Om du inte har dessa attribut skapade eller konfigurerade för din katalog bör du lägga till ett [!DNL Commerce] [produktattribut](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} och värden till dina produkter innan du startar programmet. När ett Amazon-attribut importeras kan det användas för sökning, navigering, prisregler och mycket annat. Mer information om dessa attribut finns i [Amazon: Vad är UPC, EAN, ISBN och ASIN?](https://www.amazon.com/gp/seller/asin-upc-isbn-info.html){target=&quot;_blank&quot;}

Efter introduktionen kan du när som helst hantera och uppdatera produktattribut och Amazon-mappningar.

## Produktlistor

En Amazon-lista är en produktsida för varje produkt som du säljer genom [!DNL Amazon Marketplace] med produktbeskrivningar, priser, bilder med mera mappad genom attribut. Under introduktionen kan du konfigurera dina [!DNL Commerce]-produkter så att de automatiskt kan publiceras till Amazon-listor. Du kan även importera dina befintliga Amazon-listor genom att mappa dem till dina [!DNL Commerce]-produkter.

När du har skapat en lista med [!DNL Commerce]-produkter skickas de till Amazon för godkännande. De flesta framgångsrika listorna godkänns inom några timmar. Om din lista är godkänd visas den i [!DNL Amazon Marketplace] för att kunderna ska kunna beställa direkt. Tillägget [!DNL Amazon Sales Channel] innehåller en uppsättning flikar för att granska Amazon-listor. Beroende på problem eller vilka data som krävs bör du granska ditt [!DNL Amazon Seller Central]-konto för att få specifik information om dessa listor.

- [Aktiv](./active-listings.md): Visar godkända produktlistor som är tillgängliga via Marketplace.

- [Lista](./ready-to-list.md): Listar produkter som uppfyller listkraven och som är klara att publiceras till Amazon.

- [Inaktiv](./inactive-listings.md): Listar produkter som inte är tillgängliga på marknaden på grund av att de blockerats av en viss anledning (t.ex. ett brandingproblem), stängts och måste listas om osv.

- [Ej berättigade](./ineligible-listings.md): På grund av listreglerna listas produkter som inte kan listas aktivt på marknadsplatsen (till exempel  `0` kvantitet eller försäljningsdatum).

- [Ofullständig](./incomplete-listings.md): Visar produkter som saknar nödvändig information. Uppdatera produktdata för en annan granskning.

- [Avslutat](./ended-listings.md): Visar en lista över produkter som kan listas i listan men som manuellt tagits bort från Amazon. Du kan ändra listan över de här produkterna.

## Synkroniserar data

Adobe Commerce och Magento Open Source kommunicerar produkt- och orderdata mellan ditt [!DNL Amazon Seller Central]-konto och [!DNL Commerce]-serverdelen. De kontinuerliga uppdateringarna utgör en enda källa via [!DNL Commerce] för att hantera och underhålla era inventeringar, utföra beställningar, spåra försäljningen och minska overheadkostnader och duplicering av arbetet. Rapporteringen innehåller de senaste data för att spåra trender och lösa kommunikationsproblem som fångats upp mellan de två systemen.

All synkronisering hanteras av ett [cron-jobb](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;} som är inställt på att uppdateras var femte minut i [förinställningsuppgifter](./amazon-pre-setup-tasks.md).
