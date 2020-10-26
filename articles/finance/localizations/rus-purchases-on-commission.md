---
title: Покупки по комиссии
description: В этой теме приводятся сведения о покупках, выполненных по комиссии.
author: v-nadyuz
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: roschlom
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 1941efb5f6da9a94e8829e1d8071d2a9843170c2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983995"
---
# <a name="purchases-on-commission"></a><span data-ttu-id="237de-103">Покупки по комиссии</span><span class="sxs-lookup"><span data-stu-id="237de-103">Purchases on commission</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="237de-104">Доверитель нанимает агента, чтобы найти, от собственного лица агента, но за счет доверителя, подходящего поставщика и согласовать поставку товаров (работ или услуг) для доверителя.</span><span class="sxs-lookup"><span data-stu-id="237de-104">The principal engages the agent to find, in the agent's own name but at the principal's expense, a suitable supplier, and to agree on the supply of goods (works or services) to the principal.</span></span>

<span data-ttu-id="237de-105">Счета-фактуры, получаемые агентом от поставщика, имеют следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="237de-105">Factures that an agent receives from a supplier have these characteristics:</span></span>

- <span data-ttu-id="237de-106">Агент должен зарегистрировать их на листе **Получено** журнала учета счетов-фактур.</span><span class="sxs-lookup"><span data-stu-id="237de-106">The agent must register them on the **Received** worksheet of the facture accounting journal.</span></span>
- <span data-ttu-id="237de-107">Их не требуется вводиться в книгу покупок агента, потому что агент не имеет прав на удержание налога на добавленную стоимость (НДС).</span><span class="sxs-lookup"><span data-stu-id="237de-107">They don't have to be entered in the agent's purchase book, because the agent has no right to value-added tax (VAT) deduction.</span></span>
- <span data-ttu-id="237de-108">Они должны быть скопированы, а копии должны быть сертифицированы и переданы доверителю.</span><span class="sxs-lookup"><span data-stu-id="237de-108">They must be copied, and the copies must be certified and given to the principal.</span></span>
- <span data-ttu-id="237de-109">Агент должен повторно выпустить их для доверителя.</span><span class="sxs-lookup"><span data-stu-id="237de-109">The agent must reissue them to the principal.</span></span>

<span data-ttu-id="237de-110">Счета-фактуры, которые агент повторно впускает, имеют следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="237de-110">Factures that an agent reissues have these characteristics:</span></span>

- <span data-ttu-id="237de-111">Они должны быть зарегистрированы на листе **Выпущены** журнала учета счетов-фактур.</span><span class="sxs-lookup"><span data-stu-id="237de-111">They must be registered on the **Issued** worksheet of the facture accounting journal.</span></span>
- <span data-ttu-id="237de-112">Их не требуется вводить в книгу продаж, потому что агент не имеет обязательств по начислению НДС.</span><span class="sxs-lookup"><span data-stu-id="237de-112">They don’t have to be entered in the sales book because the agent has no obligation to charge VAT.</span></span>

<span data-ttu-id="237de-113">На следующем рисунке показан бизнес-процесс регистрации сделок через посредника.</span><span class="sxs-lookup"><span data-stu-id="237de-113">The following illustration shows the business process for registering intermediary deals.</span></span> <span data-ttu-id="237de-114">В системе отражены прямоугольные элементы.</span><span class="sxs-lookup"><span data-stu-id="237de-114">Rectangular elements are reflected in the system.</span></span> <span data-ttu-id="237de-115">Овальные элементы присутствуют в бизнес-процессе, но не отражаются в системе.</span><span class="sxs-lookup"><span data-stu-id="237de-115">Oval elements are present in the business process but aren't reflected in the system.</span></span>

![Последовательность бизнес-процесса покупки по комиссии](media/Purchases_on_commission_english.jpg)

## <a name="create-a-sales-agreement-for-a-purchase-by-an-agent"></a><span data-ttu-id="237de-117">Создание договора продажи для покупки агентом</span><span class="sxs-lookup"><span data-stu-id="237de-117">Create a sales agreement for a purchase by an agent</span></span>

1. <span data-ttu-id="237de-118">Перейдите в раздел **Расчеты с клиентами** \> **Заказы** \> **Договоры продажи**.</span><span class="sxs-lookup"><span data-stu-id="237de-118">Go to **Accounts receivable** \> **Orders** \> **Sales agreements**.</span></span>
2. <span data-ttu-id="237de-119">Выберите **Создать**, чтобы открыть диалоговое окно **Создание договора продажи**.</span><span class="sxs-lookup"><span data-stu-id="237de-119">Select **New** to open the **Create sales agreement** dialog box.</span></span>
3. <span data-ttu-id="237de-120">На экспресс-вкладке **Клиент** укажите счет клиента, затем в поле **Классификация договоров продажи** выберите **Общий договор продажи**.</span><span class="sxs-lookup"><span data-stu-id="237de-120">On the **Customer** FastTab, specify the customer account, and then, in the **Sales agreement classification** field, select **Blanket sales agreement**.</span></span>
4. <span data-ttu-id="237de-121">На экспресс-вкладке **Общие сведения** в разделе **Документ** в поле **Код договора продажи** укажите код договора продажи.</span><span class="sxs-lookup"><span data-stu-id="237de-121">On the **General** FastTab, in the **Document** section, in the **Sales agreement ID** field, specify the identifier of the sales agreement.</span></span>
5. <span data-ttu-id="237de-122">Укажите другие сведения, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="237de-122">Specify other details, and then select **OK**.</span></span>

    ![Диалоговое окно создания классификаций договоров продажи](media/3_Create_sales_agreement.jpg)

6. <span data-ttu-id="237de-124">На странице **Договоры продажи** перейдите в представление **Заголовок**.</span><span class="sxs-lookup"><span data-stu-id="237de-124">On the **Sales agreements** page, switch to the **Header** view.</span></span>
7. <span data-ttu-id="237de-125">На Экспресс-вкладке **Общие сведения** в разделе **Документ** в поле **Комиссионное соглашение** выберите **Покупка комиссионером**.</span><span class="sxs-lookup"><span data-stu-id="237de-125">On the **General** FastTab, in the **Document** section, in the **Commission agreement** field, select **Purchase by commissioner**.</span></span>
8. <span data-ttu-id="237de-126">На экспресс-вкладке **Финансы** в разделе **Профиль учета** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="237de-126">On the **Financial** FastTab, in the **Inventory profile** section, specify the following details:</span></span>

    - <span data-ttu-id="237de-127">В поле **Вид деятельности** выберите **Комиссионер**.</span><span class="sxs-lookup"><span data-stu-id="237de-127">In the **Kind of activity** field, select **Commission agent**.</span></span>
    - <span data-ttu-id="237de-128">В поле **Профиль учета** выберите профиль учета, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="237de-128">In the **Inventory profile** field, select the inventory profile that you created earlier.</span></span>

    ![Страница договора продажи, экспресс-вкладка финансов](media/4_Sales_agreements.jpg)

9. <span data-ttu-id="237de-130">На панели операций на вкладке **Договор продажи** в группе **Создать** выберите **Подтверждение** для обновления статуса договора до **Действует**.</span><span class="sxs-lookup"><span data-stu-id="237de-130">On the Action Pane, on the **Sales agreement** tab, in the **Generate** group, select **Confirmation** to update status of the agreement to **Effective**.</span></span>

## <a name="create-inventory-owners-suppliers-for-a-commissioner"></a><span data-ttu-id="237de-131">Создание владельцев запасов (поставщиков) для комиссионера</span><span class="sxs-lookup"><span data-stu-id="237de-131">Create inventory owners (suppliers) for a commissioner</span></span>

1. <span data-ttu-id="237de-132">Перейдите в раздел **Запасы** \> **Настройка** \> **Аналитики** \> **Владельцы запасов**.</span><span class="sxs-lookup"><span data-stu-id="237de-132">Go to \*\*Inventory \*\* \> **Setup** \> **Dimensions** \> **Inventory owners**.</span></span>
2. <span data-ttu-id="237de-133">Выберите **Создать**, чтобы создать владельца запасов.</span><span class="sxs-lookup"><span data-stu-id="237de-133">Select **New** to create an inventory owner.</span></span>
3. <span data-ttu-id="237de-134">В поле **Владелец** введите код для владельца.</span><span class="sxs-lookup"><span data-stu-id="237de-134">In the **Owner** field, enter the code for the owner.</span></span>
4. <span data-ttu-id="237de-135">В поле **Тип счета** выберите **Поставщик**.</span><span class="sxs-lookup"><span data-stu-id="237de-135">In the **Account type** field, select **Vendor**.</span></span>
5. <span data-ttu-id="237de-136">В поле **Организация** выберите код для поставщика.</span><span class="sxs-lookup"><span data-stu-id="237de-136">In the **Account** field, select the code for the supplier.</span></span> <span data-ttu-id="237de-137">Поле **Имя** заполняется автоматически.</span><span class="sxs-lookup"><span data-stu-id="237de-137">The **Name** field is automatically filled in.</span></span>
6. <span data-ttu-id="237de-138">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="237de-138">Select **Save**.</span></span>

![Страница владельцев запасов для поставщиков](media/5_Inventory_owners.jpg)

## <a name="create-inventory-owners-principals-for-a-commissioner"></a><span data-ttu-id="237de-140">Создание владельцев запасов (доверителей) для комиссионера</span><span class="sxs-lookup"><span data-stu-id="237de-140">Create inventory owners (principals) for a commissioner</span></span>

1. <span data-ttu-id="237de-141">Перейдите в раздел **Управление запасами** \> **Настройка** \> **Аналитики** \> **Владельцы запасов**.</span><span class="sxs-lookup"><span data-stu-id="237de-141">Go to **Inventory management** \> **Setup** \> **Dimensions** \> **Inventory owners**.</span></span>
2. <span data-ttu-id="237de-142">Выберите **Создать**, чтобы создать владельца запасов.</span><span class="sxs-lookup"><span data-stu-id="237de-142">Select **New** to create an inventory owner.</span></span>
3. <span data-ttu-id="237de-143">В поле **Владелец** введите код для владельца.</span><span class="sxs-lookup"><span data-stu-id="237de-143">In the **Owner** field, enter the code for the owner.</span></span>
4. <span data-ttu-id="237de-144">В поле **Тип счета** выберите **Клиент**.</span><span class="sxs-lookup"><span data-stu-id="237de-144">In the **Account type** field, select **Customer**.</span></span>
5. <span data-ttu-id="237de-145">В поле **Организация** выберите код для доверителя.</span><span class="sxs-lookup"><span data-stu-id="237de-145">In the **Account** field, select the code for the principal.</span></span> <span data-ttu-id="237de-146">Поле **Имя** заполняется автоматически.</span><span class="sxs-lookup"><span data-stu-id="237de-146">The **Name** field is automatically filled in.</span></span>
6. <span data-ttu-id="237de-147">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="237de-147">Select **Save**.</span></span>

![Страница владельцев запасов для клиентов](media/6_Inventory_owners.jpg)

## <a name="create-a-purchase-order-and-update-the-facture-on-goods-that-are-purchased-for-a-principal"></a><span data-ttu-id="237de-149">Создание заказа на покупку и обновление счета-фактуры на товары, приобретаемые для доверителя</span><span class="sxs-lookup"><span data-stu-id="237de-149">Create a purchase order and update the facture on goods that are purchased for a principal</span></span>

1. <span data-ttu-id="237de-150">Создание заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="237de-150">Create a purchase order.</span></span>
2. <span data-ttu-id="237de-151">В строке заказа на покупку выберите код номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="237de-151">On the purchase order line, select an item number.</span></span>

> [!NOTE]
> <span data-ttu-id="237de-152">В поле **Аналитика отслеживания** для данной номенклатуры должен быть указан профиль учета, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="237de-152">The **Tracking dimension** field for the item should be set to the inventory profile that you created earlier.</span></span>

3. <span data-ttu-id="237de-153">На экспресс-вкладке **Сведения по строке** на вкладке **Продукт** в разделе **Аналитики отслеживания** в поле **Профиль учета** выберите профиль учета, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="237de-153">On the **Line details** FastTab, on the **Product** tab, in the **Tracking dimensions** section, in the **Inventory profile** field, select the inventory profile that you created earlier.</span></span>
4. <span data-ttu-id="237de-154">Если разноска счета не планируется, в поле **Владелец** выберите владельца (поставщика), который был создан ранее.</span><span class="sxs-lookup"><span data-stu-id="237de-154">If you don't plan to post the invoice, in the **Owner** field, select the owner (supplier) that you created earlier.</span></span> <span data-ttu-id="237de-155">Таким образом, при повторном выдаче счета-фактуры в отчете для доверителя указывается поставщик.</span><span class="sxs-lookup"><span data-stu-id="237de-155">In this way, you identify the supplier on the report for the principal when the facture is reissued.</span></span>

    ![Страница "Заказ на покупку"](media/7_All_purchase_orders.jpg)

5. <span data-ttu-id="237de-157">Укажите другие параметры заказа на покупку и создайте счет-фактуру.</span><span class="sxs-lookup"><span data-stu-id="237de-157">Specify other purchase order parameters, and create a facture.</span></span>

## <a name="create-a-sales-order-and-generate-a-sales-invoice-for-goods-that-are-purchased-for-a-principal"></a><span data-ttu-id="237de-158">Создание заказа на продажу и создание накладной по продаже для товаров, приобретенных для доверителя</span><span class="sxs-lookup"><span data-stu-id="237de-158">Create a sales order and generate a sales invoice for goods that are purchased for a principal</span></span>

1. <span data-ttu-id="237de-159">Создание нового заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="237de-159">Create a new sales order.</span></span>
2. <span data-ttu-id="237de-160">В поле **Код договора продажи** выберите договор для покупки агентом, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="237de-160">In the **Sales agreement ID** field, select the agreement for a purchase by the agent that you created earlier.</span></span>
3. <span data-ttu-id="237de-161">В строке заказа на продажу выберите код номенклатуры, которая была куплена ранее.</span><span class="sxs-lookup"><span data-stu-id="237de-161">On the sales order line, select the item number that was purchased earlier.</span></span>

   > [!NOTE]
   > <span data-ttu-id="237de-162">В поле **Аналитика отслеживания** для данной номенклатуры должен быть указан профиль учета, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="237de-162">The **Tracking dimension** field for the item should be set to the inventory profile that you created earlier.</span></span>

4. <span data-ttu-id="237de-163">На экспресс-вкладке **Сведения по строке** на вкладке **Настройка** в разделе **Запасы** в поле **Резервирование** выберите **Автоматически**.</span><span class="sxs-lookup"><span data-stu-id="237de-163">On the **Line details** FastTab, on the **Setup** tab, in the **Inventory** section, in the **Reservation** field, select **Automatic**.</span></span>

    ![Страница заказа на продажу](media/8_Sales_order.jpg)

5. <span data-ttu-id="237de-165">На экспресс-вкладке **Сведения по строке** на вкладке **Продукт** в разделе **Аналитики отслеживания** убедитесь, что в поле **Профиль учета** автоматически задан профиль учета, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="237de-165">On the **Line details** FastTab, on the **Product** tab, in the **Tracking dimensions** section, make sure that the **Inventory profile** field is automatically set to the inventory profile that you created earlier.</span></span>
6. <span data-ttu-id="237de-166">В поле **Владелец** выберите владельца (доверителя), созданного ранее.</span><span class="sxs-lookup"><span data-stu-id="237de-166">In the **Owner** field, select the owner (principal) that you created earlier.</span></span>
7. <span data-ttu-id="237de-167">На экспресс-вкладке **Строки заказа на продажу** выберите **Запасы \> Маркировка**.</span><span class="sxs-lookup"><span data-stu-id="237de-167">On the **Sales order lines** FastTab, select **Inventory \> Marking**.</span></span>
8. <span data-ttu-id="237de-168">Выберите проводку покупки, выберите **Пометить**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="237de-168">Select a purchase transaction, select **Set mark now**, and then select **OK**.</span></span>
9. <span data-ttu-id="237de-169">Разноска накладной.</span><span class="sxs-lookup"><span data-stu-id="237de-169">Post the invoice.</span></span>

## <a name="create-and-print-a-report-for-a-principal-and-reissue-the-sellers-factures-to-the-principal"></a><span data-ttu-id="237de-170">Создание и печать отчета для доверителя и повторный выпуск счетов-фактур продавца для доверителя</span><span class="sxs-lookup"><span data-stu-id="237de-170">Create and print a report for a principal, and reissue the seller's factures to the principal</span></span>

1. <span data-ttu-id="237de-171">Перейдите к пункту **Главная книга** \> **Периодические задачи** \> **Комиссионная торговля** \> **Отчет для доверителя**.</span><span class="sxs-lookup"><span data-stu-id="237de-171">Go to **General ledger** \> **Periodic tasks** \> **Commission trade** \> **Report for principal**.</span></span>
2. <span data-ttu-id="237de-172">Выберите **Создать**, чтобы открыть диалоговое окно **Создание отчета для доверителя.**</span><span class="sxs-lookup"><span data-stu-id="237de-172">Select **New** to open the **Create report for principal** dialog box **.**</span></span>
3. <span data-ttu-id="237de-173">В полях **Дата начала** и **Дата окончания** укажите период для отчета.</span><span class="sxs-lookup"><span data-stu-id="237de-173">In the **From date** and **To date** fields, specify the period for the report.</span></span>

   > [!NOTE]
   > <span data-ttu-id="237de-174">Поле **Дата начала** можно оставить пустым.</span><span class="sxs-lookup"><span data-stu-id="237de-174">You can leave the **From date** field blank.</span></span>

4. <span data-ttu-id="237de-175">В поле **Тип доверителя** выберите **Клиент**.</span><span class="sxs-lookup"><span data-stu-id="237de-175">In the **Principal type** field, select **Customer**.</span></span>
5. <span data-ttu-id="237de-176">В поле **Код партнера** выберите счет клиента.</span><span class="sxs-lookup"><span data-stu-id="237de-176">In the **Partner code** field, select the customer account.</span></span>
6. <span data-ttu-id="237de-177">В поле **Код договора** выберите договор продажи.</span><span class="sxs-lookup"><span data-stu-id="237de-177">In the **Agreement ID** field, select the sales agreement.</span></span>
7. <span data-ttu-id="237de-178">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="237de-178">Select **OK**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="237de-179">Для создания заголовков для всех отчетов по доверителю, которые необходимы в течение указанного периода, выберите **Функции \> Создать заголовки отчетов по отгрузкам**.</span><span class="sxs-lookup"><span data-stu-id="237de-179">To create the headers for all the reports for the principal that are required in the specified period, select **Functions \> Create report headers on shipments**.</span></span>

8. <span data-ttu-id="237de-180">Выберите **Функции \> Обновить строки отгрузки**, чтобы открыть диалоговое окно **Создание отчета для доверителя по отгрузкам**, затем выберите **OK**, чтобы создать строки для каждого отчета.</span><span class="sxs-lookup"><span data-stu-id="237de-180">Select **Functions \> Update lines on shipment** to open the **Generate report for principal on shipments** dialog box, and then select **OK** to create the lines for every report.</span></span>
9. <span data-ttu-id="237de-181">Основываясь на счетах-фактурах, полученных от продавца (поставщика), вы в качестве агента должны повторно выпустить счета-фактуры по отгруженной части товаров доверителю (клиенту) от имени продавца.</span><span class="sxs-lookup"><span data-stu-id="237de-181">Based on the factures that are received from the seller (vendor), you, as an agent, should reissue the factures on the shipped part of the goods to the principal (customer) on behalf of the seller.</span></span> <span data-ttu-id="237de-182">Эти новые счета-фактуры нумеруются в соответствии с номерной серией счетов-фактур.</span><span class="sxs-lookup"><span data-stu-id="237de-182">These new factures are numbered according to the facture's number sequence.</span></span>
10. <span data-ttu-id="237de-183">На странице **Отчет для доверителя** используйте флажок **Утверждено**, чтобы утвердить соответствующие строки счетов-фактур продавца.</span><span class="sxs-lookup"><span data-stu-id="237de-183">On the **Report for principal** page, use the **Approved** check box to approve the appropriate lines of the seller's factures.</span></span> <span data-ttu-id="237de-184">Чтобы утвердить все строки отчета, выберите **Утверждение \> Утвердить все**.</span><span class="sxs-lookup"><span data-stu-id="237de-184">To approve all the lines on the report, select **Approval \> Approve All**.</span></span>

    ![Страница отчета для доверителя](media/9_Report_for_principal.jpg)

11. <span data-ttu-id="237de-186">Выберите **Счет-фактура \> Обновить счет-фактуру**, чтобы создать повторно выпущенную счет-фактуру для доверителя.</span><span class="sxs-lookup"><span data-stu-id="237de-186">Select **Facture \> Update facture** to generate reissued factures for the principal.</span></span>
12. <span data-ttu-id="237de-187">На странице **Обновить счет-фактуру** в разделе **Комиссионная торговля** убедитесь, что поля **Продавец** и **Счет-фактура** настроены автоматически.</span><span class="sxs-lookup"><span data-stu-id="237de-187">On the **Update facture** page, in the **Commission trade** section, make sure that the **Seller** and **Facture** fields are automatically set.</span></span> <span data-ttu-id="237de-188">Если они пусты, выберите поставщика в поле **Продавец** и номер счета-фактуры покупки, который был создан в поле **Счет-фактура**.</span><span class="sxs-lookup"><span data-stu-id="237de-188">If they are blank, select the supplier in the **Seller** field and the number of the purchase facture that was created in the **Facture** field.</span></span>
13. <span data-ttu-id="237de-189">Укажите другие необходимые сведения и создайте счет-фактуру.</span><span class="sxs-lookup"><span data-stu-id="237de-189">Specify other required details, and create the facture.</span></span>

    ![Страница обновления счета-фактуры](media/10_Update_facture.jpg)

14. <span data-ttu-id="237de-191">На странице **Отчет для доверителя** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="237de-191">On the **Report for principal** page, follow these steps:</span></span>

    - <span data-ttu-id="237de-192">Выберите **Доверитель** \> **Журнал накладных** для просмотра накладной доверителя.</span><span class="sxs-lookup"><span data-stu-id="237de-192">Select **Principal** \> **Invoice journal** to view the principal's invoice.</span></span>
    - <span data-ttu-id="237de-193">Выберите **Доверитель** \> **Счет-фактура** для просмотра счета-фактуры доверителя.</span><span class="sxs-lookup"><span data-stu-id="237de-193">Select **Principal** \> **Facture** to view the principal's facture.</span></span>
    - <span data-ttu-id="237de-194">Выберите **Запросы** \> **Журнал накладных** для просмотра исходной накладной продавца.</span><span class="sxs-lookup"><span data-stu-id="237de-194">Select **Inquiries** \> **Invoice journal** to view the seller's original invoice.</span></span>
    - <span data-ttu-id="237de-195">Выберите **Запросы** \> **Счет-фактура** для просмотра исходного счета-фактуры продавца.</span><span class="sxs-lookup"><span data-stu-id="237de-195">Select **Inquiries** \> **Facture** to view the seller's original facture.</span></span>

15. <span data-ttu-id="237de-196">Выберите **Печать**, чтобы открыть диалоговое окно **Отчет для доверителя в Microsoft Excel**, затем выберите **OK**, чтобы напечатать отчет для доверителя.</span><span class="sxs-lookup"><span data-stu-id="237de-196">Select **Print** to open the **Report for principal to Microsoft Excel** dialog box, and then select **OK** to print the report for the principal.</span></span>

![Создание отчета для доверителя](media/11_Report_for_a_principal.jpg)


## <a name="print-a-facture-accounting-journal"></a><span data-ttu-id="237de-198">Печать журнала учета счетов-фактур</span><span class="sxs-lookup"><span data-stu-id="237de-198">Print a facture accounting journal</span></span>

1. <span data-ttu-id="237de-199">Выберите **Главная книга** \> **Запросы и отчеты** \> **Отчеты журналов** \> **Счет-фактура**, чтобы открыть диалоговое окно **Журнал учета счетов-фактур**.</span><span class="sxs-lookup"><span data-stu-id="237de-199">Go to **General ledger** \> **Inquiries and reports** \> **Journal reports** \> **Facture** to open the **Facture accounting journal** dialog box.</span></span>
2. <span data-ttu-id="237de-200">Укажите период для отчета, затем выберите **OK**, чтобы напечатать журнал учета счетов-фактур.</span><span class="sxs-lookup"><span data-stu-id="237de-200">Specify the period for the report, and then select **OK** to print the facture accounting journal.</span></span>

<span data-ttu-id="237de-201">Лист **Выпущенные** журнала учета счетов-фактур показывает повторно выпущенные счета-фактуры поставщика.</span><span class="sxs-lookup"><span data-stu-id="237de-201">The **Issued** worksheet of the facture accounting journal shows the reissued vendor's factures.</span></span> <span data-ttu-id="237de-202">Сведения о продавцах представлены в столбцах с 10 по 12.</span><span class="sxs-lookup"><span data-stu-id="237de-202">The information about the sellers is presented in columns 10 through 12.</span></span>

![Лист "Выпущенные" журнала учета счетов-фактур](media/12_Facture_accounting_journal_Part_1.jpg)

<span data-ttu-id="237de-204">На листе **Получено** журнала учета счетов-фактуры отображаются счета-фактуры исходного продавца, которые были утверждены в отчете для доверителя.</span><span class="sxs-lookup"><span data-stu-id="237de-204">The **Received** worksheet of the Facture accounting journal shows the original seller's factures that were approved in the report for the principal.</span></span>

![Лист "Получено" журнала учета счетов-фактур](media/13_Facture_accounting_journal_Part_2.jpg)

## <a name="prepayments"></a><span data-ttu-id="237de-206">Предоплаты</span><span class="sxs-lookup"><span data-stu-id="237de-206">Prepayments</span></span>

<span data-ttu-id="237de-207">Предоплаты, полученные от доверителя, не являются источником для начисления НДС.</span><span class="sxs-lookup"><span data-stu-id="237de-207">Prepayments that are received from a principal aren't a source for charging VAT.</span></span> <span data-ttu-id="237de-208">Они должны быть повторно отправлены одному или нескольким продавцам.</span><span class="sxs-lookup"><span data-stu-id="237de-208">They must be re-sent to one or more sellers.</span></span> <span data-ttu-id="237de-209">Эти повторно отправленные предоплаты должны быть включены в отчет для доверителя.</span><span class="sxs-lookup"><span data-stu-id="237de-209">These re-sent prepayments must be included on the report for the principal.</span></span> <span data-ttu-id="237de-210">Предоплаты, полученные от двух или более доверителей, могут быть повторно отправлены одному продавцу.</span><span class="sxs-lookup"><span data-stu-id="237de-210">Prepayments that are received from two or more principals can be re-sent to one seller.</span></span> <span data-ttu-id="237de-211">Эти повторно отправленные предоплаты должны быть включены в отчеты для доверителей.</span><span class="sxs-lookup"><span data-stu-id="237de-211">These re-sent prepayment must be included on the reports for the principals.</span></span>

### <a name="create-prepayments-a-purchase-order-a-sales-order-and-a-report-for-a-principal"></a><span data-ttu-id="237de-212">Создание предоплат, заказа на покупку, заказа на продажу и отчета для доверителя</span><span class="sxs-lookup"><span data-stu-id="237de-212">Create prepayments, a purchase order, a sales order, and a report for a principal</span></span>

1. <span data-ttu-id="237de-213">На странице **Журнал платежей клиентов** создайте предоплату клиента, затем выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="237de-213">On the **Customer payment journal** page, create a customer prepayment, and then select **Lines**.</span></span>
2. <span data-ttu-id="237de-214">На странице **Платежи клиентов** в столбце **Вид действия** выберите **Комиссионер**, чтобы указать, что предоплата будет повторно отправлена продавцам.</span><span class="sxs-lookup"><span data-stu-id="237de-214">On the **Customer payments** page, in the **Kind of activity** column, select **Commission agent** to indicate that the prepayment will be re-sent to the sellers.</span></span>

    > [!NOTE]
    > <span data-ttu-id="237de-215">Если столбец **Вид действия** не отображается, щелкните правой кнопкой мыши в строке, содержащей названия столбцов, затем выберите **Добавить столбцы**.</span><span class="sxs-lookup"><span data-stu-id="237de-215">If you don't see the **Kind of activity** column, right-click in the row that has the column names, and then select **Add columns**.</span></span> <span data-ttu-id="237de-216">Установите флажок для столбца **Вид действия**, затем выберите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="237de-216">Select the check box for the **Kind of activity** column, and then select **Insert**.</span></span>

      ![Страница журнала платежей поставщика](media/14_Customer_payments.jpg)

3. <span data-ttu-id="237de-218">На странице **Журнал платежей поставщикам** создайте предоплату поставщику, затем выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="237de-218">On the **Vendor payment journal** page, create a vendor prepayment, and then select **Lines**.</span></span>
4. <span data-ttu-id="237de-219">На странице **Платежи поставщикам** в столбце **Вид действия** выберите **Комиссионер**.</span><span class="sxs-lookup"><span data-stu-id="237de-219">On the **Vendor payments** page, in the **Kind of activity** column, select **Commission agent**.</span></span>

    ![Страница платежей поставщикам](media/15_Vendor_payments.jpg)

5. <span data-ttu-id="237de-221">Создайте счет-фактуру для предоплаты поставщику.</span><span class="sxs-lookup"><span data-stu-id="237de-221">Create a facture for the vendor prepayment.</span></span>
6. <span data-ttu-id="237de-222">Создайте заказ на покупку и счет-фактуру.</span><span class="sxs-lookup"><span data-stu-id="237de-222">Create a purchase order and a facture.</span></span>
7. <span data-ttu-id="237de-223">Создайте заказ на продажу и счет.</span><span class="sxs-lookup"><span data-stu-id="237de-223">Create a sales order and an invoice.</span></span>
8. <span data-ttu-id="237de-224">Создайте отчет для доверителя и обновите строки в отгрузках.</span><span class="sxs-lookup"><span data-stu-id="237de-224">Create a report for the principal, and update the lines on shipments.</span></span>
9. <span data-ttu-id="237de-225">В нижней части страницы **Отчет для доверителя** на вкладке **Предоплаты** в поле **Ваучер** выберите ваучер предоплаты поставщику, чтобы включить эту предоплату в отчет для доверителя.</span><span class="sxs-lookup"><span data-stu-id="237de-225">In the bottom part of the **Report for principal** page, on the **Prepayments** tab, in the **Voucher** field, select the vendor prepayment voucher to include the prepayment on the report for the principal.</span></span>

    ![Страница отчета для доверителя, вкладка предоплаты](media/16_Report_for_principal.jpg)

10. <span data-ttu-id="237de-227">Выберите **Проводки** для просмотра распределенной суммы в поле **Сумма в валюте отчетности**.</span><span class="sxs-lookup"><span data-stu-id="237de-227">Select **Transactions** to view the allocated amount in the **Amount in reporting currency** field.</span></span>

    ![Страница проводок по поставщику](media/17_Vendor_transactions.jpg)

11. <span data-ttu-id="237de-229">На странице **Отчет для доверителя** утвердите строки на вкладке **Обзор** и ваучеры на вкладке **Предоплаты**.</span><span class="sxs-lookup"><span data-stu-id="237de-229">On the **Report for principal** page, approve lines on the **Overview** tab and vouchers on the **Prepayments** tab.</span></span>
12. <span data-ttu-id="237de-230">Можно создать счет-фактуру и просмотреть счет доверителя (или счет-фактуру) или исходный счет (или счет-фактуру).</span><span class="sxs-lookup"><span data-stu-id="237de-230">You can create a facture, and view the principal's invoice (or facture) or the original invoice (or facture).</span></span>

### <a name="print-a-report-for-the-principal"></a><span data-ttu-id="237de-231">Печать отчета для доверителя</span><span class="sxs-lookup"><span data-stu-id="237de-231">Print a report for the principal</span></span>

<span data-ttu-id="237de-232">Напечатайте отчет для доверителя.</span><span class="sxs-lookup"><span data-stu-id="237de-232">Print a report for the principal.</span></span> <span data-ttu-id="237de-233">Отчет для доверителя имеет два раздела: один для отгрузок, другой для предоплат.</span><span class="sxs-lookup"><span data-stu-id="237de-233">The report for the principal has two sections: one for shipments and one for prepayments.</span></span>


![Созданный отчет о покупке](media/18_Purchase_report.jpg)

### <a name="create-a-prepayment-facture"></a><span data-ttu-id="237de-235">Создание счета-фактуры на предоплату</span><span class="sxs-lookup"><span data-stu-id="237de-235">Create a prepayment facture</span></span>

1. <span data-ttu-id="237de-236">На странице **Отчет для доверителя** на вкладке **Предоплаты** установите флажок **Утвердить**, затем выберите **Создать счет-фактуру**, чтобы зарегистрировать счет-фактуру на предоплату для доверителя.</span><span class="sxs-lookup"><span data-stu-id="237de-236">On the **Report for principal** page, on the **Prepayments** tab, select the **Approve** check box, and then select **Create facture** to register the principal's facture on the prepayment.</span></span>
2. <span data-ttu-id="237de-237">На странице **Создание счета-фактуры** используйте флажок **Отметить** для выбора соответствующих предоплат.</span><span class="sxs-lookup"><span data-stu-id="237de-237">On the **Facture create** page, use the **Mark** check box to select the relevant prepayments.</span></span>
3. <span data-ttu-id="237de-238">Выберите **Создать счет-фактуру**, чтобы открыть диалоговое окно **Создание счета-фактуры**.</span><span class="sxs-lookup"><span data-stu-id="237de-238">Select **Create facture** to open the **Facture create** dialog box.</span></span>
4. <span data-ttu-id="237de-239">Укажите дату регистрации, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="237de-239">Specify the date of the registration, and then select **OK**.</span></span>

    ![Диалоговое окно создания счета-фактуры](media/19_Facture_create.jpg)

5. <span data-ttu-id="237de-241">На странице **Отчет для доверителя** на вкладке **Предоплаты** выберите **Доверитель \> Счет-фактура**, чтобы просмотреть зарегистрированный счет-фактуру доверителя для предоплаты.</span><span class="sxs-lookup"><span data-stu-id="237de-241">On the **Report for principal** page, on the **Prepayments** tab, select **Principal \> Facture** to view the registered principal's facture for prepayment.</span></span>

    ![Страница журнала счетов-фактур](media/20_Facture_journal.jpg)

6. <span data-ttu-id="237de-243">Выберите **Печать \> Оригинал** для печати исходного счета-фактуры или выберите **Печать \> Копия**, чтобы напечатать копию счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="237de-243">Select **Print \> Original** to print the original facture, or select **Print \> Copy** to print the facture copy.</span></span>


![Распечатанный счет-фактура](media/21_Invoice-facture.jpg)

### <a name="create-a-facture-accounting-journal"></a><span data-ttu-id="237de-245">Создание журнала учета счетов-фактур</span><span class="sxs-lookup"><span data-stu-id="237de-245">Create a facture accounting journal</span></span>

<span data-ttu-id="237de-246">В журнале учета счетов-фактур отображаются утвержденные строки.</span><span class="sxs-lookup"><span data-stu-id="237de-246">The facture accounting journal shows approved lines.</span></span> <span data-ttu-id="237de-247">Можно распечатать журнал учета счетов-фактур.</span><span class="sxs-lookup"><span data-stu-id="237de-247">You can print a facture accounting journal.</span></span>

<span data-ttu-id="237de-248">Предоплаты, полученные от доверителя, будут переведены продавцу.</span><span class="sxs-lookup"><span data-stu-id="237de-248">The prepayments that are received from the principal will be transferred to the seller.</span></span> <span data-ttu-id="237de-249">Когда продавец выдает для агента счет-фактуру на предоплату, агент регистрирует счета-фактуры продавца на листе **Получено** журнала учета счетов-фактур.</span><span class="sxs-lookup"><span data-stu-id="237de-249">When the seller issues the prepayment facture to the agent, the agent registers the seller's factures on the **Received** worksheet of the facture accounting journal.</span></span> <span data-ttu-id="237de-250">Лист **Выдано** журнала учета счетов-фактур отражает счета-фактуры, которые были повторно выпущены для доверителя.</span><span class="sxs-lookup"><span data-stu-id="237de-250">The **Issued** worksheet of the facture accounting journal reflects the factures that have been reissued to the principal.</span></span>

<span data-ttu-id="237de-251">Оригинальные счета-фактуры на поставку товаров от продавцов могут быть распределены между доверителями.</span><span class="sxs-lookup"><span data-stu-id="237de-251">The original factures on the delivery of goods from sellers can be allocated among the principals.</span></span> <span data-ttu-id="237de-252">Лист **Получено** журнала учета счетов-фактур отражает исходные счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="237de-252">The **Received** worksheet of the facture accounting journal reflects the original factures.</span></span>

![Журнал учета счетов-фактур, лист "Получено"](media/22_Facture_accounting_journal_Part_2.jpg)

<span data-ttu-id="237de-254">Лист **Выдано** журнала учета счетов-фактур отражает повторно выпущенные счета-фактуры (т. е., выделенные части счетов-фактур продавцов).</span><span class="sxs-lookup"><span data-stu-id="237de-254">The **Issued** worksheet of the facture accounting journal reflects the reissued factures (that is, the allocated parts of sellers' factures).</span></span> <span data-ttu-id="237de-255">Сведения о продавцах представлены в столбцах с 10 по 12.</span><span class="sxs-lookup"><span data-stu-id="237de-255">The information about the sellers is presented in columns 10 through 12.</span></span>

![Журнал учета счетов-фактур, лист "Выпущенные"](media/23_Facture_accounting_journal_Part_1.jpg)

<span data-ttu-id="237de-257">Более подробную информацию см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="237de-257">Find more details in the following topics:</span></span>

- [<span data-ttu-id="237de-258">Проводки через посредников</span><span class="sxs-lookup"><span data-stu-id="237de-258">Transactions through intermediary</span></span>](rus-transactions-through-intermediary.md) 
- [<span data-ttu-id="237de-259">Продажи по комиссии</span><span class="sxs-lookup"><span data-stu-id="237de-259">Sales on commission</span></span>](rus-sales-on-commission.md)
