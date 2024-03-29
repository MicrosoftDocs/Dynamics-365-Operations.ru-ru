---
title: Создание заранее определенных вариантов продукта
description: В этой процедуре показано, как создать варианты продукта для шаблона продукта с использованием комбинаций аналитик продукта.
author: t-benebo
ms.date: 08/09/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a26439b8c7346cdce2b4c9804493fea94c29ac31
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335926"
---
# <a name="predefined-product-variants"></a>Заранее определенные варианты продукта

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a>Пример сценария: создание предопределенных вариантов продукта

В этом примере сценария показано, как создать варианты продукта для шаблона продукта с использованием комбинаций аналитик продукта.

### <a name="make-demo-data-available"></a>Сделать демонстрационные данные доступными

Для выполнения этого сценария с помощью предложенных здесь значений необходимо установить демонстрационные данные, а также необходимо выбрать юридическое лицо *USMF*.

### <a name="step-1-create-a-product-master"></a>Шаг 1. Создание шаблона продукта

Создание шаблона продукта:

1. Перейдите в раздел **Управление сведениями о продукте > Продукты > Шаблоны продукта**.
1. Выберите **Создать**.
1. Если поле **Номер продукта** еще не отображает номер, введите значение. Это необходимо, только если для этого поля не была настроена номерная серия.
1. В поле **Название продукта** введите название.
1. В поле **Группа аналитик продуктов** выберите группу аналитик продуктов *SizeCol* (размер и цвет).
1. Нажмите **ОК**, чтобы создать и открыть новый шаблон продукта.

### <a name="step-2-add-product-dimensions"></a>Шаг 2. Добавление аналитик продукта

В этом примере показано, как ввести аналитики продукта вручную. Можно также выбрать размер, цвет или группу стилей, включающую значения аналитик продукта, которые необходимо использовать.

Добавление аналитик продукта:

1. При открытом новом шаблоне продукта выберите **Аналитики продукта** в области действий.
1. Откройте вкладку **Размер** и выберите **Создать** на панели инструментов, чтобы добавить строку в сетку. Выполните следующие настройки для новой строки:
    - **Размер:** выберите значение размера.
    - **Имя:** введите имя для размера.
1. Выберите **Создать** на панели инструментов и добавьте второй размер в сетку с новым **Размер** и **Имя**.
1. Откройте вкладку **Цвета** и выберите **Создать** на панели инструментов, чтобы добавить строку в сетку. Выполните следующие настройки для новой строки:
    - **Цвет:** выберите значение цвета.
    - **Имя:** введите имя для цвета.
1. Выберите **Создать** на панели инструментов и добавьте второй цвет в сетку с новым **Цвет** и **Имя**.
1. Нажмите **Сохранить**.
1. Закройте страницу, чтобы вернуться в новый шаблон продукта.

### <a name="step-3-generate-product-variants"></a>Шаг 3. Создание вариантов продукта

> [!NOTE]
> В этом разделе описывается создание вариантов продукта, когда функция *Улучшения страницы предложений вариантов* не активирована. В следующем разделе приводятся сведения о создании вариантов продукта, когда эта функция доступна.

Создание вариантов продукта:

1. При открытом новом шаблоне продукта выберите **Варианты продукта** в области действий.
1. Выберите **Предложения варианта** в области действий.
1. Система создает список со всеми возможными комбинациями размеров и цветов, определенных для продукта. Выберите **Выбрать все** на панели инструментов.
    - В этом примере выбраны все возможные варианты. Если требуется использовать только подмножество возможных комбинаций аналитик продукта, установите флажки только для тех полей, которые необходимы.  
1. Выберите **Создать**.
1. Нажмите **Сохранить**.

## <a name="improved-variant-suggestions"></a>Улучшенные предложения вариантов

Функция *Усовершенствования страницы предложения вариантов* позволяет улучшить страницу **Предложения вариантов**, чтобы решить проблемы с производительностью и удобством использования для компаний с большим количеством комбинаций аналитик продукта. Усовершенствованный процесс выбора значений аналитики продукта, для которых создается предложение вариантов, значительно ускоряет и упрощает определение и выпуск соответствующего набора вариантов продукта.

Эта функция добавляет следующие усовершенствования:

- **Отложенное создание предложений вариантов**: страница **Предложения вариантов** больше не отображает предложения при первом открытии. Вместо этого необходимо явно выбрать нужные значения, а затем нажать кнопку **Предложить** для создания комбинаций. Это делает процесс более видимым и интерактивным.
- **Выбор значений аналитик:** при наличии большого количества значений аналитик обычно необходимо создать предложения вариантов, включающие только некоторые из них (например, при внедрении нового набора цветов или стилей). Улучшенная структура позволяет выбрать значения аналитик, для которых требуется создать предложения вариантов продукта. Это значительно увеличивает соответствие предлагаемых вариантов и повышает производительность и системы, и пользователя.

### <a name="turn-the-variant-suggestions-page-improvements-feature-on-or-off"></a>Включение или отключение функции улучшений страницы предложений вариантов

Чтобы использовать эту функцию, ее необходимо включить для системы. В Supply Chain Management версии 10.0.25 эта функция включена по умолчанию. В Supply Chain Management версии 10.0.29 эта функция обязательна и не может быть отключена. При запуске версии, более старой, чем 10.0.29, администраторы могут включать или выключать эту функцию путем поиска функции *Улучшения страницы предложений вариантов* в рабочей области [Управление функциями](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="work-with-the-improved-variant-suggestions"></a>Работа с усовершенствованными предложениями вариантов

Для создания предложений вариантов продукта, когда функция *Улучшения страницы предложений вариантов* включена:

1. Откройте или создайте шаблон продукта и добавьте в него необходимые аналитики продукта, как это описано в предыдущем разделе.
1. При открытом шаблоне продукта выберите **Варианты продукта** в области действий.
1. Выберите **Предложения варианта** в области действий.
1. Выберите значения, которые необходимо использовать для каждой аналитики.
1. На верхней панели инструментов выберите **Предложить**.
1. Система создает список со всеми возможными комбинациями выбранных размеров и цветов. На экспресс-вкладке **Предлагаемые варианты** установите флажок для каждой комбинации аналитики продукта, которую необходимо использовать, или выберите **Выбрать все** на панели инструментов, чтобы выбрать все из них.  
1. Выберите **Создать**, чтобы добавить варианты в текущий шаблон продукта.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
