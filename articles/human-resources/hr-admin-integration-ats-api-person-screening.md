---
title: Отбор для лица
description: В этом разделе описывается сущность отбора физического лица для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 5129348f928fd709a5fabe73917522799a2d47e0
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066301"
---
# <a name="person-screening"></a>Отбор для лица


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе описывается сущность отбора физического лица для Dynamics 365 Human Resources.

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
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Код сущности отбора для физического лица**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | Только для чтения<br>Требуется<br>Создано системой | Уникальный первичный идентификатор записи отбора физического лица. |
| **Номер субъекта**<br>mshr_partynumber<br>*Строка* | Чтение/запись<br>Требуется | Номер субъекта (лица), связанный с кандидатом. |
| **Значение ИД физического лица**<br>_mshr_fk_person_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_dirpersonentityid сущности mshr_dirpersonentity | Созданный системой уникальный идентификатор записи сущности субъекта (физического лица). |
| **ИД типа отбора**<br>mshr_screeningtypeid<br>*Строка* | Чтение/запись<br>Требуется<br>Внешний ключ: ScreeningType | Идентификатор типа отбора, определенный в модуле Human Resources. |
| **Значение ИД типа отбора**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmscreeningtypeentityid сущности mshr_hcmscreeningtypeentity | Созданный системой идентификатор для записи типа отбора в связанной сущности. |
| **Требуется к**<br>mshr_requiredby<br>*Дата и время* | Чтение/запись<br>Необязательный | Дата, к которой требуется завершить отбор. |
| **Состояние**<br>mshr_status<br>*Набор параметров mshr_hcmcompletionstatus*<br>Чтение/запись<br>Требуется | Предоставляет статус кандидата для отбора. |
| **Дата завершения**<br>mshr_completeddate<br>*Дата и время* | Чтение/запись<br>Необязательный | Дата завершения отбора. |
| **Основание**<br>mshr_note<br>*Строка* | Чтение/запись<br>Необязательный | Примечания для использования сотрудниками или менеджерами по найму персонала. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
