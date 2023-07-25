---
title: Inställningar för försäljningskanal
description: Uppdatera Commerce-konfigurationen om du vill hantera loggning, referenskälla och synkronisering för Amazon säljkanalsfunktioner.
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
role: Admin, Developer
feature: Sales Channels, Configuration, Logs
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Inställningar för försäljningskanal

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

   Med det här alternativet kan Amazon försäljningskanal använda [!DNL Commerce] [Cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html) inställningar för att bestämma kommunikations- och datasynkroniseringsintervall med [!DNL Amazon Seller Central].

1. För **[!UICONTROL Enable Debug Logging]**, välja `Enabled` för att samla in ytterligare synkroniseringsdata när felsökning behövs.

   Loggning av Amazon-försäljningskanal skrivs till `{Commerce Root}/var/log/channel_amazon.log` och kan visas i [utvecklarläge](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/developer-tools.html#operation-modes). Loggning ska bara vara `Enabled` under felsökning och bör `Disabled` när felsökningen är klar.

1. För **[!UICONTROL Read-Only Mode]**, markera `Enabled` för att blockera alla utgående API-begäranden som ändrar tillstånd.

   Med den här inställningen sparas eventuella ändringar, men skickas inte förrän [!UICONTROL Read-Only Mode] är inaktiverat. Konfigurationscachen måste rensas för skrivskyddat läge för att aktiveras. Om du vill starta dataöverföringen igen väljer du `Disabled`.

   >[!IMPORTANT]
   >
   >[!UICONTROL Read-Only Mode] är utformat för kopior av produktionsinstansen, till exempel staging eller QA, och bör inte användas på produktionsinstansen.
   >
   >När en databas migreras till en ny kopia av instansen (identifieras när en butiks URL ändras i konfigurationen), [!UICONTROL Read-Only Mode] aktiveras automatiskt.

1. Klicka **[!UICONTROL Save Config]**.

![Konfigurationsinställningar för Sales Channel](assets/config-sales-channel-global-settings.png){width="600" zoomable="yes"}
