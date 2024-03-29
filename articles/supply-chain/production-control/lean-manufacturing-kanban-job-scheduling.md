---
title: Планирование заданий канбана для бережливого производства
description: Эта статья представлена информация о визуальном контроле над планированием заданий канбана и различных способов для планирования заданий канбана.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f70c3cf44ce90b13250836013636920267d2016d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570233"
---
# <a name="kanban-job-scheduling-for-lean-manufacturing"></a>Планирование заданий канбана для бережливого производства

[!include [banner](../includes/banner.md)]

Эта статья представлена информация о визуальном контроле над планированием заданий канбана и различных способов для планирования заданий канбана.  

Страница **Планирование заданий канбана** обеспечивает визуальный контроль за графиками производственных ячеек гибкого производства. На ней приведен обзор всех заданий канбана, с множеством способов фильтрации. С этой страницы необходимо переходить на все остальные страницы, связанные с конфигурированием и выполнением канбанов.

## <a name="automatic-scheduling-of-kanban-jobs"></a>Автоматическое планирование заданий канбана
Планирование может инициироваться автоматически, если задать параметр **Автоматическое планирование количества** в правиле канбана. Если параметр **Автоматическое планирование количества** установлен равным **1**, каждое задание канбана планируется сразу же после создания. В результате получается серия операций "первым вытянул — первым получил". Если установить параметр **Автоматическое планирование количества** в значение больше 1, задания канбана перед планированием группируются. 

Эта концепция позволяет уменьшить размеры канбанов, так чтобы они были меньше фактических экономических размеров партии. Например, пусть экономический размер партии для конкретной номенклатуры (или семейства номенклатур) равен 30. Вместо того чтобы создавать канбаны с количеством продукта, равным 30, можно настроить правило канбана так, чтобы количество продукта у него было равно 10, а параметр **Автоматическое планирование количества** имел значение **3**. Хотя при автоматическом планировании задания канбана планируются для производственной ячейки только тогда, когда существует три незапланированных задания, планировщик и супервайзер цеха будут видеть, что два незапланированных задания ожидают выполнения. В этом случае планировщик или начальник цеха могут отправить эти два задания в производство путем их планирования вручную или путем создания дополнительных канбанов.

## <a name="manual-scheduling"></a>Планирование вручную
Для планирования вручную в Microsoft Dynamics AX 2012 предусмотрена доска планирования канбана. Планирование вручную можно сочетать с автоматическим планированием. Доска планирования канбана позволяет планировать и отменять запланированные задания, менять их порядок или переносить из одного периода в другой. Запланированные задания, основанные на правиле канбана, у которого значение параметра **Автоматическое планирование** больше **0**, можно вручную отменить. Однако эти задания будут перепланированы при следующем возникновении события автоматического планирования (т. е. при создании нового канбана). Для планирования вручную предусмотрены следующие команды:

-   **Запланировать**: выбранные задания планируются в соответствии со сроком, когда они должны быть выполнены. (Эта команда похожа на автоматическое планирование.)
-   **Запланировать на будущее с даты**: выбранные задания планируются в соответствии со сроком, когда они должны быть выполнены, однако результат ограничивается по указанной самой ранней дате начала.
-   **Назад**: выбранные запланированные задания перемещаются назад в последовательности в пределах периода.
-   **Вперед**: выбранные запланированные задания перемещаются вперед в последовательности в пределах периода.
-   **Предыдущий период**: выбранные запланированные задания перемещаются в начало или в конец предыдущего периода.
-   **Следующий период**: выбранные запланированные задания перемещаются в начало или в конец следующего периода.
-   **План** &gt; **Вернуть статус задания** позволяет вам отменить запланированное задание.

## <a name="lean-scheduling-groups"></a>Группы планирования бережливого производства
Каждый цвет представляет одну из групп планирования бережливого производства. Группы планирования бережливого производства можно произвольно определять как универсальные группы или как группы, относящиеся к отдельной производственной ячейке. Группам планирования можно произвольно назначать номенклатуры и аналитики. Например, в ячейке "Покраска" группа планирования может представлять цвет продукта. В работе, которая зависит от определенных требований к остастке, номенклатуры могут группироваться по потребности в оснастке, а в производственной ячейке "упаковка" номенклатуры могут группироваться по упаковочному шаблону. Использование цветов для групп планирования бережливого производства не является обязательным, но рекомендуется. Это позволяет быстрее визуально определить состояние плана. Например, очень легко увидеть, в какой день изготавливаются какие цвета, и легко понять, как оптимизировать эту работу.

## <a name="work-cell-capacity-and-period-capacity"></a>Мощность производственной ячейки и мощность периода
Мощность производственной ячейки бережливого производства всегда представляет собой параллельную мощность. Иными словами, в производственной ячейке одновременно могут быть активными несколько заданий. Мощность можно отслеживать в двух режимах: как пропускную способность и как часы.

### <a name="throughput"></a>Пропускная способность

Мощность производственной ячейки определяется средней пропускной способностью того или иного базисного периода (стандартного рабочего дня, недели или месяца). Фактическая мощность в день или в неделю затем вычисляется исходя из рабочего времени по календарю, назначенному производственной ячейке. Мощность, загружаемая заданием, — это количество задания, скорректированное на коэффициент пропускной способности номенклатуры в производственной ячейке.

### <a name="hours"></a>Часы

Доступная мощность по дням или по неделям определяются календарем, назначенным производственной ячейке. Мощность, загружаемая заданием, — это время цикла мероприятия, скорректированное на количество (количество для мероприятия по умолчанию, а не фактическое количество для задания) и на коэффициент пропускной способности номенклатуры в производственной ячейке.

#### <a name="period-capacity-factbox"></a>Информационное поле мощности периода

На странице **Планирование заданий канбана** имеется информационное поле, в котором отображается доступная и зарезервированная мощность периода для выбранной производственной ячейки. В зависимости от выбранных периодов планирования в модели производственного потока периоды отображаются как дни или как недели.

## <a name="additional-resources"></a>Дополнительные ресурсы





[!INCLUDE[footer-include](../../includes/footer-banner.md)]