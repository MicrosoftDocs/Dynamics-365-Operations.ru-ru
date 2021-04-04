---
title: Пример обработки писем-напоминаний
description: В этом разделе описывается пример создания, печати и разноски писем-напоминаний.
author: JodiChristiansen
manager: AnnBe
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: df4252513f9e3a02632561b4e465c98edc888ea7
ms.sourcegitcommit: 4ecc1bf82fbb04882d7ef5e1994ef3c07ef953dc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "5558319"
---
# <a name="process-collection-letters-example"></a><span data-ttu-id="83193-103">Пример обработки писем-напоминаний</span><span class="sxs-lookup"><span data-stu-id="83193-103">Process collection letters example</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="83193-104">В этом разделе описывается пример создания, печати и разноски писем-напоминаний.</span><span class="sxs-lookup"><span data-stu-id="83193-104">This topic goes through an example that shows the process of creating, printing, and posting collection letters.</span></span> <span data-ttu-id="83193-105">Пример основан на параметре **Игнорировать платежи и кредит-ноты при расчете кода письма-напоминания** в "Кредит и сбор задолженностей".</span><span class="sxs-lookup"><span data-stu-id="83193-105">The example is based on the **Ignore payments and credit memos when calculating collection letter code** option in Credit and collections.</span></span> <span data-ttu-id="83193-106">В нем используются данные демонстрационной компании USMF и нового клиента, US-045.</span><span class="sxs-lookup"><span data-stu-id="83193-106">It uses data in the USMF demo company and a new customer, US-045.</span></span>

<span data-ttu-id="83193-107">Чтобы начать, перейдите на **Расчеты с клиентами \> Клиенты \> Все клиенты**, выберите **создать**, а затем введите требуемые сведения для создания клиента US-045.</span><span class="sxs-lookup"><span data-stu-id="83193-107">To begin, go to **Accounts receivable \> Customers \> All customers**, select **New**, and then enter the required information to create customer US-045.</span></span>

<span data-ttu-id="83193-108">Когда вы закончите, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="83193-108">When you've finished, follow these steps.</span></span>

1. <span data-ttu-id="83193-109">Перейдите в раздел **Кредит и сбор задолженностей \> Письмо-напоминание \> Настройка последовательности писем-напоминаний**, и настройте последовательность писем-напоминаний, как показано в следующей таблице, которая назначена профилю разноски клиента.</span><span class="sxs-lookup"><span data-stu-id="83193-109">Go to **Credit and collections \> Collection letter \> Setup collection letter sequence**, and set up the collection letter sequence as shown in the following table that is assigned to the customer posting profile.</span></span>

|     <span data-ttu-id="83193-110">Код письма-напоминания</span><span class="sxs-lookup"><span data-stu-id="83193-110">Collection   letter code</span></span>      |     <span data-ttu-id="83193-111">описание</span><span class="sxs-lookup"><span data-stu-id="83193-111">Description</span></span>                           |     <span data-ttu-id="83193-112">Валютное</span><span class="sxs-lookup"><span data-stu-id="83193-112">Currency</span></span>      |     <span data-ttu-id="83193-113">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="83193-113">Main   account</span></span>        |     <span data-ttu-id="83193-114">Сбор в валюте</span><span class="sxs-lookup"><span data-stu-id="83193-114">Fee   in currency</span></span>     |     <span data-ttu-id="83193-115">Минимум сверх</span><span class="sxs-lookup"><span data-stu-id="83193-115">Minimum   over</span></span>        |     <span data-ttu-id="83193-116">Дней блокировки</span><span class="sxs-lookup"><span data-stu-id="83193-116">Days   Block</span></span>      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     <span data-ttu-id="83193-117">Письмо-напоминание 1</span><span class="sxs-lookup"><span data-stu-id="83193-117">Collection   letter 1</span></span>         |     <span data-ttu-id="83193-118">Второе уведомление с сбором</span><span class="sxs-lookup"><span data-stu-id="83193-118">Second   notification with fee</span></span>        |     <span data-ttu-id="83193-119">USD</span><span class="sxs-lookup"><span data-stu-id="83193-119">USD</span></span>           |                           |     <span data-ttu-id="83193-120">0.00</span><span class="sxs-lookup"><span data-stu-id="83193-120">0.00</span></span>                  |     <span data-ttu-id="83193-121">0.00</span><span class="sxs-lookup"><span data-stu-id="83193-121">0.00</span></span>                  |     <span data-ttu-id="83193-122">2</span><span class="sxs-lookup"><span data-stu-id="83193-122">2</span></span>                 |
|     <span data-ttu-id="83193-123">Письмо-напоминание 2</span><span class="sxs-lookup"><span data-stu-id="83193-123">Collection   letter 2</span></span>         |     <span data-ttu-id="83193-124">Второе уведомление с сбором</span><span class="sxs-lookup"><span data-stu-id="83193-124">Second   notification with fee</span></span>        |     <span data-ttu-id="83193-125">USC</span><span class="sxs-lookup"><span data-stu-id="83193-125">USC</span></span>           |     <span data-ttu-id="83193-126">403150</span><span class="sxs-lookup"><span data-stu-id="83193-126">403150</span></span>                |     <span data-ttu-id="83193-127">20.00</span><span class="sxs-lookup"><span data-stu-id="83193-127">20.00</span></span>                 |     <span data-ttu-id="83193-128">10.00</span><span class="sxs-lookup"><span data-stu-id="83193-128">10.00</span></span>                 |     <span data-ttu-id="83193-129">3</span><span class="sxs-lookup"><span data-stu-id="83193-129">3</span></span>                 |
|     <span data-ttu-id="83193-130">Сбор</span><span class="sxs-lookup"><span data-stu-id="83193-130">Collection</span></span>                    |     <span data-ttu-id="83193-131">Окончательное уведомление с сбором</span><span class="sxs-lookup"><span data-stu-id="83193-131">Final   notification with fee</span></span>         |     <span data-ttu-id="83193-132">USD</span><span class="sxs-lookup"><span data-stu-id="83193-132">USD</span></span>           |     <span data-ttu-id="83193-133">403150</span><span class="sxs-lookup"><span data-stu-id="83193-133">403150</span></span>                |     <span data-ttu-id="83193-134">50.00</span><span class="sxs-lookup"><span data-stu-id="83193-134">50.00</span></span>                 |     <span data-ttu-id="83193-135">100.00</span><span class="sxs-lookup"><span data-stu-id="83193-135">100.00</span></span>                |     <span data-ttu-id="83193-136">15</span><span class="sxs-lookup"><span data-stu-id="83193-136">15</span></span>                |

<span data-ttu-id="83193-137">На следующем рисунке показана информация, которая указана в таблице в том виде, в котором они будут отображаться на странице **письма-напоминания**.</span><span class="sxs-lookup"><span data-stu-id="83193-137">The following illustration shows the information that's in the table as it would appear on the **Collection letters** page.</span></span> 

<span data-ttu-id="83193-138">[![Настройка последовательности писем-напоминаний](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span><span class="sxs-lookup"><span data-stu-id="83193-138">[![Setting up a collection letter sequence](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span></span>

 <span data-ttu-id="83193-139">Теперь необходимо задать два параметра, которые необходимы для этого примера.</span><span class="sxs-lookup"><span data-stu-id="83193-139">You must now set the two parameters that are required for this example.</span></span>

2. <span data-ttu-id="83193-140">Выберите **Кредит и сборы \> Настройка \> Параметры модуля расчетов с клиентами** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="83193-140">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and follow these steps:</span></span>

    1. <span data-ttu-id="83193-141">На вкладке **Сбор задолженностей** настройте параметр **Игнорировать платежи и кредит-ноты при расчете кода письма-напоминания** на значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="83193-141">On the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **Yes**.</span></span>
    2. <span data-ttu-id="83193-142">Убедитесь, что в поле **Создать письмо-напоминание** для поля выбрано значение **клиент**.</span><span class="sxs-lookup"><span data-stu-id="83193-142">Make sure that the **Create collection letter per** field is set to **Customer**.</span></span>

    <span data-ttu-id="83193-143">[![Настройка параметров расчетов с клиентами для Кредит и сбор задолженностей](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span><span class="sxs-lookup"><span data-stu-id="83193-143">[![Setting Accounts receivable parameters for Credit collections](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span></span>

3. <span data-ttu-id="83193-144">Перейти к **Расчеты с клиентами \> Накладные \> Все накладные с произвольным текстом**, выберите **создать**, а затем выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="83193-144">Go to **Accounts receivable \> Invoices \> All free text invoices**, select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="83193-145">В поле **Счет клиента** выберите **US-045**.</span><span class="sxs-lookup"><span data-stu-id="83193-145">In the **Customer account** field select **US-045**.</span></span>
    2. <span data-ttu-id="83193-146">В поле **Дата накладной** введите **15/01/2021**.</span><span class="sxs-lookup"><span data-stu-id="83193-146">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="83193-147">В поле **Дата выполнения** введите **16/01/2021**.</span><span class="sxs-lookup"><span data-stu-id="83193-147">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="83193-148">На экспресс-вкладке **строки накладной** в поле **Счет ГК** введите **401100**.</span><span class="sxs-lookup"><span data-stu-id="83193-148">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="83193-149">В поле **Цена за единицу** введите **500.00**.</span><span class="sxs-lookup"><span data-stu-id="83193-149">In the **Unit price** field, enter **500.00**.</span></span>
    6. <span data-ttu-id="83193-150">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="83193-150">Select **Post**.</span></span>

    <span data-ttu-id="83193-151">Теперь необходимо ввести две кредит-ноты для клиента.</span><span class="sxs-lookup"><span data-stu-id="83193-151">You must now enter two credit notes for the customer.</span></span>

4. <span data-ttu-id="83193-152">Выберите **Создать**, а затем выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="83193-152">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="83193-153">В поле **Счет клиента** выберите **US-045**.</span><span class="sxs-lookup"><span data-stu-id="83193-153">In the **Customer account** field, select **US-045**.</span></span>
    2. <span data-ttu-id="83193-154">В поле **Дата накладной** введите **15/01/2021**.</span><span class="sxs-lookup"><span data-stu-id="83193-154">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="83193-155">В поле **Дата выполнения** введите **16/01/2021**.</span><span class="sxs-lookup"><span data-stu-id="83193-155">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="83193-156">На экспресс-вкладке **строки накладной** в поле **Счет ГК** введите **401100**.</span><span class="sxs-lookup"><span data-stu-id="83193-156">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="83193-157">В поле **Цена за единицу** введите **-100,00**.</span><span class="sxs-lookup"><span data-stu-id="83193-157">In the **Unit price** field, enter **-100.00**.</span></span>
    6. <span data-ttu-id="83193-158">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="83193-158">Select **Post**.</span></span>

5. <span data-ttu-id="83193-159">Повторите шаг 4, но введите **-200,00** в поле **Цена за единицу**.</span><span class="sxs-lookup"><span data-stu-id="83193-159">Repeat step 4, but enter **-200.00** in the **Unit price** field.</span></span>
6. <span data-ttu-id="83193-160">Перейдите на **Расчеты с клиентами \> Клиенты \> Все клиенты** и выберите клиента **US-045**.</span><span class="sxs-lookup"><span data-stu-id="83193-160">Go to **Accounts receivable \> Customers \> All customers**, and select customer **US-045**.</span></span> <span data-ttu-id="83193-161">Затем в области действий выберите **Проводки \> Проводки** для просмотра ранее разнесенных проводок клиента.</span><span class="sxs-lookup"><span data-stu-id="83193-161">Then, on the Action Pane, select **Transactions \> Transactions** to review the customer transactions that you posted earlier.</span></span>

    <span data-ttu-id="83193-162">[![Просмотр разнесенных проводок клиента](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span><span class="sxs-lookup"><span data-stu-id="83193-162">[![Reviewing the posted customer transactions](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span></span>

    <span data-ttu-id="83193-163">Вы должны создать письма-напоминания для клиента US-045.</span><span class="sxs-lookup"><span data-stu-id="83193-163">You must now create collection letters for customer US-045.</span></span>

7. <span data-ttu-id="83193-164">Выберите **Кредит и сбор задолженностей \> Письмо-напоминание \> Создание писем-напоминаний** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="83193-164">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="83193-165">Установите для параметров **накладной** и **кредит-ноты** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="83193-165">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="83193-166">По умолчанию в поле **письма-напоминания** должно быть установлено значение **Инкассация по каждому заказчику**.</span><span class="sxs-lookup"><span data-stu-id="83193-166">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="83193-167">В поле **Дата письма-напоминания** введите **19/01/2021**.</span><span class="sxs-lookup"><span data-stu-id="83193-167">In the **Collection letter date** field, enter **1/19/2021**.</span></span>
    3. <span data-ttu-id="83193-168">На экспресс-вкладке **Включаемые записи** выберите **фильтр**, а затем в поле **счет клиента** добавьте клиента **US-045**.</span><span class="sxs-lookup"><span data-stu-id="83193-168">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="83193-169">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="83193-169">Select **OK**.</span></span>
    5. <span data-ttu-id="83193-170">Выберите **ОК**, чтобы создать письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="83193-170">Select **OK** to create collection letters.</span></span>

8. <span data-ttu-id="83193-171">Выберите **Кредит и сбор задолженностей \> Письмо-напоминание \> Просмотр и обработка писем-напоминаний** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="83193-171">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="83193-172">Обратите внимание, что код письма-напоминания в строках заголовка и проводки представляет собой **письмо-напоминание 1**, потому что это письмо-напоминание является первым в последовательности.</span><span class="sxs-lookup"><span data-stu-id="83193-172">Notice that the collection letter code on both the header and the transaction lines is **Collection letter 1**, because this collection letter is the first collection letter in the sequence.</span></span> <span data-ttu-id="83193-173">(Для просмотра строк проводки, возможно, придется выбрать экспресс-вкладка **Проводки**).</span><span class="sxs-lookup"><span data-stu-id="83193-173">(To view the transaction lines, you might have to select the **Transactions** FastTab.)</span></span>

   <span data-ttu-id="83193-174">[![Проверка того, что в заголовке и строках отображается один и тот же код письма-напоминания](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span><span class="sxs-lookup"><span data-stu-id="83193-174">[![Verifying that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span></span>

    2. <span data-ttu-id="83193-175">На панели операций выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="83193-175">On the Action Pane, select **Post**.</span></span>
    3. <span data-ttu-id="83193-176">В поле **Дата разноски** введите **19/01/2021**.</span><span class="sxs-lookup"><span data-stu-id="83193-176">In the **Posting date** field, enter **1/19/2021**.</span></span>

    <span data-ttu-id="83193-177">Вы должны снова создать письма-напоминания для клиента US-045.</span><span class="sxs-lookup"><span data-stu-id="83193-177">You must now create collection letters again for customer US-045.</span></span>

9. <span data-ttu-id="83193-178">Выберите **Кредит и сбор задолженностей \> Письмо-напоминание \> Создание писем-напоминаний** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="83193-178">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="83193-179">Установите для параметров **накладной** и **кредит-ноты** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="83193-179">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="83193-180">По умолчанию в поле **письма-напоминания** должно быть установлено значение **Инкассация по каждому заказчику**.</span><span class="sxs-lookup"><span data-stu-id="83193-180">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="83193-181">В поле **Дата письма-напоминания** введите **23/01/2021**.</span><span class="sxs-lookup"><span data-stu-id="83193-181">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="83193-182">На экспресс-вкладке **Включаемые записи** выберите **фильтр**, а затем в поле **счет клиента** добавьте клиента **US-045**.</span><span class="sxs-lookup"><span data-stu-id="83193-182">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="83193-183">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="83193-183">Select **OK**.</span></span>
    5. <span data-ttu-id="83193-184">Выберите **ОК**, чтобы создать письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="83193-184">Select **OK** to create collection letters.</span></span>

10. <span data-ttu-id="83193-185">Выберите **Кредит и сбор задолженностей \> Письмо-напоминание \> Просмотр и обработка писем-напоминаний** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="83193-185">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="83193-186">Обратите внимание, что кодом письма-напоминания в заголовке является **письмо-напоминание 1**.</span><span class="sxs-lookup"><span data-stu-id="83193-186">Notice that the collection letter code on the header is **Collection letter 1**.</span></span> <span data-ttu-id="83193-187">Однако кодом в строках проводки является **письмо-напоминание 2**.</span><span class="sxs-lookup"><span data-stu-id="83193-187">However, the code on the transaction lines is **Collection letter 2**.</span></span>

   <span data-ttu-id="83193-188">[![Проверяет наличие разных кодов письма-напоминания в заголовке и строках](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span><span class="sxs-lookup"><span data-stu-id="83193-188">[![Verifies that different collection letter codes appear on the header and the lines](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span></span>

  <span data-ttu-id="83193-189">Коды отличаются, потому что параметр **Игнорировать платежи и кредит-ноты при расчете кода письма-напоминания** установлен на значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="83193-189">The codes differ because the **Ignore payments and credit memos when calculating collection letter code** option is to **Yes**.</span></span>

  2. <span data-ttu-id="83193-190">Не разносите это письмо-напоминание.</span><span class="sxs-lookup"><span data-stu-id="83193-190">Don't post this collection letter.</span></span>

11. <span data-ttu-id="83193-191">Перейдите в раздел **Кредит и сбор задолженностей \> Настройка \> Параметры модуля расчетов с клиентами**, а затем на вкладке **Сбор задолженностей** установите флажок **Игнорировать платежи и кредит-ноты при расчете кода письма-напоминания** на значение **нет**.</span><span class="sxs-lookup"><span data-stu-id="83193-191">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and then, on the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **No**.</span></span>

    <span data-ttu-id="83193-192">[![Установка для параметра "Игнорировать платежи и кредит-ноты при расчете кода письма-напоминания" значение "Нет"](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span><span class="sxs-lookup"><span data-stu-id="83193-192">[![Setting the Ignore payments and credit memos when calculating collection letter code option to No](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span></span>

    <span data-ttu-id="83193-193">Вы должны снова создать письма-напоминания для клиента US-045.</span><span class="sxs-lookup"><span data-stu-id="83193-193">You must now create collection letters again for customer US-045.</span></span>

12. <span data-ttu-id="83193-194">Выберите **Кредит и сбор задолженностей \> Письмо-напоминание \> Создание писем-напоминаний** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="83193-194">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="83193-195">Установите для параметров **накладной** и **кредит-ноты** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="83193-195">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="83193-196">По умолчанию в поле **письма-напоминания** должно быть установлено значение **Инкассация по каждому заказчику**.</span><span class="sxs-lookup"><span data-stu-id="83193-196">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="83193-197">В поле **Дата письма-напоминания** введите **23/01/2021**.</span><span class="sxs-lookup"><span data-stu-id="83193-197">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="83193-198">На экспресс-вкладке **Включаемые записи** выберите **фильтр**, а затем в поле **счет клиента** добавьте клиента **US-045**.</span><span class="sxs-lookup"><span data-stu-id="83193-198">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="83193-199">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="83193-199">Select **OK**.</span></span>
    5. <span data-ttu-id="83193-200">Выберите **ОК**, чтобы создать письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="83193-200">Select **OK** to create collection letters.</span></span>

13. <span data-ttu-id="83193-201">Перейдите в раздел **Кредит и сбор задолженностей \> Письмо-напоминание \> Просмотр и обработка писем-напоминаний** и обратите внимание, что код письма-напоминания в строках заголовка и проводки представляет собой **письмо-напоминание 2**.</span><span class="sxs-lookup"><span data-stu-id="83193-201">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and notice that the collection letter code on both the header and the transaction lines is **Collection letter 2**.</span></span>

    <span data-ttu-id="83193-202">[![Еще раз показывая, что в заголовке и строках отображается один и тот же код письма-напоминания](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span><span class="sxs-lookup"><span data-stu-id="83193-202">[![Showing again that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span></span>

    <span data-ttu-id="83193-203">Один и тот же код появляется в обоих местах, потому что параметр **Игнорировать платежи и кредит-ноты при расчете кода письма-напоминания** теперь установлен на значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="83193-203">The same code appears in both places because the **Ignore payments and credit memos when calculating collection letter code** option is now set to **No**.</span></span>
