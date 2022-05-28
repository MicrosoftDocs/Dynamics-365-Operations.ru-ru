---
title: Создание объектов затрат
description: Эта процедура демонстрирует порядок создания объектов затрат путем импорта финансовой аналитики центра затрат в модуль учета затрат через соединитель данных.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88196ea19488cd8572bf0e7883298317c9c84696
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734140"
---
# <a name="create-cost-objects"></a>Создание объектов затрат 

[!include [banner](../../includes/banner.md)]

Эта процедура демонстрирует порядок создания объектов затрат путем импорта финансовой аналитики центра затрат в модуль учета затрат через соединитель данных. В качестве демонстрационной компании для создания этой процедуры используется USMF. 


## <a name="create-new-cost-objects"></a>Создание новых объектов затрат
1. Перейдите в раздел **Учет затрат > Аналитики > Аналитики объекта затрат**.
2. Нажмите кнопку **Создать**.
3. В поле **Имя** введите значение.
4. В поле **Соединитель данных для элементов аналитик** введите или выберите значение.
5. В поле **Описание** введите значение.
6. Нажмите кнопку **Сохранить**.

## <a name="configure-the-data-connector"></a>Настройка соединителя данных
1. Щелкните **Настроить поставщика элементов аналитики**.
    * Выберите CostCenter для импорта аналитики CostCenter в модуль учета затрат.  
2. В поле **Имя аналитики** выберите Центр затрат.
3. Щелкните **OK**.

## <a name="import-cost-centers"></a>Импорт центров затрат
1. Щелкните **Импорт элементов аналитики**.
2. Щелкните **OK**.

## <a name="view-the-imported-cost-centers"></a>Просмотр импортированных центров затрат
1. Щелкните **Просмотр элементов аналитики**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
