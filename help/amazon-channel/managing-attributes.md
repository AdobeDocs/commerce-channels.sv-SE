---
title: Hantera attribut för Amazon-listor
description: Du kan hantera mappningen av Commerce-produktattribut till Amazon-attribut för att säkerställa korrekt produktinformation mellan systemen.
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Hantera attribut för Amazon-listor

Amazon och [!DNL Commerce] båda använder ett system med produktegenskaper, så kallade attribut, som används för att definiera en produkt. Attribut definierar beskrivning, innehåll, bilder, priser och olika data för dina produkter.

Kommunikationen mellan Commerce och Amazon kräver att [!DNL Commerce] attribut mappas korrekt (eller matchas) till motsvarande Amazon-attribut. När du integrerar med Amazon mappas dessa attribut till Amazon-attribut. När det är klart [!DNL Commerce] kan synka och underhålla dina Amazon-listor med [!DNL Commerce] produktkatalog.

Tänk dig att du har samma objekt i [!DNL Commerce] kataloger och Amazon-listor. Ett attribut för produkten kan vara artikelns listpris. Namnet på listpriset i [!DNL Commerce] kan ha ett namn `Price`, medan listpriset för Amazon kan namnges `ListingPrice`. Du måste instruera [!DNL Commerce] när du kommunicerar med Amazon [!DNL Commerce] attribute named `Price` är samma som Amazon-attributet med namnet `ListingPrice`. Den här processen anropas _hantera attribut_ och innehåller även funktioner för att skapa nya och redigera befintliga attribut. Se till att attributen matchar varandra på rätt sätt för att säkerställa korrekt kommunikation mellan [!DNL Commerce] och Amazon.

När attributmappning är inställd, [!DNL Commerce] kan kommunicera produktinformation fram och tillbaka med Amazon. Om du har Amazon produktlistor [!DNL Commerce] kan importera dina Amazon-produkter och -detaljer till [!DNL Commerce] -katalog så att du kan hantera dina Amazon-listor från en enda central produktkatalog.

Med Amazon försäljningskanal kan du komma åt, granska, skapa och hantera attribut efter behov i [_[!UICONTROL Attributes]_visa](./attributes-view.md) på startsidan för Amazon försäljningskanal. Om du lägger till ett attribut i [!DNL Commerce] kan det kräva en uppdatering av dessa värden för alla produkter.

Mer information om [!DNL Commerce] och Amazon-attributuppsättningar och -värden, se:

- [Hantera grundläggande attribut](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html)
- [Skapa ett attribut](./creating-attributes.md#create-an-attribute)
- [Redigera ett befintligt attribut](./creating-attributes.md#edit-an-attribute)
- [Visa attributmappning](./amazon-matching-attributes-values.md)
- [Redigera eller skapa attributmappning](./amazon-manually-update-incomplete-listing.md)
