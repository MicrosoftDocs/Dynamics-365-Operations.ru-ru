---
title: Интегрированный налог
description: Эта статья описывает интеграцию налоговых данных между приложениями для управления финансами и операциями и Dataverse.
author: josaw
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8f148b710e2294edf1e402b9b8b22cb24e60a1f2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288805"
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

