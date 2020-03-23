---
title: Изменение существующей страницы сайта
description: В этом разделе описывается, как изменить существующую страницу сайта в Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c393fc143214c2c7c7ddad9a77e273e1e53e34ac
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003449"
---
# <a name="modify-an-existing-site-page"></a>Изменение существующей страницы сайта


[!include [banner](includes/banner.md)]

В этом разделе описывается, как изменить существующую страницу сайта в Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Обзор

Когда необходимо изменить страницу, первым шагом является ее открытие в редакторе страниц. Перейдите на сайт, содержащий страницу, затем в списке страниц найдите нужную страницу. Если не удается найти страницу, можно воспользоваться функциями расширенного поиска инструмента разработки. Либо введите точное имя страницы, либо введите первые несколько букв, а затем звездочку (\*). Отображается отфильтрованный список страниц. С помощью этого списка можно найти нужную страницу. После того, как вы нашли правильную страницу, выберите имя страницы, чтобы открыть страницу в редакторе страниц.

> [!TIP]
> Если страница отображается в инспекторе страниц, ее можно выбрать и извлечь перед открытием в редакторе страниц. Таким образом можно извлекать несколько страниц одновременно.

После открытия страницы в редакторе страниц необходимо убедиться, что она извлечена вами. Панель команд в инструменте разработки является динамической, контекстно-зависимой и с учетом состояния. Таким образом отображаются только те действия, которые можно выполнить на странице в данный момент. Например, если страница не извлечена вами, кнопки **Сохранить** и **Вернуть** не появляются на панели команд. Состояние страницы также отображается в правой части окна.

Если страница еще не извлечена, выберите **Извлечь** на панели команд. Панель команд изменяется, отражая новое состояние страницы. Также вы получаете уведомление о том, что страница была извлечена вами.

Следующий шаг состоит в выполнении фактических изменений. Часто для поиска и выбора модуля, который необходимо изменить, используется дерево структуры страниц в левой части, а затем вносятся изменения на панели свойств справа. 

Однако в некоторых случаях изменения могут включать добавление или удаление модулей или фрагментов. Чтобы добавить фрагмент или модуль, используйте деревом структуры страниц, чтобы найти гнездо, в которое необходимо добавить модуль или фрагмент, затем нажмите кнопку с многоточием (**...**) для этого гнезда. Появится меню, содержащее команды для добавления модуля или фрагмента. Чтобы удалить модуль или фрагмент, найдите и выберите его в дереве структуры страницы, выберите кнопку с многоточием, затем выберите команду для удаления модуля или фрагмента.

> [!TIP]
> Кроме того, можно просматривать и изменять свойства любого модуля, который отображается в разделе предварительного просмотра "что видите, то и получите" (WYSIWYG), выбрав его непосредственно.

После завершения внесения изменений и предварительного просмотра их результатов следует вернуть страницу, выбрав **Вернуть** на панели команд. 

Чтобы немедленно опубликовать изменения, выберите **Опубликовать** на панели команд. Последняя возвращенная версия измененной страницы публикуется и становится доступной внешним пользователям, просматривающим сайт. 

## <a name="example-change-the-video-on-the-home-page"></a>Пример: изменение видео на домашней странице

В следующем примере показано, как изменить домашнюю страницу, изменив видеозапись, которая отображается в модуле видеопроигрывателя.

1. В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).
1. В области переходов слева выберите **Страницы**.
1. Найдите и выберите домашнюю страницу для ее открытия в редакторе страниц.
1. На панели команд выберите **Извлечь**.
1. В структуре страницы выберите слот **Главный**.
1. В слоте **Главный** разверните все модули гибкого контейнера.
1. Найдите и выберите модуль видеопроигрывателя.
1. В области свойств справа выберите свойство **видео**. Отображается средство выбора активов.
1. В средстве выбора активов выберите доступный видеоактив или выберите команду **Отправить новый актив**, чтобы отправить новый видеоактив.
1. Нажмите **ОК**.
1. Выберите **Сохранить**, затем выберите **Вернуть**.
1. В поле **Комментарии** введите **Изменена видеозапись**, затем выберите **ОК**.
1. Выберите **Предварительный просмотр** для предварительного просмотра обновленной страницы. По завершении закройте вкладку предварительного просмотра, чтобы вернуться к инструменту разработки.
1. Выберите **Опубликовать**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Добавление новой страницы сайта](add-new-page.md)

[Выбор макета страницы](select-page-layouts.md)

[Управление метаданными для поисковой оптимизации](manage-seo-metadata.md)

[Сохранение, предварительный просмотр и публикация страницы](save-preview-publish-page.md)

[Расширение возможностей страницы продукта](enrich-product-page.md)

[Расширение возможностей целевой страницы категории](enrich-category-page.md)

[Проверка специальных возможностей контента страницы](verify-accessibility.md)