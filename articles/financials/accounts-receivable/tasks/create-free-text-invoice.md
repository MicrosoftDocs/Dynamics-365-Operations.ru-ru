--- 
title: "Создание накладных с произвольным текстом"
description: "В этом руководстве по задаче показано, как создать накладную с произвольным текстом."
author: mikefalkner
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ef3cad6538d9efbd1c1881f4b7d771382d9b1ba8
ms.openlocfilehash: 87e293008fd748aa0dcc6b3caa94a4889bed35de
ms.contentlocale: ru-ru
ms.lasthandoff: 10/26/2017

---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="a348b-103">Создание накладных с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="a348b-103">Create a free text invoice</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a348b-104">В этом руководстве по задаче показано, как создать накладную с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="a348b-104">This task guide demonstrates creating a free text invoice.</span></span> <span data-ttu-id="a348b-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="a348b-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="a348b-106">Перейдите в раздел "Расчеты с клиентами" > "Накладные" > "Все накладные с произвольным текстом".</span><span class="sxs-lookup"><span data-stu-id="a348b-106">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="a348b-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a348b-107">Click New.</span></span>
3. <span data-ttu-id="a348b-108">В поле "Счет клиента" выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a348b-108">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="a348b-109">В качестве счета накладной по умолчанию будет использоваться тот же счет, который использовался для счета клиента.</span><span class="sxs-lookup"><span data-stu-id="a348b-109">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="a348b-110">Статус учета начинается со значения "В работе", если накладная не разнесена.</span><span class="sxs-lookup"><span data-stu-id="a348b-110">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="a348b-111">Номер накладной будет присвоен при разноске накладной.</span><span class="sxs-lookup"><span data-stu-id="a348b-111">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="a348b-112">При использовании поручений SEPA в поручение на безакцептное списание будет автоматически подставлено нужное поручение при выборе счета клиента.</span><span class="sxs-lookup"><span data-stu-id="a348b-112">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="a348b-113">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a348b-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a348b-114">В поле "Счет ГК" укажите номер счета без аналитик.</span><span class="sxs-lookup"><span data-stu-id="a348b-114">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="a348b-115">Вы также можете ввести один или несколько символов счета ГК, чтобы найти нужный счет с помощью подстановки.</span><span class="sxs-lookup"><span data-stu-id="a348b-115">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="a348b-116">Аналитики будут введены далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="a348b-116">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="a348b-117">Разверните экспресс-вкладку "Сведения о строке", чтобы добавить аналитики в счет ГК.</span><span class="sxs-lookup"><span data-stu-id="a348b-117">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="a348b-118">Перейдите на вкладку "Строка финансовой аналитики".</span><span class="sxs-lookup"><span data-stu-id="a348b-118">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="a348b-119">Аналитики используются только для выбранной строки.</span><span class="sxs-lookup"><span data-stu-id="a348b-119">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="a348b-120">Налоговая группа заполняется из данных клиента.</span><span class="sxs-lookup"><span data-stu-id="a348b-120">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="a348b-121">Если для клиента не указана налоговая группа, используется налоговая группа из счета ГК.</span><span class="sxs-lookup"><span data-stu-id="a348b-121">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="a348b-122">Значение налоговой группы номенклатур заполняется на основании счета ГК.</span><span class="sxs-lookup"><span data-stu-id="a348b-122">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="a348b-123">Если для счета ГК не указана налоговая группа номенклатур, используется налоговая группа номенклатур в параметрах налоговой группы счета ГК.</span><span class="sxs-lookup"><span data-stu-id="a348b-123">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="a348b-124">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="a348b-124">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="a348b-125">Вводить количество необязательно.</span><span class="sxs-lookup"><span data-stu-id="a348b-125">The quantity is optional.</span></span>  
9. <span data-ttu-id="a348b-126">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="a348b-126">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="a348b-127">Вводить цену за единицу необязательно.</span><span class="sxs-lookup"><span data-stu-id="a348b-127">The unit price is optional.</span></span>  
    * <span data-ttu-id="a348b-128">Сумма рассчитывается как количество, умноженное на цену за единицу.</span><span class="sxs-lookup"><span data-stu-id="a348b-128">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="a348b-129">Однако можно переопределить этот расчет и ввести сумму.</span><span class="sxs-lookup"><span data-stu-id="a348b-129">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="a348b-130">Щелкните "Налог", чтобы увидеть налог, рассчитанный для накладной.</span><span class="sxs-lookup"><span data-stu-id="a348b-130">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="a348b-131">На этой странице вы можете увидеть суммы налога, а на вкладке "Корректировка" — переопределить их.</span><span class="sxs-lookup"><span data-stu-id="a348b-131">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="a348b-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a348b-132">Click OK.</span></span>
12. <span data-ttu-id="a348b-133">Щелкните "Накладные расходы", чтобы добавить накладные расходы в накладную.</span><span class="sxs-lookup"><span data-stu-id="a348b-133">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="a348b-134">В поле "Код накладных расходов" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a348b-134">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="a348b-135">В поле "Значение накладных расходов" введите число.</span><span class="sxs-lookup"><span data-stu-id="a348b-135">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="a348b-136">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a348b-136">Close the page.</span></span>
16. <span data-ttu-id="a348b-137">Щелкните "Итоги", чтобы просмотреть сводные сведения и итоги по накладной.</span><span class="sxs-lookup"><span data-stu-id="a348b-137">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="a348b-138">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="a348b-138">Click Close.</span></span>
18. <span data-ttu-id="a348b-139">Щелкните "Разнести", чтобы выполнить разноску накладной.</span><span class="sxs-lookup"><span data-stu-id="a348b-139">Click Post to post the invoice.</span></span> <span data-ttu-id="a348b-140">Это действие можно отменить перед разноской.</span><span class="sxs-lookup"><span data-stu-id="a348b-140">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="a348b-141">Чтобы изменить время печати счетов:  выберите "Текущие" для печати каждого счета при его обновлении   или  выберите "После" для печать после обновления всех счетов.</span><span class="sxs-lookup"><span data-stu-id="a348b-141">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="a348b-142">Если необходимо изменить способ проверки кредитного лимита клиента перед разноской, измените тип "Кредитный лимит".</span><span class="sxs-lookup"><span data-stu-id="a348b-142">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="a348b-143">Если требуется напечатать накладную, выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="a348b-143">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="a348b-144">Если требуется разнести накладную, выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="a348b-144">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="a348b-145">Можно напечатать накладную без разноски.</span><span class="sxs-lookup"><span data-stu-id="a348b-145">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="a348b-146">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a348b-146">Click OK.</span></span>


