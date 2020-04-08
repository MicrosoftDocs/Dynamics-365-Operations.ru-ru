---
title: Устранение неполадок при начальной синхронизации
description: В этом разделе содержатся сведения об устранении неполадок, которые могут возникнуть при начальной синхронизации.
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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172722"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="de122-103">Устранение неполадок при начальной синхронизации</span><span class="sxs-lookup"><span data-stu-id="de122-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="de122-104">Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="de122-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="de122-105">А именно, содержатся сведения об устранении неполадок, которые могут возникнуть при начальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="de122-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="de122-106">Для некоторых вопросов, связанных с этим разделом, может потребоваться роль системного администратора или учетные данные администратора клиента Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="de122-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="de122-107">В разделе для каждого выпуска объясняется, требуются ли конкретная роль или учетные данные.</span><span class="sxs-lookup"><span data-stu-id="de122-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="de122-108">Проверка наличия ошибок исходной синхронизации в приложении Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="de122-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="de122-109">После включения шаблонов сопоставления статус сопоставлений должно быть **Выполняется**.</span><span class="sxs-lookup"><span data-stu-id="de122-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="de122-110">Если статус **Не выполняется**, при первоначальной синхронизации произошли ошибки.</span><span class="sxs-lookup"><span data-stu-id="de122-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="de122-111">Для просмотра ошибок выберите вкладку **Сведения о начальной синхронизации** на странице **Двойная запись**.</span><span class="sxs-lookup"><span data-stu-id="de122-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Вкладка сведений о начальной синхронизации](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="de122-113">Выполнение начальной синхронизации невозможно: 400 Неправильный запрос</span><span class="sxs-lookup"><span data-stu-id="de122-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="de122-114">**Роль, требуемая для исправления ошибки:** системный администратор</span><span class="sxs-lookup"><span data-stu-id="de122-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="de122-115">При попытке запуска сопоставления и исходной синхронизации может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="de122-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="de122-116">*Удаленный сервер вернул ошибку: (400) Неправильный запрос.), при экспорте AX произошла ошибка*</span><span class="sxs-lookup"><span data-stu-id="de122-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="de122-117">Ниже приведен пример полного сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="de122-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="de122-118">Если эта ошибка происходит постоянно, и вы не можете выполнить начальную синхронизацию, выполните следующие действия для устранения проблемы.</span><span class="sxs-lookup"><span data-stu-id="de122-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="de122-119">Выполните вход в виртуальную машину для приложения Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="de122-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="de122-120">Откройте консоль управления Microsoft.</span><span class="sxs-lookup"><span data-stu-id="de122-120">Open Microsoft Management Console.</span></span> 
3. <span data-ttu-id="de122-121">В области **Службы** убедитесь, что запущена служба структуры импорта и экспорта данных Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="de122-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="de122-122">Перезапустите ее, если она была остановлена, так как она необходима для исходной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="de122-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="de122-123">Ошибка начальной синхронизации: 403 Запрещено</span><span class="sxs-lookup"><span data-stu-id="de122-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="de122-124">Во время начальной синхронизации может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="de122-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="de122-125">*(\[Запрещено\], Удаленный сервер вернул ошибку: (403) Запрещено.), при экспорте AX произошла ошибка*</span><span class="sxs-lookup"><span data-stu-id="de122-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="de122-126">Чтобы устранить проблему, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="de122-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="de122-127">Выполните вход в приложение Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="de122-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="de122-128">На странице **Приложения Azure Active Directory** удалите клиент **DtAppID** и добавьте его снова.</span><span class="sxs-lookup"><span data-stu-id="de122-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Список приложений Azure AD](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a><span data-ttu-id="de122-130">Ошибки ссылки на себя во время первоначальной синхронизации</span><span class="sxs-lookup"><span data-stu-id="de122-130">Self-reference failures during initial synchronization</span></span>

<span data-ttu-id="de122-131">Если какое-либо сопоставление имеет ссылки на себя, вы можете получить сообщение об ошибке, подобное следующему примеру:</span><span class="sxs-lookup"><span data-stu-id="de122-131">You might receive an error message that resembles the following example if any of your mappings have self-references:</span></span>

<span data-ttu-id="de122-132">*В Vendors V2 следующая ошибка: код записи: новая запись, ErrorMessage: Невозможно разрешить guid для поля: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Значение подстановки не найдено: CN-001. Попробуйте эти URL-адреса для проверки, существуют ли ссылочные данные: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span><span class="sxs-lookup"><span data-stu-id="de122-132">*On the Vendors V2, the following error: Record Id: new record, ErrorMessage: Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup value was not found: CN-001. Try this URL(s) to check if the reference data exists: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span></span>

<span data-ttu-id="de122-133">Этот тип ошибки происходит во время первоначальной синхронизации сопоставлений, которые содержат ссылки на себя.</span><span class="sxs-lookup"><span data-stu-id="de122-133">This type of error occurs during initial synchronization of mappings that have self-references.</span></span> <span data-ttu-id="de122-134">В предыдущем примере счет накладной в поле ссылается на объект поставщика.</span><span class="sxs-lookup"><span data-stu-id="de122-134">In the preceding example, the field invoice account references the vendor entity.</span></span>

<span data-ttu-id="de122-135">Чтобы устранить эту проблему, возможно, потребуется выполнить сопоставление два раза до успешного выполнения первоначальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="de122-135">To fix the issue, you might have to run the mapping two times before the initial synchronization is successful.</span></span>

