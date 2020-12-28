---
title: Группы перевозчиков
description: В этой теме описывается, как настроить данные для групп перевозчиков.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2570479edac9bc8cc7aa998a8b69f54ffc10cd61
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646430"
---
# <a name="carrier-groups"></a><span data-ttu-id="d48e9-103">Группы перевозчиков</span><span class="sxs-lookup"><span data-stu-id="d48e9-103">Carrier groups</span></span>

<span data-ttu-id="d48e9-104">Группа перевозчиков — это совокупность перевозчиков и услуг перевозчиков.</span><span class="sxs-lookup"><span data-stu-id="d48e9-104">A carrier group is a collection of shipping carriers and carrier services.</span></span> <span data-ttu-id="d48e9-105">Каждая группа перевозчиков определяет предпочтительную последовательность для перевозчиков и услуг перевозчиков, которые относятся к этой группе.</span><span class="sxs-lookup"><span data-stu-id="d48e9-105">Each carrier group specifies the preferred sequence for the shipping carriers and carrier services that belong to it.</span></span>

<span data-ttu-id="d48e9-106">Когда для одного сегмента маршрута существует несколько перевозчиков и услуг перевозчиков, можно указать группу перевозчиков вместо конкретного перевозчика и услуги перевозчика в плане маршрута или в руководстве по маршруту.</span><span class="sxs-lookup"><span data-stu-id="d48e9-106">When multiple shipping carriers and carrier services exist for the same route segment, you can specify a carrier group instead of a specific shipping carrier and carrier service in the route plan or route guide.</span></span>

## <a name="create-a-carrier-group"></a><span data-ttu-id="d48e9-107">Создание группы перевозчиков</span><span class="sxs-lookup"><span data-stu-id="d48e9-107">Create a carrier group</span></span>

1. <span data-ttu-id="d48e9-108">Перейдите в раздел **Управление транспортировкой &gt; Настройка &gt; Перевозчики &gt; Группа перевозчиков**.</span><span class="sxs-lookup"><span data-stu-id="d48e9-108">Go to **Transportation management &gt; Setup &gt; Carriers &gt; Carrier group**.</span></span>
1. <span data-ttu-id="d48e9-109">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d48e9-109">Select **New**.</span></span>
1. <span data-ttu-id="d48e9-110">В поле **Группа перевозчиков** введите уникальный код (ИД) для группы.</span><span class="sxs-lookup"><span data-stu-id="d48e9-110">In the **Carrier group** field, enter a unique identifier (ID) for the group.</span></span>
1. <span data-ttu-id="d48e9-111">В поле **Имя** введите описательное имя для группы.</span><span class="sxs-lookup"><span data-stu-id="d48e9-111">In the **Name** field, enter a descriptive name for the group.</span></span>
1. <span data-ttu-id="d48e9-112">На экспресс-вкладке **Сведения** добавьте строку и выберите перевозчика и услугу перевозчика для него.</span><span class="sxs-lookup"><span data-stu-id="d48e9-112">On the **Details** FastTab, add a row, and select a shipping carrier and a carrier service for it.</span></span> <span data-ttu-id="d48e9-113">Повторяйте этот шаг до тех пор, пока не будет добавлено столько перевозчиков, сколько требуется для группы.</span><span class="sxs-lookup"><span data-stu-id="d48e9-113">Repeat this step until you've added as many carriers as you require for the group.</span></span>
1. <span data-ttu-id="d48e9-114">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d48e9-114">Close the page.</span></span>
