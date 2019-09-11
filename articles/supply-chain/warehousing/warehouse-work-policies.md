---
title: Обзор политик работы склада
description: Политики работы склада определяют, создается ли работа склада складскими процессами в производстве, исходя из типа заказа на выполнение работ, местонахождения запасов и продукта.
author: johanhoffmann
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 0a9e05fd2a08921d2718fc239afd56a957f80915
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865120"
---
# <a name="warehouse-work-policies-overview"></a><span data-ttu-id="5572f-103">Обзор политик работы склада</span><span class="sxs-lookup"><span data-stu-id="5572f-103">Warehouse work policies overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5572f-104">Политики работы склада определяют в Microsoft Dynamics 365 for Finance and Operations, создается ли работа склада складскими процессами в производстве, исходя из типа заказа на выполнение работ, местонахождения запасов и продукта.</span><span class="sxs-lookup"><span data-stu-id="5572f-104">Warehouse work policies in Microsoft Dynamics 365 for Finance and Operations control whether warehouse work is created by warehouse processes in manufacturing, based on work order type, inventory location, and product.</span></span>

<span data-ttu-id="5572f-105">Эта политика работы контролирует, создается ли работа склада для процессов склада в производстве.</span><span class="sxs-lookup"><span data-stu-id="5572f-105">This work policy controls whether warehouse work is created for warehouse processes in manufacturing.</span></span> <span data-ttu-id="5572f-106">Можно настроить политику работы с использованием сочетания **типы заказов на выполнение работ**, **местоположения запасов** и **продукта**.</span><span class="sxs-lookup"><span data-stu-id="5572f-106">You can set up the work policy by using a combination of **work order types**, an **inventory location**, and a **product**.</span></span> <span data-ttu-id="5572f-107">Например, продукт L0101 готов в выходном местоположении 001.</span><span class="sxs-lookup"><span data-stu-id="5572f-107">For example, product L0101 is reported as finished to output location 001.</span></span> <span data-ttu-id="5572f-108">Готовая продукция позже потребляется в другом производственном заказе в выходном местоположении 001.</span><span class="sxs-lookup"><span data-stu-id="5572f-108">The finished good is later consumed in another production order at output location 001.</span></span> <span data-ttu-id="5572f-109">В этом случае можно настроить политику работы для предотвращения создания работы для складирования готовых товаров, когда продукт L0101 регистрируется как готовый в выходном местоположении 001.</span><span class="sxs-lookup"><span data-stu-id="5572f-109">In this case, you can set up a work policy to prevent the work for finished goods put-away from being created when you report product L0101 as finished to output location 001.</span></span> <span data-ttu-id="5572f-110">Политика работы — это индивидуальный объект, который может быть описан с помощью следующей информации:</span><span class="sxs-lookup"><span data-stu-id="5572f-110">The work policy is an individual entity that can be described through the following information:</span></span>

-   <span data-ttu-id="5572f-111">**Имя политики работы** (уникальный код политики работы)</span><span class="sxs-lookup"><span data-stu-id="5572f-111">**Work policy name** (the unique identifier of the work policy)</span></span>
-   <span data-ttu-id="5572f-112">**Типы заказов на выполнение работ** и **Метод создания работы**</span><span class="sxs-lookup"><span data-stu-id="5572f-112">**Work order types** and **Work creation method**</span></span>
-   <span data-ttu-id="5572f-113">**Места хранения**</span><span class="sxs-lookup"><span data-stu-id="5572f-113">**Inventory locations**</span></span>
-   <span data-ttu-id="5572f-114">**Продукция**</span><span class="sxs-lookup"><span data-stu-id="5572f-114">**Products**</span></span>

## <a name="work-order-types"></a><span data-ttu-id="5572f-115">Типы заказов на выполнение работ</span><span class="sxs-lookup"><span data-stu-id="5572f-115">Work order types</span></span>
<span data-ttu-id="5572f-116">Для выбора доступны следующие типы заказов на выполнение работ:</span><span class="sxs-lookup"><span data-stu-id="5572f-116">You can select the following work order types:</span></span>

-   <span data-ttu-id="5572f-117">Готовая продукция разгружена</span><span class="sxs-lookup"><span data-stu-id="5572f-117">Finished goods put away</span></span>
-   <span data-ttu-id="5572f-118">Размещение побочных и попутных продуктов</span><span class="sxs-lookup"><span data-stu-id="5572f-118">Co-product and by-product put away</span></span>
-   <span data-ttu-id="5572f-119">Комплектация сырья</span><span class="sxs-lookup"><span data-stu-id="5572f-119">Raw material picking</span></span>

<span data-ttu-id="5572f-120">Поле **Метод создания работы** имеет значение **Никогда**.</span><span class="sxs-lookup"><span data-stu-id="5572f-120">The **Work creation method** field has the value **Never**.</span></span> <span data-ttu-id="5572f-121">Это значение указывает, что политика работы не позволяет создавать работу склада для выбранного типа заказа на выполнение работ.</span><span class="sxs-lookup"><span data-stu-id="5572f-121">This value indicates that the work policy will prevent warehouse work from being created for the selected work order type.</span></span>

## <a name="inventory-locations"></a><span data-ttu-id="5572f-122">Места хранения</span><span class="sxs-lookup"><span data-stu-id="5572f-122">Inventory locations</span></span>
<span data-ttu-id="5572f-123">Можно выбрать местоположение, к которому применяется политика работы.</span><span class="sxs-lookup"><span data-stu-id="5572f-123">You can select a location that the work policy applies to.</span></span> <span data-ttu-id="5572f-124">Если ни одно местоположение не связано с политикой работы, эта политика работы не применяется ни к каким процессам.</span><span class="sxs-lookup"><span data-stu-id="5572f-124">If no location is associated with a work policy, the work policy doesn’t apply to any processes.</span></span> <span data-ttu-id="5572f-125">На странице **Местоположения** можно также выбрать или отменить выбор политики работы для конкретного местоположения.</span><span class="sxs-lookup"><span data-stu-id="5572f-125">On the **Locations** page, you can also select or cancel the selection of the work policy for a specific location.</span></span>

## <a name="products"></a><span data-ttu-id="5572f-126">Товары</span><span class="sxs-lookup"><span data-stu-id="5572f-126">Products</span></span>
<span data-ttu-id="5572f-127">Можно выбрать продукт, к которому применяется политика работы.</span><span class="sxs-lookup"><span data-stu-id="5572f-127">You can select a product that the work policy applies to.</span></span> <span data-ttu-id="5572f-128">Можно применить политику работы либо ко всем продуктам, либо к выбранным продуктам.</span><span class="sxs-lookup"><span data-stu-id="5572f-128">You can apply the work policy to either all products or selected products.</span></span>

## <a name="example"></a><span data-ttu-id="5572f-129">Пример</span><span class="sxs-lookup"><span data-stu-id="5572f-129">Example</span></span>
<span data-ttu-id="5572f-130">В следующем примере имеются два производственных заказа, PRD-001 и PRD-00*2*.</span><span class="sxs-lookup"><span data-stu-id="5572f-130">In the following example, there are two production orders, PRD-001 and PRD-00*2*.</span></span> <span data-ttu-id="5572f-131">Производственный заказ PRD-001 имеет операцию **Сборка**, в которой готовый продукт SC1 сдается в местоположении O1.</span><span class="sxs-lookup"><span data-stu-id="5572f-131">Production order PRD-001 has an operation that is named **Assembly**, where product SC1 is being reported as finished to location O1.</span></span> <span data-ttu-id="5572f-132">Производственный заказ PRD-002 содержит операций **Покраска**, которая потребляет продукт SC1 из местоположения O1.</span><span class="sxs-lookup"><span data-stu-id="5572f-132">Production order PRD-002 has an operation that is named **Painting** and consumes product SC1 from location O1.</span></span> <span data-ttu-id="5572f-133">Производственный заказ PRD-002 также потребляет сырье RM1 из местоположения O1.</span><span class="sxs-lookup"><span data-stu-id="5572f-133">Production order PRD-002 also consumes raw material RM1 from location O1.</span></span> <span data-ttu-id="5572f-134">RM1 хранится в местоположении склада BULK-001 и будет скомплектован в местоположении O1 работой склада для комплектации сырья.</span><span class="sxs-lookup"><span data-stu-id="5572f-134">RM1 is stored in warehouse location BULK-001 and will be picked to location O1 by warehouse work for raw material picking.</span></span> <span data-ttu-id="5572f-135">Работа комплектации создается, когда производство PRD-002 запущено.</span><span class="sxs-lookup"><span data-stu-id="5572f-135">The picking work is generated when production PRD-002 is released.</span></span> 

<span data-ttu-id="5572f-136">[![Политики работы склада](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="5572f-136">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span> 

<span data-ttu-id="5572f-137">Если планируется настроить политику работы склада для этого сценария, следует рассмотреть следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="5572f-137">When you plan to configure a warehouse work policy for this scenario, you should consider the following information:</span></span>

-   <span data-ttu-id="5572f-138">Работа склада для складирования готовой продукции не требуется при регистрации продукта SC1 как завершенного из производственного заказа PRD-001 в местоположении O1.</span><span class="sxs-lookup"><span data-stu-id="5572f-138">Warehouse work for finished goods put-away isn’t required when you report product SC1 as finished from production order PRD-001 to location O1.</span></span> <span data-ttu-id="5572f-139">Это связано с тем, что операция **Покраска** для производственного заказа PRD-002 потребляет SC1 в этом же месте.</span><span class="sxs-lookup"><span data-stu-id="5572f-139">This is because the **Painting** operation for production order PRD-002 consumes SC1 at the same location.</span></span>
-   <span data-ttu-id="5572f-140">Работа склада для комплектации сырья требуется для перемещения сырья RM1 из местоположения склада BULK-001 в местоположение O1.</span><span class="sxs-lookup"><span data-stu-id="5572f-140">Warehouse work for raw material picking is required in order to move raw material RM1 from warehouse location BULK-001 to location O1.</span></span>

<span data-ttu-id="5572f-141">Ниже приводится пример политики работы, которую можно настроить на основе этой информации.</span><span class="sxs-lookup"><span data-stu-id="5572f-141">Here is an example of the work policy that you can set up, based on these considerations.</span></span>


|                                       |                                       |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="5572f-142"><strong>Имя политики работы</strong></span><span class="sxs-lookup"><span data-stu-id="5572f-142"><strong>Work policy name</strong></span></span><br> | <span data-ttu-id="5572f-143"><strong>Типы заказов на выполнение работ</strong></span><span class="sxs-lookup"><span data-stu-id="5572f-143"><strong>Work order types</strong></span></span><br> |
|         <span data-ttu-id="5572f-144">Не складировать 01     \`</span><span class="sxs-lookup"><span data-stu-id="5572f-144">No put away 01     \`</span></span>          |     <span data-ttu-id="5572f-145">- Готовая продукция складирована</span><span class="sxs-lookup"><span data-stu-id="5572f-145">- Finished good put away</span></span><br>      |
|                                       |    <span data-ttu-id="5572f-146"><strong>Местоположение</strong></span><span class="sxs-lookup"><span data-stu-id="5572f-146"><strong>Locations</strong></span></span><br>     |
|                                       |                 <span data-ttu-id="5572f-147">- O1</span><span class="sxs-lookup"><span data-stu-id="5572f-147">- O1</span></span>                  |
|                                       |    <span data-ttu-id="5572f-148"><strong>Товары</strong></span><span class="sxs-lookup"><span data-stu-id="5572f-148"><strong>Products</strong></span></span> <br>     |
|                                       |                 <span data-ttu-id="5572f-149">- SC1</span><span class="sxs-lookup"><span data-stu-id="5572f-149">- SC1</span></span>                 |

<span data-ttu-id="5572f-150">Следующие процедуры предоставляют пошаговые инструкции о том, как настроить политику работы склада для данного сценария.</span><span class="sxs-lookup"><span data-stu-id="5572f-150">The following procedures provide step-by-step instructions about how to set up the warehouse work policy for this scenario.</span></span> <span data-ttu-id="5572f-151">Также описывается пример настройки, показывающий, как сообщать о готовности производственного заказа, который не контролируется грузоместом.</span><span class="sxs-lookup"><span data-stu-id="5572f-151">A sample setup showing how to report a production order as finished to a location that isn’t license plate–controlled is also described.</span></span>

## <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="5572f-152">Настройка политики работы склада</span><span class="sxs-lookup"><span data-stu-id="5572f-152">Set up a warehouse work policy</span></span>
<span data-ttu-id="5572f-153">Процессы склада не всегда включают работу склада.</span><span class="sxs-lookup"><span data-stu-id="5572f-153">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="5572f-154">Определяя политику работы, можно предотвратить создание работы для комплектации сырья и размещения готовой продукции для набора продуктов в определенных местонахождениях.</span><span class="sxs-lookup"><span data-stu-id="5572f-154">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="5572f-155">Компания USMF с демонстрационными данными используется для создания этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="5572f-155">The USMF demo data company was used to create this procedure.</span></span> 

<span data-ttu-id="5572f-156">ЭТАПЫ (21)</span><span class="sxs-lookup"><span data-stu-id="5572f-156">STEPS (21)</span></span>

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| <span data-ttu-id="5572f-157">1.</span><span class="sxs-lookup"><span data-stu-id="5572f-157">1.</span></span>  | <span data-ttu-id="5572f-158">Перейдите в раздел "Управление складом" &gt; "Настройка" &gt; "Работа" &gt; "Политики работы".</span><span class="sxs-lookup"><span data-stu-id="5572f-158">Go to Warehouse management &gt; Setup &gt; Work &gt; Work policies.</span></span>        |
| <span data-ttu-id="5572f-159">2.</span><span class="sxs-lookup"><span data-stu-id="5572f-159">2.</span></span>  | <span data-ttu-id="5572f-160">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="5572f-160">Click New.</span></span>                                                                 |
| <span data-ttu-id="5572f-161">3.</span><span class="sxs-lookup"><span data-stu-id="5572f-161">3.</span></span>  | <span data-ttu-id="5572f-162">В поле "Имя политики работы" введите "Не работа размещения".</span><span class="sxs-lookup"><span data-stu-id="5572f-162">In the Work policy name field, type 'No put-away work'.</span></span>                    |
| <span data-ttu-id="5572f-163">4.</span><span class="sxs-lookup"><span data-stu-id="5572f-163">4.</span></span>  | <span data-ttu-id="5572f-164">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="5572f-164">Click Save.</span></span>                                                                |
| <span data-ttu-id="5572f-165">5.</span><span class="sxs-lookup"><span data-stu-id="5572f-165">5.</span></span>  | <span data-ttu-id="5572f-166">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5572f-166">Click Add.</span></span>                                                                 |
| <span data-ttu-id="5572f-167">6.</span><span class="sxs-lookup"><span data-stu-id="5572f-167">6.</span></span>  | <span data-ttu-id="5572f-168">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5572f-168">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="5572f-169">7.</span><span class="sxs-lookup"><span data-stu-id="5572f-169">7.</span></span>  | <span data-ttu-id="5572f-170">В поле "Тип заказа на выполнение работ" выберите "Размещение готовой продукции".</span><span class="sxs-lookup"><span data-stu-id="5572f-170">In the Work order type field, select 'Finished goods put away'.</span></span>            |
| <span data-ttu-id="5572f-171">8.</span><span class="sxs-lookup"><span data-stu-id="5572f-171">8.</span></span>  | <span data-ttu-id="5572f-172">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5572f-172">Click Add.</span></span>                                                                 |
| <span data-ttu-id="5572f-173">9.</span><span class="sxs-lookup"><span data-stu-id="5572f-173">9.</span></span>  | <span data-ttu-id="5572f-174">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5572f-174">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="5572f-175">10.</span><span class="sxs-lookup"><span data-stu-id="5572f-175">10.</span></span> | <span data-ttu-id="5572f-176">В поле "Тип заказа на выполнение работ" выберите "Размещение побочного и сопутствующего продуктов".</span><span class="sxs-lookup"><span data-stu-id="5572f-176">In the Work order type field, select 'Co-product and by-product put away'.</span></span> |
| <span data-ttu-id="5572f-177">11.</span><span class="sxs-lookup"><span data-stu-id="5572f-177">11.</span></span> | <span data-ttu-id="5572f-178">Разверните раздел "Места хранения".</span><span class="sxs-lookup"><span data-stu-id="5572f-178">Expand the Inventory locations section.</span></span>                                    |
| <span data-ttu-id="5572f-179">12.</span><span class="sxs-lookup"><span data-stu-id="5572f-179">12.</span></span> | <span data-ttu-id="5572f-180">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5572f-180">Click Add.</span></span>                                                                 |
| <span data-ttu-id="5572f-181">13.</span><span class="sxs-lookup"><span data-stu-id="5572f-181">13.</span></span> | <span data-ttu-id="5572f-182">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5572f-182">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="5572f-183">14.</span><span class="sxs-lookup"><span data-stu-id="5572f-183">14.</span></span> | <span data-ttu-id="5572f-184">В списке "Склад" введите "51".</span><span class="sxs-lookup"><span data-stu-id="5572f-184">In the Warehouse list, enter '51'.</span></span>                                         |
| <span data-ttu-id="5572f-185">15.</span><span class="sxs-lookup"><span data-stu-id="5572f-185">15.</span></span> | <span data-ttu-id="5572f-186">В поле "Местонахождение" введите или выберите "001".</span><span class="sxs-lookup"><span data-stu-id="5572f-186">In the Location field, enter or select '001'.</span></span>                              |
| <span data-ttu-id="5572f-187">16.</span><span class="sxs-lookup"><span data-stu-id="5572f-187">16.</span></span> | <span data-ttu-id="5572f-188">Разверните раздел "Продукты".</span><span class="sxs-lookup"><span data-stu-id="5572f-188">Expand the Products section.</span></span>                                               |
| <span data-ttu-id="5572f-189">17.</span><span class="sxs-lookup"><span data-stu-id="5572f-189">17.</span></span> | <span data-ttu-id="5572f-190">В поле "Выбор продукта" выберите "Выбрано".</span><span class="sxs-lookup"><span data-stu-id="5572f-190">In the Product selection field, select 'Selected'.</span></span>                         |
| <span data-ttu-id="5572f-191">18.</span><span class="sxs-lookup"><span data-stu-id="5572f-191">18.</span></span> | <span data-ttu-id="5572f-192">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5572f-192">Click Add.</span></span>                                                                 |
| <span data-ttu-id="5572f-193">19.</span><span class="sxs-lookup"><span data-stu-id="5572f-193">19.</span></span> | <span data-ttu-id="5572f-194">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5572f-194">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="5572f-195">20.</span><span class="sxs-lookup"><span data-stu-id="5572f-195">20.</span></span> | <span data-ttu-id="5572f-196">В поле "Код номенклатуры" введите или выберите "L0101".</span><span class="sxs-lookup"><span data-stu-id="5572f-196">In the Item number field, enter or select 'L0101'.</span></span>                         |
| <span data-ttu-id="5572f-197">21.</span><span class="sxs-lookup"><span data-stu-id="5572f-197">21.</span></span> | <span data-ttu-id="5572f-198">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="5572f-198">Click Save.</span></span>                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="5572f-199">Приемка производственного заказа как готового в местоположении, которое не контролируется грузоместом</span><span class="sxs-lookup"><span data-stu-id="5572f-199">Report a production order as finished to a location that isn’t license plate–controlled</span></span>
<span data-ttu-id="5572f-200">В этой процедуре показан пример приемки отчетности в местонахождении, которое не управляется грузоместом.</span><span class="sxs-lookup"><span data-stu-id="5572f-200">This procedure shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="5572f-201">Применимая политика работы является обязательным условием для этой задачи.</span><span class="sxs-lookup"><span data-stu-id="5572f-201">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="5572f-202">Предыдущая процедура показывает настройку политики работы.</span><span class="sxs-lookup"><span data-stu-id="5572f-202">The previous procedure shows the setup of the work policy.</span></span> 

<span data-ttu-id="5572f-203">ЭТАПЫ (25)</span><span class="sxs-lookup"><span data-stu-id="5572f-203">STEPS (25)</span></span>

<table>
<tbody>
<tr>
<td colspan="3"><span data-ttu-id="5572f-204"><strong>Подзадача: настройка выходного местонахождения.</strong></span><span class="sxs-lookup"><span data-stu-id="5572f-204"><strong>Sub-task: Set up an output location.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="5572f-205">Перейдите в раздел "Управление организацией" &gt; "Ресурсы" &gt; "Группы ресурсов".</span><span class="sxs-lookup"><span data-stu-id="5572f-205">Go to Organization administration &gt; Resources &gt; Resource groups.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="5572f-206">В списке выберите группу ресурсов "5102".</span><span class="sxs-lookup"><span data-stu-id="5572f-206">In the list, select resource group &#39;5102&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="5572f-207">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="5572f-207">Click Edit.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="5572f-208">В поле "Склад выпуска" введите "51".</span><span class="sxs-lookup"><span data-stu-id="5572f-208">In the Output warehouse field, enter &#39;51&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="5572f-209">В поле "Местонахождение выхода" введите "001".</span><span class="sxs-lookup"><span data-stu-id="5572f-209">In the Output location field, enter &#39;001&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="5572f-210">Местонахождение 001 не является местонахождением под управлением грузоместа.</span><span class="sxs-lookup"><span data-stu-id="5572f-210">Location 001 isn&#39;t a license plate–controlled location.</span></span> <span data-ttu-id="5572f-211">Местонахождение выхода, которое не находится под управлением грузоместа, можно настроить, только если для местоположения существует соответствующая политика работы.</span><span class="sxs-lookup"><span data-stu-id="5572f-211">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span></td>
</tr>
<tr>
<td colspan="3"><span data-ttu-id="5572f-212"><strong>Подзадача: создание производственного заказа и его приемка.</strong></span><span class="sxs-lookup"><span data-stu-id="5572f-212"><strong>Sub-task: Create a production order and report it as finished.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="5572f-213">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5572f-213">Close the page.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="5572f-214">Перейдите в раздел "Управление производством" &gt; "Производственные заказы" &gt; "Все производственные заказы".</span><span class="sxs-lookup"><span data-stu-id="5572f-214">Go to Production control &gt; Production orders &gt; All production orders.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="5572f-215">Щелкните "Новый производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="5572f-215">Click New production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="5572f-216">В поле "Код номенклатуры" введите "L0101".</span><span class="sxs-lookup"><span data-stu-id="5572f-216">In the Item number field, enter &#39;L0101&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="5572f-217">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="5572f-217">Click Create.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="5572f-218">В области действий щелкните "Производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="5572f-218">On the Action Pane, click Production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td><span data-ttu-id="5572f-219">Щелкните "Оценка".</span><span class="sxs-lookup"><span data-stu-id="5572f-219">Click Estimate.</span></span></td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td><span data-ttu-id="5572f-220">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="5572f-220">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td><span data-ttu-id="5572f-221">Щелкните "Начать".</span><span class="sxs-lookup"><span data-stu-id="5572f-221">Click Start.</span></span></td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td><span data-ttu-id="5572f-222">Перейдите на вкладку "Общие".</span><span class="sxs-lookup"><span data-stu-id="5572f-222">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td><span data-ttu-id="5572f-223">В поле "Автопотребление по спецификации" выберите "Никогда".</span><span class="sxs-lookup"><span data-stu-id="5572f-223">In the Automatic BOM consumption field, select &#39;Never&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td><span data-ttu-id="5572f-224">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="5572f-224">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td><span data-ttu-id="5572f-225">Щелкните "Приемка".</span><span class="sxs-lookup"><span data-stu-id="5572f-225">Click Report as finished.</span></span></td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td><span data-ttu-id="5572f-226">Перейдите на вкладку "Общие".</span><span class="sxs-lookup"><span data-stu-id="5572f-226">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td><span data-ttu-id="5572f-227">Выберите значение "Да" в поле "Допускать ошибки".</span><span class="sxs-lookup"><span data-stu-id="5572f-227">Select Yes in the Accept error field.</span></span></td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td><span data-ttu-id="5572f-228">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="5572f-228">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td><span data-ttu-id="5572f-229">В области действий щелкните "Склад".</span><span class="sxs-lookup"><span data-stu-id="5572f-229">On the Action Pane, click Warehouse.</span></span></td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td><span data-ttu-id="5572f-230">Щелкните "Сведения о работе".</span><span class="sxs-lookup"><span data-stu-id="5572f-230">Click Work details.</span></span></td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td><span data-ttu-id="5572f-231">При учете производственного заказа не была создана работа размещения.</span><span class="sxs-lookup"><span data-stu-id="5572f-231">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="5572f-232">Это происходит, потому что определена политика работы, которая предотвращает создание работы при приемке продукта L0101 в местоположении 001.</span><span class="sxs-lookup"><span data-stu-id="5572f-232">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span></td>
</tr>
</tbody>
</table>



