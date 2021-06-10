---
title: Статус выполнения
description: В этом разделе описывается набор параметров статуса выполнения для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 54ad5cc8f5f18d57b6713304cceb985acfdc93d1
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055372"
---
# <a name="completion-status"></a>Статус выполнения

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе описывается набор параметров статуса выполнения для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmcompletionstatus

Это перечисление предоставляет набор параметров значений статуса для отбора (осмотра) кандидатов. 

| значение | Этикетка | описание |
| --- | --- | --- |
| 200000000 | Не завершено | Этот кандидат еще не проходил отбор. |
| 200000001 | Пропустить | Кандидат прошел отбор. |
| 200000002 | Сбой | Кандидат не смог пройти отбор. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]