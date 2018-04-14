--- 
title: "Разрешение пользователям получать сообщения электронной почты, связанные с workflow-процессом"
description: "Систему можно настроить для отправки сообщений электронной почты пользователям при возникновении событий, связанных с workflow-процессами."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1062bbbfc5563a49cb0ba0b04bf99853f19e58ea
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="7efbd-103">Разрешение пользователям получать сообщения электронной почты, связанные с workflow-процессом</span><span class="sxs-lookup"><span data-stu-id="7efbd-103">Enable users to receive workflow-related email messages</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7efbd-104">Систему можно настроить для отправки сообщений электронной почты пользователям при возникновении событий, связанных с workflow-процессами.</span><span class="sxs-lookup"><span data-stu-id="7efbd-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="7efbd-105">Например, сообщения электронной почты можно отправлять пользователям, когда им назначаются документы для утверждения.</span><span class="sxs-lookup"><span data-stu-id="7efbd-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="7efbd-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="7efbd-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="7efbd-107">Перейдите в раздел "Администрирование системы" > "Пользователи" > "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="7efbd-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="7efbd-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="7efbd-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7efbd-109">Щелкните "Параметры пользователя".</span><span class="sxs-lookup"><span data-stu-id="7efbd-109">Click User options.</span></span>
4. <span data-ttu-id="7efbd-110">Щелкните вкладку "Workflow-процесс".</span><span class="sxs-lookup"><span data-stu-id="7efbd-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="7efbd-111">Убедитесь, что раздел "Уведомления" развернут.</span><span class="sxs-lookup"><span data-stu-id="7efbd-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="7efbd-112">В разделе "Уведомления" можно указать способ уведомления пользователя о событиях, связанных с workflow-процессами.</span><span class="sxs-lookup"><span data-stu-id="7efbd-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="7efbd-113">В поле "Тип уведомления workflow-процесса по строке" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="7efbd-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="7efbd-114">Сгруппированные — уведомления для номенклатур строки сгруппированы в одно сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="7efbd-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="7efbd-115">Индивидуальные — сообщение электронной почты отправляется для каждой номенклатуры строки.</span><span class="sxs-lookup"><span data-stu-id="7efbd-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="7efbd-116">Если требуется, чтобы пользователь получал уведомления в клиенте, установите флажок "Отправлять уведомления в электронной почте".</span><span class="sxs-lookup"><span data-stu-id="7efbd-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="7efbd-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="7efbd-117">Click Save.</span></span>
7. <span data-ttu-id="7efbd-118">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7efbd-118">Close the page.</span></span>


