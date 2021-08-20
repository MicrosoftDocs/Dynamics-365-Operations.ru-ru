---
title: Местонахождение запроса на набор сотрудников
description: В этом разделе описывается сущность местонахождения запроса на набор сотрудников для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 59b625bded2116007b353e7a6b697c30a62550d5b25d05185ecffe1401fbff27
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759751"
---
# <a name="recruiting-request-location"></a>Местонахождение запроса на набор сотрудников

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе описывается сущность местонахождения запроса на набор сотрудников для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmrecruitingrequestlocationentity

### <a name="description"></a>описание

Список местоположений, определенных как местоположения, в которых нанятые сотрудниками будут работать после приема на работу. Это местоположения, созданные для юридических лиц.

### <a name="json-representation"></a>Представление JSON

```
{
    "mshr_recruitingrequestlocationid": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_telephone": "String",
    "mshr_email": "String",
    "mshr_internetaddress": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_dataareaid": "String",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmrecruitingrequestlocationentityid": "Guid"
}
```

### <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Код местонахождения**<br>mshr_locationid<br>*Строка* | Однократная запись<br>Требуется | Созданный системой идентификатор местоположения найма на работу, удобный для восприятия пользователем. |
| **Местонахождение запроса на набор сотрудников**<br>mshr_recruitingrequestlocationid<br>*Строка* | Однократная запись<br>Требуется | Определяемый пользователем уникальный идентификатор местоположения набора персонала. |
| **Код сущности местоположения запроса на набор персонала**<br>mshr_hcmrecruitingrequestlocationentityid<br>*GUID* | Только для чтения<br>Требуется | Создаваемый системой уникальный идентификатор для записи местоположения запроса на набор сотрудников. |
| **Описание**<br>mshr_description<br>*Строка* | Чтение/запись<br>Требуется | Описание местоположения. |
| **Код страны/региона**<br>mshr_countryregionid<br>*Строка* | Только для чтения<br>Необязательный | Указывает страну или регион, гражданином которой является кандидат. |
| **Значение кода страны/региона**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Только для чтения<br>Необязательный<br>Внешний ключ: mshr_logisticaddresscountryregionentityid сущности mshr_logisticsaddresscountryregionentity | Созданный системой уникальный идентификатор страны/региона адреса. |
| **Почтовый индекс**<br>mshr_zipcode<br>*Строка* | Только для чтения<br>Необязательный | Почтовый индекс. |
| **Улица**<br>mshr_street<br>*Строка* | Только для чтения<br>Необязательный | Улица в адресе. |
| **Город**<br>mshr_city<br>*Строка* | Только для чтения<br>Необязательный | Город. |
| **Область/штат/провинция**<br>mshr_state<br>*Строка* | Только для чтения<br>Необязательный | Область, республика, край, округ. |
| **Райoн**<br>mshr_county<br>*Строка* | Только для чтения<br>Необязательный | Райoн. |
| **Телефон**<br>mshr_telephone<br>*Строка* | Чтение/запись<br>Необязательный | Номер телефона для местоположения. |
| **Электронная почта**<br>mshr_email<br>*Строка* | Чтение/запись<br>Необязательный | Адрес электронной почты. |
| **Веб-адрес**<br>mshr_internetaddress<br>*Строка* | Чтение/запись<br>Необязательный | URL-адрес веб-сайта местоположения. |
| **ИД области данных**<br>mshr_dataareaid<br>*Строка* | Чтение/запись<br>Необязательный | Указывает юридическое лицо (компанию). |
| **Значение ИД области данных**<br>_mshr_dataareaid_id_value<br>*GUID* | Только для чтения<br>Необязательный<br>Внешний ключ: cdm_companyid сущности cdm_company | Созданное системой значение GUID, идентифицирующее юридическое лицо (компанию). |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса для запроса на набор персонала](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]