---
title: Домашняя страница мобильного приложения
description: В этом разделе описывается мобильное приложение Finance and Operations и предоставляются ссылки на ресурсы, которые помогут вам реализовать его в вашей организации.
author: sericks007
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: a8183dd834b1f39773d25fa7c546d5db1c7b7749
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249034"
---
# <a name="mobile-app-home-page"></a><span data-ttu-id="e0505-103">Домашняя страница мобильного приложения</span><span class="sxs-lookup"><span data-stu-id="e0505-103">Mobile app home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0505-104">В этом разделе описывается мобильное приложение Finance and Operations и предоставляются ссылки на ресурсы, которые помогут вам реализовать его в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="e0505-104">This topic describes the Finance and Operations Operations mobile app and provides links to resources that can help you implement it in your organization.</span></span>

<a name="overview"></a><span data-ttu-id="e0505-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="e0505-105">Overview</span></span>
--------

<span data-ttu-id="e0505-106">Мобильное приложение позволяет вашей организации сделать свои бизнес-процессы доступными для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="e0505-106">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="e0505-107">После того как ваш ИТ-администратор включит функцию мобильных рабочих областей для вашей организации, пользователи могут войти в приложение и немедленно приступить к выполнению бизнес-процессов со своих мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="e0505-107">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="e0505-108">Мобильное приложение включает в себя следующие функции, которые могут помочь повысить производительность:</span><span class="sxs-lookup"><span data-stu-id="e0505-108">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="e0505-109">Пользователи могут просматривать и редактировать бизнес-данные, а также действовать на их основе, даже если они имеют непостоянное подключение к сети или их мобильные устройства полностью отключены от сети.</span><span class="sxs-lookup"><span data-stu-id="e0505-109">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="e0505-110">Когда устройство восстанавливает подключение к сети, операций с данными в автономном режиме автоматически синхронизируются.</span><span class="sxs-lookup"><span data-stu-id="e0505-110">When a device reestablishes a network connection, offline data operations are automatically synchronized.</span></span>
- <span data-ttu-id="e0505-111">Администраторы ИТ или разработчики могут создавать и публиковать мобильные рабочие области, которые были адаптированы для их организации.</span><span class="sxs-lookup"><span data-stu-id="e0505-111">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="e0505-112">Приложение использует существующие ресурсы кода.</span><span class="sxs-lookup"><span data-stu-id="e0505-112">The app uses your existing code assets.</span></span> <span data-ttu-id="e0505-113">Таким образом, не нужно повторно реализовать ваши процедуры проверки, бизнес-логику или конфигурацию безопасности.</span><span class="sxs-lookup"><span data-stu-id="e0505-113">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="e0505-114">Администраторы ИТ или разработчики могут легко разрабатывать мобильные рабочие области с помощью конструктора рабочих областей типа "указать и нажать", который входит в состав веб-клиента.</span><span class="sxs-lookup"><span data-stu-id="e0505-114">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="e0505-115">Администраторы ИТ или разработчики при необходимости могут оптимизировать возможности автономной работы рабочих областей с помощью платформы расширения бизнес-логики.</span><span class="sxs-lookup"><span data-stu-id="e0505-115">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="e0505-116">Поскольку данные по-прежнему будет обрабатываться, пока устройство является автономным, мобильные сценарии остаются содержательными и гибкими, даже если у устройства нет постоянного сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="e0505-116">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="e0505-117">Элементы мобильного приложения</span><span class="sxs-lookup"><span data-stu-id="e0505-117">Elements of the mobile app</span></span>
<span data-ttu-id="e0505-118">Навигация в мобильном приложении состоит из четырех простых концепций: панель мониторинга, рабочие области, страницы и действия.</span><span class="sxs-lookup"><span data-stu-id="e0505-118">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="e0505-119">[![Концепции навигации в мобильном приложении](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="e0505-119">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="e0505-120">При запуске приложения можно перейти к **панель мониторинга**.</span><span class="sxs-lookup"><span data-stu-id="e0505-120">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="e0505-121">На панели мониторинга находится список **рабочих областей**, которые были опубликованы.</span><span class="sxs-lookup"><span data-stu-id="e0505-121">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="e0505-122">В каждой рабочей области можно просмотреть список **страниц**, доступных для этой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e0505-122">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="e0505-123">После перехода на страницу можно выполнить ряд действий.</span><span class="sxs-lookup"><span data-stu-id="e0505-123">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="e0505-124">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="e0505-124">Here are some examples:</span></span>

    - <span data-ttu-id="e0505-125">Просмотр подробных данных.</span><span class="sxs-lookup"><span data-stu-id="e0505-125">View detailed data.</span></span>
    - <span data-ttu-id="e0505-126">Переход на другие страницы для соответствующих данных, например со сведениями о записи или строках.</span><span class="sxs-lookup"><span data-stu-id="e0505-126">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="e0505-127">Просмотр списка **действий**, которые доступны для этой страницы.</span><span class="sxs-lookup"><span data-stu-id="e0505-127">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="e0505-128">Действия позволяют создавать или редактировать существующие данные.</span><span class="sxs-lookup"><span data-stu-id="e0505-128">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="e0505-129">Процесс внедрения</span><span class="sxs-lookup"><span data-stu-id="e0505-129">Implementation process</span></span>
<span data-ttu-id="e0505-130">На следующем рисунке показан процесс реализации мобильных рабочих областей, предоставляемых корпорацией Майкрософт, и пользовательских мобильных рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="e0505-130">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

<span data-ttu-id="e0505-131">[![Процесс внедрения мобильных приложений](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span><span class="sxs-lookup"><span data-stu-id="e0505-131">[![Mobile apps implementation process](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span></span>

<span data-ttu-id="e0505-132">Следующая таблица содержит ссылки на ресурсы, которые помогут вам реализовать мобильные рабочие области, предоставляемые корпорацией Майкрософт, так и пользовательские мобильные рабочие области.</span><span class="sxs-lookup"><span data-stu-id="e0505-132">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="e0505-133">Цифры в первом столбце соответствуют пронумерованным шагам на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="e0505-133">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e0505-134">Шаг</span><span class="sxs-lookup"><span data-stu-id="e0505-134">Step</span></span></th>
<th><span data-ttu-id="e0505-135">Роль</span><span class="sxs-lookup"><span data-stu-id="e0505-135">Role</span></span></th>
<th><span data-ttu-id="e0505-136">Действие</span><span class="sxs-lookup"><span data-stu-id="e0505-136">Action</span></span></th>
<th><span data-ttu-id="e0505-137">Ресурсы, помогающие выполнить действие</span><span class="sxs-lookup"><span data-stu-id="e0505-137">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0505-138">1</span><span class="sxs-lookup"><span data-stu-id="e0505-138">1</span></span></td>
<td><span data-ttu-id="e0505-139">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="e0505-139">System administrator</span></span></td>
<td><span data-ttu-id="e0505-140">Внедрите приложения Finance and Operations в своей организации.</span><span class="sxs-lookup"><span data-stu-id="e0505-140">Implement Finance and Operations apps in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="e0505-141">Если у вас еще не была развернута версия Microsoft Dynamics 365, см. раздел <a href="../deployment/deploy-demo-environment.md">Развертывание демонстрационной среды</a>.</span><span class="sxs-lookup"><span data-stu-id="e0505-141">If you haven&#39;t yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="e0505-142">Чтобы просмотреть список мобильных рабочих областей, которые можно использовать, см. раздел <a href="mobile-workspaces-released.md">Недавно выпущенные мобильные рабочие области</a>.</span><span class="sxs-lookup"><span data-stu-id="e0505-142">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0505-143">2</span><span class="sxs-lookup"><span data-stu-id="e0505-143">2</span></span></td>
<td><span data-ttu-id="e0505-144">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="e0505-144">System administrator</span></span></td>
<td><span data-ttu-id="e0505-145"><strong>Если вы используете Microsoft Dynamics 365 for Operations версии 1611:</strong> загрузите и установите KB, обеспечивающие использование мобильных рабочих областей, которые предоставляются корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="e0505-145"><strong>If you&#39;re using Microsoft Dynamics 365 for Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="e0505-146">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="e0505-146">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="e0505-147"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Мобильные рабочие области управления затратами</a></span><span class="sxs-lookup"><span data-stu-id="e0505-147"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="e0505-148"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Мобильная рабочая область запасов в наличии</a></span><span class="sxs-lookup"><span data-stu-id="e0505-148"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="e0505-149"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Мобильные рабочие области заказов на продажу</a></span><span class="sxs-lookup"><span data-stu-id="e0505-149"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="e0505-150"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Мобильная рабочая область совместной работы с поставщиками</a></span><span class="sxs-lookup"><span data-stu-id="e0505-150"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="e0505-151"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Мобильная рабочая область регистрации времени по проектам</a></span><span class="sxs-lookup"><span data-stu-id="e0505-151"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="e0505-152"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Мобильная рабочая область управления расходами</a></span><span class="sxs-lookup"><span data-stu-id="e0505-152"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0505-153">3</span><span class="sxs-lookup"><span data-stu-id="e0505-153">3</span></span></td>
<td><span data-ttu-id="e0505-154">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="e0505-154">System administrator</span></span></td>
<td><span data-ttu-id="e0505-155">Опубликуйте мобильные рабочие области, поставляемые корпорацией Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e0505-155">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="e0505-156"><a href="publish-mobile-workspace.md">Публикация мобильной рабочей области</a>
</span><span class="sxs-lookup"><span data-stu-id="e0505-156"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0505-157">4</span><span class="sxs-lookup"><span data-stu-id="e0505-157">4</span></span></td>
<td><span data-ttu-id="e0505-158">Разработчик или независимый поставщик программного обеспечения (ISV)</span><span class="sxs-lookup"><span data-stu-id="e0505-158">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="e0505-159">Используйте мобильную платформу для создания настраиваемых мобильных рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="e0505-159">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="e0505-160"><a href="platform/mobile-platform-home-page.md">Мобильная платформа</a></span><span class="sxs-lookup"><span data-stu-id="e0505-160"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0505-161">5</span><span class="sxs-lookup"><span data-stu-id="e0505-161">5</span></span></td>
<td><span data-ttu-id="e0505-162">ISV</span><span class="sxs-lookup"><span data-stu-id="e0505-162">ISV</span></span></td>
<td><span data-ttu-id="e0505-163">Создайте пакет развертывания, содержащий настраиваемые мобильные рабочие области, и отправьте пакет в службы Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="e0505-163">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="e0505-164"><a href="../deployment/create-apply-deployable-package.md">Создание готового к развертыванию пакета</a></span><span class="sxs-lookup"><span data-stu-id="e0505-164"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0505-165">6</span><span class="sxs-lookup"><span data-stu-id="e0505-165">6</span></span></td>
<td><span data-ttu-id="e0505-166">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="e0505-166">System administrator</span></span></td>
<td><span data-ttu-id="e0505-167">Примените пакет развертывания, содержащий настраиваемые рабочие области, предоставленные независимым производителем программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="e0505-167">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="e0505-168"><a href="../deployment/apply-deployable-package-system.md">Применение готового к развертыванию пакета</a></span><span class="sxs-lookup"><span data-stu-id="e0505-168"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0505-169">7</span><span class="sxs-lookup"><span data-stu-id="e0505-169">7</span></span></td>
<td><span data-ttu-id="e0505-170">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="e0505-170">System administrator</span></span></td>
<td><span data-ttu-id="e0505-171">Опубликуйте настраиваемые мобильные рабочие области, поставляемые независимым разработчиком программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="e0505-171">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="e0505-172"><a href="publish-mobile-workspace.md">Публикация мобильной рабочей области</a></span><span class="sxs-lookup"><span data-stu-id="e0505-172"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0505-173">8</span><span class="sxs-lookup"><span data-stu-id="e0505-173">8</span></span></td>
<td><span data-ttu-id="e0505-174">Пользователь</span><span class="sxs-lookup"><span data-stu-id="e0505-174">User</span></span></td>
<td><span data-ttu-id="e0505-175">Загрузите и установите мобильное приложение.</span><span class="sxs-lookup"><span data-stu-id="e0505-175">Download and install the mobile app.</span></span></td>
<td><span data-ttu-id="e0505-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Приложение Finance and Operations для Android</a></span><span class="sxs-lookup"><span data-stu-id="e0505-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations app for Android</a></span></span><BR/><span data-ttu-id="e0505-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Приложение Finance and Operations для iOS</a></span><span class="sxs-lookup"><span data-stu-id="e0505-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations app for iOS</a></span></span><BR/>
<span data-ttu-id="e0505-178">(Windows Phone не поддерживается)</span><span class="sxs-lookup"><span data-stu-id="e0505-178">(Windows Phone unsupported)</span></span>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0505-179">9</span><span class="sxs-lookup"><span data-stu-id="e0505-179">9</span></span></td>
<td><span data-ttu-id="e0505-180">Пользователь</span><span class="sxs-lookup"><span data-stu-id="e0505-180">User</span></span></td>
<td><span data-ttu-id="e0505-181">Войдите в систему в мобильном приложении и начните работу.</span><span class="sxs-lookup"><span data-stu-id="e0505-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="e0505-182">Приложение включает в себя мобильные рабочие области, которые были опубликованы системным администратором.</span><span class="sxs-lookup"><span data-stu-id="e0505-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="e0505-183">Чтобы просмотреть список мобильных рабочих областей, которые предоставлены корпорацией Майкрософт, см. раздел <a href="mobile-workspaces-released.md">Недавно выпущенные мобильные рабочие области</a>.</span><span class="sxs-lookup"><span data-stu-id="e0505-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>
