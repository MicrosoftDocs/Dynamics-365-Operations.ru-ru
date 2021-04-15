---
title: Розничные отчеты
description: В этой теме описывается, как создаются и разносятся отчеты.
author: ashishmsft
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 8d6687ddaae28ebf278aca6a78ba798e2e79edd8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791929"
---
# <a name="retail-statements"></a><span data-ttu-id="01e47-103">Журналы операций розничной торговли</span><span class="sxs-lookup"><span data-stu-id="01e47-103">Retail statements</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="01e47-104">В Dynamics 365 Commerce процесс разноски отчетов используется для учета проводок, которые происходят в Cloud POS или Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="01e47-104">In Dynamics 365 Commerce, the statement posting process is used to account for the transactions that occur in Cloud point of sale (POS) or Modern POS (MPOS).</span></span> <span data-ttu-id="01e47-105">Процесс разноски отчетов использует график распределения для загрузки набора проводок POS в клиент центрального офиса.</span><span class="sxs-lookup"><span data-stu-id="01e47-105">The statement posting process uses the distribution schedule to pull a set of POS transactions into the headquarters (HQ) client.</span></span> <span data-ttu-id="01e47-106">Параметры, которые определены на страницах **Параметры Commerce** и **Магазины**, используются для выбора проводок, которые будут загружены в отдельные отчеты.</span><span class="sxs-lookup"><span data-stu-id="01e47-106">The parameters that are defined on the **Commerce parameters** and **Stores** pages are used to select the transactions that are pulled into individual statements.</span></span>

<span data-ttu-id="01e47-107">На следующем рисунке представлен процесс разноски отчета.</span><span class="sxs-lookup"><span data-stu-id="01e47-107">The following illustration shows the statement posting process.</span></span> <span data-ttu-id="01e47-108">В ходе этого процесса проводки, записанные в POS, передаются клиенту с помощью планировщик Commerce.</span><span class="sxs-lookup"><span data-stu-id="01e47-108">In this process, transactions that are recorded in the POS are transmitted to the client by using the Commerce scheduler.</span></span> <span data-ttu-id="01e47-109">После получения клиентом проводок можно создать, рассчитать и разнести отчет о проводках для магазина.</span><span class="sxs-lookup"><span data-stu-id="01e47-109">After the client receives the transactions, you can create, calculate, and post the transaction statement for the store.</span></span>

<span data-ttu-id="01e47-110">[![Процесс разноски отчетов](./media/retail-statements.png)](./media/retail-statements.png)</span><span class="sxs-lookup"><span data-stu-id="01e47-110">[![Statement posting process](./media/retail-statements.png)](./media/retail-statements.png)</span></span>

## <a name="creating-and-posting-statements"></a><span data-ttu-id="01e47-111">Создание и разноска отчетов</span><span class="sxs-lookup"><span data-stu-id="01e47-111">Creating and posting statements</span></span>

<span data-ttu-id="01e47-112">Можно создать отчет вручную или используя процессы пакетной обработки, настраиваемые для периодического выполнения в течение дня.</span><span class="sxs-lookup"><span data-stu-id="01e47-112">You can create a statement manually or by using batch processes that you set up to run periodically throughout the day.</span></span> <span data-ttu-id="01e47-113">В обоих случаях для создания и разноски отчетов выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="01e47-113">In both cases, the following steps are used to create and post statements.</span></span>

### <a name="create-the-statement"></a><span data-ttu-id="01e47-114">Создание отчета</span><span class="sxs-lookup"><span data-stu-id="01e47-114">Create the statement</span></span>

<span data-ttu-id="01e47-115">На этом этапе определяется магазин, для которого вручную создается отчет.</span><span class="sxs-lookup"><span data-stu-id="01e47-115">This step identifies the store that the statement is manually created for.</span></span> <span data-ttu-id="01e47-116">Если настроить процесс пакетной обработки, можно автоматически создать отчеты для всех магазинов с использованием определенного пользователем графика.</span><span class="sxs-lookup"><span data-stu-id="01e47-116">If you configure a batch process, you can automatically create statements for all stores, based on a schedule that you define.</span></span>

### <a name="calculate-the-statement"></a><span data-ttu-id="01e47-117">Расчет отчета</span><span class="sxs-lookup"><span data-stu-id="01e47-117">Calculate the statement</span></span>

<span data-ttu-id="01e47-118">На этом шаге строки проводки выбираются на основе критериев, определенных для каждого магазина на страницах **Параметры Commerce** и **Магазины**.</span><span class="sxs-lookup"><span data-stu-id="01e47-118">In this step, the transaction lines are selected based on criteria that are defined for each store on the **Commerce parameters** and **Stores** pages.</span></span> <span data-ttu-id="01e47-119">На этих страница можно определить критерии и указать способ расчета проводок.</span><span class="sxs-lookup"><span data-stu-id="01e47-119">On these pages, you define the criteria and specify how the transactions are calculated.</span></span> <span data-ttu-id="01e47-120">Для просмотра списка включенных в отчет проводок до расчета отчета используйте страницу **Проводки**.</span><span class="sxs-lookup"><span data-stu-id="01e47-120">To view a list of the transactions that are included in the statement before you calculate the statement, use the **Transactions** page.</span></span>

<span data-ttu-id="01e47-121">Расчет отчета осуществляется с использованием деклараций платежных средств из ККМ в виде учтенного количества.</span><span class="sxs-lookup"><span data-stu-id="01e47-121">Statement calculation uses tender declarations from the registers as the counted amount.</span></span> <span data-ttu-id="01e47-122">Кроме того, можно ввести учтенное количество вручную.</span><span class="sxs-lookup"><span data-stu-id="01e47-122">Alternatively, you can enter the counted amount manually.</span></span> <span data-ttu-id="01e47-123">В отчете показана разница между суммой продажи для проводок и фактической подсчитанной суммой во всех способах оплаты.</span><span class="sxs-lookup"><span data-stu-id="01e47-123">The statement shows the difference between the sales amount for the transactions and the actual counted amount in all payment methods.</span></span> <span data-ttu-id="01e47-124">Отчет разносится, только если эта разница меньше максимальной установленной для магазина разницы разноски.</span><span class="sxs-lookup"><span data-stu-id="01e47-124">The statement is posted only if this difference is less than the maximum posting difference that is defined for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="01e47-125">Процесс расчета отчетов осуществляется с использованием глобальной номерной серии.</span><span class="sxs-lookup"><span data-stu-id="01e47-125">The statement calculation process uses the global number sequence.</span></span>

<span data-ttu-id="01e47-126">При расчете отчета выполняются следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="01e47-126">When you calculate a statement, the calculation includes the following tasks:</span></span>

- <span data-ttu-id="01e47-127">Для выбранного диапазона дат помечаются проводки, которые не были включены в предыдущий расчет отчета.</span><span class="sxs-lookup"><span data-stu-id="01e47-127">For the selected date range, mark transactions that weren't included in a previous statement calculation.</span></span>
- <span data-ttu-id="01e47-128">Рассчитываются общие суммы по платежным средствам в выбранных проводках.</span><span class="sxs-lookup"><span data-stu-id="01e47-128">Calculate the total amounts that were tendered in the selected transactions.</span></span> <span data-ttu-id="01e47-129">Результаты отображаются в строках отчета в зависимости от метода агрегирования операций:</span><span class="sxs-lookup"><span data-stu-id="01e47-129">The results are shown on the statement lines, depending on the statement method:</span></span>

    - <span data-ttu-id="01e47-130">Если используется метод агрегирования операций **Итого**, отдельная строка создается для каждого способа оплаты в выбранных проводках.</span><span class="sxs-lookup"><span data-stu-id="01e47-130">If the statement method is **Total**, a line is created for each payment method in the selected transactions.</span></span>
    - <span data-ttu-id="01e47-131">Если используется способ агрегирования операций **Персонал**, отдельная строка создается для каждого способа оплаты в проводках, выполненных выбранным сотрудником.</span><span class="sxs-lookup"><span data-stu-id="01e47-131">If the statement method is **Staff**, a line is created for each payment method in transactions that were performed by the selected staff member.</span></span>
    - <span data-ttu-id="01e47-132">Если используется метод агрегирования операций **POS-терминал**, отдельная строка создается для каждого способа оплаты в проводках, выполненных с выбранной ККМ.</span><span class="sxs-lookup"><span data-stu-id="01e47-132">If the statement method is **POS terminal**, a line is created for each payment method in transactions that were performed on the selected register.</span></span>
    - <span data-ttu-id="01e47-133">Если используется метод агрегирования операций **Смена**, отдельная строка создается для каждого способа оплаты в проводках, выполненных в смену.</span><span class="sxs-lookup"><span data-stu-id="01e47-133">If the statement method is **Shift**, a line is created for each payment method in transactions that were performed during a shift.</span></span>

<span data-ttu-id="01e47-134">Если установлен флажок **Разбить по методу агрегирования операций** на странице **Магазины**, создается отдельный отчет на основании значения, выбранного в поле **Метод агрегирования операций**.</span><span class="sxs-lookup"><span data-stu-id="01e47-134">If the **Split by Statement method** check box is selected on the **Stores** page, a separate statement is created based on the value that is selected in the **Statement method** field.</span></span>

<span data-ttu-id="01e47-135">Если магазин работает после полуночи, разноску отчетов можно настроить так, чтобы она основывалась на конце рабочего дня, а не на конце календарного дня.</span><span class="sxs-lookup"><span data-stu-id="01e47-135">If your store's operating hours extend past midnight, you can configure statement posting so that it's based on the end of the business day instead of the end of the calendar day.</span></span>

<span data-ttu-id="01e47-136">На странице **Магазины** на экспресс-вкладке **Операция/закрытие** в поле **Конец рабочего дня** введите время записи последней проводки для включения в отчет рабочего дня.</span><span class="sxs-lookup"><span data-stu-id="01e47-136">On the **Stores** page, on the **Statement/closing** FastTab, in the **End of business day** field, enter the time that the last transaction must be recorded to be included in the business day's statement.</span></span> <span data-ttu-id="01e47-137">Установите флажок **Разнести как рабочий день**, чтобы разнести проводки за рабочий день.</span><span class="sxs-lookup"><span data-stu-id="01e47-137">Select the **Post as business day** check box to post the transactions within the same business day.</span></span> <span data-ttu-id="01e47-138">При разноске отчета проводки, записанные в один рабочий день, могут быть включены в один заказ на продажу, даже если они произведены до и после полуночи.</span><span class="sxs-lookup"><span data-stu-id="01e47-138">When the statement is posted, transactions that are recorded within the same business day can be included on the same sales order, even if some transactions occur before midnight and other transactions occur after midnight.</span></span>

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a><span data-ttu-id="01e47-139">Пример: разноска отчета за рабочий день, который охватывает два календарных дня</span><span class="sxs-lookup"><span data-stu-id="01e47-139">Example: Post a statement for a business day that extends over two calendar days</span></span>

<span data-ttu-id="01e47-140">Магазин открыт с 8:00 до 03:00, и установлен флажок **Разнести как рабочий день** в конфигурации магазина.</span><span class="sxs-lookup"><span data-stu-id="01e47-140">A store is open between 8:00 AM and 3:00 AM, and the **Post as business day** check box is selected in the store's configuration.</span></span> <span data-ttu-id="01e47-141">31 мая в магазине регистрируются проводки между 8:00 и полуночью.</span><span class="sxs-lookup"><span data-stu-id="01e47-141">On May 31, the store records transactions between 8:00 AM and midnight.</span></span> <span data-ttu-id="01e47-142">В магазине также регистрируются проводки с 00:01 до 3:00 1 июня.</span><span class="sxs-lookup"><span data-stu-id="01e47-142">The store also records transactions between 12:01 AM and 3:00 AM on June 1.</span></span>

<span data-ttu-id="01e47-143">При разноске магазином отчета для закрытия рабочего дня создается заказ на продажу, который включает все проводки, зарегистрированные с 8:00 до 3:00, даже если проводки были выполнены 31 мая и 1 июня.</span><span class="sxs-lookup"><span data-stu-id="01e47-143">When the store posts its statement for the close of the business day, the sales order that is generated includes all transactions that were recorded between the business hours of 8:00 AM and 3:00 AM, even though the transactions occurred on two days, May 31 and June 1.</span></span>

<span data-ttu-id="01e47-144">Если для того же магазина флажок **Разнести как рабочий день** не установлен, создаются отдельные заказы на продажу при разноске магазином отчета для закрытия рабочего дня.</span><span class="sxs-lookup"><span data-stu-id="01e47-144">If the **Post as business day** check box is cleared for the same store, separate sales orders are generated when the store posts its statement for the close of the business day.</span></span> <span data-ttu-id="01e47-145">Один заказ на продажу включает проводки, которые были зарегистрированы с 8:00 до полуночи 31 мая, а второй заказ на продажу включает проводки, которые были зарегистрированы с 00:01 до 3:00 1 июня.</span><span class="sxs-lookup"><span data-stu-id="01e47-145">One sales order includes the transactions that were recorded between the business hours of 8:00 AM and midnight on May 31, and the second sales order includes the transactions that were recorded between the business hours of 12:01 AM and 3:00 AM on June 1.</span></span>

> [!NOTE]
> <span data-ttu-id="01e47-146">Перед созданием отчетов необходимо закрыть смены в отчетном периоде.</span><span class="sxs-lookup"><span data-stu-id="01e47-146">Before you can create statements, you should close the shifts in the statement period.</span></span>

### <a name="post-the-statement"></a><span data-ttu-id="01e47-147">Разноска отчета</span><span class="sxs-lookup"><span data-stu-id="01e47-147">Post the statement</span></span>

<span data-ttu-id="01e47-148">При разноске создаются отчета заказы на продажу и накладные для продаж в отчете.</span><span class="sxs-lookup"><span data-stu-id="01e47-148">When you post a statement, sales orders and invoices are created for the sales in the statement.</span></span>

- <span data-ttu-id="01e47-149">Мелкооптовые продажи за наличные объединяются в один заказ на продажу и включаются в накладную для клиента по умолчанию, назначенного магазину.</span><span class="sxs-lookup"><span data-stu-id="01e47-149">Cash and carry sales are aggregated onto one sales order, and are invoiced for the default customer who is assigned to the store.</span></span>
- <span data-ttu-id="01e47-150">Продажи, в которых клиент был добавлен в проводку в POS, создают отдельные заказы на продажу и накладные — по одной для каждого уникального клиента.</span><span class="sxs-lookup"><span data-stu-id="01e47-150">Sales for which a customer was added to the transaction in POS generate separate sales orders and invoices, one for each unique customer.</span></span>

<span data-ttu-id="01e47-151">Журналы платежей автоматически создаются для платежей в отчете, а сведения о запасах для POS обновляются.</span><span class="sxs-lookup"><span data-stu-id="01e47-151">Payment journals are automatically created for the payments in the statement, and the inventory is updated for the POS store.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]