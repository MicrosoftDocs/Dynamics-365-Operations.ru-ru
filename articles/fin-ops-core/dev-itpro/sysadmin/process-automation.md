---
title: Автоматизация процессов
description: В этом разделе приводятся подробные сведения о том, как автоматизация процессов позволяет выполнять простое планирование процессов, которые будут выполняться сервером обработки пакетных заданий.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 08/12/2020
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
ms.openlocfilehash: e3babed18caefff16105f70a0b15b8b8cf0f08eb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568218"
---
# <a name="process-automation"></a><span data-ttu-id="168af-103">Автоматизация процессов</span><span class="sxs-lookup"><span data-stu-id="168af-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="168af-104">Автоматизация процессов позволяет выполнять простое планирование процессов, которые будут выполняться сервером обработки пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="168af-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="168af-105">Обновленное представление календаря запланированных работ позволяет конечным пользователям просматривать и выполнять действия по запланированной и завершенной работе.</span><span class="sxs-lookup"><span data-stu-id="168af-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="168af-106">Администрирование</span><span class="sxs-lookup"><span data-stu-id="168af-106">Administration</span></span>

<span data-ttu-id="168af-107">Страница центра администрирования для всех автоматизаций процессов находится в модуле администрирования системы в меню **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="168af-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="168af-108">На этой странице будут перечислены все автоматизированные процессы (серии), которые настроены в системе.</span><span class="sxs-lookup"><span data-stu-id="168af-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="168af-109">Кроме того, она позволяет добавлять новые автоматизации процессов непосредственно с этой страницы.</span><span class="sxs-lookup"><span data-stu-id="168af-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="168af-110">После настройки серии можно управлять каждой серией из данного списка.</span><span class="sxs-lookup"><span data-stu-id="168af-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="168af-111">Можно выбрать редактирование всей серии, удалить ее, просмотреть все вхождения в представлении списка или отключить эту серию, если вы хотите приостановить запланированную работу в течение некоторого времени.</span><span class="sxs-lookup"><span data-stu-id="168af-111">You can choose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a while.</span></span> 

<span data-ttu-id="168af-112">Все процессы, отключенные в управлении функциями, не отображаются, когда функция отключена.</span><span class="sxs-lookup"><span data-stu-id="168af-112">Any processes that are disabled in feature management won't show when the feature is disabled.</span></span> <span data-ttu-id="168af-113">Кроме того, механизм планирования автоматизации процесса не будет планировать обработку каких-либо событий для отключенной функции.</span><span class="sxs-lookup"><span data-stu-id="168af-113">Additionally, the process automation scheduling engine won't schedule any occurrences or background processes for a disabled feature.</span></span> <span data-ttu-id="168af-114">Повторное включение функции приведет к немедленному запуску любых запланированных событий или фоновых процессов в прошлом.</span><span class="sxs-lookup"><span data-stu-id="168af-114">Re-enabling the feature will cause any scheduled occurrences or background processes in the past to run immediately.</span></span>

## <a name="calendar-view"></a><span data-ttu-id="168af-115">Представление календаря</span><span class="sxs-lookup"><span data-stu-id="168af-115">Calendar view</span></span>

<span data-ttu-id="168af-116">Одним из ключевых преимуществ автоматизации процессов является возможность видеть запланированную работу в простом представлении календаря.</span><span class="sxs-lookup"><span data-stu-id="168af-116">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="168af-117">Это представление позволяет видеть работу за неделю.</span><span class="sxs-lookup"><span data-stu-id="168af-117">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="168af-118">Это представление будет отображаться в правой части страницы **Автоматизация процессов**.</span><span class="sxs-lookup"><span data-stu-id="168af-118">You'll see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="168af-119">Оно будет заполнено запланированной работой для выбранных серий.</span><span class="sxs-lookup"><span data-stu-id="168af-119">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="168af-120">[![Календарь автоматизации процессов](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="168af-120">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="168af-121">Изменения вхождений</span><span class="sxs-lookup"><span data-stu-id="168af-121">Occurrence changes</span></span>

<span data-ttu-id="168af-122">Каждое вхождение можно изменить без воздействия на другие вхождения, определяемые серией, из которой они происходят.</span><span class="sxs-lookup"><span data-stu-id="168af-122">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="168af-123">Вхождения запланированной работы можно изменить из представления календаря, нажав кнопку **Просмотреть/изменить** и выбрав пункт **Вхождение**.</span><span class="sxs-lookup"><span data-stu-id="168af-123">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="168af-124">Эта страница позволяет получить доступ ко всем настройкам, первоначально отображаемым в мастере настройки серии, и предоставляет возможность выполнить одно изменение для выбранного вхождения.</span><span class="sxs-lookup"><span data-stu-id="168af-124">This page allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="168af-125">Вхождение запланированной работы также может быть отключено нажатием кнопки **Отключить** в представлении календаря.</span><span class="sxs-lookup"><span data-stu-id="168af-125">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span>

## <a name="developer-documentation"></a><span data-ttu-id="168af-126">Документация Разработчика</span><span class="sxs-lookup"><span data-stu-id="168af-126">Developer documentation</span></span>

<span data-ttu-id="168af-127">Платформа автоматизации процессов позволяет разработчикам расширять платформу автоматизации процессов.</span><span class="sxs-lookup"><span data-stu-id="168af-127">The process automation framework allows developers to extend the process automation framework.</span></span> <span data-ttu-id="168af-128">В документации по [платформе автоматизации процессов](../process-automation/process-automation-framework.md) представлена информация о том, как создавать пользовательские процессы, которые должны выполняться сервером обработки пакетных заданий, запланированные мастером автоматизации процессов и отображаемые в представлении календаря автоматически.</span><span class="sxs-lookup"><span data-stu-id="168af-128">The [Process automation framework](../process-automation/process-automation-framework.md) documentation provides information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]