---
title: Профили оценки
description: В этом разделе описывается, как настроить данные для профилей оценки.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ceb2b7a5edcee6e248798a6bee114c7da7ecb18a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973968"
---
# <a name="rating-profiles"></a><span data-ttu-id="0b6e0-103">Профили оценки</span><span class="sxs-lookup"><span data-stu-id="0b6e0-103">Rating profiles</span></span>

<span data-ttu-id="0b6e0-104">Профиль оценки напоминает договор логистики (но не юридический договор).</span><span class="sxs-lookup"><span data-stu-id="0b6e0-104">A rating profile resembles a logistics contract (but not a legal contract).</span></span> <span data-ttu-id="0b6e0-105">Он используется для определения транспортных тарифов для загрузок.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-105">It's used to determine transportation tariffs for loads.</span></span> 

<span data-ttu-id="0b6e0-106">Каждый профиль оценки уникален для каждого перевозчика.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-106">Each rating profile is unique to a shipping carrier.</span></span> <span data-ttu-id="0b6e0-107">В профиле вы связываете перевозчика с шаблоном ставки.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-107">In the profile, you associate the shipping carrier with a rate master.</span></span> <span data-ttu-id="0b6e0-108">Шаблон ставки определяет назначение базы ставки и базу ставки.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-108">The rate master defines the rate base assignment and the rate base.</span></span> <span data-ttu-id="0b6e0-109">База ставки определяет ставку перевозчика.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-109">The rate base determines the rate of the carrier.</span></span>

<span data-ttu-id="0b6e0-110">Профиль оценки можно настроить с помощью общей страницы, на которой представлен обзор всех существующих профилей оценки.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-110">You can set up a rating profile by using a generic page that shows an overview of all existing rating profiles.</span></span> <span data-ttu-id="0b6e0-111">Можно также настроить профиль оценки непосредственно из перевозчика.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-111">Alternatively, you can set up a rating profile directly from the shipping carrier.</span></span> <span data-ttu-id="0b6e0-112">В обоих случаях сведения, настроенные для профиля оценки, одинаковы.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-112">In both cases, the information that you set up for the rating profile is the same.</span></span>

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a><span data-ttu-id="0b6e0-113">Создание или редактирование профиля оценки на странице профили оценки</span><span class="sxs-lookup"><span data-stu-id="0b6e0-113">Create or edit a rating profile on the Rating profiles page</span></span>

<span data-ttu-id="0b6e0-114">На странице **Профили оценки** можно просмотреть все доступные профили оценки.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-114">On the **Rating profiles** page, you can review all available rating profiles.</span></span> <span data-ttu-id="0b6e0-115">Можно также редактировать существующие профили и создавать новые профили.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-115">You can also edit existing profiles and create new profiles.</span></span>

1. <span data-ttu-id="0b6e0-116">Перейдите в раздел **Управление транспортировкой \> Настройка \> Расчет ставок \> Профиль оценки**.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-116">Go to **Transportation management \> Setup \> Rating \> Rating profile**.</span></span>
1. <span data-ttu-id="0b6e0-117">В области действий выберите **Создать**, чтобы добавить новый профиль оценки в сетку, или выберите **Правка**, чтобы изменить существующий профиль.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-117">On the Action Pane, select **New** to add a new rating profile to the grid, or select **Edit** to edit an existing profile.</span></span>
1. <span data-ttu-id="0b6e0-118">В строке для нового или существующего профиля оценки задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="0b6e0-118">In the row for the new or existing rating profile, set the following fields:</span></span>

    - <span data-ttu-id="0b6e0-119">**Профиль оценки** — введите уникальный идентификатор для профиля оценки.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-119">**Rating profile** – Enter a unique identifier (ID) for the rating profile.</span></span>
    - <span data-ttu-id="0b6e0-120">**Имя** — введите описательное имя для профиля оценки.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-120">**Name** – Enter a descriptive name for the rating profile.</span></span>
    - <span data-ttu-id="0b6e0-121">**Перевозчик** — выберите перевозчика.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-121">**Shipping carrier** – Select a shipping carrier.</span></span> <span data-ttu-id="0b6e0-122">Профиль оценки, который вы настраиваете, также будет отображаться на странице **Перевозчики** для выбранного перевозчика.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-122">The rating profile that you're setting up will also be shown on the **Shipping carriers** page for the selected carrier.</span></span>
    - <span data-ttu-id="0b6e0-123">**Сайт** и **Склад** — выберите сайт и склад.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-123">**Site** and **Warehouse** – Select a site and warehouse.</span></span>
    - <span data-ttu-id="0b6e0-124">**Механизм ставок** — выберите механизм ставок для профиля оценки.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-124">**Rate engine** – Select the rate engine for the rating profile.</span></span>
    - <span data-ttu-id="0b6e0-125">**Шаблон ставки** — выберите шаблон ставок для профиля оценки.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-125">**Rate master** – Select the rate master for the rating profile.</span></span> <span data-ttu-id="0b6e0-126">Шаблона ставки можно использовать для определения типа базы ставки и базы ставки.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-126">You can use the rate master to define a rate base type and a rate base.</span></span> <span data-ttu-id="0b6e0-127">Дополнительные сведения см. в разделе [Настройка шаблонов ставок](set-up-rate-masters.md).</span><span class="sxs-lookup"><span data-stu-id="0b6e0-127">For more information, see [Set up rate masters](set-up-rate-masters.md).</span></span>
    - <span data-ttu-id="0b6e0-128">**Механизм расчета транзитного времени** — выберите механизм расчета транзитного времени для профиля оценки.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-128">**Transit time engine** – Select the transit time engine for the rating profile.</span></span>
    - <span data-ttu-id="0b6e0-129">**Индекс топлива перевозчика** — выберите индекс топлива перевозчика для профиля оценки.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-129">**Carrier fuel index** – Select the carrier fuel index for the rating profile.</span></span>
    - <span data-ttu-id="0b6e0-130">**Фактические дата и время начала** и **Фактические дата и время окончания** — определите период, в течение которого профиль оценки должен быть активным.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-130">**Effect start date and time** and **Effective end date and time** – Define the period when the rating profile should be active.</span></span>

1. <span data-ttu-id="0b6e0-131">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-131">On the Action Pane, select **Save**.</span></span>

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a><span data-ttu-id="0b6e0-132">Создание профиля оценки непосредственно на странице перевозчиков</span><span class="sxs-lookup"><span data-stu-id="0b6e0-132">Create a rating profile directly on the Shipping carriers page</span></span>

1. <span data-ttu-id="0b6e0-133">Перейдите в раздел **Управление транспортировкой \> Настройка \> Перевозчики \> Перевозчики, осуществляющий доставку**.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-133">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="0b6e0-134">Выберите перевозчика в списке.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-134">Select a shipping carrier in the list.</span></span>
1. <span data-ttu-id="0b6e0-135">На экспресс-вкладке **Профили оценки** выберите **Создать**, чтобы создать профиль оценки.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-135">On the **Rating profiles** FastTab, select **New** to create a rating profile.</span></span>
1. <span data-ttu-id="0b6e0-136">Задайте поля для нового профиля оценки.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-136">Set the fields for the new rating profile.</span></span> <span data-ttu-id="0b6e0-137">Эти поля соответствуют полям на странице **Профили оценки**, как это описано в предыдущем разделе данной темы.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-137">These fields correspond to the fields on the **Rating profiles** page, as described in previous section of this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="0b6e0-138">Профили, созданные на странице **Перевозчики**, также отображаются на странице **Профили оценки**.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-138">Profiles that are created on the **Shipping carriers** page are also shown on the **Rating profiles** page.</span></span>
