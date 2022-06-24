---
title: Статус позиции по запросу на набор сотрудников
description: В этой статье описывается набор параметров "Статус позиции по запросу на набор сотрудников" для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 736bdbfb8759ab61202d1f17e3cdc8294be0ba84
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846424"
---
# <a name="recruiting-request-position-status"></a>Статус позиции по запросу на набор сотрудников


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой статье описывается набор параметров "Статус позиции по запросу на набор сотрудников" для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmrecruitingrequestpositionstatus

Это перечисление предоставляет набор параметров для значений статуса для каждой должности запрос на набор персонала в сущности RecruitingRequestPosition.

| значение | Этикетка | описание |
| --- | --- | --- |
| 200000000 | Открытые | Должность в запросе на набор персонала открыта для набора сотрудников. Это не означает, что для данной должности нет активного в данный момент назначения должности. В должности на момент набора персонала может существовать сотрудник. Оно указывает только на то, что должность доступна для найма в контексте запроса на набор сотрудников. |
| 200000001 | Занята | Сотрудник, выбранный для назначения на данную должность. |
| 200000002 | Отменено | Запрос на набор сотрудников для этой должности отменен. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса для запроса на набор персонала](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
