---
title: Состояние освобождения должности от доплат за сверхурочное время
description: В этом разделе описывается набор параметров состояния освобождения должности от доплат за сверхурочное время для Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8e91fbb420009d5131e2faa7dbea8a302a027e0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053859"
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