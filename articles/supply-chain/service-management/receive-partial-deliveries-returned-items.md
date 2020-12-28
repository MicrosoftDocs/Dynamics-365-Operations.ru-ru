---
title: Получение частичных поставок возврата
description: Частичные поставки определяются в терминах строк заказа на возврат, а не отгрузок по заказам на возврат.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf35169d8afd6e88b8ebe921514ed6d55607a4dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4435785"
---
# <a name="receive-partial-deliveries-of-returned-items"></a><span data-ttu-id="b87d7-103">Получение частичных поставок возврата</span><span class="sxs-lookup"><span data-stu-id="b87d7-103">Receive partial deliveries of returned items</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b87d7-104">Частичные поставки определяются в терминах строк заказа на возврат, а не отгрузок по заказам на возврат.</span><span class="sxs-lookup"><span data-stu-id="b87d7-104">Partial deliveries are defined in terms of return order lines, not return order shipments.</span></span>

<span data-ttu-id="b87d7-105">Это означает, что если полностью получено количество, указанное в одной строке заказа на возврат, но ничего не получено по другим строкам этого заказа на возврат, данная поставка не считается частичной поставкой.</span><span class="sxs-lookup"><span data-stu-id="b87d7-105">This means that if you receive the full quantity that is indicated on one return order line, but you receive nothing from the other lines in the return order, the delivery is not a partial delivery.</span></span> <span data-ttu-id="b87d7-106">Однако в том случае, если в строке заказа на возврат указано количество, равное 10 единицам измерения конкретной номенклатуры, подлежащей возврату, а было получено, только четыре единицы, то такая поставка считается частичной поставкой.</span><span class="sxs-lookup"><span data-stu-id="b87d7-106">However, if a return order line requires 10 units of a particular item to be returned, but you receive only four, it is a partial delivery.</span></span>

<span data-ttu-id="b87d7-107">Если отгруженная партия возврата содержит количество меньше полного количества по строке заказа на возврат, такую отгрузку можно отложить и дождаться прибытия остального возвращаемого количества или можно зарегистрировать и разнести неполное количество.</span><span class="sxs-lookup"><span data-stu-id="b87d7-107">If a return shipment contains less than the full quantity of a return order line, you can set the shipment aside and wait for the rest of the returned quantity to arrive, or you can register and post the partial quantity.</span></span>

## <a name="register-and-post-a-partial-quantity"></a><span data-ttu-id="b87d7-108">Регистрация и разноска неполного количества</span><span class="sxs-lookup"><span data-stu-id="b87d7-108">Register and post a partial quantity</span></span>

1.  <span data-ttu-id="b87d7-109">После выбора заказа на возврат для прибытия в форме **Обзор прибытия - склад: %1, дебаркадер: %2, имя журнала: %3** щелкните **Начать прибытие**, чтобы создать журнал прибытия, и нажмите **Журналы** \> **Показать прибытия по приходам**, чтобы открыть форму **Журнал прибытия**.</span><span class="sxs-lookup"><span data-stu-id="b87d7-109">After you select a return order for arrival on the **Arrival overview - Warehouse: %1, Dock: %2, Journal name: %3** form, click **Start arrival** to create the arrival journal, and then click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>

2.  <span data-ttu-id="b87d7-110">Выберите строку журнала, с которой нужно работать, а затем щелкните **Строки**, чтобы открыть форму **Строки журнала, местоположения**.</span><span class="sxs-lookup"><span data-stu-id="b87d7-110">Select the line of the journal that you want to work with, and then click **Lines** to open the **Journal lines, locations** form.</span></span>

3.  <span data-ttu-id="b87d7-111">Выберите строку кода номенклатуры, по которой прибыло неполное количество, а затем щелкните **Функции** \> **Разбиение**, чтобы открыть форму **Разбиение**.</span><span class="sxs-lookup"><span data-stu-id="b87d7-111">Select the line of the item number for which only a partial quantity has arrived, and then click **Functions** \> **Split** to open the **Split** form.</span></span>

4.  <span data-ttu-id="b87d7-112">В поле **Разбить количество** введите количество, отражающее общее число полученных номенклатур, а затем нажмите кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="b87d7-112">In the **Split quantity** field, enter the quantity for the total number of items that have been received, and then click **OK**.</span></span>

5.  <span data-ttu-id="b87d7-113">В форме **Строки журнала, местоположения** выберите строку для прибывшего количества номенклатур, а затем щелкните **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="b87d7-113">On the **Journal lines, locations** form, select the line for the quantity of items that has arrived, and then click **Post**.</span></span> <span data-ttu-id="b87d7-114">После прибытия номенклатур можно разнести строку для дополнительного количества.</span><span class="sxs-lookup"><span data-stu-id="b87d7-114">You can post the line for the additional quantity after the items have arrived.</span></span>




