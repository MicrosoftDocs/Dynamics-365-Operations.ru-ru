---
title: Отправка заказа на работу
description: В этом разделе описывается, как отправлять заказы на работу в модуле "Управление активами".
author: josaw1
manager: tfehr
ms.date: 08/19/2019
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
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3412b447876d5cd0b16bdbfc0a30ae1afa3e33c0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215317"
---
# <a name="dispatch-work-order"></a><span data-ttu-id="dcf80-103">Отправка заказа на работу</span><span class="sxs-lookup"><span data-stu-id="dcf80-103">Dispatch work order</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="dcf80-104">Можно запланировать один заказ на работу или задания заказа на работу одному работнику, используя функцию **Подготовить к отправке**.</span><span class="sxs-lookup"><span data-stu-id="dcf80-104">You can schedule one work order or work order jobs to one worker using the **Dispatch** functionality.</span></span>

1. <span data-ttu-id="dcf80-105">Щелкните **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="dcf80-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="dcf80-106">Выберите заказ на работу в списке.</span><span class="sxs-lookup"><span data-stu-id="dcf80-106">Select the work order in the list.</span></span>

3. <span data-ttu-id="dcf80-107">На вкладке **Общие** щелкните **Подготовить к отправке**.</span><span class="sxs-lookup"><span data-stu-id="dcf80-107">On the **General** tab, click **Dispatch**.</span></span>

4. <span data-ttu-id="dcf80-108">В диалоговом окне **Запланировать заказ на работу** выберите работника в поле **Работник**.</span><span class="sxs-lookup"><span data-stu-id="dcf80-108">In the **Schedule work order** dialog, select the worker in the **Worker** field.</span></span>

5. <span data-ttu-id="dcf80-109">В поле **Планирование времени** можно вставить ожидаемые рабочие часы в случае, когда количество ожидаемых рабочих часов отличается от прогнозируемых.</span><span class="sxs-lookup"><span data-stu-id="dcf80-109">In the **Schedule hours** field, you can insert expected work hours in case expected work hours differ from forecast hours.</span></span>

6. <span data-ttu-id="dcf80-110">В поле **Спланированное начало** можно изменить дату и время начала, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="dcf80-110">In the **Scheduled start** field, you can edit start date and time, if required.</span></span>

7. <span data-ttu-id="dcf80-111">Если процесс планирования должен учитывать ограничения по мощности для ресурсов, уже запланированных для других заданий, убедитесь, что для переключателей **Актив**, **Инструмент** и **Работник** выбрано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="dcf80-111">If the scheduling process should observe capacity limitations regarding resources already scheduled on other jobs, make sure that the **Asset**, **Tool**, and **Worker** toggle buttons are set to **Yes**.</span></span> <span data-ttu-id="dcf80-112">Если требуется просмотреть подробные сведения о процессе планирования, выберите **Да** на переключателе **Подробно**.</span><span class="sxs-lookup"><span data-stu-id="dcf80-112">If you want to see detailed information about the scheduling process, select **Yes** on the **Verbose** toggle button.</span></span> <span data-ttu-id="dcf80-113">Это означает, что подробные сведения о расчетных оценках для заказа на работу будут показаны в журнале Infolog.</span><span class="sxs-lookup"><span data-stu-id="dcf80-113">This means detailed information about the calculated scores on the work order is shown in the Infolog.</span></span>

8. <span data-ttu-id="dcf80-114">Выберите **Да** на переключателе **Игнорировать расписание**, чтобы игнорировать закрытые дни в календаре (применяется к активу, работнику и инструментам).</span><span class="sxs-lookup"><span data-stu-id="dcf80-114">Select **Yes** on the **Ignore schedule** toggle button to ignore closed days in the calendar (applies to asset, worker, and tools).</span></span> <span data-ttu-id="dcf80-115">Выберите **Да** для переключателя **Пропустить запланированное выполнение**, чтобы игнорировать ограничения, которые могли быть выбраны в заказе на работу в отношении планирования.</span><span class="sxs-lookup"><span data-stu-id="dcf80-115">Select **Yes** on the **Ignore scheduled execution** toggle button to ignore limitations that may have been selected on the work order regarding scheduling.</span></span> 

    <span data-ttu-id="dcf80-116">Для получения дополнительных сведений о настройке запланированного выполнения см. в разделе [Запланированное выполнение](../setup-for-work-orders/scheduled-execution.md).</span><span class="sxs-lookup"><span data-stu-id="dcf80-116">For information on the setup of scheduled execution, see the [Scheduled execution](../setup-for-work-orders/scheduled-execution.md) section.</span></span>

9. <span data-ttu-id="dcf80-117">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="dcf80-117">Click **OK**.</span></span> <span data-ttu-id="dcf80-118">Состояние жизненного цикла заказа на работу автоматически обновляется до состояния жизненного цикла **Запланировано**, указанного в разделе **Управление активами** > **Настройка** > **Заказы на работу** > **Модели жизненного цикла**.</span><span class="sxs-lookup"><span data-stu-id="dcf80-118">The work order lifecycle state is automatically updated to the **Scheduled** lifecycle state specified **Asset management** > **Setup** > **Work orders** > **Lifecycle models**.</span></span>

<span data-ttu-id="dcf80-119">На рисунке, приведенном ниже, показан пример выбора диспетчеризации в диалоговом окне **Планирование заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="dcf80-119">The figure below shows an example of dispatch selections in the **Schedule work order** dialog.</span></span>

![Рисунок 1](media/04-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="dcf80-121">Если необходимо удалить график в заказе на работу, выберите заказ на работу в разделе **Все заказы на работу**, и затем нажав **Удалить расписание** на вкладке **Общие**. Не забудьте вручную обновить состояние жизненного цикла заказа на работу, если удалили расписание.</span><span class="sxs-lookup"><span data-stu-id="dcf80-121">If you want to delete the schedule on a work order, select the work order in **All work orders**, and then click **Delete schedule** on the **General** tab. Remember to manually update the work order lifecycle state if you delete the schedule.</span></span>

