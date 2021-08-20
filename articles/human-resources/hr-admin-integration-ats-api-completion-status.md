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
ms.openlocfilehash: 67e464262897d89f80bd615156d56cc12a822dd4a0dfa6d5eb206c38ddd61ec5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732881"
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