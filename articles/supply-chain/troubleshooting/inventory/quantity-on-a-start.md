---
title: Количество в запущенном карантинном заказе не обновляется при разбиении заказа
description: При создании карантинного заказа и попытке его разбиения количество заказа не обновляется на оставшееся количество после разбивки.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026860"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a><span data-ttu-id="d3630-103">Количество в запущенном карантинном заказе не обновляется при разбиении заказа</span><span class="sxs-lookup"><span data-stu-id="d3630-103">Quantity on a started quarantine order isn't updated when the order is split</span></span>

<span data-ttu-id="d3630-104">Номер статьи базы знаний: 4613113</span><span class="sxs-lookup"><span data-stu-id="d3630-104">KB number: 4613113</span></span>

## <a name="symptoms"></a><span data-ttu-id="d3630-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="d3630-105">Symptoms</span></span>

<span data-ttu-id="d3630-106">При создании карантинного заказа и попытке его разбиения количество заказа не обновляется на оставшееся количество после разбивки.</span><span class="sxs-lookup"><span data-stu-id="d3630-106">When you create a quarantine order and try to split it, the order quantity isn't updated to the remaining quantity after the split.</span></span>

## <a name="resolution"></a><span data-ttu-id="d3630-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="d3630-107">Resolution</span></span>

<span data-ttu-id="d3630-108">Система не изменяет исходное количество из карантинного заказа для того, чтобы можно было отслеживать исходное количество, которое было создано для этого карантинного заказа.</span><span class="sxs-lookup"><span data-stu-id="d3630-108">The system doesn't change the original quantity from a quarantine order to ensure that you can track the original quantity that was created for that quarantine order.</span></span> <span data-ttu-id="d3630-109">Однако система отслеживает количество, разбитое из карантинного заказа.</span><span class="sxs-lookup"><span data-stu-id="d3630-109">However, the system does track the quantity that is split from a quarantine order.</span></span> <span data-ttu-id="d3630-110">Для выполнения этого отслеживания используется поле базы данных с именем `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span><span class="sxs-lookup"><span data-stu-id="d3630-110">To do this tracking, it uses a database field that is named `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span></span> <span data-ttu-id="d3630-111">Однако это поле не отображается в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="d3630-111">However, this field isn't visible in the user interface (UI).</span></span>
