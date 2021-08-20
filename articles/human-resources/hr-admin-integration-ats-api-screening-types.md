---
title: Типы отбора
description: В этом разделе описываются типы отбора для Dynamics 365 Human Resources.
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
ms.openlocfilehash: a7e726f88eb5c00fef98256de7a8f924156ba8f52392bc4dc6ae6e7914227152
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782176"
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