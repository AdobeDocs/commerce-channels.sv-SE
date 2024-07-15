---
title: "Inbyggt [!DNL Amazon Sales Channel]"
description: Läs mer om förinstallationsuppgifter, introduktionssteg och hur Amazon fungerar med Amazon Sales Channel i Adobe Commerce och Magento Open Source.
role: Leader, Admin, User
feature: Sales Channels, Integration, Tools and External Services
exl-id: 99b64083-36e6-442e-9d20-4676e78ec3ae
source-git-commit: 6321f17c0e6f9e86bb3f5755dc7710fa68d68b0d
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Inbyggt [!DNL Amazon Sales Channel]

I det här avsnittet beskrivs förinstallationsuppgifter, steg för introduktion och några viktiga begrepp för hur Amazon fungerar med Amazon försäljningskanal i Adobe Commerce och Magento Open Source.

Tillägget [!DNL Amazon Sales Channel] stöder flera Amazon-butiker. Skapa tre Amazon-butiker (en för försäljning i USA, Mexiko och Kanada) för ett enda [!DNL Amazon Seller Central]-konto som finns i Amazon-regionen USA/Kanada/Mexiko. Var och en av de tre butikerna definierar landet när det skapades. Om du har fler än ett [!DNL Amazon Seller Central]-konto kan du ha upp till tre Amazon-butiker för vart och ett av dina [!DNL Amazon Seller Central]-konton. Om du även säljer i Storbritannien har du en fjärde Amazon-butik.

>[!TIP]
>
>Ett [Professional-säljarkonto](https://sell.amazon.com/){target="_blank"} på [!DNL Amazon Seller Central] i Nordamerika eller Europa (Storbritannien) krävs. Amazon debiterar en månadsprenumeration och tar ut avgifter för försäljningen. Se [Amazon: Välj din försäljningsplan](https://sell.amazon.com/pricing.html){target="_blank"}.<br><br>
>Det är enkelt att komma igång - skapa din butik och anslut den sedan till ditt [!DNL Amazon Seller Central]-konto.
>När din butik är ansluten försöker Amazon-kanalen importera dina Amazon-listor och matcha dem med din katalog baserat på din [attributmappning](./attributes-view.md).<br><br>
>Dina inställningar för Amazon-försäljningskanal påverkar dina Amazon-listor. Som standard används din första lista, dina priser och produktinställningar. Du kan ändra dina [butiksinställningar](./ob-store-review.md) (lista, prissättning, ordning och rapportering) när butiken har anslutit till ditt [!DNL Amazon Seller Central]-konto.

| Steg | Vad som händer |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Förinställda uppgifter](./amazon-pre-setup-tasks.md) | Innan du går med måste du se till att du har ett aktivt och godkänt [!DNL Amazon Seller Central]-konto. Det finns även några [!DNL Commerce] krav och rekommendationer att slutföra innan du börjar använda programmet. |
| [Verifiera Amazon API-nyckeln](./amazon-verify-api-key.md) | När du använder Amazon-försäljningskanal kontrollerar och validerar [!DNL Commerce] automatiskt den Amazon API-nyckel som du har lagt till i din butikskonfiguration. Om API-nyckeln inte har lagts till eller är ogiltig uppmanas du att [lägga till eller uppdatera Amazon API-nyckeln](./amazon-verify-api-key.md). |
| [Butiksintegrering](./store-integration.md) | I det här steget ingår att skapa en Amazon-försäljningskanalbutik och sedan ansluta den till ditt [!DNL Amazon Seller Central]-konto. Du behöver de primära inloggningsuppgifterna för ditt [!DNL Amazon Seller Central]-konto (e-postadressen eller telefonen som används för att skapa säljarkontot) för det här steget. |
| [Skapa listregel](./ob-create-listing-rule.md) | När du har anslutit din Amazon-butik uppmanas du att skapa en listregel. Det här steget rekommenderas, men du kan även hoppa över det för att starta listimportprocessen. Du kan även komma åt dina [butiks- och listinställningar](./ob-store-review.md) på [instrumentpanelen](./amazon-store-dashboard.md) för butiken. |
