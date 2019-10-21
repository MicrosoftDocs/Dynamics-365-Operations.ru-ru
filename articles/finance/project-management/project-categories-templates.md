---
title: Синхронизация категорий расходов проекта между Finance and Operations и Project Service Automation
description: В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации категорий расходов проекта между Microsoft Dynamics 365 Finance и Dynamics 365 Project Service Automation.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 482febc91a04766216f9887ab59d30cc9aed5096
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250515"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Синхронизация категорий расходов проекта между Finance and Operations и Project Service Automation

[!include[banner](../includes/banner.md)]

В этой теме обсуждаются шаблоны и базовые задачи, которые используются для синхронизации категорий расходов проекта между Dynamics 365 Finance и Dynamics 365 Project Service Automation.

> [!NOTE]
> - В версии 8.0 доступна интеграция задач проекта, категорий проводок расходов, оценки часов, оценки затрат и блокировка функциональности.
> - Интеграция фактических данных доступна в версии 8.0.1 или новее.
> - При использовании Enterprise edition 7.3.0 после установки обновлений КБ 4132657 и 4132660 КБ, можно использовать шаблоны для интеграции задачи проекта, категорий транзакций расходов, оценок часов, оценок расходов и фактических данных и для настройки функции блокировки. Если необходимо сбросить распределения по бухгалтерским счетам, рекомендуется также установить КБ 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Поток данных для Project Service Automation для Finance

Решение по интеграции Project Service Automation и Finance использует функцию интеграции данных для синхронизации данных между экземплярами Project Service Automation и Finance. Шаблоны интеграции, доступные при использовании функции интеграции данных, включают поток данных по категориям проводок затрат проекта между Finance и Project Service Automation.

Если категории расходов по проекту освоены в Finance, поток интеграции сначала начинается из Finance идет в Project Service Automation. Идентификаторы интеграции категорий затрат по проекту затем обновляются путем синхронизации из Project Service Automation в Finance.

Если категории расходов по проекту освоены в Project Service Automation, поток интеграции сначала начинается из Project Service Automation и идет в Finance. Категории проекта должны быть уже сконфигурированы в Finance до синхронизации из Project Service Automation. Затем выполните синхронизацию из Finance обратно в Project Service Automation, а затем из Automation Service Service снова в Finance. Таким образом вы помогаете гарантировать, что категории связаны, и что повторения не создаются.

> [!NOTE]
> Как правило, категории расходов по проекту осваиваются в Finance. Тем не менее, если не они не освоены или если категории расходов уже были созданы в Project Service Automation, необходимо сначала синхронизировать с помощью шаблона категорий проводок расходов по проекту (PSA в Fin and Ops). Затем синхронизируйте с помощью шаблона категорий транзакций расходов по проекту (Fin and Ops и PSA) Затем следует выполнить синхронизацию из Project Service Automation в Finance еще раз.
>
> Если синхронизировать сначала из Project Service Automation, следующие требования должны быть выполнены в Finance перед выполнением синхронизации:
>
> - Должны существовать общие категории, совпадающие с категорией проекта, настроенной в Project Service Automation, и она должна быть включена как для **Проект**, так и для **Расходы**.
> - Для каждого юридического лица Finance, с которым необходима интеграция, должны существовать следующие категории проекта:
>
>     - **Категория проекта** существует. 
>     - **Использовать в расходах** включен.
>     - **Активно в журнале** включен.
>     - **Тип проводки** имеет значение **Расходы**.

На следующем рисунке показано, как данные синхронизируются между Project Service Automation и Finance.

[![Поток данных для интеграции Project Service Automation с Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Синхронизация категорий расходов проекта из Finance в Project Service Automation

### <a name="template-and-task"></a>Шаблон и задача

Для доступа к шаблону в центре администрирования Microsoft PowerApps выберите **Проекты** и выберите в правом верхнем углу **Новый проект** для выбора общих шаблонов.

Следующий шаблон и базовая задача используются для синхронизации категорий расходов из Finance в Project Service Automation:

- **Имя шаблона в интеграции данных:** Категория транзакции расходов по проекту (Fin and Ops и PSA)
- **Название задачи в проекте:** Синхронизация категорий в PSA

### <a name="entity-set"></a>Набор объектов

| Финансы                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Объект интеграции для категорий | Категории проводок     |

### <a name="entity-flow"></a>Поток объектов

Категории расходов проекта управляются в Finance синхронизируются с Project Service Automation как категории проводок.

### <a name="power-query"></a>Power Query

При синхронизации в Project Service Automation необходимо использовать Microsoft Power Query для Excel, чтобы настроить тип выставления счетов для категории транзакции. В шаблоне проводок расходов проекта (Fin and Ops в PSA) предусмотрены столбец по умолчанию и сопоставление. При создании собственного шаблона, необходимо добавить столбец с условиями в Power Query. Выполните следующие действия.

1. Щелкните стрелку, чтобы открыть сопоставление задачи категорий расходов по проекту в шаблон категорий проводок расходов по проекту (Fin and Ops в PSA).
2. Щелкните ссылку **Расширенный запрос и фильтрация**, чтобы открыть Power Query.
2. Выберите **Добавить столбец с условиями**.
3. Введите имя для нового столбца, например **BillingType**.
4. Ввести следующее условие: **если CATEGORYID не равно null, то 19235001, иначе null**.
5. Щелкните **OK** в столбце.
6. Убедитесь, что вы провели соответствие этого нового столбца на странице соответствия.

На следующем рисунке показан пример соответствия задания шаблона при интеграции данных. Соответствие показывает, какие данные полей будут синхронизированы из Finance в Project Service Automation.

[![Соответствие шаблона](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Синхронизация категорий расходов проекта из Project Service Automation в Finance

### <a name="template-and-task"></a>Шаблон и задача

Следующий шаблон и базовая задача используются для синхронизации категорий расходов из Project Service Automation в Finance:

- **Имя шаблона в интеграции данных:** Категория транзакции расходов по проекту (PSA в Fin and Ops)
- **Название задачи в проекте:** Синхронизация категорий в Fin Ops

### <a name="entity-set"></a>Набор объектов

| Project Service Automation | Финансы                           |
|----------------------------|-----------------------------------|
| Категории проводок     | Объект интеграции для категорий |

### <a name="entity-flow"></a>Поток объектов

Категории расходов проекта управляются в Finance синхронизируются с Project Service Automation как категории проводок. Обратная синхронизация в Finance обновляет категорию проекта в Finance с использованием кода интеграции из Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

На следующем рисунке показан пример соответствия задания шаблона при интеграции данных.

> [!NOTE]
> Соответствие показывает, какие данные полей будут синхронизированы из Project Service Automation в Finance.

[![Соответствие шаблона](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
