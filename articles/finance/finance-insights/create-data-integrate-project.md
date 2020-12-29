---
title: Создание проекта средства интеграции данных (предварительная версия)
description: В этой теме объясняется, как создать проект интегратора данных.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: fb17d5e82709a34ff088774d9e9034adb714b58c
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646261"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="512f9-103">Создание проекта средства интеграции данных (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="512f9-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="512f9-104">В этой теме объясняется, как создать проект интегратора данных.</span><span class="sxs-lookup"><span data-stu-id="512f9-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="512f9-105">Войдите в Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="512f9-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="512f9-106">Перейдите к пункту **Рабочие области \> Управление данными** и выберите **Сущности данных**.</span><span class="sxs-lookup"><span data-stu-id="512f9-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="512f9-107">Прежде чем перейти к следующему шагу, подождите, пока все сущности данных не будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="512f9-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="512f9-108">Откройте [портал Power Apps](https://make.powerapps.com/) и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="512f9-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="512f9-109">Выберите подходящую среду.</span><span class="sxs-lookup"><span data-stu-id="512f9-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="512f9-110">В левой области переходов выберите **Данные \> Подключения**.</span><span class="sxs-lookup"><span data-stu-id="512f9-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="512f9-111">Подключитесь к соответствующим экземплярам следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="512f9-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="512f9-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="512f9-112">Dynamics 365</span></span>
        - <span data-ttu-id="512f9-113">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="512f9-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="512f9-114">Откройте [среды Power Apps](https://admin.powerapps.com/environments) и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="512f9-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="512f9-115">Выберите **Интегратор данных**.</span><span class="sxs-lookup"><span data-stu-id="512f9-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="512f9-116">Выберите **Наборы подключений**.</span><span class="sxs-lookup"><span data-stu-id="512f9-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="512f9-117">Выберите **Создать набор подключений**.</span><span class="sxs-lookup"><span data-stu-id="512f9-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="512f9-118">Введите имя подключения.</span><span class="sxs-lookup"><span data-stu-id="512f9-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="512f9-119">Выберите подходящие подключения для следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="512f9-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="512f9-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="512f9-120">Dynamics 365</span></span>
        - <span data-ttu-id="512f9-121">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="512f9-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="512f9-122">Выберите соответствующее сопоставление организации.</span><span class="sxs-lookup"><span data-stu-id="512f9-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="512f9-123">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="512f9-123">Select **Create**.</span></span>

5. <span data-ttu-id="512f9-124">Откройте [среды Power Apps](https://admin.powerapps.com/environments) и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="512f9-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="512f9-125">Создайте проекты интеграции данных для следующих шаблонов, используя только что созданный набор соединений:</span><span class="sxs-lookup"><span data-stu-id="512f9-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="512f9-126">Результаты анализа платежей клиентов (из CDS в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="512f9-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="512f9-127">Результаты временных рядов потоков денежных средств (из CDS в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="512f9-127">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="512f9-128">Результаты временных рядов бюджетов (из CDS в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="512f9-128">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="512f9-129">Задайте соответствующее планирование для каждого проекта.</span><span class="sxs-lookup"><span data-stu-id="512f9-129">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="512f9-130">Если вы не видите требуется сущности в CDS, перейдите в раздел **Кредит и сбор задолженностей > Настройка > Финансовый анализ > Параметры финансового анализа**, активируйте функцию прогнозирования платежей клиентов и нажмите кнопку **Создать модель прогнозирования**.</span><span class="sxs-lookup"><span data-stu-id="512f9-130">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="512f9-131">После завершения развертывания модели ИИ (успешного или неудачного) сущности CDS, необходимые для создания интеграции, будут развернуты в CDS.</span><span class="sxs-lookup"><span data-stu-id="512f9-131">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="512f9-132">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="512f9-132">Privacy notice</span></span>

<span data-ttu-id="512f9-133">Предварительные версии (1) могут использовать меньшую степень конфиденциальности и безопасности, чем сервис Dynamics 365 Finance and Operations, (2) не включаются в соглашение об уровне обслуживания (SLA) для этого сервиса, (3), не должны использоваться для обработки личных данных или других данных, являющихся объектом соответствия юридическим или нормативным требованиям и (4) имеет ограниченную поддержку.</span><span class="sxs-lookup"><span data-stu-id="512f9-133">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
