---
title: Отбор для лица
description: В этой статье описывается сущность "Отбор для лица" для Dynamics 365 Human Resources.
author: jaredha
ms.date: 12/05/2022
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
ms.openlocfilehash: 3c316e0381f4d407ed7c4c39b5949717b71477bd
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831899"
---
# <a name="person-screening"></a>Отбор для лица


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой статье описывается сущность "Отбор для лица" для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmpersonscreeningentity

## <a name="description"></a>описание

Эта сущность описывает отборы, которые кандидат прошел или должен пройти для приема на работу.

## <a name="json-representation"></a>Представление JSON

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "_mshr_fk_screeningtype_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Тип_** | Использование | Наименование |
| --- | --- | --- |
| **Основание**<br>mshr_note<br>*Строка* | Чтение/запись<br>Необязательный | Примечания для использования сотрудниками или менеджерами по найму персонала. |
| **Требуется к**<br>mshr_requiredby<br>*Дата и время* | Чтение/запись<br>Необязательный | Дата, к которой требуется завершить отбор. |
| **Состояние**<br>mshr_status<br>*Набор параметров mshr_hcmcompletionstatus*|Чтение/запись<br>Обязательное поле | Предоставляет статус кандидата для отбора. |
| **Номер субъекта**<br>mshr_partynumber<br>*Строка* | Чтение/запись<br>Обязательное поле | Номер субъекта (лица), связанный с кандидатом. |
| **ИД типа отбора**<br>mshr_screeningtypeid<br>*Строка* | Чтение/запись<br>Требуется<br>Внешний ключ: ScreeningType | Идентификатор типа отбора, определенный в модуле Human Resources. |
| **Значение ИД типа отбора**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmscreeningtypeentityid сущности mshr_hcmscreeningtypeentity | Созданный системой идентификатор для записи типа отбора в связанной сущности. |
| **Основное поле**<br>mshr_primaryfield<br>*Строка* |  Только для чтения<br>Обязательное поле | Поле для, использования в качестве идентификатора записи сущности. |
| **Значение ИД физического лица**<br>_mshr_fk_person_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_dirpersonentityid сущности mshr_dirpersonentity | Созданный системой уникальный идентификатор записи сущности субъекта (физического лица). |
| **Код сущности отбора для физического лица**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | Только для чтения<br>Требуется<br>Создано системой| Уникальный первичный идентификатор записи отбора физического лица. |
| **Дата завершения**<br>mshr_completeddate<br>*Дата и время* | Чтение/запись<br>Необязательный | Дата завершения отбора. |


## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
