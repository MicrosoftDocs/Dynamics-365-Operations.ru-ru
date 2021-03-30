---
title: Рабочее место формирования загрузки
description: В этой теме описывается, как работать с рабочим местом формирования загрузок.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 480006a6d091acdf5c88fdbf0d9e625088d660d4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247246"
---
# <a name="load-building-workbench"></a><span data-ttu-id="83fb7-103">Рабочее место формирования загрузки</span><span class="sxs-lookup"><span data-stu-id="83fb7-103">Load building workbench</span></span>

<span data-ttu-id="83fb7-104">Рабочее место формирования загрузок позволяет применять стратегии создания загрузок при создании загрузок.</span><span class="sxs-lookup"><span data-stu-id="83fb7-104">The load building workbench lets you apply load building strategies when you create loads.</span></span>

## <a name="create-a-load-building-strategy"></a><span data-ttu-id="83fb7-105">Создание стратегии формирования загрузок</span><span class="sxs-lookup"><span data-stu-id="83fb7-105">Create a load building strategy</span></span>

<span data-ttu-id="83fb7-106">Стратегии формирования загрузок используются для автоматического формирования загрузок.</span><span class="sxs-lookup"><span data-stu-id="83fb7-106">You use load building strategies to automatically build loads.</span></span> <span data-ttu-id="83fb7-107">Эта возможность может быть полезной в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="83fb7-107">This capability can be beneficial in the following situations:</span></span>

- <span data-ttu-id="83fb7-108">При регулярной отгрузке определенного набора продуктов стратегии загрузки помогают экономить время, поскольку вам не придется каждый раз формировать одинаковую загрузку.</span><span class="sxs-lookup"><span data-stu-id="83fb7-108">If you regularly ship a specific set of products, load strategies help save time, because you don't have to build the same load every time.</span></span>
- <span data-ttu-id="83fb7-109">Если необходимо избежать появления неполных загрузок, чтобы повысить эффективность, стратегии загрузки могут способствовать максимальному заполнению каждой загрузки.</span><span class="sxs-lookup"><span data-stu-id="83fb7-109">If you want to avoid half-full loads to maximize efficiency, load strategies can help fill each load as much as possible.</span></span>

<span data-ttu-id="83fb7-110">Класс стратегии формирования загрузки, который называется `TMSLoadBuildingVolumeStrategy`, предоставляет стратегию формирования загрузки, которая называется *стратегией формирования загрузки на основе объема*.</span><span class="sxs-lookup"><span data-stu-id="83fb7-110">A load building strategy class that is named `TMSLoadBuildingVolumeStrategy` provides a load building strategy that is named *Volume-based load building strategy*.</span></span> <span data-ttu-id="83fb7-111">Эта стратегия позволяет использовать максимальные значения, определенные для высоты и веса в шаблоне загрузки, или переопределить параметры путем ввода новых значений.</span><span class="sxs-lookup"><span data-stu-id="83fb7-111">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="83fb7-112">Эта стратегия является единственной стратегией, которая включается в комплект поставки.</span><span class="sxs-lookup"><span data-stu-id="83fb7-112">This strategy is the only strategy that is included out of the box.</span></span> <span data-ttu-id="83fb7-113">(Однако у вас могут быть свои пользовательские стратегии.)</span><span class="sxs-lookup"><span data-stu-id="83fb7-113">(However, you might have some custom strategies.)</span></span>

<span data-ttu-id="83fb7-114">Чтобы воспользоваться готовой стратегией *Стратегия формирования загрузки на основе объема*, выберите ее в поле **Стратегия формирования загрузки** на странице **Рабочее место формирования загрузки** (**Управление транспортировкой &gt; Планирование &gt; Рабочее место формирования загрузки**).</span><span class="sxs-lookup"><span data-stu-id="83fb7-114">To use the out-of-box *Volume-based load building strategy* strategy, select it in the **Load building strategy** field on the **Load building workbench** page (**Transportation management &gt; Planning &gt; Load building workbench**).</span></span>

<span data-ttu-id="83fb7-115">Чтобы создать стратегию формирования загрузки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="83fb7-115">To create a load building strategy, follow these steps.</span></span>

1. <span data-ttu-id="83fb7-116">Перейдите в раздел **Управление транспортировкой &gt; Настройка &gt; Формирование загрузки &gt; Стратегии формирования загрузок**.</span><span class="sxs-lookup"><span data-stu-id="83fb7-116">Go to **Transportation management &gt; Setup &gt; Load building &gt; Load building strategies**.</span></span>
1. <span data-ttu-id="83fb7-117">В области действий выберите **Создать список классов**, чтобы убедиться в наличии последних версий всех доступных классов.</span><span class="sxs-lookup"><span data-stu-id="83fb7-117">On the Action Pane, select **Generate class list** to make sure that you have the latest versions of all available classes.</span></span>
1. <span data-ttu-id="83fb7-118">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="83fb7-118">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="83fb7-119">Введите уникальное имя стратегии, выберите для нее класс стратегии формирования загрузки и введите описание.</span><span class="sxs-lookup"><span data-stu-id="83fb7-119">Enter a unique name for the strategy, select the load building strategy class for it, and enter a description.</span></span>
1. <span data-ttu-id="83fb7-120">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="83fb7-120">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="83fb7-121">На панели операций выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="83fb7-121">On the Action Pane, select **Parameters**.</span></span>
1. <span data-ttu-id="83fb7-122">На странице **Параметры стратегии формирования загрузки** выберите **Возможный объем** в списке, а затем в поле **Значение** введите процент общего возможного объема загрузки, который должен применяться для новой стратегии формирования загрузки.</span><span class="sxs-lookup"><span data-stu-id="83fb7-122">On the **Load building strategy parameters** page, select **Volume capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total volume capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="83fb7-123">Выберите в списке **Возможный вес** в списке, а затем в поле **Значение** введите процент общего возможного веса загрузки, который должен применяться для новой стратегии формирования загрузки.</span><span class="sxs-lookup"><span data-stu-id="83fb7-123">Select **Weight capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total weight capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="83fb7-124">Закройте страницу **Параметры стратегии формирования загрузки**.</span><span class="sxs-lookup"><span data-stu-id="83fb7-124">Close the **Load building strategy parameters** page.</span></span>
1. <span data-ttu-id="83fb7-125">Закройте страницу **Стратегии формирования загрузки**.</span><span class="sxs-lookup"><span data-stu-id="83fb7-125">Close the **Load building strategies** page.</span></span>

<span data-ttu-id="83fb7-126">Теперь можно назначить стратегию формирования загрузки шаблону формирования загрузки.</span><span class="sxs-lookup"><span data-stu-id="83fb7-126">You can now assign the load building strategy to a load building template.</span></span> <span data-ttu-id="83fb7-127">Кроме того, его можно использовать непосредственно на рабочем месте планирования загрузки.</span><span class="sxs-lookup"><span data-stu-id="83fb7-127">Alternatively, you can use it directly in the load planning workbench.</span></span>

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a><span data-ttu-id="83fb7-128">Использование стратегии формирования загрузки на рабочем месте планирования загрузки</span><span class="sxs-lookup"><span data-stu-id="83fb7-128">Use a load building strategy in the load building workbench</span></span>

1. <span data-ttu-id="83fb7-129">Перейдите в раздел **Управление транспортировкой &gt; Планирование &gt; Рабочее место формирования загрузки**.</span><span class="sxs-lookup"><span data-stu-id="83fb7-129">Go to **Transportation management &gt; Planning &gt; Load building workbench**.</span></span>
1. <span data-ttu-id="83fb7-130">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="83fb7-130">Follow one of these steps:</span></span>

    - <span data-ttu-id="83fb7-131">Выберите стратегию в поле **Стратегия формирования загрузки**.</span><span class="sxs-lookup"><span data-stu-id="83fb7-131">Select a strategy in the **Load building strategy** field.</span></span>
    - <span data-ttu-id="83fb7-132">Если вы определили шаблон формирования загрузки и назначили ему стратегию формирования загрузки, на панели операций на вкладке **Управление шаблонами** выберите **Применить шаблон**.</span><span class="sxs-lookup"><span data-stu-id="83fb7-132">If you've defined a load building template and assigned the load building strategy to it, on the Action Pane, on the **Manage templates** tab, select **Apply template**.</span></span> <span data-ttu-id="83fb7-133">Затем в раскрывающемся диалоговом окне **Применить шаблон формирования загрузки** выберите шаблон в поле **Имя шаблона формирования загрузки**.</span><span class="sxs-lookup"><span data-stu-id="83fb7-133">Then, in the **Apply load building template** drop-down dialog box, select a template in the **Load building template name** field.</span></span>

1. <span data-ttu-id="83fb7-134">На экспресс-вкладке **Последовательность шаблонов загрузок** выберите один или несколько [шаблонов загрузки](load-template.md).</span><span class="sxs-lookup"><span data-stu-id="83fb7-134">On the **Load templates sequence** FastTab, select one or more [load templates](load-template.md).</span></span> <span data-ttu-id="83fb7-135">Рабочее место попытается поместить загрузку в эти типы контейнеров в указанной здесь последовательности.</span><span class="sxs-lookup"><span data-stu-id="83fb7-135">The workbench will try to fit the load into these types of containers, in the sequence that is specified here.</span></span> <span data-ttu-id="83fb7-136">Обычно необходимо поместить самые маленькие контейнеры в верхнюю часть списка, чтобы обеспечить, что сначала будет выбран наименьший из возможных контейнеров.</span><span class="sxs-lookup"><span data-stu-id="83fb7-136">Typically, you should put the smallest containers at the top of the list to ensure that the smallest possible container is selected first.</span></span>
1. <span data-ttu-id="83fb7-137">В области операций выберите **Предложить загрузки**.</span><span class="sxs-lookup"><span data-stu-id="83fb7-137">On the Action Pane, select **Propose loads**.</span></span>
1. <span data-ttu-id="83fb7-138">Проверьте предложенные загрузки и предлагаемые строки загрузки.</span><span class="sxs-lookup"><span data-stu-id="83fb7-138">Review the proposed loads and proposed load lines.</span></span>
1. <span data-ttu-id="83fb7-139">В области действий выберите **Создать загрузки** для создания загрузок на основе строк исходного документа на экспресс-вкладке **Предложенные строки загрузки**.</span><span class="sxs-lookup"><span data-stu-id="83fb7-139">On the Action Pane, select **Create loads** to create loads that are based on the source document lines on the **Proposed load lines** FastTab.</span></span>
1. <span data-ttu-id="83fb7-140">Закройте страницу **Рабочее место формирования загрузки**.</span><span class="sxs-lookup"><span data-stu-id="83fb7-140">Close the **Load building workbench** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]