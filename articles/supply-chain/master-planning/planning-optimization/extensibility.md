---
title: Расширяемость оптимизации планирования
description: В этой теме описываются сценарии расширения, которые поддерживаются в оптимизации планирования.
author: ChristianRytt
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: e18801a02ae9e904eb5bc597f9f61ed42c537ab9
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/19/2021
ms.locfileid: "7652070"
---
# <a name="planning-optimization-extensibility"></a>Расширяемость оптимизации планирования

[!include [banner](../../includes/banner.md)]

В этой теме описываются сценарии расширяемости, которые относятся к сводному планированию и поддерживаются в оптимизации планирования. Такие возможности доступны с версии Microsoft Dynamics 365 Supply Chain Management 10.0.13.

## <a name="custom-processing-when-master-planning-is-completed"></a>Настраиваемая обработка при завершении сводного планирования

В наиболее распространенных сценариях расширяемости при оптимизации планирования пользовательская обработка выполняется после обновления плана. Например, можно добавить столбец в таблицу спланированные заказы (`ReqPO`) или же можно создать некоторую статистическую информацию из созданного плана. Основная точка расширения, в которой разрешается использовать эти сценарии, это метод `jobCompletedSuccessfully` в классе `MpsMasterPlanningEvents`.

```X++
public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
```

Ниже приводится пример расширения, задающего настраиваемое поле `CstmOrderPriority` в спланированном заказе.

```X++
[ExtensionOf(classStr(MpsMasterPlanningEvents))]
public static final class MpsMasterPlanningEvents_Cstm_Extension
{
    public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
    {
        ttsbegin;

        var affectedPlannedOrdersQuery = _args.parmPostProcessingQueryBuilder().buildAffectedPlannedOrdersQuery();
        var affectedPlannedOrdersQueryRun = new QueryRun(affectedPlannedOrdersQuery);

        while (affectedPlannedOrdersQueryRun.next())
        {
            ReqPO reqPO = affectedPlannedOrdersQueryRun.get(tableNum(ReqPO));
            reqPO.selectForUpdate(true);
            reqPO.CstmOrderPriority = reqPO.ReqDate - systemDateGet() < 7 ? CstmPlannedOrderPriority::Urgent : CstmPlannedOrderPriority::Regular;
            reqPO.doUpdate();
        }

        ttscommit;

        next jobCompletedSuccessfully(_args);
    }

}
```

При добавлении пользовательской логики учитывайте следующие ограничения и рекомендации:

- Метод `jobCompletedSuccessfully` вызывается вне области проводки. Таким образом, план уже видим для пользователя, когда начинает выполняться пользовательская логика. Если настройка дополнительных полей выполняется в спланированных заказах, важно предоставить пользователям сведения о том, что значения этих полей будут считаться согласованными (другими словами, они могут быть устаревшими сразу после завершения планирования).
- Другое задание сводного планирования может быть запущено при вызове метода `jobCompletedSuccessfully`. Новое задание может повлиять на весь план или на его часть. Новое задание может обновить или удалить те же спланированные заказы или проводки требований, которые были созданы или обновлены как часть задания планирования, которое было обработано в `jobCompletedSuccessfully`. Исключения конфликтов обновления должны обрабатываться, когда это событие расширяется.
- Не следует использовать одну область проводок при расширении этого метода. Отдельное выполнение сводного планирования может создавать миллионы проводок потребностей и сотни тысяч спланированных заказов. Если все эти проводки и спланированные заказы обрабатываются в области одной проводки, то будут выполнены многие блокировки SQL и блокируются другие процессы планирования. Кроме того, если проводка выполняется длительное время, в базе данных SQL будут созданы фантомные записи. Фантомные записи отрицательно повлияют на все процессы в системе.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]