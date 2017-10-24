--- 
title: "Создание объектов затрат"
description: "Эта процедура показывает порядок создания объектов затрат путем импорта финансовой аналитики центра затрат Dynamics 365 for Finance and Operations, Enterprise edition в модуль учета затрат через соединитель данных."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5d43274aed2edbb91fd4e399cb8d45e91646b055
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="create-cost-objects"></a>Создание объектов затрат 

[!include[task guide banner](../../includes/task-guide-banner.md)]

Эта процедура показывает порядок создания объектов затрат путем импорта финансовой аналитики центра затрат Dynamics 365 for Finance and Operations, Enterprise edition в модуль учета затрат через соединитель данных. В качестве демонстрационной компании для создания этой процедуры используется USMF. Эта процедура предназначена для функции "Учет затрат", которая была добавлена в версии 1611 Dynamics 365 for Operations.


## <a name="create-new-cost-objects"></a>Создание новых объектов затрат
1. Перейдите в раздел "Учет затрат" > "Аналитики" > "Аналитики объекта затрат".
2. Щелкните "Создать".
3. В поле "Имя" введите значение.
4. В поле "Соединитель данных для элементов аналитик" введите или выберите значение.
5. В поле "Описание" введите значение.
6. Нажмите кнопку "Сохранить".

## <a name="configure-the-data-connector"></a>Настройка соединителя данных
1. Щелкните "Настроить поставщика элементов аналитики".
    * Выберите CostCenter для импорта аналитики CostCenter в модуль учета затрат.  
2. В поле "Имя аналитики" выберите "Центр затрат".
3. Нажмите кнопку "OК".

## <a name="import-cost-centers"></a>Импорт центров затрат
1. Щелкните "Импорт элементов аналитики".
2. Нажмите кнопку "OК".

## <a name="view-the-imported-cost-centers"></a>Просмотр импортированных центров затрат
1. Щелкните "Просмотр элементов аналитики".


