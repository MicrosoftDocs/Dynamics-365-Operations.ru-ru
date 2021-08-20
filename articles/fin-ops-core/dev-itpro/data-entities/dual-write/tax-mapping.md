---
title: Интегрированный налог
description: Эта тема описывает интеграцию данных налога между Finance and Operations и Dataverse.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: rhaertle
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: c7e76294944196670ed4b02ebf785c1bed7b5106f73d4b66a15a19c9a4235cbf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738560"
---
# <a name="integrated-tax"></a>Интегрированный налог

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Данные настройки налога определяют настройку для как косвенных налогов (НДС, GST, налог), так и подоходного налога. В нем описывается правило расчета налогов, налоговая ставка, налоговый учет, сопоставление и другие концепции.

## <a name="templates"></a>Шаблоны

Данные налога включают коллекцию сопоставлений таблиц, которые работают совместно во время взаимодействия данных клиентов, как показано в следующей таблице.

| Приложения Finance and Operations | Приложения для взаимодействия с клиентами | описание |
|-----------------------------|-----------------------------------|-------------|
[Налоговая группа номенклатур](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Налоговые органы](mapping-reference.md#193) | msdyn_taxauthorities | |
[CDS объекта кода налогового освобождения](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[Налоговые группы](mapping-reference.md#195) | msdyn_taxgroups | |
[Группы разноски ГК для налога V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Коды подоходного налога](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Группы подоходного налога](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
