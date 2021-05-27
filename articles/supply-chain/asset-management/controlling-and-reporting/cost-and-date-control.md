---
title: Контроль затрат и дат
description: В этом разделе описывается контроль затрат и дат в модуле "Управление активами".
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c09dee94891fb78c22e8cf9f203cb7f5531bb968
ms.sourcegitcommit: 51cad1ce3ed44ebf7eb9bdf553ee2df4c1f03135
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "6016163"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="b23c1-103">Контроль затрат и дат</span><span class="sxs-lookup"><span data-stu-id="b23c1-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b23c1-104">В управлении активами можно рассчитать затраты, чтобы получить обзор фактических затрат по сравнению с бюджетными затратами по активам, функциональным местоположениям и заказам на работу.</span><span class="sxs-lookup"><span data-stu-id="b23c1-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="b23c1-105">Фактические затраты основываются на разнесенных проводках.</span><span class="sxs-lookup"><span data-stu-id="b23c1-105">Actual costs are based on posted transactions.</span></span>

<span data-ttu-id="b23c1-106">Можно также выполнить расчет даты, если необходимо сравнить плановые даты начала и окончания с фактическими датами начала и окончания заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="b23c1-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="b23c1-107">Управление затратами для активов, функциональных местоположений и заказов на работу</span><span class="sxs-lookup"><span data-stu-id="b23c1-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="b23c1-108">Расчеты, выполняемые для активов, функциональных местоположений и заказов на работу, практически идентичны.</span><span class="sxs-lookup"><span data-stu-id="b23c1-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="b23c1-109">Единственное отличие заключается в том, что для активов и функциональных местоположений можно также включить в расчет вложенные активы и вложенные функциональные местоположения.</span><span class="sxs-lookup"><span data-stu-id="b23c1-109">The only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="b23c1-110">Датой является дата проводки, в которую была записана регистрация.</span><span class="sxs-lookup"><span data-stu-id="b23c1-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="b23c1-111">Щелкните **Управление активами** > **Запросы** > **Активы** > **Управление затратами по активам** или **Управление затратами функционального местоположения**, или **Управление активами** > **Запросы** > **Заказы на работу** > **Управление затратами по заказам на работу**.</span><span class="sxs-lookup"><span data-stu-id="b23c1-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="b23c1-112">В диалоговом окне **Управление затратами по активам** / **Управление затратами по функциональным местоположениям** / **Управление затратами по заказам на работу** выберите период, который требуется рассчитать.</span><span class="sxs-lookup"><span data-stu-id="b23c1-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a time range to be calculated.</span></span>

3. <span data-ttu-id="b23c1-113">При необходимости выберите набор финансовых аналитик, который необходимо включить в расчет.</span><span class="sxs-lookup"><span data-stu-id="b23c1-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="b23c1-114">Если не требуется показывать результаты, содержащие нулевые затраты, выберите "Да" для переключателя **Исключать нули**.</span><span class="sxs-lookup"><span data-stu-id="b23c1-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="b23c1-115">Можно использовать поле **Уровень**, чтобы указать, насколько подробными должны быть строки контроля затрат относительно функциональных местоположений.</span><span class="sxs-lookup"><span data-stu-id="b23c1-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="b23c1-116">Например, если вставить число "1" в это поле, и имеется иерархия функциональных местоположений с несколькими уровнями, все строки управления затратами для функционального местоположения будут показаны на верхнем уровне, и поэтому часы по строке могут быть добавлены из функциональных местоположений, расположенных на более низком уровне.</span><span class="sxs-lookup"><span data-stu-id="b23c1-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span>

    <span data-ttu-id="b23c1-117">Если вставить число "0" в поле **Уровень**, будет выведен подробный результат, отображающий все строки управления затратами на всех уровнях функциональных местоположений, к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="b23c1-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="b23c1-118">Выберите "Да" для переключателя **Показать открытые подтвержденные затраты**, если необходимо включить этот столбец в расчет.</span><span class="sxs-lookup"><span data-stu-id="b23c1-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="b23c1-119">Выберите "Да" для переключателя **Включить вложенные активы** для отображения затрат, относящихся к вложенным активам, в виде отдельных строк.</span><span class="sxs-lookup"><span data-stu-id="b23c1-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="b23c1-120">Если требуется ограничить поиск, можно выбрать отдельные активы/функциональные местоположения/заказы на работу на экспресс-вкладке **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="b23c1-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="b23c1-121">Нажмите **ОК**, чтобы начать расчет.</span><span class="sxs-lookup"><span data-stu-id="b23c1-121">Click **OK** to start the calculation.</span></span>

    <span data-ttu-id="b23c1-122">На следующем рисунке показан пример диалогового окна **Управление затратами по активам**.</span><span class="sxs-lookup"><span data-stu-id="b23c1-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

    ![Диалоговое окно "Управление затратами по активам"](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="b23c1-124">На странице **Управление затратами по активам** щелкните **Группировать по...**, чтобы отобразить необходимый уровень детализации для расчета.</span><span class="sxs-lookup"><span data-stu-id="b23c1-124">On the **Asset cost control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="b23c1-125">Выбранные кнопки **Группировать по...** выделяются.</span><span class="sxs-lookup"><span data-stu-id="b23c1-125">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="b23c1-126">Нажимайте кнопку, чтобы активировать или деактивировать ее.</span><span class="sxs-lookup"><span data-stu-id="b23c1-126">Click on a button to activate or deactivate it.</span></span>

## <a name="example-of-calculation-results-in-asset-cost-control"></a><span data-ttu-id="b23c1-127">Пример результатов расчета в управление затратами по активам</span><span class="sxs-lookup"><span data-stu-id="b23c1-127">Example of calculation results in asset cost control</span></span>

<span data-ttu-id="b23c1-128">На следующем снимке экрана показан пример результатов расчета в **Управление затратами по активам**.</span><span class="sxs-lookup"><span data-stu-id="b23c1-128">The screenshot below shows an example of calculation results in **Asset cost control**.</span></span>

- <span data-ttu-id="b23c1-129">В поле **Исходный бюджет** отображаются бюджетные затраты из прогноза заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="b23c1-129">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="b23c1-130">Поле **Подтвержденные затраты** показывает общую сумму расходов, которую юридическое лицо обязуется заплатить.</span><span class="sxs-lookup"><span data-stu-id="b23c1-130">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> 
- <span data-ttu-id="b23c1-131">В поле **Открытые подтвержденные затраты** отображаются обязательства по оплате для номенклатур, времени и услуг, которые были заказаны или получены, но еще не были оплачены.</span><span class="sxs-lookup"><span data-stu-id="b23c1-131">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> 
- <span data-ttu-id="b23c1-132">После разноски всех регистраций потребления связанные затраты отображаются в поле **Фактические затраты**.</span><span class="sxs-lookup"><span data-stu-id="b23c1-132">The **Actual cost** field shows related costs after all consumption registrations have been posted.</span></span>

![Пример результатов расчета в Управление затратами по активам](media/02-controlling-and-reporting.png)

<span data-ttu-id="b23c1-134">Другим способом расчета затрат является выбор нескольких активов в разделе **Все активы** или **Активные активы**.</span><span class="sxs-lookup"><span data-stu-id="b23c1-134">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="b23c1-135">Затем вы нажимаете кнопку **Управление затратами** на вкладке **Общие**. В диалоговом окне **Управление затратами по активам** выбранные активы автоматически вставляются в поле **Актив** на экспресс-вкладке **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="b23c1-135">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="b23c1-136">Щелкните **OK**, и отображается расчет затрат для выбранных активов.</span><span class="sxs-lookup"><span data-stu-id="b23c1-136">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="b23c1-137">Эта же процедура может быть выполнена для функциональных местоположений в разделе **Все функциональные местоположения** или **Активные функциональные местоположения**, а также для заказов на работу в разделе **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="b23c1-137">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>

## <a name="work-order-date-control"></a><span data-ttu-id="b23c1-138">Контроль даты заказа на работу</span><span class="sxs-lookup"><span data-stu-id="b23c1-138">Work order date control</span></span>

<span data-ttu-id="b23c1-139">Эта страница предназначена для обзора ожидаемых даты начала и окончания по сравнению с фактическими датами начала и окончания в заказах на работу.</span><span class="sxs-lookup"><span data-stu-id="b23c1-139">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="b23c1-140">Щелкните **Управление активами** > **Запросы** > **Заказы на работу** > **Управление данными заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="b23c1-140">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="b23c1-141">Щелкните **Рассчитать**.</span><span class="sxs-lookup"><span data-stu-id="b23c1-141">Click **Calculate**.</span></span>

3. <span data-ttu-id="b23c1-142">В поле **Функциональное местоположение** выберите функциональное местоположение.</span><span class="sxs-lookup"><span data-stu-id="b23c1-142">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="b23c1-143">Вставьте диапазон, для которого необходимо выполнить расчет, в поля **Начальная дата** и **Конечная дата**.</span><span class="sxs-lookup"><span data-stu-id="b23c1-143">Insert the range for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="b23c1-144">Будут включены все заказы на работу с ожидаемой датой начала в пределах диапазона.</span><span class="sxs-lookup"><span data-stu-id="b23c1-144">All work orders with expected start date within the range will be included.</span></span>

5. <span data-ttu-id="b23c1-145">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="b23c1-145">Click **OK**.</span></span>

6. <span data-ttu-id="b23c1-146">Щелкните кнопки **Группировать по...**, чтобы отобразить необходимый уровень детализации для расчета.</span><span class="sxs-lookup"><span data-stu-id="b23c1-146">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="b23c1-147">Выбранные кнопки **Группировать по...** выделяются.</span><span class="sxs-lookup"><span data-stu-id="b23c1-147">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="b23c1-148">Нажимайте кнопку, чтобы активировать или деактивировать ее.</span><span class="sxs-lookup"><span data-stu-id="b23c1-148">Click on a button to activate or deactivate it.</span></span>

## <a name="example-of-calculation-results-in-work-order-date-control"></a><span data-ttu-id="b23c1-149">Пример результатов расчета в управление датами заказов на работу</span><span class="sxs-lookup"><span data-stu-id="b23c1-149">Example of calculation results in work order date control</span></span>

<span data-ttu-id="b23c1-150">На следующем снимке экрана показан пример результатов расчета в поле **Управление датами заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="b23c1-150">The screenshot below shows an example of calculation results in **Work order date control**.</span></span>

- <span data-ttu-id="b23c1-151">В поле **Средняя задержка начала** отображается разница в днях между запланированной датой начала для заказа на работу по сравнению с фактической датой начала.</span><span class="sxs-lookup"><span data-stu-id="b23c1-151">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="b23c1-152">Если, например, фактическая дата начала была за два дня до запланированной даты начала, в этом поле будет отображено значение "–2".</span><span class="sxs-lookup"><span data-stu-id="b23c1-152">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="b23c1-153">В поле **Средняя задержка завершения** отображается разница в днях между запланированной датой завершения заказа на работу по сравнению с фактической датой завершения.</span><span class="sxs-lookup"><span data-stu-id="b23c1-153">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="b23c1-154">Если, например, фактическая дата завершения была за три дня до запланированной даты завершения, в этом поле будет отображено значение "3".</span><span class="sxs-lookup"><span data-stu-id="b23c1-154">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="b23c1-155">В полях **Случаи** отображается число случаев отклонения, связанных с запланированной и фактической датой начала, а также запланированной и фактической датой окончания заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="b23c1-155">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

![Пример результатов расчета в Управление датами заказов на работу](media/03-controlling-and-reporting.png)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]