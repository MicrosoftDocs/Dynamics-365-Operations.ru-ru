---
title: Шаблоны волны
description: В этом разделе описывается, как настроить критерии, определяющие способ обработки волн (вручную или автоматически), и работу, создаваемую при обработке волны.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: b02283a6e0a4ef0d61be8b66f82be8c125028cb0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813635"
---
# <a name="wave-templates"></a><span data-ttu-id="7bb5a-103">Шаблоны волны</span><span class="sxs-lookup"><span data-stu-id="7bb5a-103">Wave templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bb5a-104">В этом разделе описывается, как настроить критерии, определяющие способ обработки волн (вручную или автоматически), и работу, создаваемую при обработке волны.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-104">This topic describes how to set up the criteria that determine whether waves are processed manually or automatically, and the work that is generated for a warehouse when a wave is processed.</span></span> <span data-ttu-id="7bb5a-105">Чтобы определить критерии, настройте шаблоны и запросы волн, которые соответствуют волне с запущенными в производство строками в заказах на продажу, производственных заказах и канбанах.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-105">You specify the criteria by setting up wave templates and queries that match a wave with released lines in sales orders, production orders, and kanbans.</span></span>

## <a name="settings-for-wave-templates"></a><span data-ttu-id="7bb5a-106">Параметры шаблонов волн</span><span class="sxs-lookup"><span data-stu-id="7bb5a-106">Settings for wave templates</span></span>

<span data-ttu-id="7bb5a-107">При настройке шаблона волны необходимо определить следующее:</span><span class="sxs-lookup"><span data-stu-id="7bb5a-107">When you set up a wave template, you specify the following:</span></span>

- <span data-ttu-id="7bb5a-108">**Сайт** и **Cклад**, для которого шаблон создает работу.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-108">The **Site** and **Warehouse** that the template will create work for.</span></span>
- <span data-ttu-id="7bb5a-109">Порядок, в котором будет выполняться оценка шаблонов.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-109">The order in which the templates will be evaluated.</span></span> <span data-ttu-id="7bb5a-110">Последовательность, в которой шаблоны сопоставляются с запущенными в производство строками в заказах на продажу, производственных заказах и канбанах.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-110">The sequence in which the templates are matched to released lines on sales orders, production orders, and kanbans.</span></span> <span data-ttu-id="7bb5a-111">Когда выпускается строка, система применяет первый шаблон волны, для которого строка соответствует критериям.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-111">When a line is released, the system applies the first wave template that the line meets the criteria for.</span></span> <span data-ttu-id="7bb5a-112">Чем шире критерии, тем выше вероятность, что строка будет удовлетворять критериям, поэтому следует поместить шаблоны с наиболее конкретным критериями в верхней части списка.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-112">The broader the criteria, the more likely it is for a line to meet the criteria, so you should put the templates with the most specific criteria at the top of the list.</span></span> <span data-ttu-id="7bb5a-113">Используйте кнопки **Вверх** и **Вниз** на панели действий, чтобы упорядочить шаблоны в списке.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-113">Use the **Move up** and **Move down** buttons on the Action Pane to arrange templates in the list.</span></span>
- <span data-ttu-id="7bb5a-114">Действия, выполняемые каждым шаблоном.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-114">The actions taken by each template.</span></span> <span data-ttu-id="7bb5a-115">**Методы** волны выполняют действия, которые созданы шаблоном, например создание или распределение работы для каждого типа шаблона волны.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-115">The wave **Methods** perform the actions that are created by the template, such creating or distributing work for each type of wave template.</span></span>
- <span data-ttu-id="7bb5a-116">Атрибуты волны (фильтры), которые должны применяться к используемому шаблону волны.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-116">The wave attributes (filters) that must apply for the wave template to be used.</span></span>

> [!NOTE]
> <span data-ttu-id="7bb5a-117">При необходимости разработчик может создать дополнительные методы.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-117">If needed, a developer can create additional methods.</span></span> <span data-ttu-id="7bb5a-118">Полный список методов можно просмотреть на странице **Методы процесса волны**.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-118">You can view the full list of methods on the **Wave process methods** page.</span></span>

<span data-ttu-id="7bb5a-119">Некоторые параметры представляют стратегические решения для обработки волны, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-119">Some settings represent strategic decisions for wave processing, as follows:</span></span>

- <span data-ttu-id="7bb5a-120">Если шаблон используется для отгрузки номенклатур для заказов на продажу и заказов на перемещение или используется для перемещения номенклатур в производство для производственных заказов или канбанов.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-120">If the template is used for shipping items for sales orders and transfer orders, or used for moving items to production for production orders or kanbans.</span></span>
- <span data-ttu-id="7bb5a-121">Если волна обрабатывается вручную или автоматически следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7bb5a-121">If a wave is processed manually or automatically, as follows:</span></span>

  - <span data-ttu-id="7bb5a-122">**Обработка вручную** — строка добавляется в волну, запасы резервируются, однако необходимо выбрать **Обработать** на странице списка **Все полны**, чтобы создать работу комплектации для заказа.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-122">**Manual processing** – The line is added to a wave and the inventory is reserved, however, you must select **Process** on the **All waves** list page to create the picking work for the order.</span></span>
  - <span data-ttu-id="7bb5a-123">**Автоматическая обработка** — можно полностью или частично автоматизировать обработку волны.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-123">**Automatic processing** – You can fully or partially automate wave processing.</span></span> <span data-ttu-id="7bb5a-124">При полной автоматизации обработки волны создается волна, которая включает строку из заказа на продажу, производственного заказа или канбана при создании заказа на продажу, производственного заказа или канбана.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-124">If you fully-automate wave processing, a wave is created that includes the line from the sales order, production order, or kanban when a sales order, production order, or kanban is created.</span></span> <span data-ttu-id="7bb5a-125">Номенклатуры вычитаются из запасов в наличии, и создается работа комплектации.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-125">The items are deducted from on-hand inventory and the picking work is created.</span></span> <span data-ttu-id="7bb5a-126">При частичной автоматизации обработки волны можно указать значения, которые будут запускать обработку волны.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-126">If you partially automate wave processing, you can specify values that will trigger wave processing.</span></span> <span data-ttu-id="7bb5a-127">Например, можно указать максимальный вес отгрузок, достижение которого запустит обработку волны, если общий вес в строках волны достигнет этого значения.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-127">For example, you can specify a maximum weight for shipments that will trigger wave processing when the total weight of the lines in the wave reaches the value.</span></span>

- <span data-ttu-id="7bb5a-128">При назначении отгрузок открытой волне.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-128">If you assign shipments to an open wave.</span></span> <span data-ttu-id="7bb5a-129">Например, если пообещать клиентам, что заказ, размещенный до 12:00, будет отгружен в течение 24 часов, можно настроить шаблон волны таким образом, чтобы автоматически назначить строки заказа открытой волне до 12:00.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-129">For example, if you promise customers that an order placed by 12:00 PM will ship within 24 hours, you can set up the wave template to automatically assign order lines to an open wave until 12:00 PM.</span></span> <span data-ttu-id="7bb5a-130">В это время волна будет обрабатываться автоматически.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-130">At that time, the wave is automatically processed.</span></span>

<span data-ttu-id="7bb5a-131">При обработке волны создаваемая работа комплектации основывается на шаблоне работы и директиве местонахождения, которая определена для склада.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-131">When a wave is processed, the picking work that is created is based on the work template and the location directive that is specified for the warehouse.</span></span> <span data-ttu-id="7bb5a-132">Шаблон работы определяет способ создания работы комплектации, а директива местонахождения определяет местонахождения комплектации и размещения.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-132">The work template specifies how the picking work is created, and the location directive specifies the pick and put locations.</span></span>

## <a name="create-a-wave-template"></a><span data-ttu-id="7bb5a-133">Создание шаблона волны</span><span class="sxs-lookup"><span data-stu-id="7bb5a-133">Create a wave template</span></span>

<span data-ttu-id="7bb5a-134">Чтобы настроить шаблон волны, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-134">To set up a wave template, follow these steps:</span></span>

1. <span data-ttu-id="7bb5a-135">Перейдите в раздел **Управление складом** \> **Настройка** \> **Волны** \> **Шаблоны волны**.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-135">Go to **Warehouse management** \> **Setup** \> **Waves** \> **Wave templates**.</span></span>
1. <span data-ttu-id="7bb5a-136">Выберите **Создать** для создания нового шаблона волны.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-136">Select **New** to create a new wave template.</span></span>
1. <span data-ttu-id="7bb5a-137">В поле **Тип шаблона волны** выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="7bb5a-137">In the **Wave template type** field, select one of the following options:</span></span>

    - <span data-ttu-id="7bb5a-138">*Отгрузка* — используйте шаблон волны, чтобы отгрузить номенклатуры для заказов на продажу и заказов на перемещение.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-138">*Shipping* - Use the wave template for shipping items for sales orders and transfer orders.</span></span>
    - <span data-ttu-id="7bb5a-139">*Производственные заказы* — используйте шаблон волны, чтобы переместить номенклатуры для производственных заказов.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-139">*Production orders* - Use the wave template to move items for production orders.</span></span>
    - <span data-ttu-id="7bb5a-140">*Канбан* — используйте шаблон волны, чтобы переместить номенклатуры для заказов канбана.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-140">*Kanban* - Use the wave template to move items for kanban orders.</span></span>

1. <span data-ttu-id="7bb5a-141">В полях **Имя шаблона волны** и **Описание шаблона волны** введите имя и описание шаблона волны.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-141">In the **Wave template name** and **Wave template description** fields, enter a name and a description for the wave template.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7bb5a-142">Если для склада создано несколько шаблонов, номер в поле **Последовательность шаблонов волны** указывает положение шаблона в последовательности, в которой применяются шаблоны при соответствии критериям шаблона.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-142">If more than one template is created for a warehouse, the number in the **Wave template sequence** field indicates the position of the template in the sequence in which the templates are applied when the template’s criteria is met.</span></span> <span data-ttu-id="7bb5a-143">Можно выбрать **Переместить вверх** или **Переместить вниз**, чтобы изменить последовательность шаблонов.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-143">You can select **Move up** or **Move down** to rearrange the sequence of templates.</span></span>

1. <span data-ttu-id="7bb5a-144">В полях **Сайт** и **Склад** выберите сайт и склад, для которых шаблон волны создаст волны и работу комплектации.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-144">In the **Site** and **Warehouse** fields, select the site and warehouse that the wave template will create waves and picking work for.</span></span>
1. <span data-ttu-id="7bb5a-145">Если требуется автоматизировать обработку волны, внесите необходимые изменения в следующие настройки:</span><span class="sxs-lookup"><span data-stu-id="7bb5a-145">If you want to automate wave processing, make the following settings as needed:</span></span>

    - <span data-ttu-id="7bb5a-146">**Создавать волны автоматически** —установите для этого параметра значение *Да* для автоматического создания волны при выпуске заказа на продажу, производственного заказа или канбана на склад.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-146">**Automate wave creation** - Set this to *Yes* to automatically create a wave when a sales order, production order, or kanban is released to the warehouse.</span></span>
    - <span data-ttu-id="7bb5a-147">**Назначить открытым волнам** — установите для этого параметра значение *Да*, чтобы автоматически назначать строки открытой волне при выпуске строк.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-147">**Assign to open waves** - Set this to *Yes* to automatically assign lines to an open wave when the lines are released.</span></span> <span data-ttu-id="7bb5a-148">Строки назначаются волнам на основе фильтра запроса для шаблона волны.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-148">Lines are assigned to waves based on the query filter for the wave template.</span></span>
    - <span data-ttu-id="7bb5a-149">**Обрабатывать волну перед запуском на склад** — установите значение *Да*, чтобы автоматически обрабатывать волну и создавать работу, когда строка выпускается на склад.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-149">**Process wave at release to warehouse** - Set this to *Yes* to automatically process the wave and create work when a line is released to the warehouse.</span></span>
    - <span data-ttu-id="7bb5a-150">**Автоматически обрабатывать волну на пороге** — установите для этого параметра значение *Да* для автоматической обработки волны, когда ее значения достигают пороговых значений веса, отгрузки и строк, указанных в группе полей **Пороги волн**.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-150">**Process wave automatically at threshold** - Set this to *Yes* to automatically process the wave when its values reach the thresholds for weight, shipment, and lines specified in the **Wave thresholds** field group.</span></span> <span data-ttu-id="7bb5a-151">Этот параметр активен, только если в поле **Тип шаблона волны** выбрано значение *Отгрузка*.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-151">This setting is only active if *Shipping* is selected in the **Wave template type** field.</span></span>
    - <span data-ttu-id="7bb5a-152">**Автоматический запуск волны** — установите значение *Да*, чтобы автоматически выпускать волну.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-152">**Automate wave release** - Set this to *Yes* to automatically release the wave.</span></span> <span data-ttu-id="7bb5a-153">Работа комплектации создается и становится доступна на мобильных устройствах.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-153">The picking work is created and made available on mobile devices.</span></span>
    - <span data-ttu-id="7bb5a-154">**Автоматизировать выпуск работы пополнения** — установите этот параметр как *Да*, чтобы создать работу пополнения на основе запроса и автоматически запустить ее в производство.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-154">**Automate replenishment work release** - Set this to *Yes* to create demand-based replenishment work and release it automatically.</span></span> <span data-ttu-id="7bb5a-155">Необходимо добавить метод волны пополнения в шаблон волны и создать шаблон пополнения, используя тип *Спрос волны*.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-155">You must add the replenishment wave method to the wave template, and create a replenishment template using the *Wave demand* type.</span></span> <span data-ttu-id="7bb5a-156">Настройте шаблон пополнения на странице **Шаблоны пополнения**.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-156">Set up a replenishment template on the **Replenishment templates** page.</span></span> <span data-ttu-id="7bb5a-157">Для этого требуется добавить метод пополнения в шаблон волны.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-157">This requires that you add the replenish method to the wave template.</span></span>
    - <span data-ttu-id="7bb5a-158">**Продолжить обработку волны при сбое создания работы** — если для этого параметра задано значение *Да*, система будет использовать пустое местонахождение, если ей не удается зарезервировать запасы в местонахождении, предлагаемом директивой местонахождения (например из-за того, что запасов больше нет в наличии).</span><span class="sxs-lookup"><span data-stu-id="7bb5a-158">**Continue wave processing when work creation fails** - When set to *Yes*, the system will use a blank location if it can't reserve inventory at the location proposed by the location directive (for example, because the inventory is no longer available).</span></span> <span data-ttu-id="7bb5a-159">Если для этого параметра задано значение *Нет*, волна завершится сбоем, если системе не удается зарезервировать запасы.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-159">When set to *No*, the wave will fail if the system can't reserve the inventory.</span></span>

1. <span data-ttu-id="7bb5a-160">Установите необходимые значения для группы полей **Пороговые значения волны**:</span><span class="sxs-lookup"><span data-stu-id="7bb5a-160">Set the **Wave thresholds** field group as needed:</span></span>
    - <span data-ttu-id="7bb5a-161">**Пороговый вес волны** — введите максимальный вес, который может содержаться в волне.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-161">**Wave weight threshold** - Enter the maximum weight a wave can contain.</span></span>
    - <span data-ttu-id="7bb5a-162">**Порог отгрузки** — введите максимальное число отгрузок, которые могут быть включены в волну.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-162">**Shipment threshold** - Enter the maximum number of shipments that can be included in a wave.</span></span>
    - <span data-ttu-id="7bb5a-163">**Порог строк** — введите максимальное число строк, которые могут быть включены в волну.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-163">**Line threshold** - Enter the maximum number of lines that can be included in a wave.</span></span>

1. <span data-ttu-id="7bb5a-164">В группе полей **Значения по умолчанию** выберите атрибуты волны для использования в качестве дополнительных критериев шаблона волны.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-164">In the **Default values** field group, select the wave attributes to use as additional criteria for the wave template.</span></span> <span data-ttu-id="7bb5a-165">Атрибуты волны полезны при назначении дополнительных критериев, таких как имя клиента, шаблону волны.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-165">Wave attributes are useful for assigning additional criteria, such as a specific customer name, to a wave template.</span></span> <span data-ttu-id="7bb5a-166">Эти атрибуты создаются на странице **Атрибуты волны**.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-166">You create these attributes on the **Wave attributes** page.</span></span> 

1. <span data-ttu-id="7bb5a-167">Установите в поле **Политика уведомлений волны** политику, которую необходимо использовать для создания уведомлений, связанных с волнами, использующими этот шаблон.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-167">Set **Wave notification policy** to the policy you want to use for generating notifications related to waves that use this template.</span></span> <span data-ttu-id="7bb5a-168">Пример политики уведомлений волны см. в разделе [Уведомления о выполнении волн](wave-execution-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="7bb5a-168">For an example of a wave notification policy, see [Wave execution notifications](wave-execution-notifications.md).</span></span>

1. <span data-ttu-id="7bb5a-169">На экспресс-вкладке **Методы** в области **Выбранные методы** перечислены методы для выбранного шаблона волны.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-169">On the **Methods** FastTab, the **Selected methods** pane lists the methods for the selected wave template.</span></span> <span data-ttu-id="7bb5a-170">Методы волны выполняют действия, которые созданы шаблоном, например создание или распределение работы.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-170">The wave methods perform the actions that are created by the template, such creating or distributing work.</span></span> <span data-ttu-id="7bb5a-171">Эти действия также называются этапами волны.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-171">These actions are also referred to as wave steps.</span></span> <span data-ttu-id="7bb5a-172">Методы волн предопределены для каждого типа шаблона волны.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-172">Wave methods are predefined for each type of wave template.</span></span> <span data-ttu-id="7bb5a-173">Невозможно удалить предопределенные методы волны, однако можно изменить порядок методов и добавить дополнительные методы.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-173">You cannot remove the predefined wave methods, however, you can rearrange the order of the methods and add additional methods.</span></span> <span data-ttu-id="7bb5a-174">Например, при создании шаблона волны для отгрузки можно добавить методы для пополнения и контейнеризации.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-174">For example, if you’re creating a wave template for shipping, you can add methods for replenishment and containerization.</span></span> <span data-ttu-id="7bb5a-175">Контейнеризацию волны можно добавить в последовательность методов волны, чтобы определить контейнеризацию строк, обрабатываемых в шаблоне волны.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-175">Wave containerization can be added to a sequence of wave methods to define the containerization of the lines processed in a wave template.</span></span> <span data-ttu-id="7bb5a-176">Чтобы добавить дополнительный метод, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-176">To add an additional method, do the following:</span></span>

    - <span data-ttu-id="7bb5a-177">Выберите метод в области **Остальные методы**, затем выберите стрелку **Влево**, чтобы добавить его в область **Выбранные методы**.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-177">Select a method on the **Remaining methods** pane, and then select the **Left** arrow to add it to the **Selected methods** pane.</span></span>
    - <span data-ttu-id="7bb5a-178">Чтобы изменить последовательность, выберите метод и выберите стрелку **Вверх** или **Вниз**.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-178">To change the sequence, select a method, and then select **Up** or **Down** arrows.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7bb5a-179">При добавлении метода он автоматически указывается в соответствующем местоположении в последовательности этапов.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-179">When you add a method, it’s automatically listed in the appropriate location in the sequence of steps.</span></span>

1. <span data-ttu-id="7bb5a-180">Чтобы настроить запрос, который будет сопоставлять выпущенные строки с соответствующей волной, выберите **Изменить запрос** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-180">To set up the query that will match released lines to an appropriate wave, select **Edit query** on the Action Pane.</span></span>
1. <span data-ttu-id="7bb5a-181">Чтобы проверить правильность параметров шаблона волны, выберите **Проверить шаблон**.</span><span class="sxs-lookup"><span data-stu-id="7bb5a-181">To verify that the wave template settings are valid, select **Validate template**.</span></span>