---
title: Работа не может быть из-за ее статуса
description: Работа не может быть из-за ее статуса
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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924263"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a><span data-ttu-id="608b5-103">Работа не может быть из-за ее статуса</span><span class="sxs-lookup"><span data-stu-id="608b5-103">Work can't be canceled because of its status</span></span>

<span data-ttu-id="608b5-104">Код ошибки: WAX2190</span><span class="sxs-lookup"><span data-stu-id="608b5-104">Error code: WAX2190</span></span>

## <a name="symptoms"></a><span data-ttu-id="608b5-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="608b5-105">Symptoms</span></span>

<span data-ttu-id="608b5-106">Система отобразит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="608b5-106">The system shows the following error message:</span></span>

> <span data-ttu-id="608b5-107">Невозможно отменить работу %1, так как она имеет статус %2.</span><span class="sxs-lookup"><span data-stu-id="608b5-107">You cannot cancel work %1 because it has a status of %2.</span></span>

## <a name="cause"></a><span data-ttu-id="608b5-108">Причина</span><span class="sxs-lookup"><span data-stu-id="608b5-108">Cause</span></span>

<span data-ttu-id="608b5-109">Невозможно отменить работу в текущем состоянии.</span><span class="sxs-lookup"><span data-stu-id="608b5-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="608b5-110">У заголовка работы или строк работы нет ожидаемого значения **Статус работы**.</span><span class="sxs-lookup"><span data-stu-id="608b5-110">The work header or work lines don't have the expected **Work status** value.</span></span> <span data-ttu-id="608b5-111">В поле **Статус работы** в заголовке работы нет значения *Открыто* или *Выполняется*.</span><span class="sxs-lookup"><span data-stu-id="608b5-111">The **Work status** field on the work header isn't set to *Open* or *In progress*.</span></span>

## <a name="resolution"></a><span data-ttu-id="608b5-112">Приказ</span><span class="sxs-lookup"><span data-stu-id="608b5-112">Resolution</span></span>

<span data-ttu-id="608b5-113">Чтобы отменить работу, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="608b5-113">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="608b5-114">Перейдите **Управление складом \> Периодические задачи \> Очистка \> Отмена работы**.</span><span class="sxs-lookup"><span data-stu-id="608b5-114">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="608b5-115">В поле **Код работы** укажите код работы, которую необходимо отменить.</span><span class="sxs-lookup"><span data-stu-id="608b5-115">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="608b5-116">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="608b5-116">Select **OK**.</span></span>
1. <span data-ttu-id="608b5-117">Выберите **Да** для подтверждения того, что вы хотите отменить работу.</span><span class="sxs-lookup"><span data-stu-id="608b5-117">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="608b5-118">Дополнительные сведения см. в разделе [Отмена работы склада для обработки исключений](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="608b5-118">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
