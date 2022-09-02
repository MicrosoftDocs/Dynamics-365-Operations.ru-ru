---
title: Модули сравнения продуктов
description: В этой статье описываются модули сравнения продуктов и способы их реализации, чтобы клиенты могли сравнивать продукты на веб-сайтах электронной коммерции Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 08/09/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: ced471dd7e3e4c3e9be938b295edaad626a890a3
ms.sourcegitcommit: 92c4506be7dc14078e3c4f1d182edd895d64ffe0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/10/2022
ms.locfileid: "9247658"
---
# <a name="product-comparison-modules"></a>Модули сравнения продуктов

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

В этой статье описываются модули сравнения продуктов и способы их реализации, чтобы клиенты могли сравнивать продукты на веб-сайтах электронной коммерции Microsoft Dynamics 365 Commerce.

> [!NOTE]
> Модули сравнения продуктов и кнопки сравнения продуктов доступны Dynamics 365 Commerce версии 10.0.29. Они могут использоваться как на веб-сайтах «бизнес-потребитель» (B2C), так и на веб-сайтах «бизнес-бизнес» (B2B).

Функция сравнения продуктов позволяет покупателям сравнить сведения о продуктах на странице «Сравнение продуктов», помогая им принимать более взвешенное решение о покупке. Эта функциональность настраивается в конструкторе сайтов Commerce, используя модуль сравнение продукции. На страницах списка продуктов (PLP), таких как результаты категорий, результаты поиска и страницы коллекций продуктов, можно настроить кнопку для сравнения продукции, которая позволяет покупателям добавлять продукты на панель сравнения. Эта функциональность настраивается в конструкторе сайтов с помощью модуля с кнопкой "Сравнение продуктов", который работает как [модуль быстрого просмотра](quick-view-module.md).

Когда пользователи сайта добавляют продукты для сравнения, выбирая их на плитках продуктов, в нижней части страницы появится панель сравнения на панели сравнения отображаются продукты, которые в настоящее время сравниваются покупателем, а также краткий обзор продуктов. Пользователи сайта также могут добавлять продукты из страниц сведений о продуктах (PDP), а также добавлять отдельные варианты продуктов для сравнения с шаблонами продуктов.

После того как клиенты добавляют несколько продуктов на панель сравнения, они могут выбрать **Сравнение** для перенаправления на страницу сравнения продуктов. Страница сравнения продуктов показывает сведения о продукте для каждого выбранного продукта, чтобы клиенты могли сравнивать изображения, цены, аналитики продуктов (размер, стиль и цвет), статистическую информацию с оценками и другие атрибуты продукта.

На следующем рисунке показаны примеры кнопки сравнение продуктов, кнопки удалить из сравнения, панели сравнения и страницы «Сравнение продуктов».

![Обзор сравнения продуктов с кнопкой сравнения продуктов, кнопкой удаления из сравнения, панелью сравнения и страницей «Сравнение продуктов».](./media/Product-Comparison-Overview.png)

> [!NOTE]
> - Страница «Сравнение продуктов» сравнивает набор свойств продукта по умолчанию и все атрибуты, которые можно просмотреть на странице PDP для конкретного продукта.
> - Такие свойства, как режим доставки, запасы в наличии и единица измерения нельзя просмотреть на странице «Сравнение продуктов».
> - Клиенты могут добавлять продукты из разных категорий на панель сравнения при условии, что продукты из одного каталога
> - Функция сравнения продуктов в настоящее время ограничивается сравнением продуктов в отдельном каталоге. Пользователи сайта не могут выполнять сравнения между каталогами.
> - Флажок свойства **Модуль визуализации на стороне клиента** должен быть снят для всех модулей сравнения продуктов.
> - Необходимо убедиться, что кэширование на уровне страниц отключено для всех страниц, на которых используется модуль сравнения продуктов. Эти страницы включают в себя PDP, PLP и страницы сравнения продуктов. Дополнительные сведения см. в разделе [Настройка кэширования страниц](e-commerce-extensibility/page-caching.md).

Следующая иллюстрация показывает пример страницы «Сравнение продуктов».

![Страница «Сравнение продуктов».](./media/Product-Comparison-Page.png)

## <a name="add-the-product-comparison-module-to-a-new-product-comparison-page"></a>Добавление модуля сравнения продуктов на новую страницу сравнения продуктов

Можно создать специальную страницу сравнения продуктов, добавив модуль сравнения продуктов в тело страницы. В дополнение к тому, чтобы клиенты могли сравнивать информацию о продуктах по разным продуктам, можно настроить модуль сравнения продукции, чтобы предоставить клиентам возможность быстро выполнить покупку после сравнения продуктов. Модуль сравнения продуктов также содержит ячейку **Пустое сравнение**, позволяющую добавить модуль блока содержимого, описывающий пустое состояние (например, «Сравнение продуктов пустое»).

Чтобы добавить модуль сравнения продуктов на новую страницу «Сравнение продуктов», выполните следующие действия.

1. Перейдите к разделу **Страницы**, выберите **Создать**, чтобы создать страницу.
1. В диалоговом окне **Создать страницу** в разделе **Имя страницы** введите соответствующее название страницы (например, **Сравнение продуктов**), а затем выберите **Далее**.
1. В диалоговом окне **Выбор шаблона** выберите подходящий шаблон (например, шаблон, что используется страницей категории по умолчанию), а затем нажмите **Далее**.
1. В области **Выбор макета** выберите макет страницы (например, **Гибкий макет**), а затем нажмите кнопку **Далее**.
1. В области **Проверка и завершение** проверьте конфигурацию страницы. Если необходимо изменить сведения о странице, выберите **Назад**. Если сведения на странице верны, выберите **Создать страницу**.
1. В ячейке **Основной** выберите многоточие (**...**), затем выберите **Добавить модуль**.
1. В диалоговом окне **Выбрать модуль** выберите модуль **Контейнер**, затем выберите **ОК**.
1. В ячейке **Контейнер** выберите многоточие (**...**), затем выберите **Добавить модуль**.
1. В диалоговом окне **Выбор модуля** выберите модуль **Сравнение продуктов**, а затем выберите **ОК**.
1. В ячейке **Кнопка быстрого просмотра** выберите кнопку с многоточием (**...**), а затем выберите **Добавить модуль**.
1. В диалоговом окне **Выбрать модуль** выберите модуль **Быстрый просмотр продуктов**, а затем выберите **ОК**.
1. В области свойств справа задайте свойства для модуля **Быстрый просмотр продукта**.
1. В ячейке **Пустое сравнение** выберите многоточие (**...**), а затем выберите **Добавить модуль**.
1. В диалоговом окне **Выбор модуля** выберите модуль **Блок содержимого**, затем выберите **ОК**.
1. В области свойств справа задайте свойства для модуля **Блок содержимого**. 
1. Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.
1. Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.

На следующем рисунке показан пример пустой страницы сравнения в конструкторе сайтов.

![Модуль сравнения продуктов.](./media/Product-comparison-module.png)

## <a name="add-a-product-comparison-button-to-product-tiles-on-search-and-category-results-pages"></a>Добавление кнопки сравнения продуктов в плитки продуктов на страницах результатов поиска и категорий

Кнопка сравнения продуктов позволяет пользователям быстро добавлять продукт на панель сравнения при просмотре продуктов на странице списка. Пользователь может добавить один или несколько продуктов на панель сравнения со страницы списка без перехода к PDP.

Кнопка сравнения продуктов поддерживается модулями коллекции продуктов, результатов поиска и окна покупки PDP.

Добавление кнопки сравнения продуктов в плитки продуктов на страницах результатов поиска и категорий выполните следующие действия.

1. В конструкторе сайтов перейдите в раздел **Страницы** и откройте страницу «Категория», на которую требуется добавить кнопку сравнения продуктов.
1. В ячейке **Основной** выберите многоточие (**...**), затем выберите **Добавить модуль**.
1. В диалоговом окне **Выбрать модуль** выберите модуль **Результаты поиска**, затем выберите **ОК**.
1. В ячейке **Кнопка сравнения продуктов** модуля **Результаты поиска** выберите кнопку с многоточием (**...**), а затем выберите **Добавить модуль**.
1. В диалоговом окне **Выбор модуля** выберите модуль **Кнопка сравнения продуктов**, а затем выберите **ОК**.
1. В области свойств справа задайте свойства для модуля **Кнопка сравнения продуктов**.
1. Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.
1. Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.

## <a name="specify-the-maximum-number-of-products-to-show-in-the-comparison-tray"></a>Задание максимального числа продуктов для отображения на панели сравнения

Можно указать максимальное число продуктов для отображения на панели сравнения, перейдя в раздел **Настройки сайта \> Расширения** в конструкторе сайтов. Можно настроить отдельные максимальные ограничения для представлений настольных компьютерах и мобильных устройствах/планшетах. По умолчанию никакие ограничения не будут применяться, если не будет определено максимальное ограничение.

> [!NOTE]
> Для оптимального просмотра веб-страницы в браузере рекомендуется установить максимальное число продуктов на панели сравнения равным **2** для окна просмотра мобильных устройств и **4** для окна просмотра настольных компьютеров, чтобы уменьшить объем горизонтальной прокрутки.

Чтобы задать максимальное число продуктов на панели сравнения, выполните следующие действия.

1. В конструкторе сайтов перейдите к разделу **Параметры сайта \> Расширения**.
1. Для свойства **Продукты в ограничении сравнения — настольные компьютеры** введите максимальное число продуктов, которое должно отображаться на панели сравнения для окон просмотра настольных компьютеров.
1. Для свойства **Продукты в ограничении сравнения — мобильные устройства и планшеты** введите максимальное число продуктов, которое должно отображаться на панели сравнения для окон просмотра мобильных устройств и планшетов.
1. На панели команд выберите **Сохранить и опубликовать**.

![Параметры сайта для ограничения продуктов на панели сравнения.](./media/Site-settings-to-limit-products-in-comparison-tray.png)