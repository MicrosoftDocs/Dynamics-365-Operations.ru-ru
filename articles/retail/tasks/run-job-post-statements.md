--- 
title: "Настройка и выполнение задания для учета журналов операций"
description: "Эта процедура содержит инструкции по настройке и запуску регулярных пакетных заданий для разноски журналов операций для выбранного магазина или группы магазинов."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0e2dae54cc9ccfc0a85046c5478e539585c3744d
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="configure-and-run-a-job-to-post-statements"></a><span data-ttu-id="31e21-103">Настройка и выполнение задания для учета журналов операций</span><span class="sxs-lookup"><span data-stu-id="31e21-103">Configure and run a job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="31e21-104">Эта процедура содержит инструкции по настройке и запуску регулярных пакетных заданий для разноски журналов операций для выбранного магазина или группы магазинов.</span><span class="sxs-lookup"><span data-stu-id="31e21-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="31e21-105">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="31e21-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="31e21-106">Перейдите в раздел "Все рабочие области" > ..</span><span class="sxs-lookup"><span data-stu-id="31e21-106">Go to All workspaces > ..</span></span> <span data-ttu-id="31e21-107">> "Финансовая информация розничного магазина".</span><span class="sxs-lookup"><span data-stu-id="31e21-107">> Retail store financials.</span></span>
2. <span data-ttu-id="31e21-108">Щелкните "Разнести журналы операций".</span><span class="sxs-lookup"><span data-stu-id="31e21-108">Click Post statements.</span></span>
    * <span data-ttu-id="31e21-109">Выберите организационную иерархию, а затем в дереве узлов организации выберите отдельный магазин или узел.</span><span class="sxs-lookup"><span data-stu-id="31e21-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="31e21-110">Выберите узел, если вы хотите создать пакетное задание для группы магазинов.</span><span class="sxs-lookup"><span data-stu-id="31e21-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="31e21-111">Нажмите на стрелку для добавления выбора.</span><span class="sxs-lookup"><span data-stu-id="31e21-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="31e21-112">Щелкните вкладку "Выполнять в фоновом режиме".</span><span class="sxs-lookup"><span data-stu-id="31e21-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="31e21-113">Установите или снимите флажок "Пакетная обработка".</span><span class="sxs-lookup"><span data-stu-id="31e21-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="31e21-114">Щелкните "Повторение".</span><span class="sxs-lookup"><span data-stu-id="31e21-114">Click Recurrence.</span></span>
6. <span data-ttu-id="31e21-115">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="31e21-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="31e21-116">В поле "Время начала" введите время.</span><span class="sxs-lookup"><span data-stu-id="31e21-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="31e21-117">Выберите, нужно ли завершать повторы после определенного количества запусков, в конкретный день или никогда.</span><span class="sxs-lookup"><span data-stu-id="31e21-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="31e21-118">Затем выберите разные параметры, определяющие периодичность запуска задания.</span><span class="sxs-lookup"><span data-stu-id="31e21-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="31e21-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="31e21-119">Click OK.</span></span>
9. <span data-ttu-id="31e21-120">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="31e21-120">Click OK.</span></span>


