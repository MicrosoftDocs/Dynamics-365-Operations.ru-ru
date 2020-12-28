---
title: Определение и ведение каналов розничной торговли
description: Эта тема предоставляет обзор процесса для настройки реальных магазинов, которые называются магазинами в Dynamics 365 Commerce. Она содержит сведения о задачах, которую следует выполнить как до, так и после настройки магазина.
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
ms.openlocfilehash: 0fbca2c9178cd372653287afdf72deaf75442604
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415155"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="d3aee-104">Определение и ведение каналов розничной торговли</span><span class="sxs-lookup"><span data-stu-id="d3aee-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d3aee-105">Эта тема предоставляет обзор процесса для настройки реальных магазинов, которые называются магазинами в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d3aee-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as stores in Dynamics 365 Commerce.</span></span> <span data-ttu-id="d3aee-106">Она содержит сведения о задачах, которую следует выполнить как до, так и после настройки магазина.</span><span class="sxs-lookup"><span data-stu-id="d3aee-106">It includes information about the tasks that you must complete both before and after you set up a store.</span></span>

<span data-ttu-id="d3aee-107">Commerce поддерживает несколько каналов розничной торговли, таких как интернет-магазины, центры обработки вызовов и физические магазины.</span><span class="sxs-lookup"><span data-stu-id="d3aee-107">Commerce supports multiple channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="d3aee-108">Физические магазины называются магазинами.</span><span class="sxs-lookup"><span data-stu-id="d3aee-108">A brick-and-mortar store is called a store.</span></span> <span data-ttu-id="d3aee-109">Каждый магазин может иметь свои собственные способы оплаты, группы цен, контрольно-кассовые машины POS, счета выручки и расходов и сотрудников.</span><span class="sxs-lookup"><span data-stu-id="d3aee-109">Each store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="d3aee-110">Необходимо настроить все эти элементы для магазина торговли до его создания.</span><span class="sxs-lookup"><span data-stu-id="d3aee-110">You must set up all these elements for a store before you create it.</span></span> <span data-ttu-id="d3aee-111">После создания магазина торговли назначаются продукты, которые должны использоваться в магазине.</span><span class="sxs-lookup"><span data-stu-id="d3aee-111">After you create the store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="d3aee-112">Кроме того, необходимо назначить сотрудников, кассы и клиентов для магазина.</span><span class="sxs-lookup"><span data-stu-id="d3aee-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="d3aee-113">Наконец, следует добавить новый магазин в организационную иерархию.</span><span class="sxs-lookup"><span data-stu-id="d3aee-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-stores"></a><span data-ttu-id="d3aee-114">Настройка магазинов</span><span class="sxs-lookup"><span data-stu-id="d3aee-114">Setting up stores</span></span>

<span data-ttu-id="d3aee-115">Перед настройкой магазина в Commerce, необходимо выполнить некоторые задачи.</span><span class="sxs-lookup"><span data-stu-id="d3aee-115">Before you can set up a store in Commerce, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="d3aee-116">Затем можно создать магазин и добавить сведения.</span><span class="sxs-lookup"><span data-stu-id="d3aee-116">You can then create the store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="d3aee-117">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="d3aee-117">Prerequisites</span></span>

<span data-ttu-id="d3aee-118">Перед настройкой магазина необходимо выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="d3aee-118">You must complete the following tasks before you can set up a store:</span></span>

1. <span data-ttu-id="d3aee-119">Настройка организационной структуры и настройка организационных иерархий для розничных ассортиментов, пополнения и отчетности.</span><span class="sxs-lookup"><span data-stu-id="d3aee-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="d3aee-120">Настройка склада, представляющего магазин.</span><span class="sxs-lookup"><span data-stu-id="d3aee-120">Set up a warehouse that represents the store.</span></span>
3. <span data-ttu-id="d3aee-121">Настройка номерных серий для магазинов, журналов операций магазина и ваучеров журнала операций.</span><span class="sxs-lookup"><span data-stu-id="d3aee-121">Set up number sequences for stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="d3aee-122">Настройка параметров для Commerce.</span><span class="sxs-lookup"><span data-stu-id="d3aee-122">Configure parameters for Commerce.</span></span>
5. <span data-ttu-id="d3aee-123">Настройка способов оплаты, принимаемых в магазине.</span><span class="sxs-lookup"><span data-stu-id="d3aee-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="d3aee-124">Для обработки проводок кредитной карты в POS-регистрах можно также настроить службы платежей.</span><span class="sxs-lookup"><span data-stu-id="d3aee-124">To process credit card transactions at POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="d3aee-125">Настройка налоговых групп.</span><span class="sxs-lookup"><span data-stu-id="d3aee-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="d3aee-126">Настройка продуктов.</span><span class="sxs-lookup"><span data-stu-id="d3aee-126">Set up products.</span></span> <span data-ttu-id="d3aee-127">В рамках этой задачи также можно настроить иерархии продуктов, варианты продукта и ассортименты продуктов.</span><span class="sxs-lookup"><span data-stu-id="d3aee-127">As part of this task, you also set up product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="d3aee-128">Настройка ценовых групп продуктов.</span><span class="sxs-lookup"><span data-stu-id="d3aee-128">Set up product price groups.</span></span>
10. <span data-ttu-id="d3aee-129">Настройте цены продуктов.</span><span class="sxs-lookup"><span data-stu-id="d3aee-129">Set up product pricing.</span></span> <span data-ttu-id="d3aee-130">В рамках этой задачи также можно настроить корректировки цен, скидки и периоды скидки.</span><span class="sxs-lookup"><span data-stu-id="d3aee-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="d3aee-131">Настройка штатных сотрудников.</span><span class="sxs-lookup"><span data-stu-id="d3aee-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d3aee-132">Также необходимо назначить соответствующие разрешения работникам, чтобы они могли входить и выполнять задачи с помощью системы POS.</span><span class="sxs-lookup"><span data-stu-id="d3aee-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the POS system.</span></span>

12. <span data-ttu-id="d3aee-133">Настройте профили POS для назначения магазину.</span><span class="sxs-lookup"><span data-stu-id="d3aee-133">Configure the POS profiles to assign to the store.</span></span> <span data-ttu-id="d3aee-134">Эта задача включает множество других задач, таких как настройка регистров, настройка автономных профилей и настройка форматов чеков и профилей.</span><span class="sxs-lookup"><span data-stu-id="d3aee-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="d3aee-135">Просмотрите все задачи, включенные в предварительные условия, и выполните только те задачи, которые применяются к вам.</span><span class="sxs-lookup"><span data-stu-id="d3aee-135">Review all the tasks that are included in the prerequisites, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-store"></a><span data-ttu-id="d3aee-136">Настройка магазина</span><span class="sxs-lookup"><span data-stu-id="d3aee-136">Set up a store</span></span>

<span data-ttu-id="d3aee-137">После завершения обязательных задач выполните следующие задачи, чтобы настроить сведения для магазина:</span><span class="sxs-lookup"><span data-stu-id="d3aee-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the store:</span></span>

1. <span data-ttu-id="d3aee-138">Создайте магазин.</span><span class="sxs-lookup"><span data-stu-id="d3aee-138">Create a store.</span></span>
2. <span data-ttu-id="d3aee-139">Назначьте налоговую группа для магазина.</span><span class="sxs-lookup"><span data-stu-id="d3aee-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="d3aee-140">Назначьте принятые способы оплаты для магазина.</span><span class="sxs-lookup"><span data-stu-id="d3aee-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="d3aee-141">Добавьте сведения в описания продуктов, которые предлагаются в магазинах.</span><span class="sxs-lookup"><span data-stu-id="d3aee-141">Add details to the product descriptions for products that you offer in your stores.</span></span> <span data-ttu-id="d3aee-142">Например, можно добавить форматированный текст и изображения.</span><span class="sxs-lookup"><span data-stu-id="d3aee-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="d3aee-143">Эти сведения о продуктах отображаются в различных контекстах, например в регистре POS или на распечатанных этикетках.</span><span class="sxs-lookup"><span data-stu-id="d3aee-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="d3aee-144">Добавление магазина в организационную иерархию по умолчанию, которая назначена цели **Розничный ассортимент**, **Пополнение запасов для розничной торговли** или **Отчетность по розничной торговле**.</span><span class="sxs-lookup"><span data-stu-id="d3aee-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-store"></a><span data-ttu-id="d3aee-145">После настройки магазина</span><span class="sxs-lookup"><span data-stu-id="d3aee-145">After you set up a store</span></span>

<span data-ttu-id="d3aee-146">После ввода сведений для магазина, выполните следующие задачи, чтобы отправлять новые данные магазина в POS.</span><span class="sxs-lookup"><span data-stu-id="d3aee-146">After you enter the details for the store, complete these tasks to send the new store data to POS:</span></span>

1. <span data-ttu-id="d3aee-147">Настройка регистров POS для магазина.</span><span class="sxs-lookup"><span data-stu-id="d3aee-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="d3aee-148">Назначение ассортиментов продуктов магазину.</span><span class="sxs-lookup"><span data-stu-id="d3aee-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="d3aee-149">Обработайте ассортименты, чтобы создать список продуктов, включенных в ассортимент, и чтобы сделать продукты доступными в магазине.</span><span class="sxs-lookup"><span data-stu-id="d3aee-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the store.</span></span>
4. <span data-ttu-id="d3aee-150">Отправка данных, таких как номерные серии, профили оборудования и макеты экрана POS в регистры POS.</span><span class="sxs-lookup"><span data-stu-id="d3aee-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the POS registers.</span></span>
5. <span data-ttu-id="d3aee-151">Опубликуйте магазин для отправки данных о магазине в POS.</span><span class="sxs-lookup"><span data-stu-id="d3aee-151">Publish the store to send store data to POS.</span></span>
6. <span data-ttu-id="d3aee-152">Запустите задания, чтобы отправить данные магазина в POS.</span><span class="sxs-lookup"><span data-stu-id="d3aee-152">Run the jobs to send the store data to POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="d3aee-153">Организационные иерархии</span><span class="sxs-lookup"><span data-stu-id="d3aee-153">Organization hierarchies</span></span>

<span data-ttu-id="d3aee-154">Commerce использует организационные для структурирования каналов.</span><span class="sxs-lookup"><span data-stu-id="d3aee-154">Commerce uses organization hierarchies to structure channels.</span></span> <span data-ttu-id="d3aee-155">Организационные иерархии представляют собой связи между организациями, которые занимаются коммерческой деятельностью.</span><span class="sxs-lookup"><span data-stu-id="d3aee-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="d3aee-156">При настройке магазинов их можно добавить в организационную иерархию.</span><span class="sxs-lookup"><span data-stu-id="d3aee-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="d3aee-157">После этого магазины могут совместно использовать данные по ассортименту, пополнению и отчетности.</span><span class="sxs-lookup"><span data-stu-id="d3aee-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="d3aee-158">Для использования функциональности продаж Commerce необходимо включить ключ конфигурации для **Несколько получателей**.</span><span class="sxs-lookup"><span data-stu-id="d3aee-158">To use Commerce sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="d3aee-159">Этот ключ конфигурации можно найти в ключах **Конфигурация торговли** в **Администрирование системы**\> **Настройка** \> **Конфигурация лицензии**.</span><span class="sxs-lookup"><span data-stu-id="d3aee-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="d3aee-160">Это необходимо из-за различных проверок на основе адреса поставки, настроенного на уровне строки заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="d3aee-160">This is required due to various validations based on the delivery address configured at the sales order line level.</span></span>

