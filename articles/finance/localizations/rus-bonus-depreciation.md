---
title: Амортизационные премии (Россия)
description: В этой теме содержится информация об амортизационной премии для основных средств в России.
author: anasyash
manager: AnnBe
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.search.industry: ''
ms.author: anasyash
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 7bb2fcdcfba40c521f3ee53ce95ff5c5cd5f4dc3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228062"
---
# <a name="depreciation-bonuses-russia"></a><span data-ttu-id="d5eef-103">Амортизационные премии (Россия)</span><span class="sxs-lookup"><span data-stu-id="d5eef-103">Depreciation bonuses (Russia)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5eef-104">Премия амортизации — это дополнительная сумма амортизации, определяемая в течении первого года для некоторых типов производственных основных средств.</span><span class="sxs-lookup"><span data-stu-id="d5eef-104">The depreciation bonus is an additional depreciation amount that is assessed during the first year for some asset types that are operational.</span></span>

<span data-ttu-id="d5eef-105">Можно рассчитать амортизационную премию, уменьшив стоимость актива способом, отличным от обычной ставки амортизации.</span><span class="sxs-lookup"><span data-stu-id="d5eef-105">You can calculate a depreciation bonus by reducing the value of an asset through means other than the usual rate of depreciation.</span></span> <span data-ttu-id="d5eef-106">Можно применять суммы амортизационной премии в течение учетного периода после ввода актива в эксплуатацию или после крупного ремонта.</span><span class="sxs-lookup"><span data-stu-id="d5eef-106">You can apply depreciation bonus amounts during the accounting period, after the asset is put into operation, or after major repairs.</span></span> <span data-ttu-id="d5eef-107">Амортизационные премии всегда рассчитываются и применяются до других видов амортизации.</span><span class="sxs-lookup"><span data-stu-id="d5eef-107">Depreciation bonuses are always calculated and applied before other types of depreciation.</span></span>

> [!NOTE]
> <span data-ttu-id="d5eef-108">Можно возместить амортизационную премию для основного средства только в том случае, если продать ОС аффилированному клиенту в течение 5 лет с момента ввода основного средства в эксплуатацию.</span><span class="sxs-lookup"><span data-stu-id="d5eef-108">You can restore the depreciation bonus for a fixed asset only if you sell the fixed asset to an affiliated customer within five years after you put the fixed asset into operation.</span></span> <span data-ttu-id="d5eef-109">Дополнительные сведения см. в разделе [Настройка аффилированного клиента](#set-up-an-affiliated-customer).</span><span class="sxs-lookup"><span data-stu-id="d5eef-109">For more information, see the [Set up an affiliated customer](#set-up-an-affiliated-customer) section.</span></span>

## <a name="set-up-a-depreciation-bonus"></a><span data-ttu-id="d5eef-110">Настройка амортизационной премии</span><span class="sxs-lookup"><span data-stu-id="d5eef-110">Set up a depreciation bonus</span></span>

1. <span data-ttu-id="d5eef-111">Выберите **Основные средства (Россия)** \> **Настройка** \> **Амортизационная премия**.</span><span class="sxs-lookup"><span data-stu-id="d5eef-111">Select **Fixed assets (Russia)** \> **Setup** \> **Depreciation bonus**.</span></span>
2. <span data-ttu-id="d5eef-112">Выберите **Создать**, чтобы создать скидку на амортизационную премию.</span><span class="sxs-lookup"><span data-stu-id="d5eef-112">Select **New** to create a depreciation bonus allowance.</span></span>
3. <span data-ttu-id="d5eef-113">В поле **Амортизационная премия** введите уникальный идентификатор для скидки на амортизационную премию.</span><span class="sxs-lookup"><span data-stu-id="d5eef-113">In the **Depreciation bonus** field, enter a unique identifier for the depreciation bonus allowance.</span></span> <span data-ttu-id="d5eef-114">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="d5eef-114">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="d5eef-115">В поле **Процент амортизационной премии** введите процент амортизационной премии.</span><span class="sxs-lookup"><span data-stu-id="d5eef-115">In the **Depreciation bonus percent** field, enter the percentage of the depreciation bonus.</span></span>

> [!NOTE]
> <span data-ttu-id="d5eef-116">Амортизационные премии могут использоваться при создании строки журнала основных средств для типа проводки **Ввод в эксплуатацию**.</span><span class="sxs-lookup"><span data-stu-id="d5eef-116">Depreciation bonuses can be used when you create a Fixed asset journal line for the **Putting into operation** transaction type.</span></span> <span data-ttu-id="d5eef-117">Дополнительные сведения см. в [Приобретение ОС и их ввод в эксплуатацию](rus-fixed-asset-acquisition.md).</span><span class="sxs-lookup"><span data-stu-id="d5eef-117">For more information, see [Acquiring fixed assets and putting them into operation](rus-fixed-asset-acquisition.md).</span></span> <span data-ttu-id="d5eef-118">При разноске журнала основных средств система заполняет поле **амортизационная премия** в проводке по основным средствам для типа проводки **ввода в эксплуатацию**.</span><span class="sxs-lookup"><span data-stu-id="d5eef-118">When you post the Fixed asset journal, the system fills in the **Depreciation bonus** field in the fixed asset transaction of the **Putting into operation** transaction type.</span></span> <span data-ttu-id="d5eef-119">Эти сведения используются при расчете амортизации.</span><span class="sxs-lookup"><span data-stu-id="d5eef-119">This information is then used when depreciation is calculated.</span></span> 

## <a name="calculate-a-depreciation-bonus"></a><span data-ttu-id="d5eef-120">Расчет амортизационной премии</span><span class="sxs-lookup"><span data-stu-id="d5eef-120">Calculate a depreciation bonus</span></span>

<span data-ttu-id="d5eef-121">Премия амортизации рассчитывается только для налоговой моделей стоимости.</span><span class="sxs-lookup"><span data-stu-id="d5eef-121">The depreciation bonus is calculated only for the tax value model.</span></span> <span data-ttu-id="d5eef-122">Необходимо настроить профиль разноски, чтобы рассчитать премию амортизации для основных средств.</span><span class="sxs-lookup"><span data-stu-id="d5eef-122">You must set up a posting profile before you can calculate the depreciation bonus for fixed assets.</span></span> <span data-ttu-id="d5eef-123">Используйте следующую процедуру для заполнения полей амортизационной премии для всех проводок с основными средствами типа проводки **Ввод в эксплуатацию** в одно и то же время, используя настроенный фильтр.</span><span class="sxs-lookup"><span data-stu-id="d5eef-123">Use the following procedure to fill in the depreciation bonus fields for all fixed asset transactions of the **Putting into operation** transaction type at the same time by using a filter that you set.</span></span> 

1. <span data-ttu-id="d5eef-124">Выберите **Основные средства (Россия)** \> **Периодический** \> **Инициализация амортизационной премии**.</span><span class="sxs-lookup"><span data-stu-id="d5eef-124">Select **Fixed assets (Russia)** \> **Periodic** \> **Depreciation bonus initialization**.</span></span>
2. <span data-ttu-id="d5eef-125">В поле **Модель учета** выберите модель премии амортизации.</span><span class="sxs-lookup"><span data-stu-id="d5eef-125">In the **Value model** field, select a model for the depreciation bonus.</span></span>
3. <span data-ttu-id="d5eef-126">В поле **Амортизационная премия** выберите идентификатор премии амортизации, созданный в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="d5eef-126">In the **Depreciation bonus** field, select the depreciation bonus ID that you created in the previous section.</span></span>
4. <span data-ttu-id="d5eef-127">На экспресс-вкладке **Включаемые записи** выберите **Фильтр**, чтобы открыть диалоговое окно **Запрос**.</span><span class="sxs-lookup"><span data-stu-id="d5eef-127">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box.</span></span> <span data-ttu-id="d5eef-128">Введите критерии, которые используются для выбора ОС или группы ОС, для которых необходимо создать проводку.</span><span class="sxs-lookup"><span data-stu-id="d5eef-128">Then enter criteria that are used to select the fixed asset or fixed asset group that the transaction should be created for.</span></span>
5. <span data-ttu-id="d5eef-129">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d5eef-129">Select **OK**.</span></span> <span data-ttu-id="d5eef-130">Процент амортизационной премии обновляется в поле **Амортизационная премия** на странице **Проводки по ОС**.</span><span class="sxs-lookup"><span data-stu-id="d5eef-130">The depreciation bonus percentage is updated in the **Depreciation bonus** field on the **FA transactions** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d5eef-131">При разноске проводки амортизации в журнале основных средств создаются две проводки (**Основные средства (Россия)** \> **Журналы** \> **Журнал ОС**).</span><span class="sxs-lookup"><span data-stu-id="d5eef-131">When you post a depreciation transaction, two transactions are created in the Fixed asset journal (**Fixed assets (Russia)** \> **Journals** \> **FA journal**).</span></span> <span data-ttu-id="d5eef-132">Одна проводка регистрирует амортизацию, а другая проводка регистрирует амортизационную премию.</span><span class="sxs-lookup"><span data-stu-id="d5eef-132">One transaction registers the depreciation, and the other transaction registers the depreciation bonus.</span></span>

## <a name="set-up-an-affiliated-customer"></a><span data-ttu-id="d5eef-133">Настройка аффилированного клиента</span><span class="sxs-lookup"><span data-stu-id="d5eef-133">Set up an affiliated customer</span></span>

<span data-ttu-id="d5eef-134">Используйте страницу **Все клиенты**, чтобы связать клиента с внутрихолдинговым объектом.</span><span class="sxs-lookup"><span data-stu-id="d5eef-134">Use the **All customers** page to affiliate a customer with an intercompany.</span></span> <span data-ttu-id="d5eef-135">Если основное средство продается аффилированному клиенту в течение 5 лет с момента ввода основного средства в эксплуатацию, можно возместить амортизационную премию для основного средства.</span><span class="sxs-lookup"><span data-stu-id="d5eef-135">If you sell a fixed asset to an affiliated customer within five years after you put the fixed asset into operation, you can restore the depreciation bonus for the fixed asset.</span></span>

1. <span data-ttu-id="d5eef-136">Выберите **Расчеты с клиентами** \> **Клиенты** \> **Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="d5eef-136">Select **Accounts receivable** \> **Customers** \> **All customers**.</span></span>

    <span data-ttu-id="d5eef-137">– или –</span><span class="sxs-lookup"><span data-stu-id="d5eef-137">–or–</span></span>

    <span data-ttu-id="d5eef-138">Выберите **Продажи и маркетинг** \> **Клиенты** \> **Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="d5eef-138">Select **Sales and marketing** \> **Customers** \> **All customers**.</span></span>

2. <span data-ttu-id="d5eef-139">На странице списка **Все клиенты** на панели действий выберите **Создать**, чтобы создать клиента или откройте существующую запись клиента.</span><span class="sxs-lookup"><span data-stu-id="d5eef-139">On the **All customers** list page, on the Action Pane, select **New** to create a customer, or open an existing customer record.</span></span>
3. <span data-ttu-id="d5eef-140">В записи клиента на экспресс-вкладке **Накладные и поставка** задайте для параметра **Аффилированный** значение **Да**, чтобы связать этого клиента с внутрихолдинговым объектом.</span><span class="sxs-lookup"><span data-stu-id="d5eef-140">In the customer record, on the **Invoice and delivery** FastTab, set the **Affiliated** option to **Yes** to affiliate the customer with an intercompany.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d5eef-141">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d5eef-141">Additional resources</span></span>

- [<span data-ttu-id="d5eef-142">Настройка амортизации (Россия)</span><span class="sxs-lookup"><span data-stu-id="d5eef-142">Set up depreciation (Russia)</span></span>](rus-depreciation-setup.md)
- [<span data-ttu-id="d5eef-143">Методы амортизации (Россия)</span><span class="sxs-lookup"><span data-stu-id="d5eef-143">Depreciation methods (Russia)</span></span>](rus-depreciation-methods.md)
- [<span data-ttu-id="d5eef-144">Расчет амортизации для России</span><span class="sxs-lookup"><span data-stu-id="d5eef-144">Calculate depreciation for Russia</span></span>](rus-depreciation-calculation.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]