---
title: Создание заказа на покупку для разового поставщика
description: В этой процедуре показано, как создать заказ на покупку для разового поставщика.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: beaf6bcbc870e11e74289375611c631306545633
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547584"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="a15b1-103">Создание заказа на покупку для разового поставщика</span><span class="sxs-lookup"><span data-stu-id="a15b1-103">Create a purchase order for a one-time supplier</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a15b1-104">В этой процедуре показано, как создать заказ на покупку для разового поставщика.</span><span class="sxs-lookup"><span data-stu-id="a15b1-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="a15b1-105">Поставщик создается автоматически с заказом на покупку вместо того, чтобы создавать счет поставщика вручную.</span><span class="sxs-lookup"><span data-stu-id="a15b1-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="a15b1-106">Заказы на покупку обычно создаются специалистом по закупке.</span><span class="sxs-lookup"><span data-stu-id="a15b1-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="a15b1-107">Пример, представленный в этом руководстве, можно использовать в компании с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="a15b1-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="a15b1-108">В качестве предварительного требования следует настроить счет разового поставщика на странице "Параметры модуля расчетов с поставщиками".</span><span class="sxs-lookup"><span data-stu-id="a15b1-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="a15b1-109">Создание заказа на покупку для разового поставщика</span><span class="sxs-lookup"><span data-stu-id="a15b1-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="a15b1-110">Перейдите в раздел "Закупки и источники" > "Заказы на покупку" > "Все заказы на покупку".</span><span class="sxs-lookup"><span data-stu-id="a15b1-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="a15b1-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a15b1-111">Click New.</span></span>
3. <span data-ttu-id="a15b1-112">Выберите значение "Да" в поле "Разовый поставщик".</span><span class="sxs-lookup"><span data-stu-id="a15b1-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="a15b1-113">Счет поставщика автоматически создается и назначается заказу на покупку.</span><span class="sxs-lookup"><span data-stu-id="a15b1-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="a15b1-114">Счет поставщика создается на основе шаблона, указанного на вкладке "Общее" на странице "Параметры модуля расчетов с поставщиками".</span><span class="sxs-lookup"><span data-stu-id="a15b1-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="a15b1-115">В поле "Имя" введите имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="a15b1-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="a15b1-116">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a15b1-116">Click OK.</span></span>
    * <span data-ttu-id="a15b1-117">Заказ на покупку теперь можно завершить и обработать как любой другой заказ.</span><span class="sxs-lookup"><span data-stu-id="a15b1-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="a15b1-118">Не существует особых характеристик, связанных с тем, как это выполняется.</span><span class="sxs-lookup"><span data-stu-id="a15b1-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="a15b1-119">В накладной будет учитываться проводка к оплате в счете поставщика, который был создан с заказом, после чего будет обработан платеж.</span><span class="sxs-lookup"><span data-stu-id="a15b1-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span> <span data-ttu-id="a15b1-120">По завершении этого счет поставщика можно удалить.</span><span class="sxs-lookup"><span data-stu-id="a15b1-120">When this is completed, the vendor account can be deleted.</span></span> <span data-ttu-id="a15b1-121">Обычно эту операцию выполняет отдел по расчетам с поставщиками.</span><span class="sxs-lookup"><span data-stu-id="a15b1-121">This is typically done by the accounts payable department.</span></span>  

