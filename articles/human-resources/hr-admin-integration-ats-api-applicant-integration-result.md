---
title: Результат интеграции кандидата
description: В этом разделе описывается набор параметров результата интеграции заявителя для Dynamics 365 Human Resources.
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
ms.openlocfilehash: dd25eca9cccf46ec4e4bb2a1d948ca98985e73e4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467561"
---
# <a name="applicant-integration-result"></a>Результат интеграции кандидата

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе описывается набор параметров результата интеграции заявителя для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmapplicantintegrationresult

Это перечисление предоставляет статус для записи кандидата.

| значение | Этикетка | описание |
| --- | --- | --- |
| 200000000 | Не обработано | Кандидат все еще находится в процессе рассмотрения. |
| 200000001 | Принят | Кандидат был принят на работу. |
| 200000002 | Не принят на работу | Принято решение не нанимать кандидата. |
| 200000003 | Отменено | Кандидат был исключен из рассмотрения. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]