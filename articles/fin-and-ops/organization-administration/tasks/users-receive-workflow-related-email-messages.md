---
title: Разрешение пользователям получать сообщения электронной почты, связанные с workflow-процессом
description: Систему можно настроить для отправки сообщений электронной почты пользователям при возникновении событий, связанных с workflow-процессами.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 6800d02878123388611d35760123d0215e9d539f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "344601"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="d7225-103">Разрешение пользователям получать сообщения электронной почты, связанные с workflow-процессом</span><span class="sxs-lookup"><span data-stu-id="d7225-103">Enable users to receive workflow-related email messages</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d7225-104">Систему можно настроить для отправки сообщений электронной почты пользователям при возникновении событий, связанных с workflow-процессами.</span><span class="sxs-lookup"><span data-stu-id="d7225-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="d7225-105">Например, сообщения электронной почты можно отправлять пользователям, когда им назначаются документы для утверждения.</span><span class="sxs-lookup"><span data-stu-id="d7225-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="d7225-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="d7225-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="d7225-107">Перейдите в раздел "Администрирование системы" > "Пользователи" > "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="d7225-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="d7225-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="d7225-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d7225-109">Щелкните "Параметры пользователя".</span><span class="sxs-lookup"><span data-stu-id="d7225-109">Click User options.</span></span>
4. <span data-ttu-id="d7225-110">Щелкните вкладку "Workflow-процесс".</span><span class="sxs-lookup"><span data-stu-id="d7225-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="d7225-111">Убедитесь, что раздел "Уведомления" развернут.</span><span class="sxs-lookup"><span data-stu-id="d7225-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="d7225-112">В разделе "Уведомления" можно указать способ уведомления пользователя о событиях, связанных с workflow-процессами.</span><span class="sxs-lookup"><span data-stu-id="d7225-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="d7225-113">В поле "Тип уведомления workflow-процесса по строке" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="d7225-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="d7225-114">Сгруппированные — уведомления для номенклатур строки сгруппированы в одно сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d7225-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="d7225-115">Индивидуальные — сообщение электронной почты отправляется для каждой номенклатуры строки.</span><span class="sxs-lookup"><span data-stu-id="d7225-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="d7225-116">Если требуется, чтобы пользователь получал уведомления в клиенте, установите флажок "Отправлять уведомления в электронной почте".</span><span class="sxs-lookup"><span data-stu-id="d7225-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="d7225-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d7225-117">Click Save.</span></span>
7. <span data-ttu-id="d7225-118">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d7225-118">Close the page.</span></span>

