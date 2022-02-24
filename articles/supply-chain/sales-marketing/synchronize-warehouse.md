---
title: Синхронизация складов из Supply Chain Management в Field Service
description: В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации складов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 28445592d7a2a8964b1642ae52cff08be6feabbe
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529514"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a>Синхронизация складов из Supply Chain Management в Field Service

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

В этом разделе описываются шаблоны и базовые задачи, которые используются для синхронизации складов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.

[![Синхронизация бизнес-процессов между Supply Chain Management и Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Шаблоны и задачи
Следующий шаблон и базовые задачи используются для выполнения синхронизации складов из Supply Chain Management в Field Service.

**Шаблон в интеграции данных**
- Склады (из Supply Chain Management в Field Service)

**Задача в проекте интеграции данных**
- Склад

## <a name="entity-set"></a>Набор объектов
| Field Service    | Управление цепочкой поставок                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Склады                             |

## <a name="entity-flow"></a>Поток объектов
Склады, которые создаются и поддерживаются в Supply Chain Management, можно синхронизировать с Field Service через проект интеграции данных службы Common Data Service (CDS). Склады, которые требуется синхронизировать с Field Service, можно контролировать с помощью расширенных запросов и фильтрации по проекту. Склады, которые синхронизируются из Supply Chain Management, создаются в Field Service с полем **Поддерживается извне** со значением **Да**, и запись становится записью только для чтения.

## <a name="field-service-crm-solution"></a>Решение Field Service CRM
Для поддержки интеграции между Field Service и Supply Chain Management требуется дополнительная функциональная возможность решения Field Service CRM. В решении поле **Поддерживается извне** было добавлено в объект **Склад (msdyn_warehouses)**. Это поле помогает определить, обрабатывается ли склад из Supply Chain Management, или он существует только в Field Service. Для этого поля предусмотрены следующие параметры:
- **Да** — склад поступил из Supply Chain Management и не может быть изменен в Sales.
- **Нет** — склад был введен непосредственно в Field Service и поддерживается здесь.

Поле **Поддерживается извне** помогает контролировать синхронизацию уровней запасов, корректировки, передачи и использования в заказах на выполнение работ. Только склады, для которых параметр **Поддерживается извне** имеет значение **Да**, может использоваться для синхронизации непосредственно с тем же складом в другой системе. 

> [!NOTE]
> Можно создать несколько складов в Field Service (с настройкой **Поддерживается извне** = "Нет") и затем сопоставить их с одним складом с функцией расширенного запроса и фильтрации. Это используется в ситуациях, когда требуется, чтобы приложение Field Service управляло подробным уровнем запасов и отправляло только обновления в приложение Supply Chain Management. В этом случае Field Service не будет получать обновления уровней запасов из Supply Chain Management. Дополнительные сведения см. в разделах [Синхронизация корректировок запасов из Field Service в Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) и [Синхронизация заказов на выполнение работ в Field Service с заказами на продажу, связанными с проектом в Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Необходимые условия и настройка сопоставления
### <a name="data-integration-project"></a>Проект интеграции данных
Перед синхронизацией складов обязательно обновите расширенный запрос и фильтрацию в проекте, чтобы она включала только склады, которые необходимо внести из Supply Chain Management в Field Service. Обратите внимание, что понадобится склад в Field Service, чтобы применять его в заказах на выполнение работ, корректировках и перемещениях.  

Чтобы убедиться, что значение **Ключ интеграции** существует для **msdyn_warehouses**:
1. Перейдите в раздел "Интеграция данных".
2. Перейдите на вкладку **Набор подключений**.
3. Выберите набор подключений, используемый для синхронизации заказа на выполнение работ.
4. Перейдите на вкладку **Ключ интеграции**.
5. Найдите msdyn_warehouses и проверьте, что добавлен ключ **msdyn_name (имя)**. Если ключ не отображается, добавьте его, щелкнув команду **Добавить ключ**, затем нажмите кнопку **Сохранить** вверху страницы.

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

На следующем рисунке показано сопоставление шаблона в интеграции данных.

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a>Склады (из Supply Chain Management в Field Service): Склад

[![Сопоставление шаблона в интеграции данных](./media/Warehouse1.png)](./media/Warehouse1.png)
