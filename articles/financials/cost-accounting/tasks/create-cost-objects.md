---
title: Создание объектов затрат
description: Эта процедура показывает порядок создания объектов затрат путем импорта финансовой аналитики центра затрат Dynamics 365 for Finance and Operations, Enterprise edition в модуль учета затрат через соединитель данных.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8f63827977f080aa78fb385c60f757ad6b710005
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841257"
---
# <a name="create-cost-objects"></a>Создание объектов затрат 

[!include [task guide banner](../../includes/task-guide-banner.md)]

Эта процедура показывает порядок создания объектов затрат путем импорта финансовой аналитики центра затрат Dynamics 365 for Finance and Operations, Enterprise edition в модуль учета затрат через соединитель данных. В качестве демонстрационной компании для создания этой процедуры используется USMF. Эта процедура для функции учета затрат, которая была добавлена в версии 1611 Dynamics 365 for Operations.


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

