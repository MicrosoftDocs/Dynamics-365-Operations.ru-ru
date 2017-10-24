---
title: "Домашняя страница мобильного приложения"
description: "В этом разделе описывается мобильное приложение Microsoft Dynamics 365 for Unified Operations и предоставляются ссылки на ресурсы, которые помогут вам реализовать его в вашей организации."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: c73eeaaf28df8db720431d4bcd317c9721baa99d
ms.openlocfilehash: 08dcdf2f5c03de17d50910e617d20e734e6ee31e
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="mobile-app-home-page"></a><span data-ttu-id="2c974-103">Домашняя страница мобильного приложения</span><span class="sxs-lookup"><span data-stu-id="2c974-103">Mobile app home page</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2c974-104">В этом разделе описывается мобильное приложение Microsoft Dynamics 365 for Unified Operations и предоставляются ссылки на ресурсы, которые помогут вам реализовать его в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="2c974-104">This topic describes the Microsoft Dynamics 365 for Unified Operations mobile app and provides links to resources that can help you implement it in your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="2c974-105">Прежнее название мобильного приложения — *Microsoft Dynamics 365 for Finance and Operations*.</span><span class="sxs-lookup"><span data-stu-id="2c974-105">The mobile app was previously named *Microsoft Dynamics 365 for Finance and Operations*.</span></span>

<a name="overview"></a><span data-ttu-id="2c974-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="2c974-106">Overview</span></span>
--------

<span data-ttu-id="2c974-107">Мобильное приложение позволяет вашей организации сделать свои бизнес-процессы доступными для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="2c974-107">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="2c974-108">После того как ваш ИТ-администратор включит функцию мобильных рабочих областей для вашей организации, пользователи могут войти в приложение и немедленно приступить к выполнению бизнес-процессов со своих мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="2c974-108">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="2c974-109">Мобильное приложение включает в себя следующие функции, которые могут помочь повысить производительность:</span><span class="sxs-lookup"><span data-stu-id="2c974-109">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="2c974-110">Пользователи могут просматривать и редактировать бизнес-данные, а также действовать на их основе, даже если они имеют непостоянное подключение к сети или их мобильные устройства полностью отключены от сети.</span><span class="sxs-lookup"><span data-stu-id="2c974-110">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="2c974-111">Когда устройство восстанавливает подключение к сети, операций с данными в автономном режиме автоматически синхронизируются с Dynamics 365 for Finance and Operations, Enterprise edition или Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2c974-111">When a device reestablishes a network connection, offline data operations are automatically synchronized with Dynamics 365 for Finance and Operations, Enterprise edition, or Microsoft Dynamics 365 for Finance and Operations.</span></span>
- <span data-ttu-id="2c974-112">Администраторы ИТ или разработчики могут создавать и публиковать мобильные рабочие области, которые были адаптированы для их организации.</span><span class="sxs-lookup"><span data-stu-id="2c974-112">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="2c974-113">Приложение использует существующие ресурсы кода.</span><span class="sxs-lookup"><span data-stu-id="2c974-113">The app uses your existing code assets.</span></span> <span data-ttu-id="2c974-114">Таким образом, не нужно повторно реализовать ваши процедуры проверки, бизнес-логику или конфигурацию безопасности.</span><span class="sxs-lookup"><span data-stu-id="2c974-114">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="2c974-115">Администраторы ИТ или разработчики могут легко разрабатывать мобильные рабочие области с помощью конструктора рабочих областей типа "указать и нажать", который входит в состав веб-клиента.</span><span class="sxs-lookup"><span data-stu-id="2c974-115">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="2c974-116">Администраторы ИТ или разработчики при необходимости могут оптимизировать возможности автономной работы рабочих областей с помощью платформы расширения бизнес-логики.</span><span class="sxs-lookup"><span data-stu-id="2c974-116">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="2c974-117">Поскольку данные по-прежнему будет обрабатываться, пока устройство является автономным, мобильные сценарии остаются содержательными и гибкими, даже если у устройства нет постоянного сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="2c974-117">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="2c974-118">Элементы мобильного приложения</span><span class="sxs-lookup"><span data-stu-id="2c974-118">Elements of the mobile app</span></span>
<span data-ttu-id="2c974-119">Навигация в мобильном приложении состоит из четырех простых концепций: панель мониторинга, рабочие области, страницы и действия.</span><span class="sxs-lookup"><span data-stu-id="2c974-119">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="2c974-120">[![Концепции навигации в мобильном приложении](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="2c974-120">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="2c974-121">При запуске приложения можно перейти к **панель мониторинга**.</span><span class="sxs-lookup"><span data-stu-id="2c974-121">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="2c974-122">На панели мониторинга находится список **рабочих областей**, которые были опубликованы.</span><span class="sxs-lookup"><span data-stu-id="2c974-122">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="2c974-123">В каждой рабочей области можно просмотреть список **страниц**, доступных для этой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2c974-123">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="2c974-124">После перехода на страницу можно выполнить ряд действий.</span><span class="sxs-lookup"><span data-stu-id="2c974-124">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="2c974-125">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="2c974-125">Here are some examples:</span></span>

    - <span data-ttu-id="2c974-126">Просмотр подробных данных.</span><span class="sxs-lookup"><span data-stu-id="2c974-126">View detailed data.</span></span>
    - <span data-ttu-id="2c974-127">Переход на другие страницы для соответствующих данных, например со сведениями о записи или строках.</span><span class="sxs-lookup"><span data-stu-id="2c974-127">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="2c974-128">Просмотр списка **действий**, которые доступны для этой страницы.</span><span class="sxs-lookup"><span data-stu-id="2c974-128">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="2c974-129">Действия позволяют создавать или редактировать существующие данные.</span><span class="sxs-lookup"><span data-stu-id="2c974-129">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="2c974-130">Процесс внедрения</span><span class="sxs-lookup"><span data-stu-id="2c974-130">Implementation process</span></span>
<span data-ttu-id="2c974-131">На следующем рисунке показан процесс реализации мобильных рабочих областей, предоставляемых корпорацией Майкрософт, и пользовательских мобильных рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="2c974-131">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

![Процесс внедрения мобильных приложений](./media/Mobile-implementation-process-5.png)

<span data-ttu-id="2c974-133">Следующая таблица содержит ссылки на ресурсы, которые помогут вам реализовать мобильные рабочие области, предоставляемые корпорацией Майкрософт, так и пользовательские мобильные рабочие области.</span><span class="sxs-lookup"><span data-stu-id="2c974-133">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="2c974-134">Цифры в первом столбце соответствуют пронумерованным шагам на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="2c974-134">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c974-135">Шаг</span><span class="sxs-lookup"><span data-stu-id="2c974-135">Step</span></span></th>
<th><span data-ttu-id="2c974-136">Роль</span><span class="sxs-lookup"><span data-stu-id="2c974-136">Role</span></span></th>
<th><span data-ttu-id="2c974-137">Действие</span><span class="sxs-lookup"><span data-stu-id="2c974-137">Action</span></span></th>
<th><span data-ttu-id="2c974-138">Ресурсы, помогающие выполнить действие</span><span class="sxs-lookup"><span data-stu-id="2c974-138">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2c974-139">1</span><span class="sxs-lookup"><span data-stu-id="2c974-139">1</span></span></td>
<td><span data-ttu-id="2c974-140">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="2c974-140">System administrator</span></span></td>
<td><span data-ttu-id="2c974-141">Внедрение Finance and Operations или Finance and Operations в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="2c974-141">Implement Finance and Operations or Finance and Operations in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="2c974-142">Если у вас еще не была развернута версия Microsoft Dynamics 365, см. раздел <a href="../deployment/deploy-demo-environment.md">Развертывание демонстрационной среды</a>.</span><span class="sxs-lookup"><span data-stu-id="2c974-142">If you haven't yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="2c974-143">Чтобы просмотреть список мобильных рабочих областей, которые можно использовать, см. раздел <a href="mobile-workspaces-released.md">Недавно выпущенные мобильные рабочие области</a>.</span><span class="sxs-lookup"><span data-stu-id="2c974-143">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c974-144">2</span><span class="sxs-lookup"><span data-stu-id="2c974-144">2</span></span></td>
<td><span data-ttu-id="2c974-145">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="2c974-145">System administrator</span></span></td>
<td><span data-ttu-id="2c974-146"><strong>Если вы используете Microsoft Dynamics 365 for Finance and Operations версии 1611:</strong> загрузите и установите КБ, обеспечивающие использование мобильных рабочих областей, которые предоставляются корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="2c974-146"><strong>If you're using Microsoft Dynamics 365 for Finance and Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="2c974-147">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="2c974-147">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="2c974-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Мобильные рабочие области управления затратами</a></span><span class="sxs-lookup"><span data-stu-id="2c974-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="2c974-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Мобильная рабочая область запасов в наличии</a></span><span class="sxs-lookup"><span data-stu-id="2c974-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="2c974-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Мобильные рабочие области заказов на продажу</a></span><span class="sxs-lookup"><span data-stu-id="2c974-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="2c974-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Мобильная рабочая область совместной работы с поставщиками</a></span><span class="sxs-lookup"><span data-stu-id="2c974-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="2c974-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Мобильная рабочая область регистрации времени по проектам</a></span><span class="sxs-lookup"><span data-stu-id="2c974-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="2c974-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Мобильная рабочая область управления расходами</a></span><span class="sxs-lookup"><span data-stu-id="2c974-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c974-154">3</span><span class="sxs-lookup"><span data-stu-id="2c974-154">3</span></span></td>
<td><span data-ttu-id="2c974-155">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="2c974-155">System administrator</span></span></td>
<td><span data-ttu-id="2c974-156">Опубликуйте мобильные рабочие области, поставляемые корпорацией Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2c974-156">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="2c974-157"><a href="publish-mobile-workspace.md">Публикация мобильной рабочей области</a>
</span><span class="sxs-lookup"><span data-stu-id="2c974-157"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c974-158">4</span><span class="sxs-lookup"><span data-stu-id="2c974-158">4</span></span></td>
<td><span data-ttu-id="2c974-159">Разработчик или независимый поставщик программного обеспечения (ISV)</span><span class="sxs-lookup"><span data-stu-id="2c974-159">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="2c974-160">Используйте мобильную платформу для создания настраиваемых мобильных рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="2c974-160">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="2c974-161"><a href="platform/mobile-platform-home-page.md">Мобильная платформа</a></span><span class="sxs-lookup"><span data-stu-id="2c974-161"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c974-162">5</span><span class="sxs-lookup"><span data-stu-id="2c974-162">5</span></span></td>
<td><span data-ttu-id="2c974-163">ISV</span><span class="sxs-lookup"><span data-stu-id="2c974-163">ISV</span></span></td>
<td><span data-ttu-id="2c974-164">Создайте пакет развертывания, содержащий настраиваемые мобильные рабочие области, и отправьте пакет в службы Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="2c974-164">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="2c974-165"><a href="../deployment/create-apply-deployable-package.md">Создание пакета развертывания</a></span><span class="sxs-lookup"><span data-stu-id="2c974-165"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c974-166">6</span><span class="sxs-lookup"><span data-stu-id="2c974-166">6</span></span></td>
<td><span data-ttu-id="2c974-167">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="2c974-167">System administrator</span></span></td>
<td><span data-ttu-id="2c974-168">Примените пакет развертывания, содержащий настраиваемые рабочие области, предоставленные независимым производителем программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="2c974-168">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="2c974-169"><a href="../deployment/apply-deployable-package-system.md">Применение готового к развертыванию пакета</a></span><span class="sxs-lookup"><span data-stu-id="2c974-169"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c974-170">7</span><span class="sxs-lookup"><span data-stu-id="2c974-170">7</span></span></td>
<td><span data-ttu-id="2c974-171">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="2c974-171">System administrator</span></span></td>
<td><span data-ttu-id="2c974-172">Опубликуйте настраиваемые мобильные рабочие области, поставляемые независимым разработчиком программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="2c974-172">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="2c974-173"><a href="publish-mobile-workspace.md">Публикация мобильной рабочей области</a></span><span class="sxs-lookup"><span data-stu-id="2c974-173"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c974-174">8</span><span class="sxs-lookup"><span data-stu-id="2c974-174">8</span></span></td>
<td><span data-ttu-id="2c974-175">Пользователь</span><span class="sxs-lookup"><span data-stu-id="2c974-175">User</span></span></td>
<td><span data-ttu-id="2c974-176">Загрузите и установите мобильное приложение.</span><span class="sxs-lookup"><span data-stu-id="2c974-176">Download and install the mobile app.</span></span></td>
<td><ul>
<li><span data-ttu-id="2c974-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">Для ОС Android</a></span><span class="sxs-lookup"><span data-stu-id="2c974-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">For Android phones</a></span></span></li>
<li><span data-ttu-id="2c974-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">Для iPhone</a></span><span class="sxs-lookup"><span data-stu-id="2c974-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">For iPhones</a></span></span></li></ul>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c974-179">9</span><span class="sxs-lookup"><span data-stu-id="2c974-179">9</span></span></td>
<td><span data-ttu-id="2c974-180">Пользователь</span><span class="sxs-lookup"><span data-stu-id="2c974-180">User</span></span></td>
<td><span data-ttu-id="2c974-181">Войдите в систему в мобильном приложении и начните работу.</span><span class="sxs-lookup"><span data-stu-id="2c974-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="2c974-182">Приложение включает в себя мобильные рабочие области, которые были опубликованы системным администратором.</span><span class="sxs-lookup"><span data-stu-id="2c974-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="2c974-183">Чтобы просмотреть список мобильных рабочих областей, которые предоставлены корпорацией Майкрософт, см. раздел <a href="mobile-workspaces-released.md">Недавно выпущенные мобильные рабочие области</a>.</span><span class="sxs-lookup"><span data-stu-id="2c974-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>
