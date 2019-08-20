---
title: Отчетность по РБП (Россия)
description: Этот раздел содержит информацию о различных отчетах, доступных для РБП.
author: anasyash
manager: AnnBe
ms.date: 06/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: anasyash
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 40c6d8fd05dd20de95980c8bd131ad464129f6d8
ms.sourcegitcommit: 4fd51830be21b95a1398dc80d5429a74bcec73fc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2019
ms.locfileid: "1736973"
---
# <a name="reporting-for-deferrals-russia"></a><span data-ttu-id="06898-103">Отчетность по РБП (Россия)</span><span class="sxs-lookup"><span data-stu-id="06898-103">Reporting for deferrals (Russia)</span></span>

[!include [banner](../includes/banner.md)]

## <a name="deferrals-listing-report"></a><span data-ttu-id="06898-104">Отчет «Список РБП»</span><span class="sxs-lookup"><span data-stu-id="06898-104">Deferrals listing report</span></span>

<span data-ttu-id="06898-105">Отчет **Список РБП** показывает список РБП вместе с их текущим их состоянием, например, **Спланировано**, **В работе**, или **Закрыто**.</span><span class="sxs-lookup"><span data-stu-id="06898-105">The **Deferrals listing** report shows a list of deferrals together with their current status, such as **Scheduled**, **In process**, or **Closed**.</span></span> <span data-ttu-id="06898-106">Для каждого РБП в отчете также показана первоначальная сумма и оставшаяся сумма.</span><span class="sxs-lookup"><span data-stu-id="06898-106">For each deferral, the report also shows the initial amount and the remaining amount.</span></span> <span data-ttu-id="06898-107">Бухгалтеры генерируют и печатают этот отчет для анализа значения текущих сборов по РБП.</span><span class="sxs-lookup"><span data-stu-id="06898-107">Accountants generate and print this report to analyze the value of current deferral charges.</span></span>

1. <span data-ttu-id="06898-108">Перейти к **Главная книга** \> **Запросы и отчеты** \> **РБП** \> **Список РБП**.</span><span class="sxs-lookup"><span data-stu-id="06898-108">Go to **General ledger** \> **Inquiries and reports** \> **Deferrals** \> **Deferrals listing**.</span></span>
2. <span data-ttu-id="06898-109">Для фильтрации данных, появляющихся в отчете, используйте следующие параметры по умолчанию в диалоговом окне **Список РБП**.</span><span class="sxs-lookup"><span data-stu-id="06898-109">Use the following default parameters in the **Deferrals listing** dialog box to filter the data that appears on the report.</span></span>

    | <span data-ttu-id="06898-110">Поле</span><span class="sxs-lookup"><span data-stu-id="06898-110">Field</span></span>                                                 | <span data-ttu-id="06898-111">Описание</span><span class="sxs-lookup"><span data-stu-id="06898-111">Description</span></span> |
    |-------------------------------------------------------|-------------|
    | <span data-ttu-id="06898-112">Код модели</span><span class="sxs-lookup"><span data-stu-id="06898-112">Model number</span></span>                                          | <span data-ttu-id="06898-113">Выберите номер модели РБП.</span><span class="sxs-lookup"><span data-stu-id="06898-113">Select the deferral model number.</span></span> |
    | <span data-ttu-id="06898-114">Дата отчета</span><span class="sxs-lookup"><span data-stu-id="06898-114">Reporting date</span></span>                                        | <span data-ttu-id="06898-115">Выберите дату, для которой требуется создать отчет.</span><span class="sxs-lookup"><span data-stu-id="06898-115">Select the date to generate the report for.</span></span> |
    | <span data-ttu-id="06898-116">Исключать нулевые обороты</span><span class="sxs-lookup"><span data-stu-id="06898-116">Exclude zero turnovers</span></span>                                | <span data-ttu-id="06898-117">Установите этот параметр на **Да**, если РБП, которые имеют остаточную стоимость 0 (ноль), должны быть исключены из отчета.</span><span class="sxs-lookup"><span data-stu-id="06898-117">Set this option to **Yes** if deferrals that have a net book value of 0 (zero) should be excluded from the report.</span></span> |
    | <span data-ttu-id="06898-118">Идентификатор РБП (на экспресс-вкладке **Включаемые записи**)</span><span class="sxs-lookup"><span data-stu-id="06898-118">Deferral ID (on the **Records to include** FastTab)</span></span>   | <span data-ttu-id="06898-119">Код РБП, включенный в отчет.</span><span class="sxs-lookup"><span data-stu-id="06898-119">The deferral code that is included on the report.</span></span> |
    | <span data-ttu-id="06898-120">Дата присоединения (на экспресс-вкладке **Включаемые записи**)</span><span class="sxs-lookup"><span data-stu-id="06898-120">Date attached (on the **Records to include** FastTab)</span></span> | <span data-ttu-id="06898-121">Дата создания РБП, включенная в отчет.</span><span class="sxs-lookup"><span data-stu-id="06898-121">The deferral creation date that is included on the report.</span></span> |

## <a name="deferrals-transaction-listing-report"></a><span data-ttu-id="06898-122">Отчет по списку проводок РБП</span><span class="sxs-lookup"><span data-stu-id="06898-122">Deferrals transaction listing report</span></span>

<span data-ttu-id="06898-123">Отчет **Список проводок РБП** показывает проводки по РБП для модели РБП.</span><span class="sxs-lookup"><span data-stu-id="06898-123">The **Deferrals transaction listing** report shows the deferrals transactions for a deferral model.</span></span> <span data-ttu-id="06898-124">Проводки по РБП классифицируются по группе РБП.</span><span class="sxs-lookup"><span data-stu-id="06898-124">The deferrals transactions are categorized by deferrals group.</span></span> <span data-ttu-id="06898-125">Для каждой проводки по РБП отчет содержит такие сведения, как дата, тип, описание и сумма проводки.</span><span class="sxs-lookup"><span data-stu-id="06898-125">For each deferrals transaction, the report includes details such as the date, type, description, and amount of the transaction.</span></span> <span data-ttu-id="06898-126">Он также включает в себя имя РБП, статус, первоначальную сумму и сумму амортизации.</span><span class="sxs-lookup"><span data-stu-id="06898-126">It also includes the name of the deferral, the status, the initial amount, and the depreciated amount.</span></span> <span data-ttu-id="06898-127">Бухгалтеры периодически генерируют этот отчет для просмотра списка проводок по РБП.</span><span class="sxs-lookup"><span data-stu-id="06898-127">Accountants periodically generate this report to view a list of the deferrals transactions.</span></span>

1. <span data-ttu-id="06898-128">Перейти к **Главная книга** \> **Запросы и отчеты** \> **РБП** \> **Список проводок по РБП**.</span><span class="sxs-lookup"><span data-stu-id="06898-128">Go to **General ledger** \> **Inquires and reports** \> **Deferrals** \> **Deferrals transaction listing**.</span></span>
2. <span data-ttu-id="06898-129">Для фильтрации данных, появляющихся в отчете, используйте следующие параметры по умолчанию в диалоговом окне **Список проводок по РБП**.</span><span class="sxs-lookup"><span data-stu-id="06898-129">Use the following default parameters in the **Deferrals transaction listing** dialog box to filter the data that appears on the report.</span></span>

    | <span data-ttu-id="06898-130">Поле</span><span class="sxs-lookup"><span data-stu-id="06898-130">Field</span></span>                                                     | <span data-ttu-id="06898-131">Описание</span><span class="sxs-lookup"><span data-stu-id="06898-131">Description</span></span> |
    |-----------------------------------------------------------|-------------|
    | <span data-ttu-id="06898-132">Код модели</span><span class="sxs-lookup"><span data-stu-id="06898-132">Model number</span></span>                                              | <span data-ttu-id="06898-133">Выберите номер модели РБП.</span><span class="sxs-lookup"><span data-stu-id="06898-133">Select the deferral model number.</span></span> |
    | <span data-ttu-id="06898-134">Дата отчета</span><span class="sxs-lookup"><span data-stu-id="06898-134">Reporting date</span></span>                                            | <span data-ttu-id="06898-135">Выберите дату, для которой требуется создать отчет.</span><span class="sxs-lookup"><span data-stu-id="06898-135">Select the date to generate the report for.</span></span> |
    | <span data-ttu-id="06898-136">Исключать нулевые обороты</span><span class="sxs-lookup"><span data-stu-id="06898-136">Exclude zero turnovers</span></span>                                    | <span data-ttu-id="06898-137">Установите этот параметр на **Да**, если РБП, которые имеют остаточную стоимость 0 (ноль), должны быть исключены из отчета.</span><span class="sxs-lookup"><span data-stu-id="06898-137">Set this option to **Yes** if deferrals that have a net book value of 0 (zero) should be excluded from the report.</span></span> |
    | <span data-ttu-id="06898-138">Дата проводки (на экспресс-вкладке **Включаемые записи**)</span><span class="sxs-lookup"><span data-stu-id="06898-138">Transaction date (on the **Records to include** Fast Tab)</span></span> | <span data-ttu-id="06898-139">Дата разнесения проводки.</span><span class="sxs-lookup"><span data-stu-id="06898-139">The date when the transaction is posted.</span></span> |
    | <span data-ttu-id="06898-140">Идентификатор РБП (на экспресс-вкладке **Включаемые записи**)</span><span class="sxs-lookup"><span data-stu-id="06898-140">Deferral ID (on the **Records to include** Fast Tab)</span></span>      | <span data-ttu-id="06898-141">Идентификационный код РБП.</span><span class="sxs-lookup"><span data-stu-id="06898-141">The identification code of the deferral.</span></span> |
    | <span data-ttu-id="06898-142">Дата присоединения (на экспресс-вкладке **Включаемые записи**)</span><span class="sxs-lookup"><span data-stu-id="06898-142">Date attached (on the **Records to include** Fast Tab)</span></span>    | <span data-ttu-id="06898-143">Дата создания РБП.</span><span class="sxs-lookup"><span data-stu-id="06898-143">The date when the deferral is created.</span></span> |
    | <span data-ttu-id="06898-144">Код расхода (на экспресс-вкладке **Включаемые записи**)</span><span class="sxs-lookup"><span data-stu-id="06898-144">Expense code (on the **Records to include** Fast Tab)</span></span>     | <span data-ttu-id="06898-145">Код расхода РБП.</span><span class="sxs-lookup"><span data-stu-id="06898-145">The expense code of the deferrals.</span></span> |

## <a name="deferrals-balances-report"></a><span data-ttu-id="06898-146">Отчет по балансам РБП</span><span class="sxs-lookup"><span data-stu-id="06898-146">Deferrals balances report</span></span>

<span data-ttu-id="06898-147">Отчет **Балансы по РБП** показывает значения РБП, такие как первоначальные суммы, списанные суммы и суммы РБП по выбытию.</span><span class="sxs-lookup"><span data-stu-id="06898-147">The **Deferrals balances** report shows deferral values such as initial amounts, written-off sums, and retirement deferral amounts.</span></span> <span data-ttu-id="06898-148">Бухгалтеры периодически создают этот отчет для анализа сальдо по РБП за текущий период и для будущих расходов.</span><span class="sxs-lookup"><span data-stu-id="06898-148">Accountants periodically generate this report to analyze the remaining balance of deferrals for the current period and for future costs.</span></span>

1. <span data-ttu-id="06898-149">Перейти к **Главная книга** \> **Запросы и отчеты** \> **РБП** \> **Балансы по РБП**.</span><span class="sxs-lookup"><span data-stu-id="06898-149">Go to **General ledger** \> **Inquires and reports** \> **Deferrals** \> **Deferrals balances**.</span></span>
2. <span data-ttu-id="06898-150">Для фильтрации данных, появляющихся в отчете, используйте следующие параметры по умолчанию в диалоговом окне **Балансы по РБП**.</span><span class="sxs-lookup"><span data-stu-id="06898-150">Use the following default parameters in the **Deferrals balances** dialog box to filter the data that appears on the report.</span></span>

    | <span data-ttu-id="06898-151">Поле</span><span class="sxs-lookup"><span data-stu-id="06898-151">Field</span></span>                                                | <span data-ttu-id="06898-152">Описание</span><span class="sxs-lookup"><span data-stu-id="06898-152">Description</span></span> |
    |------------------------------------------------------|-------------|
    | <span data-ttu-id="06898-153">Код модели</span><span class="sxs-lookup"><span data-stu-id="06898-153">Model number</span></span>                                         | <span data-ttu-id="06898-154">Выберите номер модели, для которого информация о балансе по РБП включена в отчет.</span><span class="sxs-lookup"><span data-stu-id="06898-154">Select the model number for which the deferrals balance information is included on the report.</span></span> |
    | <span data-ttu-id="06898-155">Дата отчета</span><span class="sxs-lookup"><span data-stu-id="06898-155">Reporting date</span></span>                                       | <span data-ttu-id="06898-156">Введите дату, для которой информация о балансе по РБП включена в отчет.</span><span class="sxs-lookup"><span data-stu-id="06898-156">Enter the date for which the deferrals balance information is included on the report.</span></span> |
    | <span data-ttu-id="06898-157">Исключать нулевые обороты</span><span class="sxs-lookup"><span data-stu-id="06898-157">Exclude zero turnovers</span></span>                               | <span data-ttu-id="06898-158">Установите этот параметр на **Да**, если РБП, которые имеют остаточную стоимость 0 (ноль), должны быть исключены из отчета.</span><span class="sxs-lookup"><span data-stu-id="06898-158">Set this option to **Yes** if deferrals that have a net book value of 0 (zero) should be excluded from the report.</span></span> |
    | <span data-ttu-id="06898-159">Идентификатор РБП (на экспресс-вкладке **Включаемые записи**)</span><span class="sxs-lookup"><span data-stu-id="06898-159">Deferral ID (on the **Records to include** Fast Tab)</span></span> | <span data-ttu-id="06898-160">Идентификационный код для РБП.</span><span class="sxs-lookup"><span data-stu-id="06898-160">The identification code for the deferral.</span></span> |

## <a name="factor-for-deferrals-writing-off-report"></a><span data-ttu-id="06898-161">Отчет «Коэффициент для списания РБП».</span><span class="sxs-lookup"><span data-stu-id="06898-161">Factor for deferrals writing off report</span></span>

<span data-ttu-id="06898-162">Отчет **Коэффициенты для списания РБП** показывает список коэффициентов РБП.</span><span class="sxs-lookup"><span data-stu-id="06898-162">The **Factors for deferrals writing off** report shows a list of deferral factors.</span></span> <span data-ttu-id="06898-163">Коэффициенты РБП сгруппированы по дате начала периода, для которого формируется отчет.</span><span class="sxs-lookup"><span data-stu-id="06898-163">The deferral factors are grouped by the start date of the period that the report is generated for.</span></span> <span data-ttu-id="06898-164">Данные в этом отчете могут включать код расхода, коэффициент коэффициента, суммы по норме и базовые суммы.</span><span class="sxs-lookup"><span data-stu-id="06898-164">The data on this report might include the expense code, the coefficient of the factor, normalized amounts, and base amounts.</span></span> <span data-ttu-id="06898-165">Бухгалтеры генерируют этот отчет для просмотра списка коэффициентов РБП для расчета амортизации.</span><span class="sxs-lookup"><span data-stu-id="06898-165">Accountants generate this report to view a list of deferral factors to calculate depreciation.</span></span>

1. <span data-ttu-id="06898-166">Перейти к **Главная книга** \> **Запросы и отчеты** \> **РБП** \> **Коэффициенты списания РБП**.</span><span class="sxs-lookup"><span data-stu-id="06898-166">Go to **General ledger** \> **Inquires and reports** \> **Deferrals** \> **Factors for deferrals writing off**.</span></span>
2. <span data-ttu-id="06898-167">Для фильтрации данных, появляющихся в отчете, используйте следующие параметры по умолчанию в диалоговом окне **Коэффициенты списания РБП**.</span><span class="sxs-lookup"><span data-stu-id="06898-167">Use the following default parameters in the **Factors for deferrals writing off** dialog box to filter the data that appears on the report.</span></span>

    | <span data-ttu-id="06898-168">Поле</span><span class="sxs-lookup"><span data-stu-id="06898-168">Field</span></span>                                                    | <span data-ttu-id="06898-169">Описание</span><span class="sxs-lookup"><span data-stu-id="06898-169">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="06898-170">Дата начала (на экспресс-вкладке **Включаемые записи**)</span><span class="sxs-lookup"><span data-stu-id="06898-170">Start date (on the **Records to include** Fast Tab)</span></span>      | <span data-ttu-id="06898-171">Дата начала периода, для которого создается отчет.</span><span class="sxs-lookup"><span data-stu-id="06898-171">The start date of the period that the report is generated for.</span></span> |
    | <span data-ttu-id="06898-172">Группа РБП (на экспресс-вкладке **Включаемые записи**)</span><span class="sxs-lookup"><span data-stu-id="06898-172">Deferrals group (on the **Records to include** Fast Tab)</span></span> | <span data-ttu-id="06898-173">Идентификационный код группы РБП, для которой в отчет включены коэффициенты РБП.</span><span class="sxs-lookup"><span data-stu-id="06898-173">The identification code of the deferrals group for which the deferral factors are included on the report.</span></span> |
    | <span data-ttu-id="06898-174">Код расхода (на экспресс-вкладке **Включаемые записи**)</span><span class="sxs-lookup"><span data-stu-id="06898-174">Expense code (on the **Records to include** Fast Tab)</span></span>    | <span data-ttu-id="06898-175">Код расходов коэффициентов РБП, включенных в отчет.</span><span class="sxs-lookup"><span data-stu-id="06898-175">The expense code of the deferral factors that are included on the report.</span></span> |