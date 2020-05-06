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
ms.openlocfilehash: 853791d5ffc1d92b9fbafa2acc13cd5543c38196
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275541"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="dfc5f-103">Устранение неполадок в работе модуля двойной записи в приложениях Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dfc5f-103">Troubleshoot issues with the dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dfc5f-104">Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="dfc5f-105">А именно, в нем содержатся сведения об устранении неполадок, связанных с модулем **Двойная запись** в приложениях Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dfc5f-106">Для некоторых вопросов, связанных с этим разделом, может потребоваться роль системного администратора или учетные данные администратора клиента Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="dfc5f-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="dfc5f-107">В разделе для каждого выпуска объясняется, требуются ли конкретная роль или учетные данные.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="dfc5f-108">Вы не можете загрузить модуль двойной записи в приложение Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dfc5f-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="dfc5f-109">Если не удается открыть страницу **Двойная запись** путем выбора плитки **Двойная запись** в рабочей области **Управление данными**, возможно, служба интеграции данных не работает.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="dfc5f-110">Создайте запрос в службу поддержки для запроса перезапуска службы интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-map"></a><span data-ttu-id="dfc5f-111">Ошибка при попытке создания нового сопоставления объекта</span><span class="sxs-lookup"><span data-stu-id="dfc5f-111">Error when you try to create a new entity map</span></span>

<span data-ttu-id="dfc5f-112">**Необходимые учетные данные для устранения проблемы:** тот же пользователь, который настроил двойную запись.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="dfc5f-113">При попытке настроить новый объект для двойной записи может появиться следующее сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-113">You might receive the following error message when you try to configure a new entity for dual-write.</span></span> <span data-ttu-id="dfc5f-114">Единственным пользователем, который может создать сопоставление, является пользователь, который настроил подключение с двойной записью.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="dfc5f-115">*Код статуса отклика не указывает на успешное выполнение: 401 (Unauthorized).*</span><span class="sxs-lookup"><span data-stu-id="dfc5f-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="dfc5f-116">Ошибка при открытии интерфейса пользователя двойной записи</span><span class="sxs-lookup"><span data-stu-id="dfc5f-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="dfc5f-117">При попытке доступа к двойной записи из рабочей области **Управление данными** может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="dfc5f-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="dfc5f-118">*login.microsoftonline.com отклонил попытку подключения.*</span><span class="sxs-lookup"><span data-stu-id="dfc5f-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="dfc5f-119">Чтобы устранить эту проблему, выполните вход, используя окно InPrivate в Microsoft Edge, окно инкогнито окно в Chromium или окно инкогнито в Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="dfc5f-120">Кроме того, необходимо разблокировать или удалить сторонние файлы cookie.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="dfc5f-121">Ошибка при связи среды для двойной записи или добавлении нового сопоставления объекта</span><span class="sxs-lookup"><span data-stu-id="dfc5f-121">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="dfc5f-122">**Необходимая роль для устранения проблемы:** системный администратор как в приложениях Finance and Operations, так и в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="dfc5f-123">При связывании или создании карт может возникнуть следующая ошибка:</span><span class="sxs-lookup"><span data-stu-id="dfc5f-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="dfc5f-124">*Код состояния отклика не указывает на успешное выполнение: 403 (tokenexchange).<br> Код сеанса: \<код вашего сеанса\><br> Код корневой операции: \<код вашей корневой операции\>*</span><span class="sxs-lookup"><span data-stu-id="dfc5f-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="dfc5f-125">Эта ошибка может возникнуть, если у вас нет достаточных прав для связывания двойной записи для создания карт.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="dfc5f-126">Эта ошибка может также возникать, если среда Common Data Service была сброшена без отключения двойной записи.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-126">This error can also occur if the Common Data Service environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="dfc5f-127">Любого пользователь с ролью системного администратора как в приложениях Finance and Operations, так и в Common Data Service, может связать эти среды.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-127">Any user with system administrator role in both Finance and Operations apps and Common Data Service can link the environments.</span></span> <span data-ttu-id="dfc5f-128">Новые сопоставления объектов может добавлять только пользователь, который настроил подключение с двойной записью.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-128">Only the user who setup the dual-write connection can add new entity maps.</span></span> <span data-ttu-id="dfc5f-129">После настройки любой пользователь с ролью системного администратора может отслеживать статус и изменять сопоставления.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="dfc5f-130">Ошибка при остановке сопоставления объекта</span><span class="sxs-lookup"><span data-stu-id="dfc5f-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="dfc5f-131">При попытке остановки сопоставлений объектов может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="dfc5f-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="dfc5f-132">*\[Запрещено\], \[{"статус":403,"источник":"","сообщение":"Ошибка от обмена токенами: пользователю не разрешен доступ к подключению dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], Удаленный сервер вернул ошибку: (403) Запрещено.*</span><span class="sxs-lookup"><span data-stu-id="dfc5f-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="dfc5f-133">Эта ошибка возникает, когда связанная среда Common Data Service недоступна.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="dfc5f-134">Чтобы устранить эту проблему, создайте заявку в рабочую группу интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="dfc5f-135">Приложите трассировку сети, чтобы рабочая группа интеграции данных могла отметить карты как **Не выполняются** в серверной системе.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-an-entity-mapping"></a><span data-ttu-id="dfc5f-136">Ошибка при попытке запуска сопоставления объектов</span><span class="sxs-lookup"><span data-stu-id="dfc5f-136">Error while trying to start an entity mapping</span></span>

<span data-ttu-id="dfc5f-137">При попытке установить это состояние сопоставления на **Выполняется** может появиться сообщение об ошибке, подобное следующему:</span><span class="sxs-lookup"><span data-stu-id="dfc5f-137">You might receive an error like the following when you try to set that state of a mapping to **Running**:</span></span>

<span data-ttu-id="dfc5f-138">*Не удалось выполнить начальную синхронизацию данных. Ошибка: сбой двойной записи — не удалось зарегистрировать подключаемый модуль: невозможно построить метаданные поиска двойной записи. Ссылка на объект ошибке не установлена на экземпляр объекта.*</span><span class="sxs-lookup"><span data-stu-id="dfc5f-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="dfc5f-139">Исправление для этой ошибки зависит от причины ошибки:</span><span class="sxs-lookup"><span data-stu-id="dfc5f-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="dfc5f-140">Если сопоставление имеет зависимые сопоставления, убедитесь, что разрешены зависимые сопоставления для этого сопоставления объектов.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this entity mapping.</span></span>
+ <span data-ttu-id="dfc5f-141">Возможно, в сопоставлении отсутствуют поля источника или назначения.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-141">The mapping might be missing source or destination fields.</span></span> <span data-ttu-id="dfc5f-142">Если поле в приложении Finance and Operations отсутствует, следуйте указаниям в разделе [Отсутствующие поля объекта в сопоставлениях](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span><span class="sxs-lookup"><span data-stu-id="dfc5f-142">If a field in the Finance and Operations app is missing, then follow the steps in the section [Missing entity fields issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span></span> <span data-ttu-id="dfc5f-143">Если отсутствует поле в Common Data Service, нажмите кнопку **Обновить объекты** на сопоставлении, чтобы эти поля автоматически вводились в сопоставление.</span><span class="sxs-lookup"><span data-stu-id="dfc5f-143">If a field in Common Data Service is missing, then click **Refresh entities** button on the mapping so that the fields are automatically populated back into the mapping.</span></span>
