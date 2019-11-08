---
title: Анализ ошибки актива
description: В этом разделе описывается анализ неполадок актива в управлении активами.
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
ms.openlocfilehash: 43772903f6845409cb33c7f2a13a049a3e9aa208
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652410"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="fe4cb-103">Анализ ошибки актива</span><span class="sxs-lookup"><span data-stu-id="fe4cb-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="fe4cb-104">В управлении активами можно анализировать регистрации ошибок активов для получения обзора общего числа ошибок, зарегистрированных в течение определенного периода времени.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="fe4cb-105">Регистрации ошибок можно анализировать с различных ракурсов, например, с целью сосредоточиться на активах, типах активов, функциональных местоположениях, признаках неисправностей или типах неисправностей.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="fe4cb-106">Щелкните **Управление активами** > **Запросы** > **Ошибка актива** > **Анализ ошибки актива**.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="fe4cb-107">В диалоговом окне **Расчет анализа ошибок активов** можно использовать поле **Уровень**, чтобы указать, насколько детальные должны быть строки ошибок активов в отношении функциональных местоположений.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="fe4cb-108">Например, если вставить число "1" в это поле, и имеется структура функциональных местоположений с несколькими уровнями, все строки ошибок активов для функционального местоположения будут показаны на верхнем уровне, и поэтому часы по строке могут быть добавлены из функциональных местоположений, расположенных на более низком уровне.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
        
    <span data-ttu-id="fe4cb-109">Если вставить число "0" в поле **Уровень**, будет выведен подробный результат, отображающий все строки ошибок активов на всех уровнях функциональных местоположений, к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="fe4cb-110">Если требуется ограничить поиск, можно выбрать отдельные активы, даты сбоя, причины неисправности и средства устранения неисправностей на экспресс-вкладке **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="fe4cb-111">Нажмите **ОК**, чтобы начать расчет.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="fe4cb-112">На вкладке **Анализ ошибки актива** нажмите одну или несколько кнопок **Группировать по...**, чтобы отобразить уровень детализации, который нужно просмотреть.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-112">On the **Asset fault analysis** tab, click one or more **Group by** buttons to display the detail level you want to see.</span></span> <span data-ttu-id="fe4cb-113">Активированные кнопки выделяются.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="fe4cb-114">Активируйте или отключайте кнопки, нажимая их.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="fe4cb-115">Щелкните **Обновить вычисления**, чтобы отобразить выбранные значения на экране.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="fe4cb-116">При каждой активации или деактивации кнопки **группировать по** не забывайте нажимать кнопку **обновить вычисления**.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-116">Every time you activate or deactivate a **Group by** button, remember to click the **Update calculations** button.</span></span> <span data-ttu-id="fe4cb-117">Это необходимо, поскольку при пересчете вероятности сбоя обрабатывается большой объем данных.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

## <a name="examples"></a><span data-ttu-id="fe4cb-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="fe4cb-118">Examples</span></span>

<span data-ttu-id="fe4cb-119">Имеется множество способов анализа регистраций неисправностей.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-119">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="fe4cb-120">В этом разделе приводится пять примеров того, как различные выборки данных могут обеспечить более глубокое понимание и подробности при анализе регистрации ошибок активов.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-120">This section has five examples of how different data selections can provide more insight and detail when analyzing asset fault registrations.</span></span>

### <a name="group-by-symptoms"></a><span data-ttu-id="fe4cb-121">Группировать по симптомам</span><span class="sxs-lookup"><span data-stu-id="fe4cb-121">Group by symptoms</span></span>

<span data-ttu-id="fe4cb-122">На следующем снимке экрана выбрана только кнопка **Симптом**.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-122">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="fe4cb-123">Регистрации неисправности были сделаны для трех признаков неисправности: "Утечка воздуха", "Перегорел предохранитель" и "Застревание оборудования".</span><span class="sxs-lookup"><span data-stu-id="fe4cb-123">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="fe4cb-124">В столбце **Вероятность в %** сумма всех процентов равна 100%.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-124">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="fe4cb-125">Вероятность основана на всех регистрациях **Симптом** в этом анализе ошибок.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-125">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![Рисунок 1](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a><span data-ttu-id="fe4cb-127">Группировка по симптомам и периоду времени</span><span class="sxs-lookup"><span data-stu-id="fe4cb-127">Group by symptoms and time period</span></span>

<span data-ttu-id="fe4cb-128">На следующем снимке экрана добавлены **Год** и **Месяц**, демонстрирующие способы просмотра регистраций ошибок в течение выбранного периода.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-128">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="fe4cb-129">Признаки неисправности отображаются в виде регистраций за год/месяц.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-129">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="fe4cb-130">В столбце **Вероятность в %**, если сложить все проценты для каждого месяца, получится 100%.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-130">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="fe4cb-131">Вероятность основана на регистрациях **Симптом** в этом анализе ошибок.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-131">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="fe4cb-132">Если в активе имеется большое количество строк, но большой процент обозначается в строке, это было бы указанием симптома отказа для более детального рассмотрения, чтобы найти способ ограничения количества регистраций для этого симптома отказа.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-132">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Рисунок 2](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a><span data-ttu-id="fe4cb-134">Группировка по нескольким симптомам и активам</span><span class="sxs-lookup"><span data-stu-id="fe4cb-134">Group by multiple symptoms and assets</span></span>

<span data-ttu-id="fe4cb-135">Комбинация активов и типов активов используется в качестве основы для расчетов, показанных на трех снимках экрана ниже, с увеличением уровня детализации.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-135">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  

<span data-ttu-id="fe4cb-136">Обычно кнопки в группах панели операций **Группировать по дате**, **Группировать по активу**, **Группировать по функциональному местоположению**, а также кнопка **Ошибка** (код неисправности) содержат периоды или связи актива.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-136">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** action pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="fe4cb-137">Кнопки **Симптом**, **Область**, **Тип**, **Причина** и **Решение** являются классификациями, используемыми в управлении сбоями для анализа регистраций ошибок активов и выявления проблемных областей.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-137">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="fe4cb-138">**Группировка по симптому, активу и типу актива**</span><span class="sxs-lookup"><span data-stu-id="fe4cb-138">**Group by symptom, asset, and asset type**</span></span>

<span data-ttu-id="fe4cb-139">На снимке экрана ниже **Актив** и **Тип актива** были добавлены, чтобы предоставить более подробные сведения о регистрациях ошибок.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-139">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="fe4cb-140">Симптомы сбоя теперь разбиваются по комбинациях **Актив** / **Тип актива** / **Симптом**.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-140">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="fe4cb-141">В столбце **Вероятность в %**, если сложить все проценты для комбинации **Актив** / **Тип актива** / **Симптом** соответственно, получится 100%.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-141">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="fe4cb-142">Вероятность основана на регистрациях **Симптом** в этом анализе ошибок.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-142">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="fe4cb-143">Если в активе имеется большое количество строк, но большой процент обозначается в строке, это было бы указанием симптома отказа для более детального рассмотрения, чтобы найти способ ограничения количества регистраций для этого симптома отказа.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-143">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Рисунок 3](media/08-controlling-and-reporting.png)

<span data-ttu-id="fe4cb-145">**Группировка по двум симптомам, активу и типу актива**</span><span class="sxs-lookup"><span data-stu-id="fe4cb-145">**Group by two symptoms, asset, and asset type**</span></span>

<span data-ttu-id="fe4cb-146">На снимке экрана ниже **Область** была добавлена в **Симптом**, **Актив** и **Тип актива**, чтобы предоставить более подробные сведения о регистрациях ошибок.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-146">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="fe4cb-147">В столбце **Вероятность в %**, если сложить все проценты для комбинации **Актив** / **Тип актива** / **Симптом** для актива, получится 100%.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="fe4cb-148">Вероятность основана на комбинации **Симптом** и **Область** в этом анализе ошибок.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-148">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="fe4cb-149">Если в активе имеется большое количество строк, но большой процент обозначается в строке, это было бы указанием области отказа для более детального рассмотрения, чтобы найти способ ограничения количества регистраций для этой области отказа.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![Рисунок 4](media/09-controlling-and-reporting.png)

<span data-ttu-id="fe4cb-151">**Группировка по трем симптомам, активу и типу актива**</span><span class="sxs-lookup"><span data-stu-id="fe4cb-151">**Group by three symptom, asset, and asset type**</span></span>

<span data-ttu-id="fe4cb-152">На снимке экрана, указанном ниже, был добавлен **Тип**, и в этом примере отображается наиболее подробный расчет.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-152">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="fe4cb-153">В столбце **Вероятность в %**, если сложить все проценты для комбинации **Актив** / **Тип актива** / **Симптом** для актива, получится 100%.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-153">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="fe4cb-154">Вероятность основана на комбинации **Симптом**, **Область** и **Тип** в этом анализе ошибок.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-154">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="fe4cb-155">Если в активе имеется большое количество строк, но большой процент обозначается в строке, это было бы указанием типа отказа для более детального рассмотрения, чтобы найти способ ограничения количества регистраций для этого типа отказа.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-155">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![Рисунок 5](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="fe4cb-157">Для обзора всех регистраций ошибок, созданных в заказах на работу и в запросах на обслуживание, щелкните **Управление активами** > **Запросы** > **Ошибка актива** > **Ошибки актива**.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-157">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="fe4cb-158">На странице **Ошибки актива** выберите регистрацию неисправности актива и раскройте область **Связанные сведения**, чтобы просмотреть сведения о связанном заказе на работу или запросе на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="fe4cb-158">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>

