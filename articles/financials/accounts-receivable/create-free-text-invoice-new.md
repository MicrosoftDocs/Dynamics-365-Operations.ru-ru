--- 
title: "Создание накладных с произвольным текстом"
description: "Эта статья показывает, как создать шаблона накладной с произвольным текстом."
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e6f89a6d77ff8e1cd88632df0d9a72915086ee1e
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---

# <a name="create-a-free-text-invoice"></a><span data-ttu-id="64358-103">Создание накладных с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="64358-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64358-104">Эта статья показывает, как создать шаблона накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="64358-104">This article demonstrates how to create a free text invoice.</span></span> <span data-ttu-id="64358-105">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="64358-105">For this procedure, use the USMF demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="64358-106">Создание накладных с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="64358-106">Create a free text invoice</span></span>

1. <span data-ttu-id="64358-107">Перейдите в раздел "Расчеты с клиентами" > "Накладные" > "Все накладные с произвольным текстом".</span><span class="sxs-lookup"><span data-stu-id="64358-107">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="64358-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="64358-108">Click New.</span></span>
3. <span data-ttu-id="64358-109">В поле "Счет клиента" выберите значение.</span><span class="sxs-lookup"><span data-stu-id="64358-109">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="64358-110">В качестве счета накладной по умолчанию будет использоваться тот же счет, который использовался для счета клиента.</span><span class="sxs-lookup"><span data-stu-id="64358-110">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="64358-111">Статус учета начинается со значения "В работе", если накладная не разнесена.</span><span class="sxs-lookup"><span data-stu-id="64358-111">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="64358-112">Номер накладной будет присвоен при разноске накладной.</span><span class="sxs-lookup"><span data-stu-id="64358-112">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="64358-113">При использовании поручений SEPA в поручение на безакцептное списание будет автоматически подставлено нужное поручение при выборе счета клиента.</span><span class="sxs-lookup"><span data-stu-id="64358-113">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="64358-114">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="64358-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="64358-115">В поле "Счет ГК" укажите номер счета без аналитик.</span><span class="sxs-lookup"><span data-stu-id="64358-115">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="64358-116">Вы также можете ввести один или несколько символов счета ГК, чтобы найти нужный счет с помощью подстановки.</span><span class="sxs-lookup"><span data-stu-id="64358-116">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="64358-117">Аналитики будут введены далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="64358-117">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="64358-118">Разверните экспресс-вкладку "Сведения о строке", чтобы добавить аналитики в счет ГК.</span><span class="sxs-lookup"><span data-stu-id="64358-118">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="64358-119">Перейдите на вкладку "Строка финансовой аналитики".</span><span class="sxs-lookup"><span data-stu-id="64358-119">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="64358-120">Аналитики используются только для выбранной строки.</span><span class="sxs-lookup"><span data-stu-id="64358-120">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="64358-121">Налоговая группа заполняется из данных клиента.</span><span class="sxs-lookup"><span data-stu-id="64358-121">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="64358-122">Если для клиента не указана налоговая группа, используется налоговая группа из счета ГК.</span><span class="sxs-lookup"><span data-stu-id="64358-122">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="64358-123">Значение налоговой группы номенклатур заполняется на основании счета ГК.</span><span class="sxs-lookup"><span data-stu-id="64358-123">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="64358-124">Если для счета ГК не указана налоговая группа номенклатур, используется налоговая группа номенклатур в параметрах налоговой группы счета ГК.</span><span class="sxs-lookup"><span data-stu-id="64358-124">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="64358-125">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="64358-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="64358-126">Вводить количество необязательно.</span><span class="sxs-lookup"><span data-stu-id="64358-126">The quantity is optional.</span></span>  
9. <span data-ttu-id="64358-127">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="64358-127">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="64358-128">Вводить цену за единицу необязательно.</span><span class="sxs-lookup"><span data-stu-id="64358-128">The unit price is optional.</span></span>  
    * <span data-ttu-id="64358-129">Сумма рассчитывается как количество, умноженное на цену за единицу.</span><span class="sxs-lookup"><span data-stu-id="64358-129">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="64358-130">Однако можно переопределить этот расчет и ввести сумму.</span><span class="sxs-lookup"><span data-stu-id="64358-130">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="64358-131">Щелкните "Налог", чтобы увидеть налог, рассчитанный для накладной.</span><span class="sxs-lookup"><span data-stu-id="64358-131">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="64358-132">На этой странице вы можете увидеть суммы налога, а на вкладке "Корректировка" — переопределить их.</span><span class="sxs-lookup"><span data-stu-id="64358-132">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="64358-133">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="64358-133">Click OK.</span></span>
12. <span data-ttu-id="64358-134">Щелкните "Накладные расходы", чтобы добавить накладные расходы в накладную.</span><span class="sxs-lookup"><span data-stu-id="64358-134">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="64358-135">В поле "Код накладных расходов" введите значение.</span><span class="sxs-lookup"><span data-stu-id="64358-135">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="64358-136">В поле "Значение накладных расходов" введите число.</span><span class="sxs-lookup"><span data-stu-id="64358-136">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="64358-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="64358-137">Close the page.</span></span>
16. <span data-ttu-id="64358-138">Щелкните "Итоги", чтобы просмотреть сводные сведения и итоги по накладной.</span><span class="sxs-lookup"><span data-stu-id="64358-138">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="64358-139">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="64358-139">Click Close.</span></span>
18. <span data-ttu-id="64358-140">Щелкните "Разнести", чтобы выполнить разноску накладной.</span><span class="sxs-lookup"><span data-stu-id="64358-140">Click Post to post the invoice.</span></span> <span data-ttu-id="64358-141">Это действие можно отменить перед разноской.</span><span class="sxs-lookup"><span data-stu-id="64358-141">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="64358-142">Чтобы изменить время печати счетов:  выберите "Текущие" для печати каждого счета при его обновлении   или  выберите "После" для печать после обновления всех счетов.</span><span class="sxs-lookup"><span data-stu-id="64358-142">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="64358-143">Если необходимо изменить способ проверки кредитного лимита клиента перед разноской, измените тип "Кредитный лимит".</span><span class="sxs-lookup"><span data-stu-id="64358-143">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="64358-144">Если требуется напечатать накладную, выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="64358-144">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="64358-145">Если требуется разнести накладную, выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="64358-145">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="64358-146">Можно напечатать накладную без разноски.</span><span class="sxs-lookup"><span data-stu-id="64358-146">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="64358-147">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="64358-147">Click OK.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="64358-148">Копирование строк</span><span class="sxs-lookup"><span data-stu-id="64358-148">Copy lines</span></span>
<span data-ttu-id="64358-149">Для копирования строк в накладной с произвольным текстом выберите одну или несколько строк и выберите команду "Копировать выбранные строки".</span><span class="sxs-lookup"><span data-stu-id="64358-149">To copy lines on the free text invoice, select one or more lines and then click Copy selected lines.</span></span> <span data-ttu-id="64358-150">Можно указать количество копий, которые необходимо сделать, а также можно скопировать примечания и вложения.</span><span class="sxs-lookup"><span data-stu-id="64358-150">You can specify the number of copies that you want to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="64358-151">Можно скопировать распределения или разрешить их повторное создание при разноске.</span><span class="sxs-lookup"><span data-stu-id="64358-151">You can copy the distributions or allow them to be recreated when you post.</span></span> <span data-ttu-id="64358-152">Как только будут скопированы все строки, при необходимости можно изменить сообщение.</span><span class="sxs-lookup"><span data-stu-id="64358-152">Once you copy the lines, you can edit the information as needed.</span></span> 

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="64358-153">Создание накладных с произвольным текстом из шаблона</span><span class="sxs-lookup"><span data-stu-id="64358-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="64358-154">Можно создать накладных с произвольным текстом из шаблона.</span><span class="sxs-lookup"><span data-stu-id="64358-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="64358-155">При выборе "Создать" из шаблона на вкладке "Накладная" можно выбрать имя шаблона и накладную клиента для новой накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="64358-155">When you select New from template from the Invoice tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="64358-156">Также, можно задать значения по умолчанию, например, условия оплаты и метод оплаты от клиента или использовать значения, которые были сохранены с шаблоном.</span><span class="sxs-lookup"><span data-stu-id="64358-156">You can also choose to default values such as the terms of payment and method of payment from the customer or use the values that were saved with the template.</span></span> <span data-ttu-id="64358-157">Новая накладная с произвольным текстом будет создана, и вы сможете редактировать значения в накладной.</span><span class="sxs-lookup"><span data-stu-id="64358-157">A new free text invoice will be created and you can edit the values in that invoice.</span></span> 


