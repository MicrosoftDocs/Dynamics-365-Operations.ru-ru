---
title: Начальная дата создаваемой периодичности отбора
description: В этом разделе описывается набор параметров начальной даты создаваемой частоты отбора для Dynamics 365 Human Resources.
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
ms.openlocfilehash: bee0522ea244cab2f5d6864b2a763df6e314e02d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805162"
---
# <a name="screening-frequency-generate-from"></a>Начальная дата создаваемой периодичности отбора

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