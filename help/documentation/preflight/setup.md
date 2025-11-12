---
title: Preflight-inställning
description: Lär dig hur du konfigurerar Preflight-tillägget för AEM Sites Optimizer.
source-git-commit: 210acc5337796707ced10f2b84d473503fc06088
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---


# Preflight-inställning

AEM Sites Optimizer Preflight-identifiering av affärsmöjligheter kräver att du har skapat Preflight-tillägget i antingen Universal Editor, Document-Based Preview eller AEM Cloud Service för att kunna köra preflight-granskningar på sidorna innan de publiceras.

## Aktivera användaråtkomst

Om du vill använda preflight-tillägget måste du se till att din användare har tilldelats minst en av följande AEM Sites Optimizer-produktprofiler i [Adobe Admin Console](https://adminconsole.adobe.com):

* AEM Sites Optimizer - Föreslå användare automatiskt
* AEM Sites Optimizer - Automatisk optimering av användare

## Aktivera Preflight-tillägget

>[!BEGINTABS]

>[!TAB Universell redigerare]

Så här ställer du in Preflight i Universal Editor:

1. Öppna **Extension Manager** på:
   [https://experience.adobe.com/#/@org/aem/extension-manager/universal-editor](https://experience.adobe.com/#/@org/aem/extension-manager/universal-editor)
1. Leta reda på **AEM Sites Optimizer Preflight-tillägget** och skicka en begäran om att aktivera det.
1. **Adobe AEM-teamet** granskar och aktiverar tillägget för din organisation.
1. När tillägget har aktiverats öppnar du en sida i **Universell redigerare**, till exempel:
   `https://author-p12345-e123456.adobeaemcloud.com/ui#/@org/aem/universal-editor/canvas/author-p12345-e123456.adobeaemcloud.com/content/en/example/home.html`
1. **Preflight-tillägget** visas i **sidospåret**.
1. Välj **Preflight-tillägget** från sidospåret för att starta en **Preflight-granskning** av den aktuella sidan.

>[!TAB Dokumentbaserad redigering]

Så här ställer du in preflight för dokumentbaserad redigering:

1. Lägg till följande konfiguration till `/tools/sidekick/config.json` i ditt Edge Delivery Services-projekts GitHub-databas:

   ```json
   {
     "plugins": [
       {
         "id": "preflight",
         "titleI18n": {
           "en": "Preflight"
         },
         "environments": ["preview"],
         "event": "preflight"
       }
     ]
   }
   ```

1. Skapa en ny fil `/tools/sidekick/aem-sites-optimizer-preflight.js` och lägg till följande innehåll:

   ```javascript
   (function () {
     let isAEMSitesOptimizerPreflightAppLoaded = false;
     function loadAEMSitesOptimizerPreflightApp() {
       const script = document.createElement('script');
       script.src = 'https://experience.adobe.com/solutions/OneAdobe-aem-sites-optimizer-preflight-mfe/static-assets/resources/sidekick/client.js?source=plugin';
       script.onload = function () {
         isAEMSitesOptimizerPreflightAppLoaded = true;
       };
       script.onerror = function () {
         console.error('Error loading AEMSitesOptimizerPreflightApp.');
       };
       document.head.appendChild(script);
     }
   
     function handlePluginButtonClick() {
       if (!isAEMSitesOptimizerPreflightAppLoaded) {
         loadAEMSitesOptimizerPreflightApp();
       }
     }
   
     // Sidekick V1 extension support
     const sidekick = document.querySelector('helix-sidekick');
     if (sidekick) {
       sidekick.addEventListener('custom:preflight', handlePluginButtonClick);
     } else {
       document.addEventListener('sidekick-ready', () => {
         document.querySelector('helix-sidekick')
           .addEventListener('custom:preflight', handlePluginButtonClick);
       }, { once: true });
     }
   
     // Sidekick V2 extension support
     const sidekickV2 = document.querySelector('aem-sidekick');
     if (sidekickV2) {
       sidekickV2.addEventListener('custom:preflight', handlePluginButtonClick);
     } else {
       document.addEventListener('sidekick-ready', () => {
         document.querySelector('aem-sidekick')
           .addEventListener('custom:preflight', handlePluginButtonClick);
       }, { once: true });
     }
   }());
   ```

1. Uppdatera funktionen `loadLazy()` i `/scripts/scripts.js` för att importera preflight-skriptet för förhandsgransknings-URL:er:

   ```javascript
   if (window.location.href.includes('.aem.page')) {
      import('../tools/sidekick/aem-sites-optimizer-preflight.js');
   }
   ```

1. Öppna förhandsgransknings-URL:en (`*.aem.page`) för sidan som du vill granska.
1. I **Sidekick** klickar du på knappen **Preflight** för att starta granskningen av den aktuella sidan.

>[!TAB AEM Sites Page Editor]

Om du vill använda Preflight i AEM Sites Page Editor kan du skapa ett bokmärke i webbläsaren. Följ de här stegen:

1. Visa **bokmärkesfältet** i webbläsaren:

   * Tryck på **Ctrl+Skift+B** (Windows) eller **Cmd+Skift+B** (Mac).

1. Skapa ett nytt bokmärke i webbläsaren:

   * Högerklicka på bokmärkesfältet och välj **Ny sida** eller **Lägg till bokmärke**.
   * Klistra in följande kod i fältet **Adress (URL)**:

   ```javascript
   javascript:(function(){const script=document.createElement('script');script.src='https://experience.adobe.com/solutions/OneAdobe-aem-sites-optimizer-preflight-mfe/static-assets/resources/sidekick/client.js?source=bookmarklet&target-source=aem-cloud-service';document.head.appendChild(script);})();
   ```

1. Namnge bokmärket **Preflight** (eller något annat namn du föredrar).
1. Öppna förhandsgransknings-URL:en (`*.aem.page`) för sidan som du vill granska i **AEM Sites Page Editor**.
1. Klicka på bokmärket **Preflight** i bokmärkesfältet för att starta granskningen av den aktuella sidan.

>[!ENDTABS]

## God praxis

Tänk på följande när du kör preflight-granskningar:

* Kör alltid granskningar på **mellanlagrings- eller förhandsgranskningssidor** innan du publicerar till produktion.
* Prioritera lösningen av **viktiga problem**, till exempel brutna länkar, saknade H1-taggar eller osäkra länkar.
* Kontrollera att **autentisering är aktiverat** för skyddade mellanlagringsmiljöer innan du kör granskningar.
* Granska och använd **metataggrekommendationer** för att förbättra SEO-prestanda.
