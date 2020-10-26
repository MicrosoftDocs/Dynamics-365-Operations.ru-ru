---
title: Обзор соглашений об условиях обслуживания
description: В соглашении об уровне обслуживания с клиентом согласовывается минимальное время отклика с учетом интервала между моментом регистрации проблемы в обслуживающей компании и моментом ее решения.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01cdfe519e55ca2a9aa17f4ac181ee675b2793cf
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982363"
---
# <a name="service-level-agreements-overview"></a><span data-ttu-id="916a5-103">Обзор соглашений об условиях обслуживания</span><span class="sxs-lookup"><span data-stu-id="916a5-103">Service level agreements overview</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="916a5-104">Соглашение об уровне обслуживания (SLA) - это договор между обслуживающей компанией и обслуживаемым клиентом.</span><span class="sxs-lookup"><span data-stu-id="916a5-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="916a5-105">В SLA с клиентом согласовывается минимальное время отклика с учетом интервала между моментом регистрации проблемы в обслуживающей компании и моментом ее решения.</span><span class="sxs-lookup"><span data-stu-id="916a5-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="916a5-106">SLA устанавливает стандартный уровень обслуживания, предлагаемый клиентам, а также делает прозрачным для обслуживающей компании срок выполнения задания по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="916a5-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="916a5-107">Возможно создание любого числа соглашений об условиях обслуживания для предложения клиентам различных условий обслуживания.</span><span class="sxs-lookup"><span data-stu-id="916a5-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="916a5-108">Создание соглашения об условиях обслуживания</span><span class="sxs-lookup"><span data-stu-id="916a5-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="916a5-109">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Соглашения о сервисном обслуживании** \> **Соглашения об уровне обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="916a5-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="916a5-110">Введите имя соглашения о уровне обслуживания в поле **Соглашение об уровне обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="916a5-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="916a5-111">Укажите время, которое нужно выделить для выполнения заказов на обслуживание, связанных с соглашением об уровне обслуживания.</span><span class="sxs-lookup"><span data-stu-id="916a5-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="916a5-112">Затем выберите календарь, если нужно, чтобы соглашение об уровне обслуживания учитывало конкретный календарь.</span><span class="sxs-lookup"><span data-stu-id="916a5-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="916a5-113">Применение соглашения об условиях обслуживания</span><span class="sxs-lookup"><span data-stu-id="916a5-113">Apply a service level agreement</span></span>

<span data-ttu-id="916a5-114">Соглашение об условиях обслуживания применяется непосредственно к соглашению на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="916a5-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="916a5-115">Заказы на обслуживание, созданные вручную и прикрепленные к соглашению на обслуживание с SLA, измеряются относительного этого SLA.</span><span class="sxs-lookup"><span data-stu-id="916a5-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="916a5-116">Заказы на обслуживание, созданные автоматически, не присоединяются к соглашению об условиях обслуживания.</span><span class="sxs-lookup"><span data-stu-id="916a5-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="916a5-117">Применение соглашения об уровне обслуживания к соглашению на обслуживание</span><span class="sxs-lookup"><span data-stu-id="916a5-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="916a5-118">Щелкните **Управление сервисным обслуживанием** \> **Общее** \> **Соглашения на обслуживание** \> **Соглашения на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="916a5-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="916a5-119">Выберите соглашение о сервисном обслуживании, к которому нужно применить SLA, и щелкните **Изменить** в разделе **Панель операций**.</span><span class="sxs-lookup"><span data-stu-id="916a5-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="916a5-120">В поле **Соглашение об уровне обслуживания** выберите SLA, которое требуется назначить.</span><span class="sxs-lookup"><span data-stu-id="916a5-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="916a5-121">Применение соглашения об уровне обслуживания к группе соглашений на обслуживание</span><span class="sxs-lookup"><span data-stu-id="916a5-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="916a5-122">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Соглашения на обслуживание** \> **Группы соглашений о сервисном обслуживании**.</span><span class="sxs-lookup"><span data-stu-id="916a5-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="916a5-123">В поле **Соглашение об уровне обслуживания** выберите SLA, которое требуется назначить.</span><span class="sxs-lookup"><span data-stu-id="916a5-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="916a5-124">Отслеживание времени в заказе не обслуживание в соответствии с соглашением об условиях обслуживания</span><span class="sxs-lookup"><span data-stu-id="916a5-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="916a5-125">При создании нового заказа на обслуживание в рамках соглашения на обслуживание, которому назначено SLA, инициируется интервал поставки услуги и система начинает отслеживать время поставки.</span><span class="sxs-lookup"><span data-stu-id="916a5-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="916a5-126">Дополнительно можно задать следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="916a5-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="916a5-127">Можно начать и остановить запись времени в заказе на обслуживание, чтобы зарегистрировать общее время, потраченное в заказах на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="916a5-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="916a5-128">Можно отслеживать соответствие интервалу времени, заданному в соглашении об уровне обслуживания.</span><span class="sxs-lookup"><span data-stu-id="916a5-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="916a5-129">Можно определить коды причин, которые необходимо указать при превышении интервала времени, установленного в соглашении об уровне обслуживания.</span><span class="sxs-lookup"><span data-stu-id="916a5-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="916a5-130">См. также</span><span class="sxs-lookup"><span data-stu-id="916a5-130">See also</span></span>

[<span data-ttu-id="916a5-131">Просмотр соответствия с соглашениями об уровне обслуживания</span><span class="sxs-lookup"><span data-stu-id="916a5-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  


