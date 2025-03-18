---
title: Dokumentation för serveröverskridande skriptmöjligheter
description: Läs mer om cross-site scripting och att identifiera och åtgärda säkerhetsluckor.
badgeSecurityPosture: label="Säkerhetsposition" type="Caution" url="../../opportunity-types/security-posture.md" tooltip="Säkerhetsposition"
source-git-commit: ab2d75b1d986d83e3303e29a25d2babd1598394a
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---


# Serveröverskridande skriptmöjligheter

![Affärsmöjlighet mellan webbplatser](./assets/cross-site-scripting/hero.png){align="center"}

Serveröverskridande skriptmöjligheter (cross-site scripting) identifierar och åtgärdar säkerhetsluckor i koden som kan utnyttjas av angripare för att lägga in skadliga skript på webbsidor som visas av andra användare. Dessa skript kan stjäla känslig information, t.ex. sessionscookies, eller utföra åtgärder för användarens räkning, t.ex. ändra användarens lösenord.

## Automatisk identifiering

![Identifiera affärsmöjlighet mellan webbplatser automatiskt](./assets/cross-site-scripting/auto-identify.png){align="center"}

* **Sårbar kod** - Kod som är sårbar för attacker med korsskriptning mellan webbplatser.
* **Länk att återskapa** - Länken till sidan där sårbarheten påträffades.

## Föreslå automatiskt

![Föreslå affärsmöjlighet mellan webbplatser automatiskt](./assets/cross-site-scripting/auto-suggest.png){align="center"}

* **Föreslagen korrigering** - Ett AI-genererat förslag på hur du ska åtgärda säkerhetsluckan.

## Optimera [!BADGE Ultimate] automatiskt{type=Positive tooltip="Ultimate"}


>[!BEGINTABS]

>[!TAB Distribuera optimering]

{{auto-optimize-deploy-optimization-slack}}

>[!TAB Begär godkännande]

{{auto-optimize-request-approval}}

>[!ENDTABS]
