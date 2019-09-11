---
title: Контроль затрат и дат
description: В этом разделе описывается контроль затрат и дат в модуле "Управление активами".
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2bcd1584f6a858f7589387fbfe96267b7c16176a
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918403"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="7be41-103">Контроль затрат и дат</span><span class="sxs-lookup"><span data-stu-id="7be41-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="7be41-104">В управлении активами можно рассчитать затраты, чтобы получить обзор фактических затрат по сравнению с бюджетными затратами по активам, функциональным местоположениям и заказам на работу.</span><span class="sxs-lookup"><span data-stu-id="7be41-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="7be41-105">Фактические затраты основываются на разнесенных проводках.</span><span class="sxs-lookup"><span data-stu-id="7be41-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="7be41-106">Можно также выполнить расчет даты, если необходимо сравнить плановые даты начала и окончания с фактическими датами начала и окончания заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="7be41-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="7be41-107">Управление затратами для активов, функциональных местоположений и заказов на работу</span><span class="sxs-lookup"><span data-stu-id="7be41-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="7be41-108">Расчеты, выполняемые для активов, функциональных местоположений и заказов на работу, практически идентичны.</span><span class="sxs-lookup"><span data-stu-id="7be41-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="7be41-109">Единственное отличие заключается в том, что для активов и функциональных местоположений можно также включить в расчет вложенные активы и вложенные функциональные местоположения.</span><span class="sxs-lookup"><span data-stu-id="7be41-109">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="7be41-110">Датой является дата проводки, в которую была записана регистрация.</span><span class="sxs-lookup"><span data-stu-id="7be41-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="7be41-111">Щелкните **Управление активами** > **Запросы** > **Активы** > **Управление затратами по активам** или **Управление затратами функционального местоположения**, или **Управление активами** > **Запросы** > **Заказы на работу** > **Управление затратами по заказам на работу**.</span><span class="sxs-lookup"><span data-stu-id="7be41-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="7be41-112">В диалоговом окне **Управление затратами по активам** / **Управление затратами по функциональным местоположениям** / **Управление затратами по заказам на работу** выберите период, который требуется рассчитать.</span><span class="sxs-lookup"><span data-stu-id="7be41-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a period to be calculated.</span></span>

3. <span data-ttu-id="7be41-113">При необходимости выберите набор финансовых аналитик, который необходимо включить в расчет.</span><span class="sxs-lookup"><span data-stu-id="7be41-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="7be41-114">Если не требуется показывать результаты, содержащие нулевые затраты, выберите "Да" для переключателя **Исключать нули**.</span><span class="sxs-lookup"><span data-stu-id="7be41-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="7be41-115">Можно использовать поле **Уровень**, чтобы указать, насколько подробными должны быть строки контроля затрат относительно функциональных местоположений.</span><span class="sxs-lookup"><span data-stu-id="7be41-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> <span data-ttu-id="7be41-116">Например, если вставить число "1" в это поле, и имеется иерархия функциональных местоположений с несколькими уровнями, все строки управления затратами для функционального местоположения будут показаны на верхнем уровне, и поэтому часы по строке могут быть добавлены из функциональных местоположений, расположенных на более низком уровне.</span><span class="sxs-lookup"><span data-stu-id="7be41-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="7be41-117">Если вставить число "0" в поле **Уровень**, будет выведен подробный результат, отображающий все строки управления затратами на всех уровнях функциональных местоположений, к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="7be41-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="7be41-118">Выберите "Да" для переключателя **Показать открытые подтвержденные затраты**, если необходимо включить этот столбец в расчет.</span><span class="sxs-lookup"><span data-stu-id="7be41-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="7be41-119">Выберите "Да" для переключателя **Включить вложенные активы** для отображения затрат, относящихся к вложенным активам, в виде отдельных строк.</span><span class="sxs-lookup"><span data-stu-id="7be41-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="7be41-120">Если требуется ограничить поиск, можно выбрать отдельные активы/функциональные местоположения/заказы на работу на экспресс-вкладке **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="7be41-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="7be41-121">Нажмите **ОК**, чтобы начать расчет.</span><span class="sxs-lookup"><span data-stu-id="7be41-121">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="7be41-122">На следующем рисунке показан пример диалогового окна **Управление затратами по активам**.</span><span class="sxs-lookup"><span data-stu-id="7be41-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

![Рисунок 1](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="7be41-124">В группах панели операций **Группировать по...** на странице **Управление затратами по активам** щелкните соответствующие кнопки, чтобы отобразить необходимый уровень детализации для расчета.</span><span class="sxs-lookup"><span data-stu-id="7be41-124">In the **Group by...** action pane groups on the **Asset cost control** page, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="7be41-125">Выбранные кнопки панели операций выделяются.</span><span class="sxs-lookup"><span data-stu-id="7be41-125">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="7be41-126">Нажимайте кнопку, чтобы активировать или деактивировать ее.</span><span class="sxs-lookup"><span data-stu-id="7be41-126">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="7be41-127">На следующем рисунке показан пример результатов расчета в **Управление затратами по активам**.</span><span class="sxs-lookup"><span data-stu-id="7be41-127">The figure below shows an example of calculation results in **Asset cost control**.</span></span>

![Рисунок 2](media/02-controlling-and-reporting.png)

<span data-ttu-id="7be41-129">Другим способом расчета затрат является выбор нескольких активов в разделе **Все активы** или **Активные активы**.</span><span class="sxs-lookup"><span data-stu-id="7be41-129">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="7be41-130">Затем вы нажимаете кнопку **Управление затратами** на вкладке **Общие**. В диалоговом окне **Управление затратами по активам** выбранные активы автоматически вставляются в поле **Актив** на экспресс-вкладке **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="7be41-130">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="7be41-131">Щелкните **OK**, и отображается расчет затрат для выбранных активов.</span><span class="sxs-lookup"><span data-stu-id="7be41-131">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="7be41-132">Эта же процедура может быть выполнена для функциональных местоположений в разделе **Все функциональные местоположения** или **Активные функциональные местоположения**, а также для заказов на работу в разделе **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="7be41-132">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>

>[!NOTE]
><span data-ttu-id="7be41-133">В поле **Исходный бюджет** отображаются бюджетные затраты из прогноза заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="7be41-133">The **Original budget** field shows budget costs from the work order forecast.</span></span> <span data-ttu-id="7be41-134">Поле **Подтвержденные затраты** показывает общую сумму расходов, которую юридическое лицо обязуется заплатить.</span><span class="sxs-lookup"><span data-stu-id="7be41-134">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> <span data-ttu-id="7be41-135">В поле **Открытые подтвержденные затраты** отображаются обязательства по оплате для номенклатур, времени и услуг, которые были заказаны или получены, но еще не были оплачены.</span><span class="sxs-lookup"><span data-stu-id="7be41-135">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> <span data-ttu-id="7be41-136">После разноски всех регистраций потребления соответствующие затраты включаются в поле **Фактические затраты**.</span><span class="sxs-lookup"><span data-stu-id="7be41-136">When all consumption registrations have been posted, the related costs are included in the **Actual cost** field.</span></span>

## <a name="work-order-date-control"></a><span data-ttu-id="7be41-137">Контроль даты заказа на работу</span><span class="sxs-lookup"><span data-stu-id="7be41-137">Work order date control</span></span>

<span data-ttu-id="7be41-138">Эта страница предназначена для обзора ожидаемых даты начала и окончания по сравнению с фактическими датами начала и окончания в заказах на работу.</span><span class="sxs-lookup"><span data-stu-id="7be41-138">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="7be41-139">Щелкните **Управление активами** > **Запросы** > **Заказы на работу** > **Управление данными заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="7be41-139">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="7be41-140">Щелкните **Рассчитать**.</span><span class="sxs-lookup"><span data-stu-id="7be41-140">Click **Calculate**.</span></span>

3. <span data-ttu-id="7be41-141">В поле **Функциональное местоположение** выберите функциональное местоположение.</span><span class="sxs-lookup"><span data-stu-id="7be41-141">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="7be41-142">Вставьте период, для которого необходимо выполнить расчет, в поля **Начальная дата** и **Конечная дата**.</span><span class="sxs-lookup"><span data-stu-id="7be41-142">Insert the period for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="7be41-143">Будут включены все заказы на работу с ожидаемым началом в пределах периода.</span><span class="sxs-lookup"><span data-stu-id="7be41-143">All work orders with expected start within the period will be included.</span></span>

5. <span data-ttu-id="7be41-144">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="7be41-144">Click **OK**.</span></span>

6. <span data-ttu-id="7be41-145">В группах панели операций **Группировать по...** щелкните соответствующие кнопки, чтобы отобразить необходимый уровень детализации для расчета.</span><span class="sxs-lookup"><span data-stu-id="7be41-145">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="7be41-146">Выбранные кнопки панели операций выделяются.</span><span class="sxs-lookup"><span data-stu-id="7be41-146">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="7be41-147">Нажимайте кнопку, чтобы активировать или деактивировать ее.</span><span class="sxs-lookup"><span data-stu-id="7be41-147">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="7be41-148">На следующем рисунке показан пример результатов расчета в поле **Управление датами заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="7be41-148">The figure below shows an example of calculation results in **Work order date control**.</span></span>

![Рисунок 3](media/03-controlling-and-reporting.png)

- <span data-ttu-id="7be41-150">В поле **Средняя задержка начала** отображается разница в днях между запланированной датой начала для заказа на работу по сравнению с фактической датой начала.</span><span class="sxs-lookup"><span data-stu-id="7be41-150">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="7be41-151">Если, например, фактическая дата начала была за два дня до запланированной даты начала, в этом поле будет отображено значение "–2".</span><span class="sxs-lookup"><span data-stu-id="7be41-151">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="7be41-152">В поле **Средняя задержка завершения** отображается разница в днях между запланированной датой завершения заказа на работу по сравнению с фактической датой завершения.</span><span class="sxs-lookup"><span data-stu-id="7be41-152">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="7be41-153">Если, например, фактическая дата завершения была за три дня до запланированной даты завершения, в этом поле будет отображено значение "3".</span><span class="sxs-lookup"><span data-stu-id="7be41-153">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="7be41-154">В полях **Случаи** отображается число случаев отклонения, связанных с запланированной и фактической датой начала, а также запланированной и фактической датой окончания заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="7be41-154">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>
