---
title: Тип сертификата
description: В этом разделе описывается сущность типа сертификата для Dynamics 365 Human Resources.
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
ms.openlocfilehash: fe5713b6b5f38ad7f6857b36c6b2f63a1dc0c320
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798401"
---
# <a name="certificate-type"></a>Тип сертификата

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе описывается сущность типа сертификата для Dynamics 365 Human Resources.

Физическое имя: mshr_hcmcertificatetypeentity

## <a name="description"></a>описание

Эта сущность определяет список профессиональных типов сертификатов, настроенных в Human Resources. Эта сущность не связана с конкретным юридическим лицом (компанией).

## <a name="json-representation"></a>Представление JSON

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a>Свойства

| Свойство<br>**Физическое имя**<br>**_Вид_** | Использование | описание |
| --- | --- | --- |
| **Код сущности типа сертификата**<br>mshr_hcmcertificatetypeentityid<br>*GUID* | Только для чтения<br>Требуется 
Создано системой | Уникальный первичный идентификатор для типа сертификата. |
| **Тип сертификата**<br>mshr_certificatetype<br>*Строка* | Чтение/запись<br>Требуется | Уникальный определенный пользователем идентификатор для типа сертификата. |
| **Описание**<br>mshr_description<br>*Строка* | Чтение/запись<br>Требуется | Описание типа сертификата. |
| **Требует возобновления**<br>mshr_requirerenewal<br>*Набор параметров mshr_noyes* | Чтение/запись<br>Необязательный | Указывает, требуется ли обновление для сертификата. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]