---
title: Dokumentation för CORS-konfigurationsmöjlighet
description: Lär dig mer om CORS konfigurationsmöjlighet och att identifiera och åtgärda säkerhetsluckor på platsen.
badgeSecurityPosture: label="Säkerhetsposition" type="Caution" url="../../opportunity-types/security-posture.md" tooltip="Säkerhetsposition"
source-git-commit: cb64a34b758de8f5dcea298014ddd0ba79a24c17
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---


# CORS-konfigurationsmöjlighet

![CORS-konfigurationsmöjlighet](./assets/cors-configuration/hero.png){align="center"}

Korrekt konfigurering av Cross-Origin Resource Sharing (CORS) är nödvändigt för att skydda webbapplikationer mot obehörig dataåtkomst. När rubriken `Access-Control-Allow-Origin` är inställd på `*` kan alla domäner begära och ta emot svar, vilket kan medföra att känslig information exponeras för angripare. Denna funktion ger möjlighet att stärka säkerheten genom att implementera en kontrollerad tillåtelselista av betrodda domäner eller inaktivera CORS där det inte behövs. En säker CORS-konfiguration skyddar det privata innehållet samtidigt som man bibehåller den sömlösa åtkomsten för behöriga användare.

## Automatisk identifiering

![Identifiera CORS-konfigurationsmöjlighet automatiskt](./assets/cors-configuration/auto-identify.png){align="center"}

Automatisk identifiering söker igenom din webbplats efter CORS-felkonfigurationer och identifierar URL:er som kan komma åt obehörig åtkomst. Dessa URL:er visas i den övre tabellen tillsammans med följande information:

* **Sidprefix** - URL-sökvägsprefixet som är känsligt för CORS-felkonfigurationer.
* **Sidexempel** - En exempel-URL som kan ge obehörig åtkomst.

## Föreslå automatiskt

![Föreslå CORS-konfigurationsmöjlighet automatiskt](./assets/cors-configuration/auto-suggest.png){align="center"}

Automatiskt förslag innehåller **programkodfiler** och deras **rader** som kan granskas för att ange lax CORS-principer.


## Automatisk optimering

[!BADGE Ultimate]{type=Positive tooltip="Ultimate"}

>[!BEGINTABS]

>[!TAB Distribuera optimering]

{{auto-optimize-deploy-optimization-slack}}

>[!TAB Begär godkännande]

{{auto-optimize-request-approval}}

>[!ENDTABS]
