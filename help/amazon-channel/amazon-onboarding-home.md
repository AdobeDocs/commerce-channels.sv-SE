---
title: Anmäl dig till Amazon Sales Channel
description: 'Läs mer om förinstallationsuppgifter, introduktionssteg och hur Amazon fungerar med Amazon Sales Channel i Adobe Commerce och Magento Open Source.'
redirect_from: /sales-channels/amazon/amazon-onboarding-home.html: 
exl-id: 99b64083-36e6-442e-9d20-4676e78ec3ae
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 418
ht-degree: 0%

---

# Införliva Amazon försäljningskanal

I det här avsnittet beskrivs förinstallationsuppgifter, steg för introduktion och några viktiga begrepp för hur Amazon fungerar med Amazon försäljningskanal i Adobe Commerce och Magento Open Source.

Tillägget [!DNL Amazon Sales Channel] har stöd för flera Amazon-butiker. Skapa tre Amazon-butiker (en för försäljning i USA, Mexiko och Kanada) för ett enda [!DNL Amazon Seller Central]-konto i Amazon-regionen USA/Kanada/Mexiko. Var och en av de tre butikerna definierar landet när det skapades. Om du har fler än ett [!DNL Amazon Seller Central]-konto kan du ha upp till tre Amazon-butiker för varje [!DNL Amazon Seller Central]-konto. Om du även säljer i Storbritannien har du en fjärde Amazon-butik.

>[!TIP]
>
>Ett [Professional-säljarkonto](https://sell.amazon.com/){target=&quot;_blank&quot;} på [!DNL Amazon Seller Central] i Nordamerika eller Europa (UK) krävs. Amazon debiterar en månadsprenumeration och tar ut avgifter för försäljningen. Se [Amazon: Välj din säljplan](https://sell.amazon.com/pricing.html){target=&quot;_blank&quot;}.<br><br>
>Det är enkelt att komma igång - skapa en butik och anslut den sedan till ditt [!DNL Amazon Seller Central]-konto.
>När din butik är ansluten försöker Amazon-kanalen importera dina Amazon-listor och matcha dem med din katalog utifrån din [attributmappning](./attributes-view.md).<br><br>
>Dina inställningar för Amazon-försäljningskanal påverkar dina Amazon-listor. Som standard används din första lista, dina priser och produktinställningar. Du kan ändra dina [butiksinställningar](./ob-store-review.md) (lista, prissättning, order och rapportering) när butiken är ansluten till ditt [!DNL Amazon Seller Central]-konto.

| Steg | Vad som händer |
|--- |--- |
| [Åtgärder före installation](./amazon-pre-setup-tasks.md) | Innan du går med måste du se till att du har ett aktivt och godkänt [!DNL Amazon Seller Central]-konto. Det finns också [!DNL Commerce] krav och rekommendationer att slutföra innan introduktionen. |
| [Verifiera Amazon API-nyckeln](./amazon-verify-api-key.md) | När du använder Amazon försäljningskanal kontrollerar och validerar [!DNL Commerce] automatiskt den Amazon API-nyckel som du har lagt till i din butikskonfiguration. Om API-nyckeln inte har lagts till eller är ogiltig uppmanas du att [lägga till eller uppdatera Amazon API-nyckeln](./amazon-verify-api-key.md). |
| [Butiksintegrering](./store-integration.md) | I det här steget ingår att skapa en Amazon-försäljningskanalbutik och sedan ansluta den till ditt [!DNL Amazon Seller Central]-konto. Du behöver de primära inloggningsuppgifterna för ditt [!DNL Amazon Seller Central]-konto (e-postadressen eller telefonen som används för att skapa säljarkontot) för det här steget. |
| [Skapa listregel](./ob-create-listing-rule.md) | När du har anslutit din Amazon-butik uppmanas du att skapa en listregel. Det här steget rekommenderas, men du kan även hoppa över det för att starta listimportprocessen. Du kan även komma åt dina [inställningar för arkiv och lista](./ob-store-review.md) på butiken [kontrollpanelen](./amazon-store-dashboard.md). |
