---
title: Типы отбора
description: В этом разделе описываются типы отбора для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 361f8c866abb9d34eb3e2be7ea42626e98e34779
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805138"
---
# <a name="screening-types"></a>Типы отбора

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе описываются типы отбора для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmscreeningtypeentity

## <a name="description"></a>описание

Эта сущность описывает типы отбора, которые настраиваются компанией для процессов отбора сотрудников перед приемом на работу и текущего отбора.

## <a name="json-representation"></a>Представление JSON

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **ИД сущности типа отбора**<br>mshr_hcmscreeningtypeentityid<br>*GUID* | Только для чтения<br>Требуется<br>Создано системой | Уникальный первичный идентификатор записи типа отбора. |
| **ИД типа отбора**<br>mshr_screeningtypeid<br>*Строка* | Чтение/запись<br>Требуется | Определенный пользователем уникальный идентификатор для типа отбора. |
| **Описание**<br>mshr_description<br>*Строка* | Чтение/запись<br>Требуется | Описание типа отбора. |
| **Единица частоты**<br>mshr_frequencyunit<br>*Набор параметров mshr_hcmfrequencyunit* | Чтение/запись<br>Требуется | Описывает частоту, с которой необходимо выполнять отбор (обследование) для назначенного физического лица. |
| **Создать на основе**<br>mshr_generatefrom<br>*Набор параметров mshr_hcmfrequencygeneratefrom* | Чтение-запись<br>Требуется | Если значением частоты является любое значение, отличное от "Только однократно", значение GenerateFrom определяет дату, начиная с которой будет рассчитываться следующее событие отбора (обследования). |
| **Интервал частот**<br>mshr_frequencyinterval<br>*Целое число* | Чтение-запись<br>Требуется | Если значением частоты является любое значение, отличное от "Только однократно", необходимо определить интервал для единиц измерения времени между каждым событием отбора (обследования). |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]