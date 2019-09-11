---
title: Разрешение пользователям получать сообщения электронной почты, связанные с workflow-процессом
description: Систему можно настроить для отправки сообщений электронной почты пользователям при возникновении событий, связанных с workflow-процессами.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e08f95ef6d263ee0f8c0a94b258c8a2795786bc
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916400"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="334df-103">Разрешение пользователям получать сообщения электронной почты, связанные с workflow-процессом</span><span class="sxs-lookup"><span data-stu-id="334df-103">Enable users to receive workflow-related email messages</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="334df-104">Систему можно настроить для отправки сообщений электронной почты пользователям при возникновении событий, связанных с workflow-процессами.</span><span class="sxs-lookup"><span data-stu-id="334df-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="334df-105">Например, сообщения электронной почты можно отправлять пользователям, когда им назначаются документы для утверждения.</span><span class="sxs-lookup"><span data-stu-id="334df-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="334df-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="334df-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="334df-107">Перейдите в раздел **Область перехода > Модули > Администрирование системы > Пользователи > Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="334df-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="334df-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="334df-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="334df-109">В области **Панель операций** щелкните **Параметры пользователя**.</span><span class="sxs-lookup"><span data-stu-id="334df-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="334df-110">Перейдите на вкладку **Рабочий процесс**. Убедитесь, что раздел **Уведомления** развернут.</span><span class="sxs-lookup"><span data-stu-id="334df-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="334df-111">В разделе **Уведомления** можно указать способ уведомления пользователя о событиях, связанных с рабочими процессами.</span><span class="sxs-lookup"><span data-stu-id="334df-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="334df-112">В поле **Тип уведомления workflow-процесса по строке** выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="334df-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="334df-113">Сгруппированные — уведомления для номенклатур строки сгруппированы в одно сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="334df-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="334df-114">Индивидуальные — сообщение электронной почты отправляется для каждой номенклатуры строки.</span><span class="sxs-lookup"><span data-stu-id="334df-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="334df-115">Если требуется, чтобы пользователь получал уведомления в клиенте, установите флажок **Отправлять уведомления в электронной почте**.</span><span class="sxs-lookup"><span data-stu-id="334df-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="334df-116">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="334df-116">Click **Save**.</span></span>
7. <span data-ttu-id="334df-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="334df-117">Close the page.</span></span>

