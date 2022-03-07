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
ms.openlocfilehash: b98f25cb0129c2723a5a9e86839db0b0958bbb11
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054076"
---
# <a name="screening-frequency"></a>Частота отбора

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