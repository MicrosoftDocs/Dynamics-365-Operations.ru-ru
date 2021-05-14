---
title: Коды Национальной классификации грузов, перевозимых автотранспортом (NMFC)
description: В данном разделе описывается порядок работы с кодами Национальной классификации грузов, перевозимых автотранспортом (NMFC) в Microsoft Dynamics 365 Supply Chain Management
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0307437d3868f7ac34fa16a0913907a046ac14d4
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941890"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a><span data-ttu-id="972fc-103">Коды Национальной классификации грузов, перевозимых автотранспортом (NMFC)</span><span class="sxs-lookup"><span data-stu-id="972fc-103">National Motor Freight Classification (NMFC) codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="972fc-104">Коды Национальной классификации грузов, перевозимых автотранспортом (NMFC) позволяют классифицировать номенклатуры, которые могут быть отгружены.</span><span class="sxs-lookup"><span data-stu-id="972fc-104">National Motor Freight Classification (NMFC) codes help you classify items that can be shipped.</span></span> <span data-ttu-id="972fc-105">Код NMFC — это обозначение, используемое для группирования товаров.</span><span class="sxs-lookup"><span data-stu-id="972fc-105">The NMFC code is a designation that is used to group commodities.</span></span> <span data-ttu-id="972fc-106">Он позволяет компаниям-перевозчикам оценивать товары для отгрузки, классифицируя номенклатуры на основе таких соображений, как пригодность для автомобилей, проблемы с загрузкой, проблемы с обращением расходами и склонность к порче.</span><span class="sxs-lookup"><span data-stu-id="972fc-106">It enables transport companies to evaluate goods for shipment by classifying items based on considerations such as truck fit, loading issues, handling issues, and perishability.</span></span> <span data-ttu-id="972fc-107">Товары группируются в один из 18 классов фрахта, используя диапазон чисел от 50 до 500.</span><span class="sxs-lookup"><span data-stu-id="972fc-107">Commodities are grouped into one of 18 freight classes by using a range of numbers from 50 to 500.</span></span> <span data-ttu-id="972fc-108">Класс, в котором сгруппирован товар, основан на оценке четырех транспортных характеристик: плотность, пригодность для перевозки в контейнере, погрузочно-разгрузочные операции и обязательства.</span><span class="sxs-lookup"><span data-stu-id="972fc-108">The class that a commodity is grouped into is based on an evaluation of four transportation characteristics: density, stowability, handling, and liability.</span></span> <span data-ttu-id="972fc-109">Вместе эти характеристики определяют пригодность товара к транспортировке.</span><span class="sxs-lookup"><span data-stu-id="972fc-109">Together, these characteristics establish the commodity's transportability.</span></span>

<span data-ttu-id="972fc-110">Код NMFC связан с каждой номенклатурой отгрузки классы неполной нагрузки (LTL).</span><span class="sxs-lookup"><span data-stu-id="972fc-110">An NMFC code is associated with every less than truckload (LTL) shipping item.</span></span> <span data-ttu-id="972fc-111">Например, ноутбуку может быть назначен NMSC с классом 2,5, в то время как у электрических проводов может быть NMSC с классом 65.</span><span class="sxs-lookup"><span data-stu-id="972fc-111">For example, a laptop might be assigned an NMFC that is classed at 2.5, whereas electrical cords might be assigned an NMFC that is classed at 65.</span></span>

<span data-ttu-id="972fc-112">Эта функция может помочь работникам использовать коды NMFC для классификации номенклатур отгрузки LTL.</span><span class="sxs-lookup"><span data-stu-id="972fc-112">This feature can help workers use NMFC codes to classify LTL shipping items.</span></span> <span data-ttu-id="972fc-113">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="972fc-113">Here are some examples:</span></span>

- <span data-ttu-id="972fc-114">Если компания включает описание фрахта в транспортную накладную, перевозчик получит представление о фрахте.</span><span class="sxs-lookup"><span data-stu-id="972fc-114">If your company includes a freight description on the bill of lading (BOL), the carrier will have some idea what the freight is.</span></span> <span data-ttu-id="972fc-115">Фрахт является важной классификацией, поскольку многие транспортные компании основывают свои бизнес-модели по типам фрахта, которые они отгружают.</span><span class="sxs-lookup"><span data-stu-id="972fc-115">Freight is an important classification because many transportation companies base their whole business model on the types of freight that they ship.</span></span>
- <span data-ttu-id="972fc-116">Эта классификация может оказаться обязательной для вашей компании, поскольку она используется для определения затрат на данную загрузку.</span><span class="sxs-lookup"><span data-stu-id="972fc-116">This classification might be essential to your company because it's used to determine the cost of a given load.</span></span>
- <span data-ttu-id="972fc-117">Ваша компания может определить прибыльность логистики LTL и транспортной компании.</span><span class="sxs-lookup"><span data-stu-id="972fc-117">Your company can identify the profitability of an LTL logistics and transportation company.</span></span>

<span data-ttu-id="972fc-118">В этом разделе описывается, как работать с кодами NMFC в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="972fc-118">This topic describes how to work with NMFC codes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="972fc-119">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="972fc-119">Prerequisites</span></span>

<span data-ttu-id="972fc-120">Прежде чем можно будет создавать коды NMFC, необходимо настроить все классы фрахта LTL, которые должны быть сопоставлены с ними.</span><span class="sxs-lookup"><span data-stu-id="972fc-120">Before you can create NMFC codes, you must set up all the LTL freight classes that must be mapped to them.</span></span> <span data-ttu-id="972fc-121">Классы фрахта LTL представляют категории номенклатур, тогда как коды NMFC относятся к отдельным товарам в каждом из 18 классов фрахта.</span><span class="sxs-lookup"><span data-stu-id="972fc-121">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span> <span data-ttu-id="972fc-122">Дополнительные сведения о том, как работать с классами LTL, см. в разделе [Классы неполной загрузки (LTL)](ltl-class.md).</span><span class="sxs-lookup"><span data-stu-id="972fc-122">For more information about how to work with LTL classes, see [Less than truckload (LTL) classes](ltl-class.md).</span></span>

## <a name="create-an-nmfc-code"></a><span data-ttu-id="972fc-123">Создайте код NMFC</span><span class="sxs-lookup"><span data-stu-id="972fc-123">Create an NMFC code</span></span>

<span data-ttu-id="972fc-124">Чтобы создать код NMFC, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="972fc-124">To create an NMFC code, follow these steps.</span></span>

1. <span data-ttu-id="972fc-125">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="972fc-125">Follow one of these steps:</span></span>

    - <span data-ttu-id="972fc-126">Перейдите в раздел **Управление складом \> Настройка \> Запасы \> Коды NMFC**.</span><span class="sxs-lookup"><span data-stu-id="972fc-126">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
    - <span data-ttu-id="972fc-127">Перейдите в раздел **Управление транспортировкой \> Настройка \> Стандарты транспортировки \> Коды NMFC**.</span><span class="sxs-lookup"><span data-stu-id="972fc-127">Go to **Transportation management \> Setup \> Transportation standards \> NMFC codes**.</span></span>

1. <span data-ttu-id="972fc-128">Выберите **Создать**, чтобы создать код NMFC.</span><span class="sxs-lookup"><span data-stu-id="972fc-128">Select **New** to create an NMFC code.</span></span> <span data-ttu-id="972fc-129">Затем задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="972fc-129">Then set the following fields:</span></span>

    - <span data-ttu-id="972fc-130">**Код NMFC** — введите код NMFC для типа товара.</span><span class="sxs-lookup"><span data-stu-id="972fc-130">**NMFC code** – Enter the NMFC code for the commodity type.</span></span>
    - <span data-ttu-id="972fc-131">**Имя** — введите имя кода NMFC.</span><span class="sxs-lookup"><span data-stu-id="972fc-131">**Name** – Enter a name for the NMFC code.</span></span>
    - <span data-ttu-id="972fc-132">**Класс LTL** — выберите класс LTL, связанный с кодом NMFC.</span><span class="sxs-lookup"><span data-stu-id="972fc-132">**LTL class** – Select the LTL class that is associated with the NMFC code.</span></span>
    - <span data-ttu-id="972fc-133">**Единица обработки BOL** — определение типа обработки по умолчанию для отгрузки.</span><span class="sxs-lookup"><span data-stu-id="972fc-133">**BOL handling unit** – Define the default handling type for the shipment.</span></span>

## <a name="example-set-up-nmfc-codes"></a><span data-ttu-id="972fc-134">Пример: настройка кодов NMFC</span><span class="sxs-lookup"><span data-stu-id="972fc-134">Example: Set up NMFC codes</span></span>

<span data-ttu-id="972fc-135">В следующем примере показано, как настроить два различных кода NMFC, которые могут использоваться для различных продуктов.</span><span class="sxs-lookup"><span data-stu-id="972fc-135">The following example shows how to set up two different NMFC codes that can be used with different products.</span></span>

1. <span data-ttu-id="972fc-136">Перейдите в раздел **Управление складом \> Настройка \> Запасы \> Коды NMFC**.</span><span class="sxs-lookup"><span data-stu-id="972fc-136">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
1. <span data-ttu-id="972fc-137">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="972fc-137">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="972fc-138">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="972fc-138">On the new line, set the following values:</span></span>

    - <span data-ttu-id="972fc-139">**Код NMFC:** *92,5*</span><span class="sxs-lookup"><span data-stu-id="972fc-139">**NMFC code:** *92.5*</span></span>
    - <span data-ttu-id="972fc-140">**Название:** *Компьютеры*</span><span class="sxs-lookup"><span data-stu-id="972fc-140">**Name:** *Computers*</span></span>
    - <span data-ttu-id="972fc-141">**Класс LTL:** *92,5*</span><span class="sxs-lookup"><span data-stu-id="972fc-141">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="972fc-142">**Единица обработки BOL:** *Единица*</span><span class="sxs-lookup"><span data-stu-id="972fc-142">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="972fc-143">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="972fc-143">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="972fc-144">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="972fc-144">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="972fc-145">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="972fc-145">On the new line, set the following values:</span></span>

    - <span data-ttu-id="972fc-146">**Код NMFC:** *125*</span><span class="sxs-lookup"><span data-stu-id="972fc-146">**NMFC code:** *125*</span></span>
    - <span data-ttu-id="972fc-147">**Название:** *Телефоны*</span><span class="sxs-lookup"><span data-stu-id="972fc-147">**Name:** *Phones*</span></span>
    - <span data-ttu-id="972fc-148">**Класс LTL:** *125*</span><span class="sxs-lookup"><span data-stu-id="972fc-148">**LTL class:** *125*</span></span>
    - <span data-ttu-id="972fc-149">**Единица обработки BOL:** *Единица*</span><span class="sxs-lookup"><span data-stu-id="972fc-149">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="972fc-150">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="972fc-150">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="972fc-151">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="972fc-151">Additional resources</span></span>

- [<span data-ttu-id="972fc-152">Классы неполной загрузки (LTL)</span><span class="sxs-lookup"><span data-stu-id="972fc-152">Less than truckload (LTL) classes</span></span>](ltl-class.md)
- [<span data-ttu-id="972fc-153">Создание транспортной накладной</span><span class="sxs-lookup"><span data-stu-id="972fc-153">Create a bill of landing</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
