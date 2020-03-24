---
title: Приемка в местонахождении, не находящемся под управлением грузоместа, с устройства карты задания
description: В этой теме описывается процесс заполнения готовых продуктов в производственном заказе в запасы, если грузоместо контролирует местоположение.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: 5f61c1abfb115f02e6ff314f6a3e42bb1d3b543f
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092576"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Приемка в местонахождении, не находящемся под управлением грузоместа, с устройства карты задания 

Процесс, который называется приемкой, переводит готовые продукты в производственном заказе в запасы. Если готовый продукт активирован для расширенных складских процессов, продукт принимается в местоположении, которое называется выходным местоположением производства Сведения о настройке выходного местоположения производства, см. в разделе [Местонахождение получения из производства](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

Если место выпуска продукции контролируется грузоместом, то грузоместо должно быть предоставлено при представлении отчетности как законченной. Поле **Грузоместо** отображается в приглашении **Проверить ход выполнения** на странице **Карта задания — устройство**. Поле отображается в подсказке **Проверить ход выполнения** только при представлении отчетности о последней операции производственного заказа, а элемент для производственного заказа включен для процессов управления складом. 

Есть два варианта предоставления грузоместа
- Пользователь выбирает существующее грузоместо в поле грузоместа.
- Грузоместо автоматически создается из номерной серии и по умолчанию вносится в поле грузоместа.

Возможность автоматического создания грузоместа настраивается путем выбора грузоместа **Создать грузоместо** на странице **Настроить карту заданий для устройств**.
