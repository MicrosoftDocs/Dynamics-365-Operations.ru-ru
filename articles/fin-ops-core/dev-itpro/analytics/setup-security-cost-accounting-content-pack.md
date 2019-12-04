---
title: Настройка безопасности для содержимого Power BI анализа учета затрат
description: В этом разделе объясняется, как можно распространить защиту на уровне доступа в модуле "Учет затрат" на защиту на уровне строк в Microsoft Power BI. Данная функция позволяет гарантировать, что пользователи видят только те данные Power BI, к которым им предоставлен доступ.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d371d35352348b1cfe1dd2a5ba25e1b2b20d7d71
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769909"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="33f4d-104">Настройка безопасности для содержимого Power BI анализа учета затрат</span><span class="sxs-lookup"><span data-stu-id="33f4d-104">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33f4d-105">В этом разделе объясняется, как можно распространить защиту на уровне доступа в модуле "Учет затрат" на защиту на уровне строк в Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="33f4d-105">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="33f4d-106">Данная функция позволяет гарантировать, что пользователи видят только те данные Power BI, к которым им предоставлен доступ.</span><span class="sxs-lookup"><span data-stu-id="33f4d-106">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

## <a name="overview"></a><span data-ttu-id="33f4d-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="33f4d-107">Overview</span></span>

<span data-ttu-id="33f4d-108">Содержимое Microsoft Power BI **Анализ учета затрат** использует безопасность на уровне строк Power BI для ограничения доступа пользователя.</span><span class="sxs-lookup"><span data-stu-id="33f4d-108">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="33f4d-109">Безопасность основана на организационной иерархией уровня доступа, которая настроена в параметрах учета затрат.</span><span class="sxs-lookup"><span data-stu-id="33f4d-109">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="33f4d-110">Дополнительные сведения о содержимом Power BI **Анализ учета затрат** см. в разделе [Содержимое Power BI "Анализ учета затрат"](cost-accounting-analysis-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="33f4d-110">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="33f4d-111">Настройка</span><span class="sxs-lookup"><span data-stu-id="33f4d-111">Setup</span></span>
<span data-ttu-id="33f4d-112">Чтобы распространить безопасность уровня доступа на Power BI владелец содержимого Power BI должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="33f4d-112">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="33f4d-113">Пользователь, который публикует содержимое Power BI **Анализ учета затрат**, автоматически становится владельцем.</span><span class="sxs-lookup"><span data-stu-id="33f4d-113">The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="33f4d-114">Только владелец может настраивать безопасность в Power BI.</span><span class="sxs-lookup"><span data-stu-id="33f4d-114">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="33f4d-115">Кроме того, пока владелец добавляет других пользователей на PowerBI.com, никто, кроме владельца, не может просматривать данные в содержимом Power BI **Анализ учета затрат**.</span><span class="sxs-lookup"><span data-stu-id="33f4d-115">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1. <span data-ttu-id="33f4d-116">Опубликуйте файл определений в Power BI.</span><span class="sxs-lookup"><span data-stu-id="33f4d-116">Publish the definition file to Power BI.</span></span>
2. <span data-ttu-id="33f4d-117">Выполните вход в PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="33f4d-117">Sign in to PowerBI.com.</span></span>
3. <span data-ttu-id="33f4d-118">Найдите набор данных для содержимого Power BI **Анализ учета затрат**.</span><span class="sxs-lookup"><span data-stu-id="33f4d-118">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4. <span data-ttu-id="33f4d-119">Откройте страницу безопасности.</span><span class="sxs-lookup"><span data-stu-id="33f4d-119">Open the security page.</span></span>

    ![Открытие страницы безопасности](./media/CA-picture-1.png)

5. <span data-ttu-id="33f4d-121">Роль **Контроллер объектов затрат** уже создана.</span><span class="sxs-lookup"><span data-stu-id="33f4d-121">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="33f4d-122">Добавьте других членов, являющихся частью организационной иерархии уровня доступа модуля "Учет затрат".</span><span class="sxs-lookup"><span data-stu-id="33f4d-122">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span>

    ![Добавление членов](./media/CA-picture-2.png)

<span data-ttu-id="33f4d-124">Пользователи, которые будут добавлены к роли **Контроллер объектов затрат**, будут видеть только данные, которые им разрешено просматривать, в соответствии с определениями в организационной иерархии уровня доступа модуля "Учет затрат".</span><span class="sxs-lookup"><span data-stu-id="33f4d-124">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="33f4d-125">Безопасность на уровне строк применяется к тем плиткам и отчетам, которые встроены из Power BI.</span><span class="sxs-lookup"><span data-stu-id="33f4d-125">Row-level security applies to tiles and reports that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="33f4d-126">Обновление безопасности</span><span class="sxs-lookup"><span data-stu-id="33f4d-126">Updating security</span></span>
<span data-ttu-id="33f4d-127">Если безопасность уровня доступа в модуле "Учет затрат" обновлена и вам требуется, чтобы в Power BI отражались эти обновления, необходимо обновить хранилище объектов для содержимого Power BI **Аналитика учета затрат**.</span><span class="sxs-lookup"><span data-stu-id="33f4d-127">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="33f4d-128">После завершения обновления хранилища объектов необходимо обновить артефакты на PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="33f4d-128">After you complete the entity store update you must update the artifacts on PowerBI.com.</span></span> <span data-ttu-id="33f4d-129">Дополнительные сведения о том, как выполняется обновление хранилища объектов, см. в разделе [Интеграция Power BI с хранилищем объектов](power-bi-integration-entity-store.md#update-entity-store).</span><span class="sxs-lookup"><span data-stu-id="33f4d-129">For more information about how to do an entity store update, see [Power BI integration with Entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="33f4d-130">Владелец содержимого Power BI **Анализ учета затрат** должен также выполнить обновление хранилища объектов, если новым пользователям предоставлен доступ к организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="33f4d-130">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="33f4d-131">Кроме того, владелец должен добавить новых пользователей в роль **Контроллер объектов затрат** на PowerBI.com, чтобы к ним применялась безопасность на уровне строк.</span><span class="sxs-lookup"><span data-stu-id="33f4d-131">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="33f4d-132">Отключение защиты</span><span class="sxs-lookup"><span data-stu-id="33f4d-132">Disabling security</span></span>
<span data-ttu-id="33f4d-133">Мы полагаем, что ваша организация хочет ограничить доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="33f4d-133">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="33f4d-134">Если по какой-либо причине параметры безопасности отключены при выполнении учета затрат, владелец должен вместо этого добавить пользователей в роль **Бухгалтер по учету затрат** в Power BI.</span><span class="sxs-lookup"><span data-stu-id="33f4d-134">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="33f4d-135">При изменении безопасности с включенного состояния на отключенное рекомендуется удалить пользователей из роли **Контроллер объектов затрат**.</span><span class="sxs-lookup"><span data-stu-id="33f4d-135">If you change security from an enabled state to a disabled state, it's a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="33f4d-136">И наоборот при повторном включении безопасности.</span><span class="sxs-lookup"><span data-stu-id="33f4d-136">And vice versa if you re-enable security.</span></span> <span data-ttu-id="33f4d-137">Пользователи могут принадлежать к обеим ролям.</span><span class="sxs-lookup"><span data-stu-id="33f4d-137">Users can belong to both roles.</span></span> <span data-ttu-id="33f4d-138">Совместный доступ является объединением обеих ролей.</span><span class="sxs-lookup"><span data-stu-id="33f4d-138">Joint access is the union of both roles.</span></span> <span data-ttu-id="33f4d-139">В случает содержимого Power BI **Анализ учета затрат** пользователи, имеющие совместный доступ, обладают ограниченным доступом к данным.</span><span class="sxs-lookup"><span data-stu-id="33f4d-139">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="33f4d-140">Если ваша цель заключается в том, чтобы применить ограниченный доступ, пользователи должны быть назначены только роли **Контроллер объектов затрат**.</span><span class="sxs-lookup"><span data-stu-id="33f4d-140">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="33f4d-141">Эти обновления безопасности на уровне строк вступают в силу немедленно.</span><span class="sxs-lookup"><span data-stu-id="33f4d-141">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="33f4d-142">Соответствующие пользователи должны обновить страницы в своих браузерах.</span><span class="sxs-lookup"><span data-stu-id="33f4d-142">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33f4d-143">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="33f4d-143">Additional resources</span></span>
<span data-ttu-id="33f4d-144">Для получения дополнительных сведений о безопасности на уровне строк Power BI см. раздел [Управления безопасностью в своей модели в Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="33f4d-144">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>
