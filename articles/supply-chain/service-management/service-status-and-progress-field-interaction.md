---
title: "Взаимодействие статуса обслуживания и поля хода выполнения работ"
description: "В форме \"Заказы на сервисное обслуживание\" поле \"Ход выполнения\" под заголовком заказа на обслуживание отражает статус всего заказа на обслуживание, и указывает статус отдельных строк заказа на обслуживание."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 51ef39266e8de00488954918568d00a297a9b50a
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---


# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="61bb8-103">Взаимодействие статуса обслуживания и поля хода выполнения работ</span><span class="sxs-lookup"><span data-stu-id="61bb8-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="61bb8-104">В форме **Заказы на сервисное обслуживание** поле **Ход выполнения** под заголовком заказа на сервисное обслуживание отражает статус всего заказа на обслуживание, и указывает **Статус** отдельных строк заказа на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="61bb8-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="61bb8-105">Прогресс</span><span class="sxs-lookup"><span data-stu-id="61bb8-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="61bb8-106">Статус по строке 1</span><span class="sxs-lookup"><span data-stu-id="61bb8-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="61bb8-107">Статус по строке 2</span><span class="sxs-lookup"><span data-stu-id="61bb8-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="61bb8-108">Статус по строке 3</span><span class="sxs-lookup"><span data-stu-id="61bb8-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61bb8-109"><strong>В работе</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="61bb8-110"><strong>Создано</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="61bb8-111"><strong>Создано</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="61bb8-112"><strong>Создано</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61bb8-113"><strong>В работе</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="61bb8-114"><strong>Отменено</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="61bb8-115"><strong>Создано</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="61bb8-116"><strong>Создано</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61bb8-117"><strong>В работе</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="61bb8-118"><strong>Создано</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="61bb8-119"><strong>Отменено</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="61bb8-120"><strong>Разнесено</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61bb8-121"><strong>Отменено</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="61bb8-122"><strong>Отменено</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="61bb8-123"><strong>Отменено</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="61bb8-124"><strong>Отменено</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61bb8-125"><strong>Разнесено</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="61bb8-126"><strong>Разнесено</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="61bb8-127"><strong>Разнесено</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="61bb8-128"><strong>Разнесено</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61bb8-129"><strong>Разнесено</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="61bb8-130"><strong>Разнесено</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="61bb8-131"><strong>Отменено</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="61bb8-132"><strong>Отменено</strong></span><span class="sxs-lookup"><span data-stu-id="61bb8-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="61bb8-133">Ход выполнения заказа на сервисное обслуживание обрабатывается, если все строки имеют статус **Создано**, он также обрабатывается, если некоторые строки имеют статус **Отменено** или **Разнесено**.</span><span class="sxs-lookup"><span data-stu-id="61bb8-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="61bb8-134">Если все строки заказа на сервисное обслуживание помечены как **Разнесено**, ход выполнения заказа на обслуживание имеет статус **Разнесено**.</span><span class="sxs-lookup"><span data-stu-id="61bb8-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="61bb8-135">Если некоторые строки имеют статус **Разнесено**, а некоторые **Отменено**, ход выполнения по-прежнему будет иметь статус **Разнесено**.</span><span class="sxs-lookup"><span data-stu-id="61bb8-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  



