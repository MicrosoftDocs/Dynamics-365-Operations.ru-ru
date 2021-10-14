---
title: Добавление расчета к модели конфигурации продукта
description: Ниже описан порядок добавления нового расчета в модель конфигурации продукта.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d201061ff47203f09f96dc08ff6fc8ac437a6f9e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570665"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]