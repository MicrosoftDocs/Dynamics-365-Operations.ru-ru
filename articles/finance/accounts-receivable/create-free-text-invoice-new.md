---
title: Создание накладных с произвольным текстом
description: В этой теме описывается, как создавать накладные с произвольным текстом.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 1ac06e7d702ffe3a8cdb6bd2823f2ffdc055c722
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976531"
---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="febcb-103">Создание накладных с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="febcb-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="febcb-104">В этой теме описывается, как создавать накладные с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="febcb-104">This topic explains how to create free text invoices.</span></span> <span data-ttu-id="febcb-105">В данной процедуре используется демонстрационная компания **USMF**.</span><span class="sxs-lookup"><span data-stu-id="febcb-105">For the procedure, use the **USMF** demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="febcb-106">Создание накладных с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="febcb-106">Create a free text invoice</span></span>

1. <span data-ttu-id="febcb-107">Перейдите в раздел **Расчеты с клиентами \> Накладные \> Все накладные с произвольным текстом**.</span><span class="sxs-lookup"><span data-stu-id="febcb-107">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2. <span data-ttu-id="febcb-108">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="febcb-108">Select **New**.</span></span>
3. <span data-ttu-id="febcb-109">В поле **Счет клиента** выберите значение.</span><span class="sxs-lookup"><span data-stu-id="febcb-109">In the **Customer account** field, select a value.</span></span>

    * <span data-ttu-id="febcb-110">По умолчанию счет, выбранный в качестве счета клиента, используется в качестве счета накладной.</span><span class="sxs-lookup"><span data-stu-id="febcb-110">By default, the account that is selected as the customer account is used as the invoice account.</span></span>
    * <span data-ttu-id="febcb-111">Если накладная не разнесена, статус учета начинается со значения **В работе**.</span><span class="sxs-lookup"><span data-stu-id="febcb-111">If the invoice isn't posted, the accounting status starts with **In process**.</span></span>
    * <span data-ttu-id="febcb-112">Номер накладной будет присвоен при разноске накладной.</span><span class="sxs-lookup"><span data-stu-id="febcb-112">The invoice number will be assigned when the invoice is posted.</span></span>
    * <span data-ttu-id="febcb-113">При использовании поручений Единой зоны платежей в евро SEPA поручение на безакцептное списание вводится автоматически при выборе счета клиента.</span><span class="sxs-lookup"><span data-stu-id="febcb-113">If you're using Single Euro Payments Area (SEPA) mandates, the direct debit mandate is automatically entered when you select the customer account.</span></span>

4. <span data-ttu-id="febcb-114">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="febcb-114">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="febcb-115">В поле **Счет ГК** укажите номер счета, в которого нет аналитик.</span><span class="sxs-lookup"><span data-stu-id="febcb-115">In the **Main account** field, specify an account number that doesn't have dimensions.</span></span> <span data-ttu-id="febcb-116">Аналитики будут введены позже.</span><span class="sxs-lookup"><span data-stu-id="febcb-116">You will enter dimensions later in this topic.</span></span>

    <span data-ttu-id="febcb-117">Вы также можете ввести один или несколько символов счета ГК, чтобы найти нужный счет с помощью подстановки.</span><span class="sxs-lookup"><span data-stu-id="febcb-117">You can also enter one or more characters for the main account, and use the lookup to find the account.</span></span>

6. <span data-ttu-id="febcb-118">Выберите экспресс-вкладку **Сведения о строке**, чтобы добавить аналитики к счету ГК.</span><span class="sxs-lookup"><span data-stu-id="febcb-118">Select the **Line details** FastTab to add dimensions to the main account.</span></span>
7. <span data-ttu-id="febcb-119">Выберите вкладку **Финансовые аналитики строки**.</span><span class="sxs-lookup"><span data-stu-id="febcb-119">Select the **Financial dimensions line** tab.</span></span>

    * <span data-ttu-id="febcb-120">Аналитики используются только для выбранной строки.</span><span class="sxs-lookup"><span data-stu-id="febcb-120">The dimensions are for the selected line only.</span></span>
    * <span data-ttu-id="febcb-121">Налоговая группа подставляется из записи клиента.</span><span class="sxs-lookup"><span data-stu-id="febcb-121">The sales tax group is filled in from the customer.</span></span> <span data-ttu-id="febcb-122">Если для клиента не указана налоговая группа, используется налоговая группа из счета ГК.</span><span class="sxs-lookup"><span data-stu-id="febcb-122">If the customer doesn't have a sales tax group, the sales tax group from the main account is used.</span></span>
    * <span data-ttu-id="febcb-123">Значение налоговой группы номенклатур заполняется из счета ГК.</span><span class="sxs-lookup"><span data-stu-id="febcb-123">The items sales tax group is filled in from the main account.</span></span> <span data-ttu-id="febcb-124">Если для счета ГК не указана налоговая группа номенклатур, используется налоговая группа номенклатур, указанная в параметрах налоговой группы в главной книге.</span><span class="sxs-lookup"><span data-stu-id="febcb-124">If the main account doesn't have an item sales tax group, the item sales tax group that is specified in the sales tax parameters in General ledger is used.</span></span>

8. <span data-ttu-id="febcb-125">(Необязательно.) В поле **Количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="febcb-125">Optional: In the **Quantity** field, enter a number.</span></span>
9. <span data-ttu-id="febcb-126">(Необязательно.) В поле **Цена за единицу** введите число.</span><span class="sxs-lookup"><span data-stu-id="febcb-126">Optional: In the **Unit price** field, enter a number.</span></span>

    <span data-ttu-id="febcb-127">Сумма рассчитывается как количество, умноженное на цену за единицу.</span><span class="sxs-lookup"><span data-stu-id="febcb-127">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="febcb-128">Однако этот расчет можно переопределить, введя сумму вручную.</span><span class="sxs-lookup"><span data-stu-id="febcb-128">However, you can override that calculation by entering an amount.</span></span>

10. <span data-ttu-id="febcb-129">Выберите **Налог**, чтобы увидеть налог, рассчитанный для накладной.</span><span class="sxs-lookup"><span data-stu-id="febcb-129">Select **Sales tax** to view the sales tax that is calculated for the invoice.</span></span>

    <span data-ttu-id="febcb-130">На этой странице можно просмотреть суммы налога, а на вкладке **Корректировка** — переопределить их.</span><span class="sxs-lookup"><span data-stu-id="febcb-130">You can view the sales tax amounts on this page, or you can override the amounts on the **Adjustment** tab.</span></span>

11. <span data-ttu-id="febcb-131">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="febcb-131">Select **OK**.</span></span>
12. <span data-ttu-id="febcb-132">Выберите **Накладные расходы**, чтобы добавить в накладную накладные расходы.</span><span class="sxs-lookup"><span data-stu-id="febcb-132">Select **Charges** to add a charge to the invoice.</span></span>
13. <span data-ttu-id="febcb-133">В поле **Код накладных расходов** введите значение.</span><span class="sxs-lookup"><span data-stu-id="febcb-133">In the **Charges code** field, enter a value.</span></span>
14. <span data-ttu-id="febcb-134">В поле **Значение расходов** введите число.</span><span class="sxs-lookup"><span data-stu-id="febcb-134">In the **Charges value** field, enter a number.</span></span>
15. <span data-ttu-id="febcb-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="febcb-135">Close the page.</span></span>
16. <span data-ttu-id="febcb-136">Выберите **Итоги**, чтобы просмотреть сводные сведения и итоги по накладной.</span><span class="sxs-lookup"><span data-stu-id="febcb-136">Select **Totals** to view a summary of the invoice details and totals.</span></span>
17. <span data-ttu-id="febcb-137">Выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="febcb-137">Select **Close**.</span></span>
18. <span data-ttu-id="febcb-138">Выберите **Разнести**, чтобы разнести накладную.</span><span class="sxs-lookup"><span data-stu-id="febcb-138">Select **Post** to post the invoice.</span></span> <span data-ttu-id="febcb-139">У вас будет возможность отменить разноску, прежде чем накладная действительно будет разнесена.</span><span class="sxs-lookup"><span data-stu-id="febcb-139">You will still have an opportunity to cancel before you actually post.</span></span>

    * <span data-ttu-id="febcb-140">Можно также изменить время печати накладных.</span><span class="sxs-lookup"><span data-stu-id="febcb-140">You can change the timing of invoice printing.</span></span> <span data-ttu-id="febcb-141">Выберите **Текущий** для печати каждой накладной при ее обновлении.</span><span class="sxs-lookup"><span data-stu-id="febcb-141">Select **Current** to print each invoice as it's updated.</span></span> <span data-ttu-id="febcb-142">Выберите **После** для печати после обновления всех накладных.</span><span class="sxs-lookup"><span data-stu-id="febcb-142">Select **After** to print after all invoices have been updated.</span></span>
    * <span data-ttu-id="febcb-143">Чтобы изменить порядок проверки кредитного лимита клиента перед разноской накладной, измените значение в поле **Тип кредитного лимита**.</span><span class="sxs-lookup"><span data-stu-id="febcb-143">To change how the customer's credit limit is verified before the invoice is posted, change the value in the **Credit limit type** field.</span></span>
    * <span data-ttu-id="febcb-144">Чтобы напечатать накладную, установите этот параметр в значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="febcb-144">To print the invoice, set the option to **Yes**.</span></span>
    * <span data-ttu-id="febcb-145">Чтобы разнести накладную, установите этот параметр в значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="febcb-145">To post the invoice, set the option to **Yes**.</span></span> <span data-ttu-id="febcb-146">Можно напечатать накладную без разноски.</span><span class="sxs-lookup"><span data-stu-id="febcb-146">You can print the invoice without posting it.</span></span>

19. <span data-ttu-id="febcb-147">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="febcb-147">Select **OK**.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="febcb-148">Копирование строк</span><span class="sxs-lookup"><span data-stu-id="febcb-148">Copy lines</span></span>
<span data-ttu-id="febcb-149">Для копирования строк в накладной с произвольным текстом выберите одну или несколько строк и выберите **Копировать выбранные строки**.</span><span class="sxs-lookup"><span data-stu-id="febcb-149">To copy lines on a free text invoice, select one or more lines, and then select **Copy selected lines**.</span></span> <span data-ttu-id="febcb-150">Можно указать количество копий, которые необходимо сделать, а также скопировать примечания и вложения.</span><span class="sxs-lookup"><span data-stu-id="febcb-150">You can specify the number of copies to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="febcb-151">Можно либо скопировать распределения, либо разрешить их повторное создание при разноске.</span><span class="sxs-lookup"><span data-stu-id="febcb-151">You can either copy the distributions or let them be re-created when you post.</span></span>

<span data-ttu-id="febcb-152">После копирования строк можно отредактировать информацию требуемым образом.</span><span class="sxs-lookup"><span data-stu-id="febcb-152">After you copy lines, you can edit the information as you require.</span></span>

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="febcb-153">Создание накладных с произвольным текстом из шаблона</span><span class="sxs-lookup"><span data-stu-id="febcb-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="febcb-154">Можно создать накладных с произвольным текстом из шаблона.</span><span class="sxs-lookup"><span data-stu-id="febcb-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="febcb-155">При выборе команды **Создать из шаблона** на вкладке **Накладная** можно выбрать имя шаблона и счет клиента для новой накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="febcb-155">When you select **New from template** on the **Invoice** tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="febcb-156">Значения по умолчанию, например условия оплаты и способ оплаты от клиента, могут автоматически быть подставлены из записи клиента, или же можно использовать значения, сохраненные в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="febcb-156">Default values, such as the terms of payment and method of payment, can be automatically filled in from the customer, or you can use the values that were saved in the template.</span></span>

<span data-ttu-id="febcb-157">Будет создана новая накладная с произвольным текстом, и вы сможете редактировать значения требуемым образом.</span><span class="sxs-lookup"><span data-stu-id="febcb-157">A new free text invoice is created, and you can edit the values as you require.</span></span>
