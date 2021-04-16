---
title: Тип контакта
description: В этом разделе описывается набор параметров типа контакта для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 7db2bdcc45d057ea6aa9a5f13874cd40d4611b8c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798448"
---
# <a name="contact-type"></a>Тип контакта

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этом разделе описывается набор параметров типа контакта для Dynamics 365 Human Resources.

Физическое имя: mshr_logisticselectronicaddressmethodtype

Это перечисление предоставляет набор параметров со значениями для типов контактов кандидатов. 

| значение | Этикетка | описание |
| --- | --- | --- |
| 200000000 | Не допускается | Тип не выбран. |
| 200000001 | Телефон | Номер телефона. |
| 200000002 | Адрес электронной почты | Адрес электронной почты. |
| 200000003 | URL | URL-адрес веб-сайта. |
| 200000004 | Телекс | Номер телекса. |
| 200000005 | Факс | Номер факса. |
| 200000006 | Facebook | Учетная запись Facebook. Идентифицируется кодом пользователя. |
| 200000007 | Twitter | Учетная запись Twitter. Идентифицируется по @username. |
| 200000008 | LinkedIn | Учетная запись LinkedIn. Идентифицируется по имени пользователя. |

## <a name="see-also"></a>См. также

[Введение в интерфейс API интеграции системы отслеживания кандидатов](hr-admin-integration-ats-api-introduction.md)<br>
[Пример запроса кандидата для приема на работу](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]