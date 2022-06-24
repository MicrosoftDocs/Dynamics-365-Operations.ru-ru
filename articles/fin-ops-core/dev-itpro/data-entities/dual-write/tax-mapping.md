---
title: Интегрированный налог
description: Эта статья описывает интеграцию налоговых данных между Finance and Operations и Dataverse.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8864a9567d57739aa72fa1859f5cfce6df33e8f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864553"
---
# <a name="integrated-tax"></a>Интегрированный налог

[!include [banner](../../includes/banner.md)]



Данные настройки налога определяют настройку для как косвенных налогов (НДС, GST, налог), так и подоходного налога. В нем описывается правило расчета налогов, налоговая ставка, налоговый учет, сопоставление и другие концепции.

## <a name="templates"></a>Шаблоны

Данные налога включают коллекцию сопоставлений таблиц, которые работают совместно во время взаимодействия данных клиентов, как показано в следующей таблице.

| Приложения Finance and Operations | Приложения для взаимодействия с клиентами | Описание |
|-----------------------------|-----------------------------------|-------------|
[Налоговая группа номенклатур](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Налоговые органы](mapping-reference.md#193) | msdyn_taxauthorities | |
[CDS объекта кода налогового освобождения](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[Налоговые группы](mapping-reference.md#195) | msdyn_taxgroups | |
[Группы разноски ГК для налога V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Коды подоходного налога](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Группы подоходного налога](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
