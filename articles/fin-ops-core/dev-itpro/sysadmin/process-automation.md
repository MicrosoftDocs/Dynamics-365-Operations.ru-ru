---
title: Автоматизация процессов
description: В этом разделе приводятся подробные сведения о том, как автоматизация процессов позволяет выполнять простое планирование процессов, которые будут выполняться сервером обработки пакетных заданий.
author: RyanCCarlson2
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: a8722adfe410f15bc379f9b550f0618c881f067d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920837"
---
# <a name="process-automation"></a><span data-ttu-id="b34bf-103">Автоматизация процессов</span><span class="sxs-lookup"><span data-stu-id="b34bf-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b34bf-104">Автоматизация процессов позволяет выполнять простое планирование процессов, которые будут выполняться сервером обработки пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="b34bf-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="b34bf-105">Обновленное представление календаря запланированных работ позволяет конечным пользователям просматривать и выполнять действия по запланированной и завершенной работе.</span><span class="sxs-lookup"><span data-stu-id="b34bf-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="b34bf-106">Администрирование</span><span class="sxs-lookup"><span data-stu-id="b34bf-106">Administration</span></span>

<span data-ttu-id="b34bf-107">Страница центра администрирования для всех автоматизаций процессов находится в модуле администрирования системы в меню **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="b34bf-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="b34bf-108">На этой странице будут перечислены все автоматизированные процессы (серии), которые настроены в системе.</span><span class="sxs-lookup"><span data-stu-id="b34bf-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="b34bf-109">Кроме того, она позволяет добавлять новые автоматизации процессов непосредственно с этой страницы.</span><span class="sxs-lookup"><span data-stu-id="b34bf-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="b34bf-110">После настройки серии можно управлять каждой серией из данного списка.</span><span class="sxs-lookup"><span data-stu-id="b34bf-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="b34bf-111">Можно выбрать редактирование всей серии, удалить ее, просмотреть все вхождения в представлении списка или отключить эту серию, если вы хотите приостановить запланированную работу в течение некоторого времени.</span><span class="sxs-lookup"><span data-stu-id="b34bf-111">You can choose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a while.</span></span> 

<span data-ttu-id="b34bf-112">Все процессы, отключенные в управлении функциями, не отображаются, когда функция отключена.</span><span class="sxs-lookup"><span data-stu-id="b34bf-112">Any processes that are disabled in feature management won't show when the feature is disabled.</span></span> <span data-ttu-id="b34bf-113">Кроме того, механизм планирования автоматизации процесса не будет планировать обработку каких-либо событий для отключенной функции.</span><span class="sxs-lookup"><span data-stu-id="b34bf-113">Additionally, the process automation scheduling engine won't schedule any occurrences or background processes for a disabled feature.</span></span> <span data-ttu-id="b34bf-114">Повторное включение функции приведет к немедленному запуску любых запланированных событий или фоновых процессов в прошлом.</span><span class="sxs-lookup"><span data-stu-id="b34bf-114">Re-enabling the feature will cause any scheduled occurrences or background processes in the past to run immediately.</span></span> <span data-ttu-id="b34bf-115">Механизм планирования автоматизации процесса использует системное пакетное задание **Системное задание по опросу автоматизации процессов**.</span><span class="sxs-lookup"><span data-stu-id="b34bf-115">The process automation scheduling engine relies on the system batch job, **Process automation polling system job** to run.</span></span> <span data-ttu-id="b34bf-116">Задание не должно изменяться ни в какой момент.</span><span class="sxs-lookup"><span data-stu-id="b34bf-116">The job shouldn't be altered or tampered with at any time.</span></span> 

## <a name="calendar-view"></a><span data-ttu-id="b34bf-117">Представление календаря</span><span class="sxs-lookup"><span data-stu-id="b34bf-117">Calendar view</span></span>

<span data-ttu-id="b34bf-118">Одним из ключевых преимуществ автоматизации процессов является возможность видеть запланированную работу в простом представлении календаря.</span><span class="sxs-lookup"><span data-stu-id="b34bf-118">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="b34bf-119">Это представление позволяет видеть работу за неделю.</span><span class="sxs-lookup"><span data-stu-id="b34bf-119">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="b34bf-120">Это представление будет отображаться в правой части страницы **Автоматизация процессов**.</span><span class="sxs-lookup"><span data-stu-id="b34bf-120">You'll see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="b34bf-121">Оно будет заполнено запланированной работой для выбранных серий.</span><span class="sxs-lookup"><span data-stu-id="b34bf-121">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="b34bf-122">[![Календарь автоматизации процессов](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="b34bf-122">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="b34bf-123">Изменения вхождений</span><span class="sxs-lookup"><span data-stu-id="b34bf-123">Occurrence changes</span></span>

<span data-ttu-id="b34bf-124">Каждое вхождение можно изменить без воздействия на другие вхождения, определяемые серией, из которой они происходят.</span><span class="sxs-lookup"><span data-stu-id="b34bf-124">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="b34bf-125">Вхождения запланированной работы можно изменить из представления календаря, нажав кнопку **Просмотреть/изменить** и выбрав пункт **Вхождение**.</span><span class="sxs-lookup"><span data-stu-id="b34bf-125">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="b34bf-126">Эта страница позволяет получить доступ ко всем настройкам, первоначально отображаемым в мастере настройки серии, и предоставляет возможность выполнить одно изменение для выбранного вхождения.</span><span class="sxs-lookup"><span data-stu-id="b34bf-126">This page allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="b34bf-127">Вхождение запланированной работы также может быть отключено нажатием кнопки **Отключить** в представлении календаря.</span><span class="sxs-lookup"><span data-stu-id="b34bf-127">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span>

## <a name="developer-documentation"></a><span data-ttu-id="b34bf-128">Документация Разработчика</span><span class="sxs-lookup"><span data-stu-id="b34bf-128">Developer documentation</span></span>

<span data-ttu-id="b34bf-129">Платформа автоматизации процессов позволяет разработчикам расширять платформу автоматизации процессов.</span><span class="sxs-lookup"><span data-stu-id="b34bf-129">The process automation framework allows developers to extend the process automation framework.</span></span> <span data-ttu-id="b34bf-130">В документации по [платформе автоматизации процессов](../process-automation/process-automation-framework.md) представлена информация о том, как создавать пользовательские процессы, которые должны выполняться сервером обработки пакетных заданий, запланированные мастером автоматизации процессов и отображаемые в представлении календаря автоматически.</span><span class="sxs-lookup"><span data-stu-id="b34bf-130">The [Process automation framework](../process-automation/process-automation-framework.md) documentation provides information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
