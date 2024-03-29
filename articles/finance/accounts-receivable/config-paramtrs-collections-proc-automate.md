---
title: Настройка параметров для автоматизации процессов сбора
description: В этой статье описываются параметры, влияющие на автоматизированные процессы сбора, и даются указания по их настройке таким образом, чтобы автоматические процессы соответствовали вашим намерениям и ожиданиям.
author: JodiChristiansen
ms.date: 08/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c5d0f801c47ef2d98d8ba410dc593bd7640839c1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900052"
---
# <a name="configure-parameters-for-collection-process-automation"></a>Настройка параметров для автоматизации процессов сбора

[!include [banner](../includes/banner.md)]

В этой статье описываются параметры, влияющие на автоматизированные процессы сбора, и даются указания по их настройке таким образом, чтобы автоматические процессы соответствовали вашим намерениям и ожиданиям. Сведения о том, как автоматизировать процессы сбора, см. в разделе [Автоматизация процессов сборов](collections-process-automate.md).

## <a name="general"></a>Разное
Введите число в поле **Процент клиентов по пакетной задаче**, чтобы определить количество пакетных задач для каждого процесса автоматизации. Задайте для параметра **Автоматически отправлять письма-напоминания** значение **Да**, чтобы тип действия писем-напоминаний отправлял письма во время автоматизации. Задайте для параметра **Создавать действия для автоматизации** значение **Да** для создания и закрытия действий для типов действий, не являющихся действиями, для просмотра всех автоматических шагов, выполненных по учетной записи. Определите количество дней хранения истории сбора в параметре **Число дней хранения журнала автоматизация процессов сбора**. Когда накладная достигает последнего этапа процесса сбора, она не будет использоваться для создания будущих типов действий автоматизации процессов, если для параметра **Исключить накладную после активации последнего шага процесса** установлено значение **Да**. Следующая самая старая накладная определяет шаг следующего процесса автоматизации, чтобы обеспечить продолжение действий по автоматизации процесса сбора задолженностей. 

## <a name="payment-predictions"></a>Прогнозы платежей
Начиная с версии 10.0.21, прогнозы платежей клиентов, находящиеся в Finance Insights, прогнозируют, будут ли накладные оплачены вовремя, поздно или очень поздно. Можно настроить каждую из этих категорий в Finance Insights. Если для накладных прогнозируется оплата с задержкой, важно начать процесс сбора до того момента, когда наступит срок оплаты накладной. Эти прогнозы могут использоваться для создания действий по сборам при запуске автоматизации процессов сборов. Установите для параметра **Включить прогнозы по платежам** значение **Да** для использования прогнозов платежей клиентов для создания действий по сборам, основанным на вероятности оплаты накладных с задержкой. 

Дополнительные сведения о прогнозах платежей клиентов и Finance Insights см. в разделе [Прогнозы платежей клиентов](payment-insights-overview.md).

Когда выполняется модель прогнозов платежей клиентов, она назначает прогнозу по накладной процентные доли оплаты вовремя, с задержкой или с очень большой задержкой. Эту информацию можно использовать для автоматического запуска действий по сборам с использованием автоматизации процессов сборов в случаях, когда ожидается просроченный платеж. Можно просмотреть эти проценты на странице **Прогнозы платежей по клиентам** или **Прогнозы платежей по проводкам** в разделе **Кредит и сбор задолженностей > Сборы**. 

Если средний прогноз платежа для накладной клиента меньше, чем контрольный процент, мероприятие не создается. Если прогноз платежа больше или равен контрольному проценту, создается по одному действию на каждого клиента. Для **Прогноз: с задержкой** введите **Контрольный процент**, когда автоматизация процесса сбора должна создавать действия по сборам. Это суммарное значение для оплаты с задержкой и большой задержкой. Выберите **Шаблон делового документа**, который будет использоваться для создаваемого действия, или создайте новый. Здесь указывается **Тип**, **Назначение** и **Дни до закрытия действия**. Введите любые **Примечания**, которые будут по умолчанию использоваться в качестве описания при создании действия. Для **Прогноз: с большой задержкой** введите **Контрольный процент**, когда автоматизация процесса сбора должна создавать действия по сборам для клиента, для которого прогнозируется оплата накладных с очень большой задержкой. Выберите **Шаблон делового документа**, который будет использоваться для создаваемого действия. Здесь указывается **Тип**, **Назначение** и **Дни до закрытия действия**. Введите любые **Примечания**, которые будут по умолчанию использоваться в качестве описания при создании действия. 

### <a name="example"></a>Пример
Если контрольный процент оплаты с задержкой установлен как 60%. Когда выполняются прогнозы платежей клиентов для каждой накладной, система назначает прогнозу процентные доли оплаты вовремя, с задержкой или очень большой задержкой. Если прогноз платежа, по которому накладная будет просрочена, составляет 59% или меньше, в процессе автоматического сбора для накладной не будет создано никаких действий по сборам. Если прогноз платежа клиента для накладной превышает или равно 60%, тогда действие по сбору создается во время автоматизации процессов сборов. 

> [!NOTE]
> Прогноз оплаты с очень большой задержкой оценивается до прогноза оплаты с задержкой, так как оплата с очень большой задержкой включает накладные, для которых прогнозируется оплата с задержкой. Процесс сборов генерирует только одно действие, если накладная попадает в контрольные диапазоны "с задержкой" и "с большой задержкой". В этом случае система использует действие и деловой документ для оплаты с очень большой задержкой, так как очень большая задержка имеет более высокий приоритет. Все остальные действия, которые уже были созданы, не будут создаваться во второй раз.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
