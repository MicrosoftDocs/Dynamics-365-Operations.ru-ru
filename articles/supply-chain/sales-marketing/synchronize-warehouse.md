---
title: Синхронизация складов из Finance and Operations в Field Service
description: В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации складов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 7e6d7626c00b9d7d98ce872652653c36ce7bc975
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/14/2019
ms.locfileid: "842541"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Синхронизация складов Finance and Operations с Field Service

[!include[banner](../includes/banner.md)]

В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации складов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.

[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Шаблоны и задачи
Следующий шаблон и базовые задачи используются для выполнения синхронизации складов из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.

**Шаблон в интеграции данных**
- Склады (из Fin and Ops в Field Service)

**Задача в проекте интеграции данных**
- Склад

## <a name="entity-set"></a>Набор объектов
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Склады                             |

## <a name="entity-flow"></a>Поток объектов
Склады, которые создаются и поддерживаются в Finance and Operations, можно синхронизировать с Field Service через проект интеграции данных службы Common Data Service (CDS). Склады, которые требуется синхронизировать с Field Service, можно контролировать с помощью расширенных запросов и фильтрации по проекту. Склады, которые синхронизируются из Finance and Operations, создаются в Field Service с полем **Поддерживается извне** со значением **Да**, и запись становится записью только для чтения.

## <a name="field-service-crm-solution"></a>Решение Field Service CRM
Для поддержки интеграции между Field Service и Finance and Operations требуется дополнительная функциональная возможность решения Field Service CRM. В решении поле **Поддерживается извне** было добавлено в объект **Склад (msdyn_warehouses)**. Это поле помогает определить, обрабатывается ли склад из Finance and Operations, или он существует только в Field Service. Для этого поля предусмотрены следующие параметры:
- **Да** — склад происходит из Finance and Operations и не может быть изменен в Sales.
- **Нет** — склад был введен непосредственно в Field Service и поддерживается здесь.

Поле **Поддерживается извне** помогает контролировать синхронизацию уровней запасов, корректировки, передачи и использования в заказах на выполнение работ. Только склады, для которых параметр **Поддерживается извне** имеет значение **Да**, может использоваться для синхронизации непосредственно с тем же складом в другой системе. 

> [!NOTE]
> Можно создать несколько складов в Field Service (с настройкой **Поддерживается извне** = "Нет") и затем сопоставить их с одним складом в Finance and Operations с функцией расширенного запроса и фильтрации. Это используется в ситуациях, когда требуется, чтобы приложение Field Service управляло подробным уровнем запасов и просто отправляло обновления в приложение Finance and Operations. В этом случае Field Service не будет получать обновления уровней запасов из Finance and Operations. Дополнительные сведения см. в разделах [Синхронизация корректировок запасов из Field Service в Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) и [Синхронизация заказов на выполнение работ в Field Service с заказами на продажу, связанными с проектом в Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Необходимые условия и настройка сопоставления
### <a name="data-integration-project"></a>Проект интеграции данных
Перед синхронизацией складов обязательно обновите расширенный запрос и фильтрацию в проекте, чтобы она включала только склады, которые необходимо внести из Finance and Operations в Field Service. Обратите внимание, что понадобится склад в Field Service, чтобы применять его в заказах на выполнение работ, корректировках и перемещениях.  

Чтобы убедиться, что значение **Ключ интеграции** существует для **msdyn_warehouses**:
1. Перейдите в раздел "Интеграция данных".
2. Перейдите на вкладку **Набор подключений**.
3. Выберите набор подключений, используемый для синхронизации заказа на выполнение работ.
4. Перейдите на вкладку **Ключ интеграции**.
5. Найдите msdyn_warehouses и проверьте, что добавлен ключ **msdyn_name (имя)**. Если ключ не отображается, добавьте его, щелкнув команду **Добавить ключ**, затем нажмите кнопку **Сохранить** вверху страницы.

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

На следующем рисунке показано сопоставление шаблона в интеграции данных.

### <a name="warehouses-fin-and-ops-to-field-service-warehouse"></a>Склады (из Fin and Ops в Field Service): Склад

[![Сопоставление шаблона в интеграции данных](./media/Warehouse1.png)](./media/Warehouse1.png)
