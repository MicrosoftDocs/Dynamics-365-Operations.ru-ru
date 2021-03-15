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
ms.openlocfilehash: 157864cd0eee879013724615ce31306c99c5aa68
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125817"
---
# <a name="applicant-integration-result"></a>Результат интеграции кандидата

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