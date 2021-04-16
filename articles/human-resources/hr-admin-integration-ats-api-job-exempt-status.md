---
title: Состояние освобождения должности от доплат за сверхурочное время
description: В этом разделе описывается набор параметров состояния освобождения должности от доплат за сверхурочное время для Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4765858f389f28467ae2ac71084c15d2ba0cbe8b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798305"
---
# <a name="job-exempt-status"></a>Состояние освобождения должности от доплат за сверхурочное время

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе описывается набор параметров состояния освобождения должности от доплат за сверхурочное время для Dynamics 365 Human Resources.

Физическое имя: cdm_jobexemptstatus

Это перечисление указывает набор параметров для значений состояния освобождения должности от доплат за сверхурочное время в соответствии с FLSA. Это предусмотрено в существующем наборе параметров cdm_jobexemptstatus.

| значение | Этикетка | описание |
| --- | --- | --- |
| 200000000 | Освобождается | Должность имеет статус освобожденной от доплат за сверхурочное время в соответствии с рекомендациями FLSA. |
| 200000001 | NonExempt | Должность имеет статус не освобожденной от доплат за сверхурочное время в соответствии с рекомендациями FLSA. |
| 200000002 | Не применяется | Рекомендации по статусу FLSA не относятся к этой должности. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса для запроса на набор персонала](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]