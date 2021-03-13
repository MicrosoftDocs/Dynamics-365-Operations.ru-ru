---
title: Выставление счетов за обслуживание принадлежащих заказчику активов
description: В этом разделе описан порядок создания, обработки и выставления счетов за работу по обслуживанию, выполненную с активами, принадлежащими клиентам.
author: johanhoffmann
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 643e59f082949ed51ab61d79648a98b83a7f0b03
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131849"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a><span data-ttu-id="9e5e0-103">Выставление счетов за обслуживание принадлежащих заказчику активов</span><span class="sxs-lookup"><span data-stu-id="9e5e0-103">Bill for maintenance on customer-owned assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9e5e0-104">Функция *Выставление счетов за заказы на работу* позволяет создавать и выставлять счета за работу по обслуживанию, выполненную для активов, принадлежащих клиентам.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-104">The *Work order billing* feature lets you create, process, and bill maintenance work that is done on assets that your customers own.</span></span> <span data-ttu-id="9e5e0-105">Эта функция позволяют выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="9e5e0-105">This feature lets you perform the following tasks:</span></span>

- <span data-ttu-id="9e5e0-106">Свяжите клиентов с активами, которыми они владеют.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-106">Connect customers to the assets that they own.</span></span>
- <span data-ttu-id="9e5e0-107">Выберите клиента и просмотрите активы, которыми владеет клиент, при создании заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-107">Select a customer and view the assets that customer owns when you create a work order.</span></span>
- <span data-ttu-id="9e5e0-108">Настройте родительский проект для каждого клиента.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-108">Set up a parent project for each customer.</span></span>
- <span data-ttu-id="9e5e0-109">Зарегистрируйте часы, номенклатуры, расходы и сборы по заказу на работу, затем создайте предложение по накладной для клиента позже.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-109">Register hours, items, expenses, and fees against the work order, and then create an invoice proposal for the customer later.</span></span>

<span data-ttu-id="9e5e0-110">Кроме того, эта функция предоставляет следующие функциональные возможности:</span><span class="sxs-lookup"><span data-stu-id="9e5e0-110">In addition, the feature provides the following functionality:</span></span>

- <span data-ttu-id="9e5e0-111">Контракт по проекту из родительского проекта клиента автоматически копируется в соответствующий проект заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-111">The project contract from a customer's parent project is automatically copied to the relevant work order project.</span></span>
- <span data-ttu-id="9e5e0-112">Управление активами может теперь использовать тип проводки по проекту *сборы* как по прогнозам заказов на работу, так и по журналам заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-112">Asset management can now use the *fee* project transaction type on both work order forecasts and work order journals.</span></span>

## <a name="turn-on-the-customer-billing-feature"></a><span data-ttu-id="9e5e0-113">Включение функции выставления счетов клиенту</span><span class="sxs-lookup"><span data-stu-id="9e5e0-113">Turn on the customer billing feature</span></span>

<span data-ttu-id="9e5e0-114">Прежде чем использовать эту функцию, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-114">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="9e5e0-115">Администраторы могут использовать параметры [управления компонентами](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-115">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="9e5e0-116">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="9e5e0-116">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="9e5e0-117">**Модуль:** *Управление и учет по проектам*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-117">**Module:** *Project management and accounting*</span></span>
- <span data-ttu-id="9e5e0-118">**Название функции:** *Выставление счетов по заказу на работу*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-118">**Feature name:** *Work order billing*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="9e5e0-119">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="9e5e0-119">Example scenario</span></span>

<span data-ttu-id="9e5e0-120">Чтобы узнать, как работает эта функция, обработайте следующий пример сценария.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-120">To learn how this feature works, work through the following example scenario.</span></span>

<span data-ttu-id="9e5e0-121">Для работы с этим сценарием с помощью образцов записей и значений, указанных здесь, необходимо использовать систему, в которой установлены стандартные [демонстрационные данные](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="9e5e0-121">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="9e5e0-122">Перед началом необходимо выбрать юридическое лицо **USMF**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-122">You must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="9e5e0-123">Этот сценарий можно также использовать в качестве руководства по использованию этой функции при работе в производственной системе.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-123">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="9e5e0-124">Однако в этом случае необходимо подставить собственные значения, и у вас могут отсутствовать некоторые типы необходимых записей, предоставляемых стандартными демонстрационными данными.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-124">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a><span data-ttu-id="9e5e0-125">Шаг 1. Создайте новый контракт по проекту для клиента</span><span class="sxs-lookup"><span data-stu-id="9e5e0-125">Step 1: Create a new project contract for the customer</span></span>

1. <span data-ttu-id="9e5e0-126">Перейдите в раздел **Управление и учет по проектам \> Проекты \> Контракты по проектам**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-126">Go to **Project management and accounting \> Projects \> Project contracts**.</span></span>
1. <span data-ttu-id="9e5e0-127">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9e5e0-128">В открывшемся диалоговом окне **Создать контракт по проекту** задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9e5e0-128">In the **New project contract** dialog box, set the following values:</span></span>

    - <span data-ttu-id="9e5e0-129">**Имя:** *Pelican Wholesales*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-129">**Name:** *Pelican Wholesales*</span></span>
    - <span data-ttu-id="9e5e0-130">**Тип финансирования:** *Клиент*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-130">**Funding type:** *Customer*</span></span>
    - <span data-ttu-id="9e5e0-131">**Источник финансирования:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="9e5e0-131">**Funding source:** *US-013* (*Pelican Wholesales*)</span></span>

1. <span data-ttu-id="9e5e0-132">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-132">Select **OK**.</span></span>

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a><span data-ttu-id="9e5e0-133">Шаг 2. Создайте новый родительский проект для клиента</span><span class="sxs-lookup"><span data-stu-id="9e5e0-133">Step 2: Create a new parent project for the customer</span></span>

<span data-ttu-id="9e5e0-134">Родительский проект, созданный здесь, будет использоваться при создании заказов на работу для клиента.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-134">The parent project that you create here will be used when work orders for the customer are created.</span></span>

1. <span data-ttu-id="9e5e0-135">Перейдите в раздел **Управление и учет по проектам \> Проекты \> Все проекты**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-135">Go to **Project management and accounting \> Projects \> All projects**.</span></span>
1. <span data-ttu-id="9e5e0-136">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-136">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9e5e0-137">В диалоговом окне **Создать проект** задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9e5e0-137">In the **New project** dialog box, set the following values:</span></span>

    - <span data-ttu-id="9e5e0-138">**Тип проекта:** *Время и расходы*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-138">**Project type:** *Time and material*</span></span>
    - <span data-ttu-id="9e5e0-139">**Название проекта:** *Заказы на работу Pelican Wholesales*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-139">**Project name:** *Pelican Wholesales work orders*</span></span>
    - <span data-ttu-id="9e5e0-140">**Группа проектов:** *TM*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-140">**Project group:** *TM*</span></span>
    - <span data-ttu-id="9e5e0-141">**Код контракта по проекту:** *Pelican Wholesales* (созданный ранее контракт)</span><span class="sxs-lookup"><span data-stu-id="9e5e0-141">**Project contract ID:** *Pelican Wholesales* (the contract that you created earlier)</span></span>
    - <span data-ttu-id="9e5e0-142">**Дата начала:** выберите сегодняшнюю дату.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-142">**Start date:** Select today's date.</span></span>

1. <span data-ttu-id="9e5e0-143">Выберите **Создать проект**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-143">Select **Create project**.</span></span>
1. <span data-ttu-id="9e5e0-144">Открывается новый проект.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-144">The new project is opened.</span></span> <span data-ttu-id="9e5e0-145">Запишите значение **Код проекта**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-145">Make a note of the **Project ID** value.</span></span> <span data-ttu-id="9e5e0-146">Потребуется ввести его позже.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-146">You will have to enter it later.</span></span>

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a><span data-ttu-id="9e5e0-147">Шаг 3. Создайте новый тип заказа на работу в управлении активами</span><span class="sxs-lookup"><span data-stu-id="9e5e0-147">Step 3: Create a new work order type in Asset management</span></span>

1. <span data-ttu-id="9e5e0-148">Перейдите в раздел **Управление активами \> Настройка \> Заказ на работу \> Типы заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-148">Go to **Asset management \> Setup \> Work order \> Work order types**.</span></span>
1. <span data-ttu-id="9e5e0-149">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-149">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9e5e0-150">В список добавляется новая запись.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-150">A new record is added to the list.</span></span> <span data-ttu-id="9e5e0-151">Установите следующие значения для нее:</span><span class="sxs-lookup"><span data-stu-id="9e5e0-151">Set the following values for it:</span></span>

    - <span data-ttu-id="9e5e0-152">**Тип заказа на работу:** *Сервис*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-152">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="9e5e0-153">**Название:** *Сервисные заказы на работу*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-153">**Name:** *Service work orders*</span></span>
    - <span data-ttu-id="9e5e0-154">**Состояние жизненного цикла заказа на работу:** *Стандартное*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-154">**Work order lifecycle state:** *Standard*</span></span>

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a><span data-ttu-id="9e5e0-155">Шаг 4. Свяжите учетную запись клиента с родительским проектом</span><span class="sxs-lookup"><span data-stu-id="9e5e0-155">Step 4: Link the customer account to the parent project</span></span>

<span data-ttu-id="9e5e0-156">Теперь учетную запись клиента необходимо связать с родительским проектом в настройке проекта в модуле "Управление активами".</span><span class="sxs-lookup"><span data-stu-id="9e5e0-156">You must now link the customer account to the parent project in the project setup in Asset management.</span></span>

1. <span data-ttu-id="9e5e0-157">Перейдите в раздел **Управление активами \> Настройка \> Заказы на работу \> Настройки проектов**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-157">Go to **Asset management \> Setup \> Work orders \> Project setup**.</span></span>
1. <span data-ttu-id="9e5e0-158">На вкладке **Родительский проект** выберите **Добавить**, чтобы добавить строку.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-158">On the **Parent project** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="9e5e0-159">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9e5e0-159">On the new line, set the following values:</span></span>

    - <span data-ttu-id="9e5e0-160">**Учетная запись клиента:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="9e5e0-160">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="9e5e0-161">**Код проекта:** введите код проекта, который вы записали ранее.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-161">**Project ID:** Enter the project ID that you made a note of earlier.</span></span>

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a><span data-ttu-id="9e5e0-162">Шаг 5. Свяжите группу проектов и тип с проектом заказа на работу</span><span class="sxs-lookup"><span data-stu-id="9e5e0-162">Step 5: Link the project group and type to the work order project</span></span>

<span data-ttu-id="9e5e0-163">Вы по-прежнему должны находиться на странице **Настройка проекта** (**Управление активами \> Настройка \> Заказы на работу \> Настройка проекта**).</span><span class="sxs-lookup"><span data-stu-id="9e5e0-163">You should still be on the **Project setup** page (**Asset management \> Setup \> Work orders \> Project setup**).</span></span>

1. <span data-ttu-id="9e5e0-164">На вкладке **Группа проектов** выберите **Добавить**, чтобы добавить строку.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-164">On the **Project group** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="9e5e0-165">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9e5e0-165">On the new line, set the following values:</span></span>

    - <span data-ttu-id="9e5e0-166">**Тип заказа на работу:** *Сервис* (тип заказа на работу, который был создан ранее)</span><span class="sxs-lookup"><span data-stu-id="9e5e0-166">**Work order type:** *Service* (the work order type that you created earlier)</span></span>
    - <span data-ttu-id="9e5e0-167">**Группа проектов:** *TM*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-167">**Project group:** *TM*</span></span>

> [!NOTE]
> <span data-ttu-id="9e5e0-168">Контракт по проекту в проекте заказа на работу всегда наследуется из родительского проекта.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-168">The project contract on the work order project is always inherited from the parent project.</span></span>

### <a name="step-6-link-an-asset-to-the-customer-id"></a><span data-ttu-id="9e5e0-169">Шаг 6. Свяжите актив с кодом клиента</span><span class="sxs-lookup"><span data-stu-id="9e5e0-169">Step 6: Link an asset to the customer ID</span></span>

1. <span data-ttu-id="9e5e0-170">Перейдите к пункту **Управление активами \> Активы \> Активные активы**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-170">Go to **Asset management \> Assets \> Active assets**.</span></span>
1. <span data-ttu-id="9e5e0-171">В поле **Фильтр** введите *VE-102* и выберите фильтрацию по параметру **Актив**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-171">In the **Filter** field, enter *VE-102*, and select to filter by **Asset**.</span></span>
1. <span data-ttu-id="9e5e0-172">Выберите актив, чтобы открыть его настройки.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-172">Select the asset to open its settings.</span></span>
1. <span data-ttu-id="9e5e0-173">На экспресс-вкладке **Клиент** задайте для поля **Счет клиента** значение *US-013* (*Pelican Wholesales*).</span><span class="sxs-lookup"><span data-stu-id="9e5e0-173">On the **Customer** FastTab, set the **Customer account** field to *US-013* (*Pelican Wholesales*).</span></span>

    <span data-ttu-id="9e5e0-174">Поле **Имя** автоматически обновляется на *Pelican Wholesales*.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-174">The **Name** field is automatically updated to *Pelican Wholesales*.</span></span>

### <a name="step-7-create-a-new-work-order-on-the-asset"></a><span data-ttu-id="9e5e0-175">Шаг 7. Создайте новый заказ на работу для актива</span><span class="sxs-lookup"><span data-stu-id="9e5e0-175">Step 7: Create a new work order on the asset</span></span>

1. <span data-ttu-id="9e5e0-176">Перейдите в раздел **Управление активами \> Заказы на работу \> Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-176">Go to **Asset management \> Work orders \> Active work orders**.</span></span>
1. <span data-ttu-id="9e5e0-177">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-177">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9e5e0-178">В диалоговом окне **Создание заказа на работу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9e5e0-178">In the **Create work order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="9e5e0-179">**Тип заказа на работу:** *Сервис*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-179">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="9e5e0-180">**Описание:** *Ремонт грузовика*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-180">**Description:** *Repair Truck*</span></span>
    - <span data-ttu-id="9e5e0-181">**Учетная запись клиента:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="9e5e0-181">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="9e5e0-182">**Актив:** *VE-102*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-182">**Asset:** *VE-102*</span></span>

        > [!NOTE]
        > <span data-ttu-id="9e5e0-183">В подстановке отображаются только те активы, которые связаны с выбранной учетной записью клиента.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-183">The lookup shows only assets that are linked to the selected customer account.</span></span>

    - <span data-ttu-id="9e5e0-184">**Типа задания по обслуживанию:** *Ремонт*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-184">**Maintenance job type:** *Repair*</span></span>
    - <span data-ttu-id="9e5e0-185">**Специальность:** *Механик*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-185">**Trade:** *Mechanic*</span></span>
    - <span data-ttu-id="9e5e0-186">**Уровень сервиса:** *4*</span><span class="sxs-lookup"><span data-stu-id="9e5e0-186">**Service level:** *4*</span></span>

1. <span data-ttu-id="9e5e0-187">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-187">Select **OK**.</span></span>

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a><span data-ttu-id="9e5e0-188">Шаг 8. Проверьте заказ на работу и начните работать с ним</span><span class="sxs-lookup"><span data-stu-id="9e5e0-188">Step 8: Review the work order and start to work on it</span></span>

<span data-ttu-id="9e5e0-189">В этом разделе вы будете работать с заказом на работу, который был создан в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-189">In this section, you will work on the work order that you created in the previous section.</span></span>

1. <span data-ttu-id="9e5e0-190">Выполните следующие действия, чтобы убедиться, что родительский проект является проектом *Заказ на работу для Pelican Wholesales*:</span><span class="sxs-lookup"><span data-stu-id="9e5e0-190">Follow these steps to verify that the parent project is the *Pelican wholesales Work order* project:</span></span>

    1. <span data-ttu-id="9e5e0-191">В разделе **Задания на обслуживание из заказа на работу** выберите строку.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-191">In the **Work order maintenance jobs** section, select a line.</span></span>
    1. <span data-ttu-id="9e5e0-192">На экспресс-вкладке **Сведения по строке** проверьте значение **Код проекта**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-192">On the **Line details** FastTab, inspect the **Project ID** value.</span></span> <span data-ttu-id="9e5e0-193">Он должен быть числом с дефисом в форме *\<Parent-Project-ID\>-\<Project-ID\>*.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-193">It should be a hyphenated number in the form *\<Parent-Project-ID\>-\<Project-ID\>*.</span></span> <span data-ttu-id="9e5e0-194">Это значение является ссылкой.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-194">This value is a link.</span></span>
    1. <span data-ttu-id="9e5e0-195">Выберите ссылку на код проекта, чтобы открыть страницу, на которой можно просмотреть родительский проект и имена проектов.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-195">Select the project ID link to open a page where you can view the parent project and project names.</span></span>

1. <span data-ttu-id="9e5e0-196">В области действий на вкладке **Заказ на работу** в группе **Состояние жизненного цикла** выберите **Обновить состояние заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-196">On the Action Pane, on the **Work order** tab, in the **Lifecycle state** group, select **Update work order state**.</span></span>
1. <span data-ttu-id="9e5e0-197">В диалоговом окне **Обновление состояния заказа на работу** в столбце **Выбор** установите флажок рядом со строкой, для которой в поле **Состояние жизненного цикла** указано значение *Выполняется*.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-197">In the **Update work order state** dialog box, in the **Select** column, select the check box for the row where the **Lifecycle state** field is set to *In progress*.</span></span>
1. <span data-ttu-id="9e5e0-198">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-198">Select **OK**.</span></span>
1. <span data-ttu-id="9e5e0-199">В диалоговом окне **Состояние жизненного цикла: выполняется** выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-199">In the **Lifecycle state: InProgress** dialog box, select **OK**.</span></span>

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a><span data-ttu-id="9e5e0-200">Шаг 9. Разноска часов, затраченных на заказ на работу, и создание нового предложения по накладной</span><span class="sxs-lookup"><span data-stu-id="9e5e0-200">Step 9: Post the hours that were spent on the work order and create a new invoice proposal</span></span>

<span data-ttu-id="9e5e0-201">В этом разделе вы продолжите работать с заказом на работу, с которым работали в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-201">In this section, you will continue to work on the work order that you worked on in the previous section.</span></span>

1. <span data-ttu-id="9e5e0-202">В области действий на вкладке **Заказ на работу** в группе **Проект** выберите **Журналы**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-202">On the Action Pane, on the **Work order** tab, in the **Project** group, select **Journals**.</span></span>

    <span data-ttu-id="9e5e0-203">Отображается страница **Журнал заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-203">The **Work order journals** page appears.</span></span> <span data-ttu-id="9e5e0-204">Здесь можно зарегистрировать время, потраченное на заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-204">Here, you can register the time that you spent on the work order.</span></span>

1. <span data-ttu-id="9e5e0-205">На экспресс-вкладке **Часы** выберите **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-205">On the **Hours** FastTab, select **Add line**.</span></span>
1. <span data-ttu-id="9e5e0-206">В новой строке задайте в поле **Часы** значение *4*.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-206">On the new, line, set the **Hours** field to *4*.</span></span>
1. <span data-ttu-id="9e5e0-207">На панели операций выберите **Разнести журналы**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-207">On the Action Pane, select **Post journals**.</span></span>
1. <span data-ttu-id="9e5e0-208">Закройте страницу **Журналы заказов на работу**, чтобы вернуться к рабочему заказу.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-208">Close the **Work order journals** page to return to the work order.</span></span>
1. <span data-ttu-id="9e5e0-209">На панели операций откройте вкладку **Выставление счетов** и выберите **Создать предложение по накладной**.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-209">On the Action Pane, on the **Invoicing** tab, select **New invoice proposal**.</span></span>
1. <span data-ttu-id="9e5e0-210">В диалоговом окне **Создать предложение по накладной** в разделе **Проводки по проекту** установите флажок **Выбрать** для каждой строки, для которой необходимо выставить накладную.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-210">In the **Create invoice proposal** dialog box, in the **Project transactions** section, select the **Select** check box for every line  that you want to invoice.</span></span>
1. <span data-ttu-id="9e5e0-211">Выберите **ОК**, чтобы закрыть диалоговое окно и просмотреть новое предложение по накладным.</span><span class="sxs-lookup"><span data-stu-id="9e5e0-211">Select **OK** to close the dialog box and view the new invoice proposal.</span></span>
