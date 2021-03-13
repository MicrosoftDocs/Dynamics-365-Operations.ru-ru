---
title: Сертификат физического лица
description: В этом разделе описывается сущность сертификата физического лица для Dynamics 365 Human Resources.
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
ms.openlocfilehash: fa4582dc00341a647f1ea43ed16d9dce8bfcf688
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125361"
---
# <a name="person-certificate"></a>Сертификат физического лица

В этом разделе описывается сущность сертификата физического лица для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmpersoncertificateentity

## <a name="description"></a>описание

Эта сущность описывает профессиональные сертификаты кандидата.

## <a name="json-representation"></a>Представление JSON

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Код сущности сертификата физического лица**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | Только для чтения<br>Требуется | Созданный системой уникальный идентификатор для записи сущности сертификата физического лица. |
| **Номер субъекта**<br>mshr_partynumber<br>*Строка* | Чтение/запись<br>Требуется | ИД субъекта (физического лица) кандидата. |
| **Значение ИД физического лица**<br>_mshr_fk_person_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_dirpersonentityid сущности mshr_dirpersonentity | Созданный системой уникальный идентификатор записи сущности субъекта (физического лица). |
| **ИД типа сертификата**<br>mshr_certificatetypeid<br>*Строка* | Чтение/запись<br>Требуется |  Идентификатор типа сертификата, определенный в модуле Human Resources. |
| **Значение ИД типа сертификата**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmcertificatetypeentityid сущности mshr_hcmcertificatetypeentity | Созданный системой уникальный идентификатор типа сертификата в связанной сущности. |
| **Дата начала**<br>mshr_startdate<br>*Дата и время* | Чтение/запись<br>Требуется | Дата выпуска сертификата. |
| **Дата окончания**<br>mshr_enddate<br>*Дата и время* | Чтение/запись<br>Необязательный | Дата окончания срока действия сертификата. |
| **Основание**<br>mshr_notes<br>*Строка* | Чтение/запись<br>Необязательный | Примечания для использования сотрудниками или менеджерами по найму персонала. |
| **Основное поле**<br>mshr_primaryfield<br>*Строка* | Только для чтения<br>Требуется |  Поле для, использования в качестве идентификатора записи сущности. Комбинация номера субъекта, ИД типа сертификата и даты начала. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

