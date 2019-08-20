---
title: Взаимодействие с клиентами внутренней цепочки поставок
description: Эта процедура показывает, как просмотреть все спланированные заказы, которые будут выполняться внутрихолдинговым поставщиком.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 930a986b6dfe40d4d40de1f9ee8b1e4b88371166
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835990"
---
# <a name="collaborate-with-internal-supply-chain-customers"></a><span data-ttu-id="8cfc3-103">Взаимодействие с клиентами внутренней цепочки поставок</span><span class="sxs-lookup"><span data-stu-id="8cfc3-103">Collaborate with internal supply chain customers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8cfc3-104">Эта процедура показывает, как просмотреть все спланированные заказы, которые будут выполняться внутрихолдинговым поставщиком.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="8cfc3-105">В качестве компании с демонстрационными данными для создания этой процедуры используется DEMF.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="8cfc3-106">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="8cfc3-106">Click Master planning.</span></span>
2. <span data-ttu-id="8cfc3-107">В поле "План" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="8cfc3-108">В поле "План" выберите план 10.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="8cfc3-109">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="8cfc3-109">Click Run.</span></span>
4. <span data-ttu-id="8cfc3-110">В поле "Количество потоков" введите число.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="8cfc3-111">Представляет собой количество параллельных потоков, которые будут использоваться для сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="8cfc3-112">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8cfc3-112">Click OK.</span></span>
    * <span data-ttu-id="8cfc3-113">Это может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-113">This may take a while.</span></span>  
6. <span data-ttu-id="8cfc3-114">Щелкните "Запланированный внутрихолдинговый спрос".</span><span class="sxs-lookup"><span data-stu-id="8cfc3-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="8cfc3-115">Щелкните "Исходящий запланированный внутрихолдинговый спрос".</span><span class="sxs-lookup"><span data-stu-id="8cfc3-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="8cfc3-116">Эта страница предоставляет обзор всего планового спроса, который будет покрыт внутренним поставщиком цепи поставок.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="8cfc3-117">Разверните раздел "Подробности вышестоящего спроса".</span><span class="sxs-lookup"><span data-stu-id="8cfc3-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="8cfc3-118">В этом разделе можно просмотреть сведения о том, как будет покрыт спрос.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="8cfc3-119">Может потребоваться подождать, пока будет завершено сводное планирование в компании-поставщике, чтобы посмотреть здесь дополнительную информацию.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

