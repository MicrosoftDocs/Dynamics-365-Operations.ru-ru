---
title: Настройка самообслуживания сотрудников
description: В Microsoft Dynamics 365 Human Resources можно настроить плитки для переходов верхнего уровня в модуле дистанционного обслуживания сотрудников.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3e763a09e0a0f13eb7222a6ffbcb31b6230b83f4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797944"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="36daa-103">Настройка самообслуживания сотрудников</span><span class="sxs-lookup"><span data-stu-id="36daa-103">Configure employee self service</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="36daa-104">В Microsoft Dynamics 365 Human Resources можно настроить плитки для переходов верхнего уровня в модуле дистанционного обслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="36daa-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="36daa-105">Плитки плана льгот направляют пользователей в планы льгот, для которых они имеют право.</span><span class="sxs-lookup"><span data-stu-id="36daa-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="36daa-106">Настройка плитки планов льгот</span><span class="sxs-lookup"><span data-stu-id="36daa-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="36daa-107">В рабочей области **Управление льготами** в **Настройка** выберите **Параметры дистанционного обслуживания сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="36daa-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="36daa-108">Выберите вкладку **Настройка плитки планов льгот**, а затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="36daa-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="36daa-109">Укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="36daa-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="36daa-110">Поле</span><span class="sxs-lookup"><span data-stu-id="36daa-110">Field</span></span> | <span data-ttu-id="36daa-111">Описание</span><span class="sxs-lookup"><span data-stu-id="36daa-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="36daa-112">**Идентификатор плитки**</span><span class="sxs-lookup"><span data-stu-id="36daa-112">**Tile ID**</span></span> | <span data-ttu-id="36daa-113">Уникальный идентификатор для плитки.</span><span class="sxs-lookup"><span data-stu-id="36daa-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="36daa-114">**Текст метки плитки**</span><span class="sxs-lookup"><span data-stu-id="36daa-114">**Tile label text**</span></span> | <span data-ttu-id="36daa-115">Текст, который будет отображаться для плитки при дистанционном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="36daa-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="36daa-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="36daa-116">**Description**</span></span> | <span data-ttu-id="36daa-117">Описание плитки.</span><span class="sxs-lookup"><span data-stu-id="36daa-117">A description of the tile.</span></span> |
   | <span data-ttu-id="36daa-118">**Веб-адрес**</span><span class="sxs-lookup"><span data-stu-id="36daa-118">**Internet address**</span></span> | <span data-ttu-id="36daa-119">Введите URL-адрес страницы дистанционного обслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="36daa-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="36daa-120">**Размер плитки**</span><span class="sxs-lookup"><span data-stu-id="36daa-120">**Tile size**</span></span> | <span data-ttu-id="36daa-121">Размер плитки: маленький, средний или большой.</span><span class="sxs-lookup"><span data-stu-id="36daa-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="36daa-122">**Цель**</span><span class="sxs-lookup"><span data-stu-id="36daa-122">**Target**</span></span> | <span data-ttu-id="36daa-123">Указывает, следует ли открывать страницу в новом окне или в текущем окне.</span><span class="sxs-lookup"><span data-stu-id="36daa-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="36daa-124">**Фоновое изображение плитки**</span><span class="sxs-lookup"><span data-stu-id="36daa-124">**Tile background image**</span></span> | <span data-ttu-id="36daa-125">URL-адрес изображения, используемого для плитки (необязательно).</span><span class="sxs-lookup"><span data-stu-id="36daa-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="36daa-126">**Запустить**</span><span class="sxs-lookup"><span data-stu-id="36daa-126">**Start**</span></span> | <span data-ttu-id="36daa-127">Дата и время начала, когда плитка должна быть доступна.</span><span class="sxs-lookup"><span data-stu-id="36daa-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="36daa-128">**Окончание**</span><span class="sxs-lookup"><span data-stu-id="36daa-128">**End**</span></span> | <span data-ttu-id="36daa-129">Дата и время окончания доступности плитки.</span><span class="sxs-lookup"><span data-stu-id="36daa-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="36daa-130">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="36daa-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="36daa-131">Настройка плитки плана гибкого кредита</span><span class="sxs-lookup"><span data-stu-id="36daa-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="36daa-132">В рабочей области **Управление льготами** в **Настройка** выберите **Параметры дистанционного обслуживания сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="36daa-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="36daa-133">Выберите вкладку **Настройка плитки плана гибкого кредита**, а затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="36daa-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="36daa-134">Укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="36daa-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="36daa-135">Поле</span><span class="sxs-lookup"><span data-stu-id="36daa-135">Field</span></span> | <span data-ttu-id="36daa-136">Описание</span><span class="sxs-lookup"><span data-stu-id="36daa-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="36daa-137">**Идентификатор плитки**</span><span class="sxs-lookup"><span data-stu-id="36daa-137">**Tile ID**</span></span> | <span data-ttu-id="36daa-138">Уникальный идентификатор для плитки.</span><span class="sxs-lookup"><span data-stu-id="36daa-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="36daa-139">**Текст метки плитки**</span><span class="sxs-lookup"><span data-stu-id="36daa-139">**Tile label text**</span></span> | <span data-ttu-id="36daa-140">Текст, который будет отображаться для плитки при дистанционном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="36daa-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="36daa-141">**Описание**</span><span class="sxs-lookup"><span data-stu-id="36daa-141">**Description**</span></span> | <span data-ttu-id="36daa-142">Описание плитки.</span><span class="sxs-lookup"><span data-stu-id="36daa-142">A description of the tile.</span></span> |
   | <span data-ttu-id="36daa-143">**Веб-адрес**</span><span class="sxs-lookup"><span data-stu-id="36daa-143">**Internet address**</span></span> | <span data-ttu-id="36daa-144">Введите URL-адрес страницы дистанционного обслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="36daa-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="36daa-145">**Размер плитки**</span><span class="sxs-lookup"><span data-stu-id="36daa-145">**Tile size**</span></span> | <span data-ttu-id="36daa-146">Размер плитки: маленький, средний или большой.</span><span class="sxs-lookup"><span data-stu-id="36daa-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="36daa-147">**Цель**</span><span class="sxs-lookup"><span data-stu-id="36daa-147">**Target**</span></span> | <span data-ttu-id="36daa-148">Указывает, следует ли открывать страницу в новом окне или в текущем окне.</span><span class="sxs-lookup"><span data-stu-id="36daa-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="36daa-149">**Фоновое изображение плитки**</span><span class="sxs-lookup"><span data-stu-id="36daa-149">**Tile background image**</span></span> | <span data-ttu-id="36daa-150">URL-адрес изображения, используемого для плитки (необязательно).</span><span class="sxs-lookup"><span data-stu-id="36daa-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="36daa-151">**Запустить**</span><span class="sxs-lookup"><span data-stu-id="36daa-151">**Start**</span></span> | <span data-ttu-id="36daa-152">Дата и время начала, когда плитка должна быть доступна.</span><span class="sxs-lookup"><span data-stu-id="36daa-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="36daa-153">**Окончание**</span><span class="sxs-lookup"><span data-stu-id="36daa-153">**End**</span></span> | <span data-ttu-id="36daa-154">Дата и время окончания доступности плитки.</span><span class="sxs-lookup"><span data-stu-id="36daa-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="36daa-155">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="36daa-155">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]