---
title: Anmäl dig till Amazon Sales Channel
description: Läs mer om förinstallationsuppgifter, introduktionssteg och hur Amazon fungerar med Amazon Sales Channel i Adobe Commerce och Magento Open Source.
redirect_from: /sales-channels/amazon/amazon-onboarding-home.html
exl-id: 99b64083-36e6-442e-9d20-4676e78ec3ae
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---

# Anmäl dig till Amazon Sales Channel

I det här avsnittet beskrivs förinstallationsuppgifter, steg för introduktion och några viktiga begrepp för hur Amazon fungerar med Amazon försäljningskanal i Adobe Commerce och Magento Open Source.

The [!DNL Amazon Sales Channel] tillägg kan användas i flera Amazon-butiker. För en [!DNL Amazon Seller Central] för Amazon i USA/Kanada/Mexico och skapa tre Amazon-butiker (en för USA:s försäljning, försäljning i Mexiko och försäljning i Kanada). Var och en av de tre butikerna definierar landet när det skapades. Om du har fler än en [!DNL Amazon Seller Central] kan du ha upp till tre Amazon-butiker för var och en av dina [!DNL Amazon Seller Central] konton. Om du även säljer i Storbritannien har du en fjärde Amazon-butik.

>[!TIP]
>
>A [Professionellt säljarkonto](https://sell.amazon.com/){target="_blank"} on [!DNL Amazon Seller Central] in the North America or European (UK) region is required. Amazon charges a monthly subscription and fees for selling. See [Amazon: Choose your selling plan](https://sell.amazon.com/pricing.html){target="_blank"}.<br><br>
>Det är enkelt att komma igång - skapa en butik och anslut den sedan till [!DNL Amazon Seller Central] konto.
>När din butik är ansluten försöker Amazon-kanalen importera dina Amazon-listor och matcha dem med din katalog baserat på din [attributmappning](./attributes-view.md).<br><br>
>Dina inställningar för Amazon-försäljningskanal påverkar dina Amazon-listor. Som standard används din första lista, dina priser och produktinställningar. Du kan ändra dina [lagringsinställningar](./ob-store-review.md) (lista, prissättning, beställning och rapportering) när din butik är ansluten till din [!DNL Amazon Seller Central] konto.

| Steg | Vad som händer |
|--- |--- |
| [Åtgärder före installation](./amazon-pre-setup-tasks.md) | Innan du går med måste du se till att du har en aktiv och godkänd [!DNL Amazon Seller Central] konto. Det finns också några [!DNL Commerce] krav och rekommendationer att slutföra innan introduktionen. |
| [Verifiera Amazon API-nyckeln](./amazon-verify-api-key.md) | Vid åtkomst till Amazon försäljningskanal [!DNL Commerce] kontrollerar och validerar automatiskt Amazon API-nyckeln som du har lagt till i din butikskonfiguration. Om API-nyckeln inte har lagts till eller är ogiltig uppmanas du att [lägg till eller uppdatera din Amazon API-nyckel](./amazon-verify-api-key.md). |
| [Butiksintegrering](./store-integration.md) | I det här steget ska du skapa en Amazon-återförsäljarkanalbutik och sedan ansluta den till din [!DNL Amazon Seller Central] konto. Du behöver de primära inloggningsuppgifterna för din [!DNL Amazon Seller Central] konto (den e-postadress eller telefon som används för att skapa säljarkontot) för det här steget. |
| [Skapa listregel](./ob-create-listing-rule.md) | När du har anslutit din Amazon-butik uppmanas du att skapa en listregel. Det här steget rekommenderas, men du kan även hoppa över det för att starta listimportprocessen. Du kan även komma åt [inställningar för lagring och lista](./ob-store-review.md) i butiken [kontrollpanel](./amazon-store-dashboard.md). |
