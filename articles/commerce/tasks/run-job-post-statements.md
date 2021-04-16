---
title: Настройка и выполнение задания для разноски отчетов
description: Эта процедура содержит инструкции по настройке и запуску регулярных пакетных заданий для разноски журналов операций для выбранного магазина или группы магазинов.
author: josaw1
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 52baa707c36f3468263782dc8ec735e44af88e38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804241"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="13131-103">Настройка и выполнение задания для разноски отчетов</span><span class="sxs-lookup"><span data-stu-id="13131-103">Configure and run job to post statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13131-104">Эта процедура содержит инструкции по настройке и запуску регулярных пакетных заданий для разноски журналов операций для выбранного магазина или группы магазинов.</span><span class="sxs-lookup"><span data-stu-id="13131-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="13131-105">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="13131-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="13131-106">Перейдите в раздел "Все рабочие области" > ..</span><span class="sxs-lookup"><span data-stu-id="13131-106">Go to All workspaces > ..</span></span> <span data-ttu-id="13131-107">> Финансовая информация магазина.</span><span class="sxs-lookup"><span data-stu-id="13131-107">> Store financials.</span></span>
2. <span data-ttu-id="13131-108">Нажмите «Пакетная разноска журналов операций»</span><span class="sxs-lookup"><span data-stu-id="13131-108">Click Post statements in batch.</span></span>
    * <span data-ttu-id="13131-109">Выберите организационную иерархию, а затем в дереве узлов организации выберите отдельный магазин или узел.</span><span class="sxs-lookup"><span data-stu-id="13131-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="13131-110">Выберите узел, если вы хотите создать пакетное задание для группы магазинов.</span><span class="sxs-lookup"><span data-stu-id="13131-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="13131-111">Нажмите на стрелку для добавления выбора.</span><span class="sxs-lookup"><span data-stu-id="13131-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="13131-112">Щелкните вкладку "Выполнять в фоновом режиме". ![Выполнять в фоновом режиме](../dev-itpro/media/runbackground.png "Выполнять в фоновом режиме")</span><span class="sxs-lookup"><span data-stu-id="13131-112">Click the Run in the background tab. ![Run in the background](../dev-itpro/media/runbackground.png "Run in the background")</span></span> 
4. <span data-ttu-id="13131-113">Установите или снимите флажок "Пакетная обработка".</span><span class="sxs-lookup"><span data-stu-id="13131-113">Check or uncheck the Batch processing checkbox.</span></span>
<span data-ttu-id="13131-114">![Пакетная обработка](../dev-itpro/media/batchprocessing.png "Пакетная обработка и периодичность")</span><span class="sxs-lookup"><span data-stu-id="13131-114">![Batch Processing](../dev-itpro/media/batchprocessing.png "Batch Processing & Recurrance")</span></span> 
5. <span data-ttu-id="13131-115">Щелкните "Повторение".</span><span class="sxs-lookup"><span data-stu-id="13131-115">Click Recurrence.</span></span>
6. <span data-ttu-id="13131-116">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="13131-116">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="13131-117">В поле "Время начала" введите время.</span><span class="sxs-lookup"><span data-stu-id="13131-117">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="13131-118">Выберите, нужно ли завершать повторы после определенного количества запусков, в конкретный день или никогда.</span><span class="sxs-lookup"><span data-stu-id="13131-118">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="13131-119">Затем выберите разные параметры, определяющие периодичность запуска задания.</span><span class="sxs-lookup"><span data-stu-id="13131-119">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="13131-120">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="13131-120">Click OK.</span></span>
9. <span data-ttu-id="13131-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="13131-121">Click OK.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]