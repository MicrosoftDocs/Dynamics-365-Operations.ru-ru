---
title: Настройка и выполнение задания для разноски отчетов
description: Эта процедура содержит инструкции по настройке и запуску регулярных пакетных заданий для разноски журналов операций для выбранного магазина или группы магазинов.
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bed4cfb4875231d11ad76e4403c7995519d56e73
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003686"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="ece2a-103">Настройка и выполнение задания для разноски отчетов</span><span class="sxs-lookup"><span data-stu-id="ece2a-103">Configure and run job to post statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ece2a-104">Эта процедура содержит инструкции по настройке и запуску регулярных пакетных заданий для разноски журналов операций для выбранного магазина или группы магазинов.</span><span class="sxs-lookup"><span data-stu-id="ece2a-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="ece2a-105">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="ece2a-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="ece2a-106">Перейдите в раздел "Все рабочие области" > ..</span><span class="sxs-lookup"><span data-stu-id="ece2a-106">Go to All workspaces > ..</span></span> <span data-ttu-id="ece2a-107">> Финансовая информация магазина.</span><span class="sxs-lookup"><span data-stu-id="ece2a-107">> Store financials.</span></span>
2. <span data-ttu-id="ece2a-108">Нажмите «Пакетная разноска журналов операций»</span><span class="sxs-lookup"><span data-stu-id="ece2a-108">Click Post statements in batch.</span></span>
    * <span data-ttu-id="ece2a-109">Выберите организационную иерархию, а затем в дереве узлов организации выберите отдельный магазин или узел.</span><span class="sxs-lookup"><span data-stu-id="ece2a-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="ece2a-110">Выберите узел, если вы хотите создать пакетное задание для группы магазинов.</span><span class="sxs-lookup"><span data-stu-id="ece2a-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="ece2a-111">Нажмите на стрелку для добавления выбора.</span><span class="sxs-lookup"><span data-stu-id="ece2a-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="ece2a-112">Щелкните вкладку "Выполнять в фоновом режиме". ![Выполнять в фоновом режиме](../dev-itpro/media/runbackground.png "Выполнять в фоновом режиме")</span><span class="sxs-lookup"><span data-stu-id="ece2a-112">Click the Run in the background tab. ![Run in the background](../dev-itpro/media/runbackground.png "Run in the background")</span></span> 
4. <span data-ttu-id="ece2a-113">Установите или снимите флажок "Пакетная обработка".</span><span class="sxs-lookup"><span data-stu-id="ece2a-113">Check or uncheck the Batch processing checkbox.</span></span>
<span data-ttu-id="ece2a-114">![Пакетная обработка](../dev-itpro/media/batchprocessing.png "Пакетная обработка и периодичность")</span><span class="sxs-lookup"><span data-stu-id="ece2a-114">![Batch Processing](../dev-itpro/media/batchprocessing.png "Batch Processing & Recurrance")</span></span> 
5. <span data-ttu-id="ece2a-115">Щелкните "Повторение".</span><span class="sxs-lookup"><span data-stu-id="ece2a-115">Click Recurrence.</span></span>
6. <span data-ttu-id="ece2a-116">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="ece2a-116">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="ece2a-117">В поле "Время начала" введите время.</span><span class="sxs-lookup"><span data-stu-id="ece2a-117">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="ece2a-118">Выберите, нужно ли завершать повторы после определенного количества запусков, в конкретный день или никогда.</span><span class="sxs-lookup"><span data-stu-id="ece2a-118">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="ece2a-119">Затем выберите разные параметры, определяющие периодичность запуска задания.</span><span class="sxs-lookup"><span data-stu-id="ece2a-119">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="ece2a-120">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ece2a-120">Click OK.</span></span>
9. <span data-ttu-id="ece2a-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ece2a-121">Click OK.</span></span>

