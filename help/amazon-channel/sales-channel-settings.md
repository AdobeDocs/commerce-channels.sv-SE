---
title: Inställningar för Sales Channel
description: Uppdatera Commerce-konfigurationen om du vill hantera loggning, referenskälla och synkronisering för Amazon säljkanalsfunktioner.
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Inställningar för Sales Channel

När [!DNL Amazon Sales Channel] tillägg är installerat, standardvärden anges i Admin for Amazon-försäljningskanalen. De här inställningarna kan ändras i konfigurationsinställningarna för din Amazon Store. Dessa inställningar inkluderar:

- Intervall för rensning av aktivitetslogghistorik
- Källval för kron
- Alternativ för loggsynkronisering

## Ändra inställningarna för handelskanaler

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales Channels]** och välja **[!UICONTROL Global Settings]**.

1. För **[!UICONTROL Clear Log History]** väljer du ett alternativ:

   - `Once Daily` - Välj att rensa din butiksaktivitetshistorik en gång om dagen.

   - `Once Weekly` - Välj att rensa din butiksaktivitetshistorik en gång i veckan.

   - `Once Monthly` - (Standard) Välj att rensa din butiksaktivitetshistorik en gång i månaden.

1. För **[!UICONTROL Background Tasks (CRON) Source]**, välja `Magento CRON`.

   Med det här alternativet kan Amazon försäljningskanal använda [!DNL Commerce] [Cron](https://docs.magento.com/user-guide/system/cron.html) inställningar för att bestämma kommunikations- och datasynkroniseringsintervall med [!DNL Amazon Seller Central].

1. För **[!UICONTROL Enable Debug Logging]**, välja `Enabled` för att samla in ytterligare synkroniseringsdata när felsökning behövs.

   Loggning av Amazon-försäljningskanal skrivs till `{Commerce Root}/var/log/channel_amazon.log` och kan visas i [utvecklarläge](https://docs.magento.com/user-guide/magento/installation-modes.html){target=&quot;_blank&quot;}. Loggning ska bara vara `Enabled` under felsökning och bör `Disabled` när felsökningen är klar.

1. Klicka **[!UICONTROL Save Config]**.

![Konfigurationsinställningar för Sales Channel](assets/config-sales-channel-global-settings.png)
