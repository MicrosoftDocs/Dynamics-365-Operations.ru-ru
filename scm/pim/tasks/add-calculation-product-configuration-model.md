--- 
title: "Добавление расчета к модели конфигурации продукта"
description: "Ниже описан порядок добавления нового расчета в модель конфигурации продукта."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
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
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 9ac2d9bcc316a57941136c248a0c5ff030a1fe49
ms.contentlocale: ru-ru
ms.lasthandoff: 07/28/2017

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Добавление расчета к модели конфигурации продукта

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ниже описан порядок добавления нового расчета в модель конфигурации продукта. Он показывает, как можно создать логическое выражение с помощью оператора "если" оператор для задания высоты динамика "10" для белых динамиков и "15" для всех других корпусов. Процедура использует компонента динамика класса Hi-End в демонстрационной компании USMF.


## <a name="add-a-calculation"></a>Добавление расчета

## <a name="create-calculation-expression"></a>Создание выражения расчета
1. Щелкните "Изменить выражение".
2. В поле "ConstraintBody" введите в "If[CabinetFinish=="White", 10, 15]".
3. Щелкните "Проверить".
4. Щелкните "Закрыть".
5. Нажмите кнопку "OК".


