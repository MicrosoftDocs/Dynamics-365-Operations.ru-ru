---
title: Настройка рекомендаций по продуктам на основе машинного обучения
description: Эта процедура обновляет данные в хранилище объектов, используемые системой машинного обучения, которая обеспечивает рекомендации по продуктам, а затем обеспечивает рекомендации по продуктам в клиентах POS.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BIMeasurementDeployManagementEntityStore, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 700af913f18e23c66db53a92033def06818af1ec
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "348534"
---
# <a name="configure-machine-learning-powered-product-recommendations"></a>Настройка рекомендаций по продуктам на основе машинного обучения

[!include[task guide banner](../includes/task-guide-banner.md)]

Эта процедура обновляет данные в хранилище объектов, используемые системой машинного обучения, которая обеспечивает рекомендации по продуктам, а затем обеспечивает рекомендации по продуктам в клиентах POS. В этой процедуре используется компания с демонстрационными данными USRT.

1. Перейдите в раздел "Администрирование системы" > "Настройка" > "Хранилище объектов".
2. В списке найдите и выберите запись "RetailSales".
3. Нажмите кнопку Обновить.
4. Нажмите кнопку "OК".
5. Закройте страницу.
6. Перейдите в раздел "Розничная торговля и коммерция" > "Настройка центрального офиса" > "Параметры" > "Параметры розничной торговли".
7. Выберите вкладку "Машинное обучение".
8. Выберите значение "Да" в поле "Включить рекомендации по продуктам".
    * Если получено сообщение "Не удалось извлечь модели рекомендаций", это потому, что вы недавно обновили хранилище объектов и система еще не завершила ассимиляцию новых данных. Подождите 2-3 часа и повторите попытку.  
9. Нажмите кнопку "Сохранить".
10. Закройте страницу.

