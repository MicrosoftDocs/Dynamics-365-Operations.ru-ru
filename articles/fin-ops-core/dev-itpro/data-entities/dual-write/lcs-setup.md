---
title: Настройка двойной записи из Lifecycle Services
description: В этой теме объясняется, как настроить подключение двойной записи из Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e51b4ef1e309e5f89dc82a3776b88c505dc6593d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748549"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="f97bc-103">Настройка двойной записи из Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="f97bc-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f97bc-104">В этой теме объясняется, как настроить подключение с двойной записью между новой средой Finance and Operations и новой средой Dataverse из Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f97bc-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Dataverse environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f97bc-105">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="f97bc-105">Prerequisites</span></span>

<span data-ttu-id="f97bc-106">Для настройки подключения с двойной записью необходимо иметь права администратора.</span><span class="sxs-lookup"><span data-stu-id="f97bc-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="f97bc-107">Вы должны иметь доступ к клиенту.</span><span class="sxs-lookup"><span data-stu-id="f97bc-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="f97bc-108">Вы должны быть администратором в обеих средах Finance and Operations и Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f97bc-108">You must be an admin in both Finance and Operations environments and Dataverse environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="f97bc-109">Настройка подключения двойной записи</span><span class="sxs-lookup"><span data-stu-id="f97bc-109">Set up a dual-write connection</span></span>

<span data-ttu-id="f97bc-110">Выполните эти шаги для настройки подключения двойной записи.</span><span class="sxs-lookup"><span data-stu-id="f97bc-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="f97bc-111">В LCS перейдите к своему проекту.</span><span class="sxs-lookup"><span data-stu-id="f97bc-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="f97bc-112">Выберите **Настройка** для развертывания новой среды.</span><span class="sxs-lookup"><span data-stu-id="f97bc-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="f97bc-113">Выберите версию.</span><span class="sxs-lookup"><span data-stu-id="f97bc-113">Select the version.</span></span> 
4. <span data-ttu-id="f97bc-114">Выберите топологию.</span><span class="sxs-lookup"><span data-stu-id="f97bc-114">Select the topology.</span></span> <span data-ttu-id="f97bc-115">Если доступна только одна топология, она выбирается автоматически.</span><span class="sxs-lookup"><span data-stu-id="f97bc-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="f97bc-116">Выполните первые шаги в мастере **Параметры развертывания**.</span><span class="sxs-lookup"><span data-stu-id="f97bc-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="f97bc-117">На вкладке **Dataverse** выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="f97bc-117">On the **Dataverse** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="f97bc-118">Если среда Dataverse уже подготовлена для клиента, его можно выбрать.</span><span class="sxs-lookup"><span data-stu-id="f97bc-118">If a Dataverse environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="f97bc-119">Установите для параметра **Настроить Dataverse** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="f97bc-119">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="f97bc-120">В столбце **Доступные среды** выберите среду, которую необходимо интегрировать с данными Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f97bc-120">In the **Available environments** column, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="f97bc-121">Список включает в себя все среды, для которых у вас имеются привилегии администратора.</span><span class="sxs-lookup"><span data-stu-id="f97bc-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="f97bc-122">Установите флажок **Принимаю**, чтобы указать, что вы принимаете условия.</span><span class="sxs-lookup"><span data-stu-id="f97bc-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Вкладка Dataverse, когда среда Dataverse уже подготовлена для клиента](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="f97bc-124">Если у клиента еще нет среды Dataverse, будет подготовлена новая среда.</span><span class="sxs-lookup"><span data-stu-id="f97bc-124">If your tenant doesn't already have a Dataverse environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="f97bc-125">Установите для параметра **Настроить Dataverse** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="f97bc-125">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="f97bc-126">Введите имя для среды Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f97bc-126">Enter a name for the Dataverse environment.</span></span>
        3. <span data-ttu-id="f97bc-127">Выберите регион, в котором требуется развернуть среду.</span><span class="sxs-lookup"><span data-stu-id="f97bc-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="f97bc-128">Выберите язык и валюту по умолчанию для среды.</span><span class="sxs-lookup"><span data-stu-id="f97bc-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="f97bc-129">Изменить язык и валюту позже нельзя.</span><span class="sxs-lookup"><span data-stu-id="f97bc-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="f97bc-130">Установите флажок **Принимаю**, чтобы указать, что вы принимаете условия.</span><span class="sxs-lookup"><span data-stu-id="f97bc-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Вкладка Dataverse, если у клиента еще нет среды Dataverse](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="f97bc-132">Выполните оставшиеся шаги в мастере **Параметры развертывания**.</span><span class="sxs-lookup"><span data-stu-id="f97bc-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="f97bc-133">После того как среда имеет статус **Развернуто**, откройте страницу сведений о среде.</span><span class="sxs-lookup"><span data-stu-id="f97bc-133">After the environment has a status of **Deployed**, open the environment details page.</span></span> <span data-ttu-id="f97bc-134">В разделе **Интеграция Power Platform** показаны имена среды Finance and Operations и среды Dataverse, которые связаны.</span><span class="sxs-lookup"><span data-stu-id="f97bc-134">The **Power Platform Integration** section shows the names of the Finance and Operations environment and the Dataverse environment that are linked.</span></span>

    ![Раздел интеграции Power Platform](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="f97bc-136">Администратор среды Finance and Operations должен войти в систему LCS и выбрать пункт **Связать с CDS для приложений**, чтобы завершить связь.</span><span class="sxs-lookup"><span data-stu-id="f97bc-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="f97bc-137">На странице сведений о среде отображаются контактные данные администратора.</span><span class="sxs-lookup"><span data-stu-id="f97bc-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="f97bc-138">После завершения установления связи статус обновляется до **Связывание среды успешно выполнено**.</span><span class="sxs-lookup"><span data-stu-id="f97bc-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="f97bc-139">Чтобы открыть рабочую область **Интеграция данных** в среде Finance and Operations и управлять доступными шаблонами, выберите **Связать с CDS для приложений**.</span><span class="sxs-lookup"><span data-stu-id="f97bc-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![Кнопка "Связать с CDS для приложений" в разделе интеграции Power Platform](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="f97bc-141">Невозможно удалить связь среды с помощью LCS.</span><span class="sxs-lookup"><span data-stu-id="f97bc-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="f97bc-142">Чтобы отменить связь среды, откройте рабочую область **Интеграция данных** в среде Finance and Operations, затем выберите **Удалить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="f97bc-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]