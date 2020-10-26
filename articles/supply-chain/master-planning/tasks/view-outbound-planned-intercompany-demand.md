---
title: Просмотр исходящего запланированного внутрихолдингового спроса
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 259ce229c18466b7d29fd231dc3f0be8a6906c6b
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978112"
---
# <a name="view-outbound-planned-intercompany-demand"></a><span data-ttu-id="f31ab-103">Просмотр исходящего запланированного внутрихолдингового спроса</span><span class="sxs-lookup"><span data-stu-id="f31ab-103">View outbound planned intercompany demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f31ab-104">Эта процедура показывает, как просмотреть все спланированные заказы, которые будут выполняться внутрихолдинговым поставщиком.</span><span class="sxs-lookup"><span data-stu-id="f31ab-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="f31ab-105">В качестве компании с демонстрационными данными для создания этой процедуры используется DEMF.</span><span class="sxs-lookup"><span data-stu-id="f31ab-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="f31ab-106">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="f31ab-106">Click Master planning.</span></span>
2. <span data-ttu-id="f31ab-107">В поле "План" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f31ab-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="f31ab-108">В поле "План" выберите план 10.</span><span class="sxs-lookup"><span data-stu-id="f31ab-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="f31ab-109">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="f31ab-109">Click Run.</span></span>
4. <span data-ttu-id="f31ab-110">В поле "Количество потоков" введите число.</span><span class="sxs-lookup"><span data-stu-id="f31ab-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="f31ab-111">Представляет собой количество параллельных потоков, которые будут использоваться для сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="f31ab-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="f31ab-112">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f31ab-112">Click OK.</span></span>
    * <span data-ttu-id="f31ab-113">Это может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="f31ab-113">This may take a while.</span></span>  
6. <span data-ttu-id="f31ab-114">Щелкните "Запланированный внутрихолдинговый спрос".</span><span class="sxs-lookup"><span data-stu-id="f31ab-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="f31ab-115">Щелкните "Исходящий запланированный внутрихолдинговый спрос".</span><span class="sxs-lookup"><span data-stu-id="f31ab-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="f31ab-116">Эта страница предоставляет обзор всего планового спроса, который будет покрыт внутренним поставщиком цепи поставок.</span><span class="sxs-lookup"><span data-stu-id="f31ab-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="f31ab-117">Разверните раздел "Подробности вышестоящего спроса".</span><span class="sxs-lookup"><span data-stu-id="f31ab-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="f31ab-118">В этом разделе можно просмотреть сведения о том, как будет покрыт спрос.</span><span class="sxs-lookup"><span data-stu-id="f31ab-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="f31ab-119">Может потребоваться подождать, пока будет завершено сводное планирование в компании-поставщике, чтобы посмотреть здесь дополнительную информацию.</span><span class="sxs-lookup"><span data-stu-id="f31ab-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

