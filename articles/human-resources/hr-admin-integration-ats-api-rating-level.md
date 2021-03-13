---
title: Уровень рейтинга
description: В этом разделе описывается сущность уровня рейтинга для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1ad37c7a5b961bb03d37775168dac91e606d2b08
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125265"
---
# <a name="rating-level"></a>Уровень рейтинга

В этом разделе описывается сущность уровня рейтинга для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmratinglevelentity

## <a name="description"></a>описание

Эта сущность предоставляет доступные уровни рейтинга для навыков. Уровни рейтинга применяются для всех юридических лиц.

## <a name="json-representation"></a>Представление JSON

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **ИД сущности уровня рейтинга**<br>mshr_hcmratinglevelentityid<br>*GUID* | Только для чтения<br>Требуется<br>Создано системой | Созданный системой уникальный идентификатор для уровня. |
| **Код уровня оценки**<br>mshr_ratinglevelid<br>*Строка* | Чтение/запись<br>Требуется | Понятный пользователю уникальный идентификатор для уровня. |
| **ИД модели рейтинга**<br>mshr_ratingmodelid<br>*Строка* | Чтение/запись<br>Требуется | Модель рейтинга, к которой принадлежит уровень рейтинга. |
| **ИД сущности модели рейтинга**<br>_mshr_fk_ratingmodelentity_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmratingmodelentityid сущности mshr_hcmratingmodelentity | Созданный системой идентификатор модели рейтинга, к которой принадлежит уровень рейтинга. |
| **Описание**<br>mshr_description<br>*Строка* | Чтение/запись<br>Требуется | Описание выбранного уровня рейтинга. |
| **Множитель**<br>mshr_factor<br>*Целое число* | Чтение/запись<br>Требуется | Коэффициент для уровня рейтинга. Если сравнить номенклатуры с разным числом уровней рейтинга, этот коэффициент используется для нормализации оценок. Значение должно быть целым числом от 0 до 9. |
| **Примечание**<br>mshr_note<br>*Строка* | Чтение/запись<br>Необязательный | Любые замечания, связанные с уровнем рейтинга. |
| **Основное поле**<br>mshr_primaryfield<br>*Строка* | Только для чтения<br>Требуется | Поле для, использования в качестве идентификатора записи сущности. Комбинация кода уровня рейтинга и кода модели рейтинга. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

