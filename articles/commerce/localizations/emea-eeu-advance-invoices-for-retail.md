---
title: Авансовые счета для Commerce для Восточной Европы
description: В этом разделе объясняется, как настроить авансовые уведомления для Commerce для Восточной Европы.
author: epopov
manager: annbe
ms.date: 10/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: fc2af93880b634e6cec0015a2469fb8e4e56a7d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408517"
---
# <a name="advance-invoices-for-commerce-for-eastern-europe"></a><span data-ttu-id="4a334-103">Авансовые счета для Commerce для Восточной Европы</span><span class="sxs-lookup"><span data-stu-id="4a334-103">Advance invoices for Commerce for Eastern Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a334-104">Сведения в этом разделе применяется к локализации для Восточной Европы и относится к коммерческой сфере.</span><span class="sxs-lookup"><span data-stu-id="4a334-104">The information in this topic applies to the Eastern European localization and is specific to the commerce industry.</span></span>

<span data-ttu-id="4a334-105">Для Польши, Венгрии и Чешской Республики при получении предоплаты от клиента через POS эта предварительная оплата должна быть зарегистрирована для целей налогообложения, и необходимо создавать и печатать документ авансового счета, который включает сумму предоплаты.</span><span class="sxs-lookup"><span data-stu-id="4a334-105">For Poland, Hungary, and Czech Republic, when a prepayment is received from a customer via Point of Sale (POS), the prepayment must be registered for tax purposes, and it's required to generate and print an advance invoice document that includes the prepayment amount.</span></span> <span data-ttu-id="4a334-106">Кроме того, для Польши проводки по авансовым счетам должны разноситься в главной книге.</span><span class="sxs-lookup"><span data-stu-id="4a334-106">Additionally, for Poland, advance invoice transactions must be posted in the general ledger.</span></span>

<span data-ttu-id="4a334-107">При окончательной разноске накладной для заказа на продажу итоговый документ следует включать авансовый счет, и любые предварительные платежи необходимо указывать.</span><span class="sxs-lookup"><span data-stu-id="4a334-107">When the invoice for the sales order is finally posted, the final document should include the advance invoice, and any prepayments should be indicated.</span></span>

<span data-ttu-id="4a334-108">Если создавать заказы на продажу из модуля "Расчеты с клиентами", необходимо вручную создать авансовые счета, используя процедуру, описанную в разделе [Авансовые счета для Восточной Европы](https://docs.microsoft.com/dynamics365/unified-operations/financials/localizations/emea-advance-invoice).</span><span class="sxs-lookup"><span data-stu-id="4a334-108">If you generate sales orders from Accounts receivable, you must manually generate advance invoices by using the procedure in [Advance invoices for Eastern Europe](https://docs.microsoft.com/dynamics365/unified-operations/financials/localizations/emea-advance-invoice).</span></span> <span data-ttu-id="4a334-109">При создании заказов на продажу через POS-терминал система создает и разносит авансовые счета автоматически.</span><span class="sxs-lookup"><span data-stu-id="4a334-109">If you generate sales orders via POS, the system generates and posts the advance invoices for you.</span></span>

## <a name="supported-scenarios"></a><span data-ttu-id="4a334-110">Поддерживаемые сценарии</span><span class="sxs-lookup"><span data-stu-id="4a334-110">Supported scenarios</span></span>

<span data-ttu-id="4a334-111">Поддерживаются следующие сценарии:</span><span class="sxs-lookup"><span data-stu-id="4a334-111">The following scenarios are supported:</span></span>

- <span data-ttu-id="4a334-112">Создание и разноска авансового счета.</span><span class="sxs-lookup"><span data-stu-id="4a334-112">Create and post an advance invoice.</span></span>
- <span data-ttu-id="4a334-113">Изменение суммы депозита.</span><span class="sxs-lookup"><span data-stu-id="4a334-113">Modify a deposit amount.</span></span> <span data-ttu-id="4a334-114">Если клиент решает увеличить сумму депозит, формируется дополнительный авансовый счет.</span><span class="sxs-lookup"><span data-stu-id="4a334-114">If a customer decides to increase the amount of a deposit, an additional advance invoice is issued.</span></span> <span data-ttu-id="4a334-115">Для всех остальных изменений суммы депозита (например, если редактируется заказ клиента) создается кредит-нота для авансового счета, который был создана ранее, и новый авансовый счет формируется и разносится для исправленной суммы.</span><span class="sxs-lookup"><span data-stu-id="4a334-115">For all other changes to the deposit amount (for example, if a customer order is edited), a credit note is created for the advance invoice that was previously generated, and a new advance invoice is generated and posted for the corrected amount.</span></span>
- <span data-ttu-id="4a334-116">Отмена заказ на продажу, который был связан с авансовыми счетами.</span><span class="sxs-lookup"><span data-stu-id="4a334-116">Cancel a sales order that has linked advance invoices.</span></span> <span data-ttu-id="4a334-117">В этом случае для авансового счета создается кредит-нота.</span><span class="sxs-lookup"><span data-stu-id="4a334-117">In this case, a credit note is created for the advance invoice.</span></span>
- <span data-ttu-id="4a334-118">Разноска накладной заказа на продажу, которая была связана с авансовым счетом.</span><span class="sxs-lookup"><span data-stu-id="4a334-118">Post a sales order invoice that has linked advance invoices.</span></span> <span data-ttu-id="4a334-119">Авансовый счет, который был связан с заказом на продажу, сторнируется на сумму накладной на продажу.</span><span class="sxs-lookup"><span data-stu-id="4a334-119">The advance invoice that is linked to a sales order is reversed for the amount of the sales invoice.</span></span> <span data-ttu-id="4a334-120">Проводки авансового счета сопоставляются с проводками реверсирования авансового счета.</span><span class="sxs-lookup"><span data-stu-id="4a334-120">The advance invoice transactions are settled with advance invoice reversal transactions.</span></span>

## <a name="set-up-advance-invoices"></a><span data-ttu-id="4a334-121">Настройка авансовых счетов</span><span class="sxs-lookup"><span data-stu-id="4a334-121">Set up advance invoices</span></span>

### <a name="turn-on-the-functionality-for-creating-advance-invoices"></a><span data-ttu-id="4a334-122">Включение функции создания авансовых счетов</span><span class="sxs-lookup"><span data-stu-id="4a334-122">Turn on the functionality for creating advance invoices</span></span>

1. <span data-ttu-id="4a334-123">Перейдите в раздел **Retail и Commerce \> Настройка центрального офиса \> Параметры \> Параметры Commerce**.</span><span class="sxs-lookup"><span data-stu-id="4a334-123">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span>
2. <span data-ttu-id="4a334-124">На вкладке **Заказы клиентов** на экспресс-вкладке **Заказ** задайте для параметра **Создать авансовый счет для депозита** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="4a334-124">On the **Customer orders** tab, on the **Order** FastTab, set the **Create advance invoice for deposit** option to **Yes**.</span></span>

### <a name="define-the-parameters-for-posting-advance-invoices"></a><span data-ttu-id="4a334-125">Определение параметров для разноски авансовых счетов</span><span class="sxs-lookup"><span data-stu-id="4a334-125">Define the parameters for posting advance invoices</span></span>

1. <span data-ttu-id="4a334-126">Перейдите в раздел **Расчеты с клиентами \> Настройка \> Параметры модуля расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="4a334-126">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="4a334-127">На вкладке **Обновления** на экспресс-вкладке **Авансовый счет** задайте поля **Профиль разноски**, **Налоговая группа** и **Налоговая группа номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="4a334-127">On the **Updates** tab, on the **Advance invoice** FastTab, set the **Posting profile**, **Sales tax group**, and **Item sales tax group** fields.</span></span> <span data-ttu-id="4a334-128">Если эти поля задано правильно, авансовый счет будет разнесен.</span><span class="sxs-lookup"><span data-stu-id="4a334-128">If these fields are set correctly, the advance invoice will be posted.</span></span> <span data-ttu-id="4a334-129">Если эти поля не заданы, авансовые счета не разносятся.</span><span class="sxs-lookup"><span data-stu-id="4a334-129">If these fields aren't set, advance invoices won't be posted.</span></span>

### <a name="turn-off-posting-of-the-sales-tax-on-prepayment-journal-voucher"></a><span data-ttu-id="4a334-130">Выключение разноски налога на продажу по ваучеру журнала предоплат</span><span class="sxs-lookup"><span data-stu-id="4a334-130">Turn off posting of the Sales tax on prepayment journal voucher</span></span>

<span data-ttu-id="4a334-131">Налог по ваучеру журнала предоплат нельзя разносить, если включена разноска авансового счета.</span><span class="sxs-lookup"><span data-stu-id="4a334-131">The Sales tax on prepayment journal voucher must not be posted if advance invoice posting is turned on.</span></span> <span data-ttu-id="4a334-132">Чтобы убедиться, что это требование соблюдается, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4a334-132">To verify that this requirement is met, follow these steps.</span></span>

1. <span data-ttu-id="4a334-133">Перейдите в раздел **Расчеты с клиентами \> Настройка \> Параметры модуля расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="4a334-133">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="4a334-134">На вкладке **Главная книга и налог** на экспресс-вкладке **Платеж** убедитесь, что следующие поля пусты или для них задано значение **Нет**:</span><span class="sxs-lookup"><span data-stu-id="4a334-134">On the **Ledger and sales tax** tab, on the **Payment** FastTab, make sure that the following fields are blank or set to **No**:</span></span>

    - <span data-ttu-id="4a334-135">Налог по ваучеру журнала предоплат</span><span class="sxs-lookup"><span data-stu-id="4a334-135">Sales tax on prepayment journal voucher</span></span>
    - <span data-ttu-id="4a334-136">Профиль разноски с ваучером журнала предоплат</span><span class="sxs-lookup"><span data-stu-id="4a334-136">Posting profile with prepayment journal voucher</span></span>
    - <span data-ttu-id="4a334-137">Налоговая группа для предоплаты</span><span class="sxs-lookup"><span data-stu-id="4a334-137">Tax group for prepayment</span></span>
    - <span data-ttu-id="4a334-138">Налоговая группа номенклатур</span><span class="sxs-lookup"><span data-stu-id="4a334-138">Item Sales tax group</span></span>

## <a name="print-advance-invoices"></a><span data-ttu-id="4a334-139">Печать авансовых счетов</span><span class="sxs-lookup"><span data-stu-id="4a334-139">Print advance invoices</span></span>

<span data-ttu-id="4a334-140">Авансовые счета можно печатать с POS-терминала на принтере Microsoft Windows, который подключен к станции оборудования.</span><span class="sxs-lookup"><span data-stu-id="4a334-140">You can print advance invoices from POS on a Microsoft Windows printer that is connected to the hardware station.</span></span> <span data-ttu-id="4a334-141">Существует два варианта для печати авансового счета а с POS-терминала:</span><span class="sxs-lookup"><span data-stu-id="4a334-141">There are two options for printing an advance invoice from POS:</span></span>

- <span data-ttu-id="4a334-142">**Печать авансового счета после завершения проводки в POS.**</span><span class="sxs-lookup"><span data-stu-id="4a334-142">**Print an advance invoice after a transaction is concluded in POS.**</span></span> <span data-ttu-id="4a334-143">Этот вариант выполняется автоматически, если был создан авансовый счет и принтер Windows установлен правильно.</span><span class="sxs-lookup"><span data-stu-id="4a334-143">This option occurs automatically if an advance invoice was generated and a Windows printer was correctly set up.</span></span> <span data-ttu-id="4a334-144">В этом случае печатается только последний авансовый счет, связанный с заказом клиента.</span><span class="sxs-lookup"><span data-stu-id="4a334-144">In this case, only the last advance invoice that is linked to the customer order is printed.</span></span>
- <span data-ttu-id="4a334-145">**Повторная печать авансового счет из журнала проводок.**</span><span class="sxs-lookup"><span data-stu-id="4a334-145">**Reprint an advance invoice from the transaction journal.**</span></span> <span data-ttu-id="4a334-146">Выберите **Показать журнал**, чтобы открыть журнал проводок, найдите заказ клиента, затем выберите **Печать авансового счета**.</span><span class="sxs-lookup"><span data-stu-id="4a334-146">Select **Show journal** to open the transactions journal, find the customer order, and then select **Print Advance invoice**.</span></span> <span data-ttu-id="4a334-147">В этом случае печатаются все авансовые счета, связанные с заказом клиента.</span><span class="sxs-lookup"><span data-stu-id="4a334-147">In this case, all advance invoices that are linked to the customer order are printed.</span></span>

### <a name="set-up-a-windows-printer"></a><span data-ttu-id="4a334-148">Настройка принтера Windows</span><span class="sxs-lookup"><span data-stu-id="4a334-148">Set up a Windows printer</span></span>

<span data-ttu-id="4a334-149">Выполните следующие действия, чтобы включить печать документов с POS-терминала на принтере Windows, подключенном к станции оборудования.</span><span class="sxs-lookup"><span data-stu-id="4a334-149">Follow these steps to enable documents to be printed from POS on a Windows printer that is connected to the hardware station.</span></span>

1. <span data-ttu-id="4a334-150">Перейдите **Retail и Commerce \> Настройка канала \> Настройка POS \> Профили POS \> Профили оборудования**.</span><span class="sxs-lookup"><span data-stu-id="4a334-150">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Hardware profiles**.</span></span>
2. <span data-ttu-id="4a334-151">Выберите профиль оборудования, который относится к магазину, в котором используется принтер.</span><span class="sxs-lookup"><span data-stu-id="4a334-151">Select a hardware profile that is related to the store where the printer is used.</span></span>
3. <span data-ttu-id="4a334-152">В разделе **Принтер** или **Принтер 2** обновите параметры:</span><span class="sxs-lookup"><span data-stu-id="4a334-152">In either the **Printer** section or the **Printer 2** section, update the settings:</span></span>

    - <span data-ttu-id="4a334-153">В поле **Принтер** выберите **Драйвер Windows**.</span><span class="sxs-lookup"><span data-stu-id="4a334-153">In the **Printer** field, select **Windows driver**.</span></span>
    - <span data-ttu-id="4a334-154">В поле **Наименование устройства** введите имя принтера.</span><span class="sxs-lookup"><span data-stu-id="4a334-154">In the **Device name** field, enter the name of the printer.</span></span>

4. <span data-ttu-id="4a334-155">Перейдите в раздел **Retail и Commerce \> ИТ Retail и Commerce \> График распределения**.</span><span class="sxs-lookup"><span data-stu-id="4a334-155">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="4a334-156">Выберите задание **1090**, затем выберите **Запустить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="4a334-156">Select job **1090**, and then select **Run now**.</span></span>
