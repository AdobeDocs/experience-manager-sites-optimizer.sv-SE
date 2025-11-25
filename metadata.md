---
solution: Experience Manager
product: adobe experience manager
type: Documentation
description: AEM Sites Optimizer dokumentation.
index: y
git-repo: https://github.com/AdobeDocs/experience-manager-sites-optimizer.sv-SE
feature-set: Experience Manager Assets,Experience Manager Sites,Experience Manager, Experience Manager Forms, Experience Manager Cloud Manager
cloud: Experience Cloud
recommendations: noDisplay
source-git-commit: 2f4ef1c6f44d602bfe365a52eb692fe7faa7f05f
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---


# Metadata för intern användning

I GitHub-redigeringssystemet ordnas metadata hierarkiskt med hjälp av följande allt vanligare nivåer.

1. metadata.md
1. TillC
1. Artikel

De metadata som definieras i filen metadata.md gäller för hela repon, men kan åsidosättas på ToC- och artikelnivå. Alla åsidosättningar av metadata bör göras på lägsta möjliga nivå.

Metadata i `experience-manager-cloud-service.en`-svaret är det minsta nödvändiga.

metadata.md

* `product`
* `git-repo`
* `index`
* `solution-title`
* `solution-hub-url`
* `getting-started-title`
* `getting-started-url`
* `tutorials-title`
* `tutorials-url`

ToCS

* `sub-product`
* `user-guide-title`

Artikel

* `title`
* `description`
* `contentOwner` (endast för kärnresursinnehåll under `/help/assets`)

