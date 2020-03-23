---
title: Работа с предустановленными макетами
description: В этом разделе описывается, как работать с предустановленными макетами в Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c8149c6e443c77dabfa641a698c931176bedbc98
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002644"
---
# <a name="work-with-preset-layouts"></a>Работа с предустановленными макетами


[!include [banner](includes/banner.md)]

В этом разделе описывается, как работать с предустановленными макетами в Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Обзор

Прежде чем выполнять процедуры, описанные в этом разделе, следует ознакомиться с разделом [Предустановленные и пользовательские макеты](templates-layouts-overview.md#preset-and-custom-layouts). Общие сведения см. в разделе [Общие сведения о шаблонах и макетах](templates-layouts-overview.md).

## <a name="create-a-new-preset-layout"></a>Создание нового предустановленного макета

Существует два метода создания предустановленного макета. Можно сохранить существующий пользовательский макет или создать предустановленный макет с нуля.

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a>Создание предустановленного макета из существующего пользовательского макета

Для создания предустановленного макета из существующего пользовательского макета выполните следующие действия.

1. Откройте существующую страницу, которая в настоящее время не использует предустановленный макет, и имеет структуру модулей, которую необходимо повторно использовать для других страниц сайта.
1. Выберите **Извлечь**.
1. Выберите **Сохранить как новый макет**. Откроется диалоговое окно **Сохранить как новый макет**.
1. Введите имя и описание для предустановленного макета. Введенные значения будут отображаться для других авторов при создании новых страниц из вашего макета или при переключении на него. Поэтому введите значения, которые будут полезны для авторов страниц.
1. Нажмите **ОК**.

Предустановленный макет теперь будет доступен при создании новых страниц или выборе другого макета для страницы в той же иерархии шаблонов.

> [!TIP]
> Чтобы быстро проверить, привязана ли в данный момент конкретная страница к предустановленному макету, выберите страницу в представлении списка страниц и проверьте метаданные макета на панели свойств справа.

### <a name="create-a-new-preset-layout"></a>Создание нового предустановленного макета

Для создания предустановленного макета с нуля выполните следующие действия.

1. В области переходов слева выберите **Макеты**.
1. Выберите **Создать макет**. Откроется диалоговое окно **Создать макет**.
1. Выберите шаблон, который будет использоваться для предустановленного макета.
1. Введите имя и описание для предустановленного макета. Введенные значения будут отображаться для других авторов при создании новых страниц из вашего макета или при переключении на него. Поэтому введите значения, которые будут полезны для авторов страниц.
1. Выберите **ОК**, чтобы создать новый предустановленный макет и открыть редактор макетов.
1. В редакторе макетов добавьте и настройте модули, используя дерево структуры в левой части и на панель свойств справа. (Процесс похож на процесс для добавления и настройки модулей для шаблона в редакторе шаблонов.) Расположение модулей и всех заблокированных настроек по умолчанию становится централизованной конфигурацией модулей для всех страниц, использующих этот предустановленный макет.

## <a name="modify-a-preset-layout"></a>Изменение предустановленного макета

Чтобы изменить предустановленный макет, выполните следующие действия.

1. В области переходов слева выберите **Макеты**.
1. В редакторе макетов в дереве структуры слева выберите модуль, который необходимо изменить. Затем выполните любое из следующих действий:

    - Чтобы переместить модуль вверх или вниз внутри родительского модуля, выберите кнопку с многоточием (**...**) для модуля, затем выберите **Переместить вверх** или **Переместить вниз**.
    - Чтобы изменить настройки модуля по умолчанию, используйте панель свойств для ввода значений по умолчанию и, при необходимости, блокировки для всех нижестоящих страниц.
    - Чтобы добавить новые модули или фрагменты в модули-контейнеры, выберите кнопку с многоточием, затем выберите **Добавить модуль** или **Добавить фрагмент**.
    - Чтобы удалить модуль из макета, выберите кнопку с многоточием, затем выберите **Удалить**.

## <a name="change-a-preset-layout-theme"></a>Изменение темы предустановленного макета

Стандартной практикой является задание темы по умолчанию для всех страниц, использующих предустановленный макет.

Чтобы задать или изменить тему для всех дочерних страниц, использующих предустановленный макет, выполните следующие действия.

1. В редакторе макетов в дереве структуры слева выберите модуль-контейнер страницы. (Обычно этот модуль является вторым узлом и называется **Страница по умолчанию**.)
1. В области свойств справа в поле **Тема** выберите тему.

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a>Сохранение, возврат, предварительный просмотр и публикация предустановленного макета

Для сохранения и возврата предустановленного макета выполните следующие действия.

1. Выберите **Сохранить** в верхней части редактора макетов. Сохраненные изменения не влияют на нисходящие страницы, пока они не будут возвращены.
1. Выберите **Вернуть**. Ваши изменения теперь доступны для нижестоящих рабочих процессов.

Для предварительного просмотра изменений либо откройте существующую страницу, использующую этот предустановленный макет, либо создайте новую страницу на основе этого макета.

После предварительного просмотра изменений вашего предустановленного макета выполните одно из следующих действий, чтобы опубликовать макет на действующем сайте:

* Перейдите к пункту **Маеты**, выберите макет, затем выберите **Опубликовать**.
* В редакторе макетов выберите **Опубликовать**.
* Опубликуйте страницу, которая ссылается на неопубликованный макет. Макет будет опубликован автоматически.

> [!WARNING]
> На предустановленные макеты могут ссылаться несколько страниц. При публикации предустановленного макета имейте ввиду, что это может повлиять на компоновку нескольких страниц.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор шаблонов и макетов](templates-layouts-overview.md)

[Работа с шаблонами](work-with-templates.md)