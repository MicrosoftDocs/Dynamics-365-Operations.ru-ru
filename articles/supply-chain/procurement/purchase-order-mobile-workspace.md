---
title: Мобильная рабочая область "Утверждение заказа на покупку"
description: В этой теме содержится информация о мобильной рабочей области "Утверждение заказа на покупку", которая позволяет просматривать заказы на покупку и отвечать на них посредством действий. Например, можно утвердить или отклонить заказ на покупку.
author: RichardLuan
manager: tfehr
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 37c0fc273091af260089229ad9ee66b52dce3831
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215993"
---
# <a name="purchase-order-approval-mobile-workspace"></a><span data-ttu-id="a0b34-104">Мобильная рабочая область "Утверждение заказа на покупку"</span><span class="sxs-lookup"><span data-stu-id="a0b34-104">Purchase order approval mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0b34-105">В этой теме содержится информация о мобильной рабочей области **Утверждение заказа на покупку**.</span><span class="sxs-lookup"><span data-stu-id="a0b34-105">This topic provides information about the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="a0b34-106">Эта рабочая область позволяет просматривать заказы на покупку и отвечать на них посредством действий.</span><span class="sxs-lookup"><span data-stu-id="a0b34-106">This workspace lets you view purchase orders and respond to them through actions.</span></span> <span data-ttu-id="a0b34-107">Например, можно утвердить или отклонить заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="a0b34-107">For example, you can approve or reject a purchase order.</span></span>
 
## <a name="overview"></a><span data-ttu-id="a0b34-108">Обзор</span><span class="sxs-lookup"><span data-stu-id="a0b34-108">Overview</span></span> 
<span data-ttu-id="a0b34-109">Заказы на покупку, требующие утверждения, проходят через workflow-процесс утверждения.</span><span class="sxs-lookup"><span data-stu-id="a0b34-109">Purchase orders that requires approval go through an approval workflow.</span></span> <span data-ttu-id="a0b34-110">Workflow-процесс может включать различные этапы, которые требуют действий со стороны одного или нескольких пользователей.</span><span class="sxs-lookup"><span data-stu-id="a0b34-110">The workflow can include various steps that require that one or more people take action.</span></span> <span data-ttu-id="a0b34-111">Например, пользователю может потребоваться выполнить задачу или утвердить заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="a0b34-111">For example, a person might have to complete a task or approve the purchase order.</span></span> 

<span data-ttu-id="a0b34-112">Мобильная рабочая область **Утверждение заказа на покупку** позволяет легко просматривать заказы на покупку и утверждать их с мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="a0b34-112">The **Purchase order approval** mobile workspace lets you easily view and respond to purchase orders from your mobile device.</span></span> <span data-ttu-id="a0b34-113">Эта рабочая область также позволяет выполнять те же действия workflow-процесса, что и в веб-клиенте.</span><span class="sxs-lookup"><span data-stu-id="a0b34-113">This workspace also lets you take the same workflow actions that you can take from the web client.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a0b34-114">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="a0b34-114">Prerequisites</span></span>
<span data-ttu-id="a0b34-115">Необходимые условия различаются в зависимости от версии Supply Chain Management, развернутой в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="a0b34-115">The prerequisites vary, depending on the version of Supply Chain Management that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-supply-chain-management"></a><span data-ttu-id="a0b34-116">Необходимые условия при использовании Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a0b34-116">Prerequisites if you use Supply Chain Management</span></span> 
<span data-ttu-id="a0b34-117">Если в вашей организации развернута система Supply Chain Management, системный администратор должен опубликовать мобильную рабочую область **Утверждение заказа на покупку**.</span><span class="sxs-lookup"><span data-stu-id="a0b34-117">If Supply Chain Management has been deployed for your organization, the system administrator must publish the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="a0b34-118">См. инструкции в [Публикация мобильной рабочей области](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="a0b34-118">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="a0b34-119">Необходимые условия при использовании Microsoft Dynamics 365 for Operations версии 1611 с обновлением платформы 3 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a0b34-119">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="a0b34-120">Если в вашей организации развернута система Microsoft Dynamics 365 for Operations версии 1611 с обновлением платформы 3 или более поздней версии, системный администратор должен выполнить следующие условия.</span><span class="sxs-lookup"><span data-stu-id="a0b34-120">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a0b34-121">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="a0b34-121">Prerequisite</span></span></th>
<th><span data-ttu-id="a0b34-122">Роль</span><span class="sxs-lookup"><span data-stu-id="a0b34-122">Role</span></span></th>
<th><span data-ttu-id="a0b34-123">описание</span><span class="sxs-lookup"><span data-stu-id="a0b34-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0b34-124">Реализовать КБ 4017918.</span><span class="sxs-lookup"><span data-stu-id="a0b34-124">Implement KB 4017918.</span></span></td>
<td><span data-ttu-id="a0b34-125">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="a0b34-125">System administrator</span></span></td>
<td><span data-ttu-id="a0b34-126">KB 4017918 является обновлением X++ или исправлением метаданных, содержащим мобильную рабочую область <strong>Утверждение заказа на покупку</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0b34-126">KB 4017918 is an X++ update or metadata hotfix that contains the <strong>Purchase order approval</strong> mobile workspace.</span></span> <span data-ttu-id="a0b34-127">Для установки KB 4017918 системный администратор должен выполнить следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="a0b34-127">To implement KB 4017918, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="a0b34-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Загрузите исправление метаданных из Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="a0b34-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="a0b34-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Установите исправление метаданных</a>.</span><span class="sxs-lookup"><span data-stu-id="a0b34-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="a0b34-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Создайте пакет развертывания</a>, содержащий модель <strong>SCMMobile</strong>, затем отправьте пакет развертывания в LCS.</span><span class="sxs-lookup"><span data-stu-id="a0b34-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="a0b34-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Примените готовый к развертыванию пакет</a>.</span><span class="sxs-lookup"><span data-stu-id="a0b34-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0b34-132">Опубликуйте мобильную рабочую область <strong>Утверждение заказа на покупку</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0b34-132">Publish the <strong>Purchase order approval</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="a0b34-133">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="a0b34-133">System administrator</span></span></td>
<td><span data-ttu-id="a0b34-134">См. <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Публикация мобильной рабочей области</a>.</span><span class="sxs-lookup"><span data-stu-id="a0b34-134">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="a0b34-135">Загрузите и установите мобильное приложение</span><span class="sxs-lookup"><span data-stu-id="a0b34-135">Download and install the mobile app</span></span>
<span data-ttu-id="a0b34-136">Загрузите и установите мобильное приложение Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="a0b34-136">Download and install the Finance and Operations mobile app:</span></span>

- [<span data-ttu-id="a0b34-137">Для телефонов Android</span><span class="sxs-lookup"><span data-stu-id="a0b34-137">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="a0b34-138">Для iPhone</span><span class="sxs-lookup"><span data-stu-id="a0b34-138">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="a0b34-139">Войдите в систему в мобильном приложении</span><span class="sxs-lookup"><span data-stu-id="a0b34-139">Sign in to the mobile app</span></span>

1. <span data-ttu-id="a0b34-140">Запустите приложение на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="a0b34-140">Start the app on your mobile device.</span></span>
2. <span data-ttu-id="a0b34-141">Введите ваш URL-адрес Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a0b34-141">Enter your Microsoft Dynamics 365 URL.</span></span>
3. <span data-ttu-id="a0b34-142">При первом входе появится запрос имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="a0b34-142">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="a0b34-143">Введите свои учетные данные.</span><span class="sxs-lookup"><span data-stu-id="a0b34-143">Enter your credentials.</span></span>
4. <span data-ttu-id="a0b34-144">После входа будут показаны доступные рабочие области для вашей компании.</span><span class="sxs-lookup"><span data-stu-id="a0b34-144">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="a0b34-145">Обратите внимание, что если позже системный администратор опубликует новую рабочую область, вам потребуется обновить список мобильных рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="a0b34-145">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

![Рабочая область "Утверждение заказа на покупку" в списке доступных рабочих областей](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a><span data-ttu-id="a0b34-147">Просмотр назначенных вам заказов</span><span class="sxs-lookup"><span data-stu-id="a0b34-147">View orders that are assigned to you</span></span>
1. <span data-ttu-id="a0b34-148">На мобильном устройстве выберите рабочую область **Утверждение заказа на покупку**.</span><span class="sxs-lookup"><span data-stu-id="a0b34-148">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="a0b34-149">Выберите **Назначенные мне заказы** для просмотра всех заказов, в отношении которых вас просят предпринять действия в workflow-процессе утверждения заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="a0b34-149">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="a0b34-150">Выберите заказ.</span><span class="sxs-lookup"><span data-stu-id="a0b34-150">Select an order.</span></span> <span data-ttu-id="a0b34-151">На странице **Сведения о заказе** вы увидите информацию из заголовка заказа и строки заказа.</span><span class="sxs-lookup"><span data-stu-id="a0b34-151">On the **Order details** page, you will see the order header information and lines.</span></span> <span data-ttu-id="a0b34-152">Также вы найдете здесь инструкции из задачи workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="a0b34-152">You can also find guidelines from the workflow task.</span></span>
4. <span data-ttu-id="a0b34-153">Выберите **Распределение по бухгалтерским счетам**, чтобы открыть страницу **Заголовок — распределение по бухгалтерским счетам**.</span><span class="sxs-lookup"><span data-stu-id="a0b34-153">Select **Accounting distributions** to open the **Header accounting distributions** page.</span></span>
5. <span data-ttu-id="a0b34-154">Вернитесь на страницу **Сведения о заказе** и выберите строку.</span><span class="sxs-lookup"><span data-stu-id="a0b34-154">Return to the **Order details** page, and select a line.</span></span> <span data-ttu-id="a0b34-155">Из сведений о строке заказа можно исследовать распределение по бухгалтерским счетам для данной строки.</span><span class="sxs-lookup"><span data-stu-id="a0b34-155">From the order line details, you can also explore the line-specific accounting distributions.</span></span>

## <a name="complete-an-action-on-the-purchase-order"></a><span data-ttu-id="a0b34-156">Выполнение действия в отношении заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="a0b34-156">Complete an action on the purchase order</span></span>
<span data-ttu-id="a0b34-157">После просмотра назначенного вам заказа на покупку и чтения инструкций workflow-процесса вы должны быть готовы выполнить действие.</span><span class="sxs-lookup"><span data-stu-id="a0b34-157">After you've viewed the purchase order that is assigned to you and read the workflow instructions, you should be ready to take action.</span></span>

1. <span data-ttu-id="a0b34-158">На мобильном устройстве выберите рабочую область **Утверждение заказа на покупку**.</span><span class="sxs-lookup"><span data-stu-id="a0b34-158">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="a0b34-159">Выберите **Назначенные мне заказы** для просмотра всех заказов, в отношении которых вас просят предпринять действия в workflow-процессе утверждения заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="a0b34-159">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="a0b34-160">Выберите заказ и просмотрите страницу сведений.</span><span class="sxs-lookup"><span data-stu-id="a0b34-160">Select an order, and view the details page.</span></span>
4. <span data-ttu-id="a0b34-161">Выберите **Действия**, чтобы отобразить доступные действия.</span><span class="sxs-lookup"><span data-stu-id="a0b34-161">Select **Actions** to show the available actions.</span></span> <span data-ttu-id="a0b34-162">Доступные действия зависят от задачи, которая вам назначена.</span><span class="sxs-lookup"><span data-stu-id="a0b34-162">The actions that are available depend on the task that has been assigned to you.</span></span>

    | <span data-ttu-id="a0b34-163">Действие, связанное с задачей</span><span class="sxs-lookup"><span data-stu-id="a0b34-163">Task action</span></span>    | <span data-ttu-id="a0b34-164">Действие утверждения</span><span class="sxs-lookup"><span data-stu-id="a0b34-164">Approval action</span></span>  |
    |----------------|------------------|
    | <span data-ttu-id="a0b34-165">Подробно</span><span class="sxs-lookup"><span data-stu-id="a0b34-165">Complete</span></span>       | <span data-ttu-id="a0b34-166">Утвердить</span><span class="sxs-lookup"><span data-stu-id="a0b34-166">Approve</span></span>          |
    | <span data-ttu-id="a0b34-167">Возврат</span><span class="sxs-lookup"><span data-stu-id="a0b34-167">Return</span></span>         | <span data-ttu-id="a0b34-168">Отклонить</span><span class="sxs-lookup"><span data-stu-id="a0b34-168">Reject</span></span>           |
    | <span data-ttu-id="a0b34-169">Запросить изменение</span><span class="sxs-lookup"><span data-stu-id="a0b34-169">Request change</span></span> | <span data-ttu-id="a0b34-170">Запросить изменение</span><span class="sxs-lookup"><span data-stu-id="a0b34-170">Request change</span></span>   |
    | <span data-ttu-id="a0b34-171">Представитель</span><span class="sxs-lookup"><span data-stu-id="a0b34-171">Delegate</span></span>       | <span data-ttu-id="a0b34-172">Представитель</span><span class="sxs-lookup"><span data-stu-id="a0b34-172">Delegate</span></span>         |

5. <span data-ttu-id="a0b34-173">Выбор соответствующего действия.</span><span class="sxs-lookup"><span data-stu-id="a0b34-173">Select the appropriate action.</span></span>
6. <span data-ttu-id="a0b34-174">На странице **Завершить задачу** введите комментарий.</span><span class="sxs-lookup"><span data-stu-id="a0b34-174">On the **Complete task** page, enter a comment.</span></span> <span data-ttu-id="a0b34-175">Обратите внимание, что при выборе действия **Делегировать** необходимо выбрать пользователя, которому будет делегирована задача.</span><span class="sxs-lookup"><span data-stu-id="a0b34-175">Note that if you select the **Delegate** action, you must select a user to delegate the task to.</span></span>
7. <span data-ttu-id="a0b34-176">Выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="a0b34-176">Select **Done**.</span></span> <span data-ttu-id="a0b34-177">После обновления рабочей области заказа на покупку больше не будет в вашем списке.</span><span class="sxs-lookup"><span data-stu-id="a0b34-177">After you refresh your workspace, the purchase order will no longer be in your list.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]