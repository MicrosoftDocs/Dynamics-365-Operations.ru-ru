---
title: Операции для несоответствий
description: В этой теме описывается, как создавать и использовать операции для несоответствий.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9a6cc88b80f82d77edac0341cb6a3c0db4b42ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022212"
---
# <a name="operations-for-nonconformances"></a><span data-ttu-id="cb1d1-103">Операции для несоответствий</span><span class="sxs-lookup"><span data-stu-id="cb1d1-103">Operations for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb1d1-104">В этой теме описывается, как создавать и использовать операции для несоответствий.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-104">This topic describes how to create and use operations for nonconformances.</span></span>

<span data-ttu-id="cb1d1-105">Можно использовать страницу **Операции**, чтобы классификации работы, которая может быть выполнена для утвержденного несоответствия.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-105">You can use the **Operations** page to define classifications of the work that can be performed for an approved nonconformance.</span></span> <span data-ttu-id="cb1d1-106">При назначении связанной операции для несоответствия можно возможность предоставить сведения о связанном материале, часах трудозатрат и накладных расходах, требуемых для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-106">When you assign a related operation to a nonconformance, you can provide details such as the associated material, labor hours, and charges that are required to do the operation.</span></span> <span data-ttu-id="cb1d1-107">Эта информация используется системой для расчета оценочной стоимости операции.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-107">The system uses this information to calculate an estimated cost for the operation.</span></span> <span data-ttu-id="cb1d1-108">Подробные сведения и оценка затрат используются только для справочных целей.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-108">The detailed information and estimated costs are for reference.</span></span> <span data-ttu-id="cb1d1-109">Связанные операции для качества отличаются от операций, которые могут быть определены для маршрута производства.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-109">The related operations for quality differ from the operations that can be defined for a production route.</span></span>

> [!NOTE]
> <span data-ttu-id="cb1d1-110">Хотя можно отслеживать затраты, время и номенклатуры, используемые в операции, которая связана с несоответствием, введенные данные являются только информационными.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-110">Although you can track costs, time, and the items that are used in an operation that is related to a nonconformance, the data that you enter is only informational.</span></span> <span data-ttu-id="cb1d1-111">Они не интегрируется автоматически с главной книгой, складской субкнигой и **Посещаемость и время присутствия**.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-111">It isn't automatically integrated with the general ledger, inventory subledger, or the **Time and attendance** module.</span></span>

## <a name="examples-of-operations"></a><span data-ttu-id="cb1d1-112">Примеры операций</span><span class="sxs-lookup"><span data-stu-id="cb1d1-112">Examples of operations</span></span>

<span data-ttu-id="cb1d1-113">Вы работаете в производственной компании.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-113">You work for a manufacturing company.</span></span> <span data-ttu-id="cb1d1-114">Несоответствие было создано и утверждено для номенклатур, которые не прошедших проверку качества.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-114">A nonconformance was created and approved for items that failed a quality test.</span></span> <span data-ttu-id="cb1d1-115">Исправление было создано, чтобы указать на то, что проблема была связана с неисправным подшипником в машине.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-115">A correction was created to indicate that the problem was related to a bad bearing on a machine.</span></span> <span data-ttu-id="cb1d1-116">Для замены этого подшипника требуется несколько шагов, и ответственности отслеживается для каждой операции.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-116">Several steps are required to replace the bearing, and the responsibility for each operation is tracked.</span></span> <span data-ttu-id="cb1d1-117">Например, может потребоваться выполнить следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="cb1d1-117">For example, the following steps might be required:</span></span>

1. <span data-ttu-id="cb1d1-118">Производственная линия останавливается, и выполняется процедура ее очистки.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-118">The production line is stopped, and the clean-out routine is performed.</span></span>
1. <span data-ttu-id="cb1d1-119">Обслуживающий персонал заменяет подшипник.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-119">Maintenance personnel replace the bearing.</span></span>
1. <span data-ttu-id="cb1d1-120">Сотрудники контроля качества проверяют машину перед ее вводом в эксплуатацию.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-120">Quality assurance personnel inspect the machine before it's turned back on.</span></span>

<span data-ttu-id="cb1d1-121">Для данного примера могут быть созданы следующие операции для представления работы, которая должна быть выполнена:</span><span class="sxs-lookup"><span data-stu-id="cb1d1-121">For this example, the following operations can be created to represent the work that must be done:</span></span>

- <span data-ttu-id="cb1d1-122">Остановка производственной линии.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-122">Stop the production line.</span></span>
- <span data-ttu-id="cb1d1-123">Очистка производственной линии.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-123">Clean out the production line.</span></span>
- <span data-ttu-id="cb1d1-124">Выполнение технического обслуживания машины.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-124">Perform machine maintenance.</span></span>
- <span data-ttu-id="cb1d1-125">Проверка машины.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-125">Inspect the machine.</span></span>

## <a name="create-an-operation"></a><span data-ttu-id="cb1d1-126">Создание операции</span><span class="sxs-lookup"><span data-stu-id="cb1d1-126">Create an operation</span></span>

1. <span data-ttu-id="cb1d1-127">Перейдите в раздел **Управление запасами \> Настройка \> Управление качеством \> Операции**.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-127">Go to **Inventory management \> Setup \> Quality management \> Operations**.</span></span>
1. <span data-ttu-id="cb1d1-128">На панели операций выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-128">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="cb1d1-129">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="cb1d1-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="cb1d1-130">**Операция** — введите уникальный код или имя операции.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-130">**Operation** – Enter a unique ID or name for the operation.</span></span>
    - <span data-ttu-id="cb1d1-131">**Описание** — введите подробное описание операции.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-131">**Description** – Enter a detailed description of the operation.</span></span>
    - <span data-ttu-id="cb1d1-132">**Тип** — если операция может использоваться только с несоответствиями, относящимися к конкретному типу заказа, выберите тип заказа (*заказ на покупку* или *заказ на продажу*).</span><span class="sxs-lookup"><span data-stu-id="cb1d1-132">**Type** – If the operation can be used only with nonconformances that are related to a specific type of order, select the order type (*Purchase order* or *Sales order*).</span></span>

1. <span data-ttu-id="cb1d1-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="cb1d1-133">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb1d1-134">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cb1d1-134">Additional resources</span></span>

- [<span data-ttu-id="cb1d1-135">Обзор управления качеством</span><span class="sxs-lookup"><span data-stu-id="cb1d1-135">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="cb1d1-136">Включение управления качеством и несоответствием</span><span class="sxs-lookup"><span data-stu-id="cb1d1-136">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="cb1d1-137">Создание и обработка несоответствий</span><span class="sxs-lookup"><span data-stu-id="cb1d1-137">Create and process nonconformances</span></span>](tasks/create-process-non-conformance.md)
- [<span data-ttu-id="cb1d1-138">Работники, ответственные за утверждение несоответствий</span><span class="sxs-lookup"><span data-stu-id="cb1d1-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="cb1d1-139">Карантинные зоны для несоответствий</span><span class="sxs-lookup"><span data-stu-id="cb1d1-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="cb1d1-140">Типы диагностики для несоответствий</span><span class="sxs-lookup"><span data-stu-id="cb1d1-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="cb1d1-141">Расходы по контролю качества для несоответствий</span><span class="sxs-lookup"><span data-stu-id="cb1d1-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="cb1d1-142">Типы проблем для несоответствий</span><span class="sxs-lookup"><span data-stu-id="cb1d1-142">Problem types for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="cb1d1-143">Управление качеством для складских процессов</span><span class="sxs-lookup"><span data-stu-id="cb1d1-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
