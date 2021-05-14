---
title: Классы неполной загрузки (LTL)
description: В этой теме объясняется, что такое классы неполной нагрузки (LTL) и описывается порядок их настройки в Microsoft Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941818"
---
# <a name="less-than-truckload-ltl-classes"></a><span data-ttu-id="f9e64-103">Классы неполной загрузки (LTL)</span><span class="sxs-lookup"><span data-stu-id="f9e64-103">Less than truckload (LTL) classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9e64-104">Класс неполной нагрузки (ЛТЛ) — это класс отгрузки фрахта, который используется для классификации номенклатур, которые могут быть отгружены.</span><span class="sxs-lookup"><span data-stu-id="f9e64-104">A less than truckload (LTL) class is a freight shipping class that is used to classify items that can be shipped.</span></span> <span data-ttu-id="f9e64-105">Обычно в каждом типе продукта или товара имеется код Национальной классификации грузов, перевозимых автотранспортом (NMFC), соответствующий конкретному номеру класса фрахта для отгрузок LTL.</span><span class="sxs-lookup"><span data-stu-id="f9e64-105">Generally, every type of product or commodity has a National Motor Freight Classification (NMFC) code that corresponds to a specific freight class number for LTL shipments.</span></span> <span data-ttu-id="f9e64-106">Классы фрахта LTL представляют категории номенклатур, тогда как коды NMFC относятся к отдельным товарам в каждом из 18 классов фрахта.</span><span class="sxs-lookup"><span data-stu-id="f9e64-106">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span>

<span data-ttu-id="f9e64-107">Эта функция позволяют использовать систему для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="f9e64-107">This feature lets you use your system to perform the following tasks:</span></span>

- <span data-ttu-id="f9e64-108">Определение классов фрахта LTL, которые используются в вашей компании.</span><span class="sxs-lookup"><span data-stu-id="f9e64-108">Define the LTL freight classes that are used at your company.</span></span>
- <span data-ttu-id="f9e64-109">Назначьте каждый класс LTL коду NMFC на странице **Коды NMFC**.</span><span class="sxs-lookup"><span data-stu-id="f9e64-109">Assign each LTL class to an NMFC code on the **NMFC Codes** page.</span></span> <span data-ttu-id="f9e64-110">Дополнительные сведения см. в разделе [Коды Национальной классификации грузов, перевозимых автотранспортом (NMFC)](nmfc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f9e64-110">For more information, see [National Motor Freight Classification (NMFC) codes](nmfc-codes.md).</span></span>
- <span data-ttu-id="f9e64-111">Назначьте код NMFC (и, следовательно, связанный с кодом LTL) каждый продукт на странице **Продукты**.</span><span class="sxs-lookup"><span data-stu-id="f9e64-111">Assign an NMFC code (and therefore its associated LTL code) to each product on the **Products** page.</span></span>
- <span data-ttu-id="f9e64-112">Точная оценка класса LTL каждого продукта, которому назначен код NMFC.</span><span class="sxs-lookup"><span data-stu-id="f9e64-112">Accurately assess the LTL class of each product that an NMFC code is assigned to.</span></span>
- <span data-ttu-id="f9e64-113">Определите требования к упаковке для каждого класса LTL, проверив стандарты международного LTL.</span><span class="sxs-lookup"><span data-stu-id="f9e64-113">Determine packing requirements for each LTL class by checking the international LTL standards.</span></span> <span data-ttu-id="f9e64-114">Таким образом вы гарантируете, что ваша продукция будет надежно защищена и надежно отгружена.</span><span class="sxs-lookup"><span data-stu-id="f9e64-114">In this way, you ensure that your products will be well protected and safely shipped.</span></span>
- <span data-ttu-id="f9e64-115">Получите точную оценку отгрузки на основе класса фрахта LTL для каждого продукта.</span><span class="sxs-lookup"><span data-stu-id="f9e64-115">Get accurate shipping estimates, based on the LTL freight class for each product.</span></span>

<span data-ttu-id="f9e64-116">В этом разделе описывается, как создать классы LTL в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f9e64-116">This topic describes how to create LTL classes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="create-an-ltl-class"></a><span data-ttu-id="f9e64-117">Создание класса LTL</span><span class="sxs-lookup"><span data-stu-id="f9e64-117">Create an LTL class</span></span>

<span data-ttu-id="f9e64-118">Чтобы создать класс LTL, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f9e64-118">To create an LTL class, follow these steps.</span></span>

1. <span data-ttu-id="f9e64-119">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="f9e64-119">Follow one of these steps:</span></span>

    - <span data-ttu-id="f9e64-120">Перейдите в раздел **Управление складом \> Настройка \> Запасы \> Классы LTL**.</span><span class="sxs-lookup"><span data-stu-id="f9e64-120">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
    - <span data-ttu-id="f9e64-121">Перейдите в раздел **Управление транспортировкой \> Настройка \> Стандарты транспортировки \> Классы LTL**.</span><span class="sxs-lookup"><span data-stu-id="f9e64-121">Go to **Transportation management \> Setup \> Transportation standards \> LTL classes**.</span></span>

2. <span data-ttu-id="f9e64-122">На панели операций выберите **Создать** для создания класса LTL.</span><span class="sxs-lookup"><span data-stu-id="f9e64-122">On the Action Pane, select **New** to create an LTL class.</span></span> <span data-ttu-id="f9e64-123">Затем задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="f9e64-123">Then set the following fields:</span></span>

    - <span data-ttu-id="f9e64-124">**Класс LTL** — введите внутренний идентификатор класса LTL компании (ID) для данного типа товара.</span><span class="sxs-lookup"><span data-stu-id="f9e64-124">**LTL class** – Enter your company's internal LTL class identifier (ID) for the commodity type.</span></span> <span data-ttu-id="f9e64-125">В большинстве компаний используется международный стандарт.</span><span class="sxs-lookup"><span data-stu-id="f9e64-125">Most companies use the international standard.</span></span> <span data-ttu-id="f9e64-126">В этом случае значение этого поля будет соответствовать значению поля **Класс**.</span><span class="sxs-lookup"><span data-stu-id="f9e64-126">In that case, the value of this field will match the value of the **Class** field.</span></span> <span data-ttu-id="f9e64-127">Однако, если в компании используется собственный стандарт, введите код, соответствующий этому стандарту.</span><span class="sxs-lookup"><span data-stu-id="f9e64-127">However, if your company uses its own standard, enter a code that conforms to that standard.</span></span>
    - <span data-ttu-id="f9e64-128">**Имя** — введите описательное имя, которое поможет вам и другим пользователям выбрать правильный класс LTL для каждого кода NMFC.</span><span class="sxs-lookup"><span data-stu-id="f9e64-128">**Name** – Enter a descriptive name that will help you and other users select the correct LTL class for each NMFC code.</span></span>
    - <span data-ttu-id="f9e64-129">**Класс** — введите международный стандартный код класса LTL для типа товара.</span><span class="sxs-lookup"><span data-stu-id="f9e64-129">**Class** – Enter the international standard LTL class ID for the commodity type.</span></span> <span data-ttu-id="f9e64-130">Код, который вводится здесь, должен соответствовать официальному стандарту.</span><span class="sxs-lookup"><span data-stu-id="f9e64-130">The code that you enter here must conform to the official standard.</span></span>

## <a name="example-set-up-ltl-classes"></a><span data-ttu-id="f9e64-131">Пример: настройка классов LTL</span><span class="sxs-lookup"><span data-stu-id="f9e64-131">Example: Set up LTL classes</span></span>

<span data-ttu-id="f9e64-132">В следующем примере показано, как настроить два различных класса LTL, которые могут использоваться для различных типов продуктов.</span><span class="sxs-lookup"><span data-stu-id="f9e64-132">The following example shows how to set up two different LTL classes that you can use with different types of products.</span></span>

1. <span data-ttu-id="f9e64-133">Перейдите в раздел **Управление складом \> Настройка \> Запасы \> Классы LTL**.</span><span class="sxs-lookup"><span data-stu-id="f9e64-133">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
1. <span data-ttu-id="f9e64-134">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f9e64-134">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f9e64-135">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f9e64-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f9e64-136">**Класс LTL:** *92,5*</span><span class="sxs-lookup"><span data-stu-id="f9e64-136">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="f9e64-137">**Название:** *Компьютеры, мониторы, холодильники*</span><span class="sxs-lookup"><span data-stu-id="f9e64-137">**Name:** *Computers, monitors, refrigerators*</span></span>
    - <span data-ttu-id="f9e64-138">**Класс:** *92,5*</span><span class="sxs-lookup"><span data-stu-id="f9e64-138">**Class:** *92.5*</span></span>

1. <span data-ttu-id="f9e64-139">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f9e64-139">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="f9e64-140">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f9e64-140">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f9e64-141">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f9e64-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f9e64-142">**Класс LTL:** *125*</span><span class="sxs-lookup"><span data-stu-id="f9e64-142">**LTL class:** *125*</span></span>
    - <span data-ttu-id="f9e64-143">**Название:** *Малые бытовые приборы*</span><span class="sxs-lookup"><span data-stu-id="f9e64-143">**Name:** *Small household appliances*</span></span>
    - <span data-ttu-id="f9e64-144">**Класс:** *125*</span><span class="sxs-lookup"><span data-stu-id="f9e64-144">**Class:** *125*</span></span>

1. <span data-ttu-id="f9e64-145">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f9e64-145">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9e64-146">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f9e64-146">Additional resources</span></span>

- [<span data-ttu-id="f9e64-147">Коды Национальной классификации грузов, перевозимых автотранспортом (NMFC)</span><span class="sxs-lookup"><span data-stu-id="f9e64-147">National Motor Freight Classification (NMFC) codes</span></span>](nmfc-codes.md)
- [<span data-ttu-id="f9e64-148">Создание транспортной накладной</span><span class="sxs-lookup"><span data-stu-id="f9e64-148">Create a bill of lading</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
