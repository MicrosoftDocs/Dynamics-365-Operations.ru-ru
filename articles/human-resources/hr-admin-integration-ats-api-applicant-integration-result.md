---
title: Результат интеграции кандидата
description: В этой статье описывается набор параметров "Результат интеграции кандидата" для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 84f0ba9b197866935535a68006cfdb8c18fa3ad1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902324"
---
# <a name="applicant-integration-result"></a>Результат интеграции кандидата


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой статье описывается набор параметров "Результат интеграции кандидата" для Dynamics 365 Human Resources.

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
