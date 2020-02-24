---
title: Переключение между вариантами дизайна поставщиков
description: Эта тема описывает способ переключения интеграции данных поставщиков между приложениями Finance and Operations и Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
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
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 587a9b98f28b11e303aff4b59e9726f220d956eb
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019973"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="63aef-103">Переключение между вариантами дизайна поставщиков</span><span class="sxs-lookup"><span data-stu-id="63aef-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="63aef-104">Поток данных поставщика</span><span class="sxs-lookup"><span data-stu-id="63aef-104">Vendor data flow</span></span> 

<span data-ttu-id="63aef-105">Если используете другие приложения Dynamics 365 для обработки поставщиков и хотите изолировать информацию о поставщиках от информации о клиентах, используйте основной дизайн поставщика.</span><span class="sxs-lookup"><span data-stu-id="63aef-105">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Основной поток поставщика](media/dual-write-vendor-data-flow.png)
 
<span data-ttu-id="63aef-107">Если используете другие приложения Dynamics 365 для обработки поставщиков и хотите продолжать использовать сущность **Организация** для хранения информации о поставщиках, используйте этот расширенный дизайн поставщика.</span><span class="sxs-lookup"><span data-stu-id="63aef-107">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="63aef-108">В этом дизайне расширенные сведения о поставщике, такие как статус заблокированного поставщика и профиль поставщика, хранятся в объекте **поставщики** в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="63aef-108">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Поток расширенных поставщиков](media/dual-write-vendor-detail.jpg)
 
<span data-ttu-id="63aef-110">Выполните следующие действия, чтобы использовать расширенный дизайн поставщиков:</span><span class="sxs-lookup"><span data-stu-id="63aef-110">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="63aef-111">Пакет решения **SupplyChainCommon** содержит шаблоны workflow-процессов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="63aef-111">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="63aef-112">![Шаблоны workflow-процессов](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="63aef-112">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="63aef-113">Создание новых workflow-процессов с помощью шаблонов workflow-процессов:</span><span class="sxs-lookup"><span data-stu-id="63aef-113">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="63aef-114">Создайте новый workflow-процесс для объекта **Поставщик** с помощью шаблона workflow-процессов **Создание поставщиков в объекте "Организация"** и щелкните **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63aef-114">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="63aef-115">Этот workflow-процесс обрабатывает сценарий создания поставщиков для объекта **Организация**.</span><span class="sxs-lookup"><span data-stu-id="63aef-115">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="63aef-116">![Создание поставщиков в объекте "Организация"](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="63aef-116">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="63aef-117">Создайте новый workflow-процесс для объекта **Поставщик** с помощью шаблона workflow-процессов **Обновление объекта "Организации"** и щелкните **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63aef-117">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="63aef-118">Этот workflow-процесс обрабатывает сценарий обновления поставщиков для объекта **Организация**.</span><span class="sxs-lookup"><span data-stu-id="63aef-118">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="63aef-119">![Обновление объекта "Организации"](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="63aef-119">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="63aef-120">Создание workflow-процессов из шаблонов, созданных в объекте **Организации**.</span><span class="sxs-lookup"><span data-stu-id="63aef-120">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="63aef-121">![Создание поставщиков в объекте "Поставщики"](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="63aef-121">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="63aef-122">![Обновление объекта "Поставщики"](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="63aef-122">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="63aef-123">Workflow-процессы можно настроить как workflow-процессы в реальном времени или в фоновом режиме в соответствии с требованиями пользователя.</span><span class="sxs-lookup"><span data-stu-id="63aef-123">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="63aef-124">![Преобразование в фоновый workflow-процесс](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="63aef-124">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="63aef-125">Активируйте workflow-процессы, созданные в объектах **Организация** и **Поставщик**, чтобы начать использовать объект **Организация** для хранения информации о поставщике.</span><span class="sxs-lookup"><span data-stu-id="63aef-125">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the **Account** entity for storing vendor information.</span></span> 
 
