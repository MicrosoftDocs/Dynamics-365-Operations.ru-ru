---
title: Позиция кластера заполнена
description: В этом разделе содержится информация о функции заполненной позиции кластера. Эта функция предлагает альтернативу более жесткому принудительному выполнению правил перерывов в работе при использовании комплектации кластера, так как это позволяет увеличить предел ошибок в объемных ограничениях контейнеров или транспортной тары.
author: Mirzaab
manager: tfehr
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8d030afb568b158e6caf48b0044d595d6ec024f6
ms.sourcegitcommit: 06f64550b2043582de4018bdd3924fcc1fd5d310
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802222"
---
# <a name="cluster-position-full"></a><span data-ttu-id="b72f2-104">Позиция кластера заполнена</span><span class="sxs-lookup"><span data-stu-id="b72f2-104">Cluster position full</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b72f2-105">Функция *Позиция кластера заполнена* предлагает альтернативу более жесткому принудительному выполнению правил перерывов в работе при использовании комплектации кластера, так как это позволяет увеличить предел ошибок в объемных ограничениях контейнеров или транспортной тары.</span><span class="sxs-lookup"><span data-stu-id="b72f2-105">The *Cluster position full* feature offers an alternative to more rigid enforcement of work break rules when cluster picking is used, because it enables a larger margin of error in the volumetric constraints of containers or totes.</span></span> <span data-ttu-id="b72f2-106">В общем случае не все номенклатуры в заказе на работу помещаются в выбранный контейнер.</span><span class="sxs-lookup"><span data-stu-id="b72f2-106">In a common scenario, not all items on a work order fit into a selected container.</span></span> <span data-ttu-id="b72f2-107">Работники склада, выполняющие комплектацию кластера, имеют мало вариантов в этом сценарии: они должны либо изменить контейнер на больший размер контейнера, либо работать со своим супервизором, чтобы найти другое решение.</span><span class="sxs-lookup"><span data-stu-id="b72f2-107">Warehouse workers who are cluster picking have few options in this scenario: they must either change to a larger container size or work with their supervisor to come up with a different solution.</span></span>

<span data-ttu-id="b72f2-108">Эта функция вводит возможность выполнения кнопки **Полный** на одном из рабочих блоков кластера.</span><span class="sxs-lookup"><span data-stu-id="b72f2-108">This feature introduces the ability to run the **Full** button on one of the work units in a cluster.</span></span> <span data-ttu-id="b72f2-109">В предыдущих версиях этот параметр был доступен только для обычной комплектации заказа, а не для комплектации кластера.</span><span class="sxs-lookup"><span data-stu-id="b72f2-109">In older versions, this option was available only for regular order picking, not for cluster picking.</span></span> <span data-ttu-id="b72f2-110">Однако эта функция отличается от стандартной кнопки **Полный** в том, что отменяет оставшуюся работу.</span><span class="sxs-lookup"><span data-stu-id="b72f2-110">However, this feature differs from the standard **Full** button in that it cancels the remaining work.</span></span> <span data-ttu-id="b72f2-111">Она не предлагает пользователю добавить другую ячейку в тот же кластер, и она не создает новую работу автоматически.</span><span class="sxs-lookup"><span data-stu-id="b72f2-111">It doesn't suggest that the user add another bin to the same cluster, and it doesn't automatically create new work.</span></span>

## <a name="turn-on-the-cluster-position-full-feature"></a><span data-ttu-id="b72f2-112">Включение функции "Позиция кластера заполнена"</span><span class="sxs-lookup"><span data-stu-id="b72f2-112">Turn on the Cluster position full feature</span></span>

<span data-ttu-id="b72f2-113">Прежде чем использовать эту функцию, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="b72f2-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="b72f2-114">Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения.</span><span class="sxs-lookup"><span data-stu-id="b72f2-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="b72f2-115">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="b72f2-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b72f2-116">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="b72f2-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b72f2-117">**Название функции:** *Позиция кластера заполнена*</span><span class="sxs-lookup"><span data-stu-id="b72f2-117">**Feature name:** *Cluster position full*</span></span>

## <a name="setup"></a><span data-ttu-id="b72f2-118">Настройка</span><span class="sxs-lookup"><span data-stu-id="b72f2-118">Setup</span></span>

<span data-ttu-id="b72f2-119">В этом разделе приводятся инструкции, а также пример, в котором показано, как настроить и использовать функцию *Позиция кластера заполнена*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-119">This section provides guidelines, and an example that shows how to set up and use the *Cluster position full* feature.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="b72f2-120">Сделать образцы данных доступными</span><span class="sxs-lookup"><span data-stu-id="b72f2-120">Make sample data available</span></span>

<span data-ttu-id="b72f2-121">Для работы с этими [примером сценария](#example-scenario) с помощью образцов записей и значений, указанных здесь, необходимо использовать систему, в которой установлены стандартные [демонстрационные данные](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="b72f2-121">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="b72f2-122">Дополнительно перед началом необходимо выбрать юридическое лицо **USMF**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-122">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="b72f2-123">Этот пример сценария можно также использовать в качестве руководства по работе с этой функцией в производственной системе.</span><span class="sxs-lookup"><span data-stu-id="b72f2-123">You can also use the example scenario as guidance for working with this feature on a production system.</span></span> <span data-ttu-id="b72f2-124">Однако в этом случае необходимо подставить собственные значения для описанных здесь параметров.</span><span class="sxs-lookup"><span data-stu-id="b72f2-124">However, in that case, you must substitute your own values for the settings that are described here.</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="b72f2-125">Профили кластера</span><span class="sxs-lookup"><span data-stu-id="b72f2-125">Cluster profiles</span></span>

<span data-ttu-id="b72f2-126">Необходимо указать, должны ли коды кластера создаваться автоматически, сколько должно использоваться позиций, когда кластеры нарушаются, и как задается последовательность и выполняется проверка работы по комплектации.</span><span class="sxs-lookup"><span data-stu-id="b72f2-126">You must specify whether cluster IDs are automatically generated, how many positions are used, when clusters are broken, and how the picking work is sequenced and verified.</span></span>

1. <span data-ttu-id="b72f2-127">Перейдите **Управление складом \> Настройка \> Мобильное устройство \> Профили кластера**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-127">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="b72f2-128">В области списка выберите запись **Создать кластер**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-128">In the list pane, select the **Create Cluster** record.</span></span>
1. <span data-ttu-id="b72f2-129">На экспресс-вкладке **Общие** проверьте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b72f2-129">On the **General** FastTab, verify the following values:</span></span>

    - <span data-ttu-id="b72f2-130">**Создать код кластера:** *Да*</span><span class="sxs-lookup"><span data-stu-id="b72f2-130">**Generate cluster ID:** *Yes*</span></span>
    - <span data-ttu-id="b72f2-131">**Активировать позиции:** *Да*</span><span class="sxs-lookup"><span data-stu-id="b72f2-131">**Activate positions:** *Yes*</span></span>
    - <span data-ttu-id="b72f2-132">**Число позиций:** *2*</span><span class="sxs-lookup"><span data-stu-id="b72f2-132">**Number of positions:** *2*</span></span>
    - <span data-ttu-id="b72f2-133">**Имя позиции:** *Числовое*</span><span class="sxs-lookup"><span data-stu-id="b72f2-133">**Position name:** *Numeric*</span></span>
    - <span data-ttu-id="b72f2-134">**Разделить кластер при:** *Размещение*</span><span class="sxs-lookup"><span data-stu-id="b72f2-134">**Break cluster at:** *Put*</span></span>
    - <span data-ttu-id="b72f2-135">**Тип проверка сортировки:** *Скан позиции*</span><span class="sxs-lookup"><span data-stu-id="b72f2-135">**Sort verification type:** *Position scan*</span></span>

1. <span data-ttu-id="b72f2-136">На экспресс-вкладке **Сортировка кластера**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-136">In the **Cluster sorting** FastTab.</span></span> <span data-ttu-id="b72f2-137">Сетка должна быть пустой (то есть, она не должна содержать строк).</span><span class="sxs-lookup"><span data-stu-id="b72f2-137">The grid should be blank (that is, it should contain no lines).</span></span>

### <a name="work-templates"></a><span data-ttu-id="b72f2-138">Шаблоны работ</span><span class="sxs-lookup"><span data-stu-id="b72f2-138">Work templates</span></span>

<span data-ttu-id="b72f2-139">Необходимо определить, как создается работа комплектации для комплектации кластера.</span><span class="sxs-lookup"><span data-stu-id="b72f2-139">You must define how the picking work for cluster picking is created.</span></span>

1. <span data-ttu-id="b72f2-140">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Шаблоны работ**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-140">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="b72f2-141">В верхней части страницы задайте для поля **Тип заказа на работу** значение *Заказы на продажу*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-141">At the top of the page, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="b72f2-142">Убедитесь, что следующие шаблоны работы из демонстрационных данных перечислены.</span><span class="sxs-lookup"><span data-stu-id="b72f2-142">Make sure that the following work templates from the demo data are listed.</span></span> <span data-ttu-id="b72f2-143">Если они недоступны, выполнение сценария будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="b72f2-143">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="b72f2-144">61 Этап заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="b72f2-144">61 SO Stage</span></span>
    - <span data-ttu-id="b72f2-145">61 Комплектация кластера заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="b72f2-145">61 SO Cluster pick</span></span>

### <a name="location-directives"></a><span data-ttu-id="b72f2-146">Директивы для мест хранения</span><span class="sxs-lookup"><span data-stu-id="b72f2-146">Location directives</span></span>

<span data-ttu-id="b72f2-147">Необходимо указать, откуда будут комплектоваться номенклатуры, и где они будут помещены.</span><span class="sxs-lookup"><span data-stu-id="b72f2-147">You must specify where items are picked from and where they are put.</span></span>

1. <span data-ttu-id="b72f2-148">Перейдите в раздел **Управление складом \> Настройка \> Директивы местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-148">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b72f2-149">В заголовке списка задайте в поле **Тип заказа на работу** значение *Заказы на продажу*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-149">In the list header, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="b72f2-150">Убедитесь, что следующие директивы заказа на продажу из демонстрационных данных перечислены.</span><span class="sxs-lookup"><span data-stu-id="b72f2-150">Make sure that the following sales order directives from the demo data are listed.</span></span> <span data-ttu-id="b72f2-151">Если они недоступны, выполнение сценария будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="b72f2-151">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="b72f2-152">61 Комплектация кластера</span><span class="sxs-lookup"><span data-stu-id="b72f2-152">61 Cluster pick</span></span>
    - <span data-ttu-id="b72f2-153">61 Комплектация заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="b72f2-153">61 SO Pick order</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="b72f2-154">Пункты меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="b72f2-154">Mobile device menu items</span></span>

<span data-ttu-id="b72f2-155">Необходимо настроить пункт меню мобильного устройства для использования существующей работы под управлением комплектации кластера.</span><span class="sxs-lookup"><span data-stu-id="b72f2-155">You must configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="b72f2-156">В пункте меню мобильного устройства для комплектации кластера параметр **Разрешить разделение работы** должен быть включен, и должен быть добавлен класс работы *Комплектация заказа на продажу*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-156">In the mobile device menu item for cluster picking, the **Allow splitting of work** parameter must be turned on, and the *SO Pick* work class must be added.</span></span>

1. <span data-ttu-id="b72f2-157">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-157">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="b72f2-158">В области списка выберите запись **Создать комплектацию кластера**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-158">In the list pane, select the **Cluster Pick Create** record.</span></span>
1. <span data-ttu-id="b72f2-159">Выберите **Правка** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="b72f2-159">Select **Edit** in the Action pane.</span></span>
1. <span data-ttu-id="b72f2-160">На экспресс-вкладке **Общие** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="b72f2-160">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b72f2-161">**Кем управляется:** *Комплектация кластера*</span><span class="sxs-lookup"><span data-stu-id="b72f2-161">**Directed by:** *Cluster picking*</span></span>
    - <span data-ttu-id="b72f2-162">**Создать грузоместо:** *Да*</span><span class="sxs-lookup"><span data-stu-id="b72f2-162">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="b72f2-163">**Разрешить разделение работы:** *Да*</span><span class="sxs-lookup"><span data-stu-id="b72f2-163">**Allow splitting of work:** *Yes*</span></span>
    - <span data-ttu-id="b72f2-164">**Код профиля кластера:** *Создать кластер*</span><span class="sxs-lookup"><span data-stu-id="b72f2-164">**Cluster profile ID:** *Create Cluster*</span></span>

    <span data-ttu-id="b72f2-165">Примите для всех остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b72f2-165">Accept the default values for all other fields.</span></span>

1. <span data-ttu-id="b72f2-166">На экспресс-вкладке **Классы работы** добавьте следующие две строки, как требуется:</span><span class="sxs-lookup"><span data-stu-id="b72f2-166">On the **Work classes** FastTab, add the following two lines, as required:</span></span>

    - <span data-ttu-id="b72f2-167">Строка 1 (обычно содержится в демонстрационных данных):</span><span class="sxs-lookup"><span data-stu-id="b72f2-167">Line 1 (usually present in demo data):</span></span>

        - <span data-ttu-id="b72f2-168">**Код класса работы:** *Продажи*</span><span class="sxs-lookup"><span data-stu-id="b72f2-168">**Work class ID:** *Sales*</span></span> 
        - <span data-ttu-id="b72f2-169">**Тип заказа на работу:** *Заказы на продажу*</span><span class="sxs-lookup"><span data-stu-id="b72f2-169">**Work order type:** *Sales orders*</span></span>

    - <span data-ttu-id="b72f2-170">Строка 2 (возможно, отсутствует в демонстрационных данных):</span><span class="sxs-lookup"><span data-stu-id="b72f2-170">Line 2 (probably not present in demo data):</span></span>

        - <span data-ttu-id="b72f2-171">**Код класса работы:** *Комплектация заказа на продажу*</span><span class="sxs-lookup"><span data-stu-id="b72f2-171">**Work class ID:** *SO Pick*</span></span>
        - <span data-ttu-id="b72f2-172">**Тип заказа на работу:** *Заказы на продажу*</span><span class="sxs-lookup"><span data-stu-id="b72f2-172">**Work order type:** *Sales orders*</span></span>

1. <span data-ttu-id="b72f2-173">Перейдите к пункту **Настройка подтверждения работы** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="b72f2-173">Go to **Work confirmation setup** in the Action pane.</span></span>
1. <span data-ttu-id="b72f2-174">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-174">Select **Edit**.</span></span>
1. <span data-ttu-id="b72f2-175">Введите следующие значения в строке в сетке.</span><span class="sxs-lookup"><span data-stu-id="b72f2-175">Enter the following values on the line in grid.</span></span>
    - <span data-ttu-id="b72f2-176">**Тип работы** - *Комплектация*</span><span class="sxs-lookup"><span data-stu-id="b72f2-176">**Work type** - *Pick*</span></span>
    - <span data-ttu-id="b72f2-177">**Подтверждение продукта** - *Установите флажок*</span><span class="sxs-lookup"><span data-stu-id="b72f2-177">**Product confirmation** - *Select the check box*</span></span>

1. <span data-ttu-id="b72f2-178">Выберите **Сохранить** на панели операций и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b72f2-178">Select **Save** in the Action pane and close the page.</span></span>

## <a name="create-picking-work"></a><span data-ttu-id="b72f2-179">Создать работы комплектации</span><span class="sxs-lookup"><span data-stu-id="b72f2-179">Create picking work</span></span>

<span data-ttu-id="b72f2-180">Перед началом комплектации кластера необходимо создать некоторую исходящую работу.</span><span class="sxs-lookup"><span data-stu-id="b72f2-180">Before you can start cluster picking, you must create some outbound work.</span></span> <span data-ttu-id="b72f2-181">Профиль кластера, созданный ранее, определяет две позиции кластера.</span><span class="sxs-lookup"><span data-stu-id="b72f2-181">The cluster profile that you created earlier specifies two cluster positions.</span></span> <span data-ttu-id="b72f2-182">Поэтому для комплектации заказа на продажу должно быть создано по крайней мере два кода рабочих процессов.</span><span class="sxs-lookup"><span data-stu-id="b72f2-182">Therefore, at least two work IDs must be created for sales order picking.</span></span> <span data-ttu-id="b72f2-183">В этом случае проводки будут выполняться на складе *61*, и в них будут использоваться номенклатуры *L0101* и *T0100*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-183">For this scenario, transactions will occur in warehouse *61*, and they will use items *L0101* and *T0100*.</span></span> <span data-ttu-id="b72f2-184">Демонстрационные данные должны иметь достаточное количество запасов в наличии для этих номенклатур.</span><span class="sxs-lookup"><span data-stu-id="b72f2-184">The demo data should have enough on-hand inventory of these items.</span></span> <span data-ttu-id="b72f2-185">Убедитесь, что имеется достаточное количество запасов для выполнения проводок.</span><span class="sxs-lookup"><span data-stu-id="b72f2-185">Make sure that you have enough inventory to complete the transactions.</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="b72f2-186">Создание заказа на продажу 1</span><span class="sxs-lookup"><span data-stu-id="b72f2-186">Create sales order 1</span></span>

1. <span data-ttu-id="b72f2-187">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-187">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b72f2-188">Выберите **Создать**, чтобы создать заказ на продажу 1.</span><span class="sxs-lookup"><span data-stu-id="b72f2-188">Select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="b72f2-189">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b72f2-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b72f2-190">**Счет клиента:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="b72f2-190">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="b72f2-191">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="b72f2-191">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="b72f2-192">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-192">Select **OK**.</span></span>
1. <span data-ttu-id="b72f2-193">Открывается новый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="b72f2-193">The new sales order is opened.</span></span> <span data-ttu-id="b72f2-194">На экспресс-вкладке **Строки заказа на продажу** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="b72f2-194">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="b72f2-195">**Код номенклатуры:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="b72f2-195">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="b72f2-196">**Количество:** *5*</span><span class="sxs-lookup"><span data-stu-id="b72f2-196">**Quantity:** *5*</span></span>

1. <span data-ttu-id="b72f2-197">На экспресс-вкладке **Сведения о строке** на вкладке **Доставка** установите в поле **Подтвержденная дата отгрузки** текущую дату.</span><span class="sxs-lookup"><span data-stu-id="b72f2-197">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="b72f2-198">На экспресс-вкладке **Строки заказа на продажу** добавьте вторую строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="b72f2-198">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="b72f2-199">**Код номенклатуры:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="b72f2-199">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="b72f2-200">**Количество:** *20*</span><span class="sxs-lookup"><span data-stu-id="b72f2-200">**Quantity:** *20*</span></span>

1. <span data-ttu-id="b72f2-201">На экспресс-вкладке **Сведения о строке** на вкладке **Доставка** установите в поле **Подтвержденная дата отгрузки** текущую дату.</span><span class="sxs-lookup"><span data-stu-id="b72f2-201">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="b72f2-202">Для каждой только что добавленной строки выполните следующие действия, чтобы зарезервировать запасы:</span><span class="sxs-lookup"><span data-stu-id="b72f2-202">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="b72f2-203">Выберите строку для резервирования.</span><span class="sxs-lookup"><span data-stu-id="b72f2-203">Select the line to reserve.</span></span>
    2. <span data-ttu-id="b72f2-204">На экспресс-вкладке **Строки заказа на продажу** выберите **Запасы \> Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-204">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="b72f2-205">На странице **Резервирование** на панели операций выберите **Резервирование лота** для резервирования запасов.</span><span class="sxs-lookup"><span data-stu-id="b72f2-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="b72f2-206">Закройте страницу **Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-206">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="b72f2-207">На панели операций на вкладке **Склад** выберите вариант **Выпустить на склад**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-207">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="b72f2-208">Когда выпуск будет завершен, вы получите информационные сообщения, которые указывают коды волны и загрузки, которые были созданы.</span><span class="sxs-lookup"><span data-stu-id="b72f2-208">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="b72f2-209">Создание заказа на продажу 2</span><span class="sxs-lookup"><span data-stu-id="b72f2-209">Create sales order 2</span></span>

1. <span data-ttu-id="b72f2-210">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-210">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b72f2-211">Выберите **Создать**, чтобы создать заказ на продажу 2.</span><span class="sxs-lookup"><span data-stu-id="b72f2-211">Select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="b72f2-212">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b72f2-212">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b72f2-213">**Счет клиента:** *US-011*</span><span class="sxs-lookup"><span data-stu-id="b72f2-213">**Customer account:** *US-011*</span></span>
    - <span data-ttu-id="b72f2-214">**Склад:** *61*</span><span class="sxs-lookup"><span data-stu-id="b72f2-214">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="b72f2-215">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-215">Select **OK**.</span></span>
1. <span data-ttu-id="b72f2-216">Открывается новый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="b72f2-216">The new sales order is opened.</span></span> <span data-ttu-id="b72f2-217">На экспресс-вкладке **Строки заказа на продажу** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="b72f2-217">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="b72f2-218">**Код номенклатуры:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="b72f2-218">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="b72f2-219">**Количество:** *20*</span><span class="sxs-lookup"><span data-stu-id="b72f2-219">**Quantity:** *20*</span></span>

1. <span data-ttu-id="b72f2-220">На экспресс-вкладке **Сведения о строке** на вкладке **Доставка** установите в поле **Подтвержденная дата отгрузки** текущую дату.</span><span class="sxs-lookup"><span data-stu-id="b72f2-220">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="b72f2-221">На экспресс-вкладке **Строки заказа на продажу** добавьте вторую строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="b72f2-221">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="b72f2-222">**Код номенклатуры:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="b72f2-222">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="b72f2-223">**Количество:** *2*</span><span class="sxs-lookup"><span data-stu-id="b72f2-223">**Quantity:** *2*</span></span>

1. <span data-ttu-id="b72f2-224">На экспресс-вкладке **Сведения о строке** на вкладке **Доставка** установите в поле **Подтвержденная дата отгрузки** текущую дату.</span><span class="sxs-lookup"><span data-stu-id="b72f2-224">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="b72f2-225">Для каждой только что добавленной строки выполните следующие действия, чтобы зарезервировать запасы:</span><span class="sxs-lookup"><span data-stu-id="b72f2-225">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="b72f2-226">Выберите строку для резервирования.</span><span class="sxs-lookup"><span data-stu-id="b72f2-226">Select the line to reserve.</span></span>
    2. <span data-ttu-id="b72f2-227">На экспресс-вкладке **Строки заказа на продажу** выберите **Запасы \> Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-227">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="b72f2-228">На странице **Резервирование** на панели операций выберите **Резервирование лота** для резервирования запасов.</span><span class="sxs-lookup"><span data-stu-id="b72f2-228">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="b72f2-229">Закройте страницу **Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-229">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="b72f2-230">На панели операций на вкладке **Склад** выберите вариант **Выпустить на склад**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-230">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="b72f2-231">Когда выпуск будет завершен, вы получите информационные сообщения, которые указывают коды волны и загрузки, которые были созданы.</span><span class="sxs-lookup"><span data-stu-id="b72f2-231">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="get-work-ids-and-license-plate-numbers"></a><span data-ttu-id="b72f2-232">Получение кодов работ и номеров грузомест</span><span class="sxs-lookup"><span data-stu-id="b72f2-232">Get work IDs and license plate numbers</span></span>

<span data-ttu-id="b72f2-233">Должны быть созданы два кода работ, каждая из которых содержит две строки комплектации.</span><span class="sxs-lookup"><span data-stu-id="b72f2-233">Two work IDs should have been created, each of which has two pick lines.</span></span> <span data-ttu-id="b72f2-234">Выполните следующие действия, чтобы найти коды работ и назначения грузомест.</span><span class="sxs-lookup"><span data-stu-id="b72f2-234">Follow these steps to find the work IDs and license plate assignments.</span></span>

1. <span data-ttu-id="b72f2-235">Перейдите в раздел **Управление складом \> Работа \> Сведения о работе**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-235">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="b72f2-236">В сетке **Обзор** найдите столбец **Номер заказа** для двух только что созданных заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="b72f2-236">In the **Overview** grid, search the **Order number** column for the two sales orders that you just created.</span></span> <span data-ttu-id="b72f2-237">Для каждого заказа на продажу запишите соответствующий код работы.</span><span class="sxs-lookup"><span data-stu-id="b72f2-237">For each sales order, make a note of the corresponding work ID.</span></span>
1. <span data-ttu-id="b72f2-238">Выберите строку для каждого заказа на продажу для отображения связанной информации в сетке **Строки**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-238">Select the row for each sales order to show related information in the **Lines** grid.</span></span> <span data-ttu-id="b72f2-239">Запишите местоположение, из которого будет комплектоваться каждая номенклатура.</span><span class="sxs-lookup"><span data-stu-id="b72f2-239">Make a note of the location that each item will be picked from.</span></span>
1. <span data-ttu-id="b72f2-240">Перейдите в раздел **Управление запасами \> Запросы и отчеты \> Список количества в наличии**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-240">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="b72f2-241">На панели операций выберите **Аналитики**, чтобы открыть диалоговое окно **Отображение аналитики**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-241">On the Action Pane, select **Dimensions** to open the **Dimension display** dialog box.</span></span>
1. <span data-ttu-id="b72f2-242">Убедитесь, что установлены флажки **Грузоместо**, **Склад** и **Номер номенклатуры**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-242">Make sure that the **License plate**, **Warehouse**, and **Item number** check boxes are selected, and then select **OK**.</span></span>
1. <span data-ttu-id="b72f2-243">На панели **Фильтр** настройте следующие фильтры:</span><span class="sxs-lookup"><span data-stu-id="b72f2-243">In the **Filter** pane, set the following filters:</span></span>

    - <span data-ttu-id="b72f2-244">**Код номенклатуры** — **один из** — *L0101* и *T100*</span><span class="sxs-lookup"><span data-stu-id="b72f2-244">**Item number** – **is one of** – *L0101* and *T100*</span></span>
    - <span data-ttu-id="b72f2-245">**Склад** — **начинается с** — *61*</span><span class="sxs-lookup"><span data-stu-id="b72f2-245">**Warehouse** – **begins with** – *61*</span></span>

1. <span data-ttu-id="b72f2-246">Запишите отображаемые значения **Грузоместо**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-246">Make a note of the **License plate** values that are shown.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="b72f2-247">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="b72f2-247">Example scenario</span></span>

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a><span data-ttu-id="b72f2-248">Выполнение потока мобильных устройств — настройка подтверждения работы для продукта</span><span class="sxs-lookup"><span data-stu-id="b72f2-248">Mobile device flow execution – Work confirmation setup for the product</span></span>

1. <span data-ttu-id="b72f2-249">Выполните вход в приложение склада как пользователь на складе *61*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-249">Sign in to the warehouse app as a user in warehouse *61*.</span></span>
1. <span data-ttu-id="b72f2-250">Выберите **Исходящие \> Создание комплектации кластера**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-250">Go to **Outbound \> Cluster pick create**.</span></span>

    <span data-ttu-id="b72f2-251">Отображается страница **ЗАДАЧА: назначение работы кластеру**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-251">The **TASK: Assign work to Cluster** page appears.</span></span>

1. <span data-ttu-id="b72f2-252">Введите код работы для заказа на продажу 1, чтобы назначить его позиции кластера 1.</span><span class="sxs-lookup"><span data-stu-id="b72f2-252">Enter the work ID for sales order 1 to assign it to cluster position 1.</span></span>
1. <span data-ttu-id="b72f2-253">Выберите **ОК** (символ флажка).</span><span class="sxs-lookup"><span data-stu-id="b72f2-253">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="b72f2-254">Введите код работы для заказа на продажу 2, чтобы назначить его позиции кластера 2.</span><span class="sxs-lookup"><span data-stu-id="b72f2-254">Enter the work ID for sales order 2 to assign it to cluster position 2.</span></span>
1. <span data-ttu-id="b72f2-255">Выберите **ОК** (символ флажка).</span><span class="sxs-lookup"><span data-stu-id="b72f2-255">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="b72f2-256">Открывается страница **ЗАДАЧА: создание комплектации кластера: комплектация** и отображается *Номенклатура L0101 2 палеты*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-256">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item L0101 2 PL*.</span></span>

<span data-ttu-id="b72f2-257">Поскольку профиль кластера задает количество позиций равным 2, система автоматически направляет вас на первую консолидированную комплектацию: две палеты (PL) номенклатуры *L0101*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-257">Because the cluster profile set the number of positions to 2, the system automatically directs you to the first consolidate pick: two pallets (PL) of item *L0101*.</span></span>

<span data-ttu-id="b72f2-258">В любой момент выполнения следующих шагов можно выбрать вкладку **Сведения**, чтобы просмотреть дополнительные сведения о задаче, такие как местоположение комплектации.</span><span class="sxs-lookup"><span data-stu-id="b72f2-258">At any time during the following steps, you can select the **Details** tab to view additional information about the task, such as the picking location.</span></span>

1. <span data-ttu-id="b72f2-259">Задайте в поле **НОМЕНКЛАТУРА** значение *L0101*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-259">Set the **ITEM** field to *L0101*.</span></span> <span data-ttu-id="b72f2-260">Это подтверждает код номенклатуры, необходимый для этого пункта меню (вы настроили этот параметр ранее, выбрав **Настройка подтверждения работы** на странице **Пункт меню мобильного устройства** при создании этого пункта меню).</span><span class="sxs-lookup"><span data-stu-id="b72f2-260">This confirms the item number, which is required for this menu item (you configured this earlier by selecting **Work confirmation setup**  from the **Mobile device menu item** page when you created this menu item).</span></span>
1. <span data-ttu-id="b72f2-261">Введите номер грузоместа, связанной с номенклатурой в комплектуемом местоположении.</span><span class="sxs-lookup"><span data-stu-id="b72f2-261">Enter the license plate number that is associated with the item in the location that is being picked.</span></span> <span data-ttu-id="b72f2-262">Вы будете комплектовать две палеты.</span><span class="sxs-lookup"><span data-stu-id="b72f2-262">You will pick two pallets.</span></span>
1. <span data-ttu-id="b72f2-263">Установите в поле **LP** значение *LP\_PICK\_01*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-263">Set the **LP** field to *LP\_PICK\_01*.</span></span>
1. <span data-ttu-id="b72f2-264">Выберите **ОК** (символ флажка).</span><span class="sxs-lookup"><span data-stu-id="b72f2-264">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="b72f2-265">Будет открыта страница **ЗАДАЧА: Сортировка: Создание комплектации кластера**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-265">The **TASK: Sort: Cluster Pick Create** page appears.</span></span> <span data-ttu-id="b72f2-266">Здесь будут сортироваться две скомплектованные палеты в позицию комплектации.</span><span class="sxs-lookup"><span data-stu-id="b72f2-266">Here, you will sort the two picked pallets into a pick position.</span></span> <span data-ttu-id="b72f2-267">Эта позиция может быть транспортной тарой или контейнером, который используется для разделения скомплектованных запасов по заказам на продажу.</span><span class="sxs-lookup"><span data-stu-id="b72f2-267">This position might be a tote or container that is used to separate the picked inventory by sales order.</span></span>

1. <span data-ttu-id="b72f2-268">Просмотрите сведения, отображаемые для номенклатуры (*L0101*) и количества (*20* шт.), которые будут отсортированы в позиции 1 (для заказа на продажу 1).</span><span class="sxs-lookup"><span data-stu-id="b72f2-268">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="b72f2-269">Установите для поля **ПОЗИЦИЯ НД** значение *1*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-269">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="b72f2-270">Выберите **ОК** (символ флажка).</span><span class="sxs-lookup"><span data-stu-id="b72f2-270">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="b72f2-271">Просмотрите сведения, отображаемые для номенклатуры (*L0101*) и количества (*20* шт.), которые будут отсортированы в позиции 2 (для заказа на продажу 2).</span><span class="sxs-lookup"><span data-stu-id="b72f2-271">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="b72f2-272">Установите для поля **ПОЗИЦИЯ НД** значение *2*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-272">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="b72f2-273">Выберите **ОК** (символ флажка).</span><span class="sxs-lookup"><span data-stu-id="b72f2-273">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="b72f2-274">Открывается страница **ЗАДАЧА: создание комплектации кластера: комплектация** и отображается *Номенклатура T0100 7 шт*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-274">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item T0100 7 ea*.</span></span>

<span data-ttu-id="b72f2-275">В этом сценарии позиция 1 не может принять все количество номенклатур, которые должны быть скомплектованы для выполнения заказа на продажу 1.</span><span class="sxs-lookup"><span data-stu-id="b72f2-275">In this scenario, position 1 can't accept the full quantity of items that must be picked to fulfill sales order 1.</span></span> <span data-ttu-id="b72f2-276">Позиция должна быть помечена как заполненная.</span><span class="sxs-lookup"><span data-stu-id="b72f2-276">A position must be marked as full.</span></span> <span data-ttu-id="b72f2-277">В этом случае будет выполнена частичная комплектация для второй номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="b72f2-277">In this scenario, you will do a partial pick of the second item.</span></span> <span data-ttu-id="b72f2-278">Вторая номенклатура будет частично укомплектована для позиции 1, и будет создана новая работа с целью комплектации оставшегося количества для удовлетворения заказа.</span><span class="sxs-lookup"><span data-stu-id="b72f2-278">The second item will be partially picked for position 1, and new work will be created to pick the remaining quantity to fulfill the order.</span></span>

1. <span data-ttu-id="b72f2-279">Выберите кнопку меню (иногда называется "гамбургер" или "кнопка-гамбургер"), затем выберите **Позиция заполнена**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-279">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Position full**.</span></span>
1. <span data-ttu-id="b72f2-280">Определите заполненную позиции и выберите значение *1*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-280">Identify the position that is full, and select *1*.</span></span>
1. <span data-ttu-id="b72f2-281">Выберите **ОК** (символ флажка).</span><span class="sxs-lookup"><span data-stu-id="b72f2-281">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="b72f2-282">Введите количество комплектации, которое еще нужно скомплектовать в позицию 1.</span><span class="sxs-lookup"><span data-stu-id="b72f2-282">Enter the pick quantity that can still be picked into position 1.</span></span> <span data-ttu-id="b72f2-283">Система может определить номер комплектуемой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="b72f2-283">The system can determine which item number is being picked.</span></span>
1. <span data-ttu-id="b72f2-284">Введите *2*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-284">Enter *2*.</span></span>
1. <span data-ttu-id="b72f2-285">Выберите **ОК** (символ флажка).</span><span class="sxs-lookup"><span data-stu-id="b72f2-285">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="b72f2-286">Подтвердите код номенклатуры, чтобы завершить комплектацию оставшейся номенклатуры в позицию 2.</span><span class="sxs-lookup"><span data-stu-id="b72f2-286">Confirm the item number to complete the pick of the remaining item into position 2.</span></span>
1. <span data-ttu-id="b72f2-287">Задайте в поле **НОМЕНКЛАТУРА** значение *T0100*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-287">Set the **ITEM** field to *T0100*.</span></span>
1. <span data-ttu-id="b72f2-288">Выберите **ОК** (символ флажка).</span><span class="sxs-lookup"><span data-stu-id="b72f2-288">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="b72f2-289">Введите грузоместо, из которого осуществляется комплектация номенклатуры, задав в поле **LP** значение *LPREPL04*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-289">Enter the license plate that the item is being picked from by setting the **LP** field to *LPREPL04*.</span></span>
1. <span data-ttu-id="b72f2-290">Выберите **ОК** (символ флажка).</span><span class="sxs-lookup"><span data-stu-id="b72f2-290">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="b72f2-291">Просмотрите сведения, отображаемые для номенклатуры (*T0100*) и количества (*2* шт.), которые будут отсортированы в позиции 2 (для заказа на продажу 2).</span><span class="sxs-lookup"><span data-stu-id="b72f2-291">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="b72f2-292">Установите для поля **ПОЗИЦИЯ НД** значение *2*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-292">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="b72f2-293">Выберите **ОК** (символ флажка).</span><span class="sxs-lookup"><span data-stu-id="b72f2-293">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="b72f2-294">Просмотрите сведения, отображаемые для номенклатуры (*T0100*) и количества (*2* шт.), которые будут отсортированы в позиции 1 (для заказа на продажу 1).</span><span class="sxs-lookup"><span data-stu-id="b72f2-294">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="b72f2-295">Установите для поля **ПОЗИЦИЯ НД** значение *1*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-295">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="b72f2-296">Выберите **ОК** (символ флажка).</span><span class="sxs-lookup"><span data-stu-id="b72f2-296">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="b72f2-297">Будет открыта страница **ЗАДАЧА: Создание комплектации кластера: Размещение**.</span><span class="sxs-lookup"><span data-stu-id="b72f2-297">The **TASK: Cluster Pick Create: Put** page appears.</span></span>

<span data-ttu-id="b72f2-298">В этом сценарии комплектация кластера завершена, и пользователь направляется на размещение скомплектованных номенклатур из позиции 1 и позиции 2 в промежуточном местоположении *STAGE01*.</span><span class="sxs-lookup"><span data-stu-id="b72f2-298">In this scenario, the cluster pick has been completed, and the user is directed to put away the picked items from position 1 and position 2 into staging location *STAGE01*.</span></span>

1. <span data-ttu-id="b72f2-299">Просмотрите сведения на странице.</span><span class="sxs-lookup"><span data-stu-id="b72f2-299">Review the information on the page.</span></span> <span data-ttu-id="b72f2-300">Она показывает, что общее количество *44* будет помещено в промежуточное местоположение.</span><span class="sxs-lookup"><span data-stu-id="b72f2-300">It shows that a total quantity of *44* will be put to the staging location.</span></span>
1. <span data-ttu-id="b72f2-301">Выберите **ОК** (символ флажка).</span><span class="sxs-lookup"><span data-stu-id="b72f2-301">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="b72f2-302">Будет получено сообщение "Кластер завершен".</span><span class="sxs-lookup"><span data-stu-id="b72f2-302">You receive a "Cluster Completed" message.</span></span>

<span data-ttu-id="b72f2-303">Теперь можно использовать пункт меню **Комплектация продаж** для комплектации оставшегося количества.</span><span class="sxs-lookup"><span data-stu-id="b72f2-303">You can now use the **Sales Picking** menu item to pick the remaining quantity.</span></span> <span data-ttu-id="b72f2-304">Затем можно воспользоваться пунктом меню **Загрузка продаж**, чтобы переместить номенклатуры из промежуточного местоположения на погрузочный док.</span><span class="sxs-lookup"><span data-stu-id="b72f2-304">You can then use the **Sales loading** menu item to move the items from the staging location to the loading dock.</span></span>
