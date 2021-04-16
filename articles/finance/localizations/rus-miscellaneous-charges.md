---
title: Распределение накладных расходов пропорционально весу и объему
description: В этом разделе приводятся сведения о распределении накладных расходов.
author: v-nadyuz
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: kfend
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a7b3a8d32f1994092a88a45f984e369534f0890b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836837"
---
# <a name="allocation-of-miscellaneous-charges-in-proportion-to-weight-and-volume"></a><span data-ttu-id="3a00b-103">Распределение накладных расходов пропорционально весу и объему</span><span class="sxs-lookup"><span data-stu-id="3a00b-103">Allocation of miscellaneous charges in proportion to weight and volume</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a00b-104">Накладные расходы могут быть распределены по затратам на товары, работы или услуги, которые приобретены или проданы.</span><span class="sxs-lookup"><span data-stu-id="3a00b-104">Miscellaneous charges can be allocated to the cost of goods, either works or services, that are purchased or sold.</span></span> <span data-ttu-id="3a00b-105">Русская локализация включает два дополнительных метода для распределения накладных расходов:</span><span class="sxs-lookup"><span data-stu-id="3a00b-105">Russian localization has two additional methods to allocate charges:</span></span>

- <span data-ttu-id="3a00b-106">**В соответствии с весом брутто** — расходы распределяются поровну в соответствии с весом брутто полученных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="3a00b-106">**According to the gross weight** – Charges are allocated equally, according to the gross weight of the items that are received.</span></span> <span data-ttu-id="3a00b-107">Эта сумма равна количеству в складской проводке, умноженному на поле **Вес брутто** из карточки складируемой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3a00b-107">This amount is equal to the quantity in the inventory transaction multiplied by the **Gross weight** field from the inventory item card.</span></span>
- <span data-ttu-id="3a00b-108">**В соответствии с объемом** — расходы распределяются поровну в соответствии с объемом полученных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="3a00b-108">**According to the volume** – Charges are allocated equally, according to the volume of the items that are received.</span></span> <span data-ttu-id="3a00b-109">Эта сумма равна количеству в складской проводке, умноженному на поле **Объем** из карточки складируемой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3a00b-109">This amount is equal to the quantity in the inventory transaction multiplied by the **Volume** field from the inventory item card.</span></span>

## <a name="allocate-charges-according-to-weight-or-volume-of-goods"></a><span data-ttu-id="3a00b-110">Распределение накладных расходов по весу или объему товаров</span><span class="sxs-lookup"><span data-stu-id="3a00b-110">Allocate charges according to weight or volume of goods</span></span>

1. <span data-ttu-id="3a00b-111">Выберите **Расчеты с поставщиками \> Заказы на покупку \> Все заказы на покупку** или **Расчеты с клиентами \> Заказы \>Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="3a00b-111">Select **Accounts payable \> Purchase orders \> All purchase orders** or **Accounts receivable \> Orders \> All sales orders.**</span></span>
2. <span data-ttu-id="3a00b-112">Создать новый заказ.</span><span class="sxs-lookup"><span data-stu-id="3a00b-112">Create a new order.</span></span>
3. <span data-ttu-id="3a00b-113">В поле **Распределение накладных расходов** выберите один из новых методов распределения:</span><span class="sxs-lookup"><span data-stu-id="3a00b-113">In the **Charges allocation** field, select one of the new allocation methods:</span></span>

    - <span data-ttu-id="3a00b-114">**Вес брутто:** распределение расходов в соответствии с весом брутто.</span><span class="sxs-lookup"><span data-stu-id="3a00b-114">**Gross weight:** Allocate charges according to the gross weight.</span></span>
    - <span data-ttu-id="3a00b-115">**Объем:** распределение расходов в соответствии с объемом.</span><span class="sxs-lookup"><span data-stu-id="3a00b-115">**Volume:** Allocate charges according to the volume.</span></span>

4. <span data-ttu-id="3a00b-116">Укажите другие сведения и разнесите заказ на продажу как обычно.</span><span class="sxs-lookup"><span data-stu-id="3a00b-116">Specify other details and post the sales order as usual.</span></span>

## <a name="allocate-charges-according-to-weight-and-volume-of-goods-during-facture-creation"></a><span data-ttu-id="3a00b-117">Распределять расходы в соответствии с весом и объемом товаров при создании счета-фактуры</span><span class="sxs-lookup"><span data-stu-id="3a00b-117">Allocate charges according to weight and volume of goods during facture creation</span></span>

1. <span data-ttu-id="3a00b-118">Выберите **Расчеты с поставщиками \> Заказы на покупку \> Все заказы на покупку** или **Расчеты с клиентами \> Заказы \>Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="3a00b-118">Select **Accounts payable \> Purchase orders \> All purchase orders** or **Accounts receivable \> Orders \> All sales orders**.</span></span>
2. <span data-ttu-id="3a00b-119">Создайте новый заказ, а затем выберите **обновить счет-фактуру**.</span><span class="sxs-lookup"><span data-stu-id="3a00b-119">Create a new order, and then select **Update facture**.</span></span>
3. <span data-ttu-id="3a00b-120">На странице **обновить счет-фактуру** можно управлять накладными расходами одним из двух способов:</span><span class="sxs-lookup"><span data-stu-id="3a00b-120">On the **Update facture** page, you can maintain the charges in one of two ways:</span></span>

    - <span data-ttu-id="3a00b-121">в области действий выберите вкладку **Финансы** **\> Ведение накладных расходов \> Ведение накладных расходов**.</span><span class="sxs-lookup"><span data-stu-id="3a00b-121">On the Action Pane, select the **Financials** tab **\> Maintain charges \> Maintain charges**.</span></span> <span data-ttu-id="3a00b-122">Накладные расходы, созданные таким образом, распределяются между всеми строками заказа в соответствии с методом распределения.</span><span class="sxs-lookup"><span data-stu-id="3a00b-122">Charges created in this way will be allocated between all the order lines according to the allocation method.</span></span>
    - <span data-ttu-id="3a00b-123">На экспресс-вкладке **Строки** выберите строку, в которой будут распределяться накладные расходы, а затем выберите **финансы \> Ведение накладных расходов** чтобы поддерживать накладные расходы в строке.</span><span class="sxs-lookup"><span data-stu-id="3a00b-123">On the **Lines** FastTab, select the line on which the charges will be allocated, and then select **Financials \> Maintain charges** to maintain miscellaneous charges on the line.</span></span>

![Настройка накладных расходов в строке](media/1%20Update%20facture.png)

4. <span data-ttu-id="3a00b-125">в области действий выберите вкладку **Финансы** **\> Ведение накладных расходов \> Распределить накладные расходы** чтобы распределить накладные расходы.</span><span class="sxs-lookup"><span data-stu-id="3a00b-125">On the Action Pane, select the **Financials** tab **\> Maintain charges \> Allocate charges** to allocate charges.</span></span>
5. <span data-ttu-id="3a00b-126">На странице **Распределить накладные расходы** в поле **Распределение накладных расходов** выберите один из новых методов распределения: **вес брутто** или **объем**.</span><span class="sxs-lookup"><span data-stu-id="3a00b-126">On the **Allocate charges** page, in the **Charges allocation** field, select one of the new allocation methods: **Gross weight** or **Volume**.</span></span>

![Страница Распределить накладные расходы](media/2%20Allocate%20charges.png)

6. <span data-ttu-id="3a00b-128">Укажите другие сведения и разнесите счет-фактуру как обычно.</span><span class="sxs-lookup"><span data-stu-id="3a00b-128">Specify other details and post the facture as usual.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]