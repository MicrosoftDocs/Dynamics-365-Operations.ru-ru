---
title: Разрешение пользователям получать сообщения электронной почты, связанные с workflow-процессом
description: Систему можно настроить для отправки сообщений электронной почты пользователям при возникновении событий, связанных с workflow-процессами.
author: jasongre
manager: AnnBe
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a81e01c36081ce7131ee65344f583755fa3bfd3
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564198"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="c6a0d-103">Разрешение пользователям получать сообщения электронной почты, связанные с workflow-процессом</span><span class="sxs-lookup"><span data-stu-id="c6a0d-103">Enable users to receive workflow-related email messages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c6a0d-104">Систему можно настроить для отправки сообщений электронной почты пользователям при возникновении событий, связанных с workflow-процессами.</span><span class="sxs-lookup"><span data-stu-id="c6a0d-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="c6a0d-105">Например, сообщения электронной почты можно отправлять пользователям, когда им назначаются документы для утверждения.</span><span class="sxs-lookup"><span data-stu-id="c6a0d-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="c6a0d-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="c6a0d-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="c6a0d-107">Перейдите в раздел **Область перехода > Модули > Администрирование системы > Пользователи > Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="c6a0d-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="c6a0d-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c6a0d-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c6a0d-109">В области **Панель операций** щелкните **Параметры пользователя**.</span><span class="sxs-lookup"><span data-stu-id="c6a0d-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="c6a0d-110">Перейдите на вкладку **Рабочий процесс**. Убедитесь, что раздел **Уведомления** развернут.</span><span class="sxs-lookup"><span data-stu-id="c6a0d-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="c6a0d-111">В разделе **Уведомления** можно указать способ уведомления пользователя о событиях, связанных с рабочими процессами.</span><span class="sxs-lookup"><span data-stu-id="c6a0d-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="c6a0d-112">В поле **Тип уведомления workflow-процесса по строке** выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="c6a0d-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="c6a0d-113">Сгруппированные — уведомления для номенклатур строки сгруппированы в одно сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="c6a0d-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="c6a0d-114">Индивидуальные — сообщение электронной почты отправляется для каждой номенклатуры строки.</span><span class="sxs-lookup"><span data-stu-id="c6a0d-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="c6a0d-115">Если требуется, чтобы пользователь получал уведомления в клиенте, установите флажок **Отправлять уведомления в электронной почте**.</span><span class="sxs-lookup"><span data-stu-id="c6a0d-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="c6a0d-116">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c6a0d-116">Click **Save**.</span></span>
7. <span data-ttu-id="c6a0d-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c6a0d-117">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="c6a0d-118">Шаблоны электронной почты бизнес-правил будут поступать из шаблонов электронной почты системы или шаблонов электронной почты организации в зависимости от того, является ли бизнес-правило системным (не зависящим от компании) или организационным (заданным компанией).</span><span class="sxs-lookup"><span data-stu-id="c6a0d-118">The workflow email templates will be sourced from either system email templates or organization email templates depending on whether the workflow is a system-level (not company specific) or organization-level (company specific) workflow.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]