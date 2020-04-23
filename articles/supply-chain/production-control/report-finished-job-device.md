---
title: Приемка в местонахождении, не находящемся под управлением грузоместа, с устройства карты задания
description: В этой теме описывается процесс заполнения готовых продуктов в производственном заказе в запасы, если грузоместо контролирует местоположение.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: f5863202facc83afb91b380ba5666334783ccbcf
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211177"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="8a1f7-103">Приемка в местонахождении, не находящемся под управлением грузоместа, с устройства карты задания</span><span class="sxs-lookup"><span data-stu-id="8a1f7-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="8a1f7-104">Процесс, который называется приемкой, переводит готовые продукты в производственном заказе в запасы.</span><span class="sxs-lookup"><span data-stu-id="8a1f7-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="8a1f7-105">Если готовый продукт активирован для расширенных складских процессов, продукт принимается в местоположении, которое называется выходным местоположением производства</span><span class="sxs-lookup"><span data-stu-id="8a1f7-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="8a1f7-106">Сведения о настройке выходного местоположения производства, см. в разделе [Местонахождение получения из производства](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span><span class="sxs-lookup"><span data-stu-id="8a1f7-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="8a1f7-107">Если место выпуска продукции контролируется грузоместом, то грузоместо должно быть предоставлено при представлении отчетности как законченной.</span><span class="sxs-lookup"><span data-stu-id="8a1f7-107">If the production output location is license plate controlled, then a license plate must be provided when reporting as finished.</span></span> <span data-ttu-id="8a1f7-108">Поле **Грузоместо** отображается в приглашении **Проверить ход выполнения** на странице **Карта задания — устройство**.</span><span class="sxs-lookup"><span data-stu-id="8a1f7-108">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="8a1f7-109">Поле отображается в подсказке **Проверить ход выполнения** только при представлении отчетности о последней операции производственного заказа, а элемент для производственного заказа включен для процессов управления складом.</span><span class="sxs-lookup"><span data-stu-id="8a1f7-109">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order and the item for the production order is enabled for the warehouse management processes.</span></span> 

<span data-ttu-id="8a1f7-110">Есть два варианта предоставления грузоместа</span><span class="sxs-lookup"><span data-stu-id="8a1f7-110">There are two options for providing the license plate</span></span>
- <span data-ttu-id="8a1f7-111">Пользователь выбирает существующее грузоместо в поле грузоместа.</span><span class="sxs-lookup"><span data-stu-id="8a1f7-111">The user is selecting an existing license plate in the license plate field.</span></span>
- <span data-ttu-id="8a1f7-112">Грузоместо автоматически создается из номерной серии и по умолчанию вносится в поле грузоместа.</span><span class="sxs-lookup"><span data-stu-id="8a1f7-112">The license plate is automatically generated from a number sequence and defaulted to the license plate field.</span></span>

<span data-ttu-id="8a1f7-113">Возможность автоматического создания грузоместа настраивается путем выбора грузоместа **Создать грузоместо** на странице **Настроить карту заданий для устройств**.</span><span class="sxs-lookup"><span data-stu-id="8a1f7-113">The option to have the license plate generated automatically is configured by selecting the option **Generate license plate** on the **Configure job card for devices** page.</span></span>
