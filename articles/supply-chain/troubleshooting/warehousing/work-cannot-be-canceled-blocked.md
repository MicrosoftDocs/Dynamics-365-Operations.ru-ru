---
title: Работа не может быть отменена, поскольку она заблокирована
description: Работа не может быть отменена, поскольку она заблокирована
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924287"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a><span data-ttu-id="9c958-103">Работа не может быть отменена, поскольку она заблокирована</span><span class="sxs-lookup"><span data-stu-id="9c958-103">Work can't be canceled because it's blocked</span></span>

<span data-ttu-id="9c958-104">Код ошибки: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="9c958-104">Error code: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="9c958-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="9c958-105">Symptoms</span></span>

<span data-ttu-id="9c958-106">Система отобразит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="9c958-106">The system shows the following error message:</span></span>

> <span data-ttu-id="9c958-107">Работа %1 не может быть отменена, поскольку она заблокирована типом причины %2.</span><span class="sxs-lookup"><span data-stu-id="9c958-107">Work %1 cannot be cancelled because it is blocked by reason type %2.</span></span> <span data-ttu-id="9c958-108">Работа должна быть разблокирована, прежде чем ее можно будет отменить.</span><span class="sxs-lookup"><span data-stu-id="9c958-108">The work must be unblocked before it can be cancelled.</span></span>

## <a name="cause"></a><span data-ttu-id="9c958-109">Причина</span><span class="sxs-lookup"><span data-stu-id="9c958-109">Cause</span></span>

<span data-ttu-id="9c958-110">Работа заблокирована и не может быть отменена.</span><span class="sxs-lookup"><span data-stu-id="9c958-110">The work is blocked and can't be canceled.</span></span>

<span data-ttu-id="9c958-111">На странице **Работа** на вкладке **Общее**, параметр **Заблокировано** задан как *Да*.</span><span class="sxs-lookup"><span data-stu-id="9c958-111">On the **Work** page, on the **General** tab, the **Blocked** option is set to *Yes*.</span></span> <span data-ttu-id="9c958-112">Этот параметр указывает, что работа заблокирована.</span><span class="sxs-lookup"><span data-stu-id="9c958-112">This setting indicates that the work is blocked.</span></span> <span data-ttu-id="9c958-113">На вкладке **Причины блокировки** указано, почему работа была заблокирована.</span><span class="sxs-lookup"><span data-stu-id="9c958-113">The **Blocking reasons** tab shows why the work was blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="9c958-114">Приказ</span><span class="sxs-lookup"><span data-stu-id="9c958-114">Resolution</span></span>

<span data-ttu-id="9c958-115">Чтобы разблокировать работу, выберите вкладку **Причины блокировки** и выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="9c958-115">To unblock the work, select the **Blocking reasons** tab, and then follow one of these steps:</span></span>

- <span data-ttu-id="9c958-116">Если в поле **Причина блокировки работы** указано значение *Причина не определена*: на панели операций на вкладке **Работа** в группе **Работа** выберите **Разблокировать работу**.</span><span class="sxs-lookup"><span data-stu-id="9c958-116">If the **Work blocking reason** field is set to *Undefined reason*: On the Action Pane, on the **Work** tab, in the **Work** group, select **Unblock work**.</span></span>
- <span data-ttu-id="9c958-117">Если для поля **Причина блокировки работы** установлено значение *Обработка волны*: на панели операций на вкладке **Связанная информация** в группе **Связанная информация** выберите **Волна**.</span><span class="sxs-lookup"><span data-stu-id="9c958-117">If the **Work blocking reason** field is set to *Processing wave*: On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="9c958-118">Затем на странице **Волна** в области действий откройте вкладку **Волна** и в группе **Волна** выберите **Очистить данные волны**.</span><span class="sxs-lookup"><span data-stu-id="9c958-118">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="9c958-119">Обходное решение</span><span class="sxs-lookup"><span data-stu-id="9c958-119">Workaround</span></span>

<span data-ttu-id="9c958-120">Если предыдущие шаги не устранили проблему, можно отменить работу, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9c958-120">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="9c958-121">Перейдите **Управление складом \> Периодические задачи \> Очистка \> Отмена работы**.</span><span class="sxs-lookup"><span data-stu-id="9c958-121">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="9c958-122">В поле **Код работы** укажите код работы, которую необходимо отменить и у которой в настоящее время есть значение **Статус работы** как *Открыто*, *Выполняется*, *Отменено*, *Объединено* или *Закрыто*.</span><span class="sxs-lookup"><span data-stu-id="9c958-122">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="9c958-123">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9c958-123">Select **OK**.</span></span>
1. <span data-ttu-id="9c958-124">Выберите **Да** для подтверждения того, что вы хотите отменить работу.</span><span class="sxs-lookup"><span data-stu-id="9c958-124">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="9c958-125">Дополнительные сведения см. в разделе [Отмена работы склада для обработки исключений](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="9c958-125">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
