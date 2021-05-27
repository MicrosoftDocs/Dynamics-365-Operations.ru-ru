---
title: Настройка сборов по платежам для платежей налоговому органу TDS
description: В этой теме объясняется, как настроить сборы по платежам, взимаемые для платежей органу по налогу, удержанному в источнике (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023553"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a><span data-ttu-id="188cf-103">Настройка сборов по платежам для платежей налоговому органу TDS</span><span class="sxs-lookup"><span data-stu-id="188cf-103">Set up payment fees for TDS authority payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="188cf-104">В этой теме объясняется, как настроить сборы по платежам, взимаемые для платежей органу по налогу, удержанному в источнике (TDS).</span><span class="sxs-lookup"><span data-stu-id="188cf-104">This topic explains how to set up payment fees that are charged for Tax Deducted at Source (TDS) authority payments.</span></span>

1. <span data-ttu-id="188cf-105">Перейдите в раздел **Расчеты с поставщиками \> Настройка платежей \> Сборы по платежам**.</span><span class="sxs-lookup"><span data-stu-id="188cf-105">Go to **Accounts payable \> Payment setup \> Payment fee**.</span></span>

    <span data-ttu-id="188cf-106">[![Страница сборов по платежам](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span><span class="sxs-lookup"><span data-stu-id="188cf-106">[![Payment fee page](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span></span>

2. <span data-ttu-id="188cf-107">Выберите **Создать**, чтобы создать сборы по платежам, затем введите нужные сведения.</span><span class="sxs-lookup"><span data-stu-id="188cf-107">Select **New** to create a payment fee, and enter the required details.</span></span>
3. <span data-ttu-id="188cf-108">В поле **Тип сбора** выберите тип сбора по платежу:</span><span class="sxs-lookup"><span data-stu-id="188cf-108">In the **Fee type** field, select the type of payment fee:</span></span>

    - <span data-ttu-id="188cf-109">**Не допускается**</span><span class="sxs-lookup"><span data-stu-id="188cf-109">**None**</span></span>
    - <span data-ttu-id="188cf-110">**Процент** — процент начисляется на просроченные платежи, сделанные поставщику налогового органа TDS.</span><span class="sxs-lookup"><span data-stu-id="188cf-110">**Interest** – Interest is charged on late payments that are made to the TDS authority vendor.</span></span>
    - <span data-ttu-id="188cf-111">**Прочие** — прочие расходы начисляются на просроченные платежи, сделанные поставщику налогового органа TDS.</span><span class="sxs-lookup"><span data-stu-id="188cf-111">**Others** – Other charges are charged on late payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="188cf-112">Если выбрано значение **Процент** или **Прочие**, поле **Расходы** автоматически устанавливается как **Главная книга**.</span><span class="sxs-lookup"><span data-stu-id="188cf-112">If you select **Interest** or **Others**, the **Charge** field is automatically set to **Ledger**.</span></span>

4. <span data-ttu-id="188cf-113">Если был выбран **Процент** или **Прочие** в поле **Тип поля**, в поле **Счет ГК** выберите счет главной книги, куда разносятся расходы по проценту или другие накладные расходы.</span><span class="sxs-lookup"><span data-stu-id="188cf-113">If you selected **Interest** or **Others** in the **Field type** field, in the **Main account** field, select the ledger account to post the interest or other charges to.</span></span>
5. <span data-ttu-id="188cf-114">Введите другие необходимые сведения.</span><span class="sxs-lookup"><span data-stu-id="188cf-114">Enter the other required details.</span></span>
6. <span data-ttu-id="188cf-115">На панели операций выберите **Настройка сборов по платежам**, чтобы открыть страницу **Настройка сборов по платежам**, на которой можно настроить сборы по платежам для различных комбинаций банков, способов оплаты, спецификаций оплаты, валют и интервалов дат.</span><span class="sxs-lookup"><span data-stu-id="188cf-115">On the Action Pane, select **Payment fee setup** to open the **Payment fee setup** page, where you can set up payment fees for various combinations of banks, methods of payment, payment specifications, currencies, and date intervals.</span></span>

    <span data-ttu-id="188cf-116">[![Страница настройки сборов по платежам](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span><span class="sxs-lookup"><span data-stu-id="188cf-116">[![Payment fee setup page](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span></span>

7. <span data-ttu-id="188cf-117">На вкладке **Обзор** в поле **Группировки** укажите, для каких банков выполняется настройка сборов по платежам:</span><span class="sxs-lookup"><span data-stu-id="188cf-117">On the **Overview** tab, in the **Groupings** field, specify which banks you're setting up the payment fee for:</span></span>

    - <span data-ttu-id="188cf-118">**Таблица** — сбор является действительным для конкретного банковского счета.</span><span class="sxs-lookup"><span data-stu-id="188cf-118">**Table** – The fee is valid for a specific bank account.</span></span>
    - <span data-ttu-id="188cf-119">**Группа** — сбор является действительным для конкретной банковской группы.</span><span class="sxs-lookup"><span data-stu-id="188cf-119">**Group** – The fee is valid for a specific bank group.</span></span>
    - <span data-ttu-id="188cf-120">**Все** — сбор является действительным для всех банковских счетов.</span><span class="sxs-lookup"><span data-stu-id="188cf-120">**All** – The fee is valid for all the bank accounts.</span></span>

8. <span data-ttu-id="188cf-121">Если выбрана **Таблица** или **Группа** в поле **Группировки**, в поле **Связь с банком** выберите специальный банковский счет или банковскую группу, для которой выполняется настройка сбора по платежам.</span><span class="sxs-lookup"><span data-stu-id="188cf-121">If you selected **Table** or **Group** in the **Groupings** field, in the **Bank relation** field, select the specific bank account or bank group that you're setting up the payment fee for.</span></span>
9. <span data-ttu-id="188cf-122">В поле **Способ оплаты** выберите способ оплаты сборов.</span><span class="sxs-lookup"><span data-stu-id="188cf-122">In the **Method of payment** field, select the method of payment for the payment of fees.</span></span>
10. <span data-ttu-id="188cf-123">В поле **Спецификация оплаты** выберите или введите код спецификации оплаты, созданный на странице **Спецификация оплаты**.</span><span class="sxs-lookup"><span data-stu-id="188cf-123">In the **Payment specification** field, select or enter the payment specification code that was generated on the **Payment specification** page.</span></span>
    - <span data-ttu-id="188cf-124">Спецификация оплаты используется при использовании электронного платежа как способа оплаты.</span><span class="sxs-lookup"><span data-stu-id="188cf-124">The Payment specification is used with electronic fund transfer methods of payment.</span></span>
12. <span data-ttu-id="188cf-125">В поле **Валюта оплаты** выберите валюту, которая активирует сбор.</span><span class="sxs-lookup"><span data-stu-id="188cf-125">In the **Payment currency** field, select the currency that activates the fee.</span></span> <span data-ttu-id="188cf-126">Активация сбора возможна только для проводок, использующих выбранную валюту.</span><span class="sxs-lookup"><span data-stu-id="188cf-126">Only transactions that use the selected currency can activate the fee.</span></span> <span data-ttu-id="188cf-127">Если вы оставляете это поле пустым, все валюты активизируют сборы.</span><span class="sxs-lookup"><span data-stu-id="188cf-127">If you leave this field blank, all currencies activate the fee.</span></span>
13. <span data-ttu-id="188cf-128">В поле **Процент/сумма** выберите метод расчета.</span><span class="sxs-lookup"><span data-stu-id="188cf-128">In the **Percentage/Amount** field, select the calculation method.</span></span> <span data-ttu-id="188cf-129">Возможные варианты — **Сумма**, **Процент** и **Интервал**.</span><span class="sxs-lookup"><span data-stu-id="188cf-129">The options are **Amount**, **Percent**, and **Interval**.</span></span>
14. <span data-ttu-id="188cf-130">В поле **Сумма сбора** укажите сумму сбора как процент от платежа или сумму для одного платежа.</span><span class="sxs-lookup"><span data-stu-id="188cf-130">In the **Fee amount** field, specify the fee amount as either a percentage of the payment or the amount for one payment.</span></span>
15. <span data-ttu-id="188cf-131">В поле **Валюта сбора** укажите код валюты сбора.</span><span class="sxs-lookup"><span data-stu-id="188cf-131">In the **Fee currency** field, specify the currency code for the fee.</span></span>
16. <span data-ttu-id="188cf-132">Перейдите на вкладку **Общее**, чтобы просмотреть или изменить сведения о выбранном банковском счете.</span><span class="sxs-lookup"><span data-stu-id="188cf-132">Select the **General** tab to view or modify the details for the selected bank account.</span></span>

    <span data-ttu-id="188cf-133">[![Вкладка "Общие"](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span><span class="sxs-lookup"><span data-stu-id="188cf-133">[![General tab](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span></span>

16. <span data-ttu-id="188cf-134">В поле **Минимум** введите минимальную сумму проводки, которая активирует сбор.</span><span class="sxs-lookup"><span data-stu-id="188cf-134">In the **Minimum** field, enter the minimum transaction amount that activates the fee.</span></span>
17. <span data-ttu-id="188cf-135">В поле **Максимум** введите максимальную сумму проводки, которая активирует сбор.</span><span class="sxs-lookup"><span data-stu-id="188cf-135">In the **Maximum** field, enter the maximum transaction amount that activates the fee.</span></span>
18. <span data-ttu-id="188cf-136">В полях **Начальная дата** и **Конечная дата** укажите диапазон дат для расчета сборов.</span><span class="sxs-lookup"><span data-stu-id="188cf-136">In the **From date** and **To date** fields, define a date range for calculating fees.</span></span>
19. <span data-ttu-id="188cf-137">В поле **Минимальный сбор** укажите сумму сбора как процент от платежа или сумму для одного платежа.</span><span class="sxs-lookup"><span data-stu-id="188cf-137">In the **Minimum fee** field, specify the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
20. <span data-ttu-id="188cf-138">В поле **Налоговая группа** выберите налоговую группу, которая будет использоваться для расчета налога для суммы сбора.</span><span class="sxs-lookup"><span data-stu-id="188cf-138">In the **Sales tax group** field, select the sales tax group to use to calculate the sales tax for the fee amount.</span></span>
21. <span data-ttu-id="188cf-139">В поле **Налоговая группа номенклатур** выберите налоговую группу номенклатур, которая будет использоваться для расчета налога номенклатуры для суммы сбора.</span><span class="sxs-lookup"><span data-stu-id="188cf-139">In the **Item sales tax group** field, select the item sales tax group to use to calculate the item sales tax for the fee amount.</span></span>
22. <span data-ttu-id="188cf-140">Выберите вкладку **Интервал**.</span><span class="sxs-lookup"><span data-stu-id="188cf-140">Select the **Interval** tab.</span></span> 

    <span data-ttu-id="188cf-141">[![Вкладка «Интервал»](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span><span class="sxs-lookup"><span data-stu-id="188cf-141">[![Interval tab](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span></span>

23. <span data-ttu-id="188cf-142">В поле **Дни** введите количество дней между датой разноски (датой скидки) оплаты и датой выполнения простого векселя.</span><span class="sxs-lookup"><span data-stu-id="188cf-142">In the **Days** field, enter the number of days between the posting date (discounting date) of the payment and the due date of the promissory note.</span></span>
24. <span data-ttu-id="188cf-143">В поле **Процент/сумма** выберите, является ли спецификация процентом или установленной суммой.</span><span class="sxs-lookup"><span data-stu-id="188cf-143">In the **Percentage/Amount** field, select whether the specification is a percentage or a set amount.</span></span>
25. <span data-ttu-id="188cf-144">В поле **Сумма сбора** введите сумму сбора как процент от платежа или сумму для одного платежа.</span><span class="sxs-lookup"><span data-stu-id="188cf-144">In the **Fee amount** field, enter the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
26. <span data-ttu-id="188cf-145">Закройте страницу **Настройка сборов по платежам**.</span><span class="sxs-lookup"><span data-stu-id="188cf-145">Close the **Payment fee setup** page.</span></span>
27. <span data-ttu-id="188cf-146">Закройте страницу **Сборы по платежам**.</span><span class="sxs-lookup"><span data-stu-id="188cf-146">Close the **Payment fee** page.</span></span>
