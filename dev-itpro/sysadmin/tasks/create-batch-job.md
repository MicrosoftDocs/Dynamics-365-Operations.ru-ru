--- 
title: "Создание пакетного задания"
description: "Пакетное задание — это группа задач, отправляемых в экземпляр AOS для автоматической обработки."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 31c8e2ba87ef8c17a3147e1159104585258d4164
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-batch-job"></a><span data-ttu-id="0daa7-103">Создание пакетного задания</span><span class="sxs-lookup"><span data-stu-id="0daa7-103">Create a batch job</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0daa7-104">Пакетное задание — это группа задач, отправляемых в экземпляр AOS для автоматической обработки.</span><span class="sxs-lookup"><span data-stu-id="0daa7-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="0daa7-105">Пакетные задания выполняются с использованием параметров доступа пользователя, создавшего задание.</span><span class="sxs-lookup"><span data-stu-id="0daa7-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="0daa7-106">Следующая процедура используется для создания пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="0daa7-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="0daa7-107">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="0daa7-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="0daa7-108">Создание пакетного задания</span><span class="sxs-lookup"><span data-stu-id="0daa7-108">Create the batch job</span></span>
1. <span data-ttu-id="0daa7-109">Перейдите в раздел "Администрирование системы" > "Запросы" > "Пакетные задания".</span><span class="sxs-lookup"><span data-stu-id="0daa7-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="0daa7-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="0daa7-110">Click New.</span></span>
3. <span data-ttu-id="0daa7-111">В поле "Описание задания" введите значение.</span><span class="sxs-lookup"><span data-stu-id="0daa7-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="0daa7-112">В поле "Запланированные дата/время начала" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="0daa7-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="0daa7-113">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="0daa7-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="0daa7-114">Создание повторения</span><span class="sxs-lookup"><span data-stu-id="0daa7-114">Create a recurrence</span></span>
1. <span data-ttu-id="0daa7-115">В области действий щелкните "Пакетное задание".</span><span class="sxs-lookup"><span data-stu-id="0daa7-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="0daa7-116">Щелкните "Повторение".</span><span class="sxs-lookup"><span data-stu-id="0daa7-116">Click Recurrence.</span></span>
    * <span data-ttu-id="0daa7-117">Эти параметры используются для ввода диапазона и схемы повторения.</span><span class="sxs-lookup"><span data-stu-id="0daa7-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="0daa7-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="0daa7-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="0daa7-119">Добавление оповещений</span><span class="sxs-lookup"><span data-stu-id="0daa7-119">Add alerts</span></span>
1. <span data-ttu-id="0daa7-120">В области действий щелкните "Пакетное задание".</span><span class="sxs-lookup"><span data-stu-id="0daa7-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="0daa7-121">Щелкните "Оповещения".</span><span class="sxs-lookup"><span data-stu-id="0daa7-121">Click Alerts.</span></span>
    * <span data-ttu-id="0daa7-122">Укажите, требуется ли отправлять оповещения по завершении пакетного задания, в случае ошибки или отмены.</span><span class="sxs-lookup"><span data-stu-id="0daa7-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="0daa7-123">Затем укажите, требуется ли отображать оповещения в виде всплывающих сообщений.</span><span class="sxs-lookup"><span data-stu-id="0daa7-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="0daa7-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="0daa7-124">Click OK.</span></span>


