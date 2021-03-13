---
title: Начальная дата создаваемой периодичности отбора
description: В этом разделе описывается набор параметров начальной даты создаваемой частоты отбора для Dynamics 365 Human Resources.
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
ms.openlocfilehash: f291e28584dadc465092d99a1354fda793ff7560
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126154"
---
# <a name="screening-frequency-generate-from"></a>Начальная дата создаваемой периодичности отбора

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
