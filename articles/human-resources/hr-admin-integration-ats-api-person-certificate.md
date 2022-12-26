---
title: Сертификат физического лица
description: В этой статье описывается сущность "Сертификат физического лица" для Dynamics 365 Human Resources.
author: jaredha
ms.date: 12/15/2022
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
ms.openlocfilehash: 1f9d5a8c83d9714a4d10dec16e66ab87b794b074
ms.sourcegitcommit: 69d7dd6a2d0dc7f2661c7d1f61e8874c7bde1448
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887326"
---
# <a name="person-certificate"></a>Сертификат физического лица


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой статье описывается сущность "Сертификат физического лица" для Dynamics 365 Human Resources.

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

| Свойство<br>**Физическое имя**<br>**_Тип_** | Использование | Наименование |
| --- | --- | --- |
| **ИД типа сертификата**<br>mshr_certificatetypeid<br>*Строка* | Чтение/запись<br>Требуется |  Идентификатор типа сертификата, определенный в модуле Human Resources. |
| **Дата начала**<br>mshr_startdate<br>*Дата и время* | Чтение/запись<br>Обязательное поле | Дата выпуска сертификата. |
| **Дата окончания**<br>mshr_enddate<br>*Дата и время* | Чтение/запись<br>Необязательный | Дата окончания срока действия сертификата. |
| **Основание**<br>mshr_notes<br>*Строка* | Чтение/запись<br>Необязательный | Примечания для использования сотрудниками или менеджерами по найму персонала. |
| **Номер субъекта**<br>mshr_partynumber<br>*Строка* | Чтение/запись<br>Обязательное поле | ИД субъекта (физического лица) кандидата. |
| **Основное поле**<br>mshr_primaryfield<br>*Строка* | Только для чтения<br>Обязательное поле |  Поле для, использования в качестве идентификатора записи сущности. Комбинация номера субъекта, ИД типа сертификата и даты начала. |
| **Значение ИД типа сертификата**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmcertificatetypeentityid сущности mshr_hcmcertificatetypeentity | Созданный системой уникальный идентификатор типа сертификата в связанной сущности. |
| **Значение ИД физического лица**<br>_mshr_fk_person_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_dirpersonentityid сущности mshr_dirpersonentity | Созданный системой уникальный идентификатор записи сущности субъекта (физического лица). |
| **Код сущности сертификата физического лица**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | Только для чтения<br>Требуется | Созданный системой уникальный идентификатор для записи сущности сертификата физического лица. |




## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
