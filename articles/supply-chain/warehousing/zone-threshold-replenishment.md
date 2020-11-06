---
title: Пополнение порога зоны
description: При пополнении на основе зон используется стратегия минимального/максимального пополнения (мин/макс), но она оценивает все складские зоны, а не только отдельные ячейки. Таким образом, менеджеры склада могут быстрее узнать, когда в зоне комплектации требуются дополнительные запасы.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e13b5fd895fca7f8fe77809348d63ed8867dea9e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017330"
---
# <a name="zone-threshold-replenishment"></a><span data-ttu-id="9bf0b-104">Пополнение порога зоны</span><span class="sxs-lookup"><span data-stu-id="9bf0b-104">Zone threshold replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9bf0b-105">При пополнении на основе зон используется стратегия минимального/максимального [пополнения](replenishment.md) (мин/макс), но она оценивает все складские зоны, а не только отдельные ячейки.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-105">Zone-based replenishment uses a minimum/maximum (min/max) [replenishment](replenishment.md) strategy, but it evaluates whole warehouse zones instead of just individual locations.</span></span> <span data-ttu-id="9bf0b-106">Таким образом, менеджеры склада могут быстрее узнать, когда в зоне комплектации требуются дополнительные запасы.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-106">Therefore, warehouse managers can more quickly learn when additional inventory is required in a picking zone.</span></span>

<span data-ttu-id="9bf0b-107">Настройка для этого компонента напоминает настройку для пополнения на основе местоположения.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-107">The setup for this feature resembles the setup for location-based replenishment.</span></span> <span data-ttu-id="9bf0b-108">Однако при настройке шаблона для пополнения мин./макс. можно также указать, следует ли оценивать пороговое значение для каждого местоположения или для каждой зоны.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-108">However, when you set up a template for min/max replenishment, you can also specify whether the threshold should be evaluated per location or per zone.</span></span> <span data-ttu-id="9bf0b-109">Если настроена оценка на основе зон, необходимо добавить отдельные зоны в запрос выбора зоны.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-109">If you set up evaluation that is based on zones, you must add specific zones to the zone selection query.</span></span>

<span data-ttu-id="9bf0b-110">Как и минимальное/максимальное пополнение на основе местоположения, минимальное/максимальное пополнение на основе зоны основано на настройке минимального порогового значения запасов, которое запускает создание работы пополнения для выбранных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-110">Like location-based min/max replenishment, zone-based min/max replenishment is based the setup of a minimum inventory threshold that triggers the creation of replenishment work for selected items.</span></span> <span data-ttu-id="9bf0b-111">Эта работа пополнения приведет к увеличению запаса до указанного максимального порога для зоны.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-111">This replenishment work will increase inventory up to the specified maximum threshold for the zone.</span></span>

> [!NOTE]
> <span data-ttu-id="9bf0b-112">Процессы пополнения зоны для вариантов продукта не поддерживаются в текущем выпуске.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-112">Zone replenishment processes for product variants aren't supported in the current release.</span></span>


<span data-ttu-id="9bf0b-113">В отличие от минимального/максимального пополнения на основе местоположения, минимальное/максимальное пополнение на основе зоны не требует наличия фиксированных местоположений для оценки необходимости хранения определенной номенклатуры в местоположениях.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-113">Unlike location-based min/max replenishment, zone-based min/max replenishment doesn't require fixed locations to evaluate whether locations should store a specific item.</span></span> <span data-ttu-id="9bf0b-114">Таким образом, пополнение на основе зон позволяет использовать минимальное/максимальное пополнение, даже если отсутствуют фиксированные местонахождения для каждой номенклатуры или варианта номенклатуры на складе.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-114">Therefore, zone-based replenishment lets you use min/max replenishment even if you don't have fixed locations for each item or item variant in the warehouse.</span></span> <span data-ttu-id="9bf0b-115">Если количество в зоне падает ниже указанного минимального значения, создается работа по пополнению запасов.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-115">When a quantity in the zone falls below the specified minimum threshold, replenishment work is created.</span></span> <span data-ttu-id="9bf0b-116">Директивы местоположения определяют, в какое конкретное местоположение следует поместить запасы.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-116">Location directives will determine which specific location the inventory should be put into.</span></span>

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a><span data-ttu-id="9bf0b-117">Включение функции пополнения порога зоны</span><span class="sxs-lookup"><span data-stu-id="9bf0b-117">Turn on the Zone threshold replenishment feature</span></span>

<span data-ttu-id="9bf0b-118">Прежде чем использовать функцию *Пополнение порога зоны* , она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-118">Before you can use the *Zone threshold replenishment* feature, it must be turned on in your system.</span></span> <span data-ttu-id="9bf0b-119">Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-119">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="9bf0b-120">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="9bf0b-120">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="9bf0b-121">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="9bf0b-121">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="9bf0b-122">**Имя функции:** *Пополнения порога зоны*</span><span class="sxs-lookup"><span data-stu-id="9bf0b-122">**Feature name:** *Zone threshold replenishment*</span></span>

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a><span data-ttu-id="9bf0b-123">Настройка пополнения на основе зон</span><span class="sxs-lookup"><span data-stu-id="9bf0b-123">Set up zone-based replenishment</span></span>

<span data-ttu-id="9bf0b-124">Чтобы настроить пополнение на основе зон, необходимо настроить несколько частей системы.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-124">To set up zone-based replenishment, you must configure several parts of the system.</span></span> <span data-ttu-id="9bf0b-125">В этом разделе описываются различные параметры и предоставляются значения демонстрационных данных, которые можно ввести, если вы хотите выполнить действия по сценарию в конце этого раздела.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-125">This section introduces the various settings and provides demo data values that you can enter if you want to work through the scenario at the end of this topic.</span></span>

### <a name="set-up-directive-codes"></a><span data-ttu-id="9bf0b-126">Настройка кодов директив</span><span class="sxs-lookup"><span data-stu-id="9bf0b-126">Set up directive codes</span></span>

<span data-ttu-id="9bf0b-127">[Коды директив](control-warehouse-location-directives.md) позволяют более подробно определить шаблон местоположения, используемый в шаблоне работы.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-127">[Directive codes](control-warehouse-location-directives.md) let you be more specific when you define the location template that is used in a work template.</span></span> <span data-ttu-id="9bf0b-128">Каждый код определяет общее значение, на которое можно ссылаться при настройке каждого типа шаблона.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-128">Each code establishes a common value that you can refer to when you configure each type of template.</span></span>

#### <a name="view-and-edit-directive-codes"></a><span data-ttu-id="9bf0b-129">Просмотр и редактирование кодов директив</span><span class="sxs-lookup"><span data-stu-id="9bf0b-129">View and edit directive codes</span></span>

<span data-ttu-id="9bf0b-130">Чтобы просмотреть или изменить коды директив, перейдите к пункту **Управление складом \> Настройка \> Коды директив**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-130">To view or edit your directive codes, go to **Warehouse management \> Setup \> Directive codes**.</span></span>

#### <a name="prepare-demo-data-directive-codes"></a><span data-ttu-id="9bf0b-131">Подготовка кодов директив демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="9bf0b-131">Prepare demo data directive codes</span></span>

<span data-ttu-id="9bf0b-132">В этом примере показано, как подготовить код директивы.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-132">This example shows how to prepare a directive code.</span></span> <span data-ttu-id="9bf0b-133">Если планируется работа со сценарием в конце этого раздела, используйте приведенные здесь значения демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-133">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="9bf0b-134">В противном случае используйте собственные значения.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-134">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="9bf0b-135">Выберите юридическое лицо **USMF** для работы с демонстрационными данными.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-135">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="9bf0b-136">Перейдите в раздел **Управление складом \> Настройка \> Коды директив**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-136">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="9bf0b-137">На панели операций выберите **Создать** , чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="9bf0b-138">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9bf0b-138">In the new row, set the following values:</span></span>

    - <span data-ttu-id="9bf0b-139">**Код директивы:** _Пополнение зоны_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-139">**Directive code:** _Zone replen_</span></span>
    - <span data-ttu-id="9bf0b-140">**Описание директивы:** _Пополнение зоны_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-140">**Directive description:** _Zone replenishment_</span></span>

1. <span data-ttu-id="9bf0b-141">Выберите **Сохранить** , чтобы сохранить новый код.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-141">Select **Save** to save the new code.</span></span>

### <a name="set-up-replenishment-templates"></a><span data-ttu-id="9bf0b-142">Настроить шаблоны пополнения</span><span class="sxs-lookup"><span data-stu-id="9bf0b-142">Set up replenishment templates</span></span>

<span data-ttu-id="9bf0b-143">[Шаблоны пополнения, основанного на минимальном и максимальном количествах](tasks/set-up-min-max-replenishment-process.md), являются основным механизмом для поддержания оптимального уровня в ячейках комплектации.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-143">[Min/max replenishment templates](tasks/set-up-min-max-replenishment-process.md) are the primary mechanism for maintaining optimal levels in picking locations.</span></span> <span data-ttu-id="9bf0b-144">В этих шаблонах необходимо настроить правила, которые будут использоваться для пополнения запасов на складе.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-144">In these templates, you must set up the rules that will be used to replenish inventory in the warehouse.</span></span> <span data-ttu-id="9bf0b-145">Пополнение, для которого можно использовать шаблоны, включает пополнение на основе зон.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-145">The replenishment that the templates can be used for includes zone-based replenishment.</span></span>

#### <a name="view-and-edit-replenishment-templates"></a><span data-ttu-id="9bf0b-146">Просмотр и редактирование шаблонов пополнения</span><span class="sxs-lookup"><span data-stu-id="9bf0b-146">View and edit replenishment templates</span></span>

<span data-ttu-id="9bf0b-147">Шаблон пополнения — это набор правил, определяющих когда и как пополняются местонахождения.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-147">A replenishment template is a set of rules that control when and how a location is replenished.</span></span> <span data-ttu-id="9bf0b-148">Следует выбрать шаблон, определяющий, когда и как выполняется пополнение.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-148">You select a template to control when and how replenishment is done.</span></span> <span data-ttu-id="9bf0b-149">Для просмотра или редактирования шаблонов пополнения перейдите в раздел **Управление складом \> Настройка \> Пополнение \> Шаблоны пополнения**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-149">To view or edit your replenishment templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>

#### <a name="prepare-a-demo-data-replenishment-template"></a><span data-ttu-id="9bf0b-150">Подготовка шаблона пополнения для демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="9bf0b-150">Prepare a demo data replenishment template</span></span>

<span data-ttu-id="9bf0b-151">В этом примере показано, как подготовить шаблон пополнения.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-151">This example shows how to prepare a replenishment template.</span></span> <span data-ttu-id="9bf0b-152">Если планируется работа со сценарием в конце этого раздела, используйте приведенные здесь значения демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-152">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="9bf0b-153">В противном случае используйте собственные значения.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-153">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="9bf0b-154">Выберите юридическое лицо **USMF** для работы с демонстрационными данными.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-154">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="9bf0b-155">Перейдите в раздел **Управление складом \> Настройка \> Пополнение \> Шаблоны пополнения**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-155">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="9bf0b-156">Выберите **Правка** , чтобы перевести страницу в режим редактирования.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-156">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="9bf0b-157">На панели операций выберите **Создать** , чтобы добавить строку в сетку **Обзор**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-157">On the Action Pane, select **New** to add a row to the **Overview** grid.</span></span>
1. <span data-ttu-id="9bf0b-158">В новой строке установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-158">In the new row, set the following values.</span></span> <span data-ttu-id="9bf0b-159">Примите для всех остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-159">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="9bf0b-160">**Шаблон пополнения:** _Пополнение зоны мин/макс_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-160">**Replenish template:** _Zone min/max replen_</span></span>
    - <span data-ttu-id="9bf0b-161">**Описание:** _Пополнение зоны на основе минимального и максимального значения_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-161">**Description:** _Zone min/max replenishment_</span></span>
    - <span data-ttu-id="9bf0b-162">**Тип пополнения:** _Минимум или максимум_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-162">**Replenishment type:** _Minimum or maximum_</span></span>

1. <span data-ttu-id="9bf0b-163">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-163">Select **Save**.</span></span>
1. <span data-ttu-id="9bf0b-164">Пока новая строка все еще выбрана в сетке **Обзор** , выберите **Создать** выше сетки **Сведения о шаблоне пополнения** , чтобы добавить строку, связанную с шаблоном пополнения *Пополнение зоны мин/макс* , который только что был создан.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-164">While the new row is still selected in the **Overview** grid, select **New** above the **Replenishment Template Details** grid to add a row that is associated with the *Zone Min/Max replen* replenishment template that you just created.</span></span>
1. <span data-ttu-id="9bf0b-165">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9bf0b-165">In the new row, set the following values:</span></span>

    - <span data-ttu-id="9bf0b-166">**Порядковый номер:** введите _1_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-166">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="9bf0b-167">**Описание:** введите _Пополнение зоны комплектации_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-167">**Description:** Enter _Pick zone replenishment_.</span></span>
    - <span data-ttu-id="9bf0b-168">**Единица пополнения:** выберите _шт._</span><span class="sxs-lookup"><span data-stu-id="9bf0b-168">**Replenishment unit:** Select _ea_.</span></span>
    - <span data-ttu-id="9bf0b-169">**Тип запроса:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-169">**Request type:** Leave this field blank.</span></span>
    - <span data-ttu-id="9bf0b-170">**Код директивы:** это поле связывает шаблон пополнения с директивой местонахождения.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-170">**Directive code:** This field links the replenishment template with a location directive.</span></span> <span data-ttu-id="9bf0b-171">Выберите код директивы для демонстрационных данных, созданной ранее ( _Пополнение зоны_ ).</span><span class="sxs-lookup"><span data-stu-id="9bf0b-171">Select the demo data directive code that you created earlier ( _Zone replen_ ).</span></span>
    - <span data-ttu-id="9bf0b-172">**Шаблон работы:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-172">**Work template:** Leave this field blank.</span></span>
    - <span data-ttu-id="9bf0b-173">**Минимальное количество:** это поле определяет количество, при котором будет запускаться пополнение.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-173">**Minimum quantity:** This field sets the quantity that replenishment will be triggered at.</span></span> <span data-ttu-id="9bf0b-174">Введите _50_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-174">Enter _50_.</span></span>
    - <span data-ttu-id="9bf0b-175">**Максимальное количество:** в этом поле задается максимальное количество номенклатуры, которое может присутствовать в зоне.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-175">**Maximum quantity:** This field sets the maximum quantity of an item that can be present in a zone.</span></span> <span data-ttu-id="9bf0b-176">Созданная работа по пополнению увеличит запасы до этого количества.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-176">Generated replenishment work will increase inventory to this quantity.</span></span> <span data-ttu-id="9bf0b-177">Введите _150_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-177">Enter _150_.</span></span>
    - <span data-ttu-id="9bf0b-178">**Единица измерения:** это поле определяет единицу измерения для минимального и максимального значений.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-178">**Unit:** This field sets the unit for the minimum and maximum values.</span></span> <span data-ttu-id="9bf0b-179">Выберите _шт._</span><span class="sxs-lookup"><span data-stu-id="9bf0b-179">Select _ea_.</span></span>
    - <span data-ttu-id="9bf0b-180">**Приращение спроса:** выберите _Округление вверх_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-180">**Demand increment:** Select _Round up_.</span></span>
    - <span data-ttu-id="9bf0b-181">**Пополнять пустые фиксированные местонахождения:** установите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-181">**Replenish empty fixed locations:** Select this check box.</span></span>
    - <span data-ttu-id="9bf0b-182">**Пополнять только фиксированные местонахождения:** снимите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-182">**Replenish only fixed locations:** Clear this check box.</span></span>
    - <span data-ttu-id="9bf0b-183">**Режим запроса продукта:** выберите _Запрос продукта_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-183">**Product query mode:** Select _Product query_.</span></span>
    - <span data-ttu-id="9bf0b-184">**Область порога пополнения:** это поле определяет, должен ли шаблон оцениваться по зоне или по определенному местонахождению.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-184">**Replenishment threshold scope:** This field defines whether the template should evaluate by zone or by specific location.</span></span> <span data-ttu-id="9bf0b-185">Выберите _Зона_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-185">Select _Zone_.</span></span>
    - <span data-ttu-id="9bf0b-186">**Склад:** выберите _61_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-186">**Warehouse:** Select _61_.</span></span>

1. <span data-ttu-id="9bf0b-187">Выберите **Выбрать продукты** над сеткой **Сведения шаблона пополнения**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-187">Select **Select products** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="9bf0b-188">В диалоговом окне **Запрос продукта** на вкладке **Диапазон** выберите **Добавить** , чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-188">In the **Product query** dialog box, on the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="9bf0b-189">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9bf0b-189">In the new row, set the following values:</span></span>

    - <span data-ttu-id="9bf0b-190">**Таблица:** _Номенклатуры_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-190">**Table:** _Items_</span></span>
    - <span data-ttu-id="9bf0b-191">**Производная таблица:** _Номенклатуры_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-191">**Derived table:** _Items_</span></span>
    - <span data-ttu-id="9bf0b-192">**Поле:** _Код номенклатуры_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-192">**Field:** _Item number_</span></span>
    - <span data-ttu-id="9bf0b-193">**Критерии:** _A0001_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-193">**Criteria:** _A0001_</span></span>

1. <span data-ttu-id="9bf0b-194">Выберите **OK** , чтобы сохранить ваш запрос и закрыть это диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-194">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="9bf0b-195">Выберите **Выбрать зоны для пополнения** над сеткой **Сведения шаблона пополнения**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-195">Select **Select zones to replenish** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="9bf0b-196">В диалоговом окне **Запрос зоны** на вкладке **Диапазон** добавьте строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-196">In the **Zone query** dialog box, on the **Range** tab, add a row to the grid.</span></span>
1. <span data-ttu-id="9bf0b-197">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9bf0b-197">In the new row, set the following values:</span></span>

    - <span data-ttu-id="9bf0b-198">**Таблица:** _Зона склада_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-198">**Table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="9bf0b-199">**Производная таблица:** _Зона склада_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-199">**Derived table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="9bf0b-200">**Поле:** _Код зоны_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-200">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="9bf0b-201">**Критерии:** _ЭТАЖ_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-201">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="9bf0b-202">Выберите **OK** , чтобы сохранить ваш запрос и закрыть это диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-202">Select **OK** to save your query and close the dialog box.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="9bf0b-203">Настройка директив для места хранения</span><span class="sxs-lookup"><span data-stu-id="9bf0b-203">Set up location directives</span></span>

<span data-ttu-id="9bf0b-204">В отличие от пополнения мин./макс. на основе местонахождения, пополнение мин./макс. на основе зон требует, чтобы были настроены как директивы местонахождения комплектации, так и директивы местонахождения размещения, поскольку система оценивает всю зону вместо выбора только местоположения комплектации для исходящих работ.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-204">Unlike location-based min/max replenishment, zone-based min/max replenishment requires that you set up both pick location directives and put location directives, because the system evaluates the whole zone instead of just the pick location for outbound work.</span></span>

#### <a name="view-and-edit-location-directives"></a><span data-ttu-id="9bf0b-205">Просмотр и редактирование директив местоположения</span><span class="sxs-lookup"><span data-stu-id="9bf0b-205">View and edit location directives</span></span>

<span data-ttu-id="9bf0b-206">Чтобы просмотреть или изменить директивы местоположения, перейдите к пункту **Управление складом \> Настройка \> Директивы для мест хранения**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-206">To view or edit your location directives, go to **Warehouse management \> Setup \> Location directives**.</span></span>

<span data-ttu-id="9bf0b-207">Примеры, демонстрирующие использование настроек для создания требуемых директив местоположения комплектации и директив местоположения размещения см. в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-207">For examples that show how to use the settings to create the required pick location directives and put location directives, see the next section.</span></span>

#### <a name="prepare-demo-data-location-directives"></a><span data-ttu-id="9bf0b-208">Подготовка директив местонахождения для демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="9bf0b-208">Prepare demo data location directives</span></span>

<span data-ttu-id="9bf0b-209">Для подготовки демонстрационных данных, чтобы их можно было использовать в сценарии в конце данного раздела, необходимо создать две директивы местоположения: одну для комплектации и одну для размещения.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-209">To prepare demo data so that it can be used in the scenario at the end of this topic, you must create two location directives: one for pick and one for put.</span></span>

##### <a name="create-a-replenishment-pick-directive"></a><span data-ttu-id="9bf0b-210">Создание директивы комплектации пополнения</span><span class="sxs-lookup"><span data-stu-id="9bf0b-210">Create a replenishment pick directive</span></span>

1. <span data-ttu-id="9bf0b-211">Выберите юридическое лицо **USMF** для работы с демонстрационными данными.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-211">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="9bf0b-212">Перейдите в раздел **Управление складом \> Настройка \> Директивы местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-212">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="9bf0b-213">В левой панели задайте в поле **Тип заказа на работу** значение _Пополнение_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-213">In the left pane, set the **Work order type** field to _Replenishment_.</span></span>
1. <span data-ttu-id="9bf0b-214">На панели операций выберите **Создать** для создания новой директивы.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-214">On the Action Pane, select **New** to create a new directive.</span></span>
1. <span data-ttu-id="9bf0b-215">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9bf0b-215">Set the following values:</span></span>

    - <span data-ttu-id="9bf0b-216">**Порядковый номер:** примите значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-216">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="9bf0b-217">**Имя:** введите _Зона комплектация_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-217">**Name:** Enter _Zone pick_.</span></span>
    - <span data-ttu-id="9bf0b-218">**Тип работы:** выберите _Комплектация_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-218">**Work type:** Select _Pick_.</span></span>
    - <span data-ttu-id="9bf0b-219">**Сайт:** выберите _6_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-219">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="9bf0b-220">**Склад:** выберите _61_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-220">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="9bf0b-221">**Код директивы:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-221">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="9bf0b-222">**Несколько SKU:** для этого параметра установите значение _Нет_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-222">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="9bf0b-223">Выберите **Сохранить** для создания директивы, имеющей настройки, заданные на данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-223">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="9bf0b-224">На экспресс-вкладке **Строки** выберите **Создать** , чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-224">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="9bf0b-225">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9bf0b-225">On the new line, set the following values:</span></span>

    - <span data-ttu-id="9bf0b-226">**Порядковый номер:** введите _1_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-226">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="9bf0b-227">**Количество "От":** введите _0_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-227">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="9bf0b-228">**Количество "До":** введите _10000000_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-228">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="9bf0b-229">**Единица измерения:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-229">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="9bf0b-230">**Найти количество:** выберите _Нет_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-230">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="9bf0b-231">**Ограничить по единице:** снимите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-231">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="9bf0b-232">**Округлить в большую сторону до единицы измерения:** снимите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-232">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="9bf0b-233">**Найти упакованное количество:** снимите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-233">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="9bf0b-234">**Разрешить разделение:** выберите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-234">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="9bf0b-235">Выберите **Сохранить** , чтобы сохранить новую строку.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-235">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="9bf0b-236">Пока новая строка все еще выбрана, в сетке **Строки** выберите **Создать** на экспресс-вкладке **Действия директивы местоположения** , чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-236">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="9bf0b-237">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9bf0b-237">In the new row, set the following values:</span></span>

    - <span data-ttu-id="9bf0b-238">**Порядковый номер:** введите _1_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-238">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="9bf0b-239">**Имя:** введите _Комплектация из нефасованной_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-239">**Name:** Enter _Pick from bulk_.</span></span>
    - <span data-ttu-id="9bf0b-240">**Использование фиксированного местоположения:** выберите _Фиксированные и нефиксированные местонахождения_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-240">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="9bf0b-241">**Разрешить отрицательные запасы:** снимите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-241">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="9bf0b-242">**Пакетная обработка активирована:** снять этот флажок.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-242">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="9bf0b-243">**Стратегия:** выберите _Нет_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-243">**Strategy:** Select _None_.</span></span>

1. <span data-ttu-id="9bf0b-244">Выберите **Сохранить** , чтобы сохранить новое действие.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-244">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="9bf0b-245">Пока ваше новое действие все еще выбрано, выберите **Изменить запрос** над сеткой **Действия директивы для места хранения**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-245">While your new action still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="9bf0b-246">Отображается диалоговое окно запроса, в котором можно выбрать местонахождения, из которых выполняется пополнение.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-246">A query dialog box appears, where you can select the locations to replenish from.</span></span> <span data-ttu-id="9bf0b-247">На вкладке **Диапазон** выберите **Добавить** , чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-247">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="9bf0b-248">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9bf0b-248">In the new row, set the following values:</span></span>

    - <span data-ttu-id="9bf0b-249">**Таблица:** _Местонахождения_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-249">**Table:** _Locations_</span></span>
    - <span data-ttu-id="9bf0b-250">**Производная таблица:** _Местонахождения_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-250">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="9bf0b-251">**Поле:** _Код зоны_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-251">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="9bf0b-252">**Критерии:** _BULK_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-252">**Criteria:** _BULK_</span></span>

1. <span data-ttu-id="9bf0b-253">Выберите **OK** , чтобы сохранить ваш запрос и закрыть это диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-253">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="9bf0b-254">Для сохранения директивы местонахождения выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-254">Select **Save** to save your location directive.</span></span>

##### <a name="create-a-replenishment-put-directive"></a><span data-ttu-id="9bf0b-255">Создание директивы размещения пополнения</span><span class="sxs-lookup"><span data-stu-id="9bf0b-255">Create a replenishment put directive</span></span>

1. <span data-ttu-id="9bf0b-256">На странице **Директивы для мест хранения** в левой области убедитесь, что в поле **Тип заказа на работу** все еще установлено значение _Пополнение_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-256">On the **Location directives** page, in the left pane, make sure that the **Work order type** field is still set to _Replenishment_.</span></span>
1. <span data-ttu-id="9bf0b-257">На панели операций выберите **Создать** для создания другой новой директивы.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-257">On the Action Pane, select **New** to create another new directive.</span></span>
1. <span data-ttu-id="9bf0b-258">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9bf0b-258">Set the following values:</span></span>

    - <span data-ttu-id="9bf0b-259">**Порядковый номер:** примите значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-259">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="9bf0b-260">**Имя:** введите _Зона размещения_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-260">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="9bf0b-261">**Тип заказа на работу:** выберите _Размещение_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-261">**Work order type:** Select _Put_.</span></span>
    - <span data-ttu-id="9bf0b-262">**Сайт:** выберите _6_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-262">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="9bf0b-263">**Склад:** выберите _61_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-263">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="9bf0b-264">**Код директивы:** выберите _Зона пополнения_ , чтобы связать эту директиву места хранения с шаблоном пополнения, созданным ранее с помощью ранее созданного кода.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-264">**Directive code:** Select _Zone replen_ to link this location directive with the replenishment template that you created earlier by using the code that you created earlier.</span></span>
    - <span data-ttu-id="9bf0b-265">**Несколько SKU:** для этого параметра установите значение _Нет_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-265">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="9bf0b-266">Выберите **Сохранить** для создания директивы, имеющей настройки, заданные на данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-266">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="9bf0b-267">На экспресс-вкладке **Строки** выберите **Создать** , чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-267">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="9bf0b-268">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9bf0b-268">On the new line, set the following values:</span></span>

    - <span data-ttu-id="9bf0b-269">**Порядковый номер:** введите _1_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-269">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="9bf0b-270">**Количество "От":** введите _0_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-270">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="9bf0b-271">**Количество "До":** введите _10000000_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-271">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="9bf0b-272">**Единица измерения:** оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-272">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="9bf0b-273">**Найти количество:** выберите _Нет_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-273">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="9bf0b-274">**Ограничить по единице:** снимите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-274">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="9bf0b-275">**Округлить в большую сторону до единицы измерения:** снимите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-275">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="9bf0b-276">**Найти упакованное количество:** снимите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-276">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="9bf0b-277">**Разрешить разделение:** выберите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-277">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="9bf0b-278">Выберите **Сохранить** , чтобы сохранить новую строку.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-278">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="9bf0b-279">Пока новая строка все еще выбрана, в сетке **Строки** выберите **Создать** на экспресс-вкладке **Действия директивы местоположения** , чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-279">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="9bf0b-280">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9bf0b-280">In the new row, set the following values:</span></span>

    - <span data-ttu-id="9bf0b-281">**Порядковый номер:** введите _1_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-281">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="9bf0b-282">**Имя:** введите _Зона размещения_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-282">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="9bf0b-283">**Использование фиксированного местоположения:** выберите _Фиксированные и нефиксированные местонахождения_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-283">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="9bf0b-284">**Разрешить отрицательные запасы:** снимите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-284">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="9bf0b-285">**Пакетная обработка активирована:** снять этот флажок.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-285">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="9bf0b-286">**Стратегия:** выберите _Консолидировать_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-286">**Strategy:** Select _Consolidate_.</span></span>

1. <span data-ttu-id="9bf0b-287">Выберите **Сохранить** , чтобы сохранить новое действие.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-287">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="9bf0b-288">Пока ваше новое действие все еще выбрано, выберите **Изменить запрос** над сеткой **Действия директивы для места хранения**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-288">While your new action is still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="9bf0b-289">Отображается диалоговое окно запроса, в котором можно выбрать зону, которую требуется пополнить.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-289">A query dialog box appears, where you can select the zone to replenish to.</span></span> <span data-ttu-id="9bf0b-290">Эта зона должна быть той зоной, которая указана в шаблоне пополнения.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-290">This zone should be the same zone that is specified in the replenishment template.</span></span> <span data-ttu-id="9bf0b-291">На вкладке **Диапазон** выберите **Добавить** , чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-291">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="9bf0b-292">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9bf0b-292">In the new row, set the following values:</span></span>

    - <span data-ttu-id="9bf0b-293">**Таблица:** _Местонахождения_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-293">**Table:** _Locations_</span></span>
    - <span data-ttu-id="9bf0b-294">**Производная таблица:** _Местонахождения_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-294">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="9bf0b-295">**Поле:** _Код зоны_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-295">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="9bf0b-296">**Критерии:** _ЭТАЖ_</span><span class="sxs-lookup"><span data-stu-id="9bf0b-296">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="9bf0b-297">Выберите **OK** , чтобы сохранить ваш запрос и закрыть это диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-297">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="9bf0b-298">Для сохранения директивы местонахождения выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-298">Select **Save** to save your location directive.</span></span>

## <a name="scenario"></a><span data-ttu-id="9bf0b-299">Сценарий</span><span class="sxs-lookup"><span data-stu-id="9bf0b-299">Scenario</span></span>

<span data-ttu-id="9bf0b-300">В этом разделе представлен пример сценария, в котором показано, как работать с этой функцией.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-300">This section provides a sample scenario that shows how to work with the feature.</span></span>

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a><span data-ttu-id="9bf0b-301">Подготовка образца данных, необходимого для примера сценария</span><span class="sxs-lookup"><span data-stu-id="9bf0b-301">Prepare the sample data that is required for the sample scenario</span></span>

<span data-ttu-id="9bf0b-302">Перед началом работы со сценарием необходимо активировать примеры данных и настроить функцию, как описано в этом разделе и в предыдущих разделах этой темы.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-302">Before you start to work through the scenario, you must activate sample data and set up the feature as described in this section and in the previous sections of this topic.</span></span>

#### <a name="use-the-usmf-legal-entity"></a><span data-ttu-id="9bf0b-303">Использование юридического лица USMF</span><span class="sxs-lookup"><span data-stu-id="9bf0b-303">Use the USMF legal entity</span></span>

<span data-ttu-id="9bf0b-304">Для работы с этим сценарием с помощью образцов записей и значений, указанных здесь, необходимо использовать систему, в которой установлены стандартные [демонстрационные данные](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="9bf0b-304">To work through the scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="9bf0b-305">Дополнительно перед началом необходимо выбрать юридическое лицо **USMF**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-305">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="prepare-additional-sample-data"></a><span data-ttu-id="9bf0b-306">Подготовка дополнительных демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="9bf0b-306">Prepare additional sample data</span></span>

<span data-ttu-id="9bf0b-307">После того , как вы выбрали юридическое лицо **USMF** , добавьте необходимые дополнительные демонстрационные данные, как описано в разделе [Настройка пополнения на основе зон](#setup) ранее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-307">After you've selected the **USMF** legal entity, add the additional sample data that is required, as described in the [Set up zone-based replenishment](#setup) section earlier in this topic.</span></span>

#### <a name="check-your-on-hand-inventory"></a><span data-ttu-id="9bf0b-308">Проверка запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="9bf0b-308">Check your on-hand inventory</span></span>

<span data-ttu-id="9bf0b-309">Выполните следующие действия, чтобы убедиться, что система содержит достаточное количество запасов для поддержки образца сценария.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-309">Follow these steps to make sure that your system includes enough inventory to support the sample scenario.</span></span>

1. <span data-ttu-id="9bf0b-310">Убедитесь, что имеются запасы в наличии для номенклатуры *A0001* в двух разных местах хранения в зоне комплектации ( *ЭТАЖ* ), указанной в шаблоне пополнения.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-310">Make sure that there is on-hand inventory for item *A0001* at two different locations in the pick zone ( *FLOOR* ) that is specified in the replenishment template.</span></span> <span data-ttu-id="9bf0b-311">Однако итоговые запасы должны быть меньше необходимого минимального количества ( *50* ), указанного в шаблоне пополнения.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-311">However, the total inventory should be less than the required minimum quantity ( *50* ) that is specified on the replenishment template.</span></span> <span data-ttu-id="9bf0b-312">Таким образом можно смоделировать, как выполняется расчет для всей зоны, а не только для одного местонахождения.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-312">In this way, you can simulate how the calculation occurs for the whole zone instead of just for a single location.</span></span> <span data-ttu-id="9bf0b-313">**Для коррекции запасов при необходимости можно использовать любые складские процессы.**</span><span class="sxs-lookup"><span data-stu-id="9bf0b-313">**Use any of the warehouse processes to adjust inventory as required.**</span></span>
1. <span data-ttu-id="9bf0b-314">Убедитесь, что имеется достаточное количество запасов для номенклатуры *A0001* в сборном месте хранения, которое указано в директиве места хранения зоны комплектации, в которой работа пополнения должна комплектовать номенклатуры из кода зоны *СБОРНАЯ*.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-314">Make sure that there is enough inventory for item *A0001* at a bulk location that is specified in the zone pick location directive where the replenishment work should pick the items from zone ID *BULK*.</span></span> <span data-ttu-id="9bf0b-315">Итоговые запасы должны быть больше необходимого максимального количества ( *150* ), указанного в шаблоне пополнения.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-315">The total inventory must be more than the required maximum quantity ( *150* ) that is specified in the replenishment template.</span></span>
1. <span data-ttu-id="9bf0b-316">Необязательно, но рекомендуется: выполните следующие шаги, чтобы создать журнал корректировки запасов:</span><span class="sxs-lookup"><span data-stu-id="9bf0b-316">Optional but recommended: Follow these steps to create an inventory adjustment journal:</span></span>

    1. <span data-ttu-id="9bf0b-317">Перейдите к пункту **Управление запасами \> Записи журнала \> Номенклатуры \> Корректировка запасов**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-317">Go to **Inventory management \> Journal entries \> Items \> Inventory adjustment**.</span></span>
    1. <span data-ttu-id="9bf0b-318">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-318">Select **New**.</span></span>
    1. <span data-ttu-id="9bf0b-319">В диалоговом окне **Создание журнала запасов** в поле **Склад** выберите *61*.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-319">In the **Create inventory journal** dialog box, in the **Warehouse** field, select *61*.</span></span>
    1. <span data-ttu-id="9bf0b-320">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-320">Select **OK**.</span></span>
    1. <span data-ttu-id="9bf0b-321">На экспресс-вкладке **Строки журнала** используйте кнопку **Создать** , чтобы добавить в сетку три строки, и установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9bf0b-321">On the **Journal lines** FastTab, use the **New** button to add three lines to the grid, and set the following values.</span></span> <span data-ttu-id="9bf0b-322">После завершения настройки каждой строки выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-322">After you've finished setting up each line, select **Save**.</span></span>

        - <span data-ttu-id="9bf0b-323">**Строка 1:**</span><span class="sxs-lookup"><span data-stu-id="9bf0b-323">**Line 1:**</span></span>

            - <span data-ttu-id="9bf0b-324">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="9bf0b-324">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="9bf0b-325">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="9bf0b-325">**Site:** *6*</span></span>
            - <span data-ttu-id="9bf0b-326">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="9bf0b-326">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="9bf0b-327">**Местонахождение:** *02A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="9bf0b-327">**Location:** *02A01R1S1B*</span></span>
            - <span data-ttu-id="9bf0b-328">**Грузоместо:** выберите существующее грузоместо в списке или создайте новое грузоместо.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-328">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="9bf0b-329">**Количество:** *1000*</span><span class="sxs-lookup"><span data-stu-id="9bf0b-329">**Quantity:** *1000*</span></span>

        - <span data-ttu-id="9bf0b-330">**Строка 2:**</span><span class="sxs-lookup"><span data-stu-id="9bf0b-330">**Line 2:**</span></span>

            - <span data-ttu-id="9bf0b-331">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="9bf0b-331">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="9bf0b-332">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="9bf0b-332">**Site:** *6*</span></span>
            - <span data-ttu-id="9bf0b-333">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="9bf0b-333">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="9bf0b-334">**Местонахождение:** *07A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="9bf0b-334">**Location:** *07A01R2S1B*</span></span>
            - <span data-ttu-id="9bf0b-335">**Грузоместо:** выберите существующее грузоместо в списке или создайте новое грузоместо.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-335">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="9bf0b-336">**Количество:** *15*</span><span class="sxs-lookup"><span data-stu-id="9bf0b-336">**Quantity:** *15*</span></span>

        - <span data-ttu-id="9bf0b-337">**Строка 3:**</span><span class="sxs-lookup"><span data-stu-id="9bf0b-337">**Line 3:**</span></span>

            - <span data-ttu-id="9bf0b-338">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="9bf0b-338">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="9bf0b-339">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="9bf0b-339">**Site:** *6*</span></span>
            - <span data-ttu-id="9bf0b-340">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="9bf0b-340">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="9bf0b-341">**Местонахождение:** *07A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="9bf0b-341">**Location:** *07A01R1S1B*</span></span>
            - <span data-ttu-id="9bf0b-342">**Грузоместо:** выберите существующее грузоместо в списке или создайте новое грузоместо.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-342">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="9bf0b-343">**Количество:** *10*</span><span class="sxs-lookup"><span data-stu-id="9bf0b-343">**Quantity:** *10*</span></span>

    1. <span data-ttu-id="9bf0b-344">На панели операций выберите **Проверить**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-344">On the Action Pane, select **Validate**.</span></span> <span data-ttu-id="9bf0b-345">Исправьте все найденные ошибки перед переходом к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-345">Address any errors that are found before you move on to the next step.</span></span>
    1. <span data-ttu-id="9bf0b-346">В области действий выберите **Разнести** , чтобы разнести запасы на склад.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-346">On the Action Pane, select **Post** to post the inventory to the warehouse.</span></span>

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a><span data-ttu-id="9bf0b-347">Образец сценария: выполнение пополнения на основе минимального и максимального значений на основе зон</span><span class="sxs-lookup"><span data-stu-id="9bf0b-347">Sample scenario: Run zone-based min/max replenishment</span></span>

<span data-ttu-id="9bf0b-348">После того, как все необходимые образцы данных будут настроены, можно запустить пополнение, выполнив следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-348">After all the prerequisite sample data is in place, you can trigger replenishment by following these steps.</span></span>

1. <span data-ttu-id="9bf0b-349">Перейдите в раздел **Управление складом \> Пополнение \> Пополнения**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-349">Go to **Warehouse management \> Replenishment \> Replenishments**.</span></span>
1. <span data-ttu-id="9bf0b-350">В диалоговом окне **Пополнение** на экспресс-вкладке **Включаемые записи** выберите **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-350">In the **Replenishment** dialog box, on the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="9bf0b-351">В диалоговом окне **Запрос** на вкладке **Диапазон** измените строку таблицы по умолчанию следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9bf0b-351">In the **Inquiry** dialog box, on the **Range** tab, edit the default table row in the following way:</span></span>

    - <span data-ttu-id="9bf0b-352">**Таблица:** выберите _Шаблоны пополнения_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-352">**Table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="9bf0b-353">**Производная таблица:** выберите _Шаблоны пополнения_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-353">**Derived table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="9bf0b-354">**Поле:** выберите _Шаблон пополнения_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-354">**Field:** Select _Replenishment template_.</span></span>
    - <span data-ttu-id="9bf0b-355">**Критерии:** выберите _Пополнение мин./макс. зоны_.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-355">**Criteria:** Select _Zone min/max replen_.</span></span> <span data-ttu-id="9bf0b-356">Этот шаблон пополнения является шаблоном пополнения, созданным при подготовке демонстрационных данных для данного сценария.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-356">This replenishment template is the replenishment template that you created while you were preparing the demo data for this scenario.</span></span>

1. <span data-ttu-id="9bf0b-357">Выберите **OK** , чтобы сохранить запрос и вернуться в диалоговое окно **Пополнение**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-357">Select **OK** to save the query and go back to the **Replenishment** dialog box.</span></span>
1. <span data-ttu-id="9bf0b-358">Выберите **ОК** , чтобы выполнить шаблон пополнения.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-358">Select **OK** to run the replenishment template.</span></span>

<span data-ttu-id="9bf0b-359">Работа пополнения теперь создается для комплектации запасов из зоны *СБОРНАЯ* и пополнения ее в зону *ЭТАЖ*.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-359">Replenishment work is now created to pick inventory from the *BULK* zone and replenish it to the *FLOOR* zone.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="9bf0b-360">Примечания и советы</span><span class="sxs-lookup"><span data-stu-id="9bf0b-360">Notes and tips</span></span>

<span data-ttu-id="9bf0b-361">Вот несколько примечаний и советов по работе с этой функцией:</span><span class="sxs-lookup"><span data-stu-id="9bf0b-361">Here are a few notes and tips for working with the feature:</span></span>

- <span data-ttu-id="9bf0b-362">Чтобы настроить работу пополнения, которая ведет к нужной зоне, можно связать строки шаблона пополнения и директивы места хранения одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="9bf0b-362">To set up replenishment work that goes to the desired zone, you can link the replenishment template lines and location directives in either of the following ways:</span></span>

    - <span data-ttu-id="9bf0b-363">Измените запрос заголовка директивы места хранения и выполните фильтрацию выбранных строк шаблона пополнения.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-363">Edit the location directive header query, and filter the selected replenishment template lines.</span></span>
    - <span data-ttu-id="9bf0b-364">Используйте код директивы в строке шаблона пополнения и сопоставьте его с директивой размещения в месте хранения.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-364">Use a directive code on the replenishment template line, and match it to the put location directive.</span></span>

- <span data-ttu-id="9bf0b-365">Если используются динамические местоположения, работа пополнения будет создана либо для первого доступного местоположения, либо для местоположения, которое уже содержит запасы, если действие директивы места хранения настроено на использование стратегии **Консолидация**.</span><span class="sxs-lookup"><span data-stu-id="9bf0b-365">If you're using dynamic locations, replenishment work will be created either for the first available location or for a location that already contains inventory, if the location directive action is set up to use the **Consolidate** strategy.</span></span>
- <span data-ttu-id="9bf0b-366">При использовании фиксированных местоположений вместо зон следует использовать [стандартное пополнение на основе минимального и максимального значений](tasks/set-up-min-max-replenishment-process.md).</span><span class="sxs-lookup"><span data-stu-id="9bf0b-366">If you're using fixed locations instead of zones, you should use [standard min/max replenishment](tasks/set-up-min-max-replenishment-process.md).</span></span>
