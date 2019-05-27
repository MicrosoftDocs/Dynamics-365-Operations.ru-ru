---
title: Регистрация прихода возврата
description: Зарегистрировать приход возврата можно с помощью формы "Обзор прибытия" или формы "Регистрация".
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2be628d312e623e8ea6d92eb5edce12334190d9e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571083"
---
# <a name="register-the-receipt-of-returned-items"></a><span data-ttu-id="b4ec2-103">Регистрация прихода возврата</span><span class="sxs-lookup"><span data-stu-id="b4ec2-103">Register the receipt of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b4ec2-104">Имеется два метода регистрации поступления возвращенных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-104">There are two methods for registering the receipt of returned items.</span></span> <span data-ttu-id="b4ec2-105">Первый метод — это процесс приемки на склад, в котором используется форма **Обзор прибытия**.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-105">The first method is a warehouse receiving process that uses the **Arrival overview** form.</span></span> <span data-ttu-id="b4ec2-106">Во втором методе используется форма **Регистрация**.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-106">The second uses the **Registration** form.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a><span data-ttu-id="b4ec2-107">Регистрация прихода возвращенных номенклатур на форме "Обзор прибытия"</span><span class="sxs-lookup"><span data-stu-id="b4ec2-107">Register the receipt of returned items in the Arrival overview form</span></span>

<span data-ttu-id="b4ec2-108">Форма **Обзор прибытия** может использоваться для идентификации возврата поставки по ее номеру разрешения на возврат материалов.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-108">You can use the **Arrival overview** form to identify a return shipment by its Return Material Authorization (RMA) number.</span></span> <span data-ttu-id="b4ec2-109">Если на вкладке **Настройка** определено имя журнала и существуют строки журнала, соответствующие строкам, выбранным в форме **Обзор прибытия**, то по щелчку **Начать прибытие** создается новый заголовок журнала.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-109">If a journal name is defined on the **Setup** tab, and journal lines that correspond to the lines selected on the **Arrival overview** form exist, a new journal header is created when you click **Start arrival**.</span></span>

1.  <span data-ttu-id="b4ec2-110">Щелкните **Управление запасами** \> **Периодические операции** \> **Обзор прибытия**.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-110">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="b4ec2-111">В поле **Имя настройки** выберите **Заказ на возврат**, а затем щелкните **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-111">In the **Setup name** field, select **Return order**, and then click **Update**.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="b4ec2-112">Чтобы сузить диапазон результатов поиска, можно использовать поля <STRONG>Диапазон</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-112">You can use the <STRONG>Range</STRONG> fields to narrow the search results.</span></span> <span data-ttu-id="b4ec2-113">Можно ввести или выбрать RMA-номер в поле <STRONG>RMA-номер</STRONG>, чтобы получить точный результат.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-113">You can type or select the RMA number in the <STRONG>RMA number</STRONG> field for an exact result.</span></span> <span data-ttu-id="b4ec2-114">Чтобы определить и сохранить набор фильтров, ограничивающих входящие прибытия, которые будут отображаться на экране, откройте вкладку <STRONG>Настройка</STRONG>. Доступные фильтры включают типы, склады и доки.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-114">To define and save a set of filters that will restrict which incoming arrivals are displayed, click the <STRONG>Setup</STRONG> tab. The available filters include types, warehouses, and docks.</span></span></P>

    

    > [!WARNING]
    > <P><span data-ttu-id="b4ec2-115">В форме <STRONG>Обзор прибытия</STRONG> заказы на возврат не могут смешиваться с другими типами прибытий.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-115">Return orders cannot be mixed with other arrival types in the <STRONG>Arrival overview</STRONG> form.</span></span> <span data-ttu-id="b4ec2-116">Поэтому ссылкой всегда является заказ на продажу, но никакой идентификатор заказа на продажу не указывается в заголовке журнала.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-116">Therefore, the reference will always be sales order, but no sales order ID will be specified on the journal header.</span></span></P>



3.  <span data-ttu-id="b4ec2-117">В сетке **Поступления** найдите строку, которая соответствует возвращаемой номенклатуре, а затем установите флажок в столбце **Выбрать для прибытия**.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-117">In the **Receipts** grid, locate the line that matches the item being returned, and then select the check box in the **Select for arrival** column.</span></span>

4.  <span data-ttu-id="b4ec2-118">Чтобы исключить определенные строки из прихода возврата, например номенклатуры из исходного заказа, которые не были включены в отгрузку возврата, снимите связанные флажки **Выбрать для прибытия** в таблице **Строки** в нижней части формы.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-118">To exclude certain lines from the return receipt, such as items from the original order that were not included in the return shipment, clear the associated **Select for arrival** check boxes in the **Lines** table in the lower part of the form.</span></span>

5.  <span data-ttu-id="b4ec2-119">Нажмите кнопку **Начать прибытие**, чтобы создать журнал прибытий.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-119">Click the **Start arrival** button to create an arrival journal.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="b4ec2-120">Можно выбрать несколько заказов на возврат и включить их все в один процесс прибытия.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-120">You can select multiple return orders and include them all in a single arrival process.</span></span> <span data-ttu-id="b4ec2-121">Каждая строка заказа на возврат будет скопирована в соответствующую строку журнала прибытия номенклатур.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-121">Each return order line will be copied into a corresponding item arrival journal line.</span></span></P>

    

    > [!NOTE]
    > <P><span data-ttu-id="b4ec2-122">Журнал прибытий можно также создать вручную, пользуясь формой <STRONG>Прибытие номенклатуры</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-122">You can also manually create an arrival journal by using the <STRONG>Item arrival</STRONG> form.</span></span> 



6.  <span data-ttu-id="b4ec2-123">Щелкните **Управление запасами** \> **Журналы** \> **Прибытие номенклатуры** \> **Прибытие номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-123">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>

7.  <span data-ttu-id="b4ec2-124">Выберите журнал прибытий, который только что создали, а затем щелкните **Строки**, чтобы открыть форму **Строки журнала, местоположения**.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-124">Select the arrival journal that you just created and then click **Lines** to open the **Journal lines, locations** form.</span></span>

8.  <span data-ttu-id="b4ec2-125">На вкладке **Общие** измените число в поле **Количество**, если это необходимо, а затем назначьте код расстановки в поле **Код расстановки**.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-125">On the **General** tab, adjust the number in the **Quantity** field, if it is required, and then assign a disposition code in the **Disposition code** field.</span></span>
    
    <span data-ttu-id="b4ec2-126">Либо можно установить флажок **Управление карантином**, чтобы возвращенные номенклатуры отправлялись через процесс проверки в контексте карантинного заказа.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-126">Alternatively, you can select the **Quarantine management** check box to have the returned items sent through an inspection process in the context of a quarantine order.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="b4ec2-127">При отправке возвращенных номенклатур через карантин невозможно указать код расстановки.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-127">If you send the returned items through quarantine, you cannot specify a disposition code.</span></span></P>



9.  <span data-ttu-id="b4ec2-128">Нажмите кнопку **Проверить**.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-128">Click the **Validate** button.</span></span>

10. <span data-ttu-id="b4ec2-129">Если ошибок в процессе проверки нет, нажмите кнопку **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-129">If there are no errors in the validation process, click **Post**.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a><span data-ttu-id="b4ec2-130">Регистрация прихода возвращенных номенклатур на форме "Регистрация"</span><span class="sxs-lookup"><span data-stu-id="b4ec2-130">Register the receipt of returned items in the Registration form</span></span>

<span data-ttu-id="b4ec2-131">Для регистрации прибытия возвращенных номенклатур вместо формы **Обзор прибытия** можно использовать форму **Регистрация**.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-131">As an alternative to using the **Arrival overview** form, you can use the **Registration** form to register the arrival of returned items.</span></span>

1.  <span data-ttu-id="b4ec2-132">Выберите **Продажи и маркетинг** \> **Общее** \> **Заказы на возврат** \> **Все заказы на возврат**.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-132">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span> <span data-ttu-id="b4ec2-133">Создайте новый заказ на возврат или откройте заказ на возврат из списка.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-133">Create a new return order or open the return order from the list.</span></span> <span data-ttu-id="b4ec2-134">На экспресс-вкладке **Строки** выберите строку заказа на возврат.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-134">On the **Lines** FastTab, select the return order line.</span></span> <span data-ttu-id="b4ec2-135">Щелкните **Обновить строку**, а затем щелкните **Регистрация**.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-135">Click **Update line**, and then click **Registration**.</span></span>

2.  <span data-ttu-id="b4ec2-136">Назначьте код расстановки в поле **Код расстановки**, а затем щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-136">Assign a disposition code in the **Disposition code** field, and then click **OK**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="b4ec2-137">С помощью формы <STRONG>Регистрация</STRONG> невозможно отправить номенклатуру на проверку в качестве карантинного заказа.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-137">It is not possible to send the item for inspection as a quarantine order using the <STRONG>Registration</STRONG> form.</span></span></P>



3.  <span data-ttu-id="b4ec2-138">В сетке **Проводки** выберите проводку, которую необходимо зарегистрировать.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-138">In the **Transactions** grid, select the transaction to be registered.</span></span>

4.  <span data-ttu-id="b4ec2-139">В сетке **К регистрации сейчас** щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-139">In the **Register now** grid, click **Add**.</span></span> <span data-ttu-id="b4ec2-140">Повторяйте предыдущие два шага до тех пор, пока все возвращенные номенклатуры не появятся в сетке **К регистрации сейчас**.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-140">Repeat the previous two steps until all of the returned items appear in the **Register now** grid.</span></span>

5.  <span data-ttu-id="b4ec2-141">Щелкните **Разнести все**.</span><span class="sxs-lookup"><span data-stu-id="b4ec2-141">Click **Post all**.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4ec2-142">См. также</span><span class="sxs-lookup"><span data-stu-id="b4ec2-142">See also</span></span>

<span data-ttu-id="b4ec2-143">[Обзор поступлений (форма)](https://technet.microsoft.com/en-us/library/hh227654\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="b4ec2-143">[Arrival overview (form)](https://technet.microsoft.com/en-us/library/hh227654\(v=ax.60\))</span></span>

  


