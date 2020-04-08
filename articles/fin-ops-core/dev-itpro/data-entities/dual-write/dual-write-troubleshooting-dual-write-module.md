---
title: Устранение неполадок в работе модуля двойной записи в приложениях Finance and Operations
description: В этом разделе содержатся сведения об устранении неполадок, связанных с модулем двойной записи в приложениях Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172768"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="6bce2-103">Устранение неполадок в работе модуля двойной записи в приложениях Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6bce2-103">Troubleshoot issues with the Dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="6bce2-104">Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6bce2-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="6bce2-105">А именно, в нем содержатся сведения об устранении неполадок, связанных с модулем **Двойная запись** в приложениях Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6bce2-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6bce2-106">Для некоторых вопросов, связанных с этим разделом, может потребоваться роль системного администратора или учетные данные администратора клиента Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="6bce2-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="6bce2-107">В разделе для каждого выпуска объясняется, требуются ли конкретная роль или учетные данные.</span><span class="sxs-lookup"><span data-stu-id="6bce2-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="6bce2-108">Вы не можете загрузить модуль двойной записи в приложение Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6bce2-108">You can't load the Dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="6bce2-109">Если не удается открыть страницу **Двойная запись** путем выбора плитки **Двойная запись** в рабочей области **Управление данными**, возможно, служба интеграции данных не работает.</span><span class="sxs-lookup"><span data-stu-id="6bce2-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="6bce2-110">Создайте запрос в службу поддержки для запроса перезапуска службы интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="6bce2-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a><span data-ttu-id="6bce2-111">Ошибка при попытке создания нового сопоставления объекта</span><span class="sxs-lookup"><span data-stu-id="6bce2-111">Error when you try to create a new entity mapping</span></span>

<span data-ttu-id="6bce2-112">**Необходимые учетные данные для устранения проблемы:** администратор клиента Azure AD</span><span class="sxs-lookup"><span data-stu-id="6bce2-112">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="6bce2-113">При попытке настроить новый объект для двойной записи может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="6bce2-113">You might receive the following error message when you try to configure a new entity for dual-write:</span></span>

<span data-ttu-id="6bce2-114">*Код статуса отклика не указывает на успешное выполнение: 401 (Unauthorized).*</span><span class="sxs-lookup"><span data-stu-id="6bce2-114">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>

<span data-ttu-id="6bce2-115">Эта ошибка происходит из-за того, что только администратор клиента Azure AD может добавить новое сопоставление объекта.</span><span class="sxs-lookup"><span data-stu-id="6bce2-115">This error occurs because only an Azure AD tenant admin can add a new entity mapping.</span></span>

<span data-ttu-id="6bce2-116">Чтобы исправить ошибку, войдите в приложение Finance and Operations в качестве администратора клиента Azure AD.</span><span class="sxs-lookup"><span data-stu-id="6bce2-116">To fix the issue, sign in to the Finance and Operations app as an Azure AD admin tenant.</span></span> <span data-ttu-id="6bce2-117">Также необходимо перейти в web.PowerApps.com и повторно подтвердить подключение.</span><span class="sxs-lookup"><span data-stu-id="6bce2-117">You must also go to web.PowerApps.com and revalidate your connection.</span></span>

## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="6bce2-118">Ошибка при открытии интерфейса пользователя двойной записи</span><span class="sxs-lookup"><span data-stu-id="6bce2-118">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="6bce2-119">При попытке доступа к двойной записи из рабочей области **Управление данными** может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="6bce2-119">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="6bce2-120">*login.microsoftonline.com отклонил попытку подключения.*</span><span class="sxs-lookup"><span data-stu-id="6bce2-120">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="6bce2-121">Чтобы устранить эту проблему, выполните вход, используя окно InPrivate в Microsoft Edge, окно инкогнито окно в Chromium или окно инкогнито в Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="6bce2-121">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="6bce2-122">Кроме того, необходимо разблокировать или удалить сторонние файлы cookie.</span><span class="sxs-lookup"><span data-stu-id="6bce2-122">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="6bce2-123">Ошибка при связи среды для двойной записи или добавлении нового сопоставления объекта</span><span class="sxs-lookup"><span data-stu-id="6bce2-123">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="6bce2-124">**Необходимые учетные данные для устранения проблемы:** администратор клиента Azure AD</span><span class="sxs-lookup"><span data-stu-id="6bce2-124">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="6bce2-125">При связывании или создании карт может возникнуть следующая ошибка:</span><span class="sxs-lookup"><span data-stu-id="6bce2-125">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="6bce2-126">*Код состояния отклика не указывает на успешное выполнение: 403 (tokenexchange).<br> Код сеанса: \<код вашего сеанса\><br> Код корневой операции: \<код вашей корневой операции\>*</span><span class="sxs-lookup"><span data-stu-id="6bce2-126">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="6bce2-127">Эта ошибка может возникнуть, если у вас нет достаточных прав для связывания двойной записи для создания карт.</span><span class="sxs-lookup"><span data-stu-id="6bce2-127">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="6bce2-128">Вы должны использовать учетную запись администратора клиента Azure AD, чтобы связать среды и добавить новые сопоставления объектов.</span><span class="sxs-lookup"><span data-stu-id="6bce2-128">You must use an Azure AD tenant admin account to link environments and add new entity mappings.</span></span> <span data-ttu-id="6bce2-129">Однако после настройки можно использовать учетную запись, не являющуюся учетной записью администратора, для отслеживания состояния и изменения сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="6bce2-129">However, after setup, you can use a non-admin account to monitor status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="6bce2-130">Ошибка при остановке сопоставления объекта</span><span class="sxs-lookup"><span data-stu-id="6bce2-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="6bce2-131">При попытке остановки сопоставлений объектов может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="6bce2-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="6bce2-132">*\[Запрещено\], \[{"статус":403,"источник":"","сообщение":"Ошибка от обмена токенами: пользователю не разрешен доступ к подключению dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], Удаленный сервер вернул ошибку: (403) Запрещено.*</span><span class="sxs-lookup"><span data-stu-id="6bce2-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="6bce2-133">Эта ошибка возникает, когда связанная среда Common Data Service недоступна.</span><span class="sxs-lookup"><span data-stu-id="6bce2-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="6bce2-134">Чтобы устранить эту проблему, создайте заявку в рабочую группу интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="6bce2-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="6bce2-135">Приложите трассировку сети, чтобы рабочая группа интеграции данных могла отметить карты как **Не выполняются** в серверной системе.</span><span class="sxs-lookup"><span data-stu-id="6bce2-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>
