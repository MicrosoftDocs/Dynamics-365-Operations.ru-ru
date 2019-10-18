---
title: Частичная разборка (ликвидация) ОС
description: В этом разделе содержатся сведения о частичной разборке или ликвидации основных средств для России.
author: v-oloski
manager: AnnBe
ms.date: 09/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RAssetPosting
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Russia
ms.author: v-oloski
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 267d6f2d8958161c51c0bc637a05379980f54954
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552342"
---
# <a name="partial-fixed-asset-disassembly-liquidation"></a><span data-ttu-id="a43c6-103">Частичная разборка ОС (ликвидация)</span><span class="sxs-lookup"><span data-stu-id="a43c6-103">Partial fixed asset disassembly (liquidation)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a43c6-104">Частичная разборка (ликвидация) объектов основных средств может привести к изменению первоначальной стоимости основного средства, согласно законодательству Российской Федерации (ПБУ 6/01).</span><span class="sxs-lookup"><span data-stu-id="a43c6-104">Partial disassembly (liquidation) of fixed asset objects can cause the original value of the asset to change, in accordance with Russian Federation law (PBU 6/01).</span></span> <span data-ttu-id="a43c6-105">Снимаемые при разборке комплектующие могут учитываться как запасные части.</span><span class="sxs-lookup"><span data-stu-id="a43c6-105">The components that are removed for disassembly can be accounted for as spare parts.</span></span> <span data-ttu-id="a43c6-106">Запасы, оставшиеся после выбытия основного средства, разносятся по своей фактической себестоимости.</span><span class="sxs-lookup"><span data-stu-id="a43c6-106">The inventory that remains after the disposal of an asset is posted at its actual cost price.</span></span> <span data-ttu-id="a43c6-107">Эта себестоимость основывается на текущей рыночной стоимости запасов на дату разноски в учете.</span><span class="sxs-lookup"><span data-stu-id="a43c6-107">This price is based on the current market value of the inventory on the date of posting to accounting.</span></span>

## <a name="configure-transaction-profiles"></a><span data-ttu-id="a43c6-108">Настройка профилей проводок</span><span class="sxs-lookup"><span data-stu-id="a43c6-108">Configure transaction profiles</span></span>

<span data-ttu-id="a43c6-109">Для создания проводок частичной разборки основных средств необходимо настроить профили проводок.</span><span class="sxs-lookup"><span data-stu-id="a43c6-109">To create the partial fixed asset disassembly transactions, you must configure the transaction profiles.</span></span>

1. <span data-ttu-id="a43c6-110">Выберите **Основные средства (Россия) \> Настройка \> Профили разноски**.</span><span class="sxs-lookup"><span data-stu-id="a43c6-110">Select **Fixed assets (Russia) \> Setup \> Posting profiles**.</span></span>
2. <span data-ttu-id="a43c6-111">В области действий выберите **Параметры \> Частичная разборка**.</span><span class="sxs-lookup"><span data-stu-id="a43c6-111">On the Action Pane, select **Options \> Partial dismantlement**.</span></span>
3. <span data-ttu-id="a43c6-112">На странице **Частичная разборка** настройте счета для списания балансовой стоимости, амортизации остатка, остаточной стоимости и прибыли/убытка.</span><span class="sxs-lookup"><span data-stu-id="a43c6-112">On the **Partial dismantlement** page, set up the accounts for writing off the balance value, balance depreciation, net book value, and profit/loss.</span></span>

## <a name="create-a-partial-fixed-asset-disassembly-transaction"></a><span data-ttu-id="a43c6-113">Создание проводки частичной разборки основного средства</span><span class="sxs-lookup"><span data-stu-id="a43c6-113">Create a partial fixed asset disassembly transaction</span></span>

1. <span data-ttu-id="a43c6-114">Выберите **Основные средства (Россия) \> Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="a43c6-114">Select **Fixed assets (Russia) \> Fixed assets**.</span></span>
2. <span data-ttu-id="a43c6-115">Выберите основное средство, а затем в области действий на вкладке **Основное средство** выберите **Комплектующие**.</span><span class="sxs-lookup"><span data-stu-id="a43c6-115">Select the fixed asset, and then, on the Action Pane, on the **Fixed asset** tab, select **Componentry**.</span></span>

    <span data-ttu-id="a43c6-116">В верхней области страницы **Комплектующие** отображаются следующие сведения для выбранной номенклатуры:</span><span class="sxs-lookup"><span data-stu-id="a43c6-116">The upper pane of the **Componentry** page shows the following information for the item that you selected:</span></span>

    - <span data-ttu-id="a43c6-117">**Дата проводки** — дата сборки основного средства.</span><span class="sxs-lookup"><span data-stu-id="a43c6-117">**Date of transaction** – The date of fixed asset assembly.</span></span>
    - <span data-ttu-id="a43c6-118">**Первоначальное количество** — количество, которое было введено во время сборки.</span><span class="sxs-lookup"><span data-stu-id="a43c6-118">**Initial quantity** – The quantity that was entered during assembly.</span></span>
    - <span data-ttu-id="a43c6-119">**Текущее количество** — количество, которое в настоящее время введено для основного средства.</span><span class="sxs-lookup"><span data-stu-id="a43c6-119">**Current quantity** – The quantity that is currently entered for the fixed asset.</span></span>
    - <span data-ttu-id="a43c6-120">**Стоимость** — стоимость комплектующей.</span><span class="sxs-lookup"><span data-stu-id="a43c6-120">**Cost** – The component cost.</span></span>

3. <span data-ttu-id="a43c6-121">Выберите строку для номенклатуры, а затем выберите **Добавить в остатки**.</span><span class="sxs-lookup"><span data-stu-id="a43c6-121">Select the line for an item, and then select **Add to remains**.</span></span>
4. <span data-ttu-id="a43c6-122">В диалоговом окне **Добавить в остатки** в поле **Добавить** введите оставшееся количество.</span><span class="sxs-lookup"><span data-stu-id="a43c6-122">in the **Add to remains** dialog box, in the **Add** field, enter the remaining quantity.</span></span>

    <span data-ttu-id="a43c6-123">В поле **Доступное количество** отображается количество этой номенклатуры, которое в настоящее время присутствует в основном средстве.</span><span class="sxs-lookup"><span data-stu-id="a43c6-123">The **Available quantity** field shows the quantity of this item that is currently part of the fixed asset.</span></span>

5. <span data-ttu-id="a43c6-124">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a43c6-124">Select **OK**.</span></span>

    <span data-ttu-id="a43c6-125">Строки, помеченные в верхней области страницы **Комплектующие**, страницы переносятся в нижнюю область для частичной разборки, которая будет разнесена в запасы.</span><span class="sxs-lookup"><span data-stu-id="a43c6-125">The lines that are marked in the upper pane of the **Componentry** page are transferred to the lower pane for a partial disassembly that will be posted to inventory.</span></span> <span data-ttu-id="a43c6-126">В нижней области отображается список комплектующих для частичной разборки.</span><span class="sxs-lookup"><span data-stu-id="a43c6-126">The lower pane shows a component list for the partial disassembly.</span></span> <span data-ttu-id="a43c6-127">В верхней области в поле **Текущее количество** отображается количество комплектующей.</span><span class="sxs-lookup"><span data-stu-id="a43c6-127">In the upper pane, the **Current quantity** field shows the component quantity.</span></span> <span data-ttu-id="a43c6-128">Это количество остается в основном средстве после частичной разборки, и значение в поле **Текущее количество** обновляется.</span><span class="sxs-lookup"><span data-stu-id="a43c6-128">This quantity remains in the fixed asset after the partial disassembly, and the value of the **Current quantity** field is updated.</span></span>

6. <span data-ttu-id="a43c6-129">В нижней области выберите **Расчет цен**.</span><span class="sxs-lookup"><span data-stu-id="a43c6-129">In the lower pane, select **Calculating prices**.</span></span> <span data-ttu-id="a43c6-130">Для каждой списываемой комплектующей рассчитываются амортизация балансовой стоимости и остаточная стоимость.</span><span class="sxs-lookup"><span data-stu-id="a43c6-130">The balance value depreciation and depreciated cost are calculated for every component that is being written off.</span></span>
7. <span data-ttu-id="a43c6-131">В диалоговом окне **Расчет цен** в поле **Расчет цен** выберите метод, используемый для расчета цен:</span><span class="sxs-lookup"><span data-stu-id="a43c6-131">In the **Calculating prices** dialog box, in the **Calculating prices** field, select the method that is used to calculate prices:</span></span>

    - <span data-ttu-id="a43c6-132">**Пропорциональный** — проводка переоценки основного средства включает все комплектующие соразмерно их первоначальной стоимости.</span><span class="sxs-lookup"><span data-stu-id="a43c6-132">**Proportionate** – The fixed asset revaluation transaction includes all components in proportion to their original value.</span></span> <span data-ttu-id="a43c6-133">Дата приобретения комплектующей не учитывается.</span><span class="sxs-lookup"><span data-stu-id="a43c6-133">The acquisition date of the component isn't considered.</span></span> <span data-ttu-id="a43c6-134">Дата приобретения комплектующей не учитывается.</span><span class="sxs-lookup"><span data-stu-id="a43c6-134">The acquisition date of the component isn't considered.</span></span>
    - <span data-ttu-id="a43c6-135">**Итерационный** — проводка переоценки основного средства включает не все комплектующие соразмерно их первоначальной стоимости, а только соразмерно стоимости комплектующих, входящих в основное средство на момент проводки переоценки.</span><span class="sxs-lookup"><span data-stu-id="a43c6-135">**Iterative** – The fixed asset revaluation transaction doesn't include all components in proportion to their original value, but only in proportion to the value of the components that are included at the time of the revaluation transaction.</span></span>

8. <span data-ttu-id="a43c6-136">Если стоимость необходимо округлить до целого значения, установите для параметра **Округлять рыночную стоимость** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="a43c6-136">If the cost must be rounded to an integer value, set the **Round off market value** option to **Yes**.</span></span>
9. <span data-ttu-id="a43c6-137">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a43c6-137">Select **OK**.</span></span> <span data-ttu-id="a43c6-138">Стоимость номенклатуры рассчитывается при возврате номенклатуры в запасы. Рыночную стоимость можно вручную обновить требуемым образом.</span><span class="sxs-lookup"><span data-stu-id="a43c6-138">The cost of the item is calculated, when the item return to inventory  You can manually update the market value as you require.</span></span>

    <span data-ttu-id="a43c6-139">Комплектующие разносятся в запасы либо по их рассчитанной стоимости, либо по рыночной стоимости.</span><span class="sxs-lookup"><span data-stu-id="a43c6-139">Components are posted to the inventory with respect to either their calculated value or their market value.</span></span> <span data-ttu-id="a43c6-140">То, какая стоимость используется, определяется комиссией при разборке основного средства.</span><span class="sxs-lookup"><span data-stu-id="a43c6-140">The value that is used is determined by the commission during fixed asset disassembly.</span></span> <span data-ttu-id="a43c6-141">Разница между рыночной стоимостью и рассчитанной стоимостью — это сумма прибыли или убытка в результате разборки основных средств.</span><span class="sxs-lookup"><span data-stu-id="a43c6-141">The difference between the market value and the calculated value is the profit or loss amount in the result of the fixed asset disassembly.</span></span>

10. <span data-ttu-id="a43c6-142">В нижней области страницы **Комплектующие** на вкладке **Складские аналитики** выберите складские аналитики, которые используются для разноски номенклатуры в запасы.</span><span class="sxs-lookup"><span data-stu-id="a43c6-142">In the lower pane of the **Componentry** page, on the **Inventory dimensions** tab, select inventory dimensions that are used to post the item to inventory.</span></span>
11. <span data-ttu-id="a43c6-143">Чтобы создать проводку списания при разборке, выберите **Основные средства (Россия) \> Журналы \> Журнал ОС**.</span><span class="sxs-lookup"><span data-stu-id="a43c6-143">To create the write-off disassembly transaction, select **Fixed assets (Russia) \> Journals \> FA journal**.</span></span>
12. <span data-ttu-id="a43c6-144">Выберите **Создать**, чтобы создать журнал.</span><span class="sxs-lookup"><span data-stu-id="a43c6-144">Select **New** to create a journal.</span></span>
13. <span data-ttu-id="a43c6-145">Выберите **Строки** и затем создать **Создать**, чтобы создать строки для записи проводок списания при разборке.</span><span class="sxs-lookup"><span data-stu-id="a43c6-145">Select **Lines** and then **New** to create lines to record the write-off disassembly transactions.</span></span>
14. <span data-ttu-id="a43c6-146">В диалоговом окне **Добавление в журнал** в поле **Тип проводки** выберите **Частичная разборка**.</span><span class="sxs-lookup"><span data-stu-id="a43c6-146">In the **Add to journal** dialog box, in the **Transaction type** field, select **Partial dismantlement**.</span></span>
15. <span data-ttu-id="a43c6-147">Введите дату проводки в поле **Дата проводки**.</span><span class="sxs-lookup"><span data-stu-id="a43c6-147">In the **Transaction date** field, enter the transaction date.</span></span>
16. <span data-ttu-id="a43c6-148">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a43c6-148">Select **OK**.</span></span> <span data-ttu-id="a43c6-149">В журнале создаются строки частичной разборки основного средства в соответствии с настройками профиля амортизации.</span><span class="sxs-lookup"><span data-stu-id="a43c6-149">The partial fixed asset disassembly lines are created in the journal, according to the depreciation profile settings.</span></span>

    <span data-ttu-id="a43c6-150">Если в строке журнала нет сведений проводки, их необходимо ввести вручную.</span><span class="sxs-lookup"><span data-stu-id="a43c6-150">If there no transaction details on the journal line, you must enter them manually.</span></span>

17. <span data-ttu-id="a43c6-151">В области действий выберите **Функции \> Показать невидимые**, чтобы отобразить строки прибыли/убытка.</span><span class="sxs-lookup"><span data-stu-id="a43c6-151">On the Action Pane, select **Functions \> Show invisible** to show profit/loss lines.</span></span>
18. <span data-ttu-id="a43c6-152">В области действий выберите **Разнести \> Разнести**.</span><span class="sxs-lookup"><span data-stu-id="a43c6-152">On the Action Pane, select **Post \> Post**.</span></span> <span data-ttu-id="a43c6-153">Проводки создаются в главной книге и на счетах основных средств, и номенклатура разносится в запасы.</span><span class="sxs-lookup"><span data-stu-id="a43c6-153">Transactions are created in the ledger and fixed asset accounts, and the item is posted to inventory.</span></span>

    <span data-ttu-id="a43c6-154">Сумма проводки частичной разборки отображается в полях **Переоценка стоимости ввода в эксплуатацию для частичного демонтажа** и **Переоценка амортизации для частичного демонтажа** в диалоговом окне **Баланс по ОС** (**Основные средства (Россия) \> Модели стоимости \> Баланс**).</span><span class="sxs-lookup"><span data-stu-id="a43c6-154">The partial dismantlement transaction value is shown in the **Acquisition adjustment of partial dismantlement** and **Depreciation adjustment of partial dismantlement** fields in the **Balance by FA** dialog box (**Fixed assets (Russia) \> Value models \> Balance**).</span></span>

    <span data-ttu-id="a43c6-155">Если частичная разборка основного средства влечет за собой убыток, на странице **Расходы будущих периодов** (**Главная книга \> РБП \> Расходы будущих периодов**) создается строка, если для налоговой модели учета настроена соответствующая группа амортизации.</span><span class="sxs-lookup"><span data-stu-id="a43c6-155">If a partial fixed asset disassembly involves a loss, a line on the **Deferrals** page (**General ledger \> Deferrals \> Deferrals**) is created if the corresponding depreciation group has been set up for the tax value mode.</span></span>

> [!NOTE]
> <span data-ttu-id="a43c6-156">Можно вручную добавить номенклатуру в нижней области страницы **Комплектующие**, даже если эта номенклатура не входит в основное средство.</span><span class="sxs-lookup"><span data-stu-id="a43c6-156">You can manually add an item in the lower pane of the **Componentry** page, even if that item isn't included in the fixed asset.</span></span> <span data-ttu-id="a43c6-157">Основное средство может быть введено в эксплуатацию без комплектующих, но может быть разобрано на различные номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="a43c6-157">A fixed asset can be put into operation without componentry, but it can be dismantled to different items.</span></span>

## <a name="calculating-prices"></a><span data-ttu-id="a43c6-158">Расчет цен</span><span class="sxs-lookup"><span data-stu-id="a43c6-158">Calculating prices</span></span>

<span data-ttu-id="a43c6-159">В этом разделе содержатся примеры и математические формулы.</span><span class="sxs-lookup"><span data-stu-id="a43c6-159">This section contains examples and mathematical equations (formulas).</span></span> <span data-ttu-id="a43c6-160">Для расчета цены актива используется два метода.</span><span class="sxs-lookup"><span data-stu-id="a43c6-160">Two methods are used to calculate the price of an asset.</span></span> <span data-ttu-id="a43c6-161">По умолчанию в качестве стоимости принимается остаточная стоимость комплектующей.</span><span class="sxs-lookup"><span data-stu-id="a43c6-161">By default, the depreciated cost of a component is adopted as the cost value.</span></span>

### <a name="the-proportional-method"></a><span data-ttu-id="a43c6-162">Пропорциональный метод</span><span class="sxs-lookup"><span data-stu-id="a43c6-162">The proportional method</span></span>


<span data-ttu-id="a43c6-163">Проводка переоценки основного средства включает все комплектующие соразмерно их первоначальной стоимости.</span><span class="sxs-lookup"><span data-stu-id="a43c6-163">The fixed asset revaluation transaction includes all components in proportion to their original value.</span></span> <span data-ttu-id="a43c6-164">Дата приобретения комплектующей не учитывается.</span><span class="sxs-lookup"><span data-stu-id="a43c6-164">The acquisition date of the component isn't considered.</span></span> <span data-ttu-id="a43c6-165">Дата приобретения комплектующей не учитывается.</span><span class="sxs-lookup"><span data-stu-id="a43c6-165">The acquisition date of the component isn't considered.</span></span>

<span data-ttu-id="a43c6-166">Для каждой комплектующей, изымаемой из состава основного средства, баланс комплектующей (S<sub>j</sub>) рассчитывается по следующей формуле:</span><span class="sxs-lookup"><span data-stu-id="a43c6-166">For every component that is withdrawn from the fixed asset composition, the balance of the component (S<sub>j</sub>) is calculated by using the following formula:</span></span>

<span data-ttu-id="a43c6-167">S<sub>j</sub> = S<sub>bal</sub> × (S<sub>j,PIO</sub> ÷ S<sub>PIO</sub>)</span><span class="sxs-lookup"><span data-stu-id="a43c6-167">S<sub>j</sub> = S<sub>bal</sub> × (S<sub>j,PIO</sub> ÷ S<sub>PIO</sub>)</span></span>

<span data-ttu-id="a43c6-168">В этой формуле:</span><span class="sxs-lookup"><span data-stu-id="a43c6-168">Here is an explanation of this formula:</span></span>

- <span data-ttu-id="a43c6-169">**S<sub>bal</sub>** — балансовая стоимость основного средства.</span><span class="sxs-lookup"><span data-stu-id="a43c6-169">**S<sub>bal</sub>** – The fixed asset balance value.</span></span> <span data-ttu-id="a43c6-170">Это значение рассчитывается как сумма проводок приобретения, проводок переоценки, проводок крупного ремонта и проводок частичной разборки.</span><span class="sxs-lookup"><span data-stu-id="a43c6-170">This value is calculated as the sum of acquisition transactions, revaluation transactions, major refurbishment transactions, and partial take-down transactions.</span></span> <span data-ttu-id="a43c6-171">Проводки частичной разборки имеют отрицательный знак и автоматически вычитаются из итога.</span><span class="sxs-lookup"><span data-stu-id="a43c6-171">Partial take-down transactions have a negative sign and are automatically deducted from the total.</span></span>
- <span data-ttu-id="a43c6-172">**S<sub>j, PIO</sub>** — первоначальная стоимость изымаемых комплектующих.</span><span class="sxs-lookup"><span data-stu-id="a43c6-172">**S<sub>j,PIO</sub>** – The original value of withdrawn components.</span></span>
- <span data-ttu-id="a43c6-173">**S<sub>PIO</sub>** — первоначальная стоимость основного средства.</span><span class="sxs-lookup"><span data-stu-id="a43c6-173">**S<sub>PIO</sub>** – The original fixed asset cost.</span></span>

<span data-ttu-id="a43c6-174">Накопленная амортизация для комплектующих (A<sub>j</sub>) рассчитываются так же, как и первоначальная стоимость, если выполняется следующее условие:</span><span class="sxs-lookup"><span data-stu-id="a43c6-174">The accumulated depreciation for components (A<sub>j</sub>) is calculated in the same way as the original value where the following condition is true:</span></span>

<span data-ttu-id="a43c6-175">A<sub>j</sub> = A<sub>bal</sub> × (S<sub>j,PIO</sub> ÷ S<sub>PIO</sub>)</span><span class="sxs-lookup"><span data-stu-id="a43c6-175">A<sub>j</sub> = A<sub>bal</sub> × (S<sub>j,PIO</sub> ÷ S<sub>PIO</sub>)</span></span>

<span data-ttu-id="a43c6-176">В этой формуле:</span><span class="sxs-lookup"><span data-stu-id="a43c6-176">Here is an explanation of this formula:</span></span>

- <span data-ttu-id="a43c6-177">**A<sub>bal</sub>** — амортизация стоимости основного средства.</span><span class="sxs-lookup"><span data-stu-id="a43c6-177">**A<sub>bal</sub>** – The fixed asset value depreciation.</span></span> <span data-ttu-id="a43c6-178">Это значение рассчитывается как сумма всех проводок, которые используются для расчета амортизации основного средства, проводок переоценки амортизации основного средства и проводок частичной разборки.</span><span class="sxs-lookup"><span data-stu-id="a43c6-178">This value is calculated as the sum of all transactions that are used to calculate fixed asset depreciation, fixed asset depreciation revaluation transactions, and partial dismantlement transactions.</span></span> <span data-ttu-id="a43c6-179">Расчетное значение округляется в соответствии с конфигурацией модуля "Основные средства".</span><span class="sxs-lookup"><span data-stu-id="a43c6-179">The calculated value is rounded according to the configuration of Fixed assets.</span></span>

<span data-ttu-id="a43c6-180">Остаточная стоимость комплектующих рассчитывается как разность между балансовой стоимостью комплектующей и накопленной амортизацией комплектующей.</span><span class="sxs-lookup"><span data-stu-id="a43c6-180">The depreciated cost of components is calculated as the difference between the component balance value and the accumulated component depreciation.</span></span>

<span data-ttu-id="a43c6-181">В следующем примере показано, как вычисляется балансовая стоимость комплектующей.</span><span class="sxs-lookup"><span data-stu-id="a43c6-181">The following example shows how the component balance value is calculated.</span></span>

| <span data-ttu-id="a43c6-182">Номер транзакции</span><span class="sxs-lookup"><span data-stu-id="a43c6-182">Transaction number</span></span> | <span data-ttu-id="a43c6-183">Операция</span><span class="sxs-lookup"><span data-stu-id="a43c6-183">Operation</span></span>            | <span data-ttu-id="a43c6-184">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="a43c6-184">Amount</span></span> | <span data-ttu-id="a43c6-185">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a43c6-185">Comments</span></span>                                                            |
|--------------------|----------------------|--------|---------------------------------------------------------------------|
| <span data-ttu-id="a43c6-186">1</span><span class="sxs-lookup"><span data-stu-id="a43c6-186">1</span></span>                  | <span data-ttu-id="a43c6-187">Ввод в эксплуатацию</span><span class="sxs-lookup"><span data-stu-id="a43c6-187">Acquisition</span></span>          | <span data-ttu-id="a43c6-188">1000</span><span class="sxs-lookup"><span data-stu-id="a43c6-188">1,000</span></span>  | <span data-ttu-id="a43c6-189">Основное средство собрано из номенклатуры 1 и принято на баланс как эта сумма.</span><span class="sxs-lookup"><span data-stu-id="a43c6-189">The fixed asset is assempled from item 1 and acquired with amount.</span></span>  |
| <span data-ttu-id="a43c6-190">2</span><span class="sxs-lookup"><span data-stu-id="a43c6-190">2</span></span>                  | <span data-ttu-id="a43c6-191">Ввод в эксплуатацию</span><span class="sxs-lookup"><span data-stu-id="a43c6-191">Acquisition</span></span>          | <span data-ttu-id="a43c6-192">2000</span><span class="sxs-lookup"><span data-stu-id="a43c6-192">2,000</span></span>  | <span data-ttu-id="a43c6-193">Основное средство собрано из номенклатуры 2 и принято на баланс как эта сумма.</span><span class="sxs-lookup"><span data-stu-id="a43c6-193">The fixed asset is assempled from item 2 and acquired with amount.</span></span>  |
| <span data-ttu-id="a43c6-194">3</span><span class="sxs-lookup"><span data-stu-id="a43c6-194">3</span></span>                  | <span data-ttu-id="a43c6-195">Переоценка стоимости 1</span><span class="sxs-lookup"><span data-stu-id="a43c6-195">Cost revaluation 1</span></span>   | <span data-ttu-id="a43c6-196">1500</span><span class="sxs-lookup"><span data-stu-id="a43c6-196">1,500</span></span>  | <span data-ttu-id="a43c6-197">Основное средство переоценено.</span><span class="sxs-lookup"><span data-stu-id="a43c6-197">The fixed asset is revalued.</span></span>                                        |
| <span data-ttu-id="a43c6-198">4</span><span class="sxs-lookup"><span data-stu-id="a43c6-198">4</span></span>                  | <span data-ttu-id="a43c6-199">Амортизация</span><span class="sxs-lookup"><span data-stu-id="a43c6-199">Depreciation</span></span>         | <span data-ttu-id="a43c6-200">300</span><span class="sxs-lookup"><span data-stu-id="a43c6-200">300</span></span>    | <span data-ttu-id="a43c6-201">Рассчитана амортизация основного средства.</span><span class="sxs-lookup"><span data-stu-id="a43c6-201">Fixed asset depreciation is calculated.</span></span>                             |
| <span data-ttu-id="a43c6-202">5</span><span class="sxs-lookup"><span data-stu-id="a43c6-202">5</span></span>                  | <span data-ttu-id="a43c6-203">Ввод в эксплуатацию</span><span class="sxs-lookup"><span data-stu-id="a43c6-203">Acquisition</span></span>          | <span data-ttu-id="a43c6-204">2500</span><span class="sxs-lookup"><span data-stu-id="a43c6-204">2,500</span></span>  | <span data-ttu-id="a43c6-205">Основное средство собрано из номенклатуры 3 и принято на баланс как эта сумма.</span><span class="sxs-lookup"><span data-stu-id="a43c6-205">The fixed asset is assempled from item 3 and acquired with amount.</span></span>  |
| <span data-ttu-id="a43c6-206">6</span><span class="sxs-lookup"><span data-stu-id="a43c6-206">6</span></span>                  | <span data-ttu-id="a43c6-207">Амортизация</span><span class="sxs-lookup"><span data-stu-id="a43c6-207">Depreciation</span></span>         | <span data-ttu-id="a43c6-208">700</span><span class="sxs-lookup"><span data-stu-id="a43c6-208">700</span></span>    | <span data-ttu-id="a43c6-209">Рассчитана амортизация основного средства.</span><span class="sxs-lookup"><span data-stu-id="a43c6-209">Fixed asset depreciation is calculated.</span></span>                             |
| <span data-ttu-id="a43c6-210">7</span><span class="sxs-lookup"><span data-stu-id="a43c6-210">7</span></span>                  | <span data-ttu-id="a43c6-211">Разборка</span><span class="sxs-lookup"><span data-stu-id="a43c6-211">Disassembly</span></span>          | \*     | <span data-ttu-id="a43c6-212">Комплектующая "номенклатура 1" изъята из состава основного средства.</span><span class="sxs-lookup"><span data-stu-id="a43c6-212">The item 1 component is withdrawn from the fixed asset composition.</span></span> |
| <span data-ttu-id="a43c6-213">8</span><span class="sxs-lookup"><span data-stu-id="a43c6-213">8</span></span>                  | <span data-ttu-id="a43c6-214">Переоценка стоимости 2</span><span class="sxs-lookup"><span data-stu-id="a43c6-214">Cost revaluation 2</span></span>   | <span data-ttu-id="a43c6-215">2000</span><span class="sxs-lookup"><span data-stu-id="a43c6-215">2,000</span></span>  | <span data-ttu-id="a43c6-216">Основное средство переоценено.</span><span class="sxs-lookup"><span data-stu-id="a43c6-216">The fixed asset is revalued.</span></span>                                        |
| <span data-ttu-id="a43c6-217">9</span><span class="sxs-lookup"><span data-stu-id="a43c6-217">9</span></span>                  | <span data-ttu-id="a43c6-218">Амортизация стоимости 1</span><span class="sxs-lookup"><span data-stu-id="a43c6-218">Value depreciation 1</span></span> | <span data-ttu-id="a43c6-219">349,21</span><span class="sxs-lookup"><span data-stu-id="a43c6-219">349.21</span></span> | <span data-ttu-id="a43c6-220">Амортизация переоценена.</span><span class="sxs-lookup"><span data-stu-id="a43c6-220">The depreciation is revalued.</span></span>                                       |

<span data-ttu-id="a43c6-221">\* Во время частичной разборки основного средства (проводка 7) выполняются следующие условия:</span><span class="sxs-lookup"><span data-stu-id="a43c6-221">\* At the time of partial fixed asset disassembly (transaction 7), the following conditions are true:</span></span>

- <span data-ttu-id="a43c6-222">Балансовая стоимость основного средства составляет 1000 + 2000 + 1500 + 2500 = 7000.</span><span class="sxs-lookup"><span data-stu-id="a43c6-222">The fixed asset balance value is 1,000 + 2,000 + 1,500 + 2,500 = 7,000.</span></span>
- <span data-ttu-id="a43c6-223">Первоначальная стоимость составляет 1000 + 2000 + 2500 = 5500.</span><span class="sxs-lookup"><span data-stu-id="a43c6-223">The original cost is 1,000 + 2,000 + 2,500 = 5,500.</span></span>
- <span data-ttu-id="a43c6-224">Амортизация балансовой стоимости основного средства составляет 300 + 700 = 1000.</span><span class="sxs-lookup"><span data-stu-id="a43c6-224">The fixed asset balance depreciation is 300 + 700 = 1,000.</span></span>

<span data-ttu-id="a43c6-225">Таким образом, балансовая стоимость комплектующей "номенклатура 1" составляет 7000 × (1000 ÷ 5500) = 1272,73, а накопленная амортизация комплектующей "номенклатура 1" составляет 1000 × (1000 ÷ 5500) = 181,82.</span><span class="sxs-lookup"><span data-stu-id="a43c6-225">Therefore, the balance value of component item 1 is 7,000 × (1,000 ÷ 5,500) = 1,272.73, and the accumulated depreciation for component item 1 is 1,000 × (1,000 ÷ 5,500) = 181.82.</span></span>

<span data-ttu-id="a43c6-226">Ниже приведена балансовая стоимость комплектующей после проводок 1–7:</span><span class="sxs-lookup"><span data-stu-id="a43c6-226">Here is the balance value of the component after transactions 1 through 7 are completed:</span></span>

- <span data-ttu-id="a43c6-227">**Номенклатура 1:** 1272,73 (Выбытие комплектующей проведено с использованием указанной первоначальной стоимости.)</span><span class="sxs-lookup"><span data-stu-id="a43c6-227">**Item 1:** 1,272.73 (The component was disposed of by using the specified original cost.)</span></span>
- <span data-ttu-id="a43c6-228">**Номенклатура 2:** 2545,45</span><span class="sxs-lookup"><span data-stu-id="a43c6-228">**Item 2:** 2,545.45</span></span>
- <span data-ttu-id="a43c6-229">**Номенклатура 3:** 3181,82</span><span class="sxs-lookup"><span data-stu-id="a43c6-229">**Item 3:** 3,181.82</span></span>

<span data-ttu-id="a43c6-230">Ниже приведена накопленная амортизация комплектующей:</span><span class="sxs-lookup"><span data-stu-id="a43c6-230">Here is the accumulated component depreciation:</span></span>

- <span data-ttu-id="a43c6-231">**Номенклатура 1:** 181,82 (Выбытие комплектующей проведено с использованием указанной накопленной амортизации.)</span><span class="sxs-lookup"><span data-stu-id="a43c6-231">**Item 1:** 181.82 (The component was disposed of by using the specified accumulated depreciation.)</span></span>
- <span data-ttu-id="a43c6-232">**Номенклатура 2:** 363,64</span><span class="sxs-lookup"><span data-stu-id="a43c6-232">**Item 2:** 363.64</span></span>
- <span data-ttu-id="a43c6-233">**Номенклатура 3:** 454,54</span><span class="sxs-lookup"><span data-stu-id="a43c6-233">**Item 3:** 454.54</span></span>

<span data-ttu-id="a43c6-234">После проводок 1–9 балансовая стоимость основного средства составляет 1000 + 2000 + 1500 + 2500 + 2000 – 1272,73 = 7727,27.</span><span class="sxs-lookup"><span data-stu-id="a43c6-234">After transactions 1 through 9 are completed, the fixed asset balance value is 1,000 + 2,000 + 1,500 + 2,500 + 2,000 – 1,272.73 = 7,727.27.</span></span>

<span data-ttu-id="a43c6-235">Накопленная амортизация основного средства составляет 700 + 300 + 349,21 – 181,82 = 1167,39.</span><span class="sxs-lookup"><span data-stu-id="a43c6-235">The accumulated fixed asset depreciation is 700 + 300 + 349.21 – 181.82 = 1,167.39.</span></span>

<span data-ttu-id="a43c6-236">Первоначальная стоимость составляет 2000 + 2500.</span><span class="sxs-lookup"><span data-stu-id="a43c6-236">The original cost is 2,000 + 2,500.</span></span> <span data-ttu-id="a43c6-237">(На момент расчета основное средство состоит только из комплектующей "номенклатура 2" и комплектующей "номенклатура 3".)</span><span class="sxs-lookup"><span data-stu-id="a43c6-237">(At the time of calculation, the fixed asset consists of only component item 2 and component item 3.)</span></span>

<span data-ttu-id="a43c6-238">Ниже приведена балансовая стоимость:</span><span class="sxs-lookup"><span data-stu-id="a43c6-238">Here is the balance value:</span></span>

- <span data-ttu-id="a43c6-239">**Номенклатура 2:** 7727,27 × (2000 ÷ \[2000 + 2500\]) = 3434,34</span><span class="sxs-lookup"><span data-stu-id="a43c6-239">**Item 2:** 7,727.27 × (2,000 ÷ \[2,000 + 2,500\]) = 3,434.34</span></span>
- <span data-ttu-id="a43c6-240">**Номенклатура 3:** 7727,27 × (2500 ÷ \[2000 + 2500\]) = 4292,93</span><span class="sxs-lookup"><span data-stu-id="a43c6-240">**Item 3:** 7,727.27 × (2,500 ÷ \[2,000 + 2,500\]) = 4,292.93</span></span>

<span data-ttu-id="a43c6-241">Ниже приведена накопленная амортизация комплектующей:</span><span class="sxs-lookup"><span data-stu-id="a43c6-241">Here is the accumulated component depreciation:</span></span>

- <span data-ttu-id="a43c6-242">**Номенклатура 2:** 1167,39 × (2000 ÷ \[2000 + 2500\]) = 518,84</span><span class="sxs-lookup"><span data-stu-id="a43c6-242">**Item 2:** 1,167.39 × (2,000 ÷ \[2,000 + 2,500\]) = 518.84</span></span>
- <span data-ttu-id="a43c6-243">**Номенклатура 3:** 1167,39 × (2500 ÷ \[2000 + 2500\]) = 648,55</span><span class="sxs-lookup"><span data-stu-id="a43c6-243">**Item 3:** 1,167.39 × (2,500 ÷ \[2,000 + 2,500\]) = 648.55</span></span>

### <a name="the-iterate-method"></a><span data-ttu-id="a43c6-244">Итерационный метод</span><span class="sxs-lookup"><span data-stu-id="a43c6-244">The iterate method</span></span>

<span data-ttu-id="a43c6-245">Проводка переоценки основного средства не переоценивает все комплектующие соразмерно их первоначальной стоимости, а только соразмерно стоимости комплектующих, входящих в основное средство на момент проводки переоценки.</span><span class="sxs-lookup"><span data-stu-id="a43c6-245">The fixed asset revaluation transaction doesn't revalue all components in proportion to their original value, but only in proportion to the value of the components that are included at the time of the revaluation transaction..</span></span> <span data-ttu-id="a43c6-246">Дальше продолжает действовать метод пропорционального распределения.</span><span class="sxs-lookup"><span data-stu-id="a43c6-246">Furthermore, the proportional distribution method remains in effect.</span></span>

<span data-ttu-id="a43c6-247">Таким образом, для каждой комплектующей, подлежащей изъятию из состава основного средства, создается таблица, включающая все проводки переоценки.</span><span class="sxs-lookup"><span data-stu-id="a43c6-247">Therefore, for every component that is subject to withdrawal from the fixed asset composition, a table is created that includes all revaluation transactions.</span></span> <span data-ttu-id="a43c6-248">Крупные ремонты рассчитываются после принятия комплектующей на баланс.</span><span class="sxs-lookup"><span data-stu-id="a43c6-248">Major refurbishments are calculated after the component is acquired.</span></span> <span data-ttu-id="a43c6-249">В следующей таблице в качестве примера используется номенклатура 2.</span><span class="sxs-lookup"><span data-stu-id="a43c6-249">The following table uses item 2 as an example.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a43c6-250">i</span><span class="sxs-lookup"><span data-stu-id="a43c6-250">i</span></span></th>
<th><span data-ttu-id="a43c6-251">Сумма переоценки, Adj(i)</span><span class="sxs-lookup"><span data-stu-id="a43c6-251">Revaluation amount, Adj(i)</span></span></th>
<th><span data-ttu-id="a43c6-252">Балансовая стоимость основного средства до переоценки, S<sub>bal</sub>(i)</span><span class="sxs-lookup"><span data-stu-id="a43c6-252">Fixed asset balance value before revaluation, S<sub>bal</sub>(i)</span></span></th>
<th><span data-ttu-id="a43c6-253">Первоначальная стоимость комплектующей, S<sub>src</sub>(i)</span><span class="sxs-lookup"><span data-stu-id="a43c6-253">Original component cost, S<sub>src</sub>(i)</span></span></th>
<th><span data-ttu-id="a43c6-254">Стоимость после переоценки, S<sub>dst</sub>(i)</span><span class="sxs-lookup"><span data-stu-id="a43c6-254">Cost after revaluation, S<sub>dst</sub>(i)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a43c6-255">1</span><span class="sxs-lookup"><span data-stu-id="a43c6-255">1</span></span></td>
<td><span data-ttu-id="a43c6-256">1500</span><span class="sxs-lookup"><span data-stu-id="a43c6-256">1,500</span></span></td>
<td><span data-ttu-id="a43c6-257">3000</span><span class="sxs-lookup"><span data-stu-id="a43c6-257">3,000</span></span></td>
<td><span data-ttu-id="a43c6-258">2000</span><span class="sxs-lookup"><span data-stu-id="a43c6-258">2,000</span></span></td>
<td><span data-ttu-id="a43c6-259">S<sub>dst</sub>(i) = S<sub>src</sub>(i) × (1 + [Adj(i) ÷ S<sub>bal</sub>(i)]) = 3000</span><span class="sxs-lookup"><span data-stu-id="a43c6-259">S<sub>dst</sub>(i) = S<sub>src</sub>(i) × (1 + [Adj(i) ÷ S<sub>bal</sub>(i)]) = 3,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a43c6-260">2</span><span class="sxs-lookup"><span data-stu-id="a43c6-260">2</span></span></td>
<td><span data-ttu-id="a43c6-261">2000</span><span class="sxs-lookup"><span data-stu-id="a43c6-261">2,000</span></span></td>
<td><span data-ttu-id="a43c6-262">5500\*</span><span class="sxs-lookup"><span data-stu-id="a43c6-262">5,500\*</span></span></td>
<td><span data-ttu-id="a43c6-263">S<sub>src</sub>(i) = S<sub>dst</sub>(i–1) = 3000</span><span class="sxs-lookup"><span data-stu-id="a43c6-263">S<sub>src</sub>(i) = S<sub>dst</sub>(i–1) = 3,000</span></span></td>
<td><span data-ttu-id="a43c6-264">S<sub>dst</sub>(i) = S<sub>src</sub>(i) × (1 + [Adj(i) ÷ S<sub>bal</sub>(i)]) = 4090,91</span><span class="sxs-lookup"><span data-stu-id="a43c6-264">S<sub>dst</sub>(i) = S<sub>src</sub>(i) × (1 + [Adj(i) ÷ S<sub>bal</sub>(i)]) = 4,090.91</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a43c6-265">\* Рассчитанная балансовая стоимость основного средства включает в себя сумму переоценки основного средства, вызванной частичной разборкой основного средства.</span><span class="sxs-lookup"><span data-stu-id="a43c6-265">\* The fixed asset balance value that is calculated includes the fixed asset revaluation amount that is caused by a partial disassembly of the asset.</span></span>

<span data-ttu-id="a43c6-266">В таблице:</span><span class="sxs-lookup"><span data-stu-id="a43c6-266">Here is an explanation of the table:</span></span>

- <span data-ttu-id="a43c6-267">**Adj(i)** — стоимость текущей проводки переоценки.</span><span class="sxs-lookup"><span data-stu-id="a43c6-267">**Adj(i)** – The cost of the current revaluation transaction.</span></span>
- <span data-ttu-id="a43c6-268">**S<sub>bal</sub>(i)** — балансовая стоимость основного средства до переоценки.</span><span class="sxs-lookup"><span data-stu-id="a43c6-268">**S<sub>bal</sub>(i)** – The fixed asset balance value before revaluation.</span></span> <span data-ttu-id="a43c6-269">Эта стоимость рассчитывается как сумма всех проводок приобретения перед текущей проводкой переоценки плюс сумма всех проводок переоценки перед текущей проводкой переоценки и всех проводок крупного ремонта, минус предыдущие проводки частичной разборки основного средства.</span><span class="sxs-lookup"><span data-stu-id="a43c6-269">This value is calculated as the sum of all acquisition transactions before the current revaluation transaction, plus the sum of all revaluation transactions before the current revaluation transaction and all major refurbishment transactions, minus the previous partial fixed asset disassembly transactions.</span></span>
- <span data-ttu-id="a43c6-270">**S<sub>src</sub>(i)** — первоначальная стоимость комплектующей.</span><span class="sxs-lookup"><span data-stu-id="a43c6-270">**S<sub>src</sub>(i)** – The original component cost.</span></span> <span data-ttu-id="a43c6-271">Для первой переоценки эта стоимость устанавливается равной затратам на приобретение комплектующих.</span><span class="sxs-lookup"><span data-stu-id="a43c6-271">For a first revaluation, this value is set to the cost of acquiring the components.</span></span> <span data-ttu-id="a43c6-272">Например, если было приобретено 10 единиц и пять нужно изъять, эта сумма включает первоначальную стоимость пяти единиц.</span><span class="sxs-lookup"><span data-stu-id="a43c6-272">For example, if 10 units were acquired, and five must be withdrawn, this sum includes the original cost value of five units.</span></span> <span data-ttu-id="a43c6-273">Для всех последующих проводок эта сумма инициализируется по значению S<sub>dst</sub>(i-1).</span><span class="sxs-lookup"><span data-stu-id="a43c6-273">For all subsequent transactions, this sum is initialized from the S<sub>dst</sub>(i-1) value.</span></span>

<span data-ttu-id="a43c6-274">Расчетное значение округляется в соответствии с конфигурацией модуля "Основные средства".</span><span class="sxs-lookup"><span data-stu-id="a43c6-274">The calculated value is rounded according to the configuration of Fixed assets.</span></span>

<span data-ttu-id="a43c6-275">В данном примере балансовая стоимость комплектующей составляет 3000 после проводки переоценки 1 и 4090,91 после проводки переоценки.</span><span class="sxs-lookup"><span data-stu-id="a43c6-275">In the example, the component balance value is 3,000 after revaluation transaction 1 and 4,090.91 after revaluation transaction 2.</span></span>

<span data-ttu-id="a43c6-276">Расчет амортизации добавленной комплектующей аналогичен расчету балансовой стоимости.</span><span class="sxs-lookup"><span data-stu-id="a43c6-276">Calculation of the added component depreciation is similar to the calculation of the balance value.</span></span> <span data-ttu-id="a43c6-277">В этом случае проводки переоценки амортизации и проводки начисления амортизации аналогичны проводке переоценки.</span><span class="sxs-lookup"><span data-stu-id="a43c6-277">In this case, the depreciation revaluation transactions and depreciation accrual transactions are identical to the revaluation transaction.</span></span>

<span data-ttu-id="a43c6-278">Таблица создается для каждой комплектующей, изымаемой из состава основного средства.</span><span class="sxs-lookup"><span data-stu-id="a43c6-278">A table is created for every component that is withdrawn from the fixed asset composition.</span></span> <span data-ttu-id="a43c6-279">Строки таблицы включают в себя все проводки начисления амортизации и переоценки амортизации, совершенные после приобретения, кроме проводок переоценки амортизации, обусловленных проводками разборки.</span><span class="sxs-lookup"><span data-stu-id="a43c6-279">The lines of the table include all depreciation accrual and depreciation revaluation transactions that were completed after acquisition, except depreciation revaluation transactions that were triggered by disassembly transactions.</span></span> <span data-ttu-id="a43c6-280">См. следующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="a43c6-280">See the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a43c6-281">i</span><span class="sxs-lookup"><span data-stu-id="a43c6-281">i</span></span></th>
<th><span data-ttu-id="a43c6-282">Сумма амортизации или переоценки, Acq(i)</span><span class="sxs-lookup"><span data-stu-id="a43c6-282">Depreciation or revaluation amount, Acq(i)</span></span></th>
<th><span data-ttu-id="a43c6-283">Балансовая стоимость основного средства на момент амортизации или переоценки амортизации</span><span class="sxs-lookup"><span data-stu-id="a43c6-283">Fixed asset balance value at the time of depreciation or depreciation revaluation</span></span></th>
<th><span data-ttu-id="a43c6-284">Стоимость комплектующей, S<sub>dst</sub>(i)</span><span class="sxs-lookup"><span data-stu-id="a43c6-284">Component cost, S<sub>dst</sub>(i)</span></span></th>
<th><span data-ttu-id="a43c6-285">Амортизация после переоценки, A(i)</span><span class="sxs-lookup"><span data-stu-id="a43c6-285">Depreciation after revaluation, A(i)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a43c6-286">1</span><span class="sxs-lookup"><span data-stu-id="a43c6-286">1</span></span></td>
<td><span data-ttu-id="a43c6-287">300 (амортизация)</span><span class="sxs-lookup"><span data-stu-id="a43c6-287">300 (depreciation)</span></span></td>
<td><span data-ttu-id="a43c6-288">4500</span><span class="sxs-lookup"><span data-stu-id="a43c6-288">4,500</span></span></td>
<td><span data-ttu-id="a43c6-289">3000</span><span class="sxs-lookup"><span data-stu-id="a43c6-289">3,000</span></span></td>
<td><span data-ttu-id="a43c6-290">A(i) = A(i–1) + S<sub>dst</sub>(i) × (Acq(i) ÷ S<sub>bal</sub>) = 200</span><span class="sxs-lookup"><span data-stu-id="a43c6-290">A(i) = A(i–1) + S<sub>dst</sub>(i) × (Acq(i) ÷ S<sub>bal</sub>) = 200</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a43c6-291">2</span><span class="sxs-lookup"><span data-stu-id="a43c6-291">2</span></span></td>
<td><span data-ttu-id="a43c6-292">700 (амортизация)</span><span class="sxs-lookup"><span data-stu-id="a43c6-292">700 (depreciation)</span></span></td>
<td><span data-ttu-id="a43c6-293">7000</span><span class="sxs-lookup"><span data-stu-id="a43c6-293">7,000</span></span></td>
<td><span data-ttu-id="a43c6-294">3000</span><span class="sxs-lookup"><span data-stu-id="a43c6-294">3,000</span></span></td>
<td><span data-ttu-id="a43c6-295">A(i) = A(i–1) + S<sub>dst</sub>(i) × (Acq(i) ÷ S<sub>bal</sub>) = 500</span><span class="sxs-lookup"><span data-stu-id="a43c6-295">A(i) = A(i–1) + S<sub>dst</sub>(i) × (Acq(i) ÷ S<sub>bal</sub>) = 500</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a43c6-296">3</span><span class="sxs-lookup"><span data-stu-id="a43c6-296">3</span></span></td>
<td><span data-ttu-id="a43c6-297">349,21 (переоценка)</span><span class="sxs-lookup"><span data-stu-id="a43c6-297">349.21 (revaluation)</span></span></td>
<td><span data-ttu-id="a43c6-298">5500</span><span class="sxs-lookup"><span data-stu-id="a43c6-298">5,500</span></span></td>
<td><span data-ttu-id="a43c6-299">3000</span><span class="sxs-lookup"><span data-stu-id="a43c6-299">3,000</span></span></td>
<td><span data-ttu-id="a43c6-300">A(i) = A(i–1) + S<sub>dst</sub>(i) × (Acq(i) ÷ S<sub>bal</sub>) = 690,48</span><span class="sxs-lookup"><span data-stu-id="a43c6-300">A(i) = A(i–1) + S<sub>dst</sub>(i) × (Acq(i) ÷ S<sub>bal</sub>) = 690.48</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a43c6-301">Для первой строки амортизации значение A(i–1) равно 0.</span><span class="sxs-lookup"><span data-stu-id="a43c6-301">For the first depreciation line, the value A(i–1) equals 0 (zero).</span></span>

<span data-ttu-id="a43c6-302">Расчет накопленной амортизации комплектующей основывается на рассчитанной балансовой стоимости комплектующей.</span><span class="sxs-lookup"><span data-stu-id="a43c6-302">The calculation of accumulated component depreciation is based on the component balance value that is calculated.</span></span> <span data-ttu-id="a43c6-303">Расчет балансовой стоимости может быть объединен с расчетом амортизации.</span><span class="sxs-lookup"><span data-stu-id="a43c6-303">The balance value calculation can be combined with the depreciation calculation.</span></span> <span data-ttu-id="a43c6-304">Кроме того, может быть создана общая таблица проводок и могут быть выполнены необходимые действия, в зависимости от типа следующей проводки.</span><span class="sxs-lookup"><span data-stu-id="a43c6-304">Additionally, a general transaction table can be created, and the required steps can be performed, depending on the type of the next transaction.</span></span>

<span data-ttu-id="a43c6-305">Остаточная стоимость комплектующей рассчитывается как разность между рассчитанной балансовой стоимостью комплектующей и накопленной амортизацией комплектующей.</span><span class="sxs-lookup"><span data-stu-id="a43c6-305">The component depreciated cost is calculated as the difference between the component balance value that is calculated and the accumulated component depreciation.</span></span>

<span data-ttu-id="a43c6-306">Проводка частичной разборки оказывает косвенное влияние на балансовую стоимость основного средства.</span><span class="sxs-lookup"><span data-stu-id="a43c6-306">A partial take-down transaction has an indirect effect on the fixed asset balance.</span></span> <span data-ttu-id="a43c6-307">Проводка частичной разборки создает проводки переоценки стоимости и амортизации.</span><span class="sxs-lookup"><span data-stu-id="a43c6-307">A partial take-down transaction creates value and depreciation revaluation transactions.</span></span> <span data-ttu-id="a43c6-308">Эти проводки, в свою очередь, уже учитываются в балансовой стоимости основного средства.</span><span class="sxs-lookup"><span data-stu-id="a43c6-308">These transactions, in turn, are already considered in the fixed asset balance.</span></span>

<span data-ttu-id="a43c6-309">В результате расчета создаются балансовая стоимость, амортизация балансовой стоимости и рыночная стоимость, равная остаточной стоимости.</span><span class="sxs-lookup"><span data-stu-id="a43c6-309">As a result of the calculation, a balance value, a balance depreciation, and a market value that equals the depreciated cost are created.</span></span>
