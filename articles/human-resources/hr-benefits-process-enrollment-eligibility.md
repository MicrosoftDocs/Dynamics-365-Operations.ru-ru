---
title: Обработка приемлемости регистрации
description: В этой статье объясняется, как выполнить процесс допустимости регистрации.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0344c48460a7d1540481e09ba106526e119de72b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010281"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="68f5c-103">Обработка приемлемости регистрации</span><span class="sxs-lookup"><span data-stu-id="68f5c-103">Process enrollment eligibility</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="68f5c-104">В этой статье объясняется, как выполнить процесс допустимости регистрации.</span><span class="sxs-lookup"><span data-stu-id="68f5c-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="68f5c-105">В рабочей области **Управление льготами** в **Обработка** выберите **Обработка допустимости регистрации**.</span><span class="sxs-lookup"><span data-stu-id="68f5c-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="68f5c-106">В диалоговом окне **Выполнение процесса допустимости регистрации льгот** укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="68f5c-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="68f5c-107">Поле</span><span class="sxs-lookup"><span data-stu-id="68f5c-107">Field</span></span> | <span data-ttu-id="68f5c-108">Описание</span><span class="sxs-lookup"><span data-stu-id="68f5c-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="68f5c-109">Период регистрации</span><span class="sxs-lookup"><span data-stu-id="68f5c-109">Enrollment period</span></span> | <span data-ttu-id="68f5c-110">Период регистрации, для которого необходимо обработать допустимость регистрации.</span><span class="sxs-lookup"><span data-stu-id="68f5c-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="68f5c-111">Информация о компании</span><span class="sxs-lookup"><span data-stu-id="68f5c-111">Legal entity</span></span> | <span data-ttu-id="68f5c-112">Юридическое лицо, для которого необходимо обработать допустимость регистрации.</span><span class="sxs-lookup"><span data-stu-id="68f5c-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="68f5c-113">Рабочий</span><span class="sxs-lookup"><span data-stu-id="68f5c-113">Worker</span></span> | <span data-ttu-id="68f5c-114">Работник, для которого необходимо обработать допустимость регистрации.</span><span class="sxs-lookup"><span data-stu-id="68f5c-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="68f5c-115">Если оставить это поле пустым, допустимость регистрации будет обработана для всех работников.</span><span class="sxs-lookup"><span data-stu-id="68f5c-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="68f5c-116">План льготы</span><span class="sxs-lookup"><span data-stu-id="68f5c-116">Benefit plan</span></span> | <span data-ttu-id="68f5c-117">План льгот, для которого необходимо обработать допустимость регистрации.</span><span class="sxs-lookup"><span data-stu-id="68f5c-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="68f5c-118">Если необходимо выполнить процесс в фоновом режиме, выберите **Выполнить в фоновом режиме** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="68f5c-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="68f5c-119">Введите сведения для процесса.</span><span class="sxs-lookup"><span data-stu-id="68f5c-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="68f5c-120">Чтобы настроить повторяющееся задание, выберите **Повторение**, введите сведения о повторении, а затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="68f5c-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="68f5c-121">Чтобы настроить оповещение о заданиях, выберите **Оповещения**, выберите получаемые оповещения и нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="68f5c-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="68f5c-122">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="68f5c-122">Select **OK**.</span></span> <span data-ttu-id="68f5c-123">Процесс будет выполнен с заданными вами параметрами.</span><span class="sxs-lookup"><span data-stu-id="68f5c-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="68f5c-124">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="68f5c-124">Select **OK**.</span></span>
