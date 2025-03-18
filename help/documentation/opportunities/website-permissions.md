---
title: Dokumentation för webbplatsbehörigheter för affärsmöjligheter
description: Läs mer om möjligheterna till webbplatsbehörigheter och hur du använder dem för att öka säkerheten på din webbplats.
badgeSecurityPosture: label="Säkerhetsposition" type="Caution" url="../../opportunity-types/security-posture.md" tooltip="Säkerhetsposition"
source-git-commit: 5d1ae616ddde74f69b73ba5b44297c14b2dea36b
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---


# Webbplatsbehörigheter - möjlighet

![Behörighetsmöjlighet för webbplats](./assets/website-permissions/hero.png){align="center"}

Webbplatsbehörigheterna kan optimera webbplatsbehörigheter, vilket är avgörande för att en säker och hanterbar AEM-miljö ska kunna upprätthållas. Med den här möjligheten kan du förfina åtkomstkontroller genom att ta bort alltför breda behörigheter, som `jcr:all` på generiska sökvägar som `/` eller `/content`, och anpassa användaråtkomst till principen om minst behörighet. Genom att effektivisera behörigheter och eliminera redundans kan du minska säkerhetsriskerna, förbättra underhållet och förhindra framtida felkonfigurationer. Vidta åtgärder genom att granska och uppdatera behörigheter i AEM säkerhetsbehörighetskonsol eller kodarkivet, så att tjänstanvändarna bara har den åtkomst de verkligen behöver.

## Automatisk identifiering

![Identifiera webbplatsbehörigheter automatiskt](./assets/website-permissions/auto-identify.png){align="center"}

Funktionen **Behörighetsmöjlighet** för webbplatser identifierar och visar automatiskt

* **Användare** - Användarkontot med osäker behörighet.
* **Sökväg** - Sökvägen i AEM som påverkas av behörigheten.
* **Behörighet** - Behörigheten som är osäker.
* **Problem** - Anger vilken typ av problem som påverkar behörigheten.

## Föreslå automatiskt

![Föreslå webbplatssårbarheter automatiskt](./assets/website-permissions/auto-suggest.png){align="center"}

Automatiskt förslag ger AI-genererade rekommendationer i fältet **Föreslagna behörigheter**, så att du kan ersätta flaggade behörigheter med säkra alternativ.

## Optimera [!BADGE Ultimate] automatiskt{type=Positive tooltip="Ultimate"}

![Optimera webbplatsbehörigheter automatiskt](./assets/website-permissions/auto-optimize.png){align="center"}

Sites Optimizer Ultimate lägger till möjligheten att driftsätta automatisk optimering för de sårbarheter som hittas.

>[!BEGINTABS]

>[!TAB Distribuera optimering]

{{auto-optimize-deploy-optimization-slack}}

>[!TAB Begär godkännande]

{{auto-optimize-request-approval}}

>[!ENDTABS]
