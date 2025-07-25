---
title: Dokumentation om affärsmöjlighet för brutna interna länkar
description: Lär dig mer om de brutna länkarna och hur du kan använda dem för att förbättra engagemanget på din webbplats.
badgeEngagement: label="Engagemang" type="Caution" url="../../opportunity-types/engagement.md" tooltip="Engagemang"
source-git-commit: cb64a34b758de8f5dcea298014ddd0ba79a24c17
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 0%

---


# Möjlighet till brutna interna länkar

![Brutna interna länkmöjligheter](./assets/broken-internal-links/hero.png){align="center"}

Brutna interna länkar påverkar sökmotorns förmåga att indexera webbplatsen och påverkar både användarupplevelsen och sökmotoroptimeringen negativt. För att åtgärda det här problemet pekar de brutna interna länkarna ut trasiga URL:er och ger förslag på giltiga länkuppdateringar. Att åtgärda dessa problem kan förbättra användarinteraktionen och säkerställa smidig navigering och tillgänglighet.

Affärsmöjligheten med brutna interna länkar visar en sammanfattning högst upp på sidan, inklusive en sammanfattning av problemet och dess inverkan på er webbplats och verksamhet.

* **Prognostiserad trafik förlorad** - Den beräknade trafikförlusten på grund av brutna interna länkar.
* **Planerat trafikvärde** - Det uppskattade värdet av förlorad trafik.

## Automatisk identifiering

<!---![Auto-identify broken internal links](./assets/missing-or-invalid-metadata/auto-identify.png){align="center"}-->

De brutna interna länkarna gör det möjligt att automatiskt identifiera och visa alla brutna interna länkar på dina sidor, och inkluderar följande:

* **Refererande sida** - Sidan som innehåller den brutna länken.
* **URL för brutet mål** - Den brutna interna länken.
* **Förslag** - Ett AI-genererat förslag om hur den brutna länken ska uppdateras. Mer information finns i avsnittet för automatiska förslag.

## Föreslå automatiskt

<!--![Auto-suggest broken internal links](./assets/broken-internal-links/auto-suggest.png){align="center"}-->

Affärsmöjligheten med brutna interna länkar ger AI-genererade förslag på hur man uppdaterar brutna länkar. De här förslagen baseras på den trasiga URL:en och ger en lämplig ersättning. Om du väljer ![Informationsikonen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_InfoOutline_18_N.svg) får du en AI-genererad logik för den föreslagna uppdateringen.


>[!BEGINTABS]

>[!TAB AI-logik]

<!--[AI rationale of broken internal links](./assets/broken-internal-links/auto-suggest-ai-rationale.png) -->

Välj ![Informationsikon](https://spectrum.adobe.com/static/icons/workflow_18/Smock_InfoOutline_18_N.svg) om du vill visa AI-logiken för den föreslagna URL:en. Motiveringen förklarar varför AI anser att den föreslagna URL:en är den lämpligaste för den brutna länken. Det kan också hjälpa er att förstå AI:s beslutsprocess och fatta ett välgrundat beslut om huruvida ni ska godkänna eller avvisa förslaget.

>[!TAB Redigera mål-URL]

<!--![Edit suggested URL of broken internal links](./assets/broken-internal-links/edit-target-url.png){align="center"}-->

Om du inte håller med om det AI-genererade förslaget kan du redigera det föreslagna länkvärdet genom att välja **redigeringsikonen**. Med den här funktionen kan du ange den önskade länken manuellt. Redigeringsfönstret innehåller länkens **brutna målsökväg**, den **önskade målsökvägen** där du kan redigera länken manuellt och ett fält med det AI-genererade förslaget. När du är klar med redigeringen klickar du på **Spara** för att uppdatera den brutna länkposten. En gul punkt visas i inmatningsfältet för att ange att länken har redigerats.

>[!TAB Ignorera poster]

<!--![Ignore broken links](./assets/broken-internal-links/ignore.png){align="center"}-->

Du kan välja att ignorera poster med de brutna URL-adresserna som mål. Om du väljer ![Ta bort ikon](https://spectrum.adobe.com/static/icons/ui_18/CrossSize500.svg) tas posten bort från affärsmöjlighetslistan. Ignorerade poster kan återkopplas från fliken **Ignorerad** högst upp på affärsmöjlighetssidan.

>[!ENDTABS]


## Automatisk optimering

[!BADGE Ultimate]{type=Positive tooltip="Ultimate"}

<!---![Auto-optimize suggested invalid or missing metadata](./assets/broken-internal-links/auto-optimize.png){align="center"}-->

Sites Optimizer Ultimate lägger till möjligheten att automatiskt optimera för de brutna länkar som affärsmöjligheten hittar. <!--- TBD-need more in-depth and opportunity specific information here. What does the auto-optimization do?-->


>[!BEGINTABS]

>[!TAB Distribuera optimering]

{{auto-optimize-deploy-optimization-slack}}

>[!TAB Begär godkännande]

{{auto-optimize-request-approval}}

>[!ENDTABS]

