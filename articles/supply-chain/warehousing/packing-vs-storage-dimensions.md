---
title: Настройка различных аналитик для упаковки и хранения
description: В этой теме показано, как указать, для какого процесса (упаковка, хранение или вложенная упаковка) используется каждая указанная аналитика.
author: mirzaab
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResPhysicalProductDimensions, WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: aa5cbf807e809238489c539d3ad8c0bc34421774
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501302"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a><span data-ttu-id="eae06-103">Настройка различных аналитик для упаковки и хранения</span><span class="sxs-lookup"><span data-stu-id="eae06-103">Set different dimensions for packing and storage</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="eae06-104">Некоторые номенклатуры упакованы или хранятся таким образом, что возможно потребуется отдельно отслеживать физические аналитики для каждого из различных процессов.</span><span class="sxs-lookup"><span data-stu-id="eae06-104">Some items are packed or stored in such a way that you may need to track physical dimensions differently for each of several different processes.</span></span> <span data-ttu-id="eae06-105">Функция *Аналитики упаковки продукта* позволяет настроить один или несколько типов аналитик для каждого продукта.</span><span class="sxs-lookup"><span data-stu-id="eae06-105">The *Packaging product dimensions* feature lets you set up one or several types of dimensions for each product.</span></span> <span data-ttu-id="eae06-106">Каждый тип аналитики предоставляет набор физических измерений (вес, ширина, глубина и высота) и определяет процесс, в котором применяются эти значения физического измерения.</span><span class="sxs-lookup"><span data-stu-id="eae06-106">Each dimension type provides a set of physical measurements (weight, width, depth, and height), and establishes the process where those physical measurement values apply.</span></span> <span data-ttu-id="eae06-107">Если эта функция включена, система будет поддерживать следующие типы аналитик:</span><span class="sxs-lookup"><span data-stu-id="eae06-107">When this feature is enabled, your system will support the following types of dimensions:</span></span>

- <span data-ttu-id="eae06-108">*Хранение* — аналитики хранения используются вместе с весогабаритными параметрами местоположения, чтобы определить количество каждой номенклатуры, которое может храниться в различных местоположениях склада.</span><span class="sxs-lookup"><span data-stu-id="eae06-108">*Storage* - Storage dimensions are used along with location volumetrics to determine how many of each item can be stored in various warehouse locations.</span></span>
- <span data-ttu-id="eae06-109">*Упаковка* — аналитики упаковки используются при выполнении процесса контейнеризации и ручной упаковки для определения количества номенклатуры, помещающихся в различные типы контейнеров.</span><span class="sxs-lookup"><span data-stu-id="eae06-109">*Packing* - Packing dimensions are used during containerization and the manual packing process to determine how many of each item will fit in various container types.</span></span>
- <span data-ttu-id="eae06-110">*Вложенная упаковка*— аналитики вложенной упаковки, используются, когда процесс упаковки содержит несколько уровней.</span><span class="sxs-lookup"><span data-stu-id="eae06-110">*Nested packing* - Nested packing dimensions are used when the packing process contains multiple levels.</span></span>

<span data-ttu-id="eae06-111">Аналитики *Хранение* поддерживаются даже в том случае, когда функция *Аналитики упаковки продукта* не активирована.</span><span class="sxs-lookup"><span data-stu-id="eae06-111">*Storage* dimensions are supported even when the *Packaging product dimensions* feature isn't enabled.</span></span> <span data-ttu-id="eae06-112">Настройка выполняется с помощью страницы **Физическая аналитика** в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="eae06-112">You set these up using the **Physical dimension** page in Supply Chain Management.</span></span> <span data-ttu-id="eae06-113">Эти аналитики используются всеми процессами, в которых не указаны аналитики упаковки или вложенной упаковки.</span><span class="sxs-lookup"><span data-stu-id="eae06-113">These dimensions are used by all processes where the packing and nested packing dimensions aren't specified.</span></span>

<span data-ttu-id="eae06-114">Аналитики *упаковка* и *вложенная упаковка* настраиваются с помощью страницы **Физические аналитики продукта**, которая добавляется, когда включается функция *Аналитики упаковки продуктов*.</span><span class="sxs-lookup"><span data-stu-id="eae06-114">*Packing* and *nested packing* dimensions are set up using the **Physical product dimensions** page, which is added when you enable the *Packaging product dimensions* feature.</span></span>
<span data-ttu-id="eae06-115">В этой теме представлен сценарий, иллюстрирующий использование этой функции.</span><span class="sxs-lookup"><span data-stu-id="eae06-115">This topic provides a scenario that illustrates how to use this feature.</span></span>

## <a name="turn-on-the-packaging-product-dimensions-feature"></a><span data-ttu-id="eae06-116">Включение функции аналитик упаковки продуктов</span><span class="sxs-lookup"><span data-stu-id="eae06-116">Turn on the packaging product dimensions feature</span></span>

<span data-ttu-id="eae06-117">Прежде чем использовать эту функцию, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="eae06-117">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="eae06-118">Администраторы могут использовать рабочую область [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="eae06-118">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="eae06-119">В этом случае функция указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eae06-119">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="eae06-120">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="eae06-120">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="eae06-121">**Имя функции:** *Аналитики упаковки продуктов*</span><span class="sxs-lookup"><span data-stu-id="eae06-121">**Feature name:** *Packaging product dimensions*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="eae06-122">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="eae06-122">Example scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="eae06-123">Настройка сценария</span><span class="sxs-lookup"><span data-stu-id="eae06-123">Set up the scenario</span></span>

<span data-ttu-id="eae06-124">Перед выполнением примера сценария необходимо подготовить систему, как описано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="eae06-124">Before you can run the example scenario, you must prepare your system as described in this section.</span></span>

#### <a name="enable-demo-data"></a><span data-ttu-id="eae06-125">Включение демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="eae06-125">Enable demo data</span></span>

<span data-ttu-id="eae06-126">Для работы с этим сценарием с помощью демонстрационных записей и значений, указанных здесь, необходимо использовать систему, в которой установлены стандартные [демонстрационные данные](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="eae06-126">To work through this scenario using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="eae06-127">Дополнительно перед началом необходимо выбрать юридическое лицо *USMF*.</span><span class="sxs-lookup"><span data-stu-id="eae06-127">Additionally, you must select the *USMF* legal entity before you begin.</span></span>

#### <a name="add-a-new-physical-dimension-to-a-product"></a><span data-ttu-id="eae06-128">Добавление новой физической аналитики к продукту</span><span class="sxs-lookup"><span data-stu-id="eae06-128">Add a new physical dimension to a product</span></span>

<span data-ttu-id="eae06-129">Добавьте новую физическую аналитику для продукта, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="eae06-129">Add a new physical dimension for a product by doing the following:</span></span>

1. <span data-ttu-id="eae06-130">Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="eae06-130">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="eae06-131">Выберите продукт со значением **Код номенклатуры** *A0001*.</span><span class="sxs-lookup"><span data-stu-id="eae06-131">Select the product with **Item number** *A0001*.</span></span>
1. <span data-ttu-id="eae06-132">На панели действий откройте вкладку **Управление складскими запасами** и в группе **Склад** выберите **Физические аналитики продукта**.</span><span class="sxs-lookup"><span data-stu-id="eae06-132">On the Action Pane, open the **Manage inventory** tab and, from the **Warehouse** group, select **Physical product dimensions**.</span></span>
1. <span data-ttu-id="eae06-133">Откроется страница **Физические аналитики продукта**.</span><span class="sxs-lookup"><span data-stu-id="eae06-133">The **Physical product dimensions** page opens.</span></span> <span data-ttu-id="eae06-134">На панели действий выберите **Создать**, чтобы добавить новую аналитику в сету со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="eae06-134">On the Action Pane, select **New** to add a new dimension to the grid with the following settings:</span></span>
    - <span data-ttu-id="eae06-135">**Тип физической аналитики** - *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="eae06-135">**Physical dimension type** - *Packing*</span></span>
    - <span data-ttu-id="eae06-136">**Физические единицы измерения** - *шт.*</span><span class="sxs-lookup"><span data-stu-id="eae06-136">**Physical unit** - *pcs*</span></span>
    - <span data-ttu-id="eae06-137">**Вес** - *4*</span><span class="sxs-lookup"><span data-stu-id="eae06-137">**Weight** - *4*</span></span>
    - <span data-ttu-id="eae06-138">**Единица измерения веса** - *кг*</span><span class="sxs-lookup"><span data-stu-id="eae06-138">**Weight unit** - *kg*</span></span>
    - <span data-ttu-id="eae06-139">**Глубина** - *3*</span><span class="sxs-lookup"><span data-stu-id="eae06-139">**Depth** - *3*</span></span>
    - <span data-ttu-id="eae06-140">**Высота** - *4*</span><span class="sxs-lookup"><span data-stu-id="eae06-140">**Height** - *4*</span></span>
    - <span data-ttu-id="eae06-141">**Ширина** - *3*</span><span class="sxs-lookup"><span data-stu-id="eae06-141">**Width** - *3*</span></span>
    - <span data-ttu-id="eae06-142">**Длина** - *см*</span><span class="sxs-lookup"><span data-stu-id="eae06-142">**Length** - *cm*</span></span>
    - <span data-ttu-id="eae06-143">**Единица измерения объема** - *см3*</span><span class="sxs-lookup"><span data-stu-id="eae06-143">**Volume unit** - *cm3*</span></span>

<span data-ttu-id="eae06-144">Поле **Объем** рассчитывается автоматически на основе параметров **Глубина**, **Высота** и **Ширина**.</span><span class="sxs-lookup"><span data-stu-id="eae06-144">The **Volume** field is automatically calculated based on your **Depth**, **Height**, and **Width** settings.</span></span>

#### <a name="create-a-new-container-type"></a><span data-ttu-id="eae06-145">Создание нового типа контейнеров</span><span class="sxs-lookup"><span data-stu-id="eae06-145">Create a new container type</span></span>

<span data-ttu-id="eae06-146">Перейдите в раздел **Управление складом \> Настройка \> Контейнеры \> Типы контейнеров** и создайте новую запись со следующими настройками:</span><span class="sxs-lookup"><span data-stu-id="eae06-146">Go to **Warehouse management \> Setup \> Containers \> Container types** and create a new record with the following settings:</span></span>

- <span data-ttu-id="eae06-147">**Код типа контейнера** - *Короткая коробка*</span><span class="sxs-lookup"><span data-stu-id="eae06-147">**Container type code** - *Short Box*</span></span>
- <span data-ttu-id="eae06-148">**Описание** - *Короткая коробка*</span><span class="sxs-lookup"><span data-stu-id="eae06-148">**Description** - *Short Box*</span></span>
- <span data-ttu-id="eae06-149">**Максимальный вес нетто** - *50*</span><span class="sxs-lookup"><span data-stu-id="eae06-149">**Maximum net weight** - *50*</span></span>
- <span data-ttu-id="eae06-150">**Объем** - *144*</span><span class="sxs-lookup"><span data-stu-id="eae06-150">**Volume** - *144*</span></span>
- <span data-ttu-id="eae06-151">**Длина** - *6*</span><span class="sxs-lookup"><span data-stu-id="eae06-151">**Length** - *6*</span></span>
- <span data-ttu-id="eae06-152">**Ширина** - *6*</span><span class="sxs-lookup"><span data-stu-id="eae06-152">**Width** - *6*</span></span>
- <span data-ttu-id="eae06-153">**Высота** - *4*</span><span class="sxs-lookup"><span data-stu-id="eae06-153">**Height** - *4*</span></span>

#### <a name="create-a-container-group"></a><span data-ttu-id="eae06-154">Создание группы контейнеров</span><span class="sxs-lookup"><span data-stu-id="eae06-154">Create a container group</span></span>

<span data-ttu-id="eae06-155">Перейдите в раздел **Управление складом \> Настройка \> Контейнеры \> Группы контейнеров** и создайте новую запись со следующими настройками:</span><span class="sxs-lookup"><span data-stu-id="eae06-155">Go to **Warehouse management \> Setup \> Containers \> Container groups** and create a new record with the following settings:</span></span>

- <span data-ttu-id="eae06-156">**Код группы контейнеров** - *Короткая коробка*</span><span class="sxs-lookup"><span data-stu-id="eae06-156">**Container group ID** - *Short Box*</span></span>
- <span data-ttu-id="eae06-157">**Описание** - *Короткая коробка*</span><span class="sxs-lookup"><span data-stu-id="eae06-157">**Description** - *Short Box*</span></span>

<span data-ttu-id="eae06-158">Добавьте новую строку в раздел **Сведения**.</span><span class="sxs-lookup"><span data-stu-id="eae06-158">Add a new line to the **Details** section.</span></span> <span data-ttu-id="eae06-159">Установите в поле **Тип контейнера** значение *Короткая коробка*.</span><span class="sxs-lookup"><span data-stu-id="eae06-159">Set the **Container type** to *Short Box*.</span></span>

#### <a name="set-up-a-container-build-template"></a><span data-ttu-id="eae06-160">Настройка шаблона сборки контейнера</span><span class="sxs-lookup"><span data-stu-id="eae06-160">Set up a container build template</span></span>

<span data-ttu-id="eae06-161">Перейдите в раздел **Управление складом \> Настройка \> Контейнеры \> Шаблоны создания контейнера** и выберите **Коробки**.</span><span class="sxs-lookup"><span data-stu-id="eae06-161">Go to **Warehouse management \> Setup \> Containers \> Container build templates** and select **Boxes**.</span></span> <span data-ttu-id="eae06-162">Измените **Код группы контейнеров** на *Короткая коробка*.</span><span class="sxs-lookup"><span data-stu-id="eae06-162">Change the **Container group ID** to *Short Box*.</span></span>

### <a name="run-the-scenario"></a><span data-ttu-id="eae06-163">Выполнение сценария</span><span class="sxs-lookup"><span data-stu-id="eae06-163">Run the scenario</span></span>

<span data-ttu-id="eae06-164">После подготовки системы, как описано в предыдущем разделе, можно приступать к запуску сценария, как описано в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="eae06-164">After you have prepared your system as described in the previous section, you are ready to run the scenario as described in the next section.</span></span>

#### <a name="create-a-sales-order-and-create-a-shipment"></a><span data-ttu-id="eae06-165">Создание заказа на продажу и создание отгрузки</span><span class="sxs-lookup"><span data-stu-id="eae06-165">Create a sales order and create a shipment</span></span>

<span data-ttu-id="eae06-166">В этом процессе вы создадите отгрузку на основе аналитик *упаковка* номенклатур, высота которых меньше 3.</span><span class="sxs-lookup"><span data-stu-id="eae06-166">In this process you will create a shipment based on the item *packing* dimensions, for which the height is less than 3.</span></span>

1. <span data-ttu-id="eae06-167">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="eae06-167">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="eae06-168">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="eae06-168">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="eae06-169">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="eae06-169">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="eae06-170">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="eae06-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="eae06-171">**Склад:** *63*</span><span class="sxs-lookup"><span data-stu-id="eae06-171">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="eae06-172">Выберите **ОК**, чтобы создать заказ на продажу и закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="eae06-172">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="eae06-173">Открывается новый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="eae06-173">The new sales order is opened.</span></span> <span data-ttu-id="eae06-174">Он должно включать новую пустую строку в сетке на экспресс-вкладке **Строки заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="eae06-174">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="eae06-175">В этой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="eae06-175">On this line, set the following values:</span></span>

    - <span data-ttu-id="eae06-176">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="eae06-176">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="eae06-177">**Количество:** *5*</span><span class="sxs-lookup"><span data-stu-id="eae06-177">**Quantity:** *5*</span></span>

1. <span data-ttu-id="eae06-178">На экспресс-вкладке **Строки заказа на продажу** выберите **Запасы \> Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="eae06-178">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="eae06-179">На странице **Резервирование** на панели операций выберите **Резервирование лота** для резервирования запасов.</span><span class="sxs-lookup"><span data-stu-id="eae06-179">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="eae06-180">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="eae06-180">Close the page.</span></span>
1. <span data-ttu-id="eae06-181">На панели операций откройте вкладку **Склад** и выберите вариант **Выпустить на склад**, чтобы создать работу для склада.</span><span class="sxs-lookup"><span data-stu-id="eae06-181">On the Action Pane, open the **Warehouse** tab and select **Release to warehouse** to create work for the warehouse.</span></span>
1. <span data-ttu-id="eae06-182">На экспресс-вкладке **Строки заказа на продажу** выберите **Склад \> Сведения об отгрузке**.</span><span class="sxs-lookup"><span data-stu-id="eae06-182">On the **Sales order lines** FastTab, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="eae06-183">На панели действий откройте вкладку **Транспортировка** и выберите **Просмотреть контейнеры**.</span><span class="sxs-lookup"><span data-stu-id="eae06-183">On the Action Pane, open the **Transportation** tab and select **View containers**.</span></span> <span data-ttu-id="eae06-184">Убедитесь, что номенклатура был помещена в два контейнера *Короткая коробка*.</span><span class="sxs-lookup"><span data-stu-id="eae06-184">Confirm that the item was containerized into the two *Short Box* containers.</span></span>

#### <a name="place-an-item-into-storage"></a><span data-ttu-id="eae06-185">Помещение номенклатуры в хранилище</span><span class="sxs-lookup"><span data-stu-id="eae06-185">Place an item into storage</span></span>

1. <span data-ttu-id="eae06-186">Откройте мобильное устройство, выполните вход на склад 63 и перейдите в раздел **Запасы \> Корректировать в**.</span><span class="sxs-lookup"><span data-stu-id="eae06-186">Open the mobile device, sign in to warehouse 63 and go to **Inventory \> Adjust In**.</span></span>
1. <span data-ttu-id="eae06-187">Введите **Местоположение** = *SHORT-01*.</span><span class="sxs-lookup"><span data-stu-id="eae06-187">Enter **Loc** = *SHORT-01*.</span></span> <span data-ttu-id="eae06-188">Создайте новое грузоместо со значениями **Номенклатура** = *A0001* и **Количество** = *1 шт.*</span><span class="sxs-lookup"><span data-stu-id="eae06-188">Make a new license plate with **Item** = *A0001* and **Quantity** = *1 pcs*.</span></span>
1. <span data-ttu-id="eae06-189">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="eae06-189">Select **OK**.</span></span> <span data-ttu-id="eae06-190">Будет выведено сообщение об ошибке "Ошибка местоположения SHORT-01, так как номенклатура A0001 не помещается в указанные аналитики местоположения".</span><span class="sxs-lookup"><span data-stu-id="eae06-190">You will receive the error "Location SHORT-01 failed because item A0001 does not fit in location's specified dimensions."</span></span> <span data-ttu-id="eae06-191">Это связано с тем, что аналитики типа *Хранение* продукта больше аналитик, указанных в профиле местоположения.</span><span class="sxs-lookup"><span data-stu-id="eae06-191">This is because the *Storage* type dimensions of the product are larger than the dimensions specified on the location profile.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]