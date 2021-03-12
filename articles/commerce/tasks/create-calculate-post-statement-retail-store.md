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
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ef31bc02fe1761a587ff6bcbecf4a0f34daea9b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964878"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="f1c6a-103">Создание, расчет и разноска журналов операций для розничного магазина</span><span class="sxs-lookup"><span data-stu-id="f1c6a-103">Create, calculate, and post statements for a retail store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1c6a-104">В этой теме описано, как вручную создать, рассчитать и разнести журнал операций для магазина.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-104">This topic describes the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="f1c6a-105">Кроме того, существуют пакетные задания, которые могут быть настроены для тех же задач.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="f1c6a-106">Инструкции по настройке и запуску пакетных задач можно найти в других разделах.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="f1c6a-107">Чтобы выполнить эту процедуру, необходимо иметь проводки, которые были выполнены в кассовом терминале, а затем переданы в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics 365 Commerce.</span></span> <span data-ttu-id="f1c6a-108">В этой записи используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-108">This recording uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="f1c6a-109">Выберите **Финансовая информация магазина** с главной страницы.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-109">Select **Store financials** from the home page.</span></span>
2. <span data-ttu-id="f1c6a-110">Выберите **Новый журнал операций**.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-110">Select **New statement**.</span></span>
3. <span data-ttu-id="f1c6a-111">В поле **Номер магазина** выберите вариант в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-111">In the **Store number** field, select a option from the drop-down.</span></span>
4. <span data-ttu-id="f1c6a-112">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-112">Select **OK**.</span></span>
5. <span data-ttu-id="f1c6a-113">Группа **Настройка** имеет параметры, определяющие, какие проводки включаются в журнал операций и как они группируются по строкам журнала.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-113">The **Setup** group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="f1c6a-114">Вы можете открыть группу **Настройка** и изменить эти параметры или использовать параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-114">You can open the **Setup** group and change these settings, or you can use the defaults.</span></span>  
    - <span data-ttu-id="f1c6a-115">Поле **Метод агрегирования операций** определяет, как будут группироваться строки журнала операций.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-115">The **Statement method** field defines how the statement lines will be grouped.</span></span>  
    - <span data-ttu-id="f1c6a-116">Выберите сотрудника или кассовый терминал в поле **Персонал/регистр**, если вы хотите создать журнал операций только для определенного сотрудника или терминала.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-116">Select a staff member or a register in the **staff/register** field if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="f1c6a-117">В поле **Способ закрытия** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-117">In the **Closing method** field, select an option.</span></span>
7. <span data-ttu-id="f1c6a-118">Выберите **Создать строки журнала операций** из панели действий.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-118">Select **Calculate statement** from the Action Pane.</span></span>
8. <span data-ttu-id="f1c6a-119">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-119">Select **Yes**.</span></span>
    - <span data-ttu-id="f1c6a-120">После расчета журнала операций должны быть созданы строки с общими суммами для каждого способа оплаты и способа агрегирования операций, который был использован.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-120">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    - <span data-ttu-id="f1c6a-121">Введите рассчитанную сумму в каждую строку, если ее нужно ввести или обновить.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-121">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="f1c6a-122">В поле с рассчитанными значениями будут подставлены суммы их деклараций платежных средств, выполненных в кассовом терминале.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-122">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="f1c6a-123">Выберите **Разнести журнал операций** из панели действий.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-123">Select **Post statement** from the Action Pane.</span></span>
10. <span data-ttu-id="f1c6a-124">Выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-124">Select **Close**.</span></span>
11. <span data-ttu-id="f1c6a-125">Закройте панель.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-125">Close the pane.</span></span>
12. <span data-ttu-id="f1c6a-126">На главной странице выберите **Финансовая информация магазина**.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-126">At the home page, select **Store financials**.</span></span>
13. <span data-ttu-id="f1c6a-127">Выберите вкладку **Разнесенные журналы операций**.</span><span class="sxs-lookup"><span data-stu-id="f1c6a-127">Select the **Posted statements** tab.</span></span>

