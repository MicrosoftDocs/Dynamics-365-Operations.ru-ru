---
title: Идентификационный номер физического лица
description: В этой статье описывается сущность "Идентификационный номер физического лица" для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 2d3641ffede29b7fda904ffb6cd70cb33d7800d4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858282"
---
# <a name="person-identification-number"></a>Идентификационный номер физического лица


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой статье описывается сущность "Идентификационный номер физического лица" для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmpersonidentificationnumberentity

## <a name="description"></a>описание

Эта сущность описывает идентификационные номера для кандидата. Она позволяет потребителю API записывать идентификационные номера, такие как номера социального страхования или номера паспортов, в запись кандидата. Идентификационные номера выводятся в записи работника, но не в записи кандидата. Интегрирующее приложение может записать значения в базу данных Human Resources, но эти номера не будут видны в модуле Human Resources до тех пор, пока не будет создана запись работника для кандидата.

## <a name="json-representation"></a>Представление JSON

```json
{
    "mshr_entrytype": "String",
    "mshr_description": "String",
    "mshr_expirationdate": "Datetime",
    "mshr_isprimary": Int,
    "mshr_identificationnumber": "String",
    "mshr_partynumber": "String",
    "mshr_identificationtypeid": "String",
    "mshr_issuingagencyid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_issuingagency_id_value": "Guid",
    "_mshr_fk_identificationtype_id_value": "Guid",
    "mshr_hcmpersonidentificationnumberentityid": "Guid",
    "mshr_issueddate": "Datetime"
}
```

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **ИД сущности личного идентификационного номера физического лица**<br>mshr_hcmpersonidentificationnumberentityid<br>*GUID* | Только для чтения<br>Требуется<br>Создано системой | Уникальный первичный идентификатор записи идентификационного номера физического лица. |
| **Тип записи**<br>mshr_entrytype<br>*Строка* | Чтение-запись<br>Необязательный | Свободное значение для ссылки на тип записи для идентификационного номера. |
| **Описание**<br>mshr_description<br>*Строка* | Чтение-запись<br>Необязательный | Описание идентификационного номера. |
| **Дата окончания срока действия**<br>mshr_expirationdate<br>*Дата и время* | Чтение-запись<br>Необязательный | Дата истечения срока действия идентификационного номера или связанного документа. |
| **Является основным**<br>mshr_isprimary<br>*Набор параметров mshr_noyes* | Чтение-запись<br>Необязательный | Определяет, является ли идентификационный номер основной записью для физического лица с данным типом идентификатора. |
| **Идентификационный номер**<br>mshr_identificationnumber<br>*Строка* | Чтение-запись<br>Требуется | Идентификационный номер. |
| **Номер субъекта**<br>mshr_partynumber<br>*Строка* | Чтение-запись<br>Требуется | Идентификатор субъекта (физического лица), которому принадлежит идентификационный номер. |
| **Значение ИД физического лица**<br>_mshr_fk_person_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_dirpersonentityid сущности mshr_dirpersonentity | Уникальный идентификатор субъекта (физического лица). |
| **ИД типа документа**<br>mshr_identificationtypeid<br>*Строка* | Чтение-запись<br>Требуется | Тип идентификационного номера. |
| **Значение ИД типа документа**<br>_mshr_fk_identificationtype_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_hcmidentificationtypeentityid сущности mshr_hcmidentificationtypeentity | Созданный системой уникальный идентификатор типа идентификатора. |
| **ИД выдавшего агентства**<br>mshr_issuingagencyid<br>*Строка* | Чтение-запись<br>Необязательный | Агентство или организация, выдавшая идентификационный номер. |
| **Значение ИД выдавшего агентства**<br>_mshr_fk_issuingagency_id_value<br>*GUID* | Только для чтения<br>Необязательный<br>Внешний ключ: mshr_hcmissuingagencyentityid сущности mshr_hcmissuingagencyentity | Созданный системой уникальный идентификатор агенства, выдавшено идентификационный номер. |
| **Основное поле**<br>mshr_primaryfield<br>*Строка* | Только для чтения<br>Требуется | Поле для, использования в качестве идентификатора записи сущности. Комбинация номера субъекта, ИД типа идентификации и идентификационного номера. |
| **Дата выпуска**<br>mshr_issuedate<br>*Дата* | Чтение-запись<br>Необязательный | Дата выпуска идентификационного номера. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
