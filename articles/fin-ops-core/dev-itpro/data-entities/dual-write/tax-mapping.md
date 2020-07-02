---
title: Интегрированный налог
description: Эта тема описывает интеграцию данных налога между Finance and Operations и Common Data Service.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 69521ec8c664a7025050c94105eca58f7f2c5c00
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435568"
---
# <a name="integrated-tax"></a>Интегрированный налог

[!include [banner](../../includes/banner.md)]



Данные настройки налога определяют настройку для как косвенных налогов (НДС, GST, налог), так и подоходного налога. В нем описывается правило расчета налогов, налоговая ставка, налоговый учет, сопоставление и другие концепции.

## <a name="templates"></a>Шаблоны

Данные налога включают коллекцию сопоставлений объектов, которые работают совместно во время взаимодействия данных клиентов, как показано в следующей таблице.

Приложения Finance and Operations | Приложения на основе модели в Dynamics 365 | описание |
-------------------------|---------------------------------|----|
Налоговая группа номенклатур | msdyn_taxitemgroups |
Налоговые органы | msdyn_taxauthorities |
CDS объекта кода налогового освобождения | msdyn_taxexemptcodes |
Налоговые группы | msdyn_taxgroups |
Группы разноски ГК для налога V2 | msdyn_taxpostinggroups |
Коды подоходного налога | msdyn_withholdingtaxcodes |
Группы подоходного налога | msdyn_withholdingtaxgroups | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

