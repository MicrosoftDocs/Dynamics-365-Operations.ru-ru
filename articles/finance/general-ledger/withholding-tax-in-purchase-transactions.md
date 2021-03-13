---
title: Подоходный налог в проводках по покупкам
description: Для поставщиков, которые облагаются подоходным налогом, можно назначить **Группу подоходного налога** по умолчанию на странице **Все поставщики**.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 06997e2d6b47d867e014a7d493d91015c78a5e04
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060784"
---
# <a name="withholding-tax-in-purchase-transactions"></a><span data-ttu-id="5be09-103">Подоходный налог в проводках по покупкам</span><span class="sxs-lookup"><span data-stu-id="5be09-103">Withholding tax in purchase transactions</span></span>

<span data-ttu-id="5be09-104">Для поставщиков, которые облагаются подоходным налогом, можно назначить **Группу подоходного налога** по умолчанию на странице **Все поставщики**.</span><span class="sxs-lookup"><span data-stu-id="5be09-104">For vendors who are liable to withholding tax, you can assign the default **Withholding tax group** on the **All vendors** page.</span></span>

1. <span data-ttu-id="5be09-105">Перейдите в раздел **Область перехода > Модули > Расчеты с поставщиками > Поставщики > Все поставщики**.</span><span class="sxs-lookup"><span data-stu-id="5be09-105">Go to **Navigation pane > Modules > Accounts payable > Vendors > All vendors**.</span></span>

2. <span data-ttu-id="5be09-106">Щелкните соответствующий счет поставщика, щелкните **Правка**.</span><span class="sxs-lookup"><span data-stu-id="5be09-106">Click the respective Vendor account, click **Edit**.</span></span>

3. <span data-ttu-id="5be09-107">На вкладке **Накладная и поставка** установите в поле **Рассчитать подоходный налог** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="5be09-107">In **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="5be09-108">Подоходный налог не будет рассчитываться, если поле **Рассчитать подоходный налог** не включено для этого поставщика в данных.</span><span class="sxs-lookup"><span data-stu-id="5be09-108">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this vendor in the data.</span></span>

4. <span data-ttu-id="5be09-109">Выберите группу подоходного налога в поле **Группа подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="5be09-109">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="5be09-110">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="5be09-110">Click **Save**.</span></span>

<span data-ttu-id="5be09-111">Для номенклатур/услуг, облагаемых подоходным налогом, можно назначить значение по умолчанию в поле **Группа подоходного налога для номенклатуры** в разделе **Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="5be09-111">For items/services which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="5be09-112">Перейдите в раздел **Область переходов > Модули > Управление сведениями о продукте > Продукты > Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="5be09-112">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="5be09-113">Щелкните соответствующий номер номенклатуры, щелкните **Правка**.</span><span class="sxs-lookup"><span data-stu-id="5be09-113">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="5be09-114">На вкладке **Покупка** щелкните **Рассчитать подоходный налог**.</span><span class="sxs-lookup"><span data-stu-id="5be09-114">In **Purchase** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="5be09-115">Подоходный налог не будет рассчитываться, если в поле **Рассчитать подоходный налог** не установлено значение **Да** для этой номенклатуры на вкладке **Покупка** на странице **Выпущенный продукт**.</span><span class="sxs-lookup"><span data-stu-id="5be09-115">Withholding tax will not be calculated if **Calculate withholding tax** isn't set to **Yes** for this Item in the **Purchase** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="5be09-116">Выберите группу подоходного налога для номенклатуры в списке **Группа подоходного налога для номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="5be09-116">Select an item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="5be09-117">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="5be09-117">Click **Save**.</span></span>

<span data-ttu-id="5be09-118">Группы подоходного налога и группы подоходного налога для номенклатур могут быть назначены на страницах:</span><span class="sxs-lookup"><span data-stu-id="5be09-118">Withholding tax groups and Item withholding tax groups can be assigned in pages:</span></span> 

- <span data-ttu-id="5be09-119">**Заказ на покупку**</span><span class="sxs-lookup"><span data-stu-id="5be09-119">**Purchase order**</span></span>
- <span data-ttu-id="5be09-120">**Накладная поставщика**</span><span class="sxs-lookup"><span data-stu-id="5be09-120">**Vendor invoice**</span></span>
- <span data-ttu-id="5be09-121">**Журнал накладных**</span><span class="sxs-lookup"><span data-stu-id="5be09-121">**Invoice journal**</span></span>

<span data-ttu-id="5be09-122">Группа подоходного налога и группа подоходного налога для номенклатуры по умолчанию будут перенесены в строки при создании **Заказов на покупку** и/или **Ожидающих накладных поставщиков**.</span><span class="sxs-lookup"><span data-stu-id="5be09-122">The default Withholding tax group and Item withholding tax group will be carried into the lines when creating **Purchase orders** and/or **Pending Vendor invoices**.</span></span> <span data-ttu-id="5be09-123">Для **журнала накладных поставщиков** можно переключаться на **Рассчитать подоходный налог** и выбирать **Группа подоходного налога для номенклатуры** на вкладке **Общие** в журнале.</span><span class="sxs-lookup"><span data-stu-id="5be09-123">For **Vendor invoice journal**, you can switch on **Calculate withholding tax** and select **Item withholding tax group** in the **General** tab in the journal.</span></span>

<span data-ttu-id="5be09-124">Временная сумма подоходного налога доступна в поле **Скорректированный подоходный налог** на вкладке **Итоги** на странице **Заказ на покупку**.</span><span class="sxs-lookup"><span data-stu-id="5be09-124">The temporary amount of withholding tax is available in the field **Adjusted withholding tax** of the **Totals** tab on the **Purchase order** page.</span></span>

![Подоходный налог включается в заказ на покупку](media/withholding-tax-adjusted.png)

<span data-ttu-id="5be09-126">Подоходный налог рассчитывается в пункте **Журнал платежей поставщикам**.</span><span class="sxs-lookup"><span data-stu-id="5be09-126">Withholding tax is calculated on **Vendor payment journal**.</span></span> <span data-ttu-id="5be09-127">Можно вручную скорректировать соответствующие коды подоходного налога, а также фактические суммы подоходного налога на вкладке **Подоходный налог** на странице **Сопоставление проводок**.</span><span class="sxs-lookup"><span data-stu-id="5be09-127">You can manually adjust the applicable withholding tax codes as well as the actual withholding tax amounts in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

![Удержание может быть скорректировано вручную на странице сопоставления проводок](media/withholding-tax-vendor-payment-tab.png)

<span data-ttu-id="5be09-129">Расчетная сумма подоходного налога будет вычтена из платежа поставщику и разнесена на **Счет подоходного налога** в соответствующей операции.</span><span class="sxs-lookup"><span data-stu-id="5be09-129">The derived withholding tax amount will be deducted from the vendor payment and posted to the **Withholding tax account** in a related voucher.</span></span>

![Счет подоходного налога, показывающий соответствующую операцию](media/withholding-tax-adjusted.png)
