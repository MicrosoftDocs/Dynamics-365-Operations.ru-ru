---
title: Создание отчетов по потреблению
description: В этом разделе объясняется, как создавать отчеты по потреблению в модуле "Управление активами".
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d28acbccc35b3f59f9cca7236dd721a1d9bdead8
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216444"
---
# <a name="create-consumption-reports"></a><span data-ttu-id="1ca94-103">Создание отчетов по потреблению</span><span class="sxs-lookup"><span data-stu-id="1ca94-103">Create consumption reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="1ca94-104">После создания и разноски регистраций потребления в заказах на работу в модуле "Управление активами" доступны два отчета для просмотра сведений о потреблении.</span><span class="sxs-lookup"><span data-stu-id="1ca94-104">When you've created and posted consumption registrations on work orders in Asset Management, two reports are available to display consumption details.</span></span>


## <a name="asset-consumption-report"></a><span data-ttu-id="1ca94-105">Отчет о потреблении для активов</span><span class="sxs-lookup"><span data-stu-id="1ca94-105">Asset consumption report</span></span>

<span data-ttu-id="1ca94-106">После разноски потребления по заказам на работу можно распечатать отчет о потреблении для активов.</span><span class="sxs-lookup"><span data-stu-id="1ca94-106">When you have posted consumption on work orders, you can print an asset consumption report.</span></span> <span data-ttu-id="1ca94-107">В отчете отображаются часы, затраты часов, затраты на номенклатуры и расходы, разнесенные по активам.</span><span class="sxs-lookup"><span data-stu-id="1ca94-107">The report displays hours, hour costs, item costs, and expenses posted on assets.</span></span>

1. <span data-ttu-id="1ca94-108">Щелкните **Управление активами** > **Отчеты** > **Активы** > **Потребление для активов**.</span><span class="sxs-lookup"><span data-stu-id="1ca94-108">Click **Asset management** > **Reports** > **Assets** > **Asset consumption**.</span></span>

2. <span data-ttu-id="1ca94-109">В диалоговом окне **Потребление по активам** выберите нужные параметры и уровень детализации, выбрав **Да** для соответствующих переключателей и вставив уровень функционального местоположения в раздел **Показать**.</span><span class="sxs-lookup"><span data-stu-id="1ca94-109">In the **Asset consumption** dialog, select the parameters and detail level you want to see by selecting **Yes** on the relevant toggle buttons, and inserting a functional location level in the **Show** section.</span></span>
    - <span data-ttu-id="1ca94-110">Можно использовать поле **Уровни**, чтобы указать, насколько подробными должны быть строки активов относительно функциональных местоположений.</span><span class="sxs-lookup"><span data-stu-id="1ca94-110">You can use the **Levels** field to indicate how detailed you want the asset lines to be regarding functional locations.</span></span> 
    
        <span data-ttu-id="1ca94-111">Например, если ввести число "1" в это поле, и имеется структура функциональных местоположений с несколькими уровнями, все активы для функционального местоположения будут показаны на верхнем уровне, и поэтому строка может быть добавлена из функциональных местоположений, расположенных на более низком уровне.</span><span class="sxs-lookup"><span data-stu-id="1ca94-111">For example, if you enter the number "1" in the field, and you have a multi-level functional location structure, all assets for a functional location will be shown on the top level, and therefore a line may be added up from functional locations located at a lower level.</span></span> 
        
        <span data-ttu-id="1ca94-112">Если ввести число "0" в поле **Уровни**, будет выведен подробный результат, отображающий все активы на всех уровнях функциональных местоположений, к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="1ca94-112">If you enter the number "0" in the **Levels** field, you will see a detailed result showing all assets on all the functional location levels to which they are related.</span></span> 
        
    - <span data-ttu-id="1ca94-113">Выберите **Да** для переключателя **Сумма по всем вложенным активам**, чтобы увидеть суммы для каждого вложенного актива в отчете.</span><span class="sxs-lookup"><span data-stu-id="1ca94-113">Select **Yes** on the **Sum on all sub assets** toggle button to see sums for each sub asset in the report.</span></span>

3. <span data-ttu-id="1ca94-114">Выберите интервала дат в разделе **Даты**.</span><span class="sxs-lookup"><span data-stu-id="1ca94-114">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="1ca94-115">На экспресс-вкладке **Место назначения** выберите, необходимо ли отобразить отчет на экране, распечатать его или сохранить как файл или электронную почту.</span><span class="sxs-lookup"><span data-stu-id="1ca94-115">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="1ca94-116">При необходимости можно выбрать отдельные активы, которые будут отображаться в отчете.</span><span class="sxs-lookup"><span data-stu-id="1ca94-116">If required, you can select specific assets to be displayed in the report.</span></span> <span data-ttu-id="1ca94-117">На экспресс-вкладке **Записи для добавления** щелкните **Фильтр** и добавьте активы, которые требуется включить в отчет.</span><span class="sxs-lookup"><span data-stu-id="1ca94-117">On the **Records to include** FastTab, click **Filter**, and add the assets you want to include in the report.</span></span>

6. <span data-ttu-id="1ca94-118">Щелкните **ОК**, чтобы создать отчет.</span><span class="sxs-lookup"><span data-stu-id="1ca94-118">Click **OK** to generate the report.</span></span>


## <a name="work-order-consumption-report"></a><span data-ttu-id="1ca94-119">Отчет о потреблении по заказам на работу</span><span class="sxs-lookup"><span data-stu-id="1ca94-119">Work order consumption report</span></span>

<span data-ttu-id="1ca94-120">После разноски потребления по заказам на работу можно распечатать отчет о потреблении для заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="1ca94-120">When you have posted consumption on work orders, you can print a work order consumption report.</span></span> <span data-ttu-id="1ca94-121">В отчете отображаются часы, затраты часов, затраты на номенклатуры и расходы, разнесенные по заказам на работу.</span><span class="sxs-lookup"><span data-stu-id="1ca94-121">The report displays hours, hour costs, item costs, and expenses posted on work orders.</span></span>

1. <span data-ttu-id="1ca94-122">Щелкните **Управление активами** > **Отчеты** > **Заказы на работу** > **Потребление по заказам на работу**.</span><span class="sxs-lookup"><span data-stu-id="1ca94-122">Click **Asset management** > **Reports** > **Work orders** > **Work order consumption**.</span></span>

2. <span data-ttu-id="1ca94-123">В диалоговом окне **Потребление по заказам на работу** выберите параметры, которые требуется включить в отчет, выбрав **Да** в соответствующих переключателях в разделе **Показать**.</span><span class="sxs-lookup"><span data-stu-id="1ca94-123">In the **Work order consumption** dialog, select the parameters you want to include in the report by selecting **Yes** on the relevant toggle buttons in the **Show** section.</span></span>

3. <span data-ttu-id="1ca94-124">Выберите интервала дат в разделе **Даты**.</span><span class="sxs-lookup"><span data-stu-id="1ca94-124">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="1ca94-125">На экспресс-вкладке **Место назначения** выберите, необходимо ли отобразить отчет на экране, распечатать его или сохранить как файл или электронную почту.</span><span class="sxs-lookup"><span data-stu-id="1ca94-125">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="1ca94-126">При необходимости можно выбрать отдельные заказы на работу, которые будут отображаться в отчете.</span><span class="sxs-lookup"><span data-stu-id="1ca94-126">If required, you can select specific work orders to be displayed in the report.</span></span> <span data-ttu-id="1ca94-127">На экспресс-вкладке **Записи для добавления** щелкните **Фильтр** и добавьте заказы на работу, которые требуется включить в отчет.</span><span class="sxs-lookup"><span data-stu-id="1ca94-127">On the **Records to include** FastTab, click **Filter**, and add the work orders you want to include in the report.</span></span>

6. <span data-ttu-id="1ca94-128">Щелкните **ОК**, чтобы создать отчет.</span><span class="sxs-lookup"><span data-stu-id="1ca94-128">Click **OK** to generate the report.</span></span>


>[!NOTE]
><span data-ttu-id="1ca94-129">Можно также создать [отчет по заказу на работу](../work-orders/work-order-report.md), который содержит больше сведений о заказе на работу.</span><span class="sxs-lookup"><span data-stu-id="1ca94-129">You can also generate a [work order report](../work-orders/work-order-report.md), which contains more work order details.</span></span>

