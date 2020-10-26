---
title: Прохождение возвратом процедуры проверки
description: Прохождение возвратом процедуры проверки.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bdc42f9c5ece8e2c2570cadf623f52648b7b174e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985799"
---
# <a name="take-returned-items-through-inspection"></a><span data-ttu-id="338e3-103">Прохождение возвратом процедуры проверки</span><span class="sxs-lookup"><span data-stu-id="338e3-103">Take returned items through inspection</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="338e3-104">Щелкните **Управление запасами** \> **Периодические операции** \> **Управление качеством** \> **Карантинные заказы**.</span><span class="sxs-lookup"><span data-stu-id="338e3-104">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="338e3-105">Найдите строку заказа, соответствующую возвращенной номенклатуре, которую вы осматриваете.</span><span class="sxs-lookup"><span data-stu-id="338e3-105">Locate the order line that corresponds to the returned item that you are inspecting.</span></span>

    > [!NOTE]
    > <P><span data-ttu-id="338e3-106">Карантинный заказ может быть связан просто с одним кодом номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="338e3-106">A quarantine order can be associated with just a single item number.</span></span> <span data-ttu-id="338e3-107">Если 10 номенклатур, имеющих разные коды номенклатур, возвращены в одну отгрузку и отправлены в карантин, 10 отдельных карантинных заказов созданы.</span><span class="sxs-lookup"><span data-stu-id="338e3-107">If 10 items that have different item numbers are returned in a single shipment and sent to quarantine, 10 individual quarantine orders are created.</span></span></P>

3.  <span data-ttu-id="338e3-108">После осмотра номенклатуры выберите значение в поле **Код метода обработки**, чтобы указать, что следует сделать с номенклатурой и как должна быть обработана соответствующая финансовая проводка.</span><span class="sxs-lookup"><span data-stu-id="338e3-108">After examining the item, make a selection in the **Disposition code** field to indicate what should be done with the item and how to handle the related financial transaction.</span></span> <span data-ttu-id="338e3-109">Примеры включают возвращение номенклатуры на склад с возвратом денег клиенту, утилизация номенклатуры с отправкой замены клиенту, или возврат номенклатуры клиенту без кредитования.</span><span class="sxs-lookup"><span data-stu-id="338e3-109">Examples include returning the item to stock and refunding the customer, scrapping the item and sending a replacement to the customer, or returning the item to the customer without credit.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="338e3-110">Если нескольким возвращенным номенклатурам в одной партии невозможно присвоить одинаковый код метода обработки, следует разделить карантинный заказ (<STRONG>Функции</STRONG> &gt; <STRONG>Разделить</STRONG>), чтобы назначить отдельный код метода обработки каждой подпартии.</span><span class="sxs-lookup"><span data-stu-id="338e3-110">If multiple returned items in a single item number batch cannot be assigned the same disposition code, you must split the quarantine order (<STRONG>Functions</STRONG> &gt; <STRONG>Split</STRONG>) to assign a different disposition code to each sub-batch.</span></span></P>


4.  <span data-ttu-id="338e3-111">Закончив осмотр, щелкните **Приемка**, чтобы выпустить возвращенные номенклатуры и создать запись в журнале поступления номенклатур.</span><span class="sxs-lookup"><span data-stu-id="338e3-111">When you are finished with the inspection, click **Report as finished** to release the returned items and create an item arrival journal entry.</span></span> <span data-ttu-id="338e3-112">Лицо или подразделение, которые получают номенклатуры, затем обрабатывают журнал для номенклатур, которые будут возвращены на склад.</span><span class="sxs-lookup"><span data-stu-id="338e3-112">The person or department that receives the items then processes the journal for the items to be returned to inventory.</span></span>
    
    <span data-ttu-id="338e3-113">–или–</span><span class="sxs-lookup"><span data-stu-id="338e3-113">–or–</span></span>
    
    <span data-ttu-id="338e3-114">Закройте карантинный заказ и переместите номенклатуры обратно на склад с помощью функций **Запасы**.</span><span class="sxs-lookup"><span data-stu-id="338e3-114">End the quarantine order, and move the items back into inventory directly by using one of the **Inventory** functions.</span></span>

5.  <span data-ttu-id="338e3-115">Закройте форму, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="338e3-115">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="338e3-116">См. также</span><span class="sxs-lookup"><span data-stu-id="338e3-116">See also</span></span>

[<span data-ttu-id="338e3-117">Определение порядка списания возврата</span><span class="sxs-lookup"><span data-stu-id="338e3-117">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

  


