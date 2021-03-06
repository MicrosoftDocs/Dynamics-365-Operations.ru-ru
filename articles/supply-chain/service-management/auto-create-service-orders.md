---
title: Автоматическое создание заказов на обслуживание
description: Можно создать заказы на сервисное обслуживание, на основе соглашения о сервисном обслуживании на период действия соглашения на сервисное обслуживание.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b864aee332c82bc6b6845e7f9e425cfef377033
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824638"
---
# <a name="automatically-create-service-orders"></a>Автоматическое создание заказов на обслуживание 

[!include [banner](../includes/banner.md)]


Можно создать заказы на сервисное обслуживание, на основе соглашения о сервисном обслуживании на период действия соглашения на сервисное обслуживание.

Заказы на сервисное обслуживание, генерируемые на основании соглашений на сервисное обслуживание, присоединяются к соглашению на сервисное обслуживание.

Заказы на обслуживание генерируются автоматически по следующим настройкам:

  - Интервал соглашения на сервисное обслуживание, настроенный в строках соглашения на сервисное обслуживание. Интервал соглашения на сервисное обслуживание определяет частоту, с которой создаются строки заказа на сервисное обслуживание. Дополнительные сведения см. в разделе [Диапазоны сервисного обслуживания](service-intervals.md).

  - Период обслуживания, указываемый в полях **Дата начала** и **Дата окончания** и в форме **Создать заказы на сервисное обслуживание**. Дополнительные сведения см. в разделе [Автоматическое создание заказов на обслуживание](create-service-orders-automatically.md).

  - Параметр **Объединение заказов на сервисное обслуживание** в заголовке соглашения о сервисном обслуживании. Этот параметр определяет, созданы ли строки заказа на сервисное обслуживание из соглашения на сервисное обслуживание, объединяет заказы на сервисное обслуживание по сотруднику, задаче сервисного обслуживания, объекту сервисного обслуживания или соглашению на сервисное обслуживание. Дополнительные сведения см. в разделе [Объединение заказов на сервисное обслуживание](combine-service-orders.md).

  - Параметр **Окно времени** в строке соглашения о сервисном обслуживании. Окна времени определяют, как далеко можно передвинуть строку заказа на сервисное обслуживание относительно ее рассчитанной даты. Дополнительные сведения см. в разделе [Окна времени](time-windows.md).


> [!NOTE]
> <P>Если день, указанный для заказа на сервисное обслуживание, не открыт в календаре, выбранном в форме <STRONG>Параметры управления сервисным обслуживанием</STRONG>, вы получите сообщение о конфликте календарей. Это сообщение можно игнорировать, и заказ на сервисное обслуживание будет создан даже в том случае, если указанный день в календаре закрыт.</P>

## <a name="example-1"></a>Пример 1

Соглашение о сервисном обслуживании действует с 1 января 2012 г. до 31 декабря 2012 г. Если период сервисное обслуживания, указанный в форме **Создать заказы на сервисное обслуживание** начинается с 1 ноября 2012 г. и заканчивается 1 февраля 2013 г., заказы на сервисное обслуживание создаются начиная с 1 ноября 2012 г. до 31 декабря 2012 г.

## <a name="example-2"></a>Пример 2

Соглашение о сервисном обслуживании действует с 1 января 2012 г. до 31 декабря 2012 г. К соглашению прикреплено две строки соглашения о сервисном обслуживании. Первая строка соглашения о сервисном обслуживании имеет дату начала 2 января 2012 г. и дату окончания 1 марта 2012 г. Вторая строка соглашения о сервисном обслуживании имеет дату начала 1 апреля 2012 г. и дату окончания 31 декабря 2012 г. Можно указать период в форме **Создать заказы на сервисное обслуживание** начиная с 1 октября 2012 г. до 31 декабря 2012 г. Таким образом, заказы на обслуживание создаются только по второй строке соглашения, так как даты начала и окончания первой строки лежат ранее периода, указанного для заказа на сервисное обслуживание.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]