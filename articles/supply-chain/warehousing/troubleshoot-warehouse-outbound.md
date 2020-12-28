---
title: Устранение неполадок исходящих операций склада
description: В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с исходящими операциями склада в Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 56bd91d8a6fe895317021d806e180df3a2db302b
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645461"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a><span data-ttu-id="9678e-103">Устранение неполадок исходящих операций склада</span><span class="sxs-lookup"><span data-stu-id="9678e-103">Troubleshoot outbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9678e-104">В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с исходящими операциями склада в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9678e-104">This topic describes how to fix common issues that you might encounter while you work with outbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a><span data-ttu-id="9678e-105">Получено следующее сообщение об ошибке: "Заказ на продажу не может быть выпущен."</span><span class="sxs-lookup"><span data-stu-id="9678e-105">I receive the following error message: "Sales order could not be released."</span></span>

### <a name="issue-description"></a><span data-ttu-id="9678e-106">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="9678e-106">Issue description</span></span>

<span data-ttu-id="9678e-107">Эта проблема может возникнуть по нескольким причинам.</span><span class="sxs-lookup"><span data-stu-id="9678e-107">This issue can occur for several reasons.</span></span> <span data-ttu-id="9678e-108">Например, заказ находится на блокировке в системе управления кредитами, и отгрузки невозможно создать до тех пор, пока не будет введен действительный почтовый адрес для всех строк продаж, связанных с заказом на продажу.</span><span class="sxs-lookup"><span data-stu-id="9678e-108">For example, the order is on credit management hold, and no shipments can be created until a valid postal address is entered for all sales lines that are associated with a sales order.</span></span> <span data-ttu-id="9678e-109">Также возможна блокировка заказа, которая должна быть устранена, прежде чем заказ может быть выпущен на склад.</span><span class="sxs-lookup"><span data-stu-id="9678e-109">Alternatively, there is an order hold that must be addressed before the order can be released to the warehouse.</span></span> <span data-ttu-id="9678e-110">Эта блокировка может быть связана с определенным заказом, или она может находиться на счете клиента.</span><span class="sxs-lookup"><span data-stu-id="9678e-110">This hold might be order-specific, or it might be on the customer account.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9678e-111">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="9678e-111">Issue resolution</span></span>

<span data-ttu-id="9678e-112">Добавьте или обновите адрес в заказе на продажу и строках заказа, а затем выпустите заказ на склад.</span><span class="sxs-lookup"><span data-stu-id="9678e-112">Add or update the address on the sales order and order lines, and then release the order to the warehouse.</span></span> <span data-ttu-id="9678e-113">Заказы могут быть выпущены на склад только в том случае, если они имеют допустимый адрес поставки (согласно настройке формата адреса в модуле **Администрирование организации**).</span><span class="sxs-lookup"><span data-stu-id="9678e-113">Orders can be released to the warehouse only if they have a valid delivery address (per the address format setup in the **Organization administration** module).</span></span>

<span data-ttu-id="9678e-114">Изучите блокировку заказа и устраните проблемы.</span><span class="sxs-lookup"><span data-stu-id="9678e-114">Investigate the order hold, and address the issues.</span></span> <span data-ttu-id="9678e-115">Затем удалите блокировку из заказа или клиента и выпустите заказ на склад.</span><span class="sxs-lookup"><span data-stu-id="9678e-115">Then remove the hold from the order or customer, and release the order to the warehouse.</span></span>

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a><span data-ttu-id="9678e-116">Получено следующее сообщение: "Была подтверждена отгрузка для загрузки 1%."</span><span class="sxs-lookup"><span data-stu-id="9678e-116">I receive the following message: "The shipment for load 1% has been confirmed."</span></span> <span data-ttu-id="9678e-117">Однако никакие строки не разносятся.</span><span class="sxs-lookup"><span data-stu-id="9678e-117">However, no lines are posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9678e-118">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="9678e-118">Issue description</span></span>

<span data-ttu-id="9678e-119">Отгрузка по загрузке подтверждена, но дальнейшая разноска не выполнена.</span><span class="sxs-lookup"><span data-stu-id="9678e-119">A shipment on a load was confirmed, but no further posting occurred.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9678e-120">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="9678e-120">Issue resolution</span></span>

<span data-ttu-id="9678e-121">Подтверждение отгрузки не влияет на разноску.</span><span class="sxs-lookup"><span data-stu-id="9678e-121">Shipment confirmation doesn't affect posting.</span></span> <span data-ttu-id="9678e-122">Оно просто обновляет отгрузку и статус загрузки.</span><span class="sxs-lookup"><span data-stu-id="9678e-122">It just updates the shipment and load status.</span></span> <span data-ttu-id="9678e-123">Разноска должна выполняться в отдельном процессе.</span><span class="sxs-lookup"><span data-stu-id="9678e-123">Posting must occur in a separate process.</span></span>

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a><span data-ttu-id="9678e-124">Получено следующее сообщение об ошибке: "Невозможна обработка прямой поставки для склада %1, так как для него включено управление складом.</span><span class="sxs-lookup"><span data-stu-id="9678e-124">I receive the following error message: "Direct delivery is not able to process for warehouse 1% as it has warehouse management enabled.</span></span> <span data-ttu-id="9678e-125">Задайте другой склад, для которого управление складом не включено."</span><span class="sxs-lookup"><span data-stu-id="9678e-125">Please specify another warehouse that is not enabled for warehouse management."</span></span>

### <a name="issue-description"></a><span data-ttu-id="9678e-126">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="9678e-126">Issue description</span></span>

<span data-ttu-id="9678e-127">Номенклатура добавляется в строку продаж для прямой поставки со склада, который включен для управления складом (WMS).</span><span class="sxs-lookup"><span data-stu-id="9678e-127">An item is added to a sales line for direct delivery from a warehouse that is enabled for warehouse management (WMS).</span></span> <span data-ttu-id="9678e-128">Это сообщение об ошибке выводится при обновлении строки продаж.</span><span class="sxs-lookup"><span data-stu-id="9678e-128">You receive this error message when the sales line is updated.</span></span> 

### <a name="issue-resolution"></a><span data-ttu-id="9678e-129">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="9678e-129">Issue resolution</span></span>

<span data-ttu-id="9678e-130">Корпорация Майкрософт проверила эту проблему и определила, что она является ограничением функции.</span><span class="sxs-lookup"><span data-stu-id="9678e-130">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="9678e-131">В настоящее время WMS не поддерживает прямую поставку.</span><span class="sxs-lookup"><span data-stu-id="9678e-131">Currently, WMS doesn't support direct delivery.</span></span> <span data-ttu-id="9678e-132">Таким образом, для использования прямой поставки необходимо выбрать номенклатуру и склад, для которых не используется WMS.</span><span class="sxs-lookup"><span data-stu-id="9678e-132">Therefore, to use direct delivery, you must select a non-WMS item and warehouse.</span></span>
