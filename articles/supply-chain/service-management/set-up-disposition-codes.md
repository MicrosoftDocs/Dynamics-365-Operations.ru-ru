---
title: Настройка кодов метода обработки
description: Можно настроить коды расстановки для определения способа обработки номенклатуры, которая возвращена клиентом.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReturnDispositionCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5049c6d1fc5fcfae3bb6c7da1dd8d078ce9c33e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835782"
---
# <a name="set-up-disposition-codes"></a><span data-ttu-id="d6189-103">Настройка кодов метода обработки</span><span class="sxs-lookup"><span data-stu-id="d6189-103">Set up disposition codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d6189-104">Можно настроить коды расстановки для определения способа обработки номенклатуры, которая возвращена клиентом.</span><span class="sxs-lookup"><span data-stu-id="d6189-104">You can set up disposition codes to specify how to process an item that is returned by a customer.</span></span> <span data-ttu-id="d6189-105">Например, создайте код расстановки под названием **Ремонт и возврат**, чтобы указать, что возвращенная номенклатура будет отремонтирована, а затем будет возвращена клиенту.</span><span class="sxs-lookup"><span data-stu-id="d6189-105">For example, create a disposition code named **Repair and return** to indicate that the returned item will be repaired and then returned to the customer.</span></span> <span data-ttu-id="d6189-106">Дополнительные примеры кодов расстановки, которые обычно используются для возвращаемых клиентами номенклатур см. в разделе [Определение порядка списания возврата](specify-how-to-dispose-of-returned-items.md).</span><span class="sxs-lookup"><span data-stu-id="d6189-106">For more examples of disposition codes that are typically used for items that are returned by customers, see [Specify how to dispose of returned items](specify-how-to-dispose-of-returned-items.md).</span></span>

<span data-ttu-id="d6189-107">Можно также настроить код причины, чтобы объяснить причину почему номенклатура была возвращена.</span><span class="sxs-lookup"><span data-stu-id="d6189-107">You can also set up a reason code to help explain why an item was returned.</span></span> <span data-ttu-id="d6189-108">Для получения дополнительных сведений о кодах причин см. раздел [Настройка кодов причин возврата](set-up-return-reason-code.md).</span><span class="sxs-lookup"><span data-stu-id="d6189-108">For more information about reason codes, see [Set up return reason codes](set-up-return-reason-code.md).</span></span>

1.  <span data-ttu-id="d6189-109">Перейдите **Продажи и маркетинг** \> **Настройка** \> **Заказы на продажу** \> **Возвраты** \> **Коды метода обработки**.</span><span class="sxs-lookup"><span data-stu-id="d6189-109">Go to **Sales and marketing** \> **Setup** \> **Sales orders** \> **Returns** \> **Disposition codes**.</span></span>

2.  <span data-ttu-id="d6189-110">Выберите **Создать** для создания нового кода метода обработки.</span><span class="sxs-lookup"><span data-stu-id="d6189-110">Select **New** to create a new disposition code.</span></span>

3.  <span data-ttu-id="d6189-111">Введите уникальное описательное имя, выберите действие и введите описание для кода расстановки.</span><span class="sxs-lookup"><span data-stu-id="d6189-111">Enter a unique, descriptive name, select an action, and enter a description for the disposition code.</span></span>

4.  <span data-ttu-id="d6189-112">Если необходимо связать какую-либо оплату клиентом с данным кодом расстановки, выберите **Накладные расходы**, чтобы открыть форму **Настройка накладных расходов**.</span><span class="sxs-lookup"><span data-stu-id="d6189-112">If you want to associate any customer charges with this disposition code, select the **Charges** button to open the **Set up charges** form.</span></span>

5.  <span data-ttu-id="d6189-113">Если необходимо определить соответствие каких-либо внешних кодов собственным кодам методов обработки компании, выберите **Внешние коды**, чтобы открыть форму **Внешние коды**.</span><span class="sxs-lookup"><span data-stu-id="d6189-113">If you want to define any external codes to match with the company's own disposition codes, select the **External codes** button to open the **External codes** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6189-114">См. также</span><span class="sxs-lookup"><span data-stu-id="d6189-114">See also</span></span>

[<span data-ttu-id="d6189-115">Обзор возвратов клиентами</span><span class="sxs-lookup"><span data-stu-id="d6189-115">Customer returns overview</span></span>](disposition-and-return-reason-codes.md)

<span data-ttu-id="d6189-116">[Коды методов обработки (форма)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="d6189-116">[Disposition codes (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span></span>

<span data-ttu-id="d6189-117">[Автоматические затраты (форма)](https://technet.microsoft.com/library/aa582856\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="d6189-117">[Auto charges (form)](https://technet.microsoft.com/library/aa582856\(v=ax.60\))</span></span>

<span data-ttu-id="d6189-118">[Форма "Внешние коды" (форма)](https://technet.microsoft.com/library/aa583814\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="d6189-118">[External codes (form)](https://technet.microsoft.com/library/aa583814\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]