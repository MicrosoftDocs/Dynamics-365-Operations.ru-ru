---
title: Сброс застрявших пакетных заданий
description: В этой теме объясняется, как разрешать проблемы с застрявшими пакетными заданиями.
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: d0b12908993070a41d21ac57d6fb504fc6e3b06a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053523"
---
# <a name="reset-stuck-batch-jobs"></a><span data-ttu-id="240f3-103">Сброс застрявших пакетных заданий</span><span class="sxs-lookup"><span data-stu-id="240f3-103">Reset stuck batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a><span data-ttu-id="240f3-104">Расход</span><span class="sxs-lookup"><span data-stu-id="240f3-104">Issue</span></span>

<span data-ttu-id="240f3-105">Microsoft Dynamics 365 Human Resources может столкнуться с проблемами с пакетными заданиями, которые застряли в состоянии **Выполнение** или **Отмена** и не завершаются.</span><span class="sxs-lookup"><span data-stu-id="240f3-105">Microsoft Dynamics 365 Human Resources can experience issues with batch jobs that are stuck in either an **Executing** or **Canceling** state and don't complete.</span></span>

## <a name="resolution"></a><span data-ttu-id="240f3-106">Приказ</span><span class="sxs-lookup"><span data-stu-id="240f3-106">Resolution</span></span>

<span data-ttu-id="240f3-107">Когда пакетное задание зависает в состоянии **Выполняется** или **Отмена**, можно сбросить статус, принудительно отменив задание.</span><span class="sxs-lookup"><span data-stu-id="240f3-107">When a batch job is stuck in an **Executing** or **Canceling** state, you can reset the status by forcing the cancellation of the job.</span></span> <span data-ttu-id="240f3-108">После отмены пакетного задания его можно сбросить, установив для него статус **Ожидание**.</span><span class="sxs-lookup"><span data-stu-id="240f3-108">After you cancel it, you can reset the batch job by setting it to a **Waiting** status.</span></span> <span data-ttu-id="240f3-109">Затем оно будет снова отобрано для выполнения в следующем запланированном пакетном запуске.</span><span class="sxs-lookup"><span data-stu-id="240f3-109">It will then be picked up again for execution in the next scheduled batch run.</span></span>

1. <span data-ttu-id="240f3-110">В рабочей области **Администрирование системы** выберите страницу **Ссылки**, затем выберите **Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="240f3-110">In the **System administration** workspace, select the **Links** page, and select **Batch jobs**.</span></span>

2. <span data-ttu-id="240f3-111">На странице списка **Пакетное задание** выберите задание, которое необходимо сбросить.</span><span class="sxs-lookup"><span data-stu-id="240f3-111">On the **Batch job** list page, select the job that needs to be reset.</span></span>

3. <span data-ttu-id="240f3-112">На ленте действий выберите **Принудительная отмена** и подтвердите действие.</span><span class="sxs-lookup"><span data-stu-id="240f3-112">On the action ribbon, select **Force cancel**, and confirm the action.</span></span>

   > [!NOTE]
   > <span data-ttu-id="240f3-113">Действие **Принудительная отмена** доступно только в том случае, если выбранное пакетное задание имеет статус **Выполнение** или **Отмена**, но для данного задания не запущены процессы пакетного выполнения или отмены.</span><span class="sxs-lookup"><span data-stu-id="240f3-113">The **Force cancel** action is only available when the selected batch job has a status of either **Executing** or **Canceling**, and no batch execution or cancellation processes are running for the job.</span></span>

4. <span data-ttu-id="240f3-114">На ленте действий выберите **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="240f3-114">On the action ribbon, select **Change status**.</span></span>

5. <span data-ttu-id="240f3-115">На странице **Выбор нового состояния** выберите **Ожидание**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="240f3-115">On the **Select new status** page, select **Waiting**, and then select **OK**.</span></span>

   ![Выбор нового статуса пакетного задания](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a><span data-ttu-id="240f3-117">См. также</span><span class="sxs-lookup"><span data-stu-id="240f3-117">See also</span></span>

[<span data-ttu-id="240f3-118">Оптимизация производительности путем планирования пакетных заданий на нерабочие часы</span><span class="sxs-lookup"><span data-stu-id="240f3-118">Optimize performance by scheduling batch jobs after hours</span></span>](hr-admin-troubleshooting-batch-jobs.md)<br>
[<span data-ttu-id="240f3-119">Оптимизация производительности с помощью задач автоматической очистки</span><span class="sxs-lookup"><span data-stu-id="240f3-119">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
