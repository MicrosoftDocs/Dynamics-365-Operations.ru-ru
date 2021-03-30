---
title: Взаимодействие с клиентами внутренней цепочки поставок
description: Эта процедура показывает, как просмотреть все спланированные заказы, которые будут выполняться внутрихолдинговым поставщиком.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6fd306d21097cdc850b7e9ae14f9a292fe0d4db
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246749"
---
# <a name="collaborate-with-internal-supply-chain-customers"></a><span data-ttu-id="36f6f-103">Взаимодействие с клиентами внутренней цепочки поставок</span><span class="sxs-lookup"><span data-stu-id="36f6f-103">Collaborate with internal supply chain customers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="36f6f-104">Эта процедура показывает, как просмотреть все спланированные заказы, которые будут выполняться внутрихолдинговым поставщиком.</span><span class="sxs-lookup"><span data-stu-id="36f6f-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="36f6f-105">В качестве компании с демонстрационными данными для создания этой процедуры используется DEMF.</span><span class="sxs-lookup"><span data-stu-id="36f6f-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="36f6f-106">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="36f6f-106">Click Master planning.</span></span>
2. <span data-ttu-id="36f6f-107">В поле "План" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="36f6f-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="36f6f-108">В поле "План" выберите план 10.</span><span class="sxs-lookup"><span data-stu-id="36f6f-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="36f6f-109">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="36f6f-109">Click Run.</span></span>
4. <span data-ttu-id="36f6f-110">В поле "Количество потоков" введите число.</span><span class="sxs-lookup"><span data-stu-id="36f6f-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="36f6f-111">Представляет собой количество параллельных потоков, которые будут использоваться для сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="36f6f-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="36f6f-112">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="36f6f-112">Click OK.</span></span>
    * <span data-ttu-id="36f6f-113">Это может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="36f6f-113">This may take a while.</span></span>  
6. <span data-ttu-id="36f6f-114">Щелкните "Запланированный внутрихолдинговый спрос".</span><span class="sxs-lookup"><span data-stu-id="36f6f-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="36f6f-115">Щелкните "Исходящий запланированный внутрихолдинговый спрос".</span><span class="sxs-lookup"><span data-stu-id="36f6f-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="36f6f-116">Эта страница предоставляет обзор всего планового спроса, который будет покрыт внутренним поставщиком цепи поставок.</span><span class="sxs-lookup"><span data-stu-id="36f6f-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="36f6f-117">Разверните раздел "Подробности вышестоящего спроса".</span><span class="sxs-lookup"><span data-stu-id="36f6f-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="36f6f-118">В этом разделе можно просмотреть сведения о том, как будет покрыт спрос.</span><span class="sxs-lookup"><span data-stu-id="36f6f-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="36f6f-119">Может потребоваться подождать, пока будет завершено сводное планирование в компании-поставщике, чтобы посмотреть здесь дополнительную информацию.</span><span class="sxs-lookup"><span data-stu-id="36f6f-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]