---
title: Расчету модели конфигурации продукта
description: В этой статье описывается, как создать расчеты для атрибутов в модели конфигурации продукта
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 35057a4fc59732fea24e4d953cafed633a936ec1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878942"
---
# <a name="product-configuration-model-calculations"></a>Расчету модели конфигурации продукта

[!include [banner](../includes/banner.md)]

В этой статье описывается, как создать расчеты для атрибутов в модели конфигурации продукта.

## <a name="prerequisites"></a>Необходимые условия

Расчеты используются в модели конфигурации продукта для расчета значения конфигурации продукта. Прежде чем можно будет начать настройку расчетов, должна существовать связанная модель конфигурации продукта. Обзор процесса настройки для моделей конфигурации и соответствующих задач см. в разделе [Настройка модели конфигурации продукта](set-up-maintain-product-configuration-model.md).

## <a name="create-a-calculation"></a>Создание расчета

Расчет состоит из выражения и целевого атрибута. Дополнительные сведения см. в разделе [Вопросы и ответы по расчетам для моделей конфигурации продуктов](calculate-product-configuration-models.md).

Чтобы создать расчет для существующей модели продукта, выполните следующие действия.

1. Перейдите в раздел **Управление сведениями о продукте \> Общее \> Модели конфигурации продукта**.
1. Откройте модель конфигурации продукта, затем выберите **Изменить**.
1. На экспресс-вкладке **Расчеты** выберите **Добавить**, чтобы добавить расчет, затем установите следующие поля:

    - **Имя** — введите имя для расчета.
    - **Описание** — введите описание расчета.
    - **Целевой атрибут** — выберите атрибут, для которого выполняется расчет.

1. Выберите **Изменить выражение**.
1. В диалоговом окне **Введите расчет** добавьте в выражение необходимые атрибуты, операторы и значения. Дополнительные сведения о том, как работать с этими элементами, см. в разделе [Ограничения выражений и ограничения таблиц в моделях конфигурации продукта](expression-constraints-table-constraints-product-configuration-models.md).
1. Когда выражение будет готово, нажмите кнопку **ОК**.

## <a name="calculation-examples"></a>Пример расчета

В этом разделе представлено несколько примеров, демонстрирующих работу расчетов.

### <a name="example-1"></a>Пример 1

Целевой атрибут является логическим, и при расчете используется следующее условное выражение:

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

Это выражение возвращает целевому атрибуту значение *True*, если значение `decimalAttribute2` больше или равно `decimalAttribute1`. В противном случае он возвращает значение *False*.

### <a name="example-2"></a>Пример 2

В этом примере текстовый атрибут `textFixedList` используется в качестве целевого атрибута. Этот атрибут содержит следующий фиксированный список.

| значение | Значение решателя |
|---|---|
| A | 1a |
| млрд | 2b |
| C | 2c |

На следующем снимке экрана показано, как могут отображаться в вашей системе параметры для этого атрибута.

![Настройки типов атрибутов для примера 2.](media/model-calculations-example2.png "Настройки типов атрибутов для примера 2")

Этот атрибут используется в следующем условном операторе:

`If[integerAttribute < 150, 0, 2]`

Если `integerAttribute` меньше 150, эта инструкция возвращает текстовое значение первой записи в фиксированном списке, *A*. В противном случае возвращается текстовое значение третьей записи в фиксированном списке, *C*.

> [!NOTE]
> Фиксированный список эквивалентен перечислению (enum) с нуля, и доступ к его значениям осуществляется с помощью соответствующего целого значения. Таким образом, первое значение фиксированного списка (*A*) сопоставлено значению *0*, второе значение (*B*) сопоставлено *1*, а третье значение (*C*) сопоставлено *2*.

### <a name="example-3"></a>Пример 3

В этом примере используется целевой атрибут `textFixedList` из предыдущего примера. Он также использует другой текстовый атрибут, `textAttribute`, который содержит следующий фиксированный список.

| значение | Значение решателя |
|---|---|
| AA | 1aa |
| BB | 2bb |

На следующем снимке экрана показано, как могут отображаться в вашей системе параметры для этого атрибута.

![Настройки типов атрибутов для примера 3.](media/model-calculations-example3.png "Настройки типов атрибутов для примера 3")

Значение для атрибута `textFixedList` вычисляется с помощью следующего условного оператора:

`If[textAttribute == "1aa", 0, 2]`

Если значение `textAttribute` имеет значение решателя, которое равно *1aa*, это выражение возвращает текстовое значение первой записи в фиксированном списке `textFixedList`, *A*. В противном случае возвращается текстовое значение третьей записи в фиксированном списке `textFixedList`, *C*.

> [!NOTE]
> - Условный оператор должен использовать значение решателя атрибута.
> - В расчетах могут использоваться только атрибуты текста фиксированного списка.

## <a name="see-also"></a>См. также

- [Часто задаваемые вопросы по расчетам моделей конфигураций продуктов](calculate-product-configuration-models.md)
- [Добавление ограничения выражения к модели конфигурации продукта](tasks/add-expression-constraint-product-configuration-model.md)
- [Обзор моделей конфигурации продукта](product-configuration-models.md)
