---
title: Hantera attribut
description: Du kan hantera mappningen av Commerce-produktattribut till Amazon-attribut för att säkerställa korrekt produktinformation mellan systemen.
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Hantera attribut

Amazon och [!DNL Commerce] använder båda ett system med produktegenskaper, så kallade attribut, som används för att definiera en produkt. Attribut definierar beskrivning, innehåll, bilder, priser och olika data för dina produkter.

Kommunikationen mellan Commerce och Amazon kräver att [!DNL Commerce]-attribut mappas korrekt (eller matchas) till motsvarande Amazon-attribut. När du integrerar med Amazon mappas dessa attribut till Amazon-attribut. När det är klart kan [!DNL Commerce] synkronisera och underhålla dina Amazon-listor med din [!DNL Commerce]-produktkatalog.

Tänk dig att du har samma objekt i [!DNL Commerce]-katalogen och i Amazon-listorna. Ett attribut för produkten kan vara artikelns listpris. Namnet på listpriset i [!DNL Commerce] kan vara `Price`, medan listpriset för Amazon kan vara `ListingPrice`. Du måste instruera [!DNL Commerce] att vid kommunikation med Amazon är [!DNL Commerce]-attributet `Price` detsamma som Amazon-attributet `ListingPrice`. Den här processen kallas _hantering av attribut_ och innehåller även skapande av nya och redigering av befintliga attribut. Kontrollera att attributen är korrekt matchade för att säkerställa korrekt kommunikation mellan [!DNL Commerce] och Amazon.

När attributmappning är inställd kan [!DNL Commerce] kommunicera produktinformation fram och tillbaka med Amazon. Om du har Amazon produktlistor kan [!DNL Commerce] importera dina Amazon-produkter och -information till din [!DNL Commerce]-katalog, så att du kan hantera dina Amazon-listor från en enda central produktkatalog.

Med Amazon försäljningskanal kan du komma åt, granska, skapa och hantera attribut efter behov i [_[!UICONTROL Attributes]_-vyn](./attributes-view.md) på startsidan för Amazon försäljningskanal. Om du lägger till ett attribut i din [!DNL Commerce]-katalog kan det kräva en uppdatering av dessa värden för alla produkter.

Mer information om [!DNL Commerce] och Amazon-attributuppsättningar och -värden finns i:

- [Hantera grundläggande attribut](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}
- [Skapa ett attribut](./creating-attributes.md#create-an-attribute)
- [Redigera ett befintligt attribut](./creating-attributes.md#edit-an-attribute)
- [Visa attributmappning](./amazon-matching-attributes-values.md)
- [Redigera eller skapa attributmappning](./amazon-manually-update-incomplete-listing.md)
