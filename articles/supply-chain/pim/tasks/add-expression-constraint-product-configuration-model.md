---
title: Добавление ограничения выражения к модели конфигурации продукта
description: Ниже описан порядок добавления нового выражения ограничения в модель конфигурации продукта.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c43d7f768069c5ef201a2823a9aa626b38220073
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436052"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Добавление ограничения выражения к модели конфигурации продукта

[!include [banner](../../includes/banner.md)]

Ниже описан порядок добавления нового выражения ограничения в модель конфигурации продукта. Он показывает, как можно предписывать, что защита углов должна применяться к динамику, если пользователь выбрал металлическую переднюю решетку. Процедура использует компонента динамика класса Hi-End в демонстрационной компании USMF.


## <a name="create-an-expression-constraint"></a>Создание ограничения выражения
1. Щелкните "Определение модели вариантов продукта".
2. Щелкните "Модели конфигурации продукта".
3. В списке найдите и выберите требуемую запись.
    * В этом примере используется модель динамика класса Hi-End.  
4. В списке перейдите по ссылке в выбранной строке.
5. Разверните раздел "Ограничения".
6. Нажмите кнопку Добавить.
7. Щелкните "Создать".
8. В поле "Имя" введите значение.

## <a name="enter-expression"></a>Ввести выражение
1. Щелкните "Изменить выражение".
    * Если вы разблокируете интерфейс в записи задач на этом этапе, можно использовать IntelliSense и список символов для построения выражения ограничения.  
2. В поле "ConstraintBody" введите "Implies[FrontGrill=="Metal", CornerProtection]".
    * Логика этого выражения гласит: если передняя решетка металлическая, должен быть выбран параметр защиты углов.  
3. Щелкните "Проверить".
    * Функция проверки выполняется через выражение ограничения и проверяет наличие синтаксических ошибок.  
4. Щелкните "Закрыть".
5. Нажмите кнопку "OК".

