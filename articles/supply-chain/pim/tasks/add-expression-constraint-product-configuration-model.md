---
title: Добавление ограничения выражения к модели конфигурации продукта
description: Ниже описан порядок добавления нового выражения ограничения в модель конфигурации продукта.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920889"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Добавление ограничения выражения к модели конфигурации продукта

[!include [banner](../../includes/banner.md)]

Ниже описан порядок добавления нового выражения ограничения в модель конфигурации продукта. Он показывает, как можно предписывать, что защита углов должна применяться к динамику, если пользователь выбрал металлическую переднюю решетку. Процедура использует компонента динамика класса Hi-End в демонстрационной компании USMF.

## <a name="create-an-expression-constraint"></a>Создание ограничения выражения

1. Перейдите в раздел **Управление сведениями о продукте \> Продукты \> Модели конфигурации продукта**.
3. В списке найдите и выберите требуемую запись.
    * В этом примере используется модель динамика класса Hi-End.  
4. В списке выберите ссылку в выбранной строке.
5. Разверните раздел **Ограничения**.
6. Выберите **Добавить**.
7. Выберите **Создать**.
8. В поле **Имя** введите значение.

## <a name="enter-expression"></a>Ввести выражение

1. Выберите **Изменить выражение**.
    * Если вы разблокируете интерфейс в записи задач на этом этапе, можно использовать IntelliSense и список символов для построения выражения ограничения.  
2. В поле **ConstraintBody** введите в "Implies[FrontGrill=="Metal", CornerProtection]".
    * Логика этого выражения гласит: если передняя решетка металлическая, должен быть выбран параметр защиты углов.  
3. Выберите **Проверить**.
    * Функция проверки выполняется через выражение ограничения и проверяет наличие синтаксических ошибок.  
4. Выберите **Закрыть**.
5. Нажмите **ОК**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]