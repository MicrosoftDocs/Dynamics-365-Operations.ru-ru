---
title: Устранение неполадок при начальной настройке
description: В этом разделе содержатся сведения об устранении неполадок, которые могут возникнуть в процессе начальной настройки интеграции двойной записи между приложениями Finance and Operations и Common Data Service.
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
ms.openlocfilehash: e20c9c5e1250c8e65b5642a7c45d7ae859315697
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172676"
---
# <a name="troubleshoot-issues-during-initial-setup"></a><span data-ttu-id="8d024-103">Устранение неполадок при начальной настройке</span><span class="sxs-lookup"><span data-stu-id="8d024-103">Troubleshoot issues during initial setup</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="8d024-104">Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8d024-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="8d024-105">Конкретно, в этом разделе содержатся сведения об устранении неполадок, которые могут возникнуть в процессе начальной настройки интеграции двойной записи.</span><span class="sxs-lookup"><span data-stu-id="8d024-105">Specifically, it provides information that can help you fix issues that might occur during the initial setup of dual-write integration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d024-106">Для некоторых вопросов, связанных с этим разделом, может потребоваться роль системного администратора или учетные данные администратора клиента Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="8d024-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="8d024-107">В разделе для каждого выпуска объясняется, требуются ли конкретная роль или учетные данные.</span><span class="sxs-lookup"><span data-stu-id="8d024-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-link-a-finance-and-operations-app-to-common-data-service"></a><span data-ttu-id="8d024-108">Невозможно связать приложение Finance and Operations с Common Data Service</span><span class="sxs-lookup"><span data-stu-id="8d024-108">You can't link a Finance and Operations app to Common Data Service</span></span>

<span data-ttu-id="8d024-109">**Необходимые учетные данные для настройки двойной записи:** администратор клиента Azure AD</span><span class="sxs-lookup"><span data-stu-id="8d024-109">**Required credentials to set up dual-write:** Azure AD tenant admin</span></span>

<span data-ttu-id="8d024-110">Ошибки на странице **Настройка ссылки на Common Data Service** обычно вызываются проблемами с неполной настройкой или разрешениями.</span><span class="sxs-lookup"><span data-stu-id="8d024-110">Errors on the **Setup link to Common Data Service** page are usually caused by incomplete setup or permissions issues.</span></span> <span data-ttu-id="8d024-111">Убедитесь, что вся проверка работоспособности пройдена на странице **Настройка ссылки на Common Data Service**, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="8d024-111">Make sure that the whole health check passes on the **Setup link to Common Data Service** page, as shown in the following illustration.</span></span> <span data-ttu-id="8d024-112">Связывание двойной записи возможно только после полной проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="8d024-112">You can't link dual-write unless the whole health check passes.</span></span>

![Успешная проверка работоспособности](media/health_check.png)

<span data-ttu-id="8d024-114">Необходимы учетные данные администратора клиента Azure AD, чтобы можно было связать среды Finance and Operations и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8d024-114">You must have Azure AD tenant admin credentials to link the Finance and Operations and Common Data Service environments.</span></span> <span data-ttu-id="8d024-115">После связывания сред пользователи могут войти в систему, используя учетные данные своих учетных записей, и обновить существующее сопоставление объектов.</span><span class="sxs-lookup"><span data-stu-id="8d024-115">After you link the environments, users can sign in by using their account credentials and update an existing entity map.</span></span>

## <a name="error-when-you-open-the-link-to-common-data-service-page"></a><span data-ttu-id="8d024-116">Ошибка при открытии ссылки на страницу Common Data Service</span><span class="sxs-lookup"><span data-stu-id="8d024-116">Error when you open the Link to Common Data Service page</span></span>

<span data-ttu-id="8d024-117">**Необходимые учетные данные для устранения проблемы:** администратор клиента Azure AD</span><span class="sxs-lookup"><span data-stu-id="8d024-117">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="8d024-118">При открытии страницы **Связать с Common Data Service** в приложении Finance and Operations может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="8d024-118">You might receive the following error message when you open the **Link to Common Data Service** page in a Finance and Operations app:</span></span>

<span data-ttu-id="8d024-119">*Код статуса отклика не указывает на успешное выполнение: 404 (Не найден).*</span><span class="sxs-lookup"><span data-stu-id="8d024-119">*Response status code does not indicate success: 404 (Not Found).*</span></span>

<span data-ttu-id="8d024-120">Эта ошибка возникает, когда шаг разрешения не был завершен.</span><span class="sxs-lookup"><span data-stu-id="8d024-120">This error occurs when the consent step hasn't been completed.</span></span> <span data-ttu-id="8d024-121">Для проверки того, был ли выполнен шаг разрешения, войдите на portal.Azure.com с помощью учетной записи администратора клиента Azure AD и проверьте, появляется ли приложение независимого разработчика с идентификатором **33976c19-1db5-4c02-810e-c243db79efde** в списке Azure AD **Корпоративные приложения**.</span><span class="sxs-lookup"><span data-stu-id="8d024-121">To validate whether the consent step has been completed, sign in to portal.Azure.com by using the Azure AD tenant admin account, and see whether the third-party app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** appears in the Azure AD **Enterprise applications** list.</span></span> <span data-ttu-id="8d024-122">Если нет, необходимо предоставить согласие приложению.</span><span class="sxs-lookup"><span data-stu-id="8d024-122">If it doesn't, you must provide app consent.</span></span>

<span data-ttu-id="8d024-123">Чтобы предоставить согласие приложению, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8d024-123">To provide app consent, follow these steps.</span></span>

1. <span data-ttu-id="8d024-124">Откройте следующий URL-адрес, используя учетные данные администратора.</span><span class="sxs-lookup"><span data-stu-id="8d024-124">Open the following URL by using your admin credentials.</span></span> <span data-ttu-id="8d024-125">Вам должно быть предложено предоставить разрешение.</span><span class="sxs-lookup"><span data-stu-id="8d024-125">You should be prompted for consent.</span></span>

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. <span data-ttu-id="8d024-126">Выберите **Принять**, чтобы указать, что вы предоставляете согласие на установку приложения с идентификатором **33976c19-1db5-4c02-810e-c243db79efde** в вашем клиенте.</span><span class="sxs-lookup"><span data-stu-id="8d024-126">Select **Accept** to indicate that you're giving your consent to install the app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** in your tenant.</span></span>

    > [!TIP]
    > <span data-ttu-id="8d024-127">Это приложение необходимо для связывания Common Data Service и приложений Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8d024-127">This app is required to link Common Data Service and Finance and Operations apps.</span></span> <span data-ttu-id="8d024-128">При возникновении проблем с этим шагом откройте браузер в режиме "Инкогнито" (в Google Chrome) или в режиме InPrivate (в Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="8d024-128">If you have trouble with this step, open your browser in incognito mode (in Google Chrome) or InPrivate mode (in Microsoft Edge).</span></span>

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a><span data-ttu-id="8d024-129">Проверка правильности настройки данных компании и групп двойной записи во время связывания</span><span class="sxs-lookup"><span data-stu-id="8d024-129">Verify that company data and dual-write teams are set up correctly during linking</span></span>

<span data-ttu-id="8d024-130">Чтобы обеспечить правильную работу двойной записи, в среде Common Data Service создаются компании, выбранные во время настройки.</span><span class="sxs-lookup"><span data-stu-id="8d024-130">To ensure that dual-write works correctly, the companies that you select during configuration are created in the Common Data Service environment.</span></span> <span data-ttu-id="8d024-131">По умолчанию эти компании доступны только для чтения, и свойство **IsDualWriteEnable** имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="8d024-131">By default, these companies are read-only, and the **IsDualWriteEnable** property is set to **True**.</span></span> <span data-ttu-id="8d024-132">Кроме того, создаются ответственный подразделения и группы по умолчанию, которые включают название компании.</span><span class="sxs-lookup"><span data-stu-id="8d024-132">In addition, the default owning business unit owner and team are created and include the company name.</span></span> <span data-ttu-id="8d024-133">Перед включением карт убедитесь, что указан владелец группы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8d024-133">Before you enable the maps, verify that the default team owner is specified.</span></span> <span data-ttu-id="8d024-134">Чтобы найти объект **Компании (CDM\_Company)**, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8d024-134">To find the **Companies (CDM\_Company)** entity, follow these steps.</span></span>

1. <span data-ttu-id="8d024-135">В приложении на основе модели в Dynamics 365 выберите фильтр в верхнем правом углу.</span><span class="sxs-lookup"><span data-stu-id="8d024-135">In the model-driven app in Dynamics 365, select the filter in the upper-right corner.</span></span>
2. <span data-ttu-id="8d024-136">В раскрывающемся списке выберите **Компания**.</span><span class="sxs-lookup"><span data-stu-id="8d024-136">In the drop-down list, select **Company**.</span></span>
3. <span data-ttu-id="8d024-137">Выберите **Выполнить**, чтобы увидеть результаты.</span><span class="sxs-lookup"><span data-stu-id="8d024-137">Select **Run** to see the results.</span></span>
4. <span data-ttu-id="8d024-138">Выбор компанию, которая была связана при настройке двойной записи.</span><span class="sxs-lookup"><span data-stu-id="8d024-138">Select the company that was linked when you configured dual-write.</span></span>
5. <span data-ttu-id="8d024-139">Убедитесь, что поле **Ответственная рабочая группа по умолчанию** имеет значение.</span><span class="sxs-lookup"><span data-stu-id="8d024-139">Verify that the **Default owning team** field has a value.</span></span> <span data-ttu-id="8d024-140">На следующем рисунке в поле **Ответственная рабочая группа по умолчанию** установлено значение **Двойная запись USMF**.</span><span class="sxs-lookup"><span data-stu-id="8d024-140">In the following illustration, the **Default owning team** field is set to **USMF Dual Write**.</span></span>

    ![Проверка ответственной рабочей группы по умолчанию](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-entities-or-companies-that-can-be-linked-for-dual-write"></a><span data-ttu-id="8d024-142">Определение предельного числа юридических лиц или компаний, которые могут быть связаны с двойной записью</span><span class="sxs-lookup"><span data-stu-id="8d024-142">Find the limit on the number of legal entities or companies that can be linked for dual-write</span></span>

<span data-ttu-id="8d024-143">При попытке включения сопоставлений может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="8d024-143">You might receive the following error message when you try to enable maps:</span></span>

<span data-ttu-id="8d024-144">*Ошибка двойной записи - сбой регистрации подключаемого модуля: \[(Не удается получить карту разделов для проекта DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Ошибка Превышено максимальное число разделов, допустимое для сопоставления DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], Возникла одна или несколько ошибок.*</span><span class="sxs-lookup"><span data-stu-id="8d024-144">*Dual write failure - Plugin registration failed: \[(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], One or more errors occurred.*</span></span>

<span data-ttu-id="8d024-145">Текущий предел при связывании сред составляет примерно 40 юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="8d024-145">The current limit when you link the environments is approximately 40 legal entities.</span></span> <span data-ttu-id="8d024-146">Эта ошибка возникает, если при попытке включить сопоставления между этими средами связано более 40 юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="8d024-146">This error occurs if you try to enable maps, and more than 40 legal entities are linked between the environments.</span></span>
