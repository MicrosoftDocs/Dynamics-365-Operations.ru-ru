---
title: Устранение неполадок формирования загрузок и отгрузок
description: В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с формированием загрузок и отгрузок в Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 2933bcfd2cc526e39a4e1343cd472334a5b95607
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645340"
---
# <a name="troubleshoot-load-building-and-shipments"></a><span data-ttu-id="4c537-103">Устранение неполадок формирования загрузок и отгрузок</span><span class="sxs-lookup"><span data-stu-id="4c537-103">Troubleshoot load building and shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c537-104">В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с формированием загрузок и отгрузок в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4c537-104">This topic describes how to fix common issues that you might encounter while you work with load building and shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a><span data-ttu-id="4c537-105">Получено следующее сообщение об ошибке: "Невозможно создать строку загрузки для данной строки заказа, так как она содержит недопустимые складские аналитики..."</span><span class="sxs-lookup"><span data-stu-id="4c537-105">I receive the following error message: "You can't create a load line for this order line because it contains inventory dimensions that are invalid..."</span></span>

### <a name="issue-description"></a><span data-ttu-id="4c537-106">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="4c537-106">Issue description</span></span>

<span data-ttu-id="4c537-107">При попытке выпуска возврата заказа на продажу на склад появляется следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="4c537-107">You receive the following error message when you try to release a return sales order to the warehouse:</span></span>

> <span data-ttu-id="4c537-108">Невозможно создать строку загрузки для данной строки заказа, так как она содержит недопустимые складские аналитики.</span><span class="sxs-lookup"><span data-stu-id="4c537-108">You can't create a load line for this order line because it contains inventory dimensions that are invalid.</span></span> <span data-ttu-id="4c537-109">Нельзя ссылаться на складские аналитики, расположенные под аналитикой местоположения в иерархии резервирования.</span><span class="sxs-lookup"><span data-stu-id="4c537-109">You can't reference inventory dimensions that are located below the location dimension in the reservation hierarchy.</span></span> <span data-ttu-id="4c537-110">Удалите недопустимые аналитики из строки заказа.</span><span class="sxs-lookup"><span data-stu-id="4c537-110">Remove the invalid dimensions from the order line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4c537-111">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="4c537-111">Issue resolution</span></span>

<span data-ttu-id="4c537-112">К сожалению, продукт не поддерживает обработку загрузки для процесса возврата продажи.</span><span class="sxs-lookup"><span data-stu-id="4c537-112">Unfortunately, the product doesn't support load processing for a sales return process.</span></span> <span data-ttu-id="4c537-113">Поэтому невозможно выпустить возврат заказа на продажу на склад.</span><span class="sxs-lookup"><span data-stu-id="4c537-113">Therefore, you can't release the return sales order to the warehouse.</span></span>

<span data-ttu-id="4c537-114">В транзакциях заказа на продажу нельзя ссылаться на складские аналитики, расположенные под аналитикой **Местоположение** в иерархии резервирования.</span><span class="sxs-lookup"><span data-stu-id="4c537-114">On sales order transactions, you can't reference inventory dimensions that are located below the **Location** dimension in the reservation hierarchy.</span></span> <span data-ttu-id="4c537-115">Для разрешения неполадки удалите недопустимые аналитики из строки заказа.</span><span class="sxs-lookup"><span data-stu-id="4c537-115">The resolution is to remove the invalid dimensions from the order line.</span></span>

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a><span data-ttu-id="4c537-116">Получено следующее сообщение об ошибке: "Одна из строк уже находится в загрузке.</span><span class="sxs-lookup"><span data-stu-id="4c537-116">I receive the following error message: "One of the lines is already on a load.</span></span> <span data-ttu-id="4c537-117">Невозможно выпустить на склад."</span><span class="sxs-lookup"><span data-stu-id="4c537-117">Unable to release to warehouse."</span></span>

### <a name="issue-description"></a><span data-ttu-id="4c537-118">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="4c537-118">Issue description</span></span>

<span data-ttu-id="4c537-119">При создании вручную загрузок или при настройке процесса таким образом, чтобы загрузка уже была создана до ввода строки заказа на продажу, предполагается, что последующий выпуск будет выполнен вручную, и будут использоваться маршрут и рейтинг из загрузки.</span><span class="sxs-lookup"><span data-stu-id="4c537-119">If you manually create loads, or if you set up the process so that loads are already created before sales order line entry occurs, the assumption is that the subsequent release will be done manually, and that the route and rating from the load will be used.</span></span>

<span data-ttu-id="4c537-120">В другом возможном сценарии выполняется попытка автоматического выпуска на склад, но процессу волны не удалось создать работу.</span><span class="sxs-lookup"><span data-stu-id="4c537-120">In another possible scenario, you're trying to do an automatic release to the warehouse, but the wave process failed to create work.</span></span> <span data-ttu-id="4c537-121">Поэтому открытая отгрузка или загрузка все еще создаются.</span><span class="sxs-lookup"><span data-stu-id="4c537-121">Therefore, an open shipment or load is still created.</span></span> <span data-ttu-id="4c537-122">Эта открытая отгрузка или загрузка затем блокирует последующие попытки автоматического выпуска заказа до тех пор, пока не будет удалена открытая отгрузка или загрузка или не будет вручную выполнена повторная обработка волны.</span><span class="sxs-lookup"><span data-stu-id="4c537-122">This open shipment or load then blocks subsequent attempts to automatically release the order until you either delete the open shipment or load, or manually reprocess the wave.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4c537-123">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="4c537-123">Issue resolution</span></span>

<span data-ttu-id="4c537-124">Можно выполнить выпуск со страницы заказа на продажу, или автоматический выпуск может быть выполнен со страницы выпуска заказа на продажу, только если загрузка не существовала перед выпуском на склад.</span><span class="sxs-lookup"><span data-stu-id="4c537-124">You can release from the sales order page, or automatic release can be done from the release sales order page, only if no load exists before the release to the warehouse.</span></span> <span data-ttu-id="4c537-125">Загрузка будет создана автоматически после обработки волны.</span><span class="sxs-lookup"><span data-stu-id="4c537-125">The load will automatically be created after the wave is processed.</span></span>

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a><span data-ttu-id="4c537-126">Получено следующее сообщение об ошибке: "Исправление уведомления о поставке не может быть обработано.</span><span class="sxs-lookup"><span data-stu-id="4c537-126">I receive the following error message: "The delivery note correction can't be processed.</span></span> <span data-ttu-id="4c537-127">Уведомление о поставке содержит только номенклатуры, которые подлежат процессам управления складом, так как они не поддерживаются исправлением уведомления о поставке."</span><span class="sxs-lookup"><span data-stu-id="4c537-127">The delivery note only contains items that are subject to warehouse management processes, as these are not supported by Delivery Note correction."</span></span>

### <a name="issue-description"></a><span data-ttu-id="4c537-128">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="4c537-128">Issue description</span></span>

<span data-ttu-id="4c537-129">После разноски уведомления о поставке его невозможно отменить, так как кнопка **Отмена** недоступна.</span><span class="sxs-lookup"><span data-stu-id="4c537-129">After you post a delivery note, you can't cancel it, because the **Cancel** button is unavailable.</span></span> <span data-ttu-id="4c537-130">Вы также не можете скорректировать уведомление о поставке.</span><span class="sxs-lookup"><span data-stu-id="4c537-130">You also can't correct the delivery note.</span></span> <span data-ttu-id="4c537-131">Если вы попробуете, появится следующее сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4c537-131">If you try, you receive this error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4c537-132">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="4c537-132">Issue resolution</span></span>

<span data-ttu-id="4c537-133">Для корректировки разнесенных отборочных накладных для номенклатур, включенных для расширенного управления складом (WMS), разноска должна выполняться из загрузки, а не напрямую из заказа.</span><span class="sxs-lookup"><span data-stu-id="4c537-133">To correct posted packing slips for items that are enabled for advanced warehouse management (WMS), you must do the posting from the load, not directly from the order.</span></span>

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a><span data-ttu-id="4c537-134">Как можно создавать работу на основе исходящих загрузок вместо волн?</span><span class="sxs-lookup"><span data-stu-id="4c537-134">How can I create work from outbound loads instead of waves?</span></span>

### <a name="issue-description"></a><span data-ttu-id="4c537-135">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="4c537-135">Issue description</span></span>

<span data-ttu-id="4c537-136">Вот один из способов воспроизвести эту проблему.</span><span class="sxs-lookup"><span data-stu-id="4c537-136">Here is one way to reproduce this issue.</span></span>

1. <span data-ttu-id="4c537-137">Создайте исходящую загрузку с помощью заказа на продажу или заказа перемещения.</span><span class="sxs-lookup"><span data-stu-id="4c537-137">Create an outbound load by using a sales order or transfer order.</span></span>
2. <span data-ttu-id="4c537-138">Запустить загрузку в складе.</span><span class="sxs-lookup"><span data-stu-id="4c537-138">Release the load to the warehouse.</span></span>
3. <span data-ttu-id="4c537-139">Обратите внимание, что еще не было создано ни одной работы комплектации.</span><span class="sxs-lookup"><span data-stu-id="4c537-139">Notice that no picking work has yet been generated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4c537-140">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="4c537-140">Issue resolution</span></span>

<span data-ttu-id="4c537-141">Если работа должна быть создана сразу после выпуска загрузки, необходимо соответствующим образом настроить шаблон волны.</span><span class="sxs-lookup"><span data-stu-id="4c537-141">If work must be generated immediately when the load is released, you must configure the wave template accordingly.</span></span> <span data-ttu-id="4c537-142">В шаблоне волны задайте для следующих параметров значение *Да*:</span><span class="sxs-lookup"><span data-stu-id="4c537-142">On the wave template, set the following options to *Yes*:</span></span>

- <span data-ttu-id="4c537-143">Создавать волны автоматически</span><span class="sxs-lookup"><span data-stu-id="4c537-143">Automate wave creation</span></span>
- <span data-ttu-id="4c537-144">Обрабатывать волну перед запуском на склад</span><span class="sxs-lookup"><span data-stu-id="4c537-144">Process wave at release to warehouse</span></span>
- <span data-ttu-id="4c537-145">Автоматический запуск волны</span><span class="sxs-lookup"><span data-stu-id="4c537-145">Automate wave release</span></span>

## <a name="i-cant-re-release-a-partially-shipped-load"></a><span data-ttu-id="4c537-146">Невозможно повторно выпустить частичную загрузку.</span><span class="sxs-lookup"><span data-stu-id="4c537-146">I can't re-release a partially shipped load.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4c537-147">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="4c537-147">Issue description</span></span>

<span data-ttu-id="4c537-148">Невозможно выпустить частично отгруженную загрузку на склад.</span><span class="sxs-lookup"><span data-stu-id="4c537-148">You can't release a partially shipped load to the warehouse.</span></span> <span data-ttu-id="4c537-149">При выполнении выпуска на склад появляется сообщение "Операция завершена", но ничего не происходит, и работа для оставшегося количества не создается.</span><span class="sxs-lookup"><span data-stu-id="4c537-149">When you do the release to the warehouse, an "Operation complete" message appears, but nothing happens, and no work is created for the remaining quantity.</span></span> <span data-ttu-id="4c537-150">Эта проблема возникает при использовании функциональности транспортной загрузки и неполного резервирования.</span><span class="sxs-lookup"><span data-stu-id="4c537-150">This issue occurs when you use transport load functionality and there is an incomplete reservation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4c537-151">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="4c537-151">Issue resolution</span></span>

<span data-ttu-id="4c537-152">[Проблема статьи базы знаний 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Частично отгруженные загрузки могут быть повторно обработаны волной и повторно обработаны") исправлена в [выпуске 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span><span class="sxs-lookup"><span data-stu-id="4c537-152">[KB issue 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Partially shipped loads can be re-waved and re-processed") is fixed in [release 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span></span>
