---
title: Создание объектов затрат
description: Эта процедура демонстрирует порядок создания объектов затрат путем импорта финансовой аналитики центра затрат в модуль учета затрат через соединитель данных.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1219cb15ecec7c156579c5cf7c3a3511a141e00b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810062"
---
# <a name="create-cost-objects"></a>Создание объектов затрат 

[!include [banner](../../includes/banner.md)]

Эта процедура демонстрирует порядок создания объектов затрат путем импорта финансовой аналитики центра затрат в модуль учета затрат через соединитель данных. В качестве демонстрационной компании для создания этой процедуры используется USMF. 


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]