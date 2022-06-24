---
title: Начальная дата создаваемой периодичности отбора
description: В этой статье описывается набор параметров "Начальная дата создаваемой периодичности отбора" для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 846a35a2e8ca39ed9479601d99c8c515328d8ce5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879318"
---
# <a name="screening-frequency-generate-from"></a>Начальная дата создаваемой периодичности отбора


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой статье описывается набор параметров "Начальная дата создаваемой периодичности отбора" для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmfrequencygeneratefrom

Это перечисление предоставляет набор параметров со значениями, определяющими начальную дату вычисления для следующего необходимого отбора.

| значение | Этикетка | описание |
| --- | --- | --- |
| 200000000 Не выбрано | Значение не было выбрано. |
| 200000001 Дата завершения | Расчет выполняется по последней дате выполнения отбора. |
| 200000002 Требуемая дата | Расчет выполняется по последней требуемой дате отбора. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
