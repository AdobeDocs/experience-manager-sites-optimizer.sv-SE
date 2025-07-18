---
title: Dokumentation för serveröverskridande skriptmöjligheter
description: Läs mer om cross-site scripting och att identifiera och åtgärda säkerhetsluckor.
badgeSecurityPosture: label="Säkerhetsposition" type="Caution" url="../../opportunity-types/security-posture.md" tooltip="Säkerhetsposition"
source-git-commit: cb64a34b758de8f5dcea298014ddd0ba79a24c17
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---


# Serveröverskridande skriptmöjligheter

![Affärsmöjlighet mellan webbplatser](./assets/cross-site-scripting/hero.png){align="center"}

Serveröverskridande skriptmöjligheter (cross-site scripting) identifierar sårbarheter i koden för din webbplats. Sedan åtgärdas problem som angripare kan utnyttja för att lägga in skadliga skript på webbsidor som andra användare kan visa. Dessa skript kan stjäla känslig information, t.ex. sessionscookies, eller utföra åtgärder för användarens räkning, t.ex. ändra användarens lösenord.

## Automatisk identifiering

![Identifiera affärsmöjlighet mellan webbplatser automatiskt](./assets/cross-site-scripting/auto-identify.png){align="center"}

* **Sårbar kod** - Kod som är sårbar för attacker med korsskriptning mellan webbplatser.
* **Länk att återskapa** - Länken till sidan där sårbarheten påträffades.

## Föreslå automatiskt

![Föreslå affärsmöjlighet mellan webbplatser automatiskt](./assets/cross-site-scripting/auto-suggest.png){align="center"}

* **Föreslagen korrigering** - Ett AI-genererat förslag på hur du ska åtgärda säkerhetsluckan.

## Automatisk optimering

[!BADGE Ultimate]{type=Positive tooltip="Ultimate"}

>[!BEGINTABS]

>[!TAB Distribuera optimering]

{{auto-optimize-deploy-optimization-slack}}

>[!TAB Begär godkännande]

{{auto-optimize-request-approval}}

>[!ENDTABS]
