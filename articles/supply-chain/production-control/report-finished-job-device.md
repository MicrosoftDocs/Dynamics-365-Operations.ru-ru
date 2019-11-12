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
ms.openlocfilehash: cb809e596fd6bf3030bcee460838798435512b95
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572137"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Приемка в местонахождении, не находящемся под управлением грузоместа, с устройства карты задания 

Процесс, который называется приемкой, переводит готовые продукты в производственном заказе в запасы. Если готовый продукт активирован для расширенных складских процессов, продукт принимается в местоположении, которое называется выходным местоположением производства Сведения о настройке выходного местоположения производства, см. в разделе [Местонахождение получения из производства](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

Для выполнения этой задачи необходимо выбрать существующий номер грузоместа. Если местоположение получения из производства настроено для отслеживания с помощью грузоместа, необходимо включить номер грузоместа при приемке выходного местоположения производства как готового. Поле **Грузоместо** отображается в приглашении **Проверить ход выполнения** на странице **Карта задания — устройство**. Это поле отображается в приглашении **Проверить ход выполнения**, только при создании отчета по последней операции производственного заказа. Это поле отображается только в том случае, если номенклатура для производственного заказа включена для процессов управления складом. 
