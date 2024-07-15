---
title: Amazon och Commerce-katalogen
description: Amazon försäljningskanal importerar dina Amazon-listor till din Commerce-server och synkroniserar dem kontinuerligt med produkter och försäljning.
role: Leader, Admin, User
feature: Sales Channels, Integration, Tools and External Services, Merchandising, Catalog Management
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# Amazon och [!DNL Commerce]-katalogen

Adobe Commerce eller Magento Open Source har en katalog med alla produkter och tillhörande inställningar och information (bilder, alternativ, priser med mera) samt beställnings- och leveranskonfigurationer. Ditt [!DNL Amazon Seller Central]-konto har också en katalog- och orderkonfiguration som strikt följer din försäljning via [!DNL Amazon Marketplace].

För att du bättre ska kunna hantera och granska din produktkatalog och försäljning på en och samma plats, importerar Amazon säljkanal dina Amazon-listor till din [!DNL Commerce]-server, synkroniserar kontinuerligt med produkter och försäljning samt rapporterar problem och trender. Den stöder integreringar med flera [!DNL Amazon Seller Central]-konton och spårar alla data via ett enda gränssnitt för flera butiker.

## Produktattribut

Adobe Commerce och Magento Open Source hanterar katalogsynkroniseringar med hjälp av [attribut](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) för produkten för att definiera produktinställningar och data. Amazon använder också attribut som mappas via onboarding. Under [förinställningsaktiviteter](./amazon-pre-setup-tasks.md) för Amazon-försäljningskanal definierar du ytterligare Amazon-attribut (om det behövs) för att säkerställa korrekta produktmappningar när du importerar dina Amazon-listor till din [!DNL Commerce]-katalog. Dessa attribut omfattar UPC, EAN, ISBN och ASIN ([!DNL Amazon Standard Identification Number]). Genom introduktionen kan du synkronisera produkter mellan Amazon och [!DNL Commerce]-kataloger med dina attribut. Korrekt mappning av dina [!DNL Commerce]- och Amazon-produkter säkerställer en kontinuerlig synkronisering av produktinformation, order och lager.

Om du inte har dessa attribut skapade eller konfigurerade för din katalog bör du lägga till ett [!DNL Commerce] [product attribute](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) och värden till dina produkter innan du påbörjar introduktionen. När ett Amazon-attribut importeras kan det användas för sökning, navigering, prisregler och mycket annat. Se [Vad betyder ASIN, UPC, EAN, ISBN, SKU och andra streckkoder?](https://sellerskills.com/multi-channel-operations/what-asin-upc-ean-isbn-sku-and-other-barcodes-mean/#what-is-isbn-number){target="_blank"}

Efter introduktionen kan du när som helst hantera och uppdatera produktattribut och Amazon-mappningar.

## Produktlistor

En Amazon-lista är en produktsida för varje produkt som du säljer genom [!DNL Amazon Marketplace] med produktbeskrivningar, priser, bilder och annat mappat genom attribut. Under introduktionen kan du konfigurera dina [!DNL Commerce]-produkter så att de automatiskt kan publiceras till Amazon-listor. Du kan även importera dina befintliga Amazon-listor genom att mappa dem till dina [!DNL Commerce]-produkter.

När du har skapat en lista över [!DNL Commerce] produkter skickas de till Amazon för godkännande. De flesta framgångsrika listorna godkänns inom några timmar. Om din lista är godkänd visas den i [!DNL Amazon Marketplace] för omedelbar beställning från kunder. Tillägget [!DNL Amazon Sales Channel] innehåller en uppsättning flikar för att granska Amazon-listor. Beroende på problemet eller vilka data som krävs bör du granska ditt [!DNL Amazon Seller Central]-konto för att få mer information om dessa listor.

- [Aktiv](./active-listings.md): Visar godkända produktlistor som är tillgängliga via Marketplace.

- [Klar att listas](./ready-to-list.md): Visar produkter som uppfyller kraven för listregler och är klara att publiceras till Amazon.

- [Inaktiv](./inactive-listings.md): Visar produkter som inte är tillgängliga på marknadsplatsen på grund av att de blockerats av en viss anledning (till exempel branding-problem), stängts och måste listas om osv.

- [Ej berättigade](./ineligible-listings.md): På grund av listreglerna listas produkter som inte kan listas aktivt på marknadsplatsen (till exempel `0` kvantitet eller försäljningsdatum).

- [Ofullständig](./incomplete-listings.md): Visar produkter som saknar nödvändig information. Uppdatera produktdata för en annan granskning.

- [Avslutad](./ended-listings.md): Visar en lista över produkter som kan listas men tas bort manuellt från Amazon. Du kan ändra listan över de här produkterna.

## Synkroniserar data

Adobe Commerce och Magento Open Source kommunicerar produkt- och orderdata mellan ditt [!DNL Amazon Seller Central]-konto och [!DNL Commerce]-serverdelen. De kontinuerliga uppdateringarna tillhandahåller en enda källa via [!DNL Commerce] för att hantera och underhålla dina lager, utföra beställningar, spåra försäljningen och minska overheadkostnader och duplicering av arbetet. Rapporteringen innehåller de senaste data för att spåra trender och lösa kommunikationsproblem som fångats upp mellan de två systemen.

All synkronisering hanteras av ett [cron-jobb](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html) som är inställt på att uppdateras var femte minut i dina [förinställda uppgifter](./amazon-pre-setup-tasks.md).
