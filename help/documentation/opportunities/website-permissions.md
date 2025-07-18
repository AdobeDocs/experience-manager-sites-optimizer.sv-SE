---
title: Dokumentation för webbplatsbehörigheter för affärsmöjligheter
description: Läs mer om möjligheterna till webbplatsbehörigheter och hur du använder dem för att öka säkerheten på din webbplats.
badgeSecurityPosture: label="Säkerhetsposition" type="Caution" url="../../opportunity-types/security-posture.md" tooltip="Säkerhetsposition"
source-git-commit: cb64a34b758de8f5dcea298014ddd0ba79a24c17
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---


# Webbplatsbehörigheter - möjlighet

![Behörighetsmöjlighet för webbplats](./assets/website-permissions/hero.png){align="center"}

Webbplatsbehörigheterna kan optimera webbplatsbehörigheter, vilket är avgörande för att en säker och hanterbar AEM-miljö ska kunna upprätthållas. Med den här möjligheten kan du förfina åtkomstkontroller genom att ta bort alltför breda behörigheter, som `jcr:all` på generiska sökvägar som `/` eller `/content`, och anpassa användaråtkomst till principen om minst behörighet. Genom att effektivisera behörigheter och eliminera redundans kan du minska säkerhetsriskerna, förbättra underhållet och förhindra framtida felkonfigurationer. Granska och uppdatera behörigheter i AEM Security Permissions console eller i koddatabasen. På så sätt får användarna bara den åtkomst de verkligen behöver.

## Automatisk identifiering

![Identifiera webbplatsbehörigheter automatiskt](./assets/website-permissions/auto-identify.png){align="center"}

Funktionen **Behörighetsmöjlighet** för webbplatser identifierar och visar automatiskt

* **Användare** - Användarkontot med osäker behörighet.
* **Sökväg** - Använd flikarna längst upp för att ordna och filtrera affärsmöjligheter efter status.
* **Behörighet** - Den misstänkta behörigheten.
* **Problem** - Anger vilken typ av problem som påverkar behörigheten.

## Föreslå automatiskt

![Föreslå webbplatssårbarheter automatiskt](./assets/website-permissions/auto-suggest.png){align="center"}

Automatiskt förslag ger AI-genererade rekommendationer i fältet **Föreslagna behörigheter**, så att du kan ersätta flaggade behörigheter med säkra alternativ.

## Automatisk optimering

[!BADGE Ultimate]{type=Positive tooltip="Ultimate"}

![Optimera webbplatsbehörigheter automatiskt](./assets/website-permissions/auto-optimize.png){align="center"}

Sites Optimizer Ultimate lägger till möjligheten att driftsätta automatisk optimering för de sårbarheter som hittas.

>[!BEGINTABS]

>[!TAB Distribuera optimering]

{{auto-optimize-deploy-optimization-slack}}

>[!TAB Begär godkännande]

{{auto-optimize-request-approval}}

>[!ENDTABS]
