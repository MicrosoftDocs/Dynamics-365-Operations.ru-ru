---
title: Настройка рабочих процессов утверждения аренды
description: В этой теме объясняется, как настроить рабочий процесс утверждения, который будет выполняться при создании новой аренды.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0e7280bbf60901266c81a0c89395c5183f991425
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881670"
---
# <a name="set-up-lease-approval-workflows"></a><span data-ttu-id="f2735-103">Настройка рабочих процессов утверждения аренды</span><span class="sxs-lookup"><span data-stu-id="f2735-103">Set up lease approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2735-104">В этой теме объясняется, как настроить рабочий процесс утверждения, который будет выполняться при создании новой аренды.</span><span class="sxs-lookup"><span data-stu-id="f2735-104">The topic explains how to set up an approval workflow that will run when a new lease is created.</span></span> <span data-ttu-id="f2735-105">Дополнительные сведения об использовании рабочего процесса см. в разделе [Использование рабочих процессов утверждения аренды](use-create-lease-wrkflw.md).</span><span class="sxs-lookup"><span data-stu-id="f2735-105">For information about how to use the workflow, see [Use lease approval workflows](use-create-lease-wrkflw.md).</span></span> 

1. <span data-ttu-id="f2735-106">Перейдите в раздел **Аренда активов \> Настройка \> Рабочий процесс аренды**.</span><span class="sxs-lookup"><span data-stu-id="f2735-106">Go to **Asset leasing \> Setup \> Lease workflow**.</span></span>
2. <span data-ttu-id="f2735-107">На странице **Рабочий процесс аренды** нажмите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f2735-107">On the **Lease workflow** page, select **New**.</span></span>
3. <span data-ttu-id="f2735-108">В диалоговом окне, которое отображается, в разделе **Тип рабочего процесса** выберите ссылку **Рабочий процесс аренды**.</span><span class="sxs-lookup"><span data-stu-id="f2735-108">In the dialog box that appears, under **Workflow type**, select the **Lease workflow** link.</span></span>

    <span data-ttu-id="f2735-109">Приложение открывается.</span><span class="sxs-lookup"><span data-stu-id="f2735-109">The application is opened.</span></span> <span data-ttu-id="f2735-110">После его выполнения выполните вход в Azure Active Directory (Azure AD) для перенаправления в приложение рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="f2735-110">After it runs, sign in to Azure Active Directory (Azure AD) to be redirected to the workflow application.</span></span>

4. <span data-ttu-id="f2735-111">Перетащите элемент **Утверждение рабочего процесса аренды** в рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="f2735-111">Drag the **Lease workflow approval** element onto the workflow.</span></span>
5. <span data-ttu-id="f2735-112">Соедините один узел от **Начало** до **Утверждение рабочего процесса аренды**.</span><span class="sxs-lookup"><span data-stu-id="f2735-112">Connect one node from **Start** to **Lease workflow approval**.</span></span> <span data-ttu-id="f2735-113">Затем соедините **Утверждение рабочего процесса для аренды** с **Готово**.</span><span class="sxs-lookup"><span data-stu-id="f2735-113">Then connect **Lease workflow approval** to **End**.</span></span>
6. <span data-ttu-id="f2735-114">Дважды щелкните **Утверждение рабочего процесса аренды**.</span><span class="sxs-lookup"><span data-stu-id="f2735-114">Double-click **Lease workflow approval**.</span></span>
7. <span data-ttu-id="f2735-115">Выберите **Свойства**, а затем в разделе **Основные параметры** введите имя рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="f2735-115">Select **Properties**, and then, under **Basic settings**, enter a name for the workflow.</span></span>

    <span data-ttu-id="f2735-116">На этой странице можно также настроить дополнительные параметры для рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="f2735-116">On this page, you can also set more parameters for the workflow.</span></span> <span data-ttu-id="f2735-117">Если вы включили **Автоматические действия**, система автоматически выполнит конкретное действие.</span><span class="sxs-lookup"><span data-stu-id="f2735-117">If you've turned on **Automatic actions**, the system will automatically take a specific action.</span></span> <span data-ttu-id="f2735-118">Уведомления могут быть отправлены, если они указаны на вкладке **Уведомления**. На вкладке **Дополнительные параметры** можно указать окончательного утверждающего, установить предельное время и назначить определенные действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="f2735-118">Notifications can be sent if they are specified on the **Notifications** tab. On the **Advanced settings** tab, you can specify a final approver, set a time limit, and designate specific actions that must be completed.</span></span>

8. <span data-ttu-id="f2735-119">После завершения настройки параметров рабочего процесса выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="f2735-119">When you've finished setting the workflow parameters, select **Close**.</span></span>
9. <span data-ttu-id="f2735-120">Выберите **Шаг 1**, а затем выберите **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="f2735-120">Select **Step 1**, and then select **Properties**.</span></span>
10. <span data-ttu-id="f2735-121">В разделе **Основные параметры** введите имя шага, создайте строку темы для утверждения и укажите инструкции для утверждения.</span><span class="sxs-lookup"><span data-stu-id="f2735-121">Under **Basic settings**, enter a name for the step, create a subject line for the approval, and specify instructions for the approval.</span></span>
11. <span data-ttu-id="f2735-122">На странице **Назначение** выберите тип назначения.</span><span class="sxs-lookup"><span data-stu-id="f2735-122">On the **Assignment** page, select the assignment type.</span></span>
12. <span data-ttu-id="f2735-123">Чтобы назначить определенных пользователей для утверждения, выберите **Пользователь**, выберите пользователей, которые утверждают аренды, а затем выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="f2735-123">To assign specific users to the approval, select **User**, select the users who approve leases, and then select **Close**.</span></span>
13. <span data-ttu-id="f2735-124">Выберите **Сохранить и закрыть**, чтобы создать рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="f2735-124">Select **Save and close** to create the workflow.</span></span> <span data-ttu-id="f2735-125">Затем, когда появится запрос, выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f2735-125">Then, when you're prompted, select **OK**.</span></span>
14. <span data-ttu-id="f2735-126">На странице **Создать рабочий процесс** выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="f2735-126">On the **Create workflow** page, select **Close**.</span></span>
14. <span data-ttu-id="f2735-127">Выберите новый рабочий процесс, затем выберите **Версии**.</span><span class="sxs-lookup"><span data-stu-id="f2735-127">Select the new workflow, and then select **Versions**.</span></span> <span data-ttu-id="f2735-128">Затем выберите **Активировать**, чтобы убедиться, что рабочий процесс активен.</span><span class="sxs-lookup"><span data-stu-id="f2735-128">Then select **Make active** to ensure that the workflow is active.</span></span>
15. <span data-ttu-id="f2735-129">Выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="f2735-129">Select **Close**.</span></span> <span data-ttu-id="f2735-130">Появится новая активная версия.</span><span class="sxs-lookup"><span data-stu-id="f2735-130">The new active version appears.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
