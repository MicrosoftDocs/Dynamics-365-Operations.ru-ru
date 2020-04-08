---
title: Продажи по комиссии
description: В этой теме приводятся сведения о функциональности продажи по комиссии.
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
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 16e4aaae6505efcbe4bc50e322bcabd732dc6dba
ms.sourcegitcommit: 1fb34abfe3382bc00237a2c00184fe201c12229f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2020
ms.locfileid: "3151310"
---
# <a name="sales-on-commission"></a><span data-ttu-id="1cdbb-103">Продажи по комиссии</span><span class="sxs-lookup"><span data-stu-id="1cdbb-103">Sales on commission</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="1cdbb-104">Доверитель нанимает посредника (комиссионера) для продажи, от собственного имени комиссионера, товары доверителя (работу или услуги) третьим лицам.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-104">The principal engages the intermediary (commissioner) to sell, in the commissioner's own name, the principal's goods (works or services) to third parties.</span></span>

<span data-ttu-id="1cdbb-105">Посредник выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1cdbb-105">The intermediary performs the following actions:</span></span>

- <span data-ttu-id="1cdbb-106">Регистрирует счета-фактуры, который был выпущен для покупателя третьей стороны, на листе **Выпущено** журнала учета счетов-фактур при отгрузке товаров.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-106">Register a facture that was issued to a third-party buyer on the **Issued** worksheet of the facture accounting journal when goods are shipped.</span></span>
- <span data-ttu-id="1cdbb-107">Не регистрируйте счет-фактуру в книге продаж, так как товары принадлежат доверителю, и у посредника нет обязательств на оплату НДС.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-107">Don't register a facture in the sales book, because the goods belong to the principal, and the intermediary doesn't have the obligation to charge VAT.</span></span>
- <span data-ttu-id="1cdbb-108">Сообщите доверителю данные счета-фактуры, чтобы доверитель мог повторно выпустить счет-фактуру от своего имени.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-108">Inform the principal about the facture details, so that the principal can reissue the facture in his or her own name.</span></span>

<span data-ttu-id="1cdbb-109">После того как повторно выпущенный счет-фактура получен от доверителя, комиссионер регистрирует его на листе **Получено** журнала учета счетов-фактур.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-109">After the reissued facture is received from the principal, the commissioner registers it on the **Received** worksheet of the facture accounting journal.</span></span> <span data-ttu-id="1cdbb-110">Однако комиссионер не делает записи в книге покупок.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-110">However, the commissioner doesn't make an entry in the purchase book.</span></span>

<span data-ttu-id="1cdbb-111">Если договор содержит условия предоплаты, процедура регистрации для повторного выпуска счета-фактуры аналогична.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-111">If the agreement includes prepayment terms, the registration procedure for reissuing a facture is similar.</span></span>

<span data-ttu-id="1cdbb-112">На следующем рисунке показан бизнес-процесс регистрации сделок через посредника.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-112">The following illustration shows the business process for registering intermediary deals.</span></span> <span data-ttu-id="1cdbb-113">В системе отражены прямоугольные элементы.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-113">Rectangular elements are reflected in the system.</span></span> <span data-ttu-id="1cdbb-114">Овальные элементы присутствуют в бизнес-процессе, но не отражаются в системе.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-114">Oval elements are present in the business process but aren't reflected in the system.</span></span>

![Поток бизнес-процесса регистрация промежуточных сделок, продажи по комиссии](media/Sales_on_commission_english.jpg)

## <a name="create-a-purchase-agreement-for-a-sale-by-a-commissioner"></a><span data-ttu-id="1cdbb-116">Создание договора покупки для продажи комиссионером</span><span class="sxs-lookup"><span data-stu-id="1cdbb-116">Create a purchase agreement for a sale by a commissioner</span></span>

1. <span data-ttu-id="1cdbb-117">Перейдите **Расчеты с поставщиками** \> **Заказы на покупку** \> **Договоры покупки** или **Закупки и источники** \> **Договоры покупки** \> **Договоры покупки**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-117">Go to **Accounts payable** \> **Purchase orders** \> **Purchase agreements** or **Procurement and sourcing** \> **Purchase agreements** \> **Purchase agreements**.</span></span>
2. <span data-ttu-id="1cdbb-118">Выберите **Создать**, чтобы открыть диалоговое окно **Создание договора покупки**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-118">Select **New** to open the **Create purchase agreement** dialog box.</span></span>
3. <span data-ttu-id="1cdbb-119">На экспресс-вкладке **Поставщик** укажите счет поставщика, затем в поле **Классификация договоров покупки** выберите **Общий договор покупки**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-119">On the **Vendor** FastTab, specify the vendor account, and then, in the **Purchase agreement classification** field, select **Blanket purchase agreement**.</span></span>
4. <span data-ttu-id="1cdbb-120">На экспресс-вкладке **Общие сведения** в разделе **Документ** в поле **Код договора покупки** укажите код договора покупки.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-120">On the **General** FastTab, in the **Document** section, in the **Purchase agreement** field, specify the identifier of the purchase agreement.</span></span>
5. <span data-ttu-id="1cdbb-121">Укажите другие сведения, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-121">Specify other details, and then select **OK**.</span></span>

    ![Диалоговое окно создания классификаций договоров покупки](media/24_Create_purchase_agreement.jpg)

6. <span data-ttu-id="1cdbb-123">На странице **Договоры покупки** перейдите в представление **Заголовок**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-123">On the **Purchase agreements** page, switch to the **Header** view.</span></span>
7. <span data-ttu-id="1cdbb-124">На Экспресс-вкладке **Общие сведения** в разделе **Документ** в поле **Комиссионное соглашение** выберите **Продажа комиссионером**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-124">On the **General** FastTab, in the **Document** section, in the **Commission agreement** field, select **Sale by commissioner**.</span></span>
8. <span data-ttu-id="1cdbb-125">На экспресс-вкладке **Финансы** в разделе **Профиль учета** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="1cdbb-125">On the **Financial** FastTab, in the **Inventory profile** section, specify the following details:</span></span>

    - <span data-ttu-id="1cdbb-126">В поле **Вид деятельности** выберите **Комиссионер**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-126">In the **Kind of activity** field, select **Commission agent**.</span></span>
    - <span data-ttu-id="1cdbb-127">В поле **Профиль учета** выберите профиль учета, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-127">In the **Inventory profile** field, select the inventory profile that you created earlier.</span></span>

    ![Страница договоров покупки, экспресс-вкладка финансов](media/25_Purchase_agreements.jpg)

9. <span data-ttu-id="1cdbb-129">На панели операций на вкладке **Договор покупки** в группе **Создать** выберите **Подтверждение** для обновления статуса договора до **Действует**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-129">On the Action Pane, on the **Purchase agreement** tab, in the **Generate** group, select **Confirmation** to update the status of the agreement to **Effective**.</span></span>

## <a name="create-inventory-owners-principals"></a><span data-ttu-id="1cdbb-130">Создание владельцев запасов (доверителей)</span><span class="sxs-lookup"><span data-stu-id="1cdbb-130">Create inventory owners (principals)</span></span>

1. <span data-ttu-id="1cdbb-131">Перейдите в раздел **Управление запасами** \> **Настройка** \> **Аналитики** \> **Владельцы запасов**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-131">Go to **Inventory management** \> **Setup** \> **Dimensions** \> **Inventory owners**.</span></span>
2. <span data-ttu-id="1cdbb-132">Выберите **Создать**, чтобы создать владельца запасов.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-132">Select **New** to create an inventory owner.</span></span>
3. <span data-ttu-id="1cdbb-133">В поле **Владелец** введите код для владельца.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-133">In the **Owner** field, enter the code for the owner.</span></span>
4. <span data-ttu-id="1cdbb-134">В поле **Тип счета** выберите **Поставщик**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-134">In the **Account type** field, select **Vendor**.</span></span>
5. <span data-ttu-id="1cdbb-135">В поле **Организация** выберите код для доверителя.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-135">In the **Account** field, select the code for the principal.</span></span> <span data-ttu-id="1cdbb-136">Поле **Имя** заполняется автоматически.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-136">The **Name** field is automatically filled in.</span></span>
6. <span data-ttu-id="1cdbb-137">В поле **Код договора** выберите договор покупки, созданный ранее, чтобы связать владельца с договором.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-137">In the **Agreement ID** field, select the purchase agreement that you created earlier, to associate the owner with the agreement.</span></span>
7. <span data-ttu-id="1cdbb-138">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-138">Select **Save**.</span></span>

## <a name="create-a-purchase-order-and-generate-a-purchase-invoice"></a><span data-ttu-id="1cdbb-139">Создание заказа на покупку и создание накладной по покупке</span><span class="sxs-lookup"><span data-stu-id="1cdbb-139">Create a purchase order and generate a purchase invoice</span></span>

1. <span data-ttu-id="1cdbb-140">Создание заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-140">Create a purchase order.</span></span>
2. <span data-ttu-id="1cdbb-141">В поле **Договор покупки** выберите договор для продажи комиссионером, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-141">In the **Purchase agreement** field, select the agreement for a sale by the commissioner that you created earlier.</span></span>
3. <span data-ttu-id="1cdbb-142">В строке заказа на покупку выберите код номенклатуры, которая была продана ранее.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-142">On the purchase order line, select the item number that was sold earlier.</span></span>

  > [!NOTE]
  > <span data-ttu-id="1cdbb-143">В поле **Аналитика отслеживания** для данной номенклатуры должен быть указан профиль учета, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-143">The **Tracking dimension** field for the item should be set to the inventory profile that you created earlier.</span></span>

4. <span data-ttu-id="1cdbb-144">На экспресс-вкладке **Сведения по строке** на вкладке **Продукт** в разделе **Аналитики отслеживания** убедитесь, что в поле **Профиль учета** автоматически задан профиль учета, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-144">On the **Line details** FastTab, on the **Product** tab, in the **Tracking dimensions** section, make sure that the **Inventory profile** field is automatically set to the inventory profile that you created earlier.</span></span>
5. <span data-ttu-id="1cdbb-145">В поле **Владелец** выберите владельца (доверителя), созданного ранее.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-145">In the **Owner** field, select the owner (principal) that you created earlier.</span></span>

    ![Страница "Заказ на покупку"](media/26_All_purchase_orders.jpg)

6. <span data-ttu-id="1cdbb-147">Разноска накладной.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-147">Post the invoice.</span></span>

## <a name="create-a-sales-order-and-update-the-facture"></a><span data-ttu-id="1cdbb-148">Создание заказа на продажу и обновление счета-фактуры</span><span class="sxs-lookup"><span data-stu-id="1cdbb-148">Create a sales order and update the facture</span></span>

1. <span data-ttu-id="1cdbb-149">Создание заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-149">Create a sales order.</span></span>
2. <span data-ttu-id="1cdbb-150">В строке заказа на продажу выберите код номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-150">On sales order line, select the item number.</span></span>

   > [!NOTE]
   > <span data-ttu-id="1cdbb-151">В поле **Аналитика отслеживания** для данной номенклатуры должен быть указан профиль учета, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-151">The **Tracking dimension** field for the item should be set to the inventory profile that you created earlier.</span></span>

3. <span data-ttu-id="1cdbb-152">На экспресс-вкладке **Сведения по строке** на вкладке **Продукт** в разделе **Аналитики отслеживания** выберите профиль запасов и владельца (доверителя), которые были созданы ранее.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-152">On the **Line details** FastTab, on the **Product** tab, in the **Tracking dimensions** section, select the inventory profile and owner (principal) that you created earlier.</span></span>
4. <span data-ttu-id="1cdbb-153">На экспресс-вкладке **Строки заказа на продажу** выберите **Запасы \> Маркировка**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-153">On the **Sales order lines** FastTab, select **Inventory \> Marking**.</span></span>
5. <span data-ttu-id="1cdbb-154">Выберите проводку покупки, выберите **Пометить**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-154">Select a purchase transaction, select **Set mark now**, and then select **OK**.</span></span>

    ![Страница заказа на продажу](media/27_Sales_order.jpg)

6. <span data-ttu-id="1cdbb-156">Укажите другие параметры заказа на продажу и создайте счет-фактуру.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-156">Specify other sales order parameters, and create a facture.</span></span>

## <a name="create-and-print-a-report-for-a-principal-and-reissue-the-buyers-factures-to-the-principal"></a><span data-ttu-id="1cdbb-157">Создание и печать отчета для доверителя и повторный выпуск счетов-фактур покупателя для доверителя</span><span class="sxs-lookup"><span data-stu-id="1cdbb-157">Create and print a report for a principal, and reissue the buyer's factures to the principal</span></span>

1. <span data-ttu-id="1cdbb-158">Перейдите к пункту **Главная книга** \> **Периодические задачи** \> **Комиссионная торговля** \> **Отчет для доверителя**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-158">Go to **General ledger** \> **Periodic tasks** \> **Commission trade** \> **Report for principal**.</span></span>
2. <span data-ttu-id="1cdbb-159">Выберите **Создать**, чтобы открыть диалоговое окно **Создание отчета для доверителя**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-159">Select **New** to open the **Create report for principal** dialog box.</span></span>
3. <span data-ttu-id="1cdbb-160">В полях **Дата начала** и **Дата окончания** укажите период для отчета.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-160">In the **From date** and **To date** fields, specify the period for the report.</span></span>

   >[!NOTE]
   > <span data-ttu-id="1cdbb-161">Поле **Дата начала** можно оставить пустым.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-161">You can leave the **From date** field blank.</span></span>

4. <span data-ttu-id="1cdbb-162">В поле **Тип доверителя** выберите **Поставщик**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-162">In the **Principal type** field, select **Vendor**.</span></span>
5. <span data-ttu-id="1cdbb-163">В поле **Код партнера** выберите счет поставщика.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-163">In the **Partner code** field, select the vendor account.</span></span>
6. <span data-ttu-id="1cdbb-164">В поле **Код договора** выберите договор покупки.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-164">In the **Agreement ID** field, select the purchase agreement.</span></span>
7. <span data-ttu-id="1cdbb-165">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-165">Select **OK**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="1cdbb-166">Для создания заголовков для всех отчетов по доверителю, которые необходимы в течение указанного периода, выберите **Функции** \> **Создать заголовки отчетов по отгрузкам**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-166">To create the headers for all the reports for the principal that are required in the specified period, select **Functions** \> **Create report headers on shipments**.</span></span>

8. <span data-ttu-id="1cdbb-167">Выберите **Функции** \> **Обновить строки отгрузки**, чтобы открыть диалоговое окно **Создание отчета для доверителя по отгрузкам**, затем выберите **OK**, чтобы создать строки для каждого отчета.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-167">Select **Functions** \> **Update lines on shipment** to open the **Generate report for principal on shipments** dialog box, and then select **OK** to create the lines for every report.</span></span>
9. <span data-ttu-id="1cdbb-168">Выберите **Печать**, чтобы открыть диалоговое окно **Отчет для доверителя в Microsoft Excel**, затем выберите **OK**, чтобы напечатать отчет для доверителя.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-168">Select **Print** to open the **Report for principal to Microsoft Excel** dialog box, and then select **OK** to print the report for the principal.</span></span>
10. <span data-ttu-id="1cdbb-169">Доверитель заново выпускает счет-фактуру для агента на основе счетов-фактур, которые агент выдает покупателю.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-169">The principal reissues the facture to the agent, based on the factures that the agent issues to the buyer.</span></span> <span data-ttu-id="1cdbb-170">Доверитель узнает об этих счетах-фактурах из печатного отчета для доверителя.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-170">The principal learns about these factures from the printed report for the principal.</span></span> <span data-ttu-id="1cdbb-171">Используйте флажок **Утверждено**, чтобы выбрать строки, для которых доверитель повторно выпускает счет-фактуру, затем выберите **Утверждение** \> **Утвердить все**, чтобы утвердить строки отчета.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-171">Use the **Approved** check box to select the lines that the principal reissues the facture for, and then select **Approval** \> **Approve all** to approve the lines on the report.</span></span>

    ![Страница отчета для доверителя](media/29_Report_for_principal.jpg)

11. <span data-ttu-id="1cdbb-173">Выберите **Счет-фактура** \> **Обновить счет-фактуру**, чтобы создать счета-фактуры, повторно выпущенные доверителем.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-173">Select **Facture** \> **Update facture** to generate the factures that were reissued by the principal.</span></span>
12. <span data-ttu-id="1cdbb-174">На странице **Обновить счет-фактуру** в разделе **Комиссионная торговля** убедитесь, что поля **Покупатель** и **Счет-фактура** настроены автоматически.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-174">On the **Update facture** page, in the **Commission trade** section, make sure that the **Buyer** and **Facture** fields are automatically set.</span></span> <span data-ttu-id="1cdbb-175">Если они пусты, выберите клиента в поле **Покупатель** и номер счета-фактуры заказа на продажу, который был создан в поле **Счет-фактура**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-175">If they are blank, select the customer in the **Buyer** field and the number of the sales order facture that was created in the **Facture** field.</span></span>
13. <span data-ttu-id="1cdbb-176">Укажите другие необходимые сведения и создайте счет-фактуру.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-176">Specify other required details, and create the facture.</span></span>

    ![Страница обновления счета-фактуры](media/30_Update_facture.jpg)

14. <span data-ttu-id="1cdbb-178">На странице **Отчет для доверителя** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1cdbb-178">On the **Report for principal** page, do the following:</span></span>

    - <span data-ttu-id="1cdbb-179">Выберите **Доверитель** \> **Журнал накладных** для просмотра накладной доверителя.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-179">Select **Principal** \> **Invoice journal** to view the principal's invoice.</span></span>
    - <span data-ttu-id="1cdbb-180">Выберите **Доверитель** \> **Счет-фактура** для просмотра счета-фактуры доверителя.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-180">Select **Principal** \> **Facture** to view the principal's facture.</span></span>
    - <span data-ttu-id="1cdbb-181">Выберите **Запросы** \> **Журнал накладных** для просмотра исходной накладной для покупателя.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-181">Select **Inquiries** \> **Invoice journal** to view the original invoice to the buyer.</span></span>
    - <span data-ttu-id="1cdbb-182">Выберите **Запросы** \> **Счет-фактура** для просмотра исходного счета-фактуры для покупателя.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-182">Select **Inquiries** \> **Facture** to view the original facture to the buyer.</span></span>

## <a name="print-a-facture-accounting-journal"></a><span data-ttu-id="1cdbb-183">Печать журнала учета счетов-фактур</span><span class="sxs-lookup"><span data-stu-id="1cdbb-183">Print a facture accounting journal</span></span>

<span data-ttu-id="1cdbb-184">Утвержденные строки отчета для доверителя регистрируются на листе **Получено** журнала учета счетов-фактуры.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-184">The approved lines of the report for the principal are registered on the **Received** worksheet of the facture accounting journal.</span></span> <span data-ttu-id="1cdbb-185">Эта информация отражает сведения о доверителе в исходных счетах-фактурах на листе **Выдано** журнала учета счетов-фактур.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-185">The information reflects the information about the principal in the original factures on the **Issued** worksheet of the facture accounting journal.</span></span>

1. <span data-ttu-id="1cdbb-186">Чтобы распечатать журнал учета счетов-фактур, выберите **Главная книга** \> **Запросы и отчеты** \> **Отчеты журналов** \> **Журнал учета счетов-фактур**, чтобы открыть диалоговое окно **Журнал учета счетов-фактур**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-186">To print the facture accounting journal, go to **General ledger** \> **Inquiries and reports** \> **Journal reports** \> **Facture accounting journal** to open the **Facture accounting journal** dialog box.</span></span>
2. <span data-ttu-id="1cdbb-187">Укажите период для отчета, затем выберите **OK**, чтобы напечатать журнал учета счетов-фактур.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-187">Specify the period for the report, and then select **OK** to print the facture accounting journal.</span></span>

<span data-ttu-id="1cdbb-188">В формате печати журнала учета счетов-фактур исходные счета-фактуры для покупателей распределяются между доверителями.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-188">In the printing format of the facture accounting journal, the original factures to buyers are allocated among the principals.</span></span> <span data-ttu-id="1cdbb-189">Лист **Выдано** журнала учета счетов-фактур отражает распределенные части счетов-фактур клиентов.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-189">The **Issued** worksheet of the facture accounting journal reflects the allocated parts of the customer's factures.</span></span> <span data-ttu-id="1cdbb-190">Сведения о доверителях представлены в столбцах с 10 по 12.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-190">The information about the principals is presented in columns 10 through 12.</span></span>

![Лист "Выпущенные" журнала учета счетов-фактур](media/31_Facture_accounting_journal_Part_1.jpg)

<span data-ttu-id="1cdbb-192">Лист **Получено** журнала учета счетов-фактур отражает счета-фактуры, которые были подтверждены доверителем.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-192">The **Received** worksheet of the facture accounting journal reflects the factures that are confirmed by the principal.</span></span>

![Лист "Получено" журнала учета счетов-фактур](media/32_Facture_accounting_journal_Part_2.jpg)

## <a name="prepayments"></a><span data-ttu-id="1cdbb-194">Предоплаты</span><span class="sxs-lookup"><span data-stu-id="1cdbb-194">Prepayments</span></span>


### <a name="create-prepayments-a-sales-order-a-purchase-order-and-a-report-for-a-principal"></a><span data-ttu-id="1cdbb-195">Создание предоплат, заказа на продажу, заказа на покупку и отчета для доверителя</span><span class="sxs-lookup"><span data-stu-id="1cdbb-195">Create prepayments, a sales order, a purchase order, and a report for a principal</span></span>

<span data-ttu-id="1cdbb-196">Сумма предоплаты, полученной от клиента, может быть распределена между различными доверителями.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-196">The amount of prepayment that is received from the customer can be allocated among different principals.</span></span> <span data-ttu-id="1cdbb-197">Сумму платежа также можно изменить.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-197">The payment sum can also be edited.</span></span> <span data-ttu-id="1cdbb-198">Система гарантирует, что сумма, распределенная среди доверителей, не превысит исходную предоплату.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-198">The system makes sure that the amount that is allocated among principals doesn't exceed the original prepayment.</span></span> <span data-ttu-id="1cdbb-199">Оставшаяся сумма предоплаты может быть распределена другому доверителю или тому же доверителю в другом отчете для доверителя.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-199">The remaining prepayment amount can be allocated to another principal or to the same principal on another principal report.</span></span> <span data-ttu-id="1cdbb-200">Проводки НДС не будут разноситься в главной книге, несмотря на то, что был создан счет-фактура на предоплату поставщику.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-200">No VAT transactions will be posted in the general ledger, in spite of the vendor prepayment facture that is created.</span></span>

1. <span data-ttu-id="1cdbb-201">На странице **Журнал платежей клиентов** создайте предоплату клиента, затем выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-201">On the **Customer payment journal** page, create a customer prepayment, and then select **Lines**.</span></span>
2. <span data-ttu-id="1cdbb-202">На странице **Платежи клиентов** в столбце **Вид действия** выберите **Комиссионер**, чтобы указать, что предоплата должна быть передана доверителю.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-202">On the **Customer payments** page, in the **Kind of activity** column, select **Commission agent** to indicate that the prepayment is subject to transfer to the principal.</span></span>

  > [!NOTE]
  > <span data-ttu-id="1cdbb-203">Если столбец **Вид действия** не отображается, щелкните правой кнопкой мыши в строке, содержащей названия столбцов, затем выберите **Добавить столбцы**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-203">If you don't see the **Kind of activity** column, right-click in the row that has the column names, and then select **Add columns**.</span></span> <span data-ttu-id="1cdbb-204">Установите флажок для столбца **Вид действия**, затем выберите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-204">Select the check box for the **Kind of activity** column, and then select **Insert**.</span></span>

   ![Страница платежей клиентов](media/33_Customer_payments.jpg)

3. <span data-ttu-id="1cdbb-206">На странице **Журнал платежей поставщикам** создайте предоплату поставщику, который имеет счет-фактуру, затем выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-206">On the **Vendor payment journal** page, create a vendor prepayment that has a facture, and then select **Lines**.</span></span>
4. <span data-ttu-id="1cdbb-207">На странице **Платежи поставщикам** в столбце **Вид действия** выберите **Комиссионер**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-207">On the **Vendor payments** page, in the **Kind of activity** column, select **Commission agent**.</span></span>

    ![Страница платежей поставщикам](media/34_Vendor_payments.jpg)

5. <span data-ttu-id="1cdbb-209">Создайте заказ на покупку, затем накладную.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-209">Create a purchase order and an invoice.</span></span>
6. <span data-ttu-id="1cdbb-210">Создайте заказ на продажу и счет-фактуру.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-210">Create a sales order and a facture.</span></span>
7. <span data-ttu-id="1cdbb-211">Создайте отчет для доверителя и обновите строки в отгрузках.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-211">Create a report for the principal, and update the lines on shipments.</span></span>
8. <span data-ttu-id="1cdbb-212">В нижней части страницы **Отчет для доверителя** на вкладке **Предоплаты** в поле **Ваучер** выберите ваучер предоплаты клиента, чтобы включить эту предоплату в отчет для доверителя, который отвечает за уплату НДС.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-212">In the bottom part of the **Report for principal** page, on the **Prepayments** tab, in the **Voucher** field, select the customer prepayment voucher to include the prepayment on the report for the principal that is responsible for VAT prepayment.</span></span>

    ![Страница отчета для доверителя](media/35_Report_for_principal.jpg)

9. <span data-ttu-id="1cdbb-214">Выберите **Проводки** для просмотра распределенной суммы в поле **Сумма в валюте отчетности**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-214">Select **Transactions** to view the allocated amount in the **Amount in reporting currency** field.</span></span>

    ![Страница проводок по клиенту](media/36_Customer_transactions.jpg)

10. <span data-ttu-id="1cdbb-216">На странице **Отчет для доверителя** утвердите строки на вкладке **Обзор** и ваучеры на вкладке **Предоплаты**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-216">On the **Report for principal** page, approve lines on the **Overview** tab and vouchers on the **Prepayments** tab.</span></span>
11. <span data-ttu-id="1cdbb-217">Можно создать счет-фактуру и просмотреть счет или счет-фактуру доверителя или исходный счет или счет-фактуру.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-217">You can create a facture, and you can view the principal's invoice or facture, or the original invoice or facture.</span></span>

### <a name="print-a-report-for-a-principal"></a><span data-ttu-id="1cdbb-218">Печать отчета для доверителя</span><span class="sxs-lookup"><span data-stu-id="1cdbb-218">Print a report for a principal</span></span>

<span data-ttu-id="1cdbb-219">Напечатайте отчет для доверителя.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-219">Print a report for a principal.</span></span> <span data-ttu-id="1cdbb-220">Отчет для доверителя имеет два раздела: один для отгрузок, другой для предоплат.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-220">The report for the principal has two sections: one for shipments and one for prepayments.</span></span>

![Созданный отчет о продажах](media/37_Sales_report.jpg)


### <a name="create-a-prepayment-facture"></a><span data-ttu-id="1cdbb-222">Создание счета-фактуры на предоплату</span><span class="sxs-lookup"><span data-stu-id="1cdbb-222">Create a prepayment facture</span></span>

1. <span data-ttu-id="1cdbb-223">На странице **Отчет для доверителя** на вкладке **Предоплаты** установите флажок **Утвердить**, затем выберите **Создать счет-фактуру**, чтобы зарегистрировать счет-фактуру на предоплату для доверителя.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-223">On the **Report for principal** page, on the **Prepayments** tab, select the **Approve** check box, and then select **Create facture** to register a principal's facture on the prepayment.</span></span>
2. <span data-ttu-id="1cdbb-224">На странице **Создать счет-фактуру на предоплату** выберите **Выбрать**, чтобы открыть диалоговое окно **Выбрать предоплаты**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-224">On the **Create prepayment facture** page, select **Select** to open the **Select prepayments** dialog box.</span></span>
3. <span data-ttu-id="1cdbb-225">В полях **Начальная дата** и **Конечная дата** укажите период.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-225">In the **From date** and **End date** fields, specify the period.</span></span>
4. <span data-ttu-id="1cdbb-226">В поле **Счет поставщика** выберите счет поставщика.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-226">In the **Vendor account** field, select a vendor account.</span></span> <span data-ttu-id="1cdbb-227">Все источники счетов-фактур от выбранного поставщика включаются в диалоговое окно (утвержденные строки из отчета для доверителя и предоплаты из журналов платежей поставщикам).</span><span class="sxs-lookup"><span data-stu-id="1cdbb-227">All the sources for factures from the selected vendor are included in the dialog box (approved lines from the report for the principal and prepayments from vendor payment journals).</span></span>

  > [!NOTE]
  > <span data-ttu-id="1cdbb-228">Если поле **Счет поставщика** оставлено пустым, для обработки будут выбраны все предоплаты.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-228">If you leave the **Vendor account** field blank, all prepayments will be selected for processing.</span></span>

5. <span data-ttu-id="1cdbb-229">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-229">Select **OK**.</span></span>

    ![Диалоговое окно выбора предоплат](media/38_Select_prepayments.jpg)

6. <span data-ttu-id="1cdbb-231">На странице **Создать счет-фактуру на предоплату** используйте флажок **Отметить** для выбора соответствующей предоплаты.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-231">On the **Create prepayment facture** page, use the **Marked** check box to select the relevant prepayment.</span></span>
7. <span data-ttu-id="1cdbb-232">Укажите дату регистрации и счета-фактуры, затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-232">Specify the date of the registration and facture, and then select **Create**.</span></span>

    ![Страница "Создание счета-фактуры на предоплату"](media/39_Create_prepayment_facture.jpg)

8. <span data-ttu-id="1cdbb-234">На странице **Отчет для доверителя** на вкладке **Предоплаты** выберите **Доверитель \> Счет-фактура**, чтобы просмотреть зарегистрированный счет-фактуру доверителя для предоплаты.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-234">On the **Report for principal** page, on the **Prepayments** tab, select **Principal \> Facture** to view the registered principal's facture for prepayment.</span></span>

    ![Страница журнала счетов-фактур](media/40_Facture_journal.jpg)
    
9. <span data-ttu-id="1cdbb-236">Выберите **Печать** \> **Оригинал** для печати исходного счета-фактуры или выберите **Печать** \> **Копия**, чтобы напечатать копию счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-236">Select **Print** \> **Original** to print the original facture, or select **Print** \> **Copy** to print the facture copy.</span></span>

    ![Отчет о созданном счете-фактуре](media/41_Invoice-facture.jpg)


### <a name="create-a-facture-accounting-journal"></a><span data-ttu-id="1cdbb-238">Создание журнала учета счетов-фактур</span><span class="sxs-lookup"><span data-stu-id="1cdbb-238">Create a facture accounting journal</span></span>

<span data-ttu-id="1cdbb-239">Утвержденные строки можно зарегистрировать на странице **Журнал учета счетов-фактур** и напечатать журнал учета счетов-фактур.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-239">You can register approved lines on the **Facture accounting journal** page and print a facture accounting journal.</span></span>

## <a name="review-the-owner-that-is-assigned-to-an-agreement"></a><span data-ttu-id="1cdbb-240">Просмотр сведений о владельце, назначенном договору</span><span class="sxs-lookup"><span data-stu-id="1cdbb-240">Review the owner that is assigned to an agreement</span></span>

1. <span data-ttu-id="1cdbb-241">Выберите **Расчеты с поставщиками \> Заказы на покупку \> Договоры покупки** или **Закупки и источники \> Договоры покупки \> Договоры покупки**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-241">Go to **Accounts payable \> Purchase orders \> Purchase agreements** or **Procurement and sourcing \> Purchase agreements \> Purchase agreements**.</span></span>
2. <span data-ttu-id="1cdbb-242">Выберите соглашение, затем в области действий на вкладке **Договор покупки** в группе **Настройка** выберите **Владельцы запасов**, чтобы просмотреть владельца, назначенного данному договору.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-242">Select the agreement, and then, on the Action Pane, on the **Purchase agreement** tab, in the **Setup** group, select **Inventory owners** to review the owner that is assigned to the agreement.</span></span>
3. <span data-ttu-id="1cdbb-243">Выберите **Проводки** для просмотра проводок по запасам, связанных с владельцем запасов.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-243">Select **Transactions** to review the inventory transactions that are associated with the inventory owner.</span></span>

    ![Страница проводок по запасам](media/42_Inventory_transactions.png)

4. <span data-ttu-id="1cdbb-245">Выберите **Сведения о транзакции**.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-245">Select **Transaction details**.</span></span> <span data-ttu-id="1cdbb-246">На экспресс-вкладке **Складские аналитики** можно просмотреть владельца и профиль запасов.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-246">On the **Inventory dimensions** FastTab, you can see the owner and the inventory profile.</span></span>

    ![Страница "Сведения о транзакции"](media/43_Transaction_details.png)

<span data-ttu-id="1cdbb-248">Описанные здесь параметры позволяют отслеживать комиссионные товары по владельцу товаров в соответствии с договором.</span><span class="sxs-lookup"><span data-stu-id="1cdbb-248">The settings that are described here let you track the commission goods by the owner of the goods according to the agreement.</span></span>

<span data-ttu-id="1cdbb-249">Более подробную информацию см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="1cdbb-249">Find more details in the following topics:</span></span>

- [<span data-ttu-id="1cdbb-250">Проводки через посредников</span><span class="sxs-lookup"><span data-stu-id="1cdbb-250">Transactions through intermediary</span></span>](rus-transactions-through-intermediary.md) 
- [<span data-ttu-id="1cdbb-251">Покупки по комиссии</span><span class="sxs-lookup"><span data-stu-id="1cdbb-251">Purchases on commission</span></span>](rus-purchases-on-commission.md)
