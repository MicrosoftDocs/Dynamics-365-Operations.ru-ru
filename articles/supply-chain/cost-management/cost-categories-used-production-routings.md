---
title: Категории затрат, используемые в производственной маршрутизации
description: Эта статья содержит информацию о категориях затрат, применяемых для производств, в которых используется маршрутизация.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjCategory, RouteCostCategoryPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 78153
ms.assetid: a3fdc76c-0a27-4723-b1c7-4322f707d89e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f36154467f7d392f9bb77bf907807d8acc4f61ff
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679537"
---
# <a name="cost-categories-used-in-production-routing"></a>Категории затрат, используемые в производственной маршрутизации

[!include [banner](../includes/banner.md)]

Эта статья содержит информацию о категориях затрат, применяемых для производств, в которых используется маршрутизация.

Категории затрат используются для производств, которые используют маршрутизацию. Они назначаются операционным ресурсам и операциям маршрутизации в целях определения часовых затрат и сегментирования доли затрат в подсчитанной стоимости произведенной номенклатуры. Группы затрат, назначенные категориям затрат, классифицируют взносы в стоимость на основе операционных ресурсов и типов деятельности, таким как время настройки и время запуска. Степень детализации назначений групп затрат позволяет рассчитывать накладные расходы производства, основываясь на данных маршрутизации. 

**Примечание.** В производстве также употребляются несколько синонимов категорий затрат, такие как код коэффициента использования рабочего времени или код коэффициента использования механизмов. 

Каждая категория затрат связана с определенной записью затрат и присвоенной группой затрат. Для различных производственных целей требуются различные категории затрат.

-   Назначение различных почасовых затрат в зависимости от операционного ресурса. Например, затраты могут отличаться для различных типов рабочих навыков, механизмов или ячеек производства.
-   Назначение различных почасовых затрат для настройки времени или для запуска времени, которое связано с операцией маршрутизации.
-   Распределение затрат операционного ресурса на основании выпущенного количества предпочтительнее, чем по почасовым затратам, таким как поштучная оплата за работу.
-   Обеспечение сегментации групп затрат вкладов в себестоимость на рассчитанные затраты произведенной номенклатуры. Например, возможна сегментация на затраты на оплату труда и затраты на оборудование.
-   База для формул подсчета накладных расходов группы затрат, такие как формулы для накладных расходов, связанных с рабочей силой и механизмами или накладные расходы, связанные со временем настройки и запуска.

Категория затрат может быть присвоена периоду настройки, периоду производства и количеству для операции маршрутизации. Если, например, сегментация затрат или группы затрат различна для периода настройки и производства, тогда должны быть определены и присвоены разные категории затрат для периода настройки и периода производства. Выборочное использование категорий затрат для периодов настройки, периодов производства и количества определяется по группе маршрутизации, которая присвоена операции. Присваивание категорий затрат для времени и количества может быть разрешено политиками компании, которые определены на странице **Параметры управления производством**. 

Каждая категория затрат имеет соответствующие затраты, определенными на основе записей о затратах в рамках данной версии калькуляции стоимости. Используйте страницу **Цена для категории затрат** для определения записей затрат для определенной версии цены и площадки. Когда запись о затратах для категории затрат вводится в первый раз, она имеет статус **Ожидание** и предполагаемую дату вступления в силу. При активации записи стоимости номенклатуры происходит обновление статуса на **Активно в настоящий момент** и даты начала действия на дату активации. Различные записи цены могут указывать на различные площадки, даты вступления в силу и статусы. В расчеты спецификаций для будущего или для прошлого периодов используются записи о затратах с соответствующей датой вступления в силу. Текущая активная запись о затратах будет использована для оценки затрат на производственный заказ и для оценки времени в отчете по отношению ко времени, указанному в производственном заказе. 

Запись о затратах для категории затрат может быть относиться только к одной площадке или всей компании. Чтобы запись о затратах стала специфичной для определенного местоположения, свяжете ее с местоположением. В противном случае нулевое значение указывает, что запись о затратах применяется ко всем местоположениям в компании. Так как, например, затраты для разных местоположений могут быть различными, записи затрат должны определяться как специфичные для местоположений. 

Обычно операции маршрутизации присваиваются те же категории затрат, которые назначены операционному ресурсу или образцовой операции. При создании производственного заказа маршрутные операции в рамках маршрута производства отображают выбранную версию маршрута. Можно отказаться от категорий затрат, назначенных операциям в рамках маршрута производства. 

Некоторые типы производственных работ могут применяться к оценкам времени и отчетам проекта. В этом случае категория затрат необходима для целей производства и для целей проекта. Связанную с проектом дополнительную информацию необходимо определить, когда категория затрат помечается как категория для использования в проектах.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]