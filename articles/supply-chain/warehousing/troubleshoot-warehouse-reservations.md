---
title: Устранение неполадок резервирования в модуле "Управление складом"
description: В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с резервированием на складе в Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6151797001b1ccdb7e371c70b90c304a5ab422d8
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645128"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="612d1-103">Устранение неполадок резервирования в модуле "Управление складом"</span><span class="sxs-lookup"><span data-stu-id="612d1-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="612d1-104">В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с резервированием на складе в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="612d1-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="612d1-105">Я получаю следующее сообщение об ошибке: "Не удается удалить резервирования в связи с наличием зависимой от них работы."</span><span class="sxs-lookup"><span data-stu-id="612d1-105">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="612d1-106">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="612d1-106">Issue description</span></span>

<span data-ttu-id="612d1-107">Нельзя отменять резервирование запасов в строке продаж, так как с этой строкой связана открытая работа.</span><span class="sxs-lookup"><span data-stu-id="612d1-107">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="612d1-108">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="612d1-108">Issue resolution</span></span>

<span data-ttu-id="612d1-109">Выясните, существует ли открытая работа группы упаковки, чтобы переместить номенклатуру из станции упаковки в другое местоположение (например, *Дверь отсека*).</span><span class="sxs-lookup"><span data-stu-id="612d1-109">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="612d1-110">Просмотрите записи на страницах **Журнал создания работ** и **Сведения о работе**, чтобы определить, что физически резервирует запасы, а затем выполните или удалите работу, чтобы освободить резервирование.</span><span class="sxs-lookup"><span data-stu-id="612d1-110">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="612d1-111">Я получают следующее сообщение об ошибке: "Количество запасов -%1 не удалось обновить из-за недостаточности складских проводок для номенклатуры %2...."</span><span class="sxs-lookup"><span data-stu-id="612d1-111">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="612d1-112">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="612d1-112">Issue description</span></span>

<span data-ttu-id="612d1-113">Эта проблема может возникнуть, если система не может обновить количество запасов из-за того, что отсутствуют достаточные складские проводки с указанными аналитиками.</span><span class="sxs-lookup"><span data-stu-id="612d1-113">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="612d1-114">Ниже приведен весь текст полного сообщения об ошибке:</span><span class="sxs-lookup"><span data-stu-id="612d1-114">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="612d1-115">Количество запасов -%1 не удалось обновить из-за недостаточности складских проводок для номенклатуры %2 с аналитиками Размер=%3, Цвет=%4, Дополнения=%5, Сайт=%6, Склад=%7, Местонахождение=%8, Состояние запасов=Доступно, Грузоместо=%9, Новер партии=%10 для ссылочного кода %11 с номером лота %12.</span><span class="sxs-lookup"><span data-stu-id="612d1-115">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="612d1-116">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="612d1-116">Issue resolution</span></span>

<span data-ttu-id="612d1-117">Убедитесь, что никакие складские проводки не выполняют физическое резервирование количества.</span><span class="sxs-lookup"><span data-stu-id="612d1-117">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="612d1-118">Например, эти проводки могут открывать заказы контроля качества, записи блокировки запасов или заказы на выпуск.</span><span class="sxs-lookup"><span data-stu-id="612d1-118">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="612d1-119">Получено следующее сообщение об ошибке: "Физические запасы в наличии...невозможно зарезервировать, так как в запасе доступно только 0,00."</span><span class="sxs-lookup"><span data-stu-id="612d1-119">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="612d1-120">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="612d1-120">Issue description</span></span>

<span data-ttu-id="612d1-121">Эта проблема может возникнуть, если система не может обновить количество запасов из-за того, что отсутствуют достаточные складские проводки с указанными аналитиками.</span><span class="sxs-lookup"><span data-stu-id="612d1-121">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="612d1-122">Ниже приведен весь текст полного сообщения об ошибке:</span><span class="sxs-lookup"><span data-stu-id="612d1-122">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="612d1-123">Физические запасы в наличии Сайт=%1, Склад=%2, Состояние запасов=Доступно, Номер партии=%3, Владелец=%4: %5 невозможно зарезервировать, так как в запасах доступно только 0,00.</span><span class="sxs-lookup"><span data-stu-id="612d1-123">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="612d1-124">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="612d1-124">Issue resolution</span></span>

<span data-ttu-id="612d1-125">Вероятно, эта проблема вызвана открытой работой.</span><span class="sxs-lookup"><span data-stu-id="612d1-125">This issue is probably caused by open work.</span></span> <span data-ttu-id="612d1-126">Завершите работу или выполните получение без создания работы.</span><span class="sxs-lookup"><span data-stu-id="612d1-126">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="612d1-127">Убедитесь, что никакие складские проводки не выполняют физическое резервирование количества.</span><span class="sxs-lookup"><span data-stu-id="612d1-127">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="612d1-128">Например, эти проводки могут открывать заказы контроля качества, записи блокировки запасов или заказы на выпуск.</span><span class="sxs-lookup"><span data-stu-id="612d1-128">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="612d1-129">Получено следующее сообщение об ошибке: "Для назначения волне в строках загрузки должны быть указаны аналитики, находящийся над местоположением.</span><span class="sxs-lookup"><span data-stu-id="612d1-129">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="612d1-130">Чтобы назначить эти аналитики, зарезервируйте и заново создайте строку загрузки."</span><span class="sxs-lookup"><span data-stu-id="612d1-130">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="612d1-131">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="612d1-131">Issue description</span></span>

<span data-ttu-id="612d1-132">При использовании номенклатуры, имеющей иерархию резервирования "пакет выше" (если аналитика **Номер партии** помещается *над* аналитикой **Местоположение**), команда **Выпуск в склад** на странице **Рабочее место планирования загрузки** для неполного количества не работает.</span><span class="sxs-lookup"><span data-stu-id="612d1-132">When you use an item that has a "batch above" reservation hierarchy (with the **Batch number** dimension placed *above* the **Location** dimension), the **Release to warehouse** command on the **Load planning workbench** page for a partial quantity doesn't work.</span></span> <span data-ttu-id="612d1-133">Выводится это сообщение об ошибке, и работа с частичным количеством не создается.</span><span class="sxs-lookup"><span data-stu-id="612d1-133">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="612d1-134">Однако при использовании номенклатуры, имеющей иерархию резервирования "пакет ниже" (когда аналитика **Номер партии** помещается *под* аналитикой **Местоположение**), вы можете выпустить загрузку со страницы **Рабочее место планирования загрузки** для неполного количества.</span><span class="sxs-lookup"><span data-stu-id="612d1-134">However, if you use an item that has a "batch below" reservation hierarchy (with the **Batch number** dimension placed *below* the **Location** dimension), you can release a load from the **Load planning workbench** page for a partial quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="612d1-135">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="612d1-135">Issue resolution</span></span>

<span data-ttu-id="612d1-136">Такое поведение предусмотрено разработчиками.</span><span class="sxs-lookup"><span data-stu-id="612d1-136">This behavior is by design.</span></span> <span data-ttu-id="612d1-137">Если поместить аналитику над аналитикой **Местоположение** в иерархии резервирования, она должна быть указана до выпуска на склад.</span><span class="sxs-lookup"><span data-stu-id="612d1-137">If you put a dimension above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="612d1-138">Корпорация Майкрософт проверила эту проблему и определила, что она является ограничением функций в ходе выпусков на склад с помощью средства планирования загрузки.</span><span class="sxs-lookup"><span data-stu-id="612d1-138">Microsoft has evaluated this issue and has determined that it's a feature limitation during releases to the warehouse from the load planning workbench.</span></span> <span data-ttu-id="612d1-139">Частичные количества не могут быть выпущены, если не указана одна или несколько аналитик, расположенных выше аналитики **Местоположение**.</span><span class="sxs-lookup"><span data-stu-id="612d1-139">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

<span data-ttu-id="612d1-140">Дополнительные сведения см. в разделе [Гибкая политика резервирования аналитик на уровне склада](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="612d1-140">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>
