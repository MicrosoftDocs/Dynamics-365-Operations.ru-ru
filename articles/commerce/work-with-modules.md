---
title: Работа с модулями
description: В этой статье описывается, как и когда использовать модули в Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 91188590391501042ff0503bdc3592435c30fa63
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291955"
---
# <a name="work-with-modules"></a>Работа с модулями

[!include [banner](includes/banner.md)]

В этой статье описывается, как и когда использовать модули в Microsoft Dynamics 365 Commerce.

Модули являются логическими строительными блоками, составляющими структуру страницы, и они имеют различные цели и области действия. Некоторые модули являются контейнерами высокого уровня, и их единственная цель состоит в том, чтобы хранить и организовывать другие модули (дочерние модули). Другие модули, такие как простой модуль размещения изображений, имеют очень конкретную цель. Другие модули, например, модуль карусели, попадают где-то посередине между этими двумя категориями.

По умолчанию ваш сайт Dynamics 365 Commerce включает библиотеку модулей, которая позволяет использовать большинство основных сценариев электронной коммерции. Вы должны быть способны создавать законченный сайт электронной коммерции только с помощью этих модулей. Однако, возможно, вы захотите настроить эти модули или создать новые, пользовательские модули для конкретных нужд. Если требуется создать пользовательские модули, предусмотрен пакет средств разработки дизайна модулей (SDK), который поможет в создании библиотеки пользовательских модулей.

## <a name="container-modules-and-slots"></a>Контейнерные модули и ячейки

Как упоминалось ранее, некоторые модули предназначены для размещения дочерних модулей. Эти модули называются *контейнерами* и позволяют использовать иерархии вложенных модулей. Контейнерные модули содержат *ячейки*. Ячейки используются для обработки макета и назначения дочерних модулей в контейнере. Примером является модуль-контейнер базовой страницы (модуль верхнего уровня для любой страницы), определяющий несколько важных ячеек:

- Ячейка заголовка
- Ячейка подзаголовка
- Основная ячейка
- Ячейка нижнего колонтитула
- Ячейка вложенного нижнего колонтитула

Разработчик модуля определяет эти ячейки и определяет, какие дочерние модули и в каком количестве могут быть размещены непосредственно внутри него. Например, ячейка заголовка может поддерживать только один модуль типа **Модуль заголовка**, в то время как ячейка основного текста может поддерживать неограниченное число модулей любого типа (за исключением других модулей-контейнеров страниц).

В средствах разработки авторам страниц нет необходимости знать заранее, какие модули могут или не могут быть помещены в каждое гнездо. Когда авторы страниц выбирают ячейку и попытаются выбрать модуль для добавления в него, они увидят отфильтрованное представление типов модулей, которые поддерживаются для этого слота.

## <a name="content-modules"></a>Модули содержимого

Модули содержимого содержат содержимое и мультимедийные элементы, такие как текст (например, заголовки, параграфы и ссылки) или ссылки на ресурсы (например, изображения, видео и PDF). Типы модулей содержимого обычно включают в себя блок содержимого, блок текста и модули рекламного баннера. Модули этих трех типов могут содержать текст или мультимедиа, и они не требуют каких-либо дочерних модулей для отображения на странице.

Большая часть типичных повседневных действий по разработке страниц и контента включает модули содержимого, в основном потому что эти модули определяют реальное содержимое, отображаемое в их родительских контейнерных модулях. Доступно множество модулей содержимого, и эти модули обычно являются последними элементами, которые будут добавлены в иерархию вложенных модулей страницы.

На следующем рисунке показано, как вложены модули в ячейках родительских контейнеров-модулей.

![Вложение модулей.](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Добавление или удаление модулей

Следующие процедуры описывают добавление и удаление модулей.

### <a name="add-a-module"></a>Добавление модуля

Чтобы добавить модуль в гнездо или контейнер на странице, выполните следующие действия.

1. В области структуры слева или непосредственном на основном холсте выберите контейнер или область, к которой можно добавить дочерний модуль.

    > [!NOTE]
    > Конструктор модулей определяет список типов модулей, которые могут быть добавлены в конкретную ячейку модуля. Авторы шаблонов могут затем уточнить разрешенные параметры модуля, чтобы обеспечить согласованность оптимизации поисковых систем (SEO) и эффективность разработки для всех страниц, построенных на основе определенного шаблона. При добавлении модуля в ячейку диалоговое окно **Добавить модуль** автоматически фильтруется таким образом, чтобы отображались только модули, поддерживаемые в выбранном контейнере или ячейке. Список разрешенных модулей определяется шаблоном страницы или определением модуля контейнера.

1. При использовании области структуры выберите многоточие (**...**) рядом с именем модуля, а затем выберите **Добавить модуль**. Если используются элементы управления непосредственно внутри холста, выберите символ "плюс" (**+**) в пустой ячейке или рядом с выбранным модулем, а затем выберите команду **Добавить модуль**.

    > [!NOTE]
    > Если контейнер или слот не поддерживают новые дочерние модули, параметр **Добавить модуль** будет недоступен.

1. В диалоговом окне **Добавить модуль** найдите и выберите модуль, который требуется добавить на страницу.

    > [!TIP]
    > **Блок содержимого** — это правильный тип модуля для начинающих.

1. Выберите **ОК**, чтобы добавить выбранный модуль в выбранный контейнер или ячейку на странице.

### <a name="remove-a-module"></a>Удаление модуля

Чтобы удалить модуль из ячейки или контейнера на странице, выполните следующие действия.

1. В области структуры в левой части выберите кнопку с многоточием (**...**) рядом с названием удаляемого модуля, затем нажмите символ корзины. Кроме того, на главном холсте можно выбрать символ корзины на панели инструментов выбранного модуля.
1. При появлении запроса на подтверждение удаления модуля выберите **ОК**.

## <a name="move-a-module-to-a-new-position"></a>Перемещение модуля в новое место

Чтобы переместить модуль на новую позицию на странице, воспользуйтесь одним из следующих методов:

### <a name="move-a-module-using-the-outline-pane"></a>Перемещение модуля с помощью панели структуры

Чтобы переместить модуль с помощью панели структуры, выполните следующие действия.

1. Выберите и удерживайте модуль, который требуется переместить, в области структуры, а затем перетащите модуль на новое место в структуре. Синяя линия в структуре и на холсте обозначает место, где можно разместить модуль.
1. Отпустите модуль, чтобы поставить его в новую позицию.

### <a name="move-a-module-directly-within-the-canvas"></a>Перемещение модуля непосредственно внутри холста

Чтобы переместить модуль непосредственно внутри холста, выполните следующие действия.

1. Выберите модуль, который необходимо переместить, в холсте. 
1. Выберите символ стрелки вверх или вниз на панели инструментов модуля, а затем перетащите стрелку в новое положение на странице. Синяя линия на холсте и в структуре обозначает место, где можно разместить модуль. Если модуль нельзя переместить вверх или вниз, символ стрелки будет недоступен. 
1. Отпустите модуль, чтобы поставить его в новую позицию.

### <a name="move-a-module-using-the-ellipsis-menu"></a>Перемещение модуля с помощью меню многоточия

Чтобы переместить модуль с помощью меню многоточия, выполните следующие действия.

1. Выберите модуль в структуре или холсте.
1. Нажмите кнопку с многоточием (**...**) рядом с именем модуля в области структуры или на панели инструментов модуля в холсте.
1. Если модуль можно переместить вверх или вниз внутри контейнера или ячейки, можно увидеть параметры **Вверх** или **Вниз**. Выберите нужный параметр перемещения, чтобы переместить модуль вверх или вниз относительно его одноуровневых элементов.

## <a name="configure-modules"></a>Настройка модулей

Следующие процедуры описывают, как настраивать модули содержимого и контейнеры.

### <a name="configure-a-content-module"></a>Настройка модуля содержимого

Чтобы настроить модуль содержимого на странице, выполните следующие действия.

1. В области структуры слева разверните дерево и выберите модуль содержимого (например, **Блок содержимого**). Или же выберите модуль, который необходимо переместить, в основном холсте.
1. В области свойств модуля справа введите свойства для всех нужных элементов управления модуля.
1. На панели команд выберите **Сохранить**. Это также приведет к обновлению холста предварительного просмотра.

### <a name="edit-module-text-properties"></a>Изменение свойства текста модуля

Свойства текста модуля, которые недоступны только для чтения, могут быть отредактированы непосредственно на холсте.

Чтобы изменить свойства текста модуля, выполните следующие действия.

1. Выберите элемент управления "текст" в холсте и затем поместите курсор в то место, где необходимо отредактировать текст.
1. Введите свой текст.
1. Чтобы продолжить редактирование другого содержимого, выберите любое место вне текстового содержимого.

### <a name="inline-image-selection"></a>Выбор встроенного изображения

Изображения модуля, которые недоступны только для чтения, могут быть изменены непосредственно на холсте.

Чтобы выбрать новое изображение для модуля содержимого, выполните следующие действия.

1. Дважды щелкните изображение на холсте. Появится окно выбора мультимедиа.
1. Найдите и выберите новое изображение, которое необходимо использовать, а затем нажмите кнопку **ОК**. Новое изображение будет отображено на холсте.

### <a name="configure-a-container-module"></a>Настройка модуля контейнера

Чтобы настроить модуль контейнера на странице, выполните следующие действия.

1. Выберите контейнерный модуль на странице (например, модуль карусели или гибкого контейнера).
1. В области свойств справа разверните вложенные элементы управления, выбрав заголовки, и задайте необходимые значения элементов управления.
1. В области структуры в левой части выберите кнопку с многоточием рядом с названием контейнера или любых ячеек внутри контейнера, затем выберите **Добавить модуль**. Затем добавьте дочерние модули к выбранному контейнеру. Дополнительные сведения см. в разделе [Работа с модулями](#add-a-module) ранее в этой статье.
1. Если в родительском контейнере есть несколько одноуровневых дочерних модулей, можно изменить порядок их просмотра в родительском контейнере. Нажмите кнопку с многоточием для модуля, затем воспользуйтесь кнопками со стрелками вверх и вниз.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор шаблонов и макетов](templates-layouts-overview.md)

[Работа с шаблонами](work-with-templates.md)

[Работа с предустановленными макетами](work-with-layouts.md)

[Работа с фрагментами](work-with-fragments.md)

[Добавление модуля-контейнера на страницу](add-container-module.md)

[Работа с группами публикаций](publish-groups.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
