---
title: Определение и ведение каналов розничной торговли
description: Эта тема предоставляет обзор процесса для настройки реальных магазинов, которые называются розничными магазинами в Dynamics 365 Retail. Она содержит сведения о задачах, которую следует выполнить как до, так и после настройки розничного магазина.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 45d0386d215da15103a417502debb245c91f6309
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934616"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="c3fde-104">Определение и ведение каналов розничной торговли</span><span class="sxs-lookup"><span data-stu-id="c3fde-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c3fde-105">Эта тема предоставляет обзор процесса для настройки реальных магазинов, которые называются розничными магазинами в Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="c3fde-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Dynamics 365 Retail.</span></span> <span data-ttu-id="c3fde-106">Она содержит сведения о задачах, которую следует выполнить как до, так и после настройки розничного магазина.</span><span class="sxs-lookup"><span data-stu-id="c3fde-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="c3fde-107">Retail поддерживает несколько каналов розничной торговли, таких как интернет-магазины, центры обработки вызовов и физические магазины.</span><span class="sxs-lookup"><span data-stu-id="c3fde-107">Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="c3fde-108">Физические магазины называются розничными магазинами.</span><span class="sxs-lookup"><span data-stu-id="c3fde-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="c3fde-109">Каждый розничный магазин может иметь свои собственные способы оплаты, группы цен, контрольно-кассовые машины POS, счета выручки и расходов и сотрудников.</span><span class="sxs-lookup"><span data-stu-id="c3fde-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="c3fde-110">Необходимо настроит все эти элементы для магазина розничной торговли до его создания.</span><span class="sxs-lookup"><span data-stu-id="c3fde-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="c3fde-111">После создания магазина розничной торговли назначаются продукты, которые должны использоваться в магазине.</span><span class="sxs-lookup"><span data-stu-id="c3fde-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="c3fde-112">Кроме того, необходимо назначить сотрудников, кассы и клиентов для магазина.</span><span class="sxs-lookup"><span data-stu-id="c3fde-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="c3fde-113">Наконец, следует добавить новый магазин в организационную иерархию.</span><span class="sxs-lookup"><span data-stu-id="c3fde-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="c3fde-114">Настройка розничных магазинов</span><span class="sxs-lookup"><span data-stu-id="c3fde-114">Setting up retail stores</span></span>

<span data-ttu-id="c3fde-115">Перед настройкой розничного магазина в Retail, необходимо выполнить некоторые задачи.</span><span class="sxs-lookup"><span data-stu-id="c3fde-115">Before you can set up a retail store in Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="c3fde-116">Затем можно создать магазин розничной торговли и добавить сведения.</span><span class="sxs-lookup"><span data-stu-id="c3fde-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="c3fde-117">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="c3fde-117">Prerequisites</span></span>

<span data-ttu-id="c3fde-118">Перед настройкой магазина розничной торговли необходимо выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="c3fde-118">You must complete the following tasks before you can set up a retail store:</span></span>

1. <span data-ttu-id="c3fde-119">Настройка организационной структуры и настройка организационных иерархий для розничных ассортиментов, пополнения и отчетности.</span><span class="sxs-lookup"><span data-stu-id="c3fde-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="c3fde-120">Настройка склада, представляющего магазин розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="c3fde-120">Set up a warehouse that represents the retail store.</span></span>
3. <span data-ttu-id="c3fde-121">Настройка номерных серий для розничных магазинов, журналов операций магазина и ваучеров журнала операций.</span><span class="sxs-lookup"><span data-stu-id="c3fde-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="c3fde-122">Настройка параметров розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="c3fde-122">Configure parameters for Retail.</span></span>
5. <span data-ttu-id="c3fde-123">Настройка способов оплаты, принимаемых в магазине.</span><span class="sxs-lookup"><span data-stu-id="c3fde-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="c3fde-124">Для обработки проводок кредитной карты в Retail POS можно также настроить службы платежей.</span><span class="sxs-lookup"><span data-stu-id="c3fde-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="c3fde-125">Настройка налоговых групп.</span><span class="sxs-lookup"><span data-stu-id="c3fde-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="c3fde-126">Настройка розничных продуктов.</span><span class="sxs-lookup"><span data-stu-id="c3fde-126">Set up retail products.</span></span> <span data-ttu-id="c3fde-127">В рамках этой задачи также можно настроить иерархии розничных продуктов, варианты продукта и ассортименты продуктов.</span><span class="sxs-lookup"><span data-stu-id="c3fde-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="c3fde-128">Настройка ценовых групп продуктов.</span><span class="sxs-lookup"><span data-stu-id="c3fde-128">Set up product price groups.</span></span>
10. <span data-ttu-id="c3fde-129">Настроить ценообразование розничных продуктов.</span><span class="sxs-lookup"><span data-stu-id="c3fde-129">Set up retail product pricing.</span></span> <span data-ttu-id="c3fde-130">В рамках этой задачи также можно настроить корректировки цен, скидки и периоды скидки.</span><span class="sxs-lookup"><span data-stu-id="c3fde-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="c3fde-131">Настройка штатных сотрудников.</span><span class="sxs-lookup"><span data-stu-id="c3fde-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c3fde-132">Также необходимо назначить соответствующие разрешения работникам, чтобы они могли входить и выполнять задачи с помощью системы Retail POS.</span><span class="sxs-lookup"><span data-stu-id="c3fde-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Retail POS system.</span></span>

12. <span data-ttu-id="c3fde-133">Настройка профилей Retail POS для назначения магазину.</span><span class="sxs-lookup"><span data-stu-id="c3fde-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="c3fde-134">Эта задача включает множество других задач, таких как настройка регистров, настройка автономных профилей и настройка форматов чеков и профилей.</span><span class="sxs-lookup"><span data-stu-id="c3fde-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="c3fde-135">Просмотрите все задачи, включенные в предварительные условия, и выполните только те задачи, которые применяются к вам.</span><span class="sxs-lookup"><span data-stu-id="c3fde-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="c3fde-136">Настройка розничного магазина</span><span class="sxs-lookup"><span data-stu-id="c3fde-136">Set up a retail store</span></span>

<span data-ttu-id="c3fde-137">После завершения обязательных задач выполните следующие задачи, чтобы настроить сведения для магазина розничной торговли:</span><span class="sxs-lookup"><span data-stu-id="c3fde-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1. <span data-ttu-id="c3fde-138">создайте розничный магазин.</span><span class="sxs-lookup"><span data-stu-id="c3fde-138">Create a retail store.</span></span>
2. <span data-ttu-id="c3fde-139">Назначьте налоговую группа для магазина.</span><span class="sxs-lookup"><span data-stu-id="c3fde-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="c3fde-140">Назначьте принятые способы оплаты для магазина.</span><span class="sxs-lookup"><span data-stu-id="c3fde-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="c3fde-141">Добавьте сведения в описания продуктов, которые предлагаются в магазинах розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="c3fde-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="c3fde-142">Например, можно добавить форматированный текст и изображения.</span><span class="sxs-lookup"><span data-stu-id="c3fde-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="c3fde-143">Эти сведения о продуктах отображаются в различных контекстах, например в регистре POS или на распечатанных этикетках.</span><span class="sxs-lookup"><span data-stu-id="c3fde-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="c3fde-144">Добавление магазина в организационную иерархию по умолчанию, которая назначена цели **Розничный ассортимент**, **Пополнение запасов для розничной торговли** или **Отчетность по розничной торговле**.</span><span class="sxs-lookup"><span data-stu-id="c3fde-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="c3fde-145">После настройки розничного магазина</span><span class="sxs-lookup"><span data-stu-id="c3fde-145">After you set up a retail store</span></span>

<span data-ttu-id="c3fde-146">После ввода сведений для магазина розничной торговли выполните следующие задачи, чтобы отправлять новые данные магазина розничной торговли в Retail POS:</span><span class="sxs-lookup"><span data-stu-id="c3fde-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1. <span data-ttu-id="c3fde-147">Настройка регистров POS для магазина.</span><span class="sxs-lookup"><span data-stu-id="c3fde-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="c3fde-148">Назначение ассортиментов продуктов магазину.</span><span class="sxs-lookup"><span data-stu-id="c3fde-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="c3fde-149">Обработайте ассортименты, чтобы создать список продуктов, включенных в ассортимент, и чтобы сделать продукты доступными в розничном магазине.</span><span class="sxs-lookup"><span data-stu-id="c3fde-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4. <span data-ttu-id="c3fde-150">Отправка данных, таких как номерные серии, профили оборудования и макеты экрана POS в регистры Retail POS.</span><span class="sxs-lookup"><span data-stu-id="c3fde-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5. <span data-ttu-id="c3fde-151">Публикация магазина розничной торговли для отправки данных о магазине в Retail POS.</span><span class="sxs-lookup"><span data-stu-id="c3fde-151">Publish the retail store to send store data to Retail POS.</span></span>
6. <span data-ttu-id="c3fde-152">Выполнение заданий для отправки данных магазина в Retail POS.</span><span class="sxs-lookup"><span data-stu-id="c3fde-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="c3fde-153">Организационные иерархии</span><span class="sxs-lookup"><span data-stu-id="c3fde-153">Organization hierarchies</span></span>

<span data-ttu-id="c3fde-154">Retail использует организационные иерархии для структурирования розничных каналов.</span><span class="sxs-lookup"><span data-stu-id="c3fde-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="c3fde-155">Организационные иерархии представляют собой связи между организациями, которые занимаются коммерческой деятельностью.</span><span class="sxs-lookup"><span data-stu-id="c3fde-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="c3fde-156">При настройке магазинов их можно добавить в организационную иерархию.</span><span class="sxs-lookup"><span data-stu-id="c3fde-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="c3fde-157">После этого магазины могут совместно использовать данные по ассортименту, пополнению и отчетности.</span><span class="sxs-lookup"><span data-stu-id="c3fde-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="c3fde-158">Для использования функциональности продаж Retail необходимо включить ключ конфигурации для **Несколько получателей**.</span><span class="sxs-lookup"><span data-stu-id="c3fde-158">To use Retail sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="c3fde-159">Этот ключ конфигурации можно найти в ключах **Конфигурация торговли** в **Администрирование системы**\> **Настройка** \> **Конфигурация лицензии**.</span><span class="sxs-lookup"><span data-stu-id="c3fde-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="c3fde-160">Это необходимо из-за функций Retail, которые выполняют различные проверки на основе адреса поставки, настроенного на уровне строки заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="c3fde-160">This is required due to Retail functionality that performs various validations based on the delivery address configured at the sales order line level.</span></span>
