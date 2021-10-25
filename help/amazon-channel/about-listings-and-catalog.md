---
title: Om Amazon och Commerce Catalog
description: Amazon försäljningskanal importerar dina Amazon-listor till din Commerce-server och synkroniserar dem kontinuerligt med produkter och försäljning.
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 0%

---

# Om Amazon och [!DNL Commerce] katalog

Adobe Commerce eller Magento Open Source har en katalog med alla produkter och tillhörande inställningar och information (bilder, alternativ, priser med mera) samt beställnings- och leveranskonfigurationer. Dina [!DNL Amazon Seller Central] kontot har också en katalog- och orderkonfiguration som strikt följer din försäljning via [!DNL Amazon Marketplace].

För att hantera och granska produktkataloger och försäljning på ett och samma ställe importerar Amazon försäljningskanal dina Amazon-listor till [!DNL Commerce] i ryggen, synkroniseras kontinuerligt med produkter och försäljning, och rapporterar problem och trender. Den stöder integrering med flera [!DNL Amazon Seller Central] konton, spåra alla data via ett enda gränssnitt för flera butiker.

## Produktattribut

Adobe Commerce och Magento Open Source hanterar katalogsynkronisering med hjälp av produkten [attributes](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} för att definiera produktinställningar och data. Amazon använder också attribut som mappas via onboarding. Under [förinställningsuppgifter](./amazon-pre-setup-tasks.md) för Amazon försäljningskanal kan du definiera ytterligare Amazon-attribut (om det behövs) för att säkerställa att produktmappningarna är korrekta när du importerar Amazon-listor till dina [!DNL Commerce] katalog. Bland dessa attribut finns UPC, EAN, ISBN och ASIN ([!DNL Amazon Standard Identification Number]). Genom introduktion kan man synka produkter mellan Amazon och [!DNL Commerce] -kataloger med dina attribut. Korrekt mappning av dina [!DNL Commerce] och Amazon-produkter säkerställer en kontinuerlig synkronisering av produktinformation, beställningar och lager.

Om du inte har dessa attribut skapade eller konfigurerade för katalogen bör du lägga till en [!DNL Commerce] [produktattribut](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} och värden för dina produkter före introduktion. När ett Amazon-attribut importeras kan det användas för sökning, navigering, prisregler och mycket annat. Mer information om dessa attribut finns i [Amazon: Vad är UPC, EAN, ISBN och ASIN?](https://www.amazon.com/gp/seller/asin-upc-isbn-info.html){target=&quot;_blank&quot;}

Efter introduktionen kan du när som helst hantera och uppdatera produktattribut och Amazon-mappningar.

## Produktlistor

En Amazon-lista är en produktsida för varje produkt du säljer genom [!DNL Amazon Marketplace], med produktbeskrivningar, priser, bilder med mera mappade genom attribut. Under introduktionen kan du konfigurera [!DNL Commerce] kan automatiskt publiceras i Amazon. Du kan även importera dina befintliga Amazon-listor genom att mappa dem till [!DNL Commerce] produkter.

När du har skapat en lista [!DNL Commerce] de skickas till Amazon för godkännande. De flesta framgångsrika listorna godkänns inom några timmar. Om din lista är godkänd visas den i [!DNL Amazon Marketplace] för direktbeställningar från kunder. The [!DNL Amazon Sales Channel] I finns en uppsättning flikar för att granska Amazon-listor. Beroende på problemet eller vilka data som krävs bör du granska [!DNL Amazon Seller Central] konto för specifik information om dessa listor.

- [Aktiv](./active-listings.md): Visar godkända produktlistor som är tillgängliga via Marketplace.

- [Klar för lista](./ready-to-list.md): Listar produkter som uppfyller listkraven och som är klara att publiceras till Amazon.

- [Inaktiv](./inactive-listings.md): Listar produkter som inte är tillgängliga på marknaden på grund av att de blockerats av en viss anledning (t.ex. ett brandingproblem), stängts och måste listas om osv.

- [Ej giltiga](./ineligible-listings.md): På grund av listreglerna listas produkter som inte kan listas aktivt på marknaden (till exempel `0` antal eller försäljningsdatum).

- [Ofullständig](./incomplete-listings.md): Visar produkter som saknar nödvändig information. Uppdatera produktdata för en annan granskning.

- [Avslutade](./ended-listings.md): Visar en lista över produkter som kan listas i listan men som manuellt tagits bort från Amazon. Du kan ändra listan över de här produkterna.

## Synkroniserar data

Adobe Commerce och Magento Open Source kommunicerar produkt- och orderdata mellan [!DNL Amazon Seller Central] konto och [!DNL Commerce] serverdel. De kontinuerliga uppdateringarna utgör en enda källa via [!DNL Commerce] för att hantera och underhålla lager, utföra beställningar, hålla koll på försäljningen och minska omkostnader och dubbelarbete. Rapporteringen innehåller de senaste data för att spåra trender och lösa kommunikationsproblem som fångats upp mellan de två systemen.

All synkronisering hanteras av en [cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}, inställd på att uppdatera var femte minut i [Åtgärder före installation](./amazon-pre-setup-tasks.md).
