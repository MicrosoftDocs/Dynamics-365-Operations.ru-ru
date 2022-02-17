---
title: Частота отбора
description: В этом разделе описывается набор параметров частоты отбора для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 83cb31f3bf9d77bca0aef36fb53d90f7ccb8fff9
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068567"
---
# <a name="screening-frequency"></a>Частота отбора


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе описывается набор параметров частоты отбора для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmfrequencyunit

Это перечисление предоставляет набор параметров со значениями частоты отбора. 

| значение | Этикетка | описание |
| --- | --- | --- |
| 200000000 Только один раз | Отбор необходим только один раз. |
| 200000001 Ежедневно | Частота отбора или обследования рассчитывается в днях. |
| 200000002 Еженедельно | Частота отбора или обследования рассчитывается в неделях. |
| 200000003 Ежемесячно | Частота отбора или обследования рассчитывается в месяцах. |
| 200000004 Ежегодно | Частота отбора или обследования рассчитывается в годах. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
