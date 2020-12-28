---
title: Домашняя страница управления затратами
description: Управление затратами позволяет обрабатывать оценку и учет сырья, незаконченных товаров, готовых изделий и средств незавершенного производства.
author: AndersGirke
manager: tfehr
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9caea2d41e6d3ba74e4d156d8aeae6c4693ce7e2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436180"
---
# <a name="cost-management-home-page"></a><span data-ttu-id="f351d-103">Домашняя страница управления затратами</span><span class="sxs-lookup"><span data-stu-id="f351d-103">Cost management home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f351d-104">[Управление затратами (видео)](https://www.youtube.com/watch?v=vXzlC-mOBcg&feature=youtu.be) позволяет работать с оценкой и учетом сырья, незаконченных товаров, готовых изделий и средств незавершенного производства.</span><span class="sxs-lookup"><span data-stu-id="f351d-104">[Cost management (video)](https://www.youtube.com/watch?v=vXzlC-mOBcg&feature=youtu.be) lets you work with the valuation and accounting of raw materials, semi-finished goods, finished goods, and work-in-progress assets.</span></span> <span data-ttu-id="f351d-105">Это процесс определения, управления и отчетности для [складского учета](cost-object.md) и [учета производства](bom-calculations.md).</span><span class="sxs-lookup"><span data-stu-id="f351d-105">It is the process of defining, managing, and reporting [Inventory accounting](cost-object.md) and [Manufacturing accounting](bom-calculations.md).</span></span>

<span data-ttu-id="f351d-106">Можно определить политики затрат в следующих областях:</span><span class="sxs-lookup"><span data-stu-id="f351d-106">You can define cost policies in the following areas:</span></span>

- [<span data-ttu-id="f351d-107">Заранее определенные затраты</span><span class="sxs-lookup"><span data-stu-id="f351d-107">Predetermined cost</span></span>](costing-versions.md)
- [<span data-ttu-id="f351d-108">Учет запасов</span><span class="sxs-lookup"><span data-stu-id="f351d-108">Inventory accounting</span></span>](cost-object.md)
- [<span data-ttu-id="f351d-109">Учет производства</span><span class="sxs-lookup"><span data-stu-id="f351d-109">Manufacturing accounting</span></span>](bom-calculations.md)
- [<span data-ttu-id="f351d-110">Учет косвенных затрат</span><span class="sxs-lookup"><span data-stu-id="f351d-110">Indirect cost accounting</span></span>](costing-sheets.md)
- [<span data-ttu-id="f351d-111">Интеграция с ГК</span><span class="sxs-lookup"><span data-stu-id="f351d-111">Ledger integration</span></span>](production-order-cost-analysis.md)

<span data-ttu-id="f351d-112">Например, можно определить, какие методы оценки запасов, такие как [ФИФО](fifo-physical-value-marking.md), [взвешенное среднее](weighted-average-physical-value-marking.md), [стандартная себестоимость](prerequisites-standard-costs.md) или [скользящее среднее](moving-average.md), требуется применить к продуктам в [группе моделей номенклатуры](../inventory/reserve-inventory-quantities.md) в складском учете.</span><span class="sxs-lookup"><span data-stu-id="f351d-112">For example, you can define which inventory valuation methods, such as [FIFO](fifo-physical-value-marking.md), [Weighted average](weighted-average-physical-value-marking.md), [Standard cost](prerequisites-standard-costs.md), or [Moving average](moving-average.md) that you want to apply to products in the [Item model group](../inventory/reserve-inventory-quantities.md) in Inventory accounting.</span></span>

<span data-ttu-id="f351d-113">Доступ к учету запасов и учету производства возможен из рабочих областей **Администрирование затрат** и **Анализ затрат**.</span><span class="sxs-lookup"><span data-stu-id="f351d-113">You can access Inventory accounting and Manufacturing accounting from the **Cost administration** and **Cost analysis** workspaces.</span></span> <span data-ttu-id="f351d-114">Эти рабочие области дают полный обзор текущего состояния, ключевых индикаторов производительности (KPI) и обнаружения отклонения.</span><span class="sxs-lookup"><span data-stu-id="f351d-114">These workspaces provide a comprehensive overview of the current status, key performance indicators (KPIs), and detection of deviation.</span></span> 

<span data-ttu-id="f351d-115">Учет производства позволяет обрабатывать [позаказную калькуляцию себестоимости](production-order-cost-analysis.md) в производственных заказах и заказах партий, а также [backflush-расчет себестоимости](backflush-costing.md) для бережливого производства.</span><span class="sxs-lookup"><span data-stu-id="f351d-115">Manufacturing accounting lets you handle [Job order costing](production-order-cost-analysis.md) in production orders and batch orders, as well as [Backflush costing](backflush-costing.md) in lean manufacturing.</span></span>

<span data-ttu-id="f351d-116">[Содержимое Power BI "Управление затратами"](../../dev-itpro/analytics/cost-management-content-pack.md) предоставляет управленческие сведения о запасах и запасах по незавершенному производству (НЗП), а также о потоках затрат через них по категориям с течением времени.</span><span class="sxs-lookup"><span data-stu-id="f351d-116">The [Cost management Power BI content](../../dev-itpro/analytics/cost-management-content-pack.md) provides managerial insight into inventory and work-in-progress (WIP) inventory, and how cost flows through them by category over time.</span></span> <span data-ttu-id="f351d-117">Информация может также использоваться как подробное приложение к финансовой отчетности.</span><span class="sxs-lookup"><span data-stu-id="f351d-117">The information can also be used as a detailed supplement to the financial statement.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="f351d-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f351d-118">Additional resources</span></span>

#### <a name="whats-new-and-in-development"></a><span data-ttu-id="f351d-119">Новые возможности и текущие разработки</span><span class="sxs-lookup"><span data-stu-id="f351d-119">What's new and in development</span></span>

<span data-ttu-id="f351d-120">Перейдите в раздел [Дорожная карта Microsoft Dynamics 365](https://roadmap.dynamics.com/), чтобы узнать, какие новые функции уже выпущены, а какие еще находятся в разработке.</span><span class="sxs-lookup"><span data-stu-id="f351d-120">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span>

#### <a name="white-paper"></a><span data-ttu-id="f351d-121">Информационный документ</span><span class="sxs-lookup"><span data-stu-id="f351d-121">White paper</span></span>

<span data-ttu-id="f351d-122">В разделе [Расчет спецификации с использованием схемы калькуляции](https://www.microsoft.com/download/details.aspx?id=101937) описывается, как настроить схему калькуляции, включающую материал и производство, и как настройка влияет на результаты расчета спецификации.</span><span class="sxs-lookup"><span data-stu-id="f351d-122">[BOM calculation by using a costing sheet](https://www.microsoft.com/download/details.aspx?id=101937) describes how to set up a costing sheet that includes material and manufacturing, and how the setup affects the BOM calculation results.</span></span> <span data-ttu-id="f351d-123">Для более подробного объяснения этих тем предоставлены конкретные сценарии и данные, которые демонстрируются влияние различных параметров и конфигураций.</span><span class="sxs-lookup"><span data-stu-id="f351d-123">To better explain the topics, it provides concrete scenarios and data that demonstrates the effect of the various settings and configurations.</span></span>

#### <a name="blogs"></a><span data-ttu-id="f351d-124">Блоги</span><span class="sxs-lookup"><span data-stu-id="f351d-124">Blogs</span></span>

<span data-ttu-id="f351d-125">В [блоге группы исследований производства Dynamics AX](https://blogs.msdn.microsoft.com/axmfg) и в [блоге группы исследований Supply Chain Management в Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm) можно найти мнения, новости и другие сведения об управлении затратами.</span><span class="sxs-lookup"><span data-stu-id="f351d-125">You can find opinions, news, and other information about Cost management on the [Dynamics AX Manufacturing R&D Team blog](https://blogs.msdn.microsoft.com/axmfg) and [Supply Chain Management in Dynamics AX R&D Team blog](https://blogs.msdn.microsoft.com/dynamicsaxscm).</span></span> <span data-ttu-id="f351d-126">Хотя некоторые из этих записей посвящены предыдущей версии модуля "Управление затратами", обсуждаемые в них понятия по-прежнему применяются, а процедуры аналогичны процедурам в текущей версии.</span><span class="sxs-lookup"><span data-stu-id="f351d-126">Although some of these posts were written for the previous version of Cost management, the same concepts still apply, and the procedures are also similar in the current version.</span></span>

#### <a name="task-guides"></a><span data-ttu-id="f351d-127">Проводники по задачам</span><span class="sxs-lookup"><span data-stu-id="f351d-127">Task guides</span></span>

<span data-ttu-id="f351d-128">Дополнительная справка доступна в виде руководств по задачам.</span><span class="sxs-lookup"><span data-stu-id="f351d-128">Additional help is available as task guides.</span></span> <span data-ttu-id="f351d-129">Чтобы перейти к проводникам по задачам, нажмите кнопку "Справка" на любой странице.</span><span class="sxs-lookup"><span data-stu-id="f351d-129">To access task guides, click the Help button on any page.</span></span>