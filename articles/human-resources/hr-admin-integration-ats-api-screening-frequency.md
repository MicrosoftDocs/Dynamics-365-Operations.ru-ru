---
title: Частота отбора
description: В этом разделе описывается набор параметров частоты отбора для Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba1fba598bca088e67d8cb2865d1ea9baa97f19e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801271"
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