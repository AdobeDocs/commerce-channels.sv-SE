---
title: Hantera attribut för Amazon-listor
description: Du kan hantera mappningen av Commerce produktattribut till Amazon-attributen för att säkerställa korrekt produktinformation mellan systemen.
feature: Sales Channels, Products, Configuration
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Hantera attribut för Amazon-listor

Amazon och [!DNL Commerce] använder båda ett system med produktegenskaper, så kallade attribut, som används för att definiera en produkt. Attribut definierar beskrivning, innehåll, bilder, priser och olika data för dina produkter.

Lyckad kommunikation mellan Commerce och Amazon kräver att [!DNL Commerce]-attribut mappas korrekt (eller matchas) till motsvarande Amazon-attribut. När du integrerar med Amazon mappas dessa attribut till Amazon-attribut. När det är klart kan [!DNL Commerce] synkronisera och underhålla dina Amazon-listor med din [!DNL Commerce]-produktkatalog.

Tänk dig att du har samma objekt i din [!DNL Commerce]-katalog och i dina Amazon-listor. Ett attribut för produkten kan vara artikelns listpris. Namnet på listpriset i [!DNL Commerce] kan ha namnet `Price`, medan listpriset för Amazon kan ha namnet `ListingPrice`. Du måste instruera [!DNL Commerce] att vid kommunikation med Amazon är attributet [!DNL Commerce] med namnet `Price` detsamma som Amazon-attributet med namnet `ListingPrice`. Den här processen kallas _att hantera attribut_ och innefattar att skapa nya och redigera befintliga attribut. Kontrollera att attributen är korrekt matchade för att säkerställa korrekt kommunikation mellan [!DNL Commerce] och Amazon.

När attributmappning har konfigurerats kan [!DNL Commerce] kommunicera produktinformation fram och tillbaka med Amazon. Om du har Amazon produktlistor kan [!DNL Commerce] importera dina Amazon-produkter och information till din [!DNL Commerce]-katalog, så att du kan hantera dina Amazon-listor från en enda central produktkatalog.

Med Amazon försäljningskanal kan du komma åt, granska, skapa och hantera attribut efter behov i [_[!UICONTROL Attributes]_-vyn ](./attributes-view.md) på startsidan för Amazon försäljningskanal. Om du lägger till ett attribut i din [!DNL Commerce]-katalog kan det kräva en uppdatering av dessa värden för alla produkter.

Mer information om attributuppsättningar och värden för [!DNL Commerce] och Amazon finns i:

- [Hantera grundläggande attribut](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html)
- [Skapa ett attribut](./creating-attributes.md#create-an-attribute)
- [Redigera ett befintligt attribut](./creating-attributes.md#edit-an-attribute)
- [Visa attribut](./amazon-matching-attributes-values.md)
- [Redigera eller skapa attributmappning](./amazon-manually-update-incomplete-listing.md)
