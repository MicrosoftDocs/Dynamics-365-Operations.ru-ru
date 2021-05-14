---
title: Последняя закрытая строка работы должна быть размещением
description: Последняя закрытая строка работы должна быть размещением
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924383"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a><span data-ttu-id="6f08f-103">Последняя закрытая строка работы должна быть размещением</span><span class="sxs-lookup"><span data-stu-id="6f08f-103">The last closed work line must be a put</span></span>

<span data-ttu-id="6f08f-104">Код ошибки: WAX1285</span><span class="sxs-lookup"><span data-stu-id="6f08f-104">Error code: WAX1285</span></span>

## <a name="symptoms"></a><span data-ttu-id="6f08f-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="6f08f-105">Symptoms</span></span>

<span data-ttu-id="6f08f-106">Система отобразит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="6f08f-106">The system shows the following error message:</span></span>

> <span data-ttu-id="6f08f-107">Последняя закрытая строка работы должна быть размещением.</span><span class="sxs-lookup"><span data-stu-id="6f08f-107">The last closed work line must be a put.</span></span>

## <a name="cause"></a><span data-ttu-id="6f08f-108">Причина</span><span class="sxs-lookup"><span data-stu-id="6f08f-108">Cause</span></span>

<span data-ttu-id="6f08f-109">Невозможно отменить работу в текущем состоянии.</span><span class="sxs-lookup"><span data-stu-id="6f08f-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="6f08f-110">В строке последней работы поле **Статус работы** задается как *Закрыто*, но поле **Тип работы** не задано как *Размещение*.</span><span class="sxs-lookup"><span data-stu-id="6f08f-110">On the last work line, the **Work status** field is set to *Closed*, but the **Work type** field isn't set to *Put*.</span></span>

## <a name="resolution"></a><span data-ttu-id="6f08f-111">Приказ</span><span class="sxs-lookup"><span data-stu-id="6f08f-111">Resolution</span></span>

<span data-ttu-id="6f08f-112">Чтобы отменить работу, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6f08f-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="6f08f-113">Перейдите **Управление складом \> Периодические задачи \> Очистка \> Отмена работы**.</span><span class="sxs-lookup"><span data-stu-id="6f08f-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="6f08f-114">В поле **Код работы** укажите код работы, которую необходимо отменить.</span><span class="sxs-lookup"><span data-stu-id="6f08f-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="6f08f-115">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6f08f-115">Select **OK**.</span></span>
1. <span data-ttu-id="6f08f-116">Выберите **Да** для подтверждения того, что вы хотите отменить работу.</span><span class="sxs-lookup"><span data-stu-id="6f08f-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="6f08f-117">Дополнительные сведения см. в разделе [Отмена работы склада для обработки исключений](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="6f08f-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
