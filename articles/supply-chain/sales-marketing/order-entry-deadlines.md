---
title: Крайние сроки ввода заказа
description: Эта статья содержит сведения о крайних сроках ввода заказа. Крайний срок ввода заказа — это крайнее время, которое определяет, обрабатывается ли (и выполняется ли) заказ клиента, как если бы он был получен в текущий день или на следующий день.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventOrderEntryDeadlineGroup, InventOrderEntryDeadlineParameters, InventOrderEntryDeadlineTable, MCRAutoTaxRules
audience: Application User
ms.reviewer: kamaybac
ms.custom: 7151
ms.assetid: bbc4f9a2-df4b-4d92-9f18-25282a85541f
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 71748cb05346f7a31f51baebb86b9accc11c8478
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580536"
---
# <a name="order-entry-deadlines"></a>Крайние сроки ввода заказа

[!include [banner](../includes/banner.md)]

Эта статья содержит сведения о крайних сроках ввода заказа. Крайний срок ввода заказа — это крайнее время, которое определяет, обрабатывается ли (и выполняется ли) заказ клиента, как если бы он был получен в текущий день или на следующий день.

Во многих компаниях только заказы на продажу, полученный до конкретного времени дня, рассматриваются как полученные в этот день. Все заказы, которые получены после этого времени, обрабатываются, как если бы они были получены на следующий рабочий день. Это время отсечки для заказов называется крайним сроком ввода заказа.  

Крайние сроки ввода заказа используются как входные данные для резервирования по заказу. Поэтому они помогают управлять ожиданиями клиентов о поставках заказов. Например, клиенты могут увидеть что если они размещают заказ до определенного времени, то вы обязуетесь отгрузить товары в тот же день. Однако если они пропускают этот крайний срок, то они могут ожидать поставку только на следующий рабочий день. Вы устанавливайте крайние сроки ввода заказа на основе возможностей вашего склада и графиков перевозчика.  

Крайние сроки ввода заказов для всех дней недели устанавливаются на странице **Крайние сроки ввода заказа**. Если заказы получены после указанное времени, они обрабатываются, как если бы они были получены на следующий рабочий день. По умолчанию это время установлено как 23:59 (то есть за одну минуту до полуночи в конце соответствующего дня). Время по умолчанию можно изменить так, чтобы оно совпадало с действительными сроками отгрузки или прихода.  

Можно определить крайние сроки ввода заказов для конкретной группы клиентов. Например, вы можете захотеть разрешить определенной группе клиентов крайние сроки ввода заказов, которые будут позже, чем для других клиентов. В этом случае вы сперва определяете группы для крайних сроков ввода заказа на странице **Группы крайнего срока ввода заказа на продажу**. Затем вы назначаете группы к клиентам на странице **Клиенты**.  

Если компания состоит из нескольких подразделений, можно настроить крайние сроки ввода заказа для каждого подразделения. Если подразделения расположены в разных часовых поясах, крайние сроки ввода заказа настраивается для часового пояса каждого подразделения. Однако при работе с заказами на продажу и предложениям по продажам крайний срок ввода заказа на странице **Доступные даты отгрузки и прихода** преобразуется во время вашего часового пояса.  

На странице **Активизировать комбинации крайнего срока ввода заказа на продажу** вы определяете разрешенные сочетания подразделений и групп крайнего срока ввода заказа.

## <a name="example-order-entry-deadline"></a>Пример: крайний срок ввода заказа
Крайний срок ввода заказа во вторник был установлен равным 16:00. В некоторый вторник в 17:00 вы пытаетесь установить текущую дату как дату отгрузки. (Обратите внимание, что этом примере время упреждения отсутствует.) Если установлен флажок **Контроль даты поставки**, вы получаете предупреждение о том, что дата недопустима. Это предупреждение появляется на странице **Доступные даты отгрузки и прихода**, где вы можете после этого выбрать альтернативные даты.

## <a name="example-different-order-entry-deadlines-per-site"></a>Пример: различные крайние сроки ввода заказа для разных подразделений
Компания состоит из двух подразделений. Подразделения расположены в различных часовых поясах, как показано в следующей таблице.

| Подразделение A                      | Подразделение B                      |
|-----------------------------|-----------------------------|
| Калифорния                  | Флорида                     |
| Тихоокеанское стандартное время (PST) | Восточное стандартное время (EST) |

Подразделения А и В определили следующие крайние сроки ввода заказов.

| День недели             | A: Крайние сроки ввода заказа (PST) | B: Крайние сроки ввода заказа (EST) |
|-----------------------------|--------------------------------|--------------------------------|
| Понедельник                      | 13:00                          | 14:00:00                          |
| Вторник                     | 13:00                          | 14:00:00                          |
| Среда                   | 13:00                          | 14:00:00                          |
| Четверг                    | 13:00                          | 14:00:00                          |
| Пятница                      | 13:00                          | 14:00:00                          |

Вы — специалист по обработке заказов в штате Юта, в часовом поясе MST (горное стандартное время). Поэтому если вы размещаете заказы для подразделения A до 14:00 по MST и для подразделения B до 12:00 по MST, вы соблюдаете крайние сроки ввода заказов для обоих подразделений.  

В приведенной ниже таблице показано, как крайние сроки ввода заказов для подразделений А и В преобразуются во время часового пояса MST.

| Подразделение A: (PST)         | Подразделение A: (MST)        | Подразделение B: (EST)           | Подразделение B: (MST)        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00               | 14:00:00              | 14:00:00                 | 12:00:00              |

**Примечание.** Если действует летнее время, крайние сроки ввода заказов соответствующим образом корректируются.

## <a name="example-same-order-entry-deadline-per-site"></a>Пример: одинаковые крайние сроки ввода заказов для подразделений
Компания состоит из двух подразделений. Подразделения расположены в различных часовых поясах, как показано в следующей таблице.

| Подразделение A                      | Подразделение B                      |
|-----------------------------|-----------------------------|
| Калифорния                  | Флорида                     |
| Тихоокеанское стандартное время (PST) | Восточное стандартное время (EST) |

Подразделения А и В определили следующие крайние сроки ввода заказов.

| День недели | Тихоокеанское стандартное время (PST) и восточное стандартное время (EST) |
|-----------------|-------------|
| Понедельник          | 13:00       |
| Вторник         | 13:00       |
| Среда       | 13:00       |
| Четверг        | 13:00       |
| Пятница          | 13:00       |

Вы — специалист по обработке заказов в штате Юта, в часовом поясе MST. Поэтому если вы размещаете заказы для подразделения A до 14:00 по MST и для подразделения B до 11:00 по MST, вы соблюдаете крайние сроки ввода заказов для обоих подразделений. 

В приведенной ниже таблице показано, как крайние сроки ввода заказов для подразделений А и В преобразуются во время часового пояса MST.

| Подразделение A: (PST)         | Подразделение A: (MST)        | Подразделение B: (EST)           | Подразделение B: (MST)        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00               | 14:00:00              | 13:00                 | 11:00:00              |

**Примечание.** Если действует летнее время, крайние сроки ввода заказов соответствующим образом корректируются.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Графики поставки](delivery-schedules.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]