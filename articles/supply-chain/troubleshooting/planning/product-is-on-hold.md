---
title: Продукт заблокирован для проводок
description: После утверждения спланированных заказов вы получаете сообщение об ошибке с информацией, что номенклатура заблокирована для проводок.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301287"
---
# <a name="product-is-on-hold-for-transactions"></a><span data-ttu-id="ef6d9-103">Продукт заблокирован для проводок</span><span class="sxs-lookup"><span data-stu-id="ef6d9-103">Product is on hold for transactions</span></span>

<span data-ttu-id="ef6d9-104">Код ошибки: SYS13295</span><span class="sxs-lookup"><span data-stu-id="ef6d9-104">Error code: SYS13295</span></span>

## <a name="symptoms"></a><span data-ttu-id="ef6d9-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="ef6d9-105">Symptoms</span></span>

<span data-ttu-id="ef6d9-106">После того, как вы утвердили спланированные заказы, вы получите следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="ef6d9-106">After you firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="ef6d9-107">Номенклатура %1 заблокирована для проводок в %2.</span><span class="sxs-lookup"><span data-stu-id="ef6d9-107">Item %1 is on hold for transactions in %2.</span></span>

## <a name="cause"></a><span data-ttu-id="ef6d9-108">Причина</span><span class="sxs-lookup"><span data-stu-id="ef6d9-108">Cause</span></span>

<span data-ttu-id="ef6d9-109">При описании заблокированных номенклатур система использует термины *заблокировано*, *остановлено* и *на удержании* взаимозаменяемо.</span><span class="sxs-lookup"><span data-stu-id="ef6d9-109">When describing blocked items, system uses the terms *blocked*, *stopped*, and *on hold* interchangeably.</span></span> <span data-ttu-id="ef6d9-110">Эта ошибка означает, что номенклатура устанавливается как **Остановлено** в настройках заказа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ef6d9-110">This error means that the item is set as **Stopped** in its default order settings.</span></span>

<span data-ttu-id="ef6d9-111">Если номенклатура заблокирована и вы добавляете ее в строку заказа на покупку или заказа на продажу, вы получаете предупреждение.</span><span class="sxs-lookup"><span data-stu-id="ef6d9-111">If an item is blocked, and you add it to a purchase order or sales order line, you receive a warning message.</span></span> <span data-ttu-id="ef6d9-112">Когда номенклатура заблокирована, складские проводки, связанные со строкой заказа на покупку или продажу не могут быть изменены (например при разноске отборочной накладной или накладной).</span><span class="sxs-lookup"><span data-stu-id="ef6d9-112">When an item is blocked, inventory transactions that are related to the purchase order or sales order line can't be modified (for example, when you post a packing slip or an invoice).</span></span> <span data-ttu-id="ef6d9-113">Имеется возможность заблокировать купленную номенклатуру и одновременно продать эту номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="ef6d9-113">You can block a purchased item, and, at the same time, sell the item.</span></span> <span data-ttu-id="ef6d9-114">В этом случае флажок **Остановлено** выбран в заказе на покупку, но номенклатура не блокируется на складе, или в заказе на продажу.</span><span class="sxs-lookup"><span data-stu-id="ef6d9-114">In this case, the **Stopped** check box is selected on a purchase order, but the item isn't blocked in inventory or on a sales order.</span></span>

<span data-ttu-id="ef6d9-115">Вот некоторые из условий, которые могут привести к блокировке продажи кода номенклатуры:</span><span class="sxs-lookup"><span data-stu-id="ef6d9-115">Here are some of the conditions that can cause an item number to be blocked from being sold:</span></span>

- <span data-ttu-id="ef6d9-116">Номенклатура все еще находится в стадии разработки или производства.</span><span class="sxs-lookup"><span data-stu-id="ef6d9-116">The item is still under development or manufacture.</span></span> <span data-ttu-id="ef6d9-117">Таким образом, вы не хотите, чтобы она был продана или зарезервирована.</span><span class="sxs-lookup"><span data-stu-id="ef6d9-117">Therefore, you don't want it to be sold or reserved.</span></span>
- <span data-ttu-id="ef6d9-118">Вы получили много дефектных номенклатур, и дефекты должны быть исправлены, прежде чем номенклатура может быть продана.</span><span class="sxs-lookup"><span data-stu-id="ef6d9-118">You've received many defective items, and the defects must be corrected before the item can be sold.</span></span>

<span data-ttu-id="ef6d9-119">В случае такого типа можно заблокировать номенклатуру до тех пор, пока проблема не будет решена.</span><span class="sxs-lookup"><span data-stu-id="ef6d9-119">In cases of this type, you can block the item until the issue is resolved.</span></span>

<span data-ttu-id="ef6d9-120">Если номенклатура заблокирована и создается строка заказа на возврат, вы получаете сообщение.</span><span class="sxs-lookup"><span data-stu-id="ef6d9-120">If an item is blocked, and you create a return order line, you receive a message.</span></span> <span data-ttu-id="ef6d9-121">Невозможно заблокировать серию или лот номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="ef6d9-121">You can't block a series or a lot of an item.</span></span> <span data-ttu-id="ef6d9-122">Если необходимо блокировать часть номенклатуры, это можно сделать, переместив складские запасы или заблокировав полный запас для этого периода.</span><span class="sxs-lookup"><span data-stu-id="ef6d9-122">If parts of an item must be blocked, you can block them by moving inventory or by blocking the full stock of the item for that period.</span></span>

## <a name="resolution"></a><span data-ttu-id="ef6d9-123">Решение</span><span class="sxs-lookup"><span data-stu-id="ef6d9-123">Resolution</span></span>

- <span data-ttu-id="ef6d9-124">Откройте страницу **Параметры заказа по умолчанию** для номенклатуры и снимите флажок **Остановлено**.</span><span class="sxs-lookup"><span data-stu-id="ef6d9-124">Open the **Default order settings** page for the item, and clear the **Stopped** checkbox.</span></span>
