---
title: Подоходный налог в проводках по продажам
description: В этом разделе перечислены шаги, которые необходимо выполнить, чтобы исключить расчет подоходного налога для выбранных клиентов. Для клиентов, которые указывают в своих платежах вам подоходный налог, можно назначить группу подоходного налога по умолчанию.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8e11ce10faa9b450b6f36a856b34b06b4ee1838d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842352"
---
# <a name="withholding-tax-in-sales-transactions"></a><span data-ttu-id="f641a-104">Подоходный налог в проводках по продажам</span><span class="sxs-lookup"><span data-stu-id="f641a-104">Withholding tax in sales transactions</span></span>

<span data-ttu-id="f641a-105">В этом разделе перечислены шаги, которые необходимо выполнить, чтобы исключить расчет подоходного налога для выбранных клиентов.</span><span class="sxs-lookup"><span data-stu-id="f641a-105">This topic lists the steps for avoiding the calculation of withholding tax for selected customers.</span></span> <span data-ttu-id="f641a-106">Для клиентов, которые указывают в своих платежах вам подоходный налог, можно назначить параметр **Группа подоходного налога** по умолчанию на странице **Клиенты**.</span><span class="sxs-lookup"><span data-stu-id="f641a-106">For customers who specify withholding tax in their payments to you, you can assign the default **Withholding tax group** on the **Customers** page.</span></span> 

1. <span data-ttu-id="f641a-107">Перейдите в раздел **Область перехода > Модули > Расчеты с клиентами > Клиенты > Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="f641a-107">Go to **Navigation pane > Modules > Accounts receivable > Customers > All customers**.</span></span>

2. <span data-ttu-id="f641a-108">Щелкните соответствующий счет клиента, щелкните **Правка**.</span><span class="sxs-lookup"><span data-stu-id="f641a-108">Click the respective customer account, click **Edit**.</span></span>

3. <span data-ttu-id="f641a-109">На вкладке **Накладная и поставка** установите в поле **Рассчитать подоходный налог** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="f641a-109">In the **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="f641a-110">Подоходный налог не будет рассчитываться, если поле **Рассчитать подоходный налог** не включено для этого клиента в справочнике.</span><span class="sxs-lookup"><span data-stu-id="f641a-110">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this customer in the master data.</span></span>

4. <span data-ttu-id="f641a-111">Выберите группу подоходного налога в поле **Группа подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="f641a-111">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="f641a-112">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f641a-112">Click **Save**.</span></span>

<span data-ttu-id="f641a-113">Для номенклатур/услуг, облагаемых подоходным налогом, можно назначить значение по умолчанию в поле **Группа подоходного налога для номенклатуры** в разделе **Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="f641a-113">For items/services, which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="f641a-114">Перейдите в раздел **Область переходов > Модули > Управление сведениями о продукте > Продукты > Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="f641a-114">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="f641a-115">Щелкните соответствующий номер номенклатуры, щелкните **Правка**.</span><span class="sxs-lookup"><span data-stu-id="f641a-115">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="f641a-116">На вкладке **Продажа** щелкните **Рассчитать подоходный налог**.</span><span class="sxs-lookup"><span data-stu-id="f641a-116">In the **Sell** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="f641a-117">Подоходный налог не будет рассчитываться, если в поле **Рассчитать подоходный налог** не установлено значение **Да** для этой номенклатуры на вкладке **Продажа** на странице **Выпущенный продукт**.</span><span class="sxs-lookup"><span data-stu-id="f641a-117">Withholding tax will not be calculated if **Calculate withholding tax** is not set to **Yes** for this Item in the **Sell** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="f641a-118">Выберите группу подоходного налога для номенклатуры в списке **Группа подоходного налога для номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="f641a-118">Select an Item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="f641a-119">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f641a-119">Click **Save**.</span></span>

<span data-ttu-id="f641a-120">Группы подоходного налога и группы подоходного налога для номенклатур могут быть назначены с помощью страницы **Заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="f641a-120">Withholding tax groups and Item withholding tax groups can be assigned using the **Sales order** page.</span></span> 

<span data-ttu-id="f641a-121">Группа подоходного налога по умолчанию и группа подоходного налога для номенклатуры будут использоваться в качестве записей по умолчанию в строках заказа на продажу при создании нового заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="f641a-121">The default Withholding tax group and Item withholding tax group will be used as default entries on sales order lines when you create a new sales order.</span></span>

<span data-ttu-id="f641a-122">Подоходный налог рассчитывается и разносится с помощью **Журнала платежей клиентов**.</span><span class="sxs-lookup"><span data-stu-id="f641a-122">Withholding tax is calculated and posted with **Customer payment journal**.</span></span> <span data-ttu-id="f641a-123">Можно вручную скорректировать соответствующий код подоходного налога, а также фактическую сумму подоходного налога на вкладке **Подоходный налог** на странице **Сопоставление проводок**.</span><span class="sxs-lookup"><span data-stu-id="f641a-123">You can manually adjust the applicable withholding tax code, as well as the actual withholding tax amount in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

<span data-ttu-id="f641a-124">Расчетная сумма подоходного налога будет вычтена из платежа клиента и разнесена на **Корреспондирующий счет подоходного налога** в соответствующей операции.</span><span class="sxs-lookup"><span data-stu-id="f641a-124">The calculated withholding tax amount will be deducted from the customer payment and posted to the **Withholding tax offset** account in a related voucher.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]