---
title: Bästa praxis och begränsningar för  [!DNL Amazon sales channel]
description: Läs om de bästa metoderna och begränsningarna när du använder Amazon försäljningskanal för Adobe Commerce och Magento Open Source.
role: Leader, Admin, User
feature: Sales Channels, Best Practices
exl-id: 7f7faae1-7aa7-413c-b534-1039e6a35173
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Bästa praxis och begränsningar för [!DNL Amazon sales channel]

De bästa sätten är att

- Amazon försäljningskanal kan påverka dina Amazon-listor genom att öka eller minska priser, synkronisera produktinformation (inklusive tillgängligt lager) samt lägga till, uppdatera och avsluta (ta bort) listor. Granska dina listor efter status under installationen och justera inställningarna ([listinställningar](./listing-settings.md), [listregler](./listing-rules.md), [prisregler](./pricing-products.md), [åsidosättningar](./overrides.md) och så vidare) innan du slutför din butiksinställning. Dessa inställningar kan även ändras efter installationen, efter behov.

- Amazon försäljningskanal kan ange prisregler för att automatiskt justera ditt listpris. Automatiska prisskyddsfunktioner inkluderar funktionerna [lägsta pris](./floor-price.md) och [valfritt tak](./optional-ceiling-price.md) i [Intelligenta omprisregler](./intelligent-repricing-rules.md). Med hjälp av dessa skyddsmekanismer kan du säkerställa att dina listpriser inte hamnar under din kostnad eller över ett definierat pris.

- Datasynkronisering mellan Amazon försäljningskanal och Amazon styrs av dina [[!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html) -inställningar. Inbyggd begränsning mellan [!DNL Commerce] och Amazon bidrar till att säkerställa en smidig och effektiv dataöverföring, men under e-handelstrafiktider (som Black Friday) kan Amazon system ta längre tid än vanligt att uppdatera. Ställ in din [!DNL Commerce]-kron så att den körs en gång var femte minut.

- Amazon försäljningskanal importerar din beställningsinformation från Amazon. Om du vill hantera dina Amazon-beställningar i Amazon försäljningskanal måste du se till att dina [orderinställningar](./order-settings.md) är definierade för import och skapa en motsvarande [!DNL Commerce]-ordning för varje Amazon-beställning. Om det inte är definierat kan du bara se din beställningsinformation från Amazon. Alla skatter för försäljning via Amazon hanteras och remitteras fortfarande via ditt [!DNL Amazon Seller Central]-konto. I vissa delstater måste Amazon automatiskt ta ut och återbetala skatter. För andra delstater har säljarna möjlighet att beräkna skatter manuellt eller automatiskt. Se [Amazon: Skattepolicyer](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&amp;language=en_US/){target="_blank"}. Du kanske måste logga in på ditt [!DNL Amazon Seller Central]-konto för att kunna visa Amazon skattepolicydokumentation.

- För regioner i Storbritannien är det bäst att registrera sig i [Amazon momskalkylningstjänst](https://sell.amazon.co.uk/learn/vat-resources/){target="_blank"} innan du börjar prenumerera på Amazon försäljningskanal.

  >[!NOTE]
  >
  >Det kan ta 10-14 dagar för Amazon att verifiera och aktivera momsberäkningstjänstkontot.

Begränsningarna är:

- Paket, presentkort och grupperade produkttyper som ingår i din [!DNL Commerce]-katalog stöds inte av Amazon försäljningskanal för notering till Amazon.

- Amazon försäljningskanal kan inte skapa en lista för en produkt som inte har en befintlig eller tidigare Amazon-lista. Om en produkt inte finns i [!DNL Amazon Seller Central] med ett ASIN måste den läggas till i [!DNL Amazon Seller Central] så att Amazon kan tilldela produkten ett ASIN. När en produkt har lagts till i Amazon och en lista har skapats kan den matchas mot din katalog i Amazon försäljningskanal och synkroniseras.
