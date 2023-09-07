---
title: '''[!DNL Amazon Sales Channel] versionsinformation'
description: Läs versionsinformationen om du vill ha information om alla [!DNL Amazon Sales Channel] releaser.
feature: Sales Channels, Release Notes
exl-id: 792782e0-9097-42f7-9fc0-509ece02e407
source-git-commit: df8bbec23d34b53a0e694c924aca5b1ed41e4d08
workflow-type: tm+mt
source-wordcount: '2024'
ht-degree: 0%

---

# [!DNL Amazon Sales Channel] versionsinformation

>[!IMPORTANT]
>
> [!DNL Amazon sales channel] kan installeras på instanser med Magento Open Source, Adobe Commerce och Adobe Commerce i molninfrastrukturversionerna 2.3.x och 2.4.x. Tillägget stöds inte längre i Adobe Commerce 2.1, Magento Open Source 2.2 eller Magento 1.
> <br>Support finns för [!DNL Amazon sales channel]  version 4.0.0 och 4.1.0 endast i Adobe Commerce 2.3.x.
> <br>[!DNL Amazon sales channel] version 4.2.0+ är kompatibel med Adobe Commerce 2.3.x, men support finns endast för Adobe Commerce 2.4.x-versioner.
>

I versionsinformationen beskrivs den första versionen av [!DNL Amazon sales channel] och innehåller:

![Nytt](../assets/new.svg) Nya funktioner
![Korrigerat problem](../assets/fix.svg) Korrigeringar och förbättringar
![Känt fel](../assets/bug.svg) Kända fel

Se [Kommande versioner](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) för versionshantering, support och kompatibilitet.

Se [Produkttillgänglighet](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) om du vill veta vilka Adobe Commerce-versioner som stöder det här tillägget.

## v4.5.0

*30 augusti 2023*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg) API-gatewayen Adobe.IO har lagts till, från MAGI, för förbättrad autentiseringssäkerhet. `ServicesId` har ett nytt användargränssnitt för att hantera dina Adobe.IO-inloggningsuppgifter, liknande andra [Adobe Commerce Services](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html).

>[!NOTE]
>
>Handlarna måste se till att [privata och offentliga API-nycklar](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html) uppdateras för produktion.


![Korrigerat problem](../assets/fix.svg) Identifierade ett konfigurationsinställningsproblem och åtgärdade orderskapandeflödet.

## v4.4.4

*7 mars 2023*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Korrigerat problem](../assets/fix.svg) Stöd för Adobe Commerce 2.4.6 och PHP 8.2 har lagts till.

![Korrigerat problem](../assets/fix.svg) Minskat brus i loggar.

![Korrigerat problem](../assets/fix.svg) Förbättrad stabilitet vid uppdatering.

![Korrigerat problem](../assets/fix.svg) Förenklade processen för att köra en enda åtgärdsliknande pull eller för att ansöka från CLI.

![Korrigerat problem](../assets/fix.svg) Uppgraderade beroendet för `magento/services-connector`.

![Korrigerat problem](../assets/fix.svg) Korrigerade synkroniseringsproblem i brittiska konton med ogiltig landskod.

![Korrigerat problem](../assets/fix.svg) Hårdkodad entitet_type_id för katalogproduktentiteten orsakar problem med Magento-priskällan.

![Korrigerat problem](../assets/fix.svg) Ett problem har korrigerats som förhindrar att konton som har tagits bort på en serverdel från en annan instans också tas bort från användargränssnittet.

![Korrigerat problem](../assets/fix.svg) Ett problem med import av vissa vagnsregler har korrigerats.

## v4.4.3

*7 mars 2023*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Korrigera](../assets/fix.svg) Stöd för Adobe Commerce 2.4.4 har lagts till.

## v4.4.2

*11 november 2021*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Korrigera](../assets/fix.svg) Uppdaterade beroenden som stöder andra uppdaterade tillägg.
![Korrigera](../assets/fix.svg) Stöd för PHP 8.1 har lagts till.

## v4.4.1

*11 november 2021*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Korrigera](../assets/fix.svg) Förändrade hur Adobe Commerce tar emot _Användarnamn_ från Amazon. Tidigare uppstod ett fel när beställningen skapades när _Användarnamn_ fältet innehåller specialtecken. Adobe Commerce får nu _Användarnamn_ data och filtrerar bort specialtecknen så att ordningen kan skapas.

## v4.4.0

*9 april 2021*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg) Stöd för skrivskyddat läge har lagts till i konfigurationen. Se [inställningar för försäljningskanal](sales-channel-settings.md).

![Korrigera](../assets/fix.svg) Dataflödet har ändrats så att flera kopior av samma instans kan hämta uppdateringar samtidigt.

![Korrigera](../assets/fix.svg) Synkroniseringsprocessen för kontoinformation har ändrats. Ett cron-jobb som ska synkroniseras med fjärrkontot har lagts till och samma funktioner har lagts till i CLI-kommandona.

![Korrigera](../assets/fix.svg) CLI-kommandoargument och flaggor har lagts till för mer exakt kontroll.

![Korrigera](../assets/fix.svg) Källan för bakgrundsuppgifter (cron) i systemkonfigurationen har korrigerats.

![Korrigera](../assets/fix.svg) Problemet med att det inte gick att skapa order när landskoden ställdes in på Puerto Rico (PR) har korrigerats.

## v4.3.0

*3 mars 2021*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Korrigera](../assets/fix.svg) <!--CHAN-xxxx-->The _Beställningsinformation_ funktionen har fått en ny design och är inte längre beroende av _Importera order_ inställning. Beställningsinformationen visas nu i Amazon Sales Channel-gränssnittet för alla beställningar.

![Korrigera](../assets/fix.svg) I _[!UICONTROL Marketing]_i Admin har namnet ändrats från_[!UICONTROL Amazon]_ till _[!UICONTROL Amazon Sales Channel]_.

![Känt fel](../assets/bug.svg) **Viktigt**: Kända problem med kompatibiliteten med Adobe Commerce 2.4.0 har åtgärdats i Adobe Commerce 2.4.1.

- Amazon cron-processer i `error` läge
- Installation med Commerce 2.4.0 misslyckas när arkiv skapas i databasen
- Det går inte att skapa produkten när MSI installeras

## v4.2.0

*3 mars 2021*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

Om du har en tidigare [!DNL Amazon sales channel] version som är installerad och som försöker uppdatera din Adobe Commerce till version 2.4.0, uppmanas du att uppdatera tillägget innan du kan slutföra Adobe Commerce-uppdateringen.

![Känt fel](../assets/bug.svg) När [!DNL Amazon sales channel] 4.2.0 är integrerat med version 2.4.0 och [Inventory management](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html?lang=en) är aktiverat finns det ett känt fel som förhindrar att produkter läggs till i din Commerce-katalog. Detta problem kommer att åtgärdas i en framtida version av Commerce.

![Nytt](../assets/new.svg) [!DNL Amazon sales channel] har förbättrats för att kunna ta emot textbaserade adressdata och matcha dem med standardiserade adressformat, inklusive ort, delstat och postnummer. Med den här uppdateringen kan beställningar och leveranser av data synkroniseras (synkroniseras) med Amazon utan adressfel.<br/>En kund anger till exempel ort, delstat och postnummer som `Escondido, californiA 92025-1501`. Amazon Sales Channel importerar och matchar data enligt standardformatet som `Escondido, CA 92025`och sedan synkroniserar det tillbaka till Amazon i detta standardiserade format.

![Nytt](../assets/new.svg) Stöd för PHP 7.4 har lagts till.

![Nytt](../assets/new.svg) <!--CHAN-4334-->Stöd för Adobe Commerce 2.4.x har lagts till. Tidigare versioner kan vara kompatibla med Commerce 2.4.x, men stöds inte. Se [Kommande versioner](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) för versionskompatibilitet. Amazon Sales Channel måste uppdateras till 4.2.0 innan Adobe Commerce 2.4.0-uppdateringen kan slutföras.

![Korrigera](../assets/fix.svg) <!--CHAN-4431-->Ett problem som orsakade ett fel har korrigerats _Åtkomst nekad_ fel för kunder i Storbritannien.

![Korrigera](../assets/fix.svg) <!--CHAN-4394-->Ett problem som gjorde att Amazon leveransstatus inte kunde synkroniseras med motsvarande handelsorder har korrigerats, vilket innebar att orderns leveransstatus låstes som `Pending` inom handel och `Unshipped` i Amazon. Med den nya standardiserade adressfunktionen har dessa leveransstatusfel åtgärdats.

![Korrigera](../assets/fix.svg) <!--ticket#-->Uppdaterad ordersynkronisering (synkronisering) för att ignorera misslyckade orderimporter, vilket minskar antalet synkroniseringsförsök och tillåter efterföljande importer att bearbetas, med begäran om ordersynkronisering som skickas var femte minut. Synkroniseringsfel registreras fortfarande i felloggen, men markeras som&quot;bearbetade&quot; för att tillåta ytterligare loggningsfunktioner. Dessutom [!DNL Amazon sales channel] tar nu automatiskt bort överflödiga data som samlats in för order som inte kan skapas i Commerce.

![Korrigera](../assets/fix.svg) Loggning av fel har uppdaterats för att samla in mer information om ej infångade undantag och uppdateringsfel för tillägg.

![Korrigera](../assets/fix.svg) <!--ticket#-->Ett problem som orsakade den första synkroniseringen av _lägsta pris_ data som ska misslyckas på grund av att en _pris_ värde.

![Korrigera](../assets/fix.svg) <!--CHAN-4410-->Korrigerade problem som orsakade filtreringsfel i _Amazon beställningar_ när datumintervallfältet lämnas tomt.

![Korrigera](../assets/fix.svg) <!--CHAN-4439-->Ett problem som orsakade kvantitetsrelaterade fel i lager- och leveranssynkronisering har korrigerats. Tillägget avrundar nu kvantitetsvärden som anges i decimalform innan de synkroniseras med Amazon.<br/> Om en handlare till exempel manuellt anger en kvantitet `2.5`, avrundas värdet nedåt till `2` och sedan synkroniserar den uppdaterade kvantiteten med Amazon.

## v4.1.0

*7 maj 2020*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg) <!--4247, 4230-->Processen för orderimport har ändrats så att den överensstämmer med kraven för handelsorder. Dessa ändringar åtgärdar problem som hindrade Commerce från att skapa motsvarande order för en importerad order. Se [Hantera order](managing-orders.md) för information om orderblockerare och lösningar.

![Nytt](../assets/new.svg) <!--CHAN-CHAN-4167, 4297, 4311, 4312, 4324-->Uppdaterade _Senaste order_ -avsnittet på butikspanelen och lade till ett nytt _Alla order_ som visar alla dina Amazon-order, inklusive filteralternativ och sidnumrering för att visa fler order. Se [Amazon Store Dashboard](amazon-store-dashboard.md) och [Visa Amazon-beställningar](amazon-orders-all.md).

![Nytt](../assets/new.svg) Lagt till _[!UICONTROL Order Notes]_kolumn för den omdesignade_[!UICONTROL Amazon Orders]_ tabell i båda _[!UICONTROL Recent Orders]_och_[!UICONTROL All Orders]_ vyer. _[!UICONTROL Order Notes]_meddela handlaren att det är något problem med orderns import. Se [Visa Amazon-beställningar](amazon-orders-all.md).

![Nytt](../assets/new.svg) <!--CHAN-4013-->Uppdaterade produktvillkorsparametrar som är anpassade till [Amazon förnyat](https://sell.amazon.com/programs/renewed) program. Se [Förnyade produkter](renewed-products.md).

![Nytt](../assets/new.svg) <!--CHAN-3680-->Uppdaterat [Beställningsinformation för Amazon](amazon-order-details.md) att inkludera&quot;generiska data&quot; för order som levereras av Amazon. Se [Fulifyllt av](fulfilled-by.md).

![Korrigera](../assets/fix.svg) <!--CHAN-4069-->Ett problem som orsakade förvrängning av ikoner på butikskortet har korrigerats.

![Korrigera](../assets/fix.svg) <!--CHAN-4165-->Ett fel som förhindrar _Inloggning_ skärmen inte visas när sessionen har gått ut.

![Korrigera](../assets/fix.svg) <!--CHAN-4211-->Ett problem har korrigerats som förhindrar att Amazon orderskattebelopp importeras till den nya handelsordern.

![Korrigera](../assets/fix.svg) <!--CHAN-4234-->Ett problem som orsakade att intäktssummor visades på butikens kontrollpanel för att inkludera order i har korrigerats `Canceled` eller `Error` status.

![Korrigera](../assets/fix.svg) <!--CHAN-4326-->Ett problem som orsakade orderimportfel associerade med tredjepartstillägg som använder har korrigerats _Magento Shipping_ metoder för att skapa order.

![Korrigera](../assets/fix.svg) <!--CHAN-4357-->Ett problem som orsakade fel när kronisynkronisering kördes har korrigerats. Ett lås har lagts till i CLI-kommandot som förhindrar att två cron-jobb synkroniseras samtidigt.

![Korrigera](../assets/fix.svg) Uppdaterad skyddsprofil för innehåll som stöds med Commerce version 2.3.5.

## v4.0.0

*25 mars 2020*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

>[!IMPORTANT]
>
>Amazon Sales Channel 4.0.0 stöds inte för Adobe Commerce 2.3.5. För support med Adobe Commerce 2.3.5, uppgradera till Amazon Sales Channel 4.1.0.

![Nytt](../assets/new.svg) En ny introduktion [Amazon Sales Channel](amazon-sales-channel-home.md) hemsida med förbättrad&quot;kortvy&quot; för din butiksinformation.

![Nytt](../assets/new.svg) En ny introduktion [instrumentpanel för butik](amazon-store-dashboard.md) med lista, beställningar och information om lagringsinställningar.

![Nytt](../assets/new.svg) En enklare och smidigare [introduktionsprocess](amazon-onboarding-home.md) och [standardinställningar för lagring](default-store-settings.md) så att ni kan integrera butikerna snabbare.

![Känt fel](../assets/bug.svg) <!--CHAN-4102--> När [skapa attribut](managing-attributes.md) för import av bilder från listor och **Lagra vyer** är inställd på `All Store Views (Global)`finns det ett känt fel som förhindrar att bilder importeras till alla butiksvyer. Om du ändrar inställningen för **Lagra vyer (för att importera värden till)** till en viss butik importeras bilderna för den butiken.

## v3.0.1

*11 november 2019*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Korrigera](../assets/fix.svg) **Inställningar för numeriskt fält**: <!--CHAN-3779-->Fält som kräver ett numeriskt värde har uppdaterats så att endast numeriska tecken accepteras. Exempel: Prisregelinställningar > Justeringsbelopp

![Korrigera](../assets/fix.svg) **Länkar till användarhandboken**: <!--CHAN-3778-->Felaktig _Användarhandbok_ länkarna har korrigerats.

![Korrigera](../assets/fix.svg) **Duplicera Amazon-listor**: <!--CHAN-3593-->Ett problem som tidigare orsakade dubbletter av Amazon-listor har nu åtgärdats. Före den här versionen lade tillägget till landskoden för Amazon-regionen i SKU-värden när listor importerades. Listan matchar katalogobjektet, men tillägget skapade en ny, duplicerad lista med den tillagda SKU:n. I den här versionen ändrar inte tillägget SKU:n för importerade listor och inga ändringar görs i befintliga listor. Du kan använda [!UICONTROL End Listing(s)] på Amazon om du vill ta bort dubblettlistor.

## v3.0.0

*7 oktober 2019*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg) **Amazon UK Marketplace ute nu**: Användare kan välja den brittiska marknadsplatsen när de skapar och integrerar en Commerce Store. Den här uppgraderingen i Storbritannien innehåller ytterligare support för:

- [Amazon momskalkyleringstjänst](https://sell.amazon.co.uk/learn/vat-resources){target="_blank"}

- [Produktmomskod](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"} information.

![Nytt](../assets/new.svg) **Förbättrad loggning**: <!--CHAN-3642, 3672-->Implementerat **Aktivera felsökningsloggning** för att samla in ytterligare synkroniseringsdata när felsökning behövs. Se [Inställningar för Sales Channeler](https://experienceleague.adobe.com/docs/commerce-admin/config/sales-channels.html) i konfigurationsreferensen.

![Korrigera](../assets/fix.svg) **Produktkatalog**: <!--CHAN-3687-->Ett problem som gjorde att bilder som importerats med en Amazon-lista inte kunde användas i motsvarande Commerce-katalogprodukt har korrigerats.

![Korrigera](../assets/fix.svg) **Skapa order**: <!--CHAN-3708-->Ett problem som hindrade Commerce från att skapa order för en Amazon-order som inte matchar en Commerce-katalogprodukt har korrigerats.

![Känt fel](../assets/bug.svg) **Duplicera Amazon-listor**: <!--CHAN-3593-->Detta gör att katalogen skapar ett objekt för en importerad lista med samma SKU men med en regionkod tillagd i slutet. Amazon bearbetar sedan den ändrade SKU:n som ett nytt objekt och skapar en lista. Detta problem kommer att åtgärdas i en framtida version.

## v2.0.0

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

>[!NOTE]
>
>Version 1.0.0 fanns endast i begränsad version.

![Nytt](../assets/new.svg)  **Förenklad registrering och underhåll**: Lägg till och integrera med ditt Amazon Seller-konto genom en stegvis process med detaljerade instruktioner från administratören. Underhåll butiker, konton och listade produkter via en och samma kontrollpanel.

![Nytt](../assets/new.svg)  **Stöd för flera konton**: Hantera och övervaka flera Amazon-varumärken och marknadsplatsregioner via Admin.

![Nytt](../assets/new.svg)  **Intelligent prissättning**: Ställ in automatiska regler för omprissättning för att öka chanserna till den avtalade Buy Boxen. Ställ in priser för att dynamiskt justera till Buy Boxens aktuella pris eller lägsta konkurrentpris. Ange gränser för omprissättning för att skydda din marginal.

![Nytt](../assets/new.svg)  **Listhantering**: Automatisera produktlistor och synkronisera din Commerce-katalog med Amazon Marketplace med hjälp av listregler. Lägg till specifika åsidosättningar för att exakt kontrollera dina erbjudanden. Övervaka och hantera alla listor direkt från administratören.

![Nytt](../assets/new.svg)  **Enhetliga Inventory management**: Håll lagerkvantiteterna i Commerce och Amazon synkroniserade.

![Nytt](../assets/new.svg)  **Hantering av order och uppfyllelse**: Spåra Amazon-beställningar via kontrollpanelen med smidig kommunikation och lageruppdateringar. Slutför och spåra orderleveranser som utförts av Amazon, handlaren har uppfyllt eller en blandning av metoder.

![Känt fel](../assets/bug.svg)  Du kan få längre väntetider för att uppdatera produktkvantiteter. Uppdateringar för produktkvantitet kan ta ~två timmar att synkronisera.

![Känt fel](../assets/bug.svg)  Importerade order kan ha en typ av _Prime_ eller _Premium_ beställningar. Du bör verifiera dessa beställningar på ditt Amazon Seller-konto.

![Känt fel](../assets/bug.svg)  Ej berättigade paketprodukter kan visas som berättigade att listas på Amazon. En av produkterna i den paketerade produkten är kanske inte berättigad. Om du råkar ut för problem kontrollerar du om du har rätt att köpa programartiklar som paketerats.

![Känt fel](../assets/bug.svg)  När du använder Inventory management för Commerce 2.3.x kan en partiell omindexering inte utlösas när en order skapas. Den försäljningsbara kvantiteten beräknas om till en timme, vilket kan orsaka överförsäljning under uppdateringsintervallet.
