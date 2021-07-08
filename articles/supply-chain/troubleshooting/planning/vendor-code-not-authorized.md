---
title: Код поставщика не авторизован для определенного продукта и даты
description: При попытке утверждения спланированного заказа или добавления строки в заказ на покупку будет выведено сообщение об ошибке, в котором говорится, что код поставщика не авторизован для продукта и даты.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294167"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a><span data-ttu-id="1dc26-103">Код поставщика не авторизован для определенного продукта и даты</span><span class="sxs-lookup"><span data-stu-id="1dc26-103">Vendor code isn't authorized for a specific product and date</span></span>

<span data-ttu-id="1dc26-104">Код ошибки: SYP4881415</span><span class="sxs-lookup"><span data-stu-id="1dc26-104">Error code: SYP4881415</span></span>

## <a name="symptoms"></a><span data-ttu-id="1dc26-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="1dc26-105">Symptoms</span></span>

<span data-ttu-id="1dc26-106">При попытке утвердить спланированный заказ или добавить строку в заказ на покупку выводится следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="1dc26-106">When you try to firm a planned order or add a line to a purchase order, you receive the following error message:</span></span>

> <span data-ttu-id="1dc26-107">Код поставщика %1 не разрешен для действия "%2" в %3.</span><span class="sxs-lookup"><span data-stu-id="1dc26-107">Vendor code %1 is not authorized for %2 on %3.</span></span>

## <a name="cause"></a><span data-ttu-id="1dc26-108">Причина</span><span class="sxs-lookup"><span data-stu-id="1dc26-108">Cause</span></span>

<span data-ttu-id="1dc26-109">Ошибка возникает из-за того поле **Способ проверки утвержденных поставщиков** имеет значение *Только предупреждение* или *Не разрешено* для указанного продукта, и поставщик не авторизован для поставки этого продукта в данный момент.</span><span class="sxs-lookup"><span data-stu-id="1dc26-109">The error occurs because the **Approved vendor check method** field is set to *Warning only* or *Not allowed* for the specified product, and the vendor isn't currently authorized to supply that product.</span></span>

## <a name="resolution"></a><span data-ttu-id="1dc26-110">Решение</span><span class="sxs-lookup"><span data-stu-id="1dc26-110">Resolution</span></span>

<span data-ttu-id="1dc26-111">Чтобы решить эту проблему, отключите проверку поставщика для соответствующего продукта или утвердите поставщика.</span><span class="sxs-lookup"><span data-stu-id="1dc26-111">To fix this issue, either disable the vendor check for the relevant product or approve the vendor.</span></span>

<span data-ttu-id="1dc26-112">Чтобы отключить проверку продукта для поставщика, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1dc26-112">To disable the vendor check for a product, follow these steps.</span></span>

1. <span data-ttu-id="1dc26-113">Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="1dc26-113">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="1dc26-114">Откройте соответствующий продукт.</span><span class="sxs-lookup"><span data-stu-id="1dc26-114">Open the relevant product.</span></span>
1. <span data-ttu-id="1dc26-115">На экспресс-вкладке **Покупка** задайте в поле **Способ проверки утвержденных поставщиков** значение, отличное от *Только предупреждение* или *Не разрешено*.</span><span class="sxs-lookup"><span data-stu-id="1dc26-115">On the **Purchase** FastTab, set the **Approved vendor check method** field to a value other than *Warning only* or *Not allowed*.</span></span>

<span data-ttu-id="1dc26-116">Чтобы утвердить поставщика для продукта, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1dc26-116">To approve a vendor for a product, follow these steps.</span></span>

1. <span data-ttu-id="1dc26-117">Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="1dc26-117">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="1dc26-118">Откройте соответствующую номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="1dc26-118">Open the relevant item.</span></span>
1. <span data-ttu-id="1dc26-119">В области действий на вкладке **Покупка** в группе **Утвержденный поставщик** выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="1dc26-119">On the Action Pane, on the **Purchase** tab, in the **Approved vendor** group, select **Setup**.</span></span>
1. <span data-ttu-id="1dc26-120">На странице списка **Утвержденный поставщик** добавьте строку в сетку и установите для нее следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1dc26-120">On the **Approved vendor** list page, add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="1dc26-121">**Поставщик** — выберите поставщика, которого необходимо утвердить для текущего продукта.</span><span class="sxs-lookup"><span data-stu-id="1dc26-121">**Vendor** – Select the vendor to approve for the current product.</span></span>
    - <span data-ttu-id="1dc26-122">**Дата вступления в силу** — выберите первую дату, для которой утвержден поставщик.</span><span class="sxs-lookup"><span data-stu-id="1dc26-122">**Effective date** – Select the first date that the vendor is approved for.</span></span>
    - <span data-ttu-id="1dc26-123">**Дата окончания срока действия** — выберите последнюю дату, для которой утвержден поставщик.</span><span class="sxs-lookup"><span data-stu-id="1dc26-123">**Expiration date** – Select the last date that the vendor is approved for.</span></span>

<span data-ttu-id="1dc26-124">Для дополнительной информации см. [Утверждение поставщиков для определенных продуктов](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span><span class="sxs-lookup"><span data-stu-id="1dc26-124">For more information, see [Approve vendors for specific products](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span></span>
