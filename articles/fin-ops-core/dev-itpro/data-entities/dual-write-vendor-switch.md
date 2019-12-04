---
title: Переключение между дизайнами поставщиков
description: ''
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
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772372"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="9e0ce-102">Переключение между дизайнами поставщиков</span><span class="sxs-lookup"><span data-stu-id="9e0ce-102">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="9e0ce-103">Поток данных поставщика</span><span class="sxs-lookup"><span data-stu-id="9e0ce-103">Vendor data flow</span></span> 

<span data-ttu-id="9e0ce-104">Если используете другие приложения Dynamics 365 для обработки поставщиков и хотите изолировать информацию о поставщиках от информации о клиентах, используйте основной дизайн поставщика.</span><span class="sxs-lookup"><span data-stu-id="9e0ce-104">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Основной поток поставщика](media/dual-write-switch-1.png)
 
<span data-ttu-id="9e0ce-106">Если используете другие приложения Dynamics 365 для обработки поставщиков и хотите продолжать использовать сущность **Организация** для хранения информации о поставщиках, используйте этот расширенный дизайн поставщика.</span><span class="sxs-lookup"><span data-stu-id="9e0ce-106">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="9e0ce-107">В этом дизайне расширенные сведения о поставщике, такие как статус заблокированного поставщика и профиль поставщика, хранятся в объекте **поставщики** в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9e0ce-107">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Поток расширенных поставщиков](media/dual-write-switch-2.png)
 
<span data-ttu-id="9e0ce-109">Выполните следующие действия, чтобы использовать расширенный дизайн поставщиков:</span><span class="sxs-lookup"><span data-stu-id="9e0ce-109">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="9e0ce-110">Пакет решения **SupplyChainCommon** содержит шаблоны workflow-процессов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="9e0ce-110">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="9e0ce-111">![Шаблоны workflow-процессов](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="9e0ce-111">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="9e0ce-112">Создание новых workflow-процессов с помощью шаблонов workflow-процессов:</span><span class="sxs-lookup"><span data-stu-id="9e0ce-112">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="9e0ce-113">Создайте новый workflow-процесс для объекта **Поставщик** с помощью шаблона workflow-процессов **Создание поставщиков в объекте "Организация"** и щелкните **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9e0ce-113">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="9e0ce-114">Этот workflow-процесс обрабатывает сценарий создания поставщиков для объекта **Организация**.</span><span class="sxs-lookup"><span data-stu-id="9e0ce-114">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9e0ce-115">![Создание поставщиков в объекте "Организация"](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="9e0ce-115">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="9e0ce-116">Создайте новый workflow-процесс для объекта **Поставщик** с помощью шаблона workflow-процессов **Обновление объекта "Организации"** и щелкните **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9e0ce-116">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="9e0ce-117">Этот workflow-процесс обрабатывает сценарий обновления поставщиков для объекта **Организация**.</span><span class="sxs-lookup"><span data-stu-id="9e0ce-117">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9e0ce-118">![Обновление объекта "Организации"](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="9e0ce-118">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="9e0ce-119">Создание workflow-процессов из шаблонов, созданных в объекте **Организации**.</span><span class="sxs-lookup"><span data-stu-id="9e0ce-119">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9e0ce-120">![Создание поставщиков в объекте "Поставщики"](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="9e0ce-120">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="9e0ce-121">![Обновление объекта "Поставщики"](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="9e0ce-121">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="9e0ce-122">Workflow-процессы можно настроить как workflow-процессы в реальном времени или в фоновом режиме в соответствии с требованиями пользователя.</span><span class="sxs-lookup"><span data-stu-id="9e0ce-122">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9e0ce-123">![Преобразование в фоновый workflow-процесс](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="9e0ce-123">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="9e0ce-124">Активируйте workflow-процессы, созданные в объектах **Организация** и **Поставщик**, чтобы начать использовать объект **Организация** Customer Engagement для хранения информации о поставщике.</span><span class="sxs-lookup"><span data-stu-id="9e0ce-124">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the Customer Engagement **Account** entity for storing vendor information.</span></span> 
 
