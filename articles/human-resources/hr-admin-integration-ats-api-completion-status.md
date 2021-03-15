---
title: Статус выполнения
description: В этом разделе описывается набор параметров статуса выполнения для Dynamics 365 Human Resources.
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
ms.openlocfilehash: e9024e00b5d25117fd255084609c4f8db9284f32
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125697"
---
# <a name="completion-status"></a>Статус выполнения

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