---
title: Обновления отборочной накладной для возвратов
description: Перед тем как можно будет зарегистрировать приход возврата на склад, необходимо обновить отборочную накладную того заказа, к которому принадлежат возвращаемые номенклатуры.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7f5bf5adb603d7edb40960b70cb71e25a2f0456
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983875"
---
# <a name="packing-slip-updates-for-returns"></a><span data-ttu-id="9d716-103">Обновления отборочной накладной для возвратов</span><span class="sxs-lookup"><span data-stu-id="9d716-103">Packing slip updates for returns</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="9d716-104">Перед тем как можно будет зарегистрировать приход возврата на склад, необходимо обновить отборочную накладную того заказа, к которому принадлежат возвращаемые номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="9d716-104">Before returned items can be received into inventory, the packing slip for the order to which they belong must be updated.</span></span> <span data-ttu-id="9d716-105">Процесс обновления финансовых проводок схож с процессом обновления накладных, а процесс обновления отборочных накладных — это физическое обновление записи о запасах, в результате которого вносятся изменения в сведения о запасах.</span><span class="sxs-lookup"><span data-stu-id="9d716-105">Just as the invoice update process is the update to the financial transaction, the packing slip update process is the physical update of the inventory record, which means that it commits the changes to inventory.</span></span> <span data-ttu-id="9d716-106">В случае возврата шаги, назначенные действию расположения, выполняются на этапе обновления отборочной накладной.</span><span class="sxs-lookup"><span data-stu-id="9d716-106">In the case of returns, the steps that are assigned to the disposition action are implemented during the packing slip update.</span></span>

<span data-ttu-id="9d716-107">Обработка обновления отборочной накладной может производиться либо в журнале прибытия номенклатур, либо в заказе на возврат.</span><span class="sxs-lookup"><span data-stu-id="9d716-107">The packing slip update can be processed in either the item arrival journal or the return order.</span></span>

<span data-ttu-id="9d716-108">В процессе разноски отборочных накладных ссылочный номер отборочной накладной из отгрузочной документации клиента можно связать с другими строками заказа.</span><span class="sxs-lookup"><span data-stu-id="9d716-108">As part of the process for posting packing slips, the packing slip reference number from the customer’s shipping documents can be associated with the order lines.</span></span> <span data-ttu-id="9d716-109">Эта связь не является обязательной и используется только в справочных целях.</span><span class="sxs-lookup"><span data-stu-id="9d716-109">This association is optional and for reference only.</span></span> <span data-ttu-id="9d716-110">Она не создает никаких обновлений проводок.</span><span class="sxs-lookup"><span data-stu-id="9d716-110">It does not create any transactional updates.</span></span>

<span data-ttu-id="9d716-111">Если прибыли не все из ожидаемых возвращаемых номенклатур, необходимо включить в обновление отборочной накладной только принятое количество.</span><span class="sxs-lookup"><span data-stu-id="9d716-111">If not all of the expected return items have arrived, you should include only the quantity that has been received in the packing slip update.</span></span> <span data-ttu-id="9d716-112">Остальные номенклатуры оставьте в заказе до тех пор, пока не будут получены остальные части отгрузки возврата.</span><span class="sxs-lookup"><span data-stu-id="9d716-112">Leave the remaining items on the order until the rest of the return shipment has arrived.</span></span>

<span data-ttu-id="9d716-113">Если номенклатура из карантина отправляется в отдел отгрузки и приемки, например если инспектор по карантину не знает, где сохранить номенклатуру в запасах, соответствующую отборочную накладную необходимо обновить, чтобы правильно зарегистрировать ее и использовать код местоположения, указанный в результате размещения на карантин.</span><span class="sxs-lookup"><span data-stu-id="9d716-113">If an item is sent back from quarantine to the Shipping and Receiving department, such as when the quarantine inspector does not know where to store the item in inventory, the corresponding packing slip must be updated to correctly register and act on the disposition code that is specified as a result of the quarantine.</span></span>

<span data-ttu-id="9d716-114">При обновлении отборочной накладной для возвращенной номенклатуры из договора продажи, обязательство по договору продажи в отношении данной номенклатуры автоматически обновляется, отражая изменение количества или объема товара.</span><span class="sxs-lookup"><span data-stu-id="9d716-114">When you update a packing slip for a returned item that is from a sales agreement, the sales agreement commitment for that item is automatically updated to reflect the change in the quantity or the amount.</span></span> 

## <a name="see-also"></a><span data-ttu-id="9d716-115">См. также</span><span class="sxs-lookup"><span data-stu-id="9d716-115">See also</span></span>

[<span data-ttu-id="9d716-116">Выполнение обновлений накладной для возвратов</span><span class="sxs-lookup"><span data-stu-id="9d716-116">Perform invoice updates for returns</span></span>](perform-invoice-updates-for-returns.md)

  


