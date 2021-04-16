---
title: Поддержка функций налогов для заказов на перемещение
description: В этой теме объясняется поддержка новой функции налогов для заказов на перемещение с помощью службы расчета налогов.
author: kailiang
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 55597e4f0f40677e793b4c182e4b0ced01057751
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832569"
---
# <a name="tax-feature-support-for-transfer-orders"></a><span data-ttu-id="201b3-103">Поддержка функций налогов для заказов на перемещение</span><span class="sxs-lookup"><span data-stu-id="201b3-103">Tax feature support for transfer orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="201b3-104">В этой теме приводятся сведения об интеграции расчета налога и разноски в заказах на перемещение.</span><span class="sxs-lookup"><span data-stu-id="201b3-104">This topic provides information about tax calculation and posting integration in transfer orders.</span></span> <span data-ttu-id="201b3-105">Эта функция позволяет настраивать расчет налогов и разноску в заказах на перемещение для перемещения запасов.</span><span class="sxs-lookup"><span data-stu-id="201b3-105">This functionality lets you set up tax calculation and posting in transfer orders for stock transfers.</span></span> <span data-ttu-id="201b3-106">В положениях по налогу на добавленную стоимость (НДС) в Европейском Союзе (ЕС) перемещение запасов считается поставками внутри сообщества и приобретением внутри сообщества.</span><span class="sxs-lookup"><span data-stu-id="201b3-106">Under European Union (EU) value-added tax (VAT) regulations, stock transfers are considered intra-community supply and intra-community acquisitions.</span></span>

<span data-ttu-id="201b3-107">Для настройки и использования этой функции необходимо выполнить три основных шага:</span><span class="sxs-lookup"><span data-stu-id="201b3-107">To configure and use this functionality, you must complete three main steps:</span></span>

1. <span data-ttu-id="201b3-108">**Настройка RCS:** в службе Regulatory Configuration Services настройте функцию налогов, налоговые коды и применимость налоговых кодов для определения налоговых кодов в заказах на перемещение.</span><span class="sxs-lookup"><span data-stu-id="201b3-108">**RCS setup:** In Regulatory Configuration Service, set up the tax feature, tax codes, and tax codes applicability for tax code determination in transfer orders.</span></span>
2. <span data-ttu-id="201b3-109">**Настройка Finance:** в Microsoft Dynamics 365 Finance включите функцию **Налог в заказах на перемещение**, настройте параметры налоговой службы для запасов и настройте основные параметры налога.</span><span class="sxs-lookup"><span data-stu-id="201b3-109">**Finance setup:** In Microsoft Dynamics 365 Finance, turn on the **Tax in transfer order** feature, set up the tax service parameters for inventory, and set up core tax parameters.</span></span>
3. <span data-ttu-id="201b3-110">**Настройка запасов:** настройка конфигурации запасов для проводок по заказам на перемещение.</span><span class="sxs-lookup"><span data-stu-id="201b3-110">**Inventory setup:** Set up the inventory configuration for transfer order transactions.</span></span>

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a><span data-ttu-id="201b3-111">Настройка RCS для проводок налогов и заказов на перемещение</span><span class="sxs-lookup"><span data-stu-id="201b3-111">Set up RCS for tax and transfer order transactions</span></span>

<span data-ttu-id="201b3-112">Выполните следующие действия, чтобы настроить налог, который участвует в заказе на перемещение.</span><span class="sxs-lookup"><span data-stu-id="201b3-112">Follow these steps to set up the tax that is involved in a transfer order.</span></span> <span data-ttu-id="201b3-113">В показанном здесь примере используется заказ на перемещение из Нидерландов в Бельгию.</span><span class="sxs-lookup"><span data-stu-id="201b3-113">In the example that is shown here, the transfer order is from the Netherlands to Belgium.</span></span>

1. <span data-ttu-id="201b3-114">На странице **Налоговые функции** на вкладке **Версии** выберите черновую версию функции, затем выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="201b3-114">On the **Tax features** page, on the **Versions** tab, select the draft feature version, and then select **Edit**.</span></span>

    ![Выбор правки](../media/image1.png)

2. <span data-ttu-id="201b3-116">На странице **Настройка налоговых функций** на вкладке **Налоговые коды** выберите **Добавить** для создания новых налоговых кодов.</span><span class="sxs-lookup"><span data-stu-id="201b3-116">On the **Tax features setup** page, on the **Tax codes** tab, select **Add** to create new tax codes.</span></span> <span data-ttu-id="201b3-117">В данном примере создаются три налоговых кода: **NL-Exempt**, **BE-RC-21** и **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="201b3-117">For this example, three tax codes are created: **NL-Exempt**, **BE-RC-21**, and **BE-RC+21**.</span></span>

    - <span data-ttu-id="201b3-118">Когда заказ на перемещение отгружается со склада в Нидерландах, применяется налоговый код, освобожденный от уплаты НДС (**NL-Exempt**).</span><span class="sxs-lookup"><span data-stu-id="201b3-118">When a transfer order is shipped from a warehouse in the Netherlands, the Netherlands VAT exempted tax code (**NL-Exempt**) is applied.</span></span>
      
        <span data-ttu-id="201b3-119">Создайте код налога **NL-Exempt**.</span><span class="sxs-lookup"><span data-stu-id="201b3-119">Create the tax code **NL-Exempt**.</span></span>
        1. <span data-ttu-id="201b3-120">Выберите **Добавить**, введите **NL-Exempt** в поле **Налоговый код**.</span><span class="sxs-lookup"><span data-stu-id="201b3-120">Select **Add**, enter **NL-Exempt** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="201b3-121">Выберите **По чистой сумме** в поле **Налоговый компонент**.</span><span class="sxs-lookup"><span data-stu-id="201b3-121">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="201b3-122">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="201b3-122">Select **Save**.</span></span>
        4. <span data-ttu-id="201b3-123">Выберите **Добавить** в таблице **Ставка**.</span><span class="sxs-lookup"><span data-stu-id="201b3-123">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="201b3-124">Переключите **Не облагается** в значение **Да** в разделе **Общие**.</span><span class="sxs-lookup"><span data-stu-id="201b3-124">Swtich **Is Exempt** to **Yes** in the **General** section.</span></span>

        ![Код налога NL-Exempt](../media/image2.png)

    - <span data-ttu-id="201b3-126">Когда заказ на перемещение поступает на склад в Бельгии, механизм возмещения расходов применяется с использованием налоговых кодов **BE-RC-21** и **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="201b3-126">When a transfer order is received at a Belgium warehouse, the reverse charge mechanism is applied by using the **BE-RC-21** and **BE-RC+21** tax codes.</span></span>
        
        <span data-ttu-id="201b3-127">Создайте налоговый код **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="201b3-127">Create the tax code **BE-RC-21**.</span></span>      
        1. <span data-ttu-id="201b3-128">Выберите **Добавить**, введите **BE-RC-21** в поле **Налоговый код**.</span><span class="sxs-lookup"><span data-stu-id="201b3-128">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="201b3-129">Выберите **По чистой сумме** в поле **Налоговый компонент**.</span><span class="sxs-lookup"><span data-stu-id="201b3-129">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="201b3-130">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="201b3-130">Select **Save**.</span></span>
        4. <span data-ttu-id="201b3-131">Выберите **Добавить** в таблице **Ставка**.</span><span class="sxs-lookup"><span data-stu-id="201b3-131">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="201b3-132">Введите **-21** в поле **Ставка налога**.</span><span class="sxs-lookup"><span data-stu-id="201b3-132">Enter **-21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="201b3-133">Переключите **Является возмещением расходов** в значение **Да** в разделе **Общие**.</span><span class="sxs-lookup"><span data-stu-id="201b3-133">Swtich **Is Reverse Charge** to **Yes** in the **General** section.</span></span>
        7. <span data-ttu-id="201b3-134">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="201b3-134">Select **Save**.</span></span>

        ![Налоговый код BE-RC-21 для возмещения расходов](../media/image3.png)
        
        <span data-ttu-id="201b3-136">Создайте налоговый код **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="201b3-136">Create the tax code **BE-RC+21**.</span></span>
        1. <span data-ttu-id="201b3-137">Выберите **Добавить**, введите **BE-RC-21** в поле **Налоговый код**.</span><span class="sxs-lookup"><span data-stu-id="201b3-137">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="201b3-138">Выберите **По чистой сумме** в поле **Налоговый компонент**.</span><span class="sxs-lookup"><span data-stu-id="201b3-138">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="201b3-139">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="201b3-139">Select **Save**.</span></span>
        4. <span data-ttu-id="201b3-140">Выберите **Добавить** в таблице **Ставка**.</span><span class="sxs-lookup"><span data-stu-id="201b3-140">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="201b3-141">Введите **21** в поле **Ставка налога**.</span><span class="sxs-lookup"><span data-stu-id="201b3-141">Enter **21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="201b3-142">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="201b3-142">Select **Save**.</span></span>

        ![Налоговый код BE-RC+21 для возмещения расходов](../media/image4.png)

3. <span data-ttu-id="201b3-144">Определите применимость налоговых кодов.</span><span class="sxs-lookup"><span data-stu-id="201b3-144">Define the applicability of the tax codes.</span></span>

    1. <span data-ttu-id="201b3-145">Выберите **Управление столбцами**, затем выберите столбцы, которые следует использовать для построения таблицы применимости.</span><span class="sxs-lookup"><span data-stu-id="201b3-145">Select **Manage columns**, and then select columns that should be used to build the applicability table.</span></span>

        > [!NOTE]
        > <span data-ttu-id="201b3-146">Обязательно добавьте столбцы **Бизнес-процесс** и **Направления налогов** в таблицу.</span><span class="sxs-lookup"><span data-stu-id="201b3-146">Be sure to add the **Business process** and **Tax directions** columns to the table.</span></span> <span data-ttu-id="201b3-147">Оба столбца являются важными для функций налогов в заказах на перемещение.</span><span class="sxs-lookup"><span data-stu-id="201b3-147">Both columns are essential to the functionality for tax in transfer orders.</span></span>

    2. <span data-ttu-id="201b3-148">Добавьте правила применимости.</span><span class="sxs-lookup"><span data-stu-id="201b3-148">Add applicability rules.</span></span> <span data-ttu-id="201b3-149">Не оставляйте поля **Налоговые коды**, **Налоговая группа** и **Налоговая группа номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="201b3-149">Don't leave the **Tax codes**, **Tax group**, and **Item tax group** fields blank.</span></span>
        
        <span data-ttu-id="201b3-150">Добавьте новое правило для отгрузки заказа на перемещение.</span><span class="sxs-lookup"><span data-stu-id="201b3-150">Add a new rule for transfer order shipment.</span></span>
        1. <span data-ttu-id="201b3-151">Выберите **Добавить** в таблице **Правила применимости**.</span><span class="sxs-lookup"><span data-stu-id="201b3-151">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="201b3-152">В поле **Бизнес-процесс** выберите **Запасы**, чтобы сделать правило применимым для заказа на перемещение.</span><span class="sxs-lookup"><span data-stu-id="201b3-152">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="201b3-153">В поле **Поставка из страны/региона** введите **NLD**.</span><span class="sxs-lookup"><span data-stu-id="201b3-153">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="201b3-154">В поле **Поставка в страну/регион** введите **BEL**.</span><span class="sxs-lookup"><span data-stu-id="201b3-154">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="201b3-155">В поле **Направление налога** выберите **Вывод**, чтобы применить правило к отгрузке заказов на перемещение.</span><span class="sxs-lookup"><span data-stu-id="201b3-155">In the **Tax direction** field, select **Output** to make the rule applicable to transfer order shipment.</span></span>
        6. <span data-ttu-id="201b3-156">В поле **Налоговые коды** выберите **NL-Exempt**.</span><span class="sxs-lookup"><span data-stu-id="201b3-156">In the **Tax codes** field, select **NL-Exempt**.</span></span>
        7. <span data-ttu-id="201b3-157">В полях **Налоговая группа** и **Налоговая группа номенклатур** введите соответствующую налоговую группу и налоговую группу номенклатур, которые определены в системе Finance.</span><span class="sxs-lookup"><span data-stu-id="201b3-157">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>
        
        <span data-ttu-id="201b3-158">Добавьте другое правило для приемки заказа на перемещение.</span><span class="sxs-lookup"><span data-stu-id="201b3-158">Add another rule for transfer order receipt.</span></span>
        1. <span data-ttu-id="201b3-159">Выберите **Добавить** в таблице **Правила применимости**.</span><span class="sxs-lookup"><span data-stu-id="201b3-159">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="201b3-160">В поле **Бизнес-процесс** выберите **Запасы**, чтобы сделать правило применимым для заказа на перемещение.</span><span class="sxs-lookup"><span data-stu-id="201b3-160">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="201b3-161">В поле **Поставка из страны/региона** введите **NLD**.</span><span class="sxs-lookup"><span data-stu-id="201b3-161">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="201b3-162">В поле **Поставка в страну/регион** введите **BEL**.</span><span class="sxs-lookup"><span data-stu-id="201b3-162">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="201b3-163">В поле **Направление налога** выберите **Ввод**, чтобы применить правило к поступлению заказов на перемещение.</span><span class="sxs-lookup"><span data-stu-id="201b3-163">In the **Tax direction** field, select **Input** to make the rule applicable to transfer order receipt.</span></span>
        6. <span data-ttu-id="201b3-164">В поле **Налоговые коды** выберите **BE-RC+21** и **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="201b3-164">In the **Tax codes** field, select **BE-RC+21** and **BE-RC-21**.</span></span>
        7. <span data-ttu-id="201b3-165">В полях **Налоговая группа** и **Налоговая группа номенклатур** введите соответствующую налоговую группу и налоговую группу номенклатур, которые определены в системе Finance.</span><span class="sxs-lookup"><span data-stu-id="201b3-165">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>

        ![Правила применимости](../media/image5.png)

4. <span data-ttu-id="201b3-167">Выполните и опубликуйте новую версию функции налога.</span><span class="sxs-lookup"><span data-stu-id="201b3-167">Complete and publish the new tax feature version.</span></span>

    <span data-ttu-id="201b3-168">[![Изменение статуса новой версии](../media/image6.png)](../media/image6.png)</span><span class="sxs-lookup"><span data-stu-id="201b3-168">[![Changing the status of the new version](../media/image6.png)](../media/image6.png)</span></span>

## <a name="set-up-finance-for-transfer-order-transactions"></a><span data-ttu-id="201b3-169">Настройка Finance для проводок заказов на перемещение</span><span class="sxs-lookup"><span data-stu-id="201b3-169">Set up Finance for transfer order transactions</span></span>

<span data-ttu-id="201b3-170">Выполните следующие действия, чтобы включить и настроить налоги для заказов на перемещение.</span><span class="sxs-lookup"><span data-stu-id="201b3-170">Follow these steps to enable and set up taxes for transfer orders.</span></span>

1. <span data-ttu-id="201b3-171">В Finance перейдите в раздел **Рабочие области** \> **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="201b3-171">In Finance, go to **Workspaces** \> **Feature management**.</span></span>
2. <span data-ttu-id="201b3-172">В списке найдите и выберите функцию **Налог в заказе на перемещение**, затем выберите **Включить**, чтобы включить ее.</span><span class="sxs-lookup"><span data-stu-id="201b3-172">In the list, find and select the **Tax in transfer order** feature, and then select **Enable now** to turn it on.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="201b3-173">Функция **Налог в заказах на перемещение** полностью зависит от налоговой службы.</span><span class="sxs-lookup"><span data-stu-id="201b3-173">The **Tax in transfer order** feature is fully dependent on the tax service.</span></span> <span data-ttu-id="201b3-174">Таким образом, она может быть включена только после установки налоговой службы.</span><span class="sxs-lookup"><span data-stu-id="201b3-174">Therefore, it can be turned on only after you've installed the tax service.</span></span>

    ![Функция налога в заказах на перемещение](../media/image7.png)

3. <span data-ttu-id="201b3-176">Включите налоговую услугу и выберите бизнес-процесс **Запасы**.</span><span class="sxs-lookup"><span data-stu-id="201b3-176">Enable the tax service, and select the **Inventory** business process.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="201b3-177">Необходимо выполнить этот шаг для каждого юридического лица в Finance, в котором вы хотите получить доступ к налоговой службе и функции налога в заказах на перемещение.</span><span class="sxs-lookup"><span data-stu-id="201b3-177">You must complete this step for each legal entity in Finance where you want the tax service and the functionality for tax in transfer orders to be available.</span></span>

    1. <span data-ttu-id="201b3-178">Перейдите в раздел **Налог** \> **Настройка** \> **Конфигурация налога** \> **Настройка налоговой службы**.</span><span class="sxs-lookup"><span data-stu-id="201b3-178">Go to **Tax** \> **Setup** \> **Tax configuration** \> **Tax service setup**.</span></span>
    2. <span data-ttu-id="201b3-179">В поле **Бизнес-процесс** выберите **Запасы**.</span><span class="sxs-lookup"><span data-stu-id="201b3-179">In the **Business process** field, select **Inventory**.</span></span>

    ![Задание поля бизнес-процесса](../media/image8.png)

4. <span data-ttu-id="201b3-181">Убедитесь, что механизм возмещения расходов настроен.</span><span class="sxs-lookup"><span data-stu-id="201b3-181">Verify that the reverse charge mechanism is set up.</span></span> <span data-ttu-id="201b3-182">Перейдите в раздел **Главная книга** \> **Настройка** \> **Параметры**, а затем на вкладке **Возмещение расходов** убедитесь, что для параметра **Включить возмещение расходов** установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="201b3-182">Go to **General ledger** \> **Setup** \> **Parameters**, and then, on the **Reverse charge** tab, verify that the **Enable reverse charge** option is set to **Yes**.</span></span>

    ![Включение параметра возмещения расходов](../media/image9.png)

5. <span data-ttu-id="201b3-184">Убедитесь, что соответствующие налоговые коды, налоговые группы, налоговые группы номенклатур и регистрационные номера НДС были настроены в Finance в соответствии с указаниями налоговой службы.</span><span class="sxs-lookup"><span data-stu-id="201b3-184">Verify that the related tax codes, tax groups, item tax groups, and VAT registration numbers have been set up in Finance according to the tax service guidance.</span></span>
6. <span data-ttu-id="201b3-185">Настройте промежуточный транзитный счет.</span><span class="sxs-lookup"><span data-stu-id="201b3-185">Set up an interim transit account.</span></span> <span data-ttu-id="201b3-186">Этот шаг требуется только в том случае, если налог, применяемый к заказу на перемещение, не применяется к механизму налогового освобождения или возмещения расходов.</span><span class="sxs-lookup"><span data-stu-id="201b3-186">This step is required only when the tax that is applied to a transfer order isn't applicable to a tax exempted or reverse charge mechanism.</span></span>

    1. <span data-ttu-id="201b3-187">Перейдите в раздел **Налог** \> **Настройка** \> **Налог** \> **Группы разноски ГК**.</span><span class="sxs-lookup"><span data-stu-id="201b3-187">Go to **Tax** \> **Setup** \> **Sales tax** \> **Ledger posting groups**.</span></span>
    2. <span data-ttu-id="201b3-188">В поле **Промежуточный транзитный** выберите счет ГК.</span><span class="sxs-lookup"><span data-stu-id="201b3-188">In the **Interim transit** field, select a ledger account.</span></span>

    ![Выбор промежуточного транзитного счета](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a><span data-ttu-id="201b3-190">Настройка базовых запасов для проводок заказов на перемещение</span><span class="sxs-lookup"><span data-stu-id="201b3-190">Set up basic inventory for transfer order transactions</span></span>

<span data-ttu-id="201b3-191">Выполните следующие действия, чтобы настроить основные запасы, чтобы включить проводки заказов на перемещение.</span><span class="sxs-lookup"><span data-stu-id="201b3-191">Follow these steps to set up basic inventory to enable transfer order transactions.</span></span>

1. <span data-ttu-id="201b3-192">Создайте сайты отгрузки и получения для складов в разных странах или регионах и добавьте основной адрес для каждого сайта.</span><span class="sxs-lookup"><span data-stu-id="201b3-192">Create ship-from and ship-to sites for your warehouses in different countries or regions, and add the primary address for each site.</span></span>

    1. <span data-ttu-id="201b3-193">Перейдите в раздел **Управление складом** \> **Настройка** \> **Склад** \> **Сайты**.</span><span class="sxs-lookup"><span data-stu-id="201b3-193">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Sites**.</span></span>
    2. <span data-ttu-id="201b3-194">Выберите **Создать**, чтобы создать сайт, который будет назначен складу позже.</span><span class="sxs-lookup"><span data-stu-id="201b3-194">Select **New** to create the site that you will assign to a warehouse later.</span></span>
    3. <span data-ttu-id="201b3-195">Повторите шаг 2 для всех других сайтов, которые необходимо создать.</span><span class="sxs-lookup"><span data-stu-id="201b3-195">Repeat step 2 for all the other sites that you must create.</span></span>

    > [!NOTE]
    > <span data-ttu-id="201b3-196">Один из созданных сайтов должен иметь имя **Транзитный**.</span><span class="sxs-lookup"><span data-stu-id="201b3-196">One of the sites that you create should be named **Transit**.</span></span> <span data-ttu-id="201b3-197">В последующих шагах этой процедуры этот сайт будет назначен транзитному складу, так что ваучеры запасов, связанные с налогами, могут быть разнесены в проводках "отгрузка" и "получение" для заказов на перемещение.</span><span class="sxs-lookup"><span data-stu-id="201b3-197">In later steps of this procedure, you will assign this site to the transit warehouse, so that tax-related inventory vouchers can be posted in "ship" and "receive" transactions for transfer orders.</span></span> <span data-ttu-id="201b3-198">Адрес транзитного сайта не имеет отношения к расчету налога.</span><span class="sxs-lookup"><span data-stu-id="201b3-198">The address of the transit site is irrelevant to tax calculation.</span></span> <span data-ttu-id="201b3-199">Поэтому поле может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="201b3-199">Therefore, you can leave it blank.</span></span>

    ![Настройка сайтов](../media/image11.png)

2. <span data-ttu-id="201b3-201">Создайте склад отгрузки, транзитный склад и склад получения.</span><span class="sxs-lookup"><span data-stu-id="201b3-201">Create ship-from, transit, and ship-to warehouses.</span></span> <span data-ttu-id="201b3-202">Любая адресная информация, которая хранится на складе, будет переопределять адрес сайта во время расчета налога.</span><span class="sxs-lookup"><span data-stu-id="201b3-202">Any address information that is maintained in a warehouse will override the site address during tax calculation.</span></span>

    1. <span data-ttu-id="201b3-203">Перейдите в раздел **Управление складом** \> **Настройка** \> **Склад** \> **Склады**.</span><span class="sxs-lookup"><span data-stu-id="201b3-203">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Warehouses**.</span></span>
    2. <span data-ttu-id="201b3-204">Выберите **Создать**, чтобы создать склад, и назначьте его соответствующему складу.</span><span class="sxs-lookup"><span data-stu-id="201b3-204">Select **New** to create a warehouse, and assign it to the corresponding site.</span></span>
    3. <span data-ttu-id="201b3-205">Повторите шаг 2 для создания склада для каждого сайта, как это необходимо.</span><span class="sxs-lookup"><span data-stu-id="201b3-205">Repeat step 2 to create a warehouse for each site as required.</span></span>

    ![Настройка складов](../media/image12.png)

    > [!NOTE]
    > <span data-ttu-id="201b3-207">Для склада отгрузки в поле **Транзитный склад** для проводок заказов на перемещение должен быть выбран транзитный склад.</span><span class="sxs-lookup"><span data-stu-id="201b3-207">For a ship-from warehouse, a transit warehouse must be selected in the **Transit warehouse** field for transfer order transactions.</span></span>
    >
    > ![Выбор транзитного склада](../media/image13.png)

3. <span data-ttu-id="201b3-209">Убедитесь, что конфигурация разноски запасов настроена для проводок заказов на перемещение.</span><span class="sxs-lookup"><span data-stu-id="201b3-209">Verify that the inventory posting configuration is set up for transfer order transactions.</span></span>

    1. <span data-ttu-id="201b3-210">Выберите **Управление запасами** \> **Настройка** \> **Разноска** \> **Разноска**.</span><span class="sxs-lookup"><span data-stu-id="201b3-210">Go to **Inventory management** \> **Setup** \> **Posting** \> **Posting**.</span></span>
    2. <span data-ttu-id="201b3-211">На вкладке **Запасы** убедитесь, что счет ГК настроен для разноски как **Расхода запасов**, так и **Поступления запасов**.</span><span class="sxs-lookup"><span data-stu-id="201b3-211">On the **Inventory** tab, verify that a ledger account is set up for both **Inventory issue** and **Inventory receipt** posting.</span></span>

        ![Настройка разноски расхода запасов и поступления запасов](../media/image14.png)

    3. <span data-ttu-id="201b3-213">Убедитесь, что счет ГК настроен для разноски **Внутрихолдинговые расчеты с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="201b3-213">Verify that a ledger account is set up for **Inter-unit payable** posting.</span></span>

        ![Настройка разноски внутрихолдинговых расчетов с поставщиками](../media/image15.png)

    4. <span data-ttu-id="201b3-215">Убедитесь, что счет ГК настроен для разноски **Внутрихолдинговые расчеты с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="201b3-215">Verify that a ledger account is set up for **Inter-unit receivable** posting.</span></span>

        ![Настройка разноски внутрихолдинговых расчетов с клиентами](../media/image16.png)
