---
title: Спецификации актива
description: В этом разделе описываются спецификации актива в «Управлении активами».
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32bb95445a31c1de949c6aa1821bf84d42198acb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214811"
---
# <a name="asset-boms"></a><span data-ttu-id="05633-103">Спецификации актива</span><span class="sxs-lookup"><span data-stu-id="05633-103">Asset BOMs</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="05633-104">В этом разделе описываются спецификации актива в «Управлении активами».</span><span class="sxs-lookup"><span data-stu-id="05633-104">This topic describes asset bills of materials (BOMs) in Asset Management.</span></span> <span data-ttu-id="05633-105">Страница **Спецификация актива** показывает список всех номенклатур (запасные части и другие номенклатуры), которые используются в активе в течение всего срока его службы.</span><span class="sxs-lookup"><span data-stu-id="05633-105">The **Asset BOM** page shows a list of all items (spare parts and other items) that are used on an asset during its whole lifetime.</span></span> <span data-ttu-id="05633-106">При создании нового актива следует рассмотреть настройку спецификации актива как части процедуры настройки.</span><span class="sxs-lookup"><span data-stu-id="05633-106">When you create a new asset, you should consider setting up an asset BOM as a part of the setup procedure.</span></span> <span data-ttu-id="05633-107">Таким образом, можно отслеживать историю номенклатур для актива с даты создания.</span><span class="sxs-lookup"><span data-stu-id="05633-107">In this way, you can track item history for the asset from the creation date.</span></span>

<span data-ttu-id="05633-108">После завершения задания обслуживания и регистрации потребления номенклатуры в заказе на работу можно отслеживать потребление запасных частей и других номенклатур, используемых в активе.</span><span class="sxs-lookup"><span data-stu-id="05633-108">After you've completed a maintenance job, and item consumption has been registered on a work order, you can track consumption of spare parts and other items that are used on the asset.</span></span> <span data-ttu-id="05633-109">Эта функция позволяет вести полную запись потребления номенклатуры для всех ваших активов.</span><span class="sxs-lookup"><span data-stu-id="05633-109">This functionality lets you keep a complete item consumption record for all your assets.</span></span> <span data-ttu-id="05633-110">Например, запись может быть использована для мониторинга того, часто ли заменяется определенная запасная часть, или для отслеживания запасных частей или других номенклатур, которые в настоящее время используются на активе.</span><span class="sxs-lookup"><span data-stu-id="05633-110">For example, you can use the record to monitor whether a specific spare part is often replaced, or to keep track of the spare parts or other items that are currently used on an asset.</span></span>

> [!NOTE]
> <span data-ttu-id="05633-111">В заказе на работу потребление номенклатуры может включать как запасные части, так и другие дополнительные предметы, такие как смазочные материалы, болты и прокладки.</span><span class="sxs-lookup"><span data-stu-id="05633-111">On a work order, item consumption might include both spare parts and other, additional items, such as lubricants, bolts, and gaskets.</span></span>

<span data-ttu-id="05633-112">Спецификация актива может быть автоматически обновлена на основе настройки в «Управлении активами».</span><span class="sxs-lookup"><span data-stu-id="05633-112">An asset BOM can be automatically updated based on the setup in Asset Management.</span></span> <span data-ttu-id="05633-113">Если состояние жизненного цикла заказа на работу создано для обработки готовых или завершенных заказов на работу, и если параметр **Обновить спецификацию актива** для этого состояния жизненного цикла заказа на работу установлен на **Да** на странице **Состояния жизненного цикла заказа на работу**, все номенклатуры, которые используются в заказе на работу, будут автоматически обновляться на странице **Спецификация актива**, когда заказ на работу обновляется до этого состояния жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="05633-113">If a work order lifecycle state has been created to handle finished or completed work orders, and if the **Update asset BOM** option for that work order lifecycle state is set to **Yes** on the **Work order lifecycle states** page, all items that are used on the work order will be automatically updated on the **Asset BOM** page when the work order is updated to that lifecycle state.</span></span> 


<span data-ttu-id="05633-114">Вы также можете вручную обновить спецификацию актива, создавая новые строки номенклатур на странице **Спецификация актива**.</span><span class="sxs-lookup"><span data-stu-id="05633-114">You can also manually update an asset BOM by creating new item lines on the **Asset BOM** page.</span></span>

<span data-ttu-id="05633-115">На странице **Спецификация актива** можно отслеживать историю запасных частей для активов после регистрации потребления номенклатуры в заказе на работу.</span><span class="sxs-lookup"><span data-stu-id="05633-115">On the **Asset BOM** page, you can track spare parts history for assets after item consumption is registered on a work order.</span></span> <span data-ttu-id="05633-116">Чтобы использовать эту функциональность, необходимо выбрать номенклатурные группы, которые должны использоваться для регистрации запасных частей на странице **Группы номенклатуры запасных частей**.</span><span class="sxs-lookup"><span data-stu-id="05633-116">To use this functionality, you must select the item groups that should be used for spare parts registration on the **Spare parts item groups** page.</span></span>

<span data-ttu-id="05633-117">Чтобы использовать функциональность спецификации актива, необходимо сначала настроить необходимые номенклатурные группы запасных частей.</span><span class="sxs-lookup"><span data-stu-id="05633-117">To use asset BOM functionality, you must first set up the required spare parts items groups.</span></span> <span data-ttu-id="05633-118">Затем, если вы хотите, чтобы спецификация актива была автоматически обновлена после завершения заказа на работу, можно настроить состояние жизненного цикла заказа на работу для обработки этого обновления.</span><span class="sxs-lookup"><span data-stu-id="05633-118">Then, if you want the asset BOM to be automatically updated when a work order is completed, you can set up a work order lifecycle state to handle that update.</span></span> 


## <a name="set-up-spare-parts-item-groups"></a><span data-ttu-id="05633-119">Настройка номенклатурных групп запасных частей</span><span class="sxs-lookup"><span data-stu-id="05633-119">Set up spare parts item groups</span></span>

<span data-ttu-id="05633-120">Настройка истории запасных частей основана на номенклатурных группах, которые создаются в модуле **Управления запасами и складами**.</span><span class="sxs-lookup"><span data-stu-id="05633-120">The setup of spare parts history is based on item groups that are created in the **Inventory and warehouse management** module.</span></span> <span data-ttu-id="05633-121">В «Управлении активами» вы настраиваете номенклатурные группы, чтобы можно было отслеживать историю запасных частей для номенклатур в выбранных номенклатурных группах.</span><span class="sxs-lookup"><span data-stu-id="05633-121">In Asset Management, you set up item groups so that you can track spare parts history for the items in the selected item groups.</span></span>

1. <span data-ttu-id="05633-122">Выберите **Управление активами** \> **Настройка** \> **Актив** \> **Номенклатурные группы запасных частей**.</span><span class="sxs-lookup"><span data-stu-id="05633-122">Select **Asset management** \> **Setup** \> **Asset** \> **Spare parts item groups**.</span></span>
2. <span data-ttu-id="05633-123">Выберите **Создать** для настройки номенклатурной группы.</span><span class="sxs-lookup"><span data-stu-id="05633-123">Select **New** to set up an item group.</span></span>
3. <span data-ttu-id="05633-124">В поле **Номенклатурная группа** выберите группу.</span><span class="sxs-lookup"><span data-stu-id="05633-124">In the **Item group** field, select the group.</span></span> <span data-ttu-id="05633-125">Имя группы автоматически вводится в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="05633-125">The name of the group is automatically entered in the **Name** field.</span></span>

## <a name="view-and-update-asset-boms"></a><span data-ttu-id="05633-126">Просмотр и обновление спецификаций актива</span><span class="sxs-lookup"><span data-stu-id="05633-126">View and update asset BOMs</span></span>

<span data-ttu-id="05633-127">После разнесения потребления номенклатуры в заказе на работу можно просмотреть зарегистрированное потребление номенклатуры на странице **Спецификация актива**.</span><span class="sxs-lookup"><span data-stu-id="05633-127">After you post item consumption on a work order, you can view the registered item consumption on the **Asset BOM** page.</span></span>

1. <span data-ttu-id="05633-128">Выберите **Управление активами** \> **Общие** \> **Активы** \> **Активные активы**.</span><span class="sxs-lookup"><span data-stu-id="05633-128">Select **Asset management** \> **Common** \> **Assets** \> **Active assets**.</span></span> <span data-ttu-id="05633-129">Выберите актив в списке, а затем выберите **Спецификация актива**.</span><span class="sxs-lookup"><span data-stu-id="05633-129">Select the asset in the list, and then select **Asset BOM**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="05633-130">Для просмотра всех регистраций потребления номенклатуры по всем активам, выберите **Управление активами** \> **Запросы** \> **Активы** \> **Спецификации актива**.</span><span class="sxs-lookup"><span data-stu-id="05633-130">To view all item consumption registrations on all assets, select **Asset management** \> **Inquiries** \> **Assets** \> **Asset BOM**.</span></span>

2. <span data-ttu-id="05633-131">Выберите **Обновить спецификацию актива**.</span><span class="sxs-lookup"><span data-stu-id="05633-131">Select **Update asset BOM**.</span></span> <span data-ttu-id="05633-132">Вы можете добавить активы, типы активов и ресурсы в обновление, по мере необходимости, выбрав **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="05633-132">You can add assets, asset types, and resources to the update as you require by selecting **Select**.</span></span> <span data-ttu-id="05633-133">Выберите **ОК**, чтобы начать обновление.</span><span class="sxs-lookup"><span data-stu-id="05633-133">Select **OK** to start the update.</span></span> <span data-ttu-id="05633-134">Функцию обновления можно настроить в качестве пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="05633-134">You can also set up the Update function as a batch job.</span></span>
3. <span data-ttu-id="05633-135">Если вы хотите увидеть больше информации, которая связана с номенклатурами, можно добавить складские аналитики.</span><span class="sxs-lookup"><span data-stu-id="05633-135">If you want to see more information that is related to the items, you can add inventory dimensions.</span></span> <span data-ttu-id="05633-136">Выберите **Запасы** \> **Отображение аналитик**, а затем выберите флажки для аналитик, которые вы хотите видеть.</span><span class="sxs-lookup"><span data-stu-id="05633-136">Select **Inventory** \> **Dimensions display**, and then select the check boxes for the dimensions that you want to see.</span></span> <span data-ttu-id="05633-137">Чтобы сохранить эту настройку для всех активов на странице **Спецификация актива**, установите параметр **Сохранить настройки** на **Да**.</span><span class="sxs-lookup"><span data-stu-id="05633-137">To keep this setup for all assets on the **Asset BOM** page, set the **Save setup** option to **Yes**.</span></span>
4. <span data-ttu-id="05633-138">Чтобы получить обзор того, где в «Управлении активами» используется номенклатура в выбранной строке по отношению к активам, типу задания по умолчанию, запасным частям и заказам на работу, выберите **Применимость номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="05633-138">To get an overview of where in Asset Management the item on the selected line is used, in relation to assets, job type defaults, spare parts, and work orders, select **Item where used**.</span></span> 
5. <span data-ttu-id="05633-139">Если вы хотите видеть только активные строки номенклатур, выберите **Просмотр** \> **Текущий**.</span><span class="sxs-lookup"><span data-stu-id="05633-139">If you want to see only active item lines, select **View** \> **Current**.</span></span> <span data-ttu-id="05633-140">Чтобы увидеть все строки номенклатуры, включая строки, на которых дата окончания срока действия раньше текущей даты, выберите **Просмотр** \> **Все**.</span><span class="sxs-lookup"><span data-stu-id="05633-140">To see all item lines, including lines where the expiration date is earlier than the current date, select **View** \> **All**.</span></span>

> [!NOTE]
> <span data-ttu-id="05633-141">Когда вы завершили заказ на работу, если некоторые номенклатуры или запасные части, связанные с соответствующим активом, просрочены или были заменены другими номенклатурами или запасными частями, мы рекомендуем вам обновить спецификацию актива соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="05633-141">When you've completed a work order, if some items or spare parts that are related to the related asset have expired or have been replaced by other items or spare parts, we recommend that you update the asset BOM accordingly.</span></span>

## <a name="create-a-new-item-line-in-an-asset-bom"></a><span data-ttu-id="05633-142">Создание новой строки номенклатуры в спецификации актива</span><span class="sxs-lookup"><span data-stu-id="05633-142">Create a new item line in an asset BOM</span></span>

<span data-ttu-id="05633-143">Можно вручную создавать строки номенклатур для активов.</span><span class="sxs-lookup"><span data-stu-id="05633-143">You can manually create item lines for assets.</span></span>

1. <span data-ttu-id="05633-144">На странице **Спецификация актива** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="05633-144">On the **Asset BOM** page, select **New**.</span></span>
2. <span data-ttu-id="05633-145">В поле **Актив** выберите актив для добавления строки номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="05633-145">In the **Asset** field, select the asset to add an item line for.</span></span>
3. <span data-ttu-id="05633-146">В поле **Номер строки** введите последовательный номер строки.</span><span class="sxs-lookup"><span data-stu-id="05633-146">In the **Line number** field, enter a sequential line number.</span></span>
4. <span data-ttu-id="05633-147">В поле **Действует с** введите дату начала для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="05633-147">In the **Effective** field, enter a start date for the item.</span></span>
5. <span data-ttu-id="05633-148">Если срок действия номенклатуры закончился, введите дату окончания в поле **Действует по**.</span><span class="sxs-lookup"><span data-stu-id="05633-148">If the item will expire, in the **Expiration** field, enter an end date.</span></span>
6. <span data-ttu-id="05633-149">В поле **Код номенклатуры** выберите номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="05633-149">In the **Item number** field, select the item.</span></span> <span data-ttu-id="05633-150">Имя группы автоматически вводится в поле **Наименование продукта**.</span><span class="sxs-lookup"><span data-stu-id="05633-150">The name is automatically entered in the **Product name** field.</span></span>
7. <span data-ttu-id="05633-151">Введите используемое количество в поле **Количество**.</span><span class="sxs-lookup"><span data-stu-id="05633-151">In the **Quantity** field, enter the quantity that is used.</span></span> <span data-ttu-id="05633-152">Поле **Единица измерения** обновляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="05633-152">The **Unit** field is automatically updated.</span></span>
