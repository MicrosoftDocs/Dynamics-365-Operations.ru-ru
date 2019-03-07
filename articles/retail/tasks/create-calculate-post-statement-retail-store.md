---
title: Создание, расчет и разноска журнала операций для розничного магазина
description: В этой процедуре описано, как вручную создать, рассчитать и разнести журнал операций для магазина.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9ea30e7e008bfcce77a7ee2f4d7d01a6cf1ababc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "354399"
---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a><span data-ttu-id="0de41-103">Создание, расчет и разноска журнала операций для розничного магазина</span><span class="sxs-lookup"><span data-stu-id="0de41-103">Create, calculate, and post a statement for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="0de41-104">В этой процедуре описано, как вручную создать, рассчитать и разнести журнал операций для магазина.</span><span class="sxs-lookup"><span data-stu-id="0de41-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="0de41-105">Кроме того, существуют пакетные задания, которые могут быть настроены для тех же задач.</span><span class="sxs-lookup"><span data-stu-id="0de41-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="0de41-106">Инструкции по настройке и запуску пакетных задач можно найти в других разделах.</span><span class="sxs-lookup"><span data-stu-id="0de41-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="0de41-107">Чтобы выполнить эту процедуру, необходимо иметь проводки, которые были выполнены в кассовом терминале, а затем переданы в Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="0de41-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="0de41-108">В этой записи используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="0de41-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="0de41-109">Эта процедура может ссылаться на Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="0de41-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="0de41-110">Обратите внимание, что теперь Dynamics AX называется Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="0de41-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="0de41-111">Перейдите в раздел "Все рабочие области" > ..</span><span class="sxs-lookup"><span data-stu-id="0de41-111">Go to All workspaces > ..</span></span> <span data-ttu-id="0de41-112">> "Финансовая информация розничного магазина".</span><span class="sxs-lookup"><span data-stu-id="0de41-112">> Retail store financials.</span></span>
2. <span data-ttu-id="0de41-113">Щелкните "Новый журнал операций".</span><span class="sxs-lookup"><span data-stu-id="0de41-113">Click New statement.</span></span>
3. <span data-ttu-id="0de41-114">В поле "Номер магазина" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="0de41-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0de41-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="0de41-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="0de41-116">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="0de41-116">Click OK.</span></span>
    * <span data-ttu-id="0de41-117">Группа "Настройка" имеет параметры, определяющие, какие проводки включаются в журнал операций и как они группируются по строкам журнала.</span><span class="sxs-lookup"><span data-stu-id="0de41-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="0de41-118">В можете открыть группу "Настройка" и изменить эти параметры или использовать параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0de41-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="0de41-119">Поле "Метод агрегирования операций" определяет, как будут группироваться строки журнала операций.</span><span class="sxs-lookup"><span data-stu-id="0de41-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="0de41-120">Выберите сотрудника или кассовый терминал, если вы хотите создать журнал операций только для определенного сотрудника или терминала.</span><span class="sxs-lookup"><span data-stu-id="0de41-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="0de41-121">В поле "Способ закрытия" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="0de41-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="0de41-122">Щелкните "Создать строки журнала операций".</span><span class="sxs-lookup"><span data-stu-id="0de41-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="0de41-123">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="0de41-123">Click Yes.</span></span>
    * <span data-ttu-id="0de41-124">После расчета журнала операций должны быть созданы строки с общими суммами для каждого способа оплаты и способа агрегирования операций, который был использован.</span><span class="sxs-lookup"><span data-stu-id="0de41-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="0de41-125">Введите рассчитанную сумму в каждую строку, если ее нужно ввести или обновить.</span><span class="sxs-lookup"><span data-stu-id="0de41-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="0de41-126">В поле с рассчитанными значениями будут подставлены суммы их деклараций платежных средств, выполненных в кассовом терминале.</span><span class="sxs-lookup"><span data-stu-id="0de41-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="0de41-127">Щелкните "Разнести журнал операций".</span><span class="sxs-lookup"><span data-stu-id="0de41-127">Click Post statement.</span></span>
10. <span data-ttu-id="0de41-128">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="0de41-128">Click Close.</span></span>
11. <span data-ttu-id="0de41-129">Перейдите в раздел "Розничная торговля и коммерция" > "Каналы" > "Финансовая информация розничного магазина".</span><span class="sxs-lookup"><span data-stu-id="0de41-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="0de41-130">Щелкните вкладку "Разнесенные журналы операций".</span><span class="sxs-lookup"><span data-stu-id="0de41-130">Click the Posted statements tab.</span></span>

