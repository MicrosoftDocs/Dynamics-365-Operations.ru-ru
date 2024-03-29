---
title: Анализ затрат по производственному заказу
description: В этой статье приводятся сведения об анализе затрат, который можно выполнить для завершенных и текущих производственных заказов. Вы можете анализировать оценочные и фактические затраты, используя страницу "Расчет цены" или отчет "Оценка затрат и калькуляция себестоимости". Можно просматривать сведения об оценочных и фактических затратах (и количестве) для каждых компонентной номенклатуры, операции маршрутизации и элемента косвенных затрат.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage, ProdSetupHistoricalCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79634
ms.assetid: ded5da04-f787-49f7-b5e5-75c2a2b92930
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd303efb5aee53eec36fac7ec6329d28aacf96a1
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672300"
---
# <a name="production-order-cost-analysis"></a>Анализ затрат по производственному заказу

[!include [banner](../includes/banner.md)]

В этой статье приводятся сведения об анализе затрат, который можно выполнить для завершенных и текущих производственных заказов. Вы можете анализировать оценочные и фактические затраты, используя страницу "Расчет цены" или отчет "Оценка затрат и калькуляция себестоимости". Можно просматривать сведения об оценочных и фактических затратах (и количестве) для каждых компонентной номенклатуры, операции маршрутизации и элемента косвенных затрат.

Фактические затраты по производственному заказу учитывают зарегистрированное потребление материалов и операции маршрутизации. Доступ к подробным проводкам по зарегистрированному потреблению материалов, операциям маршрутизации и косвенным затратам для производственного заказа можно получить на странице **Разноски по производству**.

## <a name="variance-analysis-for-a-completed-production-order"></a>Анализ расхождений в выполненном производственном заказе
Расхождения отражают сравнение отчетных производственных действий и расчета стандартной себестоимости для производственной номенклатуры. Расхождения не отражают различия с оценочной стоимостью производственного заказа. Включаемые в отчеты производственные мероприятия включают потребление материала и маршрутные операции, а также связанные косвенные затраты и количество, заявленное как принятое. Рассчитываются четыре типа расхождений:

-   Расхождение размера лота
-   Расхождение производственного количества
-   Расхождение по производственной цене
-   Расхождение производственного замещения

На следующем графике показаны расхождения четырех типов, отражающие разницу между фактическими затратами по производственному заказу и расчетными затратами в записи о затратах на номенклатуру после завершения производственного заказа. 

![Расхождения, которые отвечают за различия в выполненном производственном заказе.](./media/control.jpg) 

Производственные отклонения можно проанализировать с помощью страницы **Расхождение** или отчета **Расхождение в производстве**. Используйте параметры отображения, чтобы просматривать подробные сведения об отклонениях по номенклатуре и операционному ресурсу или по группе затрат. Политика детализации затрат в параметрах запасов определяет, будут ли отклонения отслеживаться по группе затрат. Вы также можете использовать параметры отображения **один**, **несколько** или **всего** для просмотра сводных значений отклонений. Подробные сведения об отклонениях могут помочь вам определить источник каждого из отклонений. Чтобы спрогнозировать отклонения до завершения производственного заказа, проанализируйте подробные сведения, приведенные в отчете **Оценка затрат и калькуляция себестоимости**.

## <a name="cost-analysis-for-current-production-orders"></a>Анализ затрат для текущих производственных заказов
Отдельные отчеты предоставляют информацию о каждом типе проводок. Эти отчеты используются для анализа затрат по производственным операциям, включаемым в отчет. Информация отображается только для текущих производственных заказов со статусом **Начатые** или **Принято**.

-   **Сырье в обработке** — в этом отчете перечисляются проводки по отгрузочным накладным, которые были зарегистрированы по текущим производственным заказам на указанную дату проводки. Отчет отражает израсходованное количество компонента и сумму затрат для каждой проводки. Используйте критерии выбора для номенклатуры с одним компонентом. Например, можно распечатать информацию об израсходованном количестве компонента по применимым производственным заказам. Израсходованное количество не обновляется в соответствии с принятыми количествами для родительской номенклатуры. Поэтому фактическое количество сырья в обработке может быть завышено.
-   **Незавершенное производство** — в этом отчете перечисляются маршрутные проводки (или проводки заданий), которые были зарегистрированы по текущим производственным заказам на указанную дату проводки. В отчете отражаются часы, сумма и количество (как количество годных, так и количество дефектных изделий), зафиксированные для каждой проводки. Он также включает такие сведения, как номер операции, код операции и операционный ресурс. Дополнительно в отчете отображается суммарное время и сумма по всем проводкам по производственному заказу, а также количество, учтенное как готовое.
-   **Косвенные затраты в процессе** — в этом отчете перечисляются косвенные затраты, которые были понесены по производственным заказам. Эти данные основываются на зарегистрированном потреблении операций маршрутизации и компонентов на указанную дату проводки. В отчете указывается тип косвенных затрат (накладные расходы или ставка), код листа калькуляции себестоимости для косвенных затрат и сумма затрат для каждой проводки. Этот отчет не содержит сведений о карте маршрута или проводке по отгрузочной накладной, создавшей косвенные затраты.
-   **В процессе калькуляции себестоимости производства** — в отчете перечисляется комбинированное потребление, учитывающее материалы, операции маршрутизации и косвенные затраты по производственным заказам на указанную дату проводки.
-   **Приемка номенклатуры в обработке** — в этом отчете перечисляются текущие производственные заказы и проводки по учету готовой номенклатуры на указанную дату проводки.


## <a name="additional-resources"></a>Дополнительные ресурсы

[Общие источники отклонений цены производства от себестоимости](common-sources-of-production-variances.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]