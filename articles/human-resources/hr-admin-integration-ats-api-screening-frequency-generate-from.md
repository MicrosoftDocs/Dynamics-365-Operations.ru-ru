---
title: Начальная дата создаваемой периодичности отбора
description: В этом разделе описывается набор параметров начальной даты создаваемой частоты отбора для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 27c6c62f3ac312ee502df969f25f1b16761cba03
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067812"
---
# <a name="screening-frequency-generate-from"></a>Начальная дата создаваемой периодичности отбора


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе описывается набор параметров начальной даты создаваемой частоты отбора для Dynamics 365 Human Resources.

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
