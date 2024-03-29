---
title: Опыт работы физического лица
description: В этой статье описывается сущность "Опыт работы физического лица" для Dynamics 365 Human Resources.
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
ms.openlocfilehash: d306213e4c647ecd4be98598cba92376aba0d5bb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856435"
---
# <a name="person-professional-experience"></a>Опыт работы физического лица


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой статье описывается сущность "Опыт работы физического лица" для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmpersonprofessionalexperienceentity

## <a name="description"></a>описание

Эта сущность описывает профессиональный опыт или историю работы кандидата.

## <a name="json-representation"></a>Представление JSON

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **ИД сущности опыта работы физического лица**<br>mshr_hcmpersonprofessionalexperienceentityid<br>*GUID* | Только для чтения<br>Требуется | Созданный системой уникальный идентификатор записи сущности. |
| **Номер субъекта**<br>mshr_partynumber<br>*Строка* | Чтение/запись<br>Требуется | Уникальный идентификатор записи физического лица для кандидата. |
| **Значение ИД физического лица**<br>_mshr_fk_person_id_value<br>*GUID* | Только для чтения<br>Требуется<br>Внешний ключ: mshr_dirpersonentityid сущности mshr_dirpersonentity | Созданный системой уникальный идентификатор записи сущности физического лица. |
| **Должность работодателя**<br>mshr_employerposition<br>*Строка* | Чтение/запись<br>Требуется | Заголовок должности, занимаемой кандидатом во время занятости. |
| **Имя работодателя**<br>mshr_employername<br>*Строка* | Чтение/запись<br>Требуется | Имя работодателя. |
| **Местоположение работодателя**<br>mshr_employerlocation<br>*Строка* | Чтение/запись<br>Необязательный | Местоположение работодателя. Максимальная длина: 60. Особый формат не определен и не требуется. |
| **Телефон**<br>mshr_phone<br>*Строка* | Чтение/запись<br>Необязательный | Номер телефона работодателя. |
| **URL**<br>mshr_url<br>*Строка* | Чтение/запись<br>Необязательный | URL-адрес веб-сайта работодателя. |
| **Дата начала**<br>mshr_startdate<br>*Дата и время* | Чтение/запись<br>Требуется | Дата начала работы кандидата. |
| **Дата окончания**<br>mshr_enddate<br>*Дата и время* | Чтение/запись<br>Необязательный | Дата окончания работы кандидата или значение NULL, если кандидат все еще работает здесь. |
| **Разрешить связываться с работодателем**<br>mshr_allowcontactemployer<br>*Набор параметров mshr_hrmblankyesno* | Чтение/запись<br>Необязательный | Указывает, разрешает ли кандидат связь с предыдущим работодателем. |
| **Основание**<br>mshr_note<br>*Строка* | Чтение/запись<br>Необязательный | Примечания для использования сотрудником или менеджером по найму персонала. |
| **Основное поле**<br>mshr_primaryfield<br>*Строка* | Только для чтения<br>Требуется | Поле, используемое в качестве первичного идентификатора записи сущности. Комбинация номера субъекта, начальной даты, должности работодателя и имени работодателя. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
