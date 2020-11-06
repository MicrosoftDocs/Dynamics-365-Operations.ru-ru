---
title: Создание заказа на покупку для разового поставщика
description: В этой процедуре показано, как создать заказ на покупку для разового поставщика.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fc935b346adfe9548b024f22a2fbfb5af9a802d
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018106"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="67a1e-103">Создание заказа на покупку для разового поставщика</span><span class="sxs-lookup"><span data-stu-id="67a1e-103">Create a purchase order for a one-time supplier</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="67a1e-104">В этой процедуре показано, как создать заказ на покупку для разового поставщика.</span><span class="sxs-lookup"><span data-stu-id="67a1e-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="67a1e-105">Поставщик создается автоматически с заказом на покупку вместо того, чтобы создавать счет поставщика вручную.</span><span class="sxs-lookup"><span data-stu-id="67a1e-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="67a1e-106">Заказы на покупку обычно создаются специалистом по закупке.</span><span class="sxs-lookup"><span data-stu-id="67a1e-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="67a1e-107">Пример, представленный в этом руководстве, можно использовать в компании с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="67a1e-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="67a1e-108">В качестве предварительного требования следует настроить счет разового поставщика на странице "Параметры модуля расчетов с поставщиками".</span><span class="sxs-lookup"><span data-stu-id="67a1e-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="67a1e-109">Создание заказа на покупку для разового поставщика</span><span class="sxs-lookup"><span data-stu-id="67a1e-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="67a1e-110">Перейдите в раздел "Закупки и источники" > "Заказы на покупку" > "Все заказы на покупку".</span><span class="sxs-lookup"><span data-stu-id="67a1e-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="67a1e-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="67a1e-111">Click New.</span></span>
3. <span data-ttu-id="67a1e-112">Выберите значение "Да" в поле "Разовый поставщик".</span><span class="sxs-lookup"><span data-stu-id="67a1e-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="67a1e-113">Счет поставщика автоматически создается и назначается заказу на покупку.</span><span class="sxs-lookup"><span data-stu-id="67a1e-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="67a1e-114">Счет поставщика создается на основе шаблона, указанного на вкладке "Общее" на странице "Параметры модуля расчетов с поставщиками".</span><span class="sxs-lookup"><span data-stu-id="67a1e-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="67a1e-115">В поле "Имя" введите имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="67a1e-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="67a1e-116">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="67a1e-116">Click OK.</span></span>
    * <span data-ttu-id="67a1e-117">Заказ на покупку теперь можно завершить и обработать как любой другой заказ.</span><span class="sxs-lookup"><span data-stu-id="67a1e-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="67a1e-118">Не существует особых характеристик, связанных с тем, как это выполняется.</span><span class="sxs-lookup"><span data-stu-id="67a1e-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="67a1e-119">В накладной будет учитываться проводка к оплате в счете поставщика, который был создан с заказом, после чего будет обработан платеж.</span><span class="sxs-lookup"><span data-stu-id="67a1e-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span>

