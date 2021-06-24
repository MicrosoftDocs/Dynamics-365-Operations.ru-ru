---
title: Создание проекта средства интеграции данных (предварительная версия)
description: В этой теме объясняется, как создать проект интегратора данных.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 59f85c64ea7b1f539a245e08b76bd6a34797b0ca
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186476"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="22079-103">Создание проекта средства интеграции данных (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="22079-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="22079-104">В этой теме объясняется, как создать проект интегратора данных.</span><span class="sxs-lookup"><span data-stu-id="22079-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="22079-105">Войдите в Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="22079-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="22079-106">Перейдите к пункту **Рабочие области \> Управление данными** и выберите **Сущности данных**.</span><span class="sxs-lookup"><span data-stu-id="22079-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="22079-107">Прежде чем перейти к следующему шагу, подождите, пока все сущности данных не будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="22079-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="22079-108">Откройте [портал Power Apps](https://make.powerapps.com/) и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="22079-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="22079-109">Выберите подходящую среду.</span><span class="sxs-lookup"><span data-stu-id="22079-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="22079-110">В левой области переходов выберите **Данные \> Подключения**.</span><span class="sxs-lookup"><span data-stu-id="22079-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="22079-111">Подключитесь к соответствующим экземплярам следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="22079-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="22079-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="22079-112">Dynamics 365</span></span>
        - <span data-ttu-id="22079-113">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="22079-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="22079-114">Откройте [среды Power Apps](https://admin.powerapps.com/environments) и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="22079-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="22079-115">Выберите **Интегратор данных**.</span><span class="sxs-lookup"><span data-stu-id="22079-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="22079-116">Выберите **Наборы подключений**.</span><span class="sxs-lookup"><span data-stu-id="22079-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="22079-117">Выберите **Создать набор подключений**.</span><span class="sxs-lookup"><span data-stu-id="22079-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="22079-118">Введите имя подключения.</span><span class="sxs-lookup"><span data-stu-id="22079-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="22079-119">Выберите подходящие подключения для следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="22079-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="22079-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="22079-120">Dynamics 365</span></span>
        - <span data-ttu-id="22079-121">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="22079-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="22079-122">Выберите соответствующее сопоставление организации.</span><span class="sxs-lookup"><span data-stu-id="22079-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="22079-123">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="22079-123">Select **Create**.</span></span>

5. <span data-ttu-id="22079-124">Откройте [среды Power Apps](https://admin.powerapps.com/environments) и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="22079-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="22079-125">Создайте проекты интеграции данных для следующих шаблонов, используя только что созданный набор соединений:</span><span class="sxs-lookup"><span data-stu-id="22079-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="22079-126">Результаты анализа платежей клиентов (из CDS в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="22079-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
            - <span data-ttu-id="22079-127">Если используется версия 10.0.17 или более поздняя, необходимо использовать шаблон с именем, результат Аналитики платежей клиентов (из CDS в Fin and Ops 10.0.17+).</span><span class="sxs-lookup"><span data-stu-id="22079-127">If you are using version 10.0.17 or later, you need to use the template named, Customer payment insights result (CDS to Fin and Ops 10.0.17+).</span></span>
        - <span data-ttu-id="22079-128">Результаты временных рядов потоков денежных средств (из CDS в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="22079-128">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="22079-129">Результаты временных рядов бюджетов (из CDS в Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="22079-129">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="22079-130">Задайте соответствующее планирование для каждого проекта.</span><span class="sxs-lookup"><span data-stu-id="22079-130">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="22079-131">Если вы не видите требуется сущности в CDS, перейдите в раздел **Кредит и сбор задолженностей > Настройка > Финансовый анализ > Параметры финансового анализа**, активируйте функцию прогнозирования платежей клиентов и нажмите кнопку **Создать модель прогнозирования**.</span><span class="sxs-lookup"><span data-stu-id="22079-131">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="22079-132">После завершения развертывания модели ИИ (успешного или неудачного) сущности CDS, необходимые для создания интеграции, будут развернуты в CDS.</span><span class="sxs-lookup"><span data-stu-id="22079-132">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
