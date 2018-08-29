--- 
title: "Настройка системы для отправки пользователям сообщений электронной почты, связанных с workflow-процессом"
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
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 04d90c9ded1ba7fb1ceac4ff1d54f54f6c43f9e9
ms.contentlocale: ru-ru
ms.lasthandoff: 08/09/2018

---
# <a name="configure-the-system-to-send-workflow-related-email-to-users"></a><span data-ttu-id="6344e-103">Настройка системы для отправки пользователям сообщений электронной почты, связанных с workflow-процессом</span><span class="sxs-lookup"><span data-stu-id="6344e-103">Configure the system to send workflow-related email to users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6344e-104">Систему можно настроить для отправки сообщений электронной почты пользователям при возникновении событий, связанных с workflow-процессами.</span><span class="sxs-lookup"><span data-stu-id="6344e-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="6344e-105">Например, сообщения электронной почты можно отправлять пользователям, когда им назначаются документы для утверждения.</span><span class="sxs-lookup"><span data-stu-id="6344e-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="6344e-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="6344e-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="6344e-107">Перейдите в раздел "Администрирование системы" > "Пользователи" > "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="6344e-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="6344e-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="6344e-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="6344e-109">Щелкните "Параметры пользователя".</span><span class="sxs-lookup"><span data-stu-id="6344e-109">Click User options.</span></span>
4. <span data-ttu-id="6344e-110">Щелкните вкладку "Workflow-процесс".</span><span class="sxs-lookup"><span data-stu-id="6344e-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="6344e-111">Убедитесь, что раздел "Уведомления" развернут.</span><span class="sxs-lookup"><span data-stu-id="6344e-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="6344e-112">В разделе "Уведомления" можно указать способ уведомления пользователя о событиях, связанных с workflow-процессами.</span><span class="sxs-lookup"><span data-stu-id="6344e-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="6344e-113">В поле "Тип уведомления workflow-процесса по строке" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="6344e-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="6344e-114">Сгруппированные — уведомления для номенклатур строки сгруппированы в одно сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6344e-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="6344e-115">Индивидуальные — сообщение электронной почты отправляется для каждой номенклатуры строки.</span><span class="sxs-lookup"><span data-stu-id="6344e-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="6344e-116">Если требуется, чтобы пользователь получал уведомления в клиенте, установите флажок "Отправлять уведомления в электронной почте".</span><span class="sxs-lookup"><span data-stu-id="6344e-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="6344e-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6344e-117">Click Save.</span></span>
7. <span data-ttu-id="6344e-118">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6344e-118">Close the page.</span></span>


