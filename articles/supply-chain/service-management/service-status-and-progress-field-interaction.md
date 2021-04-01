---
title: Взаимодействие статуса обслуживания и поля хода выполнения работ
description: В форме "Заказы на сервисное обслуживание" поле "Ход выполнения" под заголовком заказа на обслуживание отражает статус всего заказа на обслуживание, и указывает статус отдельных строк заказа на обслуживание.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c66871d07bdfd949e29a704f53b3e5698d996c2d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254223"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="c6771-103">Взаимодействие статуса обслуживания и поля хода выполнения работ</span><span class="sxs-lookup"><span data-stu-id="c6771-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c6771-104">В форме **Заказы на сервисное обслуживание** поле **Ход выполнения** под заголовком заказа на сервисное обслуживание отражает статус всего заказа на обслуживание, и указывает **Статус** отдельных строк заказа на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="c6771-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6771-105">Прогресс</span><span class="sxs-lookup"><span data-stu-id="c6771-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="c6771-106">Статус по строке 1</span><span class="sxs-lookup"><span data-stu-id="c6771-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="c6771-107">Статус по строке 2</span><span class="sxs-lookup"><span data-stu-id="c6771-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="c6771-108">Статус по строке 3</span><span class="sxs-lookup"><span data-stu-id="c6771-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6771-109"><strong>В работе</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="c6771-110"><strong>Создано</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="c6771-111"><strong>Создано</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="c6771-112"><strong>Создано</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6771-113"><strong>В работе</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="c6771-114"><strong>Отменено</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="c6771-115"><strong>Создано</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="c6771-116"><strong>Создано</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6771-117"><strong>В работе</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="c6771-118"><strong>Создано</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="c6771-119"><strong>Отменено</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="c6771-120"><strong>Разнесено</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6771-121"><strong>Отменено</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="c6771-122"><strong>Отменено</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="c6771-123"><strong>Отменено</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="c6771-124"><strong>Отменено</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6771-125"><strong>Разнесено</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="c6771-126"><strong>Разнесено</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="c6771-127"><strong>Разнесено</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="c6771-128"><strong>Разнесено</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6771-129"><strong>Разнесено</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="c6771-130"><strong>Разнесено</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="c6771-131"><strong>Отменено</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="c6771-132"><strong>Отменено</strong></span><span class="sxs-lookup"><span data-stu-id="c6771-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c6771-133">Ход выполнения заказа на сервисное обслуживание обрабатывается, если все строки имеют статус **Создано**, он также обрабатывается, если некоторые строки имеют статус **Отменено** или **Разнесено**.</span><span class="sxs-lookup"><span data-stu-id="c6771-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="c6771-134">Если все строки заказа на сервисное обслуживание помечены как **Разнесено**, ход выполнения заказа на обслуживание имеет статус **Разнесено**.</span><span class="sxs-lookup"><span data-stu-id="c6771-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="c6771-135">Если некоторые строки имеют статус **Разнесено**, а некоторые **Отменено**, ход выполнения по-прежнему будет иметь статус **Разнесено**.</span><span class="sxs-lookup"><span data-stu-id="c6771-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]