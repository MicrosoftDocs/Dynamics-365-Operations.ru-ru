---
title: Статус должности запроса набора персонала
description: В этом разделе описывается набор параметров состояния должности для запроса на набор сотрудников для Dynamics 365 Human Resources.
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
ms.openlocfilehash: dee34366289f2e7ade1a1ae24bea15c0d19683d79720a44a6327879e8060a810
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725898"
---
# <a name="recruiting-request-position-status"></a>Статус должности запроса набора персонала

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе описывается набор параметров состояния должности для запроса на набор сотрудников для Dynamics 365 Human Resources.

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