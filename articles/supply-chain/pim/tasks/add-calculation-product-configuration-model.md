---
title: Добавление расчета к модели конфигурации продукта
description: Ниже описан порядок добавления нового расчета в модель конфигурации продукта.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32bc2ac5815c2739147664f1e1df2528178db51e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213408"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Добавление расчета к модели конфигурации продукта

[!include [banner](../../includes/banner.md)]

Ниже описан порядок добавления нового расчета в модель конфигурации продукта. Он показывает, как можно создать логическое выражение с помощью оператора "если" оператор для задания высоты динамика "10" для белых динамиков и "15" для всех других корпусов. Процедура использует компонента динамика класса Hi-End в демонстрационной компании USMF.


## <a name="add-a-calculation"></a>Добавление расчета

## <a name="create-calculation-expression"></a>Создание выражения расчета
1. Щелкните "Изменить выражение".
2. В поле "ConstraintBody" введите в "If[CabinetFinish=="White", 10, 15]".
3. Щелкните "Проверить".
4. Щелкните "Закрыть".
5. Нажмите кнопку "OК".

