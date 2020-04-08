---
title: Массовое закрытие финансовых периодов
description: В этой теме демонстрируется, как заблокировать период или закрыть период на постоянной основе одновременно для нескольких юридических лиц.
author: aprilolson
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a149b35c6964166207effc799a02cd4c59bbb843
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144990"
---
# <a name="mass-financial-period-close"></a><span data-ttu-id="ce7f8-103">Массовое закрытие финансовых периодов</span><span class="sxs-lookup"><span data-stu-id="ce7f8-103">Mass financial period close</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ce7f8-104">В этой теме демонстрируется, как заблокировать период или закрыть период на постоянной основе одновременно для нескольких юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-104">This topic shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="ce7f8-105">Кроме того, задача показывает, как ограничить разноску группы пользователей конкретными модулями.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="ce7f8-106">В области переходов выберите **Модули > Главная книга > Закрытие периода > Календари книги учета**.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-106">In the navigation pane, go to **Modules > General ledger > Period close > Ledger calendars**.</span></span> <span data-ttu-id="ce7f8-107">Обратите внимание, что список юридических лиц зависит от финансового календаря, выбранного на странице.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="ce7f8-108">Отображаются только юридические лица, использующие выбранный финансовый календарь.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-108">Only legal entities using the selected fiscal calendar will display.</span></span>
2. <span data-ttu-id="ce7f8-109">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-109">Select **Edit**.</span></span>
3. <span data-ttu-id="ce7f8-110">Выберите период, для которого необходимо изменить статус.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="ce7f8-111">Выберите юридические лица, для которых необходимо обновить статус.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-111">Select the legal entities for which you want to update the status.</span></span> <span data-ttu-id="ce7f8-112">Можно быстро выбрать все юридические лица, установив флажок в левой верхней части сетки.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-112">You can quickly select all legal entities by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="ce7f8-113">Выберите **Доступ для обновления модуля**, чтобы определить доступ разноски к выбранному модулю.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-113">Select **Update module access** to define the posting access to a selected module.</span></span> <span data-ttu-id="ce7f8-114">Статус модуля можно также обновлять поочередно, редактирую записи в сетке.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="ce7f8-115">Эта кнопка полезна, когда требуется быстро выполнять обновление нескольких записей юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="ce7f8-116">В модуле **Приложение** выберите модуль, для которого нужно обновить статус.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-116">In the **Application** module, select the module that you want to update the status.</span></span> <span data-ttu-id="ce7f8-117">Щелкните **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-117">Click **Select**.</span></span>
7. <span data-ttu-id="ce7f8-118">В поле **Уровень доступа** выберите **Все**, **Нет** или определенную группу пользователей.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-118">In the **Access** level, select **All**, **None**, or a specific user group.</span></span> <span data-ttu-id="ce7f8-119">Щелкните **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-119">Click **Select**.</span></span> <span data-ttu-id="ce7f8-120">"Все" означает, что всем пользователям с разрешением на редактирование разрешено разносить, если период имеет значение "открыт".</span><span class="sxs-lookup"><span data-stu-id="ce7f8-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="ce7f8-121">"Нет" означает, что пользователям не разрешено разносить в модуль, если период имеет значение "открыт".</span><span class="sxs-lookup"><span data-stu-id="ce7f8-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="ce7f8-122">Конкретная группа пользователей означает, что только пользователи данной группы могут выполнять разноску в модуль, если период имеет значение "открыт".</span><span class="sxs-lookup"><span data-stu-id="ce7f8-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="ce7f8-123">Выберите **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-123">Select **Update**.</span></span>
9. <span data-ttu-id="ce7f8-124">Выберите другой период для обновления статуса.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="ce7f8-125">Выберите юридические лица, для которых необходимо обновить статус периода.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="ce7f8-126">Выберите **Обновить статус периода** и задайте статус **Заблокировано**, **Открытый** или **Закрытый на постоянной основе**.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-126">Select **Update period status** and set the status of **On hold**, **Open**, or **Permanently closed**.</span></span> <span data-ttu-id="ce7f8-127">**Открытый** означает, что период можно разнести при условии, что у пользователя есть доступ.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-127">**Open** indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="ce7f8-128">**Заблокировано** означает, что разноска в период невозможна, но период может быть повторно открыт.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-128">**On hold** means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="ce7f8-129">**Закрытый на постоянной основе** означает, что период закрыт и его открытие невозможно.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-129">**Permanently closed** means the period is closed and can never be opened.</span></span> <span data-ttu-id="ce7f8-130">Разноска корректировок невозможна.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="ce7f8-131">Не рекомендуется задавать период как **Закрытый на постоянной основе**, пока не будут сделаны все корректировки и аудиты.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-131">We do not recommend setting a period to **Permanently closed** until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="ce7f8-132">Выберите **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="ce7f8-132">Select **Update**.</span></span>

