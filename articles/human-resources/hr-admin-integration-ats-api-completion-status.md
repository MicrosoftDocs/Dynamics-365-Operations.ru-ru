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
ms.openlocfilehash: da91084d30873b79033d789beab829da9fbdb010
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065554"
---
# <a name="completion-status"></a>Статус выполнения


[!INCLUDE [PEAP](../includes/peap-1.md)]

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
