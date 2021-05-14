---
title: Работа остается заблокированной
description: Работа остается заблокированной
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924138"
---
# <a name="work-remains-blocked"></a><span data-ttu-id="40bec-103">Работа остается заблокированной</span><span class="sxs-lookup"><span data-stu-id="40bec-103">Work remains blocked</span></span>

<span data-ttu-id="40bec-104">Код ошибки: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="40bec-104">Error code: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="40bec-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="40bec-105">Symptoms</span></span>

<span data-ttu-id="40bec-106">Система отобразит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="40bec-106">The system shows the following error message:</span></span>

> <span data-ttu-id="40bec-107">Работа %1 остается заблокированной, так как связанная волна %2 имеет статус %3.</span><span class="sxs-lookup"><span data-stu-id="40bec-107">Work %1 remains blocked because the related wave %2 has status %3.</span></span>

## <a name="cause"></a><span data-ttu-id="40bec-108">Причина</span><span class="sxs-lookup"><span data-stu-id="40bec-108">Cause</span></span>

<span data-ttu-id="40bec-109">В настоящее время работа обрабатывается в волне и не может быть разблокирована по одной из следующих причин:</span><span class="sxs-lookup"><span data-stu-id="40bec-109">The work is currently being processed on a wave and can't be unblocked, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="40bec-110">На вкладке **Причины блокировки** поле **Причина блокировки работы** для одной или нескольких строк задано как *Обработка волны*.</span><span class="sxs-lookup"><span data-stu-id="40bec-110">On the **Blocking reasons** tab, the **Work blocking reason** field for one or more lines is set to *Processing wave*.</span></span>
- <span data-ttu-id="40bec-111">Когда выбрано **Волна** в группе **Связанная информация** на вкладке **Связанная информация** области действий, поле **Статус волны** задается как *Обработка*.</span><span class="sxs-lookup"><span data-stu-id="40bec-111">When you select **Wave** in the **Related information** group on the **Related information** tab of the Action Pane, the **Wave status** field is set to *Processing*.</span></span>

## <a name="resolution"></a><span data-ttu-id="40bec-112">Приказ</span><span class="sxs-lookup"><span data-stu-id="40bec-112">Resolution</span></span>

<span data-ttu-id="40bec-113">В области действий на вкладке **Связанная информация** в группе **Связанная информация** выберите **Волна**.</span><span class="sxs-lookup"><span data-stu-id="40bec-113">On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="40bec-114">Затем на странице **Волна** в области действий откройте вкладку **Волна** и в группе **Волна** выберите **Очистить данные волны**.</span><span class="sxs-lookup"><span data-stu-id="40bec-114">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="40bec-115">Обходное решение</span><span class="sxs-lookup"><span data-stu-id="40bec-115">Workaround</span></span>

<span data-ttu-id="40bec-116">Если предыдущие шаги не устранили проблему, можно отменить работу, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="40bec-116">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="40bec-117">Перейдите **Управление складом \> Периодические задачи \> Очистка \> Отмена работы**.</span><span class="sxs-lookup"><span data-stu-id="40bec-117">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="40bec-118">В поле **Код работы** укажите код работы, которую необходимо отменить и у которой в настоящее время есть значение **Статус работы** как *Открыто*, *Выполняется*, *Отменено*, *Объединено* или *Закрыто*.</span><span class="sxs-lookup"><span data-stu-id="40bec-118">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="40bec-119">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="40bec-119">Select **OK**.</span></span>
1. <span data-ttu-id="40bec-120">Выберите **Да** для подтверждения того, что вы хотите отменить работу.</span><span class="sxs-lookup"><span data-stu-id="40bec-120">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="40bec-121">Дополнительные сведения см. в разделе [Отмена работы склада для обработки исключений](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="40bec-121">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
