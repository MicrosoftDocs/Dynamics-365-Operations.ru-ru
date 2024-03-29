---
title: Визуализация исходящей рабочей нагрузки
description: В этой статье представлена информация об визуализации исходящей рабочей нагрузке. Эта функция позволяет менеджерам склада и супервизорам создавать пользовательские диаграммы рабочей нагрузки, которые могут использоваться для отслеживания хода текущей работы и количества остатков. Менеджеры склада могут создавать несколько представлений и настраивать автоматическое обновление по мере необходимости.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-08-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 78d0d81095bb52a314936dd7590a5690d94ecb15
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334426"
---
# <a name="outbound-workload-visualization"></a>Визуализация исходящей рабочей нагрузки

[!include [banner](../includes/banner.md)]

Расширенные возможности настройки, доступные на странице **Визуализация исходящей рабочей нагрузки**, позволяют менеджерам и руководителям склада создавать пользовательские диаграммы рабочей нагрузки, которые могут использоваться для отслеживания хода текущей работы и оставшегося количества. Менеджеры склада могут создавать несколько представлений и настраивать автоматическое обновление по мере необходимости. Визуализации исходящих рабочих нагрузок подходят для отображения на страницах производительности склада.

Эта функция может использоваться для отслеживания хода работы по комплектации. Эта функция интегрирована с модулем управления персоналом, и если управление персоналом настроено, визуализации исходящих рабочих нагрузок могут показать расчетное количество часов, остающихся для операции комплектации, которая отображается (отфильтрована).

## <a name="turn-the-outbound-workload-visualization-feature-on-or-off"></a>Включение или отключение функции визуализации исходящей рабочей нагрузки

Чтобы использовать эту функцию, ее необходимо включить для системы. В Supply Chain Management версии 10.0.25 эта функция включена по умолчанию. В Supply Chain Management версии 10.0.29 эта функция обязательна и не может быть отключена. При запуске версии, более старой, чем 10.0.29, администраторы могут включать или выключать эту функцию путем поиска функции *Визуализация исходящей рабочей нагрузки* в рабочей области [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="set-up-outbound-workload-visualizations"></a>Настройка визуализаций исходящей рабочей нагрузки

Для настройки визуализаций необходимо создать коллекцию фильтров (представлений) и сконструировать каждый фильтр, чтобы показать различный тип анализа. Для создания фильтров используется страница **Настройка фильтров**.

Чтобы настроить визуализацию исходящей рабочей нагрузки, выполните следующие действия.

1. Перейдите в раздел **Управление складом \> Отчеты по мониторингу склада \> Визуализация исходящей рабочей нагрузки**.

    Отображается страница **Визуализация исходящей рабочей нагрузки**. После создания некоторых фильтров на этой странице будет отображаться визуализация. Может быть создано любое число фильтров. Все созданные фильтры будут сохранены под учетной записью пользователя, чтобы их можно было использовать позднее. Другими словами, каждый пользователь будет иметь свой собственный набор фильтров, которые он создал. Эти фильтры не будут использоваться совместно с другими пользователями.

1. На странице **Визуализация исходящей загрузки** в области действий на вкладке **Фильтры** выберите **Настройка фильтров**.
1. На странице **Настройка фильтров** на панели операций выберите **Создать**, чтобы добавить фильтр, затем задайте для него следующие поля:

    - **Таблица группы оси X** — выберите таблицу, содержащую поле, которое должно использоваться для группировки значений на оси X.
    - **Поле группы оси X** — из полей таблицы, выбранной в поле **Таблица группы оси X**, выберите поле, которое должно использоваться для группировки значений оси X.
    - **Таблица значений оси X** — выберите таблицу, содержащую поле, которое должно использоваться для дальнейшего анализа групп.
    - **Поле значений оси X** — из полей таблицы, выбранной в поле **Таблица значений оси X**, выберите поле, которое предоставляет значения, которые должны анализироваться для каждой группы.
    - **Автообновление** — выберите, следует ли автоматически обновлять визуализацию.
    - **Интервал обновления (в минутах)** — введите число минут между автоматическими обновлениями.
    - **Уровень отображения** — выберите, следует ли отображать на диаграмме открытые строки или открытые счетчики заголовков.
    - **Тип комплектации** — если для поля **Уровень отображения** задано значение _Открытые строки_, следует указать, должно ли количество открытых рабочих строк в диаграмме включать начальные комплектации, промежуточные комплектации или начальные и промежуточные комплектации.
    - **Сайт** — выберите сайт, для которого необходимо загрузить диаграмму.
    - **Склад** — выберите склад, для которого необходимо загрузить диаграмму.
    - **Дни для включения** — введите число дней в прошлом, для которых должна быть создана диаграмма.
    - **Тип заказа на работу** — выберите типы исходящих заказов на работу, по которым выполняется фильтрация.

    ![Страница настройки фильтров.](media/work-viz-filters-1.png "Страница настройки фильтров")

1. Закройте страницу **Настройка фильтров**, чтобы вернуться на страницу **Визуализация исходящей рабочей нагрузки**.

    На странице **Визуализация исходящей рабочей нагрузки** отображаются данные на основе новых настроек фильтра. Ваш новый фильтр теперь доступен и выбран в поле **Фильтр**. В верхней части диаграммы доступны следующие поля:

    - **Фильтр** — в этом поле представлены все созданные ранее вами фильтры. Выбор фильтра для просмотра его данных в диаграмме.
    - **Последнее обновление** — в этом поле отображаются дата и время последнего обновления данных в диаграмме.
    - **Оценочное/фактическое время** — если в системе настроены трудовые стандарты, установите для этого параметра значение *Да*, чтобы отобразить накопленное оценочное время комплектации в верхней части каждого столбца диаграммы. Если вы не используете трудовые стандарты, этот параметр недоступен.

    ![Пример визуализации.](media/work-viz-chart.png "Пример визуализации")

1. Выберите любой столбец в диаграмме, чтобы просмотреть сведения о связанной рабочей строке.

    ![Сведения строки работы.](media/work-viz-work-details.png "Сведения строки работы")

## <a name="example-outbound-workload-visualization-for-zones"></a>Пример. Визуализация исходящей рабочей нагрузки для зон

В данном примере требуется настроить визуализацию, отображающую строки работ для каждой зоны, и статус каждой из строк работ (_Открыто_, _Закрыто_ или _Отменено_). В этом случае можно настроить фильтр со следующими настройками:

- **Имя фильтра** — введите имя для этого фильтра (например, _Зона и состояние работы_).
- **Описание** — введите краткое описание для этого фильтра (например, _Зона и состояние работы_).
- **Таблица группы оси X** — выберите _Местоположения._
- **Группа оси X** — выберите _Код зоны_.
- **Таблица значений оси X** — выберите _Работа_, так как необходимо просмотреть работу по каждой зоне.
- **Поле значений оси X** — выберите _Состояние работы_, так как необходимо просмотреть состояние работы.
- **Автообновление** — выберите, следует ли автоматически обновлять визуализацию.
- **Тип комплектации** — выберите _Начальные комплектации и промежуточные комплектации_, так как необходимо включить как начальные комплектации, так и комплектации из промежуточных местоположений. Другими словами, вы с целом хотите включить все имеющиеся у вас строки работы комплектации.
- **Уровень отображения** — выберите _Открытые строки_, поскольку требуется просмотреть информацию по каждой строке, а не по заголовку работы.

На следующем рисунке показан пример получающейся диаграммы.

![Визуализация зон и состояния работы.](media/work-viz-chart.png "Визуализация зон и состояния работы")

На этой диаграмме показаны две зоны с именами **ЭТАЖ** и **СБОРНАЯ**, плюс зона с именем **Пусто**. Зона **Пусто** представляет все строки работ, не являющиеся участниками каких-либо зон. Диаграмма всегда показывает все несвязанные отфильтрованные данные как **Пусто**, чтобы предоставить как можно большую видимость. В зоне **ЭТАЖ** на диаграмме показаны три закрытые строки и четыре открытые строки. В зоне **СБОРНАЯ** на диаграмме показаны четыре закрытые строки, одна открытая строка и 24 отмененные строки. Наконец, на диаграмме показаны восемь закрытых строк, не являющихся частью какой-либо зоны и, следовательно, они отображаются как **Пустые**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]