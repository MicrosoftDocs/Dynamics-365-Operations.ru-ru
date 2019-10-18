---
title: Создание, расчет и разноска журналов операций для розничного магазина
description: В этой теме описано, как вручную создать, рассчитать и разнести журнал операций для магазина.
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
ms.openlocfilehash: 4517b9ddeb648b3d789773fc0dcb1ecd3c8be85c
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024806"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="2a0b4-103">Создание, расчет и разноска журналов операций для розничного магазина</span><span class="sxs-lookup"><span data-stu-id="2a0b4-103">Create, calculate, and post statements for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="2a0b4-104">В этой теме описано, как вручную создать, рассчитать и разнести журнал операций для магазина.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-104">This topic describes the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="2a0b4-105">Кроме того, существуют пакетные задания, которые могут быть настроены для тех же задач.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="2a0b4-106">Инструкции по настройке и запуску пакетных задач можно найти в других разделах.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="2a0b4-107">Чтобы выполнить эту процедуру, необходимо иметь проводки, которые были выполнены в кассовом терминале, а затем переданы в Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics 365 Retail.</span></span> <span data-ttu-id="2a0b4-108">В этой записи используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-108">This recording uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="2a0b4-109">Выберите **Финансовая информация розничного магазина** с главной страницы.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-109">Select **Retail store financials** from the home page.</span></span>
2. <span data-ttu-id="2a0b4-110">Выберите **Новый журнал операций**.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-110">Select **New statement**.</span></span>
3. <span data-ttu-id="2a0b4-111">В поле **Номер магазина** выберите вариант в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-111">In the **Store number** field, select a option from the drop-down.</span></span>
4. <span data-ttu-id="2a0b4-112">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-112">Select **OK**.</span></span>
5. <span data-ttu-id="2a0b4-113">Группа **Настройка** имеет параметры, определяющие, какие проводки включаются в журнал операций и как они группируются по строкам журнала.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-113">The **Setup** group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="2a0b4-114">Вы можете открыть группу **Настройка** и изменить эти параметры или использовать параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-114">You can open the **Setup** group and change these settings, or you can use the defaults.</span></span>  
    - <span data-ttu-id="2a0b4-115">Поле **Метод агрегирования операций** определяет, как будут группироваться строки журнала операций.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-115">The **Statement method** field defines how the statement lines will be grouped.</span></span>  
    - <span data-ttu-id="2a0b4-116">Выберите сотрудника или кассовый терминал в поле **Персонал/регистр**, если вы хотите создать журнал операций только для определенного сотрудника или терминала.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-116">Select a staff member or a register in the **staff/register** field if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="2a0b4-117">В поле **Способ закрытия** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-117">In the **Closing method** field, select an option.</span></span>
7. <span data-ttu-id="2a0b4-118">Выберите **Создать строки журнала операций** из панели действий.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-118">Select **Calculate statement** from the Action Pane.</span></span>
8. <span data-ttu-id="2a0b4-119">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-119">Select **Yes**.</span></span>
    - <span data-ttu-id="2a0b4-120">После расчета журнала операций должны быть созданы строки с общими суммами для каждого способа оплаты и способа агрегирования операций, который был использован.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-120">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    - <span data-ttu-id="2a0b4-121">Введите рассчитанную сумму в каждую строку, если ее нужно ввести или обновить.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-121">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="2a0b4-122">В поле с рассчитанными значениями будут подставлены суммы их деклараций платежных средств, выполненных в кассовом терминале.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-122">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="2a0b4-123">Выберите **Разнести журнал операций** из панели действий.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-123">Select **Post statement** from the Action Pane.</span></span>
10. <span data-ttu-id="2a0b4-124">Выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-124">Select **Close**.</span></span>
11. <span data-ttu-id="2a0b4-125">Закройте панель.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-125">Close the pane.</span></span>
12. <span data-ttu-id="2a0b4-126">На главной странице выберите **Финансовая информация розничного магазина**.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-126">At the home page, select **Retail store financials**.</span></span>
13. <span data-ttu-id="2a0b4-127">Выберите вкладку **Разнесенные журналы операций**.</span><span class="sxs-lookup"><span data-stu-id="2a0b4-127">Select the **Posted statements** tab.</span></span>

