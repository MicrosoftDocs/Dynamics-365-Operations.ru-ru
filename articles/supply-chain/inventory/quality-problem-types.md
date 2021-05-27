---
title: Типы проблем для несоответствий
description: В этой теме описывается, как создавать и использовать типы проблем для несоответствий.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 742edec8570610efe41a2c627efd1df586e0733e
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022164"
---
# <a name="problem-types-for-nonconformances"></a><span data-ttu-id="4d570-103">Типы проблем для несоответствий</span><span class="sxs-lookup"><span data-stu-id="4d570-103">Problem types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d570-104">В этой теме описывается, как создавать и использовать типы проблем для несоответствий.</span><span class="sxs-lookup"><span data-stu-id="4d570-104">This topic describes how to create and use problem types for nonconformances.</span></span>

<span data-ttu-id="4d570-105">Используйте страницу **Типы проблем**, чтобы определить классификацию проблем качества, которые могут возникнуть для различных типов несоответствий.</span><span class="sxs-lookup"><span data-stu-id="4d570-105">You use the **Problem types** page to define a classification of the quality problems that might occur for the various nonconformance types.</span></span> <span data-ttu-id="4d570-106">Для каждого создаваемого типа проблемы необходимо указать типы несоответствий, с которыми может использоваться тип проблемы.</span><span class="sxs-lookup"><span data-stu-id="4d570-106">For each problem type that you create, you must specify the types of nonconformances that the problem type can be used with.</span></span> <span data-ttu-id="4d570-107">Можно настроить следующие типы несоответствий:</span><span class="sxs-lookup"><span data-stu-id="4d570-107">You can set up the following nonconformance types:</span></span>

- <span data-ttu-id="4d570-108">**Внутреннее** — несоответствия этого типа относятся к запасам в наличии (например, к заказам контроля качества или карантинным заказам).</span><span class="sxs-lookup"><span data-stu-id="4d570-108">**Internal** – Nonconformances of this type are related to on-hand inventory (for example, quality orders or quarantine orders).</span></span>
- <span data-ttu-id="4d570-109">**Клиент** — несоответствия этого типа относятся к заказам на продажу.</span><span class="sxs-lookup"><span data-stu-id="4d570-109">**Customer** – Nonconformances of this type are related to sales orders.</span></span>
- <span data-ttu-id="4d570-110">**Поставщик** — несоответствия этого типа относятся к заказам на покупку.</span><span class="sxs-lookup"><span data-stu-id="4d570-110">**Vendor** – Nonconformances of this type are related to purchase orders.</span></span>
- <span data-ttu-id="4d570-111">**Запрос на обслуживание** — несоответствия этого типа относятся к заказам на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="4d570-111">**Service request** – Nonconformances of this type are related to service orders.</span></span>
- <span data-ttu-id="4d570-112">**Производство** — несоответствия этого типа связаны с заказами партий или производственными заказами.</span><span class="sxs-lookup"><span data-stu-id="4d570-112">**Production** – Nonconformances of this type are related to batch orders or production orders.</span></span>
- <span data-ttu-id="4d570-113">**Производство сопутствующих продуктов** — несоответствия этого типа связаны с заказами партий для сопутствующих продуктов.</span><span class="sxs-lookup"><span data-stu-id="4d570-113">**Co-product production** – Nonconformances of this type are related to batch orders for co-products.</span></span>

<span data-ttu-id="4d570-114">При создании нового типа проблемы выберите **Типы несоответствия** на панели операций, чтобы создать список одного или нескольких типов несоответствий, которые разрешены для данного типа проблемы.</span><span class="sxs-lookup"><span data-stu-id="4d570-114">When you create a new problem type, select **Non conformance types** on the Action Pane to create a list of one or more nonconformance types that are authorized for the problem type.</span></span> <span data-ttu-id="4d570-115">Например, тип проблемы, относящийся к коду дефекта, может применяться ко всем типам несоответствия.</span><span class="sxs-lookup"><span data-stu-id="4d570-115">For example, a problem type that is related to a defect code might apply to all nonconformance types.</span></span> <span data-ttu-id="4d570-116">Однако тип проблемы, относящийся к жалобам клиентов, может применяться только к типам несоответствия **Клиент** и **Запрос на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="4d570-116">However, a problem type that is related to customer complaints might apply only to the **Customer** and **Service request** nonconformance types.</span></span>

## <a name="examples-of-problem-types"></a><span data-ttu-id="4d570-117">Примеры типов проблем</span><span class="sxs-lookup"><span data-stu-id="4d570-117">Examples of problem types</span></span>

<span data-ttu-id="4d570-118">Ниже приводятся примеры сценариев для типов проблем, которые могут использоваться с другими типами несоответствия:</span><span class="sxs-lookup"><span data-stu-id="4d570-118">Here are some examples of scenarios for problem types that can be used with the different nonconformance types:</span></span>

- <span data-ttu-id="4d570-119">**Клиент:** клиент подал жалобу, клиент сделал возврат или не соблюдается спецификация качества.</span><span class="sxs-lookup"><span data-stu-id="4d570-119">**Customer:** A customer filed a complaint, a customer made a return, or quality specifications weren't met.</span></span>
- <span data-ttu-id="4d570-120">**Поставщик:** продукт поврежден, спецификации качества не соблюдены или получен неправильный продукт.</span><span class="sxs-lookup"><span data-stu-id="4d570-120">**Vendor:** The product was damaged, quality specifications weren't met, or the wrong product was received.</span></span>
- <span data-ttu-id="4d570-121">**Запрос на обслуживание:** спецификации качества не соблюдена, клиент направил жалобу или необходимо обслуживание оборудования.</span><span class="sxs-lookup"><span data-stu-id="4d570-121">**Service request:** Quality specifications weren't met, a customer filed a complaint, or machine maintenance is required.</span></span>
- <span data-ttu-id="4d570-122">**Производство:** спецификации качества не соблюдены, необходимо обслуживание оборудования или продукт поврежден.</span><span class="sxs-lookup"><span data-stu-id="4d570-122">**Production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>
- <span data-ttu-id="4d570-123">**Производство сопутствующих продуктов:** спецификации качества не соблюдены, необходимо обслуживание оборудования или продукт поврежден.</span><span class="sxs-lookup"><span data-stu-id="4d570-123">**Co-product production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a><span data-ttu-id="4d570-124">Создание типа проблемы и назначение его типу несоответствия</span><span class="sxs-lookup"><span data-stu-id="4d570-124">Create a problem type and assign it to nonconformance types</span></span>

1. <span data-ttu-id="4d570-125">Перейдите в раздел **Управление запасами \> Настройка \> Управление качеством \> Типы проблемы**.</span><span class="sxs-lookup"><span data-stu-id="4d570-125">Go to **Inventory management \> Setup \> Quality management \> Problem types**.</span></span>
1. <span data-ttu-id="4d570-126">На панели операций выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="4d570-126">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="4d570-127">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="4d570-127">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="4d570-128">**Тип проблемы** — введите уникальный код или имя типа проблемы.</span><span class="sxs-lookup"><span data-stu-id="4d570-128">**Problem type** – Enter a unique ID or name for the problem type.</span></span>
    - <span data-ttu-id="4d570-129">**Описание** — введите подробное описание типа проблемы.</span><span class="sxs-lookup"><span data-stu-id="4d570-129">**Description** – Enter a detailed description of the problem type.</span></span>

1. <span data-ttu-id="4d570-130">Когда новая строка все еще выбрана, выберите **Типы несоответствия** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="4d570-130">While the new row is still selected, select **Non conformance types** on the Action Pane.</span></span>
1. <span data-ttu-id="4d570-131">На панели операций выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="4d570-131">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="4d570-132">Затем в новой строке задайте в поле **Тип несоответствия** тип несоответствия, который требуется разрешить для данного типа проблемы.</span><span class="sxs-lookup"><span data-stu-id="4d570-132">Then, for the new row, set the **Non conformance type** field to the nonconformance type that you want to allow for the problem type.</span></span>
1. <span data-ttu-id="4d570-133">Повторите предыдущий шаг для каждого дополнительного типа несоответствия, который необходимо разрешить для данного типа проблемы.</span><span class="sxs-lookup"><span data-stu-id="4d570-133">Repeat the previous step for each additional nonconformance type that you want to authorize for the problem type.</span></span>
1. <span data-ttu-id="4d570-134">Закройте страницы.</span><span class="sxs-lookup"><span data-stu-id="4d570-134">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d570-135">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4d570-135">Additional resources</span></span>

- [<span data-ttu-id="4d570-136">Обзор управления качеством</span><span class="sxs-lookup"><span data-stu-id="4d570-136">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="4d570-137">Включение управления качеством и несоответствием</span><span class="sxs-lookup"><span data-stu-id="4d570-137">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="4d570-138">Работники, ответственные за утверждение несоответствий</span><span class="sxs-lookup"><span data-stu-id="4d570-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="4d570-139">Карантинные зоны для несоответствий</span><span class="sxs-lookup"><span data-stu-id="4d570-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="4d570-140">Типы диагностики для несоответствий</span><span class="sxs-lookup"><span data-stu-id="4d570-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="4d570-141">Расходы по контролю качества для несоответствий</span><span class="sxs-lookup"><span data-stu-id="4d570-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="4d570-142">Операции для несоответствий</span><span class="sxs-lookup"><span data-stu-id="4d570-142">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="4d570-143">Управление качеством для складских процессов</span><span class="sxs-lookup"><span data-stu-id="4d570-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
