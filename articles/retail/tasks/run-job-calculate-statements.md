--- 
title: "Настройка и выполнение задания для расчета журналов операций"
description: "Эта процедура содержит инструкции по настройке и запуску регулярных пакетных заданий для создания и расчета журналов операций для выбранного магазина или группы магазинов."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 7bc936cdba771d322676565c2615ad75649cc50b
ms.contentlocale: ru-ru
ms.lasthandoff: 02/07/2018

---
# <a name="configure-and-run-a-job-to-calculate-statements"></a><span data-ttu-id="ca98b-103">Настройка и выполнение задания для расчета журналов операций</span><span class="sxs-lookup"><span data-stu-id="ca98b-103">Configure and run a job to calculate statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ca98b-104">Эта процедура содержит инструкции по настройке и запуску регулярных пакетных заданий для создания и расчета журналов операций для выбранного магазина или группы магазинов.</span><span class="sxs-lookup"><span data-stu-id="ca98b-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="ca98b-105">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="ca98b-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="ca98b-106">Перейдите в раздел "Все рабочие области" > "Финансовая информация розничного магазина".</span><span class="sxs-lookup"><span data-stu-id="ca98b-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="ca98b-107">Щелкните "Создать строки журнала операций".</span><span class="sxs-lookup"><span data-stu-id="ca98b-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="ca98b-108">Выберите конкретный магазин или узел, если вы хотите создать пакетное задание для группы магазинов.</span><span class="sxs-lookup"><span data-stu-id="ca98b-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="ca98b-109">Нажмите на стрелку для добавления выбора.</span><span class="sxs-lookup"><span data-stu-id="ca98b-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="ca98b-110">Щелкните вкладку "Выполнять в фоновом режиме".</span><span class="sxs-lookup"><span data-stu-id="ca98b-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="ca98b-111">В поле "Пакетная обработка" выберите "Да".</span><span class="sxs-lookup"><span data-stu-id="ca98b-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="ca98b-112">Щелкните "Повторение".</span><span class="sxs-lookup"><span data-stu-id="ca98b-112">Click Recurrence.</span></span>
6. <span data-ttu-id="ca98b-113">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="ca98b-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="ca98b-114">В поле "Время начала" введите время.</span><span class="sxs-lookup"><span data-stu-id="ca98b-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="ca98b-115">Выберите параметр "Дата завершения не указана".</span><span class="sxs-lookup"><span data-stu-id="ca98b-115">Select the No end date option.</span></span>
9. <span data-ttu-id="ca98b-116">В поле PatternUnit введите "Дни".</span><span class="sxs-lookup"><span data-stu-id="ca98b-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="ca98b-117">В поле "На" введите число.</span><span class="sxs-lookup"><span data-stu-id="ca98b-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="ca98b-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ca98b-118">Click OK.</span></span>
12. <span data-ttu-id="ca98b-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ca98b-119">Click OK.</span></span>


