---
title: Статус освобождения должности от доплат за сверхурочное время
description: В этой статье описывается набор параметров "Статус освобождения должности от доплат за сверхурочное время"для Dynamics 365 Human Resources.
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
ms.openlocfilehash: e59a71264d50cecce4d31dfa26ad7f05ef3f34e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894682"
---
# <a name="job-exempt-status"></a>Статус освобождения должности от доплат за сверхурочное время


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой статье описывается набор параметров "Статус освобождения должности от доплат за сверхурочное время"для Dynamics 365 Human Resources.

Физическое имя: cdm_jobexemptstatus

Это перечисление указывает набор параметров для значений статуса освобождения должности от доплат за сверхурочное время в соответствии с FLSA. Это предусмотрено в существующем наборе параметров cdm_jobexemptstatus.

| значение | Этикетка | описание |
| --- | --- | --- |
| 200000000 | Освобождается | Должность имеет статус освобожденной от доплат за сверхурочное время в соответствии с рекомендациями FLSA. |
| 200000001 | NonExempt | Должность имеет статус не освобожденной от доплат за сверхурочное время в соответствии с рекомендациями FLSA. |
| 200000002 | Не применяется | Рекомендации по статусу FLSA не относятся к этой должности. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса для запроса на набор персонала](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
