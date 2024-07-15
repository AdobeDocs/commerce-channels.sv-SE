---
title: '[!DNL Amazon Sales Channel] versionsinformation'
description: Läs versionsinformationen om du vill ha information om alla  [!DNL Amazon Sales Channel] releaser.
feature: Sales Channels, Release Notes
exl-id: 792782e0-9097-42f7-9fc0-509ece02e407
source-git-commit: df8bbec23d34b53a0e694c924aca5b1ed41e4d08
workflow-type: tm+mt
source-wordcount: '2010'
ht-degree: 0%

---

# Versionsinformation för [!DNL Amazon Sales Channel]

>[!IMPORTANT]
>
> [!DNL Amazon sales channel] kan installeras på instanser med Magento Open Source, Adobe Commerce och Adobe Commerce i molninfrastrukturversionerna 2.3.x och 2.4.x. Tillägget stöds inte längre i Adobe Commerce 2.1, Magento Open Source 2.2 eller Magento 1.
> <br>Stöd finns endast för [!DNL Amazon sales channel] version 4.0.0 och 4.1.0 på Adobe Commerce 2.3.x.
> <br>[!DNL Amazon sales channel] version 4.2.0+ är kompatibel med Adobe Commerce 2.3.x, men support finns endast för Adobe Commerce 2.4.x-versioner.
>

Dessa versionsinformation beskriver den första versionen av [!DNL Amazon sales channel] och innehåller:

![Nya](../assets/new.svg) nya funktioner
![ Åtgärdat problem ](../assets/fix.svg) Korrigeringar och förbättringar
![Kända fel](../assets/bug.svg)

Se [Kommande versioner](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) för versionshantering, support och kompatibilitet.

Se [Produkttillgänglighet](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) om du vill veta vilka Adobe Commerce-versioner som stöder det här tillägget.

## v4.5.0

*30 augusti 2023*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg) har lagt till API-gatewayen Adobe.IO, som ändrats från MAGI, för förbättrad autentiseringssäkerhet. `ServicesId` har ett nytt användargränssnitt för att hantera dina Adobe.IO-autentiseringsuppgifter, som liknar andra [Adobe Commerce-tjänster](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html).

>[!NOTE]
>
>Marknadsförarna måste se till att [privata och offentliga API-nycklar](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html) uppdateras för produktion.


![Korrigerat problem](../assets/fix.svg) upptäckte ett konfigurationsinställningsproblem och åtgärdade orderskapandeflödet.

## v4.4.4

*7 mars 2023*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Korrigerat problem](../assets/fix.svg) Stöd för Adobe Commerce 2.4.6 och PHP 8.2 har lagts till.

![Korrigerat problem](../assets/fix.svg) Minskat brus i loggar.

![Korrigerat problem](../assets/fix.svg) Förbättrad stabilitet vid hämtning av uppdateringar.

![Korrigerat problem](../assets/fix.svg) Förenklade processen för att köra en enda åtgärdsliknande pull eller för att tillämpa från CLI.

![Korrigerat problem](../assets/fix.svg) Uppgraderade beroendet för `magento/services-connector`.

![Korrigerat problem](../assets/fix.svg) Korrigerade synkroniseringsproblem i brittiska konton med ogiltig landskod.

![Korrigerat problem](../assets/fix.svg) Enhet_type_id för katalogproduktentiteten som hårdkodats orsakar problem med Magento Price Source.

![Korrigerat problem](../assets/fix.svg) Ett problem som hindrade konton som tagits bort från en annan instans från att tas bort från gränssnittet har korrigerats.

![Korrigerat problem](../assets/fix.svg) Ett problem med import av vissa kundvagnsregler har korrigerats.

## v4.4.3

*7 mars 2023*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Korrigera](../assets/fix.svg) Stöd för Adobe Commerce 2.4.4 har lagts till.

## v4.4.2

*11 november 2021*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Åtgärda](../assets/fix.svg) Beroenden har uppdaterats för stöd av andra uppdaterade tillägg.
![Korrigera](../assets/fix.svg) Stöd för PHP 8.1 har lagts till.

## v4.4.1

*11 november 2021*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Korrigera](../assets/fix.svg) Ändrat sättet som Adobe Commerce tar emot fältet _Användarnamn_ från Amazon. Tidigare uppstod ett fel när ordningen skapades när fältet _Användarnamn_ innehöll specialtecken. Adobe Commerce tar nu emot _användarnamnsdata_ och filtrerar bort specialtecknen så att ordningen kan skapas.

## v4.4.0

*9 april 2021*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg) Stöd för skrivskyddat läge har lagts till i konfigurationen. Se [inställningar för försäljningskanal](sales-channel-settings.md).

![Korrigera](../assets/fix.svg) Dataflödet har ändrats så att flera kopior av samma instans kan hämta uppdateringar samtidigt.

![Korrigera](../assets/fix.svg) Synkroniseringsprocessen för synkronisering av kontoinformation har ändrats. Ett cron-jobb som ska synkroniseras med fjärrkontot har lagts till och samma funktioner har lagts till i CLI-kommandona.

![Korrigera](../assets/fix.svg) CLI-kommandoargument och flaggor har lagts till för mer exakt kontroll.

![Korrigera](../assets/fix.svg) Source för bakgrundsåtgärder (cron) i systemkonfigurationen har korrigerats.

![Korrigering](../assets/fix.svg) Korrigerade problemet som förhindrade att order skapades när landskoden ställdes in på Puerto Rico (PR).

## v4.3.0

*3 mars 2021*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Korrigera](../assets/fix.svg) <!--CHAN-xxxx-->Funktionen _Beställningsinformation_ har fått en ny utformning och är inte längre beroende av inställningen för _Importera order_. Beställningsinformationen visas nu i Amazon Sales Channel-gränssnittet för alla beställningar.

![Korrigera](../assets/fix.svg) På menyn _[!UICONTROL Marketing]_i Admin har namnet ändrats från_[!UICONTROL Amazon]_ till _[!UICONTROL Amazon Sales Channel]_.

![Känt fel](../assets/bug.svg) **Viktigt**: Kända problem med Adobe Commerce 2.4.0-kompatibilitet har lösts i Adobe Commerce 2.4.1.

- Amazon cron-processer i läget `error`
- Installationen med Commerce 2.4.0 misslyckas när arkiv skapas i databasen
- Det går inte att skapa produkten när MSI installeras

## v4.2.0

*3 mars 2021*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

Om du har en tidigare version av [!DNL Amazon sales channel] installerad och försöker uppdatera din Adobe Commerce till version 2.4.0, uppmanas du att uppdatera tillägget innan du kan slutföra Adobe Commerce-uppdateringen.

![Känt fel](../assets/bug.svg) När [!DNL Amazon sales channel] 4.2.0 har integrerats med version 2.4.0 och [Inventory management](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html?lang=en) har aktiverats finns det ett känt fel som förhindrar att produkter läggs till i din Commerce-katalog. Detta problem kommer att åtgärdas i en framtida version av Commerce.

![Nytt](../assets/new.svg) [!DNL Amazon sales channel] har förbättrats för att ta emot textbaserade adressdata och matcha dem med standardiserade adressformat, inklusive ort, delstat och postnummer. Med den här uppdateringen kan beställningar och leveranser av data synkroniseras (synkroniseras) med Amazon utan adressfel.<br/>En kund anger till exempel ort, delstat och postnummer som `Escondido, californiA 92025-1501`. Amazon Sales Channel importerar och matchar data till standardformatet som `Escondido, CA 92025`, och synkroniserar sedan tillbaka dem till Amazon i det här standardformatet.

![Nytt](../assets/new.svg) Stöd för PHP 7.4 har lagts till.

![Nytt](../assets/new.svg) <!--CHAN-4334-->Stöd för Adobe Commerce 2.4.x har lagts till. Tidigare versioner kan vara kompatibla med Commerce 2.4.x, men stöds inte. Se [Kommande versioner](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) för versionskompatibilitet. Amazon Sales Channel måste uppdateras till 4.2.0 innan Adobe Commerce 2.4.0-uppdateringen kan slutföras.

![Korrigera](../assets/fix.svg) <!--CHAN-4431-->Ett fel som orsakade ett _Åtkomst nekad_-fel för kunder i Storbritannien har korrigerats.

![Korrigera](../assets/fix.svg) <!--CHAN-4394-->Ett fel har korrigerats som gjorde att Amazon leveransstatus inte kunde synkroniseras med motsvarande Commerce-order, vilket innebar att orderns leveransstatus låstes som `Pending` i Commerce och `Unshipped` i Amazon. Med den nya standardiserade adressfunktionen har dessa leveransstatusfel åtgärdats.

![Åtgärda](../assets/fix.svg) <!--ticket#-->Uppdaterad ordersynkronisering (synkronisering) för att ignorera misslyckade orderimporter, vilket minskar antalet synkroniseringsförsök och tillåter efterföljande importer att bearbetas, med begäran om ordersynkronisering som skickas var femte minut. Synkroniseringsfel registreras fortfarande i felloggen, men markeras som&quot;bearbetade&quot; för att tillåta ytterligare loggningsfunktioner. Dessutom tar [!DNL Amazon sales channel] nu automatiskt bort överflödiga data som samlats in för order som inte kan skapas i Commerce.

![Åtgärda](../assets/fix.svg) Felloggningen har uppdaterats för att samla in mer information om ej infångade undantag och uppdateringsfel för tillägg.

![Korrigera](../assets/fix.svg) <!--ticket#-->Ett fel som orsakade att den första synkroniseringen av _lägsta priset_-data misslyckades på grund av att _price_-värdet saknas.

![Åtgärda](../assets/fix.svg) <!--CHAN-4410-->Korrigerade problem som orsakade filtreringsfel i vyn _Amazon-order_ när datumintervallfältet lämnas tomt.

![Korrigera](../assets/fix.svg) <!--CHAN-4439-->Ett problem som orsakade kvantitetsrelaterade fel i lager- och leveranssynkronisering har korrigerats. Tillägget avrundar nu kvantitetsvärden som anges i decimalform innan de synkroniseras med Amazon.<br/> När en handlare till exempel manuellt anger en kvantitet på `2.5` avrundas värdet nedåt till `2` och sedan synkroniseras den uppdaterade kvantiteten med Amazon.

## v4.1.0

*7 maj 2020*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg) <!--4247, 4230-->Beställningsimporten har ändrats så att den överensstämmer med Commerce orderkrav. Dessa ändringar åtgärdar problem som gjorde att Commerce inte kunde skapa motsvarande order för en importerad order. Mer information om orderblockerare och lösningar finns i [Hantera beställningar](managing-orders.md).

![Nytt](../assets/new.svg) <!--CHAN-CHAN-4167, 4297, 4311, 4312, 4324-->Uppdaterade avsnittet _Senaste beställningar_ på butikspanelen och lade till en ny vy _Alla beställningar_ som visar alla dina Amazon-beställningar, inklusive filteralternativ och sidnumrering för att visa fler beställningar. Se [Amazon Store Dashboard](amazon-store-dashboard.md) och [Visa Amazon-beställningar](amazon-orders-all.md).

![Nytt](../assets/new.svg) har lagt till kolumnen _[!UICONTROL Order Notes]_i den omdesignade tabellen_[!UICONTROL Amazon Orders]_ i både _[!UICONTROL Recent Orders]_- och_[!UICONTROL All Orders]_-vyer. _[!UICONTROL Order Notes]_meddela handlaren att det har uppstått ett problem med orderns import. Se [Visa Amazon-beställningar](amazon-orders-all.md).

![Nytt](../assets/new.svg) <!--CHAN-4013-->Uppdaterade produktvillkorsparametrar som är i linje med programmet [Amazon Renewed](https://sell.amazon.com/programs/renewed). Se [Förnyade produkter](renewed-products.md).

![Nytt](../assets/new.svg) <!--CHAN-3680-->Uppdaterat [Amazon-beställningsinformation](amazon-order-details.md) för att inkludera&quot;generiska data&quot; för beställningar som har utförts av Amazon. Se [Fullgjord av](fulfilled-by.md).

![Korrigera](../assets/fix.svg) <!--CHAN-4069-->Ett fel som orsakade förvrängning av ikoner på butikskortet har korrigerats.

![Korrigera](../assets/fix.svg) <!--CHAN-4165-->Ett fel har korrigerats som förhindrar att skärmen _Inloggning_ visas efter att sessionen har gått ut.

![Åtgärda](../assets/fix.svg) <!--CHAN-4211-->Ett fel har korrigerats som förhindrar att Amazon ordermomsbelopp importeras till den nya Commerce-ordern.

![Korrigera](../assets/fix.svg) <!--CHAN-4234-->Ett problem har korrigerats som gjorde att intäktssummor visades på butikens kontrollpanel så att beställningar i statusen `Canceled` eller `Error` inkluderades.

![Åtgärda](../assets/fix.svg) <!--CHAN-4326-->Ett problem har korrigerats som orsakade orderimportfel associerade med tredjepartstillägg som använder _Magento Shipping_-metoder för att skapa order.

![Korrigera](../assets/fix.svg) <!--CHAN-4357-->Ett fel som orsakade fel när cron-synkronisering kördes har korrigerats. Ett lås har lagts till i CLI-kommandot som förhindrar att två cron-jobb synkroniseras samtidigt.

![Korrigera](../assets/fix.svg) Uppdaterad skyddsprofil för innehåll för stöd med Commerce version 2.3.5.

## v4.0.0

*25 mars 2020*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

>[!IMPORTANT]
>
>Amazon Sales Channel 4.0.0 stöds inte för Adobe Commerce 2.3.5. För support med Adobe Commerce 2.3.5, uppgradera till Amazon Sales Channel 4.1.0.

![Nytt](../assets/new.svg) Introducerade en ny [Amazon-Sales Channel](amazon-sales-channel-home.md)-hemsida med förbättrad&quot;kortvy&quot; för din butiksinformation.

![Nytt](../assets/new.svg) Introducerade en ny [butikspanel](amazon-store-dashboard.md) med information om listning, senaste beställningar och lagringsinställningar.

![Nytt](../assets/new.svg) Introducerade en enklare och smidigare [introduktionsprocess](amazon-onboarding-home.md) och [standardinställningar för butik](default-store-settings.md) för att få butikerna integrerade snabbare.

![Känt fel](../assets/bug.svg) <!--CHAN-4102--> När [skapar attribut](managing-attributes.md) för import av bilder från listor och **Store Views** är inställt på `All Store Views (Global)` finns det ett känt fel som förhindrar bilderna från att importeras till alla butiksvyer. Om du ändrar inställningen för **butiksvyer (för att importera värden till)** till en viss butik importeras bilderna för den butiken.

## v3.0.1

*11 november 2019*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Korrigera](../assets/fix.svg) **Inställningar för numeriska fält**: <!--CHAN-3779-->Fält som kräver ett numeriskt värde har uppdaterats så att endast numeriska tecken accepteras. Exempel: Prisregelinställningar > Justeringsbelopp

![Korrigera](../assets/fix.svg) **Länkar till användarhandboken**: <!--CHAN-3778-->Felaktiga _länkar i användarhandboken_ har korrigerats.

![Korrigera](../assets/fix.svg) **Duplicera Amazon-listor**: <!--CHAN-3593-->Ett tidigare rapporterade problem som orsakar dubbletter av Amazon-listor har nu korrigerats. Före den här versionen lade tillägget till landskoden för Amazon-regionen i SKU-värden när listor importerades. Listan matchar katalogobjektet, men tillägget skapade en ny, duplicerad lista med den tillagda SKU:n. I den här versionen ändrar inte tillägget SKU:n för importerade listor och inga ändringar görs i befintliga listor. Du kan använda alternativet [!UICONTROL End Listing(s)] för Amazon för att ta bort dubblettlistor.

## v3.0.0

*7 oktober 2019*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg) **Amazon UK Marketplace nu tillgängligt**: Användare kan välja den brittiska marknadsplatsen när de skapar och integrerar en Commerce-butik. Den här uppgraderingen i Storbritannien innehåller ytterligare support för:

- [Amazon momsberäkningstjänst](https://sell.amazon.co.uk/learn/vat-resources){target="_blank"}

- [Information om produktskattekod](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}.

![Nytt](../assets/new.svg) **Förbättrad loggning**: <!--CHAN-3642, 3672-->Funktionen **Aktivera felsökningsloggning** har implementerats för att samla in ytterligare synkroniseringsdata när felsökning behövs. Läs avsnittet [Inställningar för Sales Channeler](https://experienceleague.adobe.com/docs/commerce-admin/config/sales-channels.html) i konfigurationsreferensen.

![Korrigera](../assets/fix.svg) **Produktkatalog**: <!--CHAN-3687-->Ett fel har korrigerats som gjorde att bilder som importerats med en Amazon-lista inte kunde användas för motsvarande Commerce-katalogprodukt.

![Åtgärda](../assets/fix.svg) **Skapa order**: <!--CHAN-3708-->Ett fel har korrigerats som förhindrar Commerce från att skapa order för en Amazon-order som inte matchar en Commerce-katalogprodukt.

![Känt fel](../assets/bug.svg) **Duplicera Amazon-listor**: <!--CHAN-3593-->Det här problemet gör att katalogen skapar ett objekt för en importerad lista, med samma SKU men med en regionkod tillagd i slutet. Amazon bearbetar sedan den ändrade SKU:n som ett nytt objekt och skapar en lista. Detta problem kommer att åtgärdas i en framtida version.

## v2.0.0

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

>[!NOTE]
>
>Version 1.0.0 fanns endast i begränsad version.

![Nytt](../assets/new.svg) **Förenklat introduktion och underhåll**: Lägg till och integrera med ditt Amazon Seller-konto genom en steg-för-steg-process med detaljerade instruktioner som är tillgängliga via administratören. Underhåll butiker, konton och listade produkter via en och samma kontrollpanel.

![Nytt](../assets/new.svg) **Stöd för flera konton**: Hantera och övervaka flera Amazon-varumärken och marknadsplatsregioner via administratören.

![Nytt](../assets/new.svg) **Intelligent prissättning**: Ställ in automatiska omprissättningsregler för att öka dina chanser för den lagrade Buy Boxen. Ställ in priser för att dynamiskt justera till Buy Boxens aktuella pris eller lägsta konkurrentpris. Ange gränser för omprissättning för att skydda din marginal.

![Nytt](../assets/new.svg) **Listhantering**: Automatisera produktlistor och synkronisera din Commerce-katalog till Amazon Marketplace med listregler. Lägg till specifika åsidosättningar för att exakt kontrollera dina erbjudanden. Övervaka och hantera alla listor direkt från administratören.

![Nytt](../assets/new.svg) **Konsekvent Inventory management**: Håll lagerkvantiteterna för Commerce och Amazon synkroniserade.

![Nytt](../assets/new.svg) **Order- och Fulfillment Management**: Spåra Amazon-beställningar via kontrollpanelen med smidig kommunikation och lageruppdateringar. Slutför och spåra orderleveranser som utförts av Amazon, handlaren har uppfyllt eller en blandning av metoder.

![Känt fel](../assets/bug.svg) Du kan få längre väntetider för att uppdatera produktkvantiteter. Uppdateringar för produktkvantitet kan ta ~två timmar att synkronisera.

![Känt problem](../assets/bug.svg) Importerade order kan ha typen _Prime_ eller _Premium_. Du bör verifiera dessa beställningar på ditt Amazon Seller-konto.

![Känd utgåva](../assets/bug.svg) Ej berättigade paketerade produkter kan visas som berättigade att listas på Amazon. En av produkterna i den paketerade produkten är kanske inte berättigad. Om du råkar ut för problem kontrollerar du om du har rätt att köpa programartiklar som paketerats.

![Känt fel](../assets/bug.svg) När du använder Inventory management för Commerce 2.3.x kan en partiell omindexering inte utlösas när en order skapas. Den försäljningsbara kvantiteten beräknas om till en timme, vilket kan orsaka överförsäljning under uppdateringsintervallet.
