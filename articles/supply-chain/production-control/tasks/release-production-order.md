---
title: Выпуск производственного заказа
description: В этой процедуре показано, как запустить в производство производственный заказ.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmRelease, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e98adea620d74bdb7a90cedc9b256d9883b27525
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148988"
---
# <a name="release-a-production-order"></a><span data-ttu-id="15533-103">Выпуск производственного заказа</span><span class="sxs-lookup"><span data-stu-id="15533-103">Release a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="15533-104">В этой процедуре показано, как запустить в производство производственный заказ.</span><span class="sxs-lookup"><span data-stu-id="15533-104">This procedure shows how to release a production order.</span></span> <span data-ttu-id="15533-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="15533-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="15533-106">Это четвертая из семи процедур, которая объясняет жизненный цикл производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="15533-106">This is the fourth procedure out of seven which explains the production order lifecycle.</span></span>

1. <span data-ttu-id="15533-107">Перейдите в раздел "Управление производством" > "Производственные заказы" > "Все производственные заказы".</span><span class="sxs-lookup"><span data-stu-id="15533-107">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="15533-108">В сетке выберите производственный заказ со статусом "Запланировано".</span><span class="sxs-lookup"><span data-stu-id="15533-108">In the grid, select a production order that has the Scheduled status.</span></span>  
2. <span data-ttu-id="15533-109">В области действий щелкните "Производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="15533-109">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="15533-110">Щелкните "Запуск в производство".</span><span class="sxs-lookup"><span data-stu-id="15533-110">Click Release.</span></span>
    * <span data-ttu-id="15533-111">На этой странице можно подтвердить выпуск выбранного диапазона производственных заказов.</span><span class="sxs-lookup"><span data-stu-id="15533-111">On this page, you can confirm the release of the selected range of production orders.</span></span> <span data-ttu-id="15533-112">Щелкните "Выбрать" для добавления заказов.</span><span class="sxs-lookup"><span data-stu-id="15533-112">Click Select if you want to add orders.</span></span>  
    * <span data-ttu-id="15533-113">Шаг "Запуск в производство" указывает, когда производственный заказ запускается в производство в цехе производства, чтобы операторы цеха могли сообщать о ходе выполнения производственных заданий.</span><span class="sxs-lookup"><span data-stu-id="15533-113">The Release step indicates when the production order is released to the production shop floor so that the shop floor operators can report progress on the production jobs.</span></span> <span data-ttu-id="15533-114">Можно выпустить производственные документы, содержащие соответствующую информацию об обработке заданий.</span><span class="sxs-lookup"><span data-stu-id="15533-114">Production papers that contain relevant information about processing the jobs can be issued.</span></span> <span data-ttu-id="15533-115">Работа склада для комплектации сырья создается для номенклатур, настроенных для процесса склада.</span><span class="sxs-lookup"><span data-stu-id="15533-115">The warehouse work for raw material picking is generated for the items that are set up for the warehouse process.</span></span>  
4. <span data-ttu-id="15533-116">Перейдите на вкладку "Общие".</span><span class="sxs-lookup"><span data-stu-id="15533-116">Click the General tab.</span></span>
    * <span data-ttu-id="15533-117">Выберите, какие отчеты по производству следует напечатать.</span><span class="sxs-lookup"><span data-stu-id="15533-117">Select which production reports should be printed.</span></span> <span data-ttu-id="15533-118">В отчете по карте задания печатается одна страница для каждого запланированного задания, и для него требуется запланировать производственный заказ на уровне работы.</span><span class="sxs-lookup"><span data-stu-id="15533-118">The Job card report prints a page for each scheduled job and requires the production order to be scheduled at the job level.</span></span> <span data-ttu-id="15533-119">Отчет содержит сведения о запланированном времени начала и окончания, количестве для производства и ресурсах, обрабатывающих задание.</span><span class="sxs-lookup"><span data-stu-id="15533-119">The report contains information about the scheduled start and end time, the quantity to produce, and which resource processes the job.</span></span> <span data-ttu-id="15533-120">В отчете о маршрутных заданиях указывается та же информация на той же странице, но не печатается страница для каждого задания.</span><span class="sxs-lookup"><span data-stu-id="15533-120">The Route job report collects the same information on the same page, but does not print a page for each job.</span></span> <span data-ttu-id="15533-121">В отчете по карте маршрута отображаются только операции, но не задания.</span><span class="sxs-lookup"><span data-stu-id="15533-121">The Route card report only shows the operations but not the jobs.</span></span> <span data-ttu-id="15533-122">Поэтому для данного отчета не требуется планирование заданий, но его можно использовать, когда производственные заказы планируются на уровне операций.</span><span class="sxs-lookup"><span data-stu-id="15533-122">Therefore, this report does not require job scheduling, but can be used when production orders are scheduled at the operation level.</span></span>  
5. <span data-ttu-id="15533-123">Установите флажок "Печать карты маршрута".</span><span class="sxs-lookup"><span data-stu-id="15533-123">Click the Print route card checkbox.</span></span>
6. <span data-ttu-id="15533-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="15533-124">Click OK.</span></span>
7. <span data-ttu-id="15533-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="15533-125">Close the page.</span></span>

