---
title: Статус должности запроса набора персонала
description: В этом разделе описывается набор параметров состояния должности для запроса на набор сотрудников для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 3f7bae64f58f0bdc1603b3c1b5493f1ebcfa8de9
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126058"
---
# <a name="recruiting-request-position-status"></a>Статус должности запроса набора персонала

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