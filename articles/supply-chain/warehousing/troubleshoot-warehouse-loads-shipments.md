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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f49a91afe9281f912d6d3579ac8e52cb1d8e5b5d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994061"
---
# <a name="troubleshoot-load-building-and-shipments"></a><span data-ttu-id="e0d8c-103">Устранение неполадок формирования загрузок и отгрузок</span><span class="sxs-lookup"><span data-stu-id="e0d8c-103">Troubleshoot load building and shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0d8c-104">В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с формированием загрузок и отгрузок в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-104">This topic describes how to fix common issues that you might encounter while you work with load building and shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a><span data-ttu-id="e0d8c-105">Получено следующее сообщение об ошибке: "Невозможно создать строку загрузки для данной строки заказа, так как она содержит недопустимые складские аналитики..."</span><span class="sxs-lookup"><span data-stu-id="e0d8c-105">I receive the following error message: "You can't create a load line for this order line because it contains inventory dimensions that are invalid..."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e0d8c-106">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="e0d8c-106">Issue description</span></span>

<span data-ttu-id="e0d8c-107">При попытке выпуска возврата заказа на продажу на склад появляется следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="e0d8c-107">You receive the following error message when you try to release a return sales order to the warehouse:</span></span>

> <span data-ttu-id="e0d8c-108">Невозможно создать строку загрузки для данной строки заказа, так как она содержит недопустимые складские аналитики.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-108">You can't create a load line for this order line because it contains inventory dimensions that are invalid.</span></span> <span data-ttu-id="e0d8c-109">Нельзя ссылаться на складские аналитики, расположенные под аналитикой местоположения в иерархии резервирования.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-109">You can't reference inventory dimensions that are located below the location dimension in the reservation hierarchy.</span></span> <span data-ttu-id="e0d8c-110">Удалите недопустимые аналитики из строки заказа.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-110">Remove the invalid dimensions from the order line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e0d8c-111">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="e0d8c-111">Issue resolution</span></span>

<span data-ttu-id="e0d8c-112">К сожалению, продукт не поддерживает обработку загрузки для процесса возврата продажи.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-112">Unfortunately, the product doesn't support load processing for a sales return process.</span></span> <span data-ttu-id="e0d8c-113">Поэтому невозможно выпустить возврат заказа на продажу на склад.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-113">Therefore, you can't release the return sales order to the warehouse.</span></span>

<span data-ttu-id="e0d8c-114">В транзакциях заказа на продажу нельзя ссылаться на складские аналитики, расположенные под аналитикой **Местоположение** в иерархии резервирования.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-114">On sales order transactions, you can't reference inventory dimensions that are located below the **Location** dimension in the reservation hierarchy.</span></span> <span data-ttu-id="e0d8c-115">Для разрешения неполадки удалите недопустимые аналитики из строки заказа.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-115">The resolution is to remove the invalid dimensions from the order line.</span></span>

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a><span data-ttu-id="e0d8c-116">Получено следующее сообщение об ошибке: "Одна из строк уже находится в загрузке.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-116">I receive the following error message: "One of the lines is already on a load.</span></span> <span data-ttu-id="e0d8c-117">Невозможно выпустить на склад."</span><span class="sxs-lookup"><span data-stu-id="e0d8c-117">Unable to release to warehouse."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e0d8c-118">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="e0d8c-118">Issue description</span></span>

<span data-ttu-id="e0d8c-119">При создании вручную загрузок или при настройке процесса таким образом, чтобы загрузка уже была создана до ввода строки заказа на продажу, предполагается, что последующий выпуск будет выполнен вручную, и будут использоваться маршрут и рейтинг из загрузки.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-119">If you manually create loads, or if you set up the process so that loads are already created before sales order line entry occurs, the assumption is that the subsequent release will be done manually, and that the route and rating from the load will be used.</span></span>

<span data-ttu-id="e0d8c-120">В другом возможном сценарии выполняется попытка автоматического выпуска на склад, но процессу волны не удалось создать работу.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-120">In another possible scenario, you're trying to do an automatic release to the warehouse, but the wave process failed to create work.</span></span> <span data-ttu-id="e0d8c-121">Поэтому открытая отгрузка или загрузка все еще создаются.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-121">Therefore, an open shipment or load is still created.</span></span> <span data-ttu-id="e0d8c-122">Эта открытая отгрузка или загрузка затем блокирует последующие попытки автоматического выпуска заказа до тех пор, пока не будет удалена открытая отгрузка или загрузка или не будет вручную выполнена повторная обработка волны.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-122">This open shipment or load then blocks subsequent attempts to automatically release the order until you either delete the open shipment or load, or manually reprocess the wave.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e0d8c-123">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="e0d8c-123">Issue resolution</span></span>

<span data-ttu-id="e0d8c-124">Можно выполнить выпуск со страницы заказа на продажу, или автоматический выпуск может быть выполнен со страницы выпуска заказа на продажу, только если загрузка не существовала перед выпуском на склад.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-124">You can release from the sales order page, or automatic release can be done from the release sales order page, only if no load exists before the release to the warehouse.</span></span> <span data-ttu-id="e0d8c-125">Загрузка будет создана автоматически после обработки волны.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-125">The load will automatically be created after the wave is processed.</span></span>

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a><span data-ttu-id="e0d8c-126">Получено следующее сообщение об ошибке: "Исправление уведомления о поставке не может быть обработано.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-126">I receive the following error message: "The delivery note correction can't be processed.</span></span> <span data-ttu-id="e0d8c-127">Уведомление о поставке содержит только номенклатуры, которые подлежат процессам управления складом, так как они не поддерживаются исправлением уведомления о поставке."</span><span class="sxs-lookup"><span data-stu-id="e0d8c-127">The delivery note only contains items that are subject to warehouse management processes, as these are not supported by Delivery Note correction."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e0d8c-128">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="e0d8c-128">Issue description</span></span>

<span data-ttu-id="e0d8c-129">После разноски уведомления о поставке его невозможно отменить, так как кнопка **Отмена** недоступна.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-129">After you post a delivery note, you can't cancel it, because the **Cancel** button is unavailable.</span></span> <span data-ttu-id="e0d8c-130">Вы также не можете скорректировать уведомление о поставке.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-130">You also can't correct the delivery note.</span></span> <span data-ttu-id="e0d8c-131">Если вы попробуете, появится следующее сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-131">If you try, you receive this error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e0d8c-132">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="e0d8c-132">Issue resolution</span></span>

<span data-ttu-id="e0d8c-133">Для корректировки разнесенных отборочных накладных для номенклатур, включенных для расширенного управления складом (WMS), разноска должна выполняться из загрузки, а не напрямую из заказа.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-133">To correct posted packing slips for items that are enabled for advanced warehouse management (WMS), you must do the posting from the load, not directly from the order.</span></span>

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a><span data-ttu-id="e0d8c-134">Как можно создавать работу на основе исходящих загрузок вместо волн?</span><span class="sxs-lookup"><span data-stu-id="e0d8c-134">How can I create work from outbound loads instead of waves?</span></span>

### <a name="issue-description"></a><span data-ttu-id="e0d8c-135">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="e0d8c-135">Issue description</span></span>

<span data-ttu-id="e0d8c-136">Вот один из способов воспроизвести эту проблему.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-136">Here is one way to reproduce this issue.</span></span>

1. <span data-ttu-id="e0d8c-137">Создайте исходящую загрузку с помощью заказа на продажу или заказа перемещения.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-137">Create an outbound load by using a sales order or transfer order.</span></span>
2. <span data-ttu-id="e0d8c-138">Запустить загрузку в складе.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-138">Release the load to the warehouse.</span></span>
3. <span data-ttu-id="e0d8c-139">Обратите внимание, что еще не было создано ни одной работы комплектации.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-139">Notice that no picking work has yet been generated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e0d8c-140">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="e0d8c-140">Issue resolution</span></span>

<span data-ttu-id="e0d8c-141">Если работа должна быть создана сразу после выпуска загрузки, необходимо соответствующим образом настроить шаблон волны.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-141">If work must be generated immediately when the load is released, you must configure the wave template accordingly.</span></span> <span data-ttu-id="e0d8c-142">В шаблоне волны задайте для следующих параметров значение *Да*:</span><span class="sxs-lookup"><span data-stu-id="e0d8c-142">On the wave template, set the following options to *Yes*:</span></span>

- <span data-ttu-id="e0d8c-143">Создавать волны автоматически</span><span class="sxs-lookup"><span data-stu-id="e0d8c-143">Automate wave creation</span></span>
- <span data-ttu-id="e0d8c-144">Обрабатывать волну перед запуском на склад</span><span class="sxs-lookup"><span data-stu-id="e0d8c-144">Process wave at release to warehouse</span></span>
- <span data-ttu-id="e0d8c-145">Автоматический запуск волны</span><span class="sxs-lookup"><span data-stu-id="e0d8c-145">Automate wave release</span></span>

## <a name="i-cant-re-release-a-partially-shipped-load"></a><span data-ttu-id="e0d8c-146">Невозможно повторно выпустить частичную загрузку.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-146">I can't re-release a partially shipped load.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e0d8c-147">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="e0d8c-147">Issue description</span></span>

<span data-ttu-id="e0d8c-148">Невозможно выпустить частично отгруженную загрузку на склад.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-148">You can't release a partially shipped load to the warehouse.</span></span> <span data-ttu-id="e0d8c-149">При выполнении выпуска на склад появляется сообщение "Операция завершена", но ничего не происходит, и работа для оставшегося количества не создается.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-149">When you do the release to the warehouse, an "Operation complete" message appears, but nothing happens, and no work is created for the remaining quantity.</span></span> <span data-ttu-id="e0d8c-150">Эта проблема возникает при использовании функциональности транспортной загрузки и неполного резервирования.</span><span class="sxs-lookup"><span data-stu-id="e0d8c-150">This issue occurs when you use transport load functionality and there is an incomplete reservation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e0d8c-151">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="e0d8c-151">Issue resolution</span></span>

<span data-ttu-id="e0d8c-152">[Проблема статьи базы знаний 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Частично отгруженные загрузки могут быть повторно обработаны волной и повторно обработаны") исправлена в [выпуске 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span><span class="sxs-lookup"><span data-stu-id="e0d8c-152">[KB issue 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Partially shipped loads can be re-waved and re-processed") is fixed in [release 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span></span>
