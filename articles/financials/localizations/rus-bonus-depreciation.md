---
title: Амортизационные премии (Россия)
description: В этой теме содержится информация об амортизационной премии для основных средств в России.
author: anasyash
manager: AnnBe
ms.date: 10/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.search.industry: ''
ms.author: anasyash
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: dc423acc7e8fe6281ab9b6d0a021cc6e393c59d8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1538357"
---
# <a name="depreciation-bonuses-russia"></a><span data-ttu-id="73e0f-103">Амортизационные премии (Россия)</span><span class="sxs-lookup"><span data-stu-id="73e0f-103">Depreciation bonuses (Russia)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73e0f-104">Премия амортизации — это дополнительная сумма амортизации, определяемая в течении первого года для некоторых типов производственных основных средств.</span><span class="sxs-lookup"><span data-stu-id="73e0f-104">The depreciation bonus is an additional depreciation amount that is assessed during the first year for some asset types that are operational.</span></span>

<span data-ttu-id="73e0f-105">Можно рассчитать амортизационную премию, уменьшив стоимость актива способом, отличным от обычной ставки амортизации.</span><span class="sxs-lookup"><span data-stu-id="73e0f-105">You can calculate a depreciation bonus by reducing the value of an asset through means other than the usual rate of depreciation.</span></span> <span data-ttu-id="73e0f-106">Можно применять суммы амортизационной премии в течение учетного периода после ввода актива в эксплуатацию или после крупного ремонта.</span><span class="sxs-lookup"><span data-stu-id="73e0f-106">You can apply depreciation bonus amounts during the accounting period, after the asset is put into operation, or after major repairs.</span></span> <span data-ttu-id="73e0f-107">Амортизационные премии всегда рассчитываются и применяются до других видов амортизации.</span><span class="sxs-lookup"><span data-stu-id="73e0f-107">Depreciation bonuses are always calculated and applied before other types of depreciation.</span></span>

> [!NOTE]
> <span data-ttu-id="73e0f-108">Можно возместить амортизационную премию для основного средства только в том случае, если продать ОС аффилированному клиенту в течение 5 лет с момента ввода основного средства в эксплуатацию.</span><span class="sxs-lookup"><span data-stu-id="73e0f-108">You can restore the depreciation bonus for a fixed asset only if you sell the fixed asset to an affiliated customer within five years after you put the fixed asset into operation.</span></span> <span data-ttu-id="73e0f-109">Дополнительные сведения см. в разделе [Настройка аффилированного клиента](#set-up-an-affiliated-customer).</span><span class="sxs-lookup"><span data-stu-id="73e0f-109">For more information, see the [Set up an affiliated customer](#set-up-an-affiliated-customer) section.</span></span>

## <a name="set-up-a-depreciation-bonus"></a><span data-ttu-id="73e0f-110">Настройка амортизационной премии</span><span class="sxs-lookup"><span data-stu-id="73e0f-110">Set up a depreciation bonus</span></span>

1. <span data-ttu-id="73e0f-111">Выберите **Основные средства (Россия)** \> **Настройка** \> **Амортизационная премия**.</span><span class="sxs-lookup"><span data-stu-id="73e0f-111">Select **Fixed assets (Russia)** \> **Setup** \> **Depreciation bonus**.</span></span>
2. <span data-ttu-id="73e0f-112">Выберите **Создать**, чтобы создать скидку на амортизационную премию.</span><span class="sxs-lookup"><span data-stu-id="73e0f-112">Select **New** to create a depreciation bonus allowance.</span></span>
3. <span data-ttu-id="73e0f-113">В поле **Амортизационная премия** введите уникальный идентификатор для скидки на амортизационную премию.</span><span class="sxs-lookup"><span data-stu-id="73e0f-113">In the **Depreciation bonus** field, enter a unique identifier for the depreciation bonus allowance.</span></span> <span data-ttu-id="73e0f-114">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="73e0f-114">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="73e0f-115">В поле **Процент амортизационной премии** введите процент амортизационной премии.</span><span class="sxs-lookup"><span data-stu-id="73e0f-115">In the **Depreciation bonus percent** field, enter the percentage of the depreciation bonus.</span></span>

## <a name="calculate-a-depreciation-bonus"></a><span data-ttu-id="73e0f-116">Расчет амортизационной премии</span><span class="sxs-lookup"><span data-stu-id="73e0f-116">Calculate a depreciation bonus</span></span>

<span data-ttu-id="73e0f-117">Премия амортизации рассчитывается только для налоговой моделей стоимости.</span><span class="sxs-lookup"><span data-stu-id="73e0f-117">The depreciation bonus is calculated only for the tax value model.</span></span> <span data-ttu-id="73e0f-118">Необходимо настроить профиль разноски, чтобы рассчитать премию амортизации для основных средств.</span><span class="sxs-lookup"><span data-stu-id="73e0f-118">You must set up a posting profile before you can calculate the depreciation bonus for fixed assets.</span></span>

1. <span data-ttu-id="73e0f-119">Выберите **Основные средства (Россия)** \> **Периодический** \> **Инициализация амортизационной премии**.</span><span class="sxs-lookup"><span data-stu-id="73e0f-119">Select **Fixed assets (Russia)** \> **Periodic** \> **Depreciation bonus initialization**.</span></span>
2. <span data-ttu-id="73e0f-120">В поле **Модель учета** выберите модель премии амортизации.</span><span class="sxs-lookup"><span data-stu-id="73e0f-120">In the **Value model** field, select a model for the depreciation bonus.</span></span>
3. <span data-ttu-id="73e0f-121">В поле **Амортизационная премия** выберите идентификатор премии амортизации, созданный в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="73e0f-121">In the **Depreciation bonus** field, select the depreciation bonus ID that you created in the previous section.</span></span>
4. <span data-ttu-id="73e0f-122">На экспресс-вкладке **Включаемые записи** выберите **Фильтр**, чтобы открыть диалоговое окно **Запрос**.</span><span class="sxs-lookup"><span data-stu-id="73e0f-122">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box.</span></span> <span data-ttu-id="73e0f-123">Введите критерии, которые используются для выбора ОС или группы ОС, для которых необходимо создать проводку.</span><span class="sxs-lookup"><span data-stu-id="73e0f-123">Then enter criteria that are used to select the fixed asset or fixed asset group that the transaction should be created for.</span></span>
5. <span data-ttu-id="73e0f-124">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="73e0f-124">Select **OK**.</span></span> <span data-ttu-id="73e0f-125">Процент амортизационной премии обновляется в поле **Амортизационная премия** на странице **Проводки по ОС**.</span><span class="sxs-lookup"><span data-stu-id="73e0f-125">The depreciation bonus percentage is updated in the **Depreciation bonus** field on the **FA transactions** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="73e0f-126">При разноске проводки амортизации в журнале основных средств создаются две проводки (**Основные средства (Россия)** \> **Журналы** \> **Журнал ОС**).</span><span class="sxs-lookup"><span data-stu-id="73e0f-126">When you post a depreciation transaction, two transactions are created in the Fixed asset journal (**Fixed assets (Russia)** \> **Journals** \> **FA journal**).</span></span> <span data-ttu-id="73e0f-127">Одна проводка регистрирует амортизацию, а другая проводка регистрирует амортизационную премию.</span><span class="sxs-lookup"><span data-stu-id="73e0f-127">One transaction registers the depreciation, and the other transaction registers the depreciation bonus.</span></span>

## <a name="set-up-an-affiliated-customer"></a><span data-ttu-id="73e0f-128">Настройка аффилированного клиента</span><span class="sxs-lookup"><span data-stu-id="73e0f-128">Set up an affiliated customer</span></span>

<span data-ttu-id="73e0f-129">Используйте страницу **Все клиенты**, чтобы связать клиента с внутрихолдинговым объектом.</span><span class="sxs-lookup"><span data-stu-id="73e0f-129">Use the **All customers** page to affiliate a customer with an intercompany.</span></span> <span data-ttu-id="73e0f-130">Если основное средство продается аффилированному клиенту в течение 5 лет с момента ввода основного средства в эксплуатацию, можно возместить амортизационную премию для основного средства.</span><span class="sxs-lookup"><span data-stu-id="73e0f-130">If you sell a fixed asset to an affiliated customer within five years after you put the fixed asset into operation, you can restore the depreciation bonus for the fixed asset.</span></span>

1. <span data-ttu-id="73e0f-131">Выберите **Расчеты с клиентами** \> **Клиенты** \> **Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="73e0f-131">Select **Accounts receivable** \> **Customers** \> **All customers**.</span></span>

    <span data-ttu-id="73e0f-132">– или –</span><span class="sxs-lookup"><span data-stu-id="73e0f-132">–or–</span></span>

    <span data-ttu-id="73e0f-133">Выберите **Продажи и маркетинг** \> **Клиенты** \> **Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="73e0f-133">Select **Sales and marketing** \> **Customers** \> **All customers**.</span></span>

2. <span data-ttu-id="73e0f-134">На странице списка **Все клиенты** на панели действий выберите **Создать**, чтобы создать клиента или откройте существующую запись клиента.</span><span class="sxs-lookup"><span data-stu-id="73e0f-134">On the **All customers** list page, on the Action Pane, select **New** to create a customer, or open an existing customer record.</span></span>
3. <span data-ttu-id="73e0f-135">В записи клиента на экспресс-вкладке **Накладные и поставка** задайте для параметра **Аффилированный** значение **Да**, чтобы связать этого клиента с внутрихолдинговым объектом.</span><span class="sxs-lookup"><span data-stu-id="73e0f-135">In the customer record, on the **Invoice and delivery** FastTab, set the **Affiliated** option to **Yes** to affiliate the customer with an intercompany.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73e0f-136">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="73e0f-136">Additional resources</span></span>

- [<span data-ttu-id="73e0f-137">Настройка амортизации (Россия)</span><span class="sxs-lookup"><span data-stu-id="73e0f-137">Depreciation setup (Russia)</span></span>](rus-depreciation-setup.md)
- [<span data-ttu-id="73e0f-138">Методы амортизации (Россия)</span><span class="sxs-lookup"><span data-stu-id="73e0f-138">Depreciation methods (Russia)</span></span>](rus-depreciation-methods.md)
- [<span data-ttu-id="73e0f-139">Расчет амортизации (Россия)</span><span class="sxs-lookup"><span data-stu-id="73e0f-139">Depreciation calculation (Russia)</span></span>](rus-depreciation-calculation.md)
