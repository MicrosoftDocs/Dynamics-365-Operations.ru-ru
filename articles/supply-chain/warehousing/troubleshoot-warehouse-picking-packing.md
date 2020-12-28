---
title: Устранение неполадок комплектации и упаковки
description: В этой теме описывается устранение распространенных проблем, которые могут встретиться при комплектации и упаковке в Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 74854fa95837dd8a133860e2a017be4c92ff84a3
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645485"
---
# <a name="troubleshoot-picking-and-packing"></a><span data-ttu-id="49e85-103">Устранение неполадок комплектации и упаковки</span><span class="sxs-lookup"><span data-stu-id="49e85-103">Troubleshoot picking and packing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49e85-104">В этой теме описывается устранение распространенных проблем, которые могут встретиться при комплектации и упаковке в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="49e85-104">This topic describes how to fix common issues that you might encounter while you pick and pack in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a><span data-ttu-id="49e85-105">Получено следующее сообщение об ошибке: "Местоположение аналитики не может быть оставлено пустым, если установлен серийный номер аналитики."</span><span class="sxs-lookup"><span data-stu-id="49e85-105">I receive the following error message: "Dimension location can't be left blank if dimension serial number is set."</span></span>

### <a name="issue-description"></a><span data-ttu-id="49e85-106">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="49e85-106">Issue description</span></span>

<span data-ttu-id="49e85-107">Это сообщение об ошибке появляется, если заказ на перемещение для серийной номенклатуры создается с использованием склада, который активирован для расширенного управления складом (WMS), а затем, после завершения работы, вы пытаетесь подтвердить отгрузку.</span><span class="sxs-lookup"><span data-stu-id="49e85-107">You receive this error message if you create a transfer order for a serial item by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="49e85-108">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="49e85-108">Issue resolution</span></span>

<span data-ttu-id="49e85-109">Поле **Местоположение прихода по умолчанию** пусто для транзитного склада у склада "из".</span><span class="sxs-lookup"><span data-stu-id="49e85-109">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="49e85-110">Чтобы решить эту проблему, необходимо указать местоположение прихода по умолчанию на транзитном складе.</span><span class="sxs-lookup"><span data-stu-id="49e85-110">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="49e85-111">Убедитесь, что это местоположение управляется грузоместом.</span><span class="sxs-lookup"><span data-stu-id="49e85-111">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a><span data-ttu-id="49e85-112">Получено следующее сообщение об ошибке: "Недопустимое грузоместо."</span><span class="sxs-lookup"><span data-stu-id="49e85-112">I receive the following error message: "Invalid license plate."</span></span>

### <a name="issue-description"></a><span data-ttu-id="49e85-113">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="49e85-113">Issue description</span></span>

<span data-ttu-id="49e85-114">Вы получаете это сообщение об ошибке в приложении склада при сканировании кода грузоместа.</span><span class="sxs-lookup"><span data-stu-id="49e85-114">You receive this error message in the warehouse app when you scan a license plate ID.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="49e85-115">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="49e85-115">Issue resolution</span></span>

<span data-ttu-id="49e85-116">Убедитесь, что код грузоместа существует в таблице грузомест, и что номенклатуры и количества в грузоместе доступны (иными словами, они не заблокированы).</span><span class="sxs-lookup"><span data-stu-id="49e85-116">Make sure that the license plate ID exists in the license plates table, and that the items and quantities on the license plate are available (in other words, they aren't blocked).</span></span>

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a><span data-ttu-id="49e85-117">Получено следующее сообщение об ошибке: "Поле 'Вес загрузки'(=-%1) может содержать только положительные числа.</span><span class="sxs-lookup"><span data-stu-id="49e85-117">I receive the following error message: "Field 'Load weight'(=-%1) can only contain positive numbers.</span></span> <span data-ttu-id="49e85-118">Обновление отменено."</span><span class="sxs-lookup"><span data-stu-id="49e85-118">Update has been canceled."</span></span>

### <a name="issue-description"></a><span data-ttu-id="49e85-119">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="49e85-119">Issue description</span></span>

<span data-ttu-id="49e85-120">Это сообщение об ошибке выводится в том случае, если имеется открытая работа при обработке работы из местоположения упаковки в промежуточные местоположения или из промежуточных местоположений в местоположения дока.</span><span class="sxs-lookup"><span data-stu-id="49e85-120">You receive this error message if there is open work when you process work from packing locations to staging locations, or from staging locations to dock locations.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="49e85-121">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="49e85-121">Issue resolution</span></span>

<span data-ttu-id="49e85-122">Чтобы устранить эту проблему, перейдите на страницу **Администрирование системы \> Периодические задачи \> База данных \> Проверка целостности** и запустите процесс **Проверка целостности веса загрузки склада**.</span><span class="sxs-lookup"><span data-stu-id="49e85-122">To fix this issue, go to **System administration \> Periodic tasks \> Database \> Consistency check**, and run the process for **Warehouse load weight consistency check**.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="49e85-123">Я получил следующее сообщение об ошибке: "Количество недействительно для единицы %1."</span><span class="sxs-lookup"><span data-stu-id="49e85-123">I receive the following error message: "The quantity is not valid for unit %1."</span></span>

### <a name="issue-description"></a><span data-ttu-id="49e85-124">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="49e85-124">Issue description</span></span>

<span data-ttu-id="49e85-125">Это сообщение об ошибке появляется при попытке выполнить *раздельную комплектацию* по нескольким партиям.</span><span class="sxs-lookup"><span data-stu-id="49e85-125">You receive this error message when you try to perform a *split pick* across multiple batches.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="49e85-126">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="49e85-126">Issue resolution</span></span>

<span data-ttu-id="49e85-127">Работник склада должен использовать процесс *недостаточной комплектации* в приложении склада.</span><span class="sxs-lookup"><span data-stu-id="49e85-127">The warehouse worker must use the *Short picking* process in the warehouse app.</span></span> <span data-ttu-id="49e85-128">При попытке комплектации нескольких партий из одного местоположения можно также использовать параметр **Полный** в приложении склада.</span><span class="sxs-lookup"><span data-stu-id="49e85-128">If you're trying to pick multiple batches from the same location, you can also use the **Full** option in the warehouse app.</span></span>

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a><span data-ttu-id="49e85-129">Не удается переместить запасы в местоположение, управляемое грузоместом.</span><span class="sxs-lookup"><span data-stu-id="49e85-129">I can't move inventory to a location that is license plate–controlled.</span></span>

### <a name="issue-description"></a><span data-ttu-id="49e85-130">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="49e85-130">Issue description</span></span>

<span data-ttu-id="49e85-131">Невозможно уменьшить скомплектованное количество для загрузки.</span><span class="sxs-lookup"><span data-stu-id="49e85-131">You can't reduce picked quantities on a load.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="49e85-132">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="49e85-132">Issue resolution</span></span>

<span data-ttu-id="49e85-133">В более ранних версиях невозможно уменьшить скомплектованное количество для загрузки.</span><span class="sxs-lookup"><span data-stu-id="49e85-133">In earlier versions, you can't reduce picked quantities on a load.</span></span> <span data-ttu-id="49e85-134">Однако теперь можно разукомплектовывать в местоположение, управляемое грузоместом.</span><span class="sxs-lookup"><span data-stu-id="49e85-134">However, you can now unpick to a license plate–controlled location.</span></span> <span data-ttu-id="49e85-135">Необходимо указать как значение **Местоположение**, так и значение **Грузоместо** для строки загрузки на странице **Уменьшить скомплектованное количество**.</span><span class="sxs-lookup"><span data-stu-id="49e85-135">You must specify both a **Location** value and a **License plate** value for the load line on the **Reduce picked quantity** page.</span></span>

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a><span data-ttu-id="49e85-136">Можно ли печатать уведомление о поставке или упаковочное содержимое по складам?</span><span class="sxs-lookup"><span data-stu-id="49e85-136">Can I print a delivery note or packing content by warehouse?</span></span>

### <a name="issue-description"></a><span data-ttu-id="49e85-137">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="49e85-137">Issue description</span></span>

<span data-ttu-id="49e85-138">Необходимо напечатать уведомление о поставке или упаковочное содержимое по складам или сайтам на странице **Обновление строк шаблона аудита работы**.</span><span class="sxs-lookup"><span data-stu-id="49e85-138">You want to print a delivery note or packing content by warehouse or site on the **Work audit template line update** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="49e85-139">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="49e85-139">Issue resolution</span></span>

<span data-ttu-id="49e85-140">При печати документа с помощью параметров управления печатью ограничьте область (сайт или склад) посредством управления печатью, а не выбором команды **Изменить параметры печати** на странице **Обновление строк шаблона аудита работ**.</span><span class="sxs-lookup"><span data-stu-id="49e85-140">When you print a document by using Print management settings, limit the scope (site/warehouse) through Print management instead of by selecting **Edit print settings** on the **Work audit template line update** page.</span></span>

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a><span data-ttu-id="49e85-141">Невозможно отменить отборочную накладную после ее разноски из заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="49e85-141">I can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="49e85-142">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="49e85-142">Issue description</span></span>

<span data-ttu-id="49e85-143">Если процессы комплектации и отгрузки включены для WMS, невозможно отменить отборочную накладную после ее разноски из заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="49e85-143">When picking and shipping processes are enabled for WMS, you can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="49e85-144">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="49e85-144">Issue resolution</span></span>

<span data-ttu-id="49e85-145">Для корректировки разнесенных отборочных накладных для номенклатур, включенных для WMS, разноска должна выполняться из загрузки, а не из заказа.</span><span class="sxs-lookup"><span data-stu-id="49e85-145">To correct posted packing slips for items that are enabled for WMS, the posting must occur from the load, not from the order.</span></span> <span data-ttu-id="49e85-146">Корпорация Майкрософт проверила эту проблему и определила, что она является ограничением функции.</span><span class="sxs-lookup"><span data-stu-id="49e85-146">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="49e85-147">В общем случае заказ на продажу, который был скомплектованы и отгружен в процессах управления складом, может быть обновлен отборочной накладной из загрузки или отгрузки и самого документа заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="49e85-147">In general, a sales order that has been picked and shipped through warehouse management processes can be packing slip–updated from the load or shipment and the sales order document itself.</span></span> <span data-ttu-id="49e85-148">Однако, если обновить заказ на продажу по отборочной накладной из документа заказа на продажу, реверсирование отборочной накладной все равно невозможно выполнить из загрузки или заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="49e85-148">However, if you packing slip–update the sales order from the sales order document, packing slip reversal still can't be done from the load or sales order.</span></span> <span data-ttu-id="49e85-149">Поэтому рекомендуется использовать разноску отборочной накладной из загрузки.</span><span class="sxs-lookup"><span data-stu-id="49e85-149">Therefore, we recommend that you use the packing slip posting from the load.</span></span> <span data-ttu-id="49e85-150">В этом случае сторнирование, которое должно быть выполнено из загрузки, будет включено.</span><span class="sxs-lookup"><span data-stu-id="49e85-150">In this case, the reversal that must be done from the load will be enabled.</span></span>

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a><span data-ttu-id="49e85-151">Я получают следующее сообщение об ошибке: "Для кластера не найдено достаточно работы".</span><span class="sxs-lookup"><span data-stu-id="49e85-151">I receive the following error message: "Not enough work can be found for cluster."</span></span>

### <a name="issue-description"></a><span data-ttu-id="49e85-152">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="49e85-152">Issue description</span></span>

<span data-ttu-id="49e85-153">При использовании процесса *Комплектация кластера, управляемая системой* при настройке профиля кластера, в котором, например, можно скомплектовать 10 позиций, процесс работает как запланировано, если для комплектации на 10 позиций достаточно работы.</span><span class="sxs-lookup"><span data-stu-id="49e85-153">When you use the *System directed cluster picking* process, if you configure a cluster profile where, for example, 10 positions can be picked, the process works as planned when there is enough work to pick to 10 positions.</span></span> <span data-ttu-id="49e85-154">Однако если есть только восемь позиций для комплектации, вы получаете это сообщение об ошибке, так как недостаточно работы для одного кластера.</span><span class="sxs-lookup"><span data-stu-id="49e85-154">However, if there are only eight positions to pick, you receive this error message, because there isn't enough work for one cluster.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="49e85-155">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="49e85-155">Issue resolution</span></span>

<span data-ttu-id="49e85-156">Чтобы устранить эту проблему, отредактируйте профиль кластера и установите для параметра **Активировать позиции** значение *Нет*.</span><span class="sxs-lookup"><span data-stu-id="49e85-156">To fix this issue, edit the cluster profile, and set the **Activate positions** option to *No*.</span></span>
