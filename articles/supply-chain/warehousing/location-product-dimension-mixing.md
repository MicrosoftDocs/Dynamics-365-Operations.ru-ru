---
title: Смешивание аналитик продуктов в местонахождении
description: В этой теме содержится информация о смешивании аналитик продуктов в местонахождении. Эта функция профиля местонахождения помогает улучшить управление местоположением при использовании вариантов продуктов или продуктов, имеющих аналитики, например, в индустрии моды. Она позволяет определить, могут ли быть смешаны конфигурации, цвета, стили и размеры для конкретного профиля местоположения, или же можно поместить только одну из этих аналитик или их комбинацию в одно и то же местонахождение.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: b0309c7a7240d7cac9e5b5724a028f2dc70199e4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217037"
---
# <a name="location-product-dimension-mixing"></a><span data-ttu-id="b89c1-105">Смешивание аналитик продуктов в местонахождении</span><span class="sxs-lookup"><span data-stu-id="b89c1-105">Location product dimension mixing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b89c1-106">Смешивание аналитик продуктов в местонахождении — это функция профиля местонахождения, которая помогает улучшить управление местоположением при использовании вариантов продуктов или продуктов, имеющих аналитики, например, в индустрии моды.</span><span class="sxs-lookup"><span data-stu-id="b89c1-106">Location product dimension mixing is location profile functionality that helps improve location management when product variants or products that have dimensions are used, such as in the fashion industry.</span></span> <span data-ttu-id="b89c1-107">Она позволяет определить, могут ли быть смешаны конфигурации, цвета, стили и размеры для конкретного профиля местоположения, или же можно поместить только одну из этих аналитик или их комбинацию в одно и то же местонахождение.</span><span class="sxs-lookup"><span data-stu-id="b89c1-107">It lets you decide whether configurations, colors, styles, and sizes can be mixed for a specific location profile, or whether just one of these dimensions or a combination of them can be put to the same location.</span></span>

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a><span data-ttu-id="b89c1-108">Включение функции смешивания аналитики продуктов в местонахождении</span><span class="sxs-lookup"><span data-stu-id="b89c1-108">Turn on the Location product dimension mixing feature</span></span>

<span data-ttu-id="b89c1-109">Прежде чем использовать функцию смешивания аналитики продуктов в местонахождении, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="b89c1-109">Before you can use location product dimension mixing, the feature must be turned on in your system.</span></span> <span data-ttu-id="b89c1-110">Администраторы могут использовать рабочую область [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="b89c1-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b89c1-111">В этом случае функция указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b89c1-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b89c1-112">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="b89c1-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b89c1-113">**Имя функции:** *Смешивание аналитики продуктов в местонахождении*</span><span class="sxs-lookup"><span data-stu-id="b89c1-113">**Feature name:** *Location product dimension mixing*</span></span>

## <a name="setup"></a><span data-ttu-id="b89c1-114">Настройка</span><span class="sxs-lookup"><span data-stu-id="b89c1-114">Setup</span></span>

<span data-ttu-id="b89c1-115">Каждое местоположение склада должно иметь связанный с ним профиль местоположения, описывающий свойства местоположения.</span><span class="sxs-lookup"><span data-stu-id="b89c1-115">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location.</span></span> <span data-ttu-id="b89c1-116">Таким образом, все местоположения, использующие один и тот же профиль местоположения, смогут разрешать смешивание аналитики продуктов после ее настройки.</span><span class="sxs-lookup"><span data-stu-id="b89c1-116">Therefore, all locations that use the same location profile will be able to allow product dimension mixing after it has been set up.</span></span>

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a><span data-ttu-id="b89c1-117">Настройка профилей местоположений для разрешения смешивания аналитик продуктов</span><span class="sxs-lookup"><span data-stu-id="b89c1-117">Configure location profiles to allow product dimension mixing</span></span>

1. <span data-ttu-id="b89c1-118">Перейдите в раздел **Управление складом \> Настройка \> Склад \> Профили местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-118">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="b89c1-119">В списке профилей местоположения выберите **НАВГРУЗ**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-119">In the list of location profiles, select **BULK**.</span></span>
1. <span data-ttu-id="b89c1-120">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-120">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b89c1-121">На экспресс-вкладке **Общие** установите для параметра **Включить смешивание аналитик продуктов в местонахождении** значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="b89c1-121">On the **General** FastTab, set the **Enable location product dimension specific mixing** option to *Yes*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b89c1-122">Можно установить для этого параметра значение *Да* только в том случае, если для параметра **Разрешить смешанные номенклатуры** установлено значение *Нет*.</span><span class="sxs-lookup"><span data-stu-id="b89c1-122">You can set this option to *Yes* only if the **Allow mixed items** option is set to *No*.</span></span>

1. <span data-ttu-id="b89c1-123">На экспресс-вкладке **Разрешенное смешивание номенклатур продуктов** установите для параметра **Размер** значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="b89c1-123">On the **Allowed product dimension mixing** FastTab, set the **Size** option to *Yes*.</span></span> <span data-ttu-id="b89c1-124">В сценарии, описанном в этом разделе, смешивание может выполняться только для продуктов с различной аналитикой **Размер**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-124">In the scenario that is described in this topic, mixing can be done only for products that have different **Size** dimensions.</span></span> <span data-ttu-id="b89c1-125">Однако также доступны и другие варианты.</span><span class="sxs-lookup"><span data-stu-id="b89c1-125">However, other options are also available.</span></span>
1. <span data-ttu-id="b89c1-126">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-126">Select **Save**.</span></span>

### <a name="create-a-new-product-master-and-product-variants"></a><span data-ttu-id="b89c1-127">Создайте новый шаблон продукта и варианты продукта.</span><span class="sxs-lookup"><span data-stu-id="b89c1-127">Create a new product master and product variants</span></span>

1. <span data-ttu-id="b89c1-128">Перейдите в раздел **Управление сведениями о продукте \> Продукты \> Шаблоны продукта**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-128">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="b89c1-129">На панели операций выберите **Создать** для создания шаблона продукта.</span><span class="sxs-lookup"><span data-stu-id="b89c1-129">On the Action Pane, select **New** to create a product master.</span></span>
1. <span data-ttu-id="b89c1-130">В диалоговом окне **Создать продукт** задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b89c1-130">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b89c1-131">**Тип продукта:** *Номенклатура*</span><span class="sxs-lookup"><span data-stu-id="b89c1-131">**Product type:** *Item*</span></span>
    - <span data-ttu-id="b89c1-132">**Подтип продукта:** *Шаблон продукта*</span><span class="sxs-lookup"><span data-stu-id="b89c1-132">**Product subtype:** *Product master*</span></span>
    - <span data-ttu-id="b89c1-133">**Номер продукта:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="b89c1-133">**Product number:** *B0001*</span></span>
    - <span data-ttu-id="b89c1-134">**Название продукта:** *Размер B0001*</span><span class="sxs-lookup"><span data-stu-id="b89c1-134">**Product name:** *B0001 Size*</span></span>
    - <span data-ttu-id="b89c1-135">**Группа аналитик продуктов:** *Размер*</span><span class="sxs-lookup"><span data-stu-id="b89c1-135">**Product dimension group:** *Size*</span></span>
    - <span data-ttu-id="b89c1-136">**Метод конфигурации:** *Заранее определенный вариант*</span><span class="sxs-lookup"><span data-stu-id="b89c1-136">**Configuration technology:** *Predefined variant*</span></span>

1. <span data-ttu-id="b89c1-137">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-137">Select **OK**.</span></span>
1. <span data-ttu-id="b89c1-138">На странице **Сведения о продукте** на экспресс-вкладке **Общие** задайте следующие значения.</span><span class="sxs-lookup"><span data-stu-id="b89c1-138">On the **Product details** page, on the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b89c1-139">**Автоматическое создание вариантов:** *Да*</span><span class="sxs-lookup"><span data-stu-id="b89c1-139">**Generate variants automatically:** *Yes*</span></span>
    - <span data-ttu-id="b89c1-140">**Группа размеров:** *CASUALDHIR*</span><span class="sxs-lookup"><span data-stu-id="b89c1-140">**Size group:** *CASUALDHIR*</span></span>

1. <span data-ttu-id="b89c1-141">Для просмотра предопределенных вариантов на панели операций выберите **Варианты продукта**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-141">To view the predefined variants, on the Action Pane, select **Product variants**.</span></span>

    <span data-ttu-id="b89c1-142">Отображается страница **Варианты продукта**, на которой отображается список вариантов из конфигурации группы размеров.</span><span class="sxs-lookup"><span data-stu-id="b89c1-142">The **Product variants** page appears and shows a list of variants from the configuration of the size group.</span></span>

### <a name="release-products-to-the-usmf-company"></a><span data-ttu-id="b89c1-143">Выпустите продукты в компанию USMF</span><span class="sxs-lookup"><span data-stu-id="b89c1-143">Release products to the USMF company</span></span>

1. <span data-ttu-id="b89c1-144">В области операций выберите **Использовать продукты**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-144">On the Action Pane, select **Release products**.</span></span>
1. <span data-ttu-id="b89c1-145">На странице **Выбор продуктов для выпуска** проверьте, что в списке указан номер продукта *B0001*, затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-145">On the **Select products to release** page, confirm that product number *B0001* is in the list, and then select **Next**.</span></span>
1. <span data-ttu-id="b89c1-146">Выберите **Далее**, чтобы подтвердить варианты продукта для выпуска.</span><span class="sxs-lookup"><span data-stu-id="b89c1-146">Select **Next** to confirm the product variants to release.</span></span>
1. <span data-ttu-id="b89c1-147">На странице **Выбор компаний для выпуска** выберите *USMF*, затем выберите **Далее**, чтобы подтвердить выбор.</span><span class="sxs-lookup"><span data-stu-id="b89c1-147">On the **Select companies to release to** page, select *USMF*, and then select **Next** to confirm the selection.</span></span>
1. <span data-ttu-id="b89c1-148">На странице **Подтвердить выбор** выберите **Готово**, чтобы завершить выпуск.</span><span class="sxs-lookup"><span data-stu-id="b89c1-148">On the **Confirm selection** page, select **Finish** to complete the release.</span></span>

    <span data-ttu-id="b89c1-149">Вы получаете сообщение "Операция завершена".</span><span class="sxs-lookup"><span data-stu-id="b89c1-149">You receive an "Operation completed" message.</span></span>

### <a name="update-a-released-product-in-the-usmf-company"></a><span data-ttu-id="b89c1-150">Обновление выпущенного продукта в компании USMF</span><span class="sxs-lookup"><span data-stu-id="b89c1-150">Update a released product in the USMF company</span></span>

1. <span data-ttu-id="b89c1-151">Убедитесь, что вы выполнили вход в компанию **USMF**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-151">Make sure that you're signed in to the **USMF** company.</span></span>
1. <span data-ttu-id="b89c1-152">Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**, чтобы завершить создание выпущенного продукта.</span><span class="sxs-lookup"><span data-stu-id="b89c1-152">Go to **Product information management \> Products \> Released products** to finish creating the released product.</span></span>
1. <span data-ttu-id="b89c1-153">Найдите и выберите код номенклатуры *B0001*, чтобы открыть страницу **Сведения о выпущенном продукте**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-153">Find and select item number *B0001* to open the **Released product details** page.</span></span>
1. <span data-ttu-id="b89c1-154">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-154">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b89c1-155">На экспресс-вкладке **Общие** убедитесь, что в поле **Группа моделей номенклатуры** установлено значение *ФИФО*.</span><span class="sxs-lookup"><span data-stu-id="b89c1-155">On the **General** FastTab, make sure that the **Item model group** field is set to *FIFO*.</span></span>
1. <span data-ttu-id="b89c1-156">На панели операций на вкладке **Продукт** в группе **Настройка** выберите **Группы аналитики**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-156">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Dimension groups**.</span></span>
1. <span data-ttu-id="b89c1-157">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b89c1-157">Set the following values:</span></span>

    - <span data-ttu-id="b89c1-158">**Группа аналитик хранения:** *Товары*</span><span class="sxs-lookup"><span data-stu-id="b89c1-158">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="b89c1-159">**Группа аналитик отслеживания:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="b89c1-159">**Tracking dimension group:** *None*</span></span>

1. <span data-ttu-id="b89c1-160">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-160">Select **OK**.</span></span>
1. <span data-ttu-id="b89c1-161">На панели операций на вкладке **Продукт** в группе **Настройка** выберите **Иерархия резервирования**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-161">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Reservation hierarchy**.</span></span>
1. <span data-ttu-id="b89c1-162">Задайте для поля **Иерархия резервирования** значение *По умолчанию*, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-162">Set the **Reservation hierarchy** field to *Default*, and then select **OK**.</span></span>
1. <span data-ttu-id="b89c1-163">На экспресс-вкладке **Общие** в разделе **Администрирование** обратите внимание, что выбранные параметры были обновлены.</span><span class="sxs-lookup"><span data-stu-id="b89c1-163">On the **General** FastTab, in the **Administration** section, notice that your selections have been updated.</span></span>
1. <span data-ttu-id="b89c1-164">На экспресс-вкладке **Покупка** в поле **Цена** введите *10*.</span><span class="sxs-lookup"><span data-stu-id="b89c1-164">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="b89c1-165">На экспресс-вкладке **Управление затратами** в поле **Номенклатурная группа** введите *Аудио*.</span><span class="sxs-lookup"><span data-stu-id="b89c1-165">On the **Manage costs** FastTab, in the **Item group** field, enter *Audio*.</span></span>
1. <span data-ttu-id="b89c1-166">На экспресс-вкладке **Покупка** в поле **Цена** введите *10*.</span><span class="sxs-lookup"><span data-stu-id="b89c1-166">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="b89c1-167">На экспресс-вкладке **Склад** в поле **Код группы упорядочения единиц** введите *шт.*</span><span class="sxs-lookup"><span data-stu-id="b89c1-167">On the **Warehouse** FastTab, in the **Unit sequence group ID** field, enter *ea*.</span></span>
1. <span data-ttu-id="b89c1-168">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-168">Select **Save**.</span></span>

### <a name="create-a-location-directive"></a><span data-ttu-id="b89c1-169">Создание директивы местонахождения</span><span class="sxs-lookup"><span data-stu-id="b89c1-169">Create a location directive</span></span>

1. <span data-ttu-id="b89c1-170">Перейдите в раздел **Управление складом \> Настройка \> Директивы местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-170">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b89c1-171">В левой области в поле **Тип заказа на работу** выберите *Заказ на покупку*.</span><span class="sxs-lookup"><span data-stu-id="b89c1-171">In the left pane, in the **Work order type** field, select *Purchase orders*.</span></span>
1. <span data-ttu-id="b89c1-172">В списке выберите директиву местонахождения с именем *24 Прямая по заказу на покупку*.</span><span class="sxs-lookup"><span data-stu-id="b89c1-172">In the list, select the location directive that is named *24 PO Direct*.</span></span>
1. <span data-ttu-id="b89c1-173">На экспресс-вкладке **Действия директивы местоположения** выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="b89c1-173">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b89c1-174">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b89c1-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b89c1-175">**Порядковый номер**: *1*</span><span class="sxs-lookup"><span data-stu-id="b89c1-175">**Sequence number:** *1*</span></span>

        <span data-ttu-id="b89c1-176">Новая строка должна находиться перед предыдущей существующей строкой.</span><span class="sxs-lookup"><span data-stu-id="b89c1-176">The new line should be in front of the previously existing line.</span></span> <span data-ttu-id="b89c1-177">Чтобы внести изменения, воспользуйтесь кнопками **Вверх** и **Вниз** на панели инструментов, либо измените значение в поле **Порядковый номер** существующей строки на *2*.</span><span class="sxs-lookup"><span data-stu-id="b89c1-177">To make the change, use the **Move up** and **Move down** buttons on the toolbar, or change the existing line's **Sequence number** value to *2*.</span></span>

    - <span data-ttu-id="b89c1-178">**Имя:** *Поместить в профиль местоположения НАВГРУЗ*</span><span class="sxs-lookup"><span data-stu-id="b89c1-178">**Name:** *Put to BULK Location profile*</span></span>
    - <span data-ttu-id="b89c1-179">**Использование фиксированного местоположения:** *Фиксированные и нефиксированные местонахождения*</span><span class="sxs-lookup"><span data-stu-id="b89c1-179">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>
    - <span data-ttu-id="b89c1-180">**Разрешить отрицательные запасы:** *Снять этот флажок (=Нет)*</span><span class="sxs-lookup"><span data-stu-id="b89c1-180">**Allow negative inventory:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="b89c1-181">**Пакетная обработка активирована:** *Снять этот флажок (=Нет)*</span><span class="sxs-lookup"><span data-stu-id="b89c1-181">**Batch enabled:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="b89c1-182">**Стратегия:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="b89c1-182">**Strategy:** *None*</span></span>

1. <span data-ttu-id="b89c1-183">Пока новая строка остается выбранной, выберите **Изменить запрос** над сеткой.</span><span class="sxs-lookup"><span data-stu-id="b89c1-183">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="b89c1-184">В диалоговом окне запроса на вкладке **Диапазон** выберите **Добавить**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="b89c1-184">In the query dialog box, on the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="b89c1-185">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b89c1-185">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b89c1-186">**Таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="b89c1-186">**Table:** *Locations*</span></span>
    - <span data-ttu-id="b89c1-187">**Производная таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="b89c1-187">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="b89c1-188">**Поле:** *Код профиля местонахождения*</span><span class="sxs-lookup"><span data-stu-id="b89c1-188">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="b89c1-189">**Критерии:** *BULK*</span><span class="sxs-lookup"><span data-stu-id="b89c1-189">**Criteria:** *BULK*</span></span>

1. <span data-ttu-id="b89c1-190">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-190">Select **OK**.</span></span>
1. <span data-ttu-id="b89c1-191">На странице **Директивы местоположения** на панели действий выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-191">On the **Location directives** page, on the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="b89c1-192">В экспресс-вкладке **Действия директивы местоположения** в поле **Стратегия** если используется стратегия местоположения *Консолидация*, настройка экспресс-вкладки **Разрешенное смешивание номенклатур продуктов** в **Профили местоположения** будет переопределена, и номенклатуры будут помещены в то же местоположение даже в том случае, если это действие не разрешено данной настройкой.</span><span class="sxs-lookup"><span data-stu-id="b89c1-192">On the **Location Directive Actions** FastTab **Strategy** field, if you use the *Consolidate* location strategy, the setup of the **Allowed product dimension mixing** FastTab on the **Location profiles** will be overridden, and items will be put to the same location even if this behavior isn't allowed by the setup.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="b89c1-193">Создание элемента меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="b89c1-193">Create a mobile device menu item</span></span>

1. <span data-ttu-id="b89c1-194">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-194">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="b89c1-195">На панели операций выберите **Создать** для создания пункта меню для использования для сортировки.</span><span class="sxs-lookup"><span data-stu-id="b89c1-195">On the Action Pane, select **New** to create a menu item to use for sorting.</span></span>
1. <span data-ttu-id="b89c1-196">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b89c1-196">In the header, set the following values:</span></span>

    - <span data-ttu-id="b89c1-197">**Название пункта меню:** *Получение строки заказа на покупку*</span><span class="sxs-lookup"><span data-stu-id="b89c1-197">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="b89c1-198">**Заголовок:** *Получение строки заказа на покупку*</span><span class="sxs-lookup"><span data-stu-id="b89c1-198">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="b89c1-199">**Режим:** *Работа*</span><span class="sxs-lookup"><span data-stu-id="b89c1-199">**Mode:** *Work*</span></span>
    - <span data-ttu-id="b89c1-200">**Использовать существующую работу:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="b89c1-200">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="b89c1-201">На экспресс-вкладке **Общие** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="b89c1-201">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b89c1-202">**Процесс создания работы:** *Получение строки заказа на покупку и размещение*</span><span class="sxs-lookup"><span data-stu-id="b89c1-202">**Work creation process:** *Purchase order line receiving and putaway*</span></span>
    - <span data-ttu-id="b89c1-203">**Создать грузоместо:** *Да*</span><span class="sxs-lookup"><span data-stu-id="b89c1-203">**Generate license plate:** *Yes*</span></span>

1. <span data-ttu-id="b89c1-204">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-204">Select **Save**.</span></span>

### <a name="configure-the-mobile-device-menu"></a><span data-ttu-id="b89c1-205">Настройка меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="b89c1-205">Configure the mobile device menu</span></span>

1. <span data-ttu-id="b89c1-206">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="b89c1-207">В списке меню выберите **Входящие**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-207">In the list of menus, select **Inbound**.</span></span>
1. <span data-ttu-id="b89c1-208">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-208">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b89c1-209">В списке **Доступные меню и пункты меню** найдите и выберите пункт меню **Получение строки заказа на покупку**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-209">In the **Available Menus And Menu Items** list, find and select the **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="b89c1-210">Нажмите кнопку со стрелкой вправо, чтобы переместить пункт меню **Получение строки заказа на покупку** в список **Структура меню**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-210">Select the right arrow button to move the **PO line receiving** menu item to the **Menu Structure** list.</span></span> <span data-ttu-id="b89c1-211">Таким образом, вы добавляете новый пункт меню в выбранное меню.</span><span class="sxs-lookup"><span data-stu-id="b89c1-211">In this way, you add your new menu item to the selected menu.</span></span>
1. <span data-ttu-id="b89c1-212">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-212">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="b89c1-213">Сценарий</span><span class="sxs-lookup"><span data-stu-id="b89c1-213">Scenario</span></span>

<span data-ttu-id="b89c1-214">В этом демонстрационном сценарии показано, как можно поместить два различных варианта продукта в одно и то же местонахождение, когда профиль местоположения не допускает смешанных номенклатур, но включена функция *Смешивание аналитик продуктов в местонахождении*.</span><span class="sxs-lookup"><span data-stu-id="b89c1-214">This demo scenario shows how two different product variants can be put to the same location when the location profile doesn't allow for mixed items, but the *Location product dimension mixing* feature is enabled.</span></span> <span data-ttu-id="b89c1-215">В этом случае в качестве критерия будет использоваться вариант **Размер**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-215">In this case, you will use the **Size** variant as the criterion.</span></span>

<span data-ttu-id="b89c1-216">Прежде чем начать, убедитесь, что на складе *24* имеются пустые местонахождения, в которых используется профиль местоположения *НАВГРУЗ*.</span><span class="sxs-lookup"><span data-stu-id="b89c1-216">Before you begin, make sure that there are empty locations in warehouse *24* that use the *BULK* location profile.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="b89c1-217">Создание заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="b89c1-217">Create a purchase order</span></span>

<span data-ttu-id="b89c1-218">Будет создан заказ на покупку, имеющий три строки: две строки для одного и того же номера продукта, но разных вариантов **Размер**, и третью строку для другого продукта без вариантов.</span><span class="sxs-lookup"><span data-stu-id="b89c1-218">You will create a purchase order that has three lines: two lines for the same product number but different **Size** variants, and a third line for a different product that has no variants.</span></span>

1. <span data-ttu-id="b89c1-219">Перейдите в раздел **Расчеты с поставщиками \> Заказы на покупку \> Все заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-219">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="b89c1-220">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-220">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b89c1-221">В диалоговом окне **Создание заказа на покупку** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b89c1-221">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b89c1-222">**Счет поставщика:** *1001*</span><span class="sxs-lookup"><span data-stu-id="b89c1-222">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="b89c1-223">**Склад:** *24*</span><span class="sxs-lookup"><span data-stu-id="b89c1-223">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="b89c1-224">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-224">Select **OK**.</span></span>
1. <span data-ttu-id="b89c1-225">Создается заказ на покупку, и на экспресс-вкладке **Строки заказа на покупку** добавляется новая строка.</span><span class="sxs-lookup"><span data-stu-id="b89c1-225">The purchase order is created, and a new line is added on the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="b89c1-226">Запишите номер заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="b89c1-226">Make a note of the purchase order number.</span></span>
1. <span data-ttu-id="b89c1-227">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b89c1-227">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b89c1-228">**Код номенклатуры:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="b89c1-228">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="b89c1-229">**Размер** *L*</span><span class="sxs-lookup"><span data-stu-id="b89c1-229">**Size** *L*</span></span>
    - <span data-ttu-id="b89c1-230">**Количество:** *2*</span><span class="sxs-lookup"><span data-stu-id="b89c1-230">**Quantity:** *2*</span></span>

1. <span data-ttu-id="b89c1-231">Выберите **Добавить строку** над сеткой, чтобы добавить вторую строку заказа на покупку, и установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b89c1-231">Select **Add line** above the grid to add a second purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="b89c1-232">**Код номенклатуры:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="b89c1-232">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="b89c1-233">**Размер** *XL*</span><span class="sxs-lookup"><span data-stu-id="b89c1-233">**Size** *XL*</span></span>
    - <span data-ttu-id="b89c1-234">**Количество:** *2*</span><span class="sxs-lookup"><span data-stu-id="b89c1-234">**Quantity:** *2*</span></span>

1. <span data-ttu-id="b89c1-235">Выберите **Добавить строку**, чтобы добавить третью строку заказа на покупку, и установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b89c1-235">Select **Add line** to add a third purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="b89c1-236">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b89c1-236">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="b89c1-237">**Количество:** *1*</span><span class="sxs-lookup"><span data-stu-id="b89c1-237">**Quantity:** *1*</span></span>

<span data-ttu-id="b89c1-238">1. Выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-238">1.Select **Save**.</span></span>

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a><span data-ttu-id="b89c1-239">Получение строк заказа на покупку в приложении склада</span><span class="sxs-lookup"><span data-stu-id="b89c1-239">Receive purchase order lines in the warehouse app</span></span>

1. <span data-ttu-id="b89c1-240">Выполните вход в приложение склада в качестве пользователя, который имеет доступ к складу *24*.</span><span class="sxs-lookup"><span data-stu-id="b89c1-240">Sign in to the warehouse app as a user who is enabled for warehouse *24*.</span></span>
1. <span data-ttu-id="b89c1-241">Выберите меню **Входящий**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-241">Select the **Inbound** menu.</span></span>
1. <span data-ttu-id="b89c1-242">Выберите **Получение строки заказа на покупку**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-242">Select **PO Line receiving**.</span></span>
1. <span data-ttu-id="b89c1-243">Выберите поле **PONUM**, затем введите номер заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="b89c1-243">Select the **PONUM** field, and then enter the purchase order number.</span></span>
1. <span data-ttu-id="b89c1-244">Подтвердите запись, выбрав кнопку подтверждения (✔) в нижней части страницы.</span><span class="sxs-lookup"><span data-stu-id="b89c1-244">Confirm your entry by selecting the confirm button ( ✔ ) at the bottom of the page.</span></span>
1. <span data-ttu-id="b89c1-245">Введите номер строки из принимаемого заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="b89c1-245">Enter the line number from the purchase order that is being received.</span></span> <span data-ttu-id="b89c1-246">Выберите поле **LINENUM**, затем введите *1* с помощью числовой панели.</span><span class="sxs-lookup"><span data-stu-id="b89c1-246">Select the **LINENUM** field, and then use the number pad to enter *1*.</span></span>
1. <span data-ttu-id="b89c1-247">Подтвердите ввод.</span><span class="sxs-lookup"><span data-stu-id="b89c1-247">Confirm your entry.</span></span>
1. <span data-ttu-id="b89c1-248">Ввод количества для получения.</span><span class="sxs-lookup"><span data-stu-id="b89c1-248">Enter the quantity to receive.</span></span> <span data-ttu-id="b89c1-249">Два раза выберите кнопку знак "плюс" (**+**), чтобы увеличить значение в поле **Кол-во** до значения *2*.</span><span class="sxs-lookup"><span data-stu-id="b89c1-249">Select the plus sign (**+**) button two times to increase the value in the **Qty** field to *2*.</span></span>
1. <span data-ttu-id="b89c1-250">Зарегистрируйте запись, выбрав кнопку (✔) в нижней части страницы, затем подтвердите ввод, снова выбрав кнопку (✔).</span><span class="sxs-lookup"><span data-stu-id="b89c1-250">Register your entry by selecting the button ( ✔ ) at the bottom of the page, and then confirm your entry by selecting the button ( ✔ ) again.</span></span>
1. <span data-ttu-id="b89c1-251">Просмотрите информацию на странице **Заказы на покупку: размещение**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-251">View the information on the **Purchase orders: Put** page.</span></span> <span data-ttu-id="b89c1-252">На этой странице отображается работа, которая была создана для размещения (Работа 1).</span><span class="sxs-lookup"><span data-stu-id="b89c1-252">This page shows the work that has been created for the put-away (Work 1).</span></span>

    <span data-ttu-id="b89c1-253">Отображается местоположение, в котором будет размещаться полученная номенклатура, грузоместо, номенклатура, размер и количество задачи **Получение строки заказа на покупку**, которая только что была выполнено.</span><span class="sxs-lookup"><span data-stu-id="b89c1-253">The location where the received item will be put away, the license plate, the item, the size, and the quantity of the **PO Line receiving** task that you just completed are shown.</span></span>

1. <span data-ttu-id="b89c1-254">Подтвердите работу по размещению.</span><span class="sxs-lookup"><span data-stu-id="b89c1-254">Confirm the put-away work.</span></span>
1. <span data-ttu-id="b89c1-255">Повторите шаги с 4 по 11 для строки заказа на покупку 2.</span><span class="sxs-lookup"><span data-stu-id="b89c1-255">Repeat the steps 4 through 11 for the purchase order line 2.</span></span> <span data-ttu-id="b89c1-256">Однако на шаге 8 укажите количество *1*.</span><span class="sxs-lookup"><span data-stu-id="b89c1-256">However, in step 8, specify a quantity of *1*.</span></span>

    <span data-ttu-id="b89c1-257">Новая работа размещения (работа 2) создается для того же местоположения, что и работа 1.</span><span class="sxs-lookup"><span data-stu-id="b89c1-257">New put-away work (Work 2) is created for the same location as Work 1.</span></span>

1. <span data-ttu-id="b89c1-258">Повторите шаги с 4 по 11 снова для строки заказа на покупку 2.</span><span class="sxs-lookup"><span data-stu-id="b89c1-258">Repeat the steps 4 through 11 again for purchase order line 2.</span></span> <span data-ttu-id="b89c1-259">На шаге 8 укажите оставшееся количество *1*.</span><span class="sxs-lookup"><span data-stu-id="b89c1-259">In step 8, specify the remaining quantity of *1*.</span></span>

    <span data-ttu-id="b89c1-260">Новая работа размещения (работа 3) создается для того же местоположения, что и работа 1 и работа 2.</span><span class="sxs-lookup"><span data-stu-id="b89c1-260">New put-away work (Work 3) is created for the same location as Work 1 and Work 2.</span></span> <span data-ttu-id="b89c1-261">Это поведение происходит из-за того, что используется стратегия директивы местоположения *Консолидировать*, а на экспресс-вкладке **Разрешенное смешивание номенклатур продуктов** в настройке *Сборные* **профили местонахождения** разрешается смешивание в местонахождении варианта **Размер**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-261">This behavior occurs because the *Consolidate* location directive strategy is used, and the **Allowed product dimension mixing** FastTab on the *Bulk* **Location profiles** setup allows the **Size** variant to be mixed on a location.</span></span>

1. <span data-ttu-id="b89c1-262">Повторите шаги с 4 по 11 для строки заказа на покупку 3.</span><span class="sxs-lookup"><span data-stu-id="b89c1-262">Repeat the steps 4 through 11 for purchase order line 3.</span></span> <span data-ttu-id="b89c1-263">На шаге 8 укажите количество *1* для кода номенклатуры *A0001*.</span><span class="sxs-lookup"><span data-stu-id="b89c1-263">In step 8, specify a quantity of *1* for item number *A0001*.</span></span>

    <span data-ttu-id="b89c1-264">Новая работа размещения (работа 4) создается для другого местоположения, отличного от местоположения, используемого для строк заказа на покупку 1 и 2.</span><span class="sxs-lookup"><span data-stu-id="b89c1-264">New put-away work (Work 4) is created for a different location than the location that is used for purchase order lines 1 and 2.</span></span> <span data-ttu-id="b89c1-265">Это происходит из-за того, что профиль местоположения не допускает использования смешанных продуктов, но он позволяет использовать смешанные аналитики для одного и того же шаблона продукта.</span><span class="sxs-lookup"><span data-stu-id="b89c1-265">This behavior occurs because the location profile doesn't allow for mixed products, but it does allow for mixed dimensions of the same product master.</span></span>

1. <span data-ttu-id="b89c1-266">Выберите кнопку меню в верхней части страницы (иногда называется "гамбургер" или "кнопка-гамбургер"), затем выберите команду **Отмена**, чтобы выйти из пункта **Получение строки заказа на покупку**.</span><span class="sxs-lookup"><span data-stu-id="b89c1-266">Select the Menu button at the top of the page (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit **PO Line receiving**.</span></span>

> [!TIP]
> <span data-ttu-id="b89c1-267">Можно повторить этот сценарий, но на этот раз задать **Размер** - *Нет* на экспресс-вкладке **Разрешить смешивание номенклатур продуктов** в **профилях местоположения** *НАВГРУЗ*, чтобы ни одна из аналитик продуктов не могла быть смешанной.</span><span class="sxs-lookup"><span data-stu-id="b89c1-267">You can repeat this scenario, but this time, set **Size** - *No* under the **Allow product dimension mixing** FastTab on the *BULK* **Location profiles**, so that none of the product dimensions can be mixed.</span></span> <span data-ttu-id="b89c1-268">В этом случае при получении заказа на покупку каждый вариант продукта будет помещен в новое местоположение.</span><span class="sxs-lookup"><span data-stu-id="b89c1-268">In this case, when you receive the purchase order, each product variant will be put to a new location.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]