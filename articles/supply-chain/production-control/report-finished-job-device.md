---
title: Приемка в местонахождении, не находящемся под управлением грузоместа, с устройства карты задания
description: В этой теме описывается процесс заполнения готовых продуктов в производственном заказе в запасы, если грузоместо контролирует местоположение.
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 35ad27a6b8a52bfd086fbe4fc57b1681ff88fd5b
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/11/2019
ms.locfileid: "1995150"
---
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="b9c23-103">Приемка в местонахождении, не находящемся под управлением грузоместа, с устройства карты задания</span><span class="sxs-lookup"><span data-stu-id="b9c23-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="b9c23-104">Процесс, который называется приемкой, переводит готовые продукты в производственном заказе в запасы.</span><span class="sxs-lookup"><span data-stu-id="b9c23-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="b9c23-105">Если готовый продукт активирован для расширенных складских процессов, продукт принимается в местоположении, которое называется выходным местоположением производства</span><span class="sxs-lookup"><span data-stu-id="b9c23-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="b9c23-106">Сведения о настройке выходного местоположения производства, см. в разделе [Местонахождение получения из производства](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span><span class="sxs-lookup"><span data-stu-id="b9c23-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="b9c23-107">Для выполнения этой задачи необходимо выбрать существующий номер грузоместа.</span><span class="sxs-lookup"><span data-stu-id="b9c23-107">You must select an existing license plate number to complete this task.</span></span> <span data-ttu-id="b9c23-108">Если местоположение получения из производства настроено для отслеживания с помощью грузоместа, необходимо включить номер грузоместа при приемке выходного местоположения производства как готового.</span><span class="sxs-lookup"><span data-stu-id="b9c23-108">If the production output location is set up to be tracked by license plate, then a license plate number must be included when reporting the production output location as finished.</span></span> <span data-ttu-id="b9c23-109">Поле **Грузоместо** отображается в приглашении **Проверить ход выполнения** на странице **Карта задания — устройство**.</span><span class="sxs-lookup"><span data-stu-id="b9c23-109">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="b9c23-110">Это поле отображается в приглашении **Проверить ход выполнения**, только при создании отчета по последней операции производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="b9c23-110">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order.</span></span> <span data-ttu-id="b9c23-111">Это поле отображается только в том случае, если номенклатура для производственного заказа включена для процессов управления складом.</span><span class="sxs-lookup"><span data-stu-id="b9c23-111">The field is only shown if the item for the production order is enabled for the warehouse management processes.</span></span> 
