---
title: Состояние освобождения должности от доплат за сверхурочное время
description: В этом разделе описывается набор параметров состояния освобождения должности от доплат за сверхурочное время для Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0cd6ffc01793c8ff12e36175c7c9feaf8a4b3cdf
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125577"
---
# <a name="job-exempt-status"></a>Состояние освобождения должности от доплат за сверхурочное время

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
