---
title: "Синхронизация категорий расходов проекта из Project Service Automation"
description: "В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации категорий расходов проекта между Microsoft Dynamics 365 for Finance and Operations и Dynamics 365 for Project Service Automation."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: ru-ru
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Синхронизация категорий расходов проекта между Finance and Operations и Project Service Automation

В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации категорий расходов проекта между Microsoft Dynamics 365 for Finance and Operations и Dynamics 365 for Project Service Automation.

> [!NOTE]
> Dynamics 365 for Finance and Operations версии 8.0. доступна интеграция задач проекта, категорий проводок расходов, оценки часов, оценки затрат и блокировка функциональности.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Поток данных для Project Service Automation и Finance and Operations

Решение по интеграции Project Service Automation и Finance and Operations использует функцию интеграции данных для синхронизации данных между экземплярами Project Service Automation и Finance and Operations. Шаблоны интеграции, доступные при использовании функции интеграции данных, включают поток данных по категориям проводок затрат проекта Project Service Automation и Finance and Operations.

Если категории расходов по проекту освоены в Finance and Operations, поток интеграции сначала происходит из Finance and Operations в Project Service Automation, а затем обновляются идентификаторы интеграции категорий расходов проекта в результате синхронизации из Project Service Automation в Finance and Operations.

Если категории расходов по проекту освоены в Project Service Automation, поток интеграции сначала начинается из Project Service Automation и идет в Finance and Operations. Категории проекта должны быть уже сконфигруированы в Finance and Operations до синхронизации из Project Service Automation. Затем выполните синхронизацию из Finance and Operations обратно в Project Service Automation, а затем из Automation Service Service снова в Finance and Operations. Это гарантирует, что категории будут связаны и не создадутся дубликаты.

> [!NOTE]
> Как правило, категории расходов по проекту будут освоены в Finance and Operations. Если это не ваша ситуация или у вас уже есть категории затрат, созданные в Project Service Automation, вы должны сначала синхронизировать, используя категории проводок затрат по проекту (PSA и Fin и Ops), а затем синхронизировать с использованием категорий транзакций затрат по проекту (Fin и Ops to PSA). Следует затем запустить синхронизацию от PSA к Fin and Ops еще раз.

> Если осуществлять синхронизацию сначала из Project Service Automation, категорий проекта должны уже быть настроены в Finance and Operations и любая категория по проекту, которая должна быть синхронизирована с категориями транзакции Project Service Automation должна быть настроена как **Активно в журналах**.

На следующем рисунке показано, как данные синхронизируются между Project Service Automation и Finance and Operations.

[![Поток данных для интеграции Project Service Automation с Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)


## <a name="templates-and-tasks"></a>Шаблоны и задачи

Для доступа к доступным шаблонам в центре администрирования Microsoft PowerApps выберите **Проекты**и выберите в правом верхнем углу **Новый проект** для выбора общих шаблонов.

Следующий шаблон и базовая задача используются для синхронизации категорий расходов из Finance and Operations в Project Service Automation:

-  **Имя шаблона в интеграции данных:** Категория транзакции расходов по проекту (Fin and Ops и PSA)
-  **Название задачи в проекте:** Синхронизация категорий в PSA

## <a name="entity-set"></a>Набор объектов

| Finance and Operations               | Project Service Automation    |
|--------------------------------------|-------------------------------|
| Объект интеграции для категорий    | Категории проводок        |

## <a name="entity-flow"></a>Поток объектов

Категории расходов проекта управляются в Finance and Operations синхронизируются с Project Service Automation как категории проводок.

## <a name="power-query"></a>Power Query

Необходимо использовать Microsoft Power Query, чтобы настроить тип выставления счетов для категории транзакции при синхронизации для Project Service Automation. В шаблоне проводок расходов проекта (Fin and Ops и PSA) есть столбец по умолчанию и уже имеется соответствие. При создании собственного шаблона, необходимо добавить столбец с условиями в Power Query.
- Откройте форму «Расширенный запрос и фильтрация» в рамках задания по соответствию задачи по категориям расходов проекта.
- Выберите **Добавить столбец с условиями**.
- Назвать новый столбец, например «BillingType».
- Ввести следующее условие: если **CATEGORYID не равен null, затем 19235001, в противном случае — значение null**.
- Щелкните **OK** в столбце.
- Убедитесь, что вы провели соответствие этого нового столбца на странице соответствия.

На следующем рисунке показан пример соответствия задания шаблона при интеграции данных. Соответствие показывает, какие данные полей будут синхронизированы из Finance and Operations в Project Service Automation.

[![Соответствие шаблона](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

Следующий шаблон и базовая задача используются для синхронизации категорий расходов из Project Service Automation в Finance and Operations:

-**Имя шаблона в интеграции данных:** Категории транзакции расходов по проекту (PSA и Fin and Ops) —**Название задачи в проекте:** синхронизировать с Fin Ops

## <a name="entity-set"></a>Набор объектов

| Project Service Automation      | Finance and Operations             |
|---------------------------------|------------------------------------|
| Категории проводок          | Объект интеграции для категорий  | 

## <a name="entity-flow"></a>Поток объектов

Категории расходов проекта управляются в Finance and Operations синхронизируются с Project Service Automation как категории проводок. Обратная синхронизация в Finance and Operations обновляет интеграцию кода из Project Service Automation в категории проекта Finance and Operations.

На следующем рисунке показан пример соответствия задания шаблона при интеграции данных.

> [!NOTE]
> Соответствие показывает, какие данные полей будут синхронизированы из Project Service Automation в Finance and Operations.

[![Соответствие шаблона](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)

