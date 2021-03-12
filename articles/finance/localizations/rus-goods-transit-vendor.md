---
title: Товары в пути от поставщика
description: В этой теме приводятся сведения о параметрах и действиях, которые необходимы для акта инвентаризации товаров в транзите (ИНВ-6).
author: anasyash
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: anasyash
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: 8.1.2
ms.openlocfilehash: df8ee4f8a7773737a288bc75352cdd21e456d4cf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990107"
---
# <a name="goods-in-transit-from-vendor-russia"></a><span data-ttu-id="a1b32-103">Товары в пути от поставщика (Россия)</span><span class="sxs-lookup"><span data-stu-id="a1b32-103">Goods in transit from vendor (Russia)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1b32-104">Процесс инвентаризации номенклатуры (ИНВ-6) используется для определения количества и стоимости складских номенклатур, которые находятся в транзите при инвентаризации запасов.</span><span class="sxs-lookup"><span data-stu-id="a1b32-104">The item counting process (INV-6) is used to identify the quantity and value of inventory items that are in transit when inventory is counted.</span></span>

<span data-ttu-id="a1b32-105">Процесс инвентаризации номенклатур выполняется в контексте номенклатур, отгрузочных документов и поставщиков.</span><span class="sxs-lookup"><span data-stu-id="a1b32-105">The item counting process is done in the context of nomenclatures, shipping documents, and vendors.</span></span>

## <a name="set-up-an-inventory-profile-for-a-transferable-item"></a><span data-ttu-id="a1b32-106">Настройка профиля учета для переносимой номенклатуры</span><span class="sxs-lookup"><span data-stu-id="a1b32-106">Set up an inventory profile for a transferable item</span></span>
<span data-ttu-id="a1b32-107">Чтобы отразить товары и материалы в транзите, можно настроить вид запасов для вида деятельности **Основной**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-107">To reflect the goods and materials that are in transit, you can set the kind of inventory for the **Basic** kind of activity.</span></span> <span data-ttu-id="a1b32-108">Поле **Вид запасов** может иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a1b32-108">The **Kind of inventory** field can have the following values:</span></span>

- <span data-ttu-id="a1b32-109">Общий</span><span class="sxs-lookup"><span data-stu-id="a1b32-109">Common</span></span>
- <span data-ttu-id="a1b32-110">Купленные товары в пути</span><span class="sxs-lookup"><span data-stu-id="a1b32-110">Purchased items in route</span></span>

1. <span data-ttu-id="a1b32-111">Перейдите в раздел **Управление запасами** \> **Настройка** \> **Аналитики** \> **Профили учета**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-111">Go to **Inventory management** \> **Setup** \> **Dimensions** \> **Inventory profiles**.</span></span>
2. <span data-ttu-id="a1b32-112">Выберите **Создать**, чтобы создать профиль учета для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="a1b32-112">Select **New** to create an inventory profile for an item.</span></span>
3. <span data-ttu-id="a1b32-113">В поле **Профиль учета** введите имя профиля учета.</span><span class="sxs-lookup"><span data-stu-id="a1b32-113">In the **Inventory profile** field, enter the name of the inventory profile.</span></span>
4. <span data-ttu-id="a1b32-114">В поле **Имя** введите описание профиля учета.</span><span class="sxs-lookup"><span data-stu-id="a1b32-114">In the **Name** field, enter a description of the inventory profile.</span></span>
5. <span data-ttu-id="a1b32-115">На экспресс-вкладке **Настройка** в поле **Вид деятельности** выберите **Основной**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-115">On the **Setup** FastTab, in the **Kind of activity** field, select **Basic**.</span></span>
6. <span data-ttu-id="a1b32-116">Установите для параметра **Не подбирать** значение **Да**, чтобы запретить автоматическое сопоставление запасов в наличии из данного профиля учета с совместимым профилем учета.</span><span class="sxs-lookup"><span data-stu-id="a1b32-116">Set the **Don't match option** to **Yes** to prevent on-hand inventory that uses this inventory profile from being automatically matched with a compatible inventory profile.</span></span>
7. <span data-ttu-id="a1b32-117">В поле **Вид запасов** выберите **Купленные товары в пути**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-117">In the **Kind of inventory** field, select **Purchased items in route**.</span></span> <span data-ttu-id="a1b32-118">Для параметров **Инициализировать аналитику** и **Контролировать аналитику в заказе на покупку** автоматически устанавливается значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-118">The **Initialize dimension** and **Control dimension in purchase order** options are automatically set to **Yes**.</span></span>

> [!NOTE]
> <span data-ttu-id="a1b32-119">Поле **Вид запасов** доступно только в том случае, если выбрано значение **Основной** в поле **Вид деятельности**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-119">The **Kind of inventory** field is available only if you select **Basic** in the **Kind of activity** field.</span></span>

8. <span data-ttu-id="a1b32-120">На экспресс-вкладке **Приоритет подбора** выберите **Вверх** или **Вниз**, чтобы изменить порядок профиля запасов.</span><span class="sxs-lookup"><span data-stu-id="a1b32-120">On the **Matching priority** FastTab, select **Up** or **Down** to change the order of the inventory profile.</span></span>
9. <span data-ttu-id="a1b32-121">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a1b32-121">Select **Save**, and close the page.</span></span>

  ![Страница профилей учета](media/goods-in-transit-vendor-01.png)
 
## <a name="set-up-a-number-sequence-for-the-counting-act-inv-6-report"></a><span data-ttu-id="a1b32-123">Настройка номерной серии для отчета по акту инвентаризации (ИНВ-6)</span><span class="sxs-lookup"><span data-stu-id="a1b32-123">Set up a number sequence for the Counting act (INV-6) report</span></span>

1. <span data-ttu-id="a1b32-124">Перейдите в раздел **Управление запасами** \> **Настройка** \> **Параметры управления запасами и складами**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-124">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="a1b32-125">На вкладке **Номерные серии** в поле **Код номерной серии** выберите номерную серию для ссылки **Акт инвентаризации (ИНВ-6)**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-125">On the **Number sequences** tab, in the **Number sequence code** field, select a number sequence for the **Counting act (INV-6)** reference.</span></span>
3. <span data-ttu-id="a1b32-126">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a1b32-126">Select **Save**, and close the page.</span></span>

## <a name="set-up-an-inventory-journal-name-for-the-counting-act-inv-6-report"></a><span data-ttu-id="a1b32-127">Настройка имени журнала инвентаризации запасов для отчета об акте инвентаризации (INV-6)</span><span class="sxs-lookup"><span data-stu-id="a1b32-127">Set up an inventory journal name for the Counting act (INV-6) report</span></span>

1. <span data-ttu-id="a1b32-128">Перейдите в раздел **Управление запасами** \> **Настройка** \> **Имена журналов** \> **Запасы**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-128">Go to **Inventory management** \> **Setup** \> **Journal names** \> **Inventory**.</span></span>
2. <span data-ttu-id="a1b32-129">Создайте имя журнала.</span><span class="sxs-lookup"><span data-stu-id="a1b32-129">Create a journal name.</span></span>
3. <span data-ttu-id="a1b32-130">В поле **Имя** введите имя журнала запасов.</span><span class="sxs-lookup"><span data-stu-id="a1b32-130">In the **Name** field, enter the inventory journal name.</span></span>
4. <span data-ttu-id="a1b32-131">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="a1b32-131">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="a1b32-132">В поле **Тип журнала** выберите **Инвентаризация**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-132">In the **Journal type** field, select **Counting**.</span></span>
6. <span data-ttu-id="a1b32-133">На экспресс-вкладке **Отчеты** в поле **Доступно** выберите **Акт инвентаризации (ИНВ-6)**, затем выберите кнопку со стрелкой влево, чтобы переместить отчет в поле **Выбрано**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-133">On the **Reports** FastTab, in the **Available** field, select **Counting act (INV-6)**, and then select the left arrow button to move the report to the **Selected** field.</span></span>

> [!NOTE]
> <span data-ttu-id="a1b32-134">Если поле **Доступно** пусто, выберите **Обновить** на панели операций, чтобы обновить список доступных отчетов.</span><span class="sxs-lookup"><span data-stu-id="a1b32-134">If the **Available** field is blank, select **Update** on the Action Pane to update the list of available reports.</span></span>

7. <span data-ttu-id="a1b32-135">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a1b32-135">Select **Save**, and close the page.</span></span>

  ![Страница имен журналов запасов](media/goods-in-transit-vendor-2.png)
 
## <a name="add-officials-to-the-counting-act-inv-6-report"></a><span data-ttu-id="a1b32-137">Добавление должностных лиц для отчета "Акт инвентаризации ИНВ-6"</span><span class="sxs-lookup"><span data-stu-id="a1b32-137">Add officials to the Counting act (INV-6) report</span></span>
<span data-ttu-id="a1b32-138">Можно указать должностных лиц компании, участвующих в процессе инвентаризации номенклатур, для отчета **Акт инвентаризации (ИНВ-6)**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-138">You can specify the company officials who are involved in the item counting process for the **Counting act (INV-6)** report.</span></span>

1. <span data-ttu-id="a1b32-139">Откройте **Управление организацией** \> **Настройка** \> **Контакты** \> **Должностные лица**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-139">Go to **Organization administration** \> **Setup** \> **Contacts** \> **Officials**.</span></span>
2. <span data-ttu-id="a1b32-140">На вкладке **Запасы** выберите параметр **Акт инвентаризации (ИНВ-6)**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-140">On the **Inventory** tab, select the **Counting act (INV-6)** option.</span></span>
3. <span data-ttu-id="a1b32-141">Выберите **Создать**, чтобы создать должностное лицо для отчета **Акт инвентаризации (ИНВ-6)**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-141">Select **New** to create an official for the **Counting act (INV-6)** report.</span></span>
4. <span data-ttu-id="a1b32-142">В поле **Должность** выберите назначение должностного лица.</span><span class="sxs-lookup"><span data-stu-id="a1b32-142">In the **Position** field, select the designation of the official.</span></span>
5. <span data-ttu-id="a1b32-143">В поле **Имя** введите имя должностного лица.</span><span class="sxs-lookup"><span data-stu-id="a1b32-143">In the **Name** field, enter the name of the official.</span></span>
6. <span data-ttu-id="a1b32-144">В поле **Название должности** выберите название должности должностного лица.</span><span class="sxs-lookup"><span data-stu-id="a1b32-144">In the **Job title** field, select the job title of the official.</span></span>

> [!NOTE]
> <span data-ttu-id="a1b32-145">По умолчанию название должности копируется из записи выбранного сотрудника.</span><span class="sxs-lookup"><span data-stu-id="a1b32-145">By default, the job title is copied from the selected employee's record.</span></span>
 
  ![Страница должностных лиц](media/goods-in-transit-vendor-03.png)
 
7. <span data-ttu-id="a1b32-147">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a1b32-147">Select **Save**, and close the page.</span></span>

### <a name="create-an-inventory-tracking-dimension-group-for-the-counting-act-inv-6-report"></a><span data-ttu-id="a1b32-148">Создание группы аналитик отслеживания запасов для отчета по акту инвентаризации (ИНВ-6)</span><span class="sxs-lookup"><span data-stu-id="a1b32-148">Create an inventory tracking dimension group for the Counting act (INV-6) report</span></span>

1. <span data-ttu-id="a1b32-149">Откройте **Управление сведениями о продукте** \> **Настройка** \> **Группы аналитик и вариантов** \> **Группы аналитик отслеживания**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-149">Go to **Product information management** \> **Setup** \> **Dimension and variant groups** \> **Tracking dimension groups**.</span></span>
2. <span data-ttu-id="a1b32-150">Выберите **Создать**, чтобы создать группу аналитик.</span><span class="sxs-lookup"><span data-stu-id="a1b32-150">Select **New** to create a dimension group.</span></span>
3. <span data-ttu-id="a1b32-151">В поле **Имя** введите полное имя группы аналитик.</span><span class="sxs-lookup"><span data-stu-id="a1b32-151">In the **Name** field, enter the name of the dimension group.</span></span>
4. <span data-ttu-id="a1b32-152">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="a1b32-152">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="a1b32-153">На экспресс-вкладке **Аналитики отслеживания** в строке **Профиль учета** установите флажки **Активный**, **Первичная аналитика хранения**, **Физические запасы**, **Финансовые запасы**, **План покрытия по аналитикам** и **Перемещение**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-153">On the **Tracking dimensions** FastTab, on the **Inventory profile** line, select the **Active**, **Primary stocking**, **Physical inventory**, **Financial inventory**, **Coverage plan by dimension**, and **Transfer** check boxes.</span></span>
6. <span data-ttu-id="a1b32-154">В строке **Ответственный** установите флажки **Активный**, **Физические запасы**, **Финансовые запасы** и **Перемещение**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-154">On the **Owner** line, select the **Active**, **Physical inventory**, **Financial inventory**, and **Transfer** check boxes.</span></span>

> [!NOTE]
> <span data-ttu-id="a1b32-155">Чтобы в отчете отображались детали отгрузки и платежных документов, в строке **Номер партии** установите флажки **Активный** и **Физические запасы**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-155">To make the report reflect the details of shipping and payment documents, on the **Batch number** line, select the **Active** and **Physical inventory** check boxes.</span></span>

  ![Страница групп аналитик отслеживания](media/goods-in-transit-vendor-04.png)
 
7. <span data-ttu-id="a1b32-157">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-157">Select **Save**.</span></span>

## <a name="create-a-purchase-agreement"></a><span data-ttu-id="a1b32-158">Создание договора покупки</span><span class="sxs-lookup"><span data-stu-id="a1b32-158">Create a purchase agreement</span></span>

1. <span data-ttu-id="a1b32-159">Перейдите в раздел **Расчеты с поставщиками** \> **Заказы на покупку** \> **Договоры покупки**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-159">Go to **Accounts payable** \> **Purchase orders** \> **Purchase agreements**.</span></span>
2. <span data-ttu-id="a1b32-160">Выберите **Создать**, чтобы открыть диалоговое окно **Создание договора покупки**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-160">Select **New** to open the **Create purchase agreement** dialog box.</span></span>
3. <span data-ttu-id="a1b32-161">На экспресс-вкладке **Поставщик** в поле **Счет поставщика** выберите счет поставщика.</span><span class="sxs-lookup"><span data-stu-id="a1b32-161">On the **Vendor** FastTab, in the **Vendor account** field, select the vendor account.</span></span>
4. <span data-ttu-id="a1b32-162">В поле **Классификация договоров покупки** выберите **Общий договор покупки**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-162">In the **Purchase agreement classification** field, select **Blanket purchase agreement**.</span></span>
5. <span data-ttu-id="a1b32-163">На экспресс-вкладке **Общие сведения** в разделе **Документ** в поле **Договор покупки** введите код договора покупки.</span><span class="sxs-lookup"><span data-stu-id="a1b32-163">On the **General** FastTab, in the **Document** section, in the **Purchase agreement** field, enter the ID of the purchase agreement.</span></span>
6. <span data-ttu-id="a1b32-164">Укажите другие сведения, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-164">Specify other details, and then select **OK**.</span></span>
7. <span data-ttu-id="a1b32-165">На странице **Договоры покупки** переключитесь в представление **Заголовок**, затем на экспресс-вкладке **Финансы** в разделе **Профиль учета** настройте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="a1b32-165">On the **Purchase agreements** page, switch to the **Header** view, and then, on the **Financial** FastTab, in the **Inventory profile** section, set the following fields:</span></span>

- <span data-ttu-id="a1b32-166">В поле **Вид деятельности** выберите **Основной**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-166">In the **Kind of activity** field, select **Basic**.</span></span>
- <span data-ttu-id="a1b32-167">В поле **Профиль учета** выберите профиль учета, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="a1b32-167">In the **Inventory profile** field, select the inventory profile that you created earlier.</span></span>
 
  ![Страница договоров покупки](media/goods-in-transit-vendor-05.png)
 
8. <span data-ttu-id="a1b32-169">На панели операций на вкладке **Договор покупки** в группе **Создать** выберите **Подтверждение** для обновления статуса договора покупки до **Действует**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-169">On the Action Pane, on the **Purchase agreement** tab, in the **Generate** group, select **Confirmation** to update the status of the purchase agreement to **Effective**.</span></span>

## <a name="add-an-inventory-owner-to-the-counting-act-inv-6-report"></a><span data-ttu-id="a1b32-170">Добавление владельца запасов в отчет по акту инвентаризации (ИНВ-6)</span><span class="sxs-lookup"><span data-stu-id="a1b32-170">Add an inventory owner to the Counting act (INV-6) report</span></span>

1. <span data-ttu-id="a1b32-171">Перейдите в раздел **Управление запасами** \> **Настройка** \> **Аналитики** \> **Владельцы запасов**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-171">Go to **Inventory management** \> **Setup** \> **Dimensions** \> **Inventory owners**.</span></span>
2. <span data-ttu-id="a1b32-172">Выберите **Создать**, чтобы добавить владельца запасов.</span><span class="sxs-lookup"><span data-stu-id="a1b32-172">Select **New** to add an inventory owner.</span></span>
3. <span data-ttu-id="a1b32-173">В поле **Владелец** введите код владельца.</span><span class="sxs-lookup"><span data-stu-id="a1b32-173">In the **Owner** field, enter the owner code.</span></span>
4. <span data-ttu-id="a1b32-174">В поле **Тип счета** выберите **Поставщик**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-174">In the **Account type** field, select **Vendor**.</span></span>
5. <span data-ttu-id="a1b32-175">В поле **Счет** выберите код принципала.</span><span class="sxs-lookup"><span data-stu-id="a1b32-175">In the **Account** field, select the principal code.</span></span> <span data-ttu-id="a1b32-176">Поле **Имя** заполняется автоматически.</span><span class="sxs-lookup"><span data-stu-id="a1b32-176">The **Name** field is filled in automatically.</span></span>
6. <span data-ttu-id="a1b32-177">В поле **Код договора** выберите договор покупки, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="a1b32-177">In the **Agreement ID** field, select the purchase agreement that you created earlier.</span></span> <span data-ttu-id="a1b32-178">Таким образом, новый владелец связывается с договором.</span><span class="sxs-lookup"><span data-stu-id="a1b32-178">In this way, you associate the new owner with the agreement.</span></span>

  ![Страница владельцев запасов](media/goods-in-transit-vendor-06.png)

7. <span data-ttu-id="a1b32-180">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-180">Select **Save**.</span></span>

## <a name="register-goods-and-materials-that-are-in-transit"></a><span data-ttu-id="a1b32-181">Регистрация товаров и материалов в пути</span><span class="sxs-lookup"><span data-stu-id="a1b32-181">Register goods and materials that are in transit</span></span>

1. <span data-ttu-id="a1b32-182">Создание нового заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="a1b32-182">Create a new purchase order.</span></span> <span data-ttu-id="a1b32-183">В поле **Договор покупки** выберите ранее созданный договор покупки, затем в строке заказа на покупку в поле **Код номенклатуры** выберите код номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="a1b32-183">In the **Purchase agreement** field, select the purchase agreement that you created earlier, and then, on the purchase order line, in the **Item number** field, select the item number.</span></span>

> [!NOTE]
> <span data-ttu-id="a1b32-184">В поле **Аналитика отслеживания** для данной номенклатуры должен быть указан профиль учета, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="a1b32-184">The **Tracking dimension** field for the item should be set to the inventory profile that you created earlier.</span></span>

2. <span data-ttu-id="a1b32-185">На экспресс-вкладке **Сведения по строке** на вкладке **Продукт** в разделе **Аналитика отслеживания** проверьте, что в поле **Профиль учета** выбран профиль учета, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="a1b32-185">On the **Line details** FastTab, on the **Product** tab, in the **Tracking dimension** section, validate that the **Inventory profile** field is set to the inventory profile that you created earlier.</span></span>
3. <span data-ttu-id="a1b32-186">В поле **Владелец** выберите запись, созданную ранее.</span><span class="sxs-lookup"><span data-stu-id="a1b32-186">In the **Owner** field, select the record that you created earlier.</span></span>

  ![Страница заказа на покупку](media/goods-in-transit-vendor-07.png)

4. <span data-ttu-id="a1b32-188">Выполните разноску накладной обычным способом.</span><span class="sxs-lookup"><span data-stu-id="a1b32-188">Post the invoice in the usual way.</span></span>

## <a name="generate-a-counting-act-inv-6-report"></a><span data-ttu-id="a1b32-189">Создание отчета по акту инвентаризации (ИНВ-6)</span><span class="sxs-lookup"><span data-stu-id="a1b32-189">Generate a Counting act (INV-6) report</span></span>
<span data-ttu-id="a1b32-190">Можно использовать диалоговое окно **Печать акта инвентаризации (ИНВ-6)** для создания отчета **Акт инвентаризации (ИНВ-6)** в виде файла Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="a1b32-190">You can use the **Print of counting act (INV-6)** dialog box to generate a **Counting act (INV-6)** report as a Microsoft Excel file.</span></span> <span data-ttu-id="a1b32-191">Этот отчет необходимо создать для отслеживания номенклатур, перемещаемых между складами, и для создания инвентарного списка приобретенных номенклатур, находящихся в состоянии перемещения.</span><span class="sxs-lookup"><span data-stu-id="a1b32-191">You must generate this report to track items that are transferred between warehouses and to create a counting list of the items in the transfer that have been purchased.</span></span> <span data-ttu-id="a1b32-192">Инвентаризационная опись может содержать запасы в наличии.</span><span class="sxs-lookup"><span data-stu-id="a1b32-192">The counting list can contain on-hand inventory holdings.</span></span>

1. <span data-ttu-id="a1b32-193">Перейдите в раздел **Управление запасами** \> **Записи журнала** \> **Инвентаризация номенклатуры** \> **Инвентаризация**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-193">Go to **Inventory management** \> **Journal entries** \> **Item counting** \> **Counting**.</span></span>
2. <span data-ttu-id="a1b32-194">Выберите **Создать**, чтобы открыть диалоговое окно **Отображение аналитик**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-194">Select **New** to open the **Dimensions display** dialog box.</span></span>
3. <span data-ttu-id="a1b32-195">На экспресс-вкладке **Обзор** убедитесь, что в поле **Имя** указано имя журнала запасов, который был создан ранее.</span><span class="sxs-lookup"><span data-stu-id="a1b32-195">On the **Overview** FastTab, validate that the **Name** field is set to the inventory journal name that you created earlier.</span></span>
4. <span data-ttu-id="a1b32-196">В разделе **Запасы магазина** задайте поля **Место** и **Склад**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-196">In the **Store inventory** section, set the **Site** and **Warehouse** fields.</span></span>
5. <span data-ttu-id="a1b32-197">На экспресс-вкладке **Подсчет по** убедитесь, что для параметров **Профиль учета** и **Владелец** задано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-197">On the **Counting by** FastTab, validate that the **Inventory profile** and **Owner** options are set to **Yes**.</span></span>

> [!NOTE]
> <span data-ttu-id="a1b32-198">Можно также установить для параметров **Номер партии** и **Склад** значение **Да**, если эти аналитики применимы.</span><span class="sxs-lookup"><span data-stu-id="a1b32-198">You can also set the **Batch number** and **Warehouse** options to **Yes**, if those dimensions are applicable.</span></span>
 
  ![Диалоговое окно отображения аналитик](media/goods-in-transit-vendor-08.png)
 
6. <span data-ttu-id="a1b32-200">Выберите **ОК**, чтобы создать журнал инвентаризации запасов для перемещаемых номенклатур.</span><span class="sxs-lookup"><span data-stu-id="a1b32-200">Select **OK** to create an inventory counting journal for the items in the transfer.</span></span>
7. <span data-ttu-id="a1b32-201">На странице **Инвентаризация** на экспресс-вкладке **Строки журнала** создайте строку и выберите код номенклатуры, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="a1b32-201">On the **Counting** page, in the **Journal lines** FastTab, create a line, and select the item number that you created earlier.</span></span>
8. <span data-ttu-id="a1b32-202">На экспресс-вкладке **Сведения по строке** на вкладке **Складские аналитики** в полях **Профиль учета** и **Владелец** выберите записи, которые были созданы ранее.</span><span class="sxs-lookup"><span data-stu-id="a1b32-202">On the **Line details** FastTab, on the **Inventory dimensions** tab, in the **Inventory profile** and **Owner** fields, select the records that you created earlier.</span></span> <span data-ttu-id="a1b32-203">Поле **В наличии** в строке журнала обновляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="a1b32-203">The **On-hand** field on the journal line is automatically updated.</span></span>
9. <span data-ttu-id="a1b32-204">На экспресс-вкладке **Строки журнала** выберите **Функции** \> **Создать Инвентаризационную опись**, чтобы создать инвентаризационную опись.</span><span class="sxs-lookup"><span data-stu-id="a1b32-204">On the **Journal lines** FastTab, select **Functions** \> **Create counting list** to create a counting list.</span></span> <span data-ttu-id="a1b32-205">Для каждой строки поле **Фактический остаток** обновляется значением, которое указано в поле **В наличии**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-205">For each line, the **Counted** field is updated with the value that is specified in the **On-hand** field.</span></span>

  ![Страница инвентаризации](media/goods-in-transit-vendor-09.png)

10. <span data-ttu-id="a1b32-207">На панели операций выберите **Печать** \> **Акт инвентаризации (ИНВ-6)**, чтобы открыть диалоговое окно **Печать акта инвентаризации (ИНВ-6)**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-207">On the Action Pane, select **Print** \> **Counting act (INV-6)** to open the **Print of counting act (INV-6)** dialog box.</span></span>
11. <span data-ttu-id="a1b32-208">В поле **Дата составления акта** выберите дату, когда процесс инвентаризации запланирован для выполнения.</span><span class="sxs-lookup"><span data-stu-id="a1b32-208">In the **Date of act completion** field, select the date when the counting process is scheduled to be completed.</span></span>
12. <span data-ttu-id="a1b32-209">В полях **Дата начала** и **Дата окончания**, выберите начальную и конечную даты периода инвентаризации запасов.</span><span class="sxs-lookup"><span data-stu-id="a1b32-209">In the **Start date** and **End date** fields, select the start and end dates of the inventory counting period.</span></span>
13. <span data-ttu-id="a1b32-210">В поле **Номер заказа** введите номер заказа, для которого создается отчет **Акт инвентаризации ИНВ-6**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-210">In the **Order number** field, enter the order number that you're generating the **Counting act INV-6** report for.</span></span>
14. <span data-ttu-id="a1b32-211">В поле **Дата приказа** выберите дату проводки заказа, для которого создается отчет **Акт инвентаризации ИНВ-6**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-211">In the **Resolution date** field, select the transaction date of the order that you're generating the **Counting act INV-6** report for.</span></span>

> [!NOTE]
> <span data-ttu-id="a1b32-212">Значения в полях **Журнал**, **Номер аналитики** и **Тип складских запасов** основаны на проводках инвентаризации запасов.</span><span class="sxs-lookup"><span data-stu-id="a1b32-212">The values in the **Journal**, **Dimension number**, and **Kind of inventory** fields are based on the inventory counting transactions.</span></span> <span data-ttu-id="a1b32-213">Чтобы изменить значения этих полей, выберите **Фильтр.**</span><span class="sxs-lookup"><span data-stu-id="a1b32-213">To change the values of these fields, select **Filter**.</span></span> <span data-ttu-id="a1b32-214">Например, можно изменить эти значения для создания отчета для другого журнала или другой аналитики.</span><span class="sxs-lookup"><span data-stu-id="a1b32-214">For example, you can modify these values to generate the report for a different journal or a different dimension.</span></span>

  ![Печать акта инвентаризации (ИНВ-6)](media/goods-in-transit-vendor-10.png)
 
15. <span data-ttu-id="a1b32-216">Выберите **OK**, чтобы создать отчет **Акт инвентаризации (ИНВ-6)**.</span><span class="sxs-lookup"><span data-stu-id="a1b32-216">Select **OK** to generate the **Counting act (INV-6)** report.</span></span>

  ![Распечатанный отчет акта инвентаризации (ИНВ-6)](media/goods-in-transit-vendor-11.png)
 
