---
title: Управление атрибутами и группами атрибутов
description: В этом разделе описывается, как использовать атрибуты, чтобы предоставить способ описания продукта и его характеристик с помощью определенных пользователем полей.
author: ashishmsft
manager: AnnBe
ms.date: 04/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application pdate 5, AX 8.0
ms.openlocfilehash: 11f385514cc12733987a4855b626c067ff355b54
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023761"
---
# <a name="manage-attributes-and-attribute-groups"></a>Управление атрибутами и группами атрибутов

[!include [banner](includes/banner.md)]

*Атрибуты* предоставляют способ дальнейшего описания продукта и его характеристик через определенные пользователем поля (например, **Объем памяти**, **Емкость жесткого диска**, **Соответствие требованиям Energy Star** и так далее). Атрибуты можно связывать с различными объектами Commerce, такими как категории продуктов и каналы, и устанавливать для них значения по умолчанию. Будучи связанными с категориями продуктов или каналами, продукты наследуют их атрибуты и значения по умолчанию. Значения по умолчанию могут быть переопределены на уровне отдельного продукта, на уровне канала или в каталоге.


Например, типичный телевизионный продукт может иметь следующие атрибуты.

| Категория   | Атрибут                | Допустимые значения          | Значение по умолчанию |
|------------|--------------------------|-----------------------------|---------------|
| Теле- и видеооборудование | Марка                    | Любое действительное значение марки       | None          |
| Телевизор         | Размер экрана              | 20–80 дюймов                | None          |
|            | Разрешение по вертикали      | 480i, 720p, 1080i или 1080p | 1080p         |
|            | Частота обновления экрана      | 60 Гц, 120 Гц или 240 Гц       | 60 Гц          |
|            | Входы HDMI              | 0–10                        | 3             |
|            | Входы DVI               | 0–10                        | 1             |
|            | Композитные входы         | 0–10                        | 2             |
|            | Компонентные входы         | 0–10                        | 1             |
| ЖК        | 3D Ready                 | Да или Нет                   | Да           |
|            | 3D               | Да или Нет                   | Нет            |
| Плазменный     | Температура эксплуатации от      | 32–110 градусов              | 32            |
|            | Температура эксплуатации до        | 32–110 градусов              | 100           |
| Проекционный | Гарантия на проекционную трубку | 6, 12 или 18 месяцев         | 12;            |
|            | \# проекционных трубок   | 1–5                         | 3             |

## <a name="attributes-and-attribute-types"></a>Атрибуты и типы атрибутов

Атрибуты основываются на *типах атрибутов*. Тип атрибута определяет тип данных, которые можно ввести для определенного атрибута. Поддерживаются следующие типы атрибутов:

- **Валюта** — этот тип поддерживает значение в валюте. Его можно ограничить (то есть, он может поддерживать диапазон значений) или оставить открытым.
- **Дата и время** — этот тип поддерживает значение даты и времени. Он может быть ограниченным или открытым.
- **Десятичный** — этот тип поддерживает числовое значение, которое включают в себя десятичные разряды. Он также поддерживает единицу измерения. Он может быть ограниченным или открытым.
- **Целочисленный** — этот тип поддерживает числовое значение. Он также поддерживает единицу измерения. Он может быть ограниченным или открытым.
- **Текст** — этот тип поддерживает текстовое значение. Он также поддерживает предопределенный набор возможных значений (то есть, *перечисление*).
- **Логический** — этот тип поддерживает двоичное значение (**истина** или **ложь**).
- **Ссылка** — этот тип ссылается на другие атрибуты.

### <a name="set-up-attribute-types"></a>Настройка типов атрибутов

1. Выполните вход в клиент бэк-офиса в качестве директора по сбыту.
2. Перейдите в раздел **Управление сведениями о продукте** &gt; **Настройка** &gt; **Категории и атрибуты** &gt; **Типы атрибутов**.
3. Создайте два типа атрибутов типа **Текст**, установите для параметра **Фиксированный список** значение **Да**, затем добавьте список значений:

    - Назовите один атрибут **Форма линзы** и добавьте следующие значения: **Овальная**, **Квадратная** и **Прямоугольная**.
    - Назовите другой тип атрибута **Марка солнцезащитных очков** и добавьте следующие значения: **Ray ban**, **Aviator** и **Oakley**.

![Типы атрибутов](media/AttributeType.png)

### <a name="set-up-an-attribute"></a>Настройка атрибута

1. Выполните вход в клиент бэк-офиса в качестве директора по сбыту.
2. Перейдите в раздел **Управление сведениями о продукте** &gt; **Настройка** &gt; **Категории и атрибуты** &gt; **Атрибуты**.
3. Создать атрибут с именем **Линза**.
4. Задайте в поле **Тип атрибута** значение **Форма линзы**.

![Атрибуты](media/Attribute.png)

## <a name="attribute-metadata"></a>Метаданные атрибута

*Метаданные атрибута* позволяют выбрать параметры для указания поведения атрибутов для каждого продукта. Например, можно указать, являются ли атрибуты обязательными, можно ли их использовать для поиска и в качестве фильтра.

Для продуктов можно переопределить параметры метаданных атрибута на уровне канала. Эта возможность обсуждается далее в этом разделе.

Как вы, возможно, заметили, страница **Атрибуты** включает параметры, которые связаны с метаданными атрибутов. В разделе **Метаданные атрибута для POS** один параметр с именем **Возможно уточнение** влияет на поведение значений атрибутов в POS или способ, которым система обрабатывает эти значения атрибутов. Только атрибуты, для которых вы можете установить для параметра **Возможно уточнение** значение **Да**, будут отображаться для уточнения или фильтрации продуктов в POS.

Вот остальные параметры метаданных атрибутов на странице **Атрибуты**:

- Возможность поиска
- Возможно извлечение
- Возможен запрос
- Возможность сортировки
- Разрешить ввод нескольких значений
- Игнорировать регистр и форматирование
- Полное совпадение

Эти параметры были изначально предназначены для улучшения функции поиска для витрины интернет-магазина. Хотя Commerce не включает готовой витрины интернет-магазина, он включает пакета средств разработки eCommerce Publishing Software Development Kit (пакет SDK). Клиенты могут использовать этот пакет SDK для размещения продуктов в индексе поиска по своему выбору. Хотя данные о продукции импортируются, клиенты по-прежнему смогут отличать данные, по которым возможен поиск, данные, которые можно запрашивать, и т. д. Таким образом, они могут создать оптимальный индекс, обеспечивающий индексацию только тех атрибутов, которые, *по их мнению*, должны быть проиндексированы.

Сведения о назначении этих оставшихся параметров см. в разделе [Обзор схемы поиска в SharePoint Server 2013](https://technet.microsoft.com/library/jj219669.aspx).

## <a name="filter-settings-for-attributes"></a>Настройки фильтра для атрибутов

Настройки фильтра для атрибутов позволяют определить, как фильтры для атрибутов будут показаны в POS-терминале. Для доступа к настройкам фильтра для атрибута на странице **Атрибуты** выберите атрибут, затем выберите в области действий пункт **Настройки фильтра**.

Страница **Параметры отображения фильтра** включает следующие поля:

- **Имя** — по умолчанию это поле имеет значение имени атрибута. Однако это значение можно изменить.
- **Параметр отображения** — доступны следующие параметры:

    - **Одно значение** — этот параметр доступен для следующих типов атрибутов: **Логический**, **Валюта**, **Десятичный**, **Целочисленный** и **Текст**. Этот параметр позволяет выбирать одно значение для этих атрибутов в клиенте для уточнения.
    - **Несколько значений** — этот параметр доступен для следующих типов атрибутов: **Валюта**, **Десятичный**, **Целочисленный** и **Текст**. Этот параметр позволяет выбирать несколько значений для этого атрибута в клиенте для уточнения.

- **Управление отображением** — доступны следующие параметры:

    - **Список** — этот параметр доступен для всех типов атрибутов.
    - **Диапазон** — этот параметр доступен для следующих типов атрибутов: **Валюта**, **Десятичный** и **Целочисленный**.
    - **Ползунок** — этот параметр доступен для следующих типов атрибутов: **Валюта**, **Десятичный** и **Целочисленный**.
    - **Ползунок с панелями** — этот параметр доступен для следующих типов атрибутов: **Валюта**, **Десятичный** и **Целочисленный**.

- **Пороговое значение** — этот параметр является обязательным, если выбрано значение **Диапазон** как тип отображения элемента управления. Можно определять значения с помощью точки с запятой (;) в качестве разделителя.

    Например, для такого фильтра, как **Объем сумки**, пороговое значение может быть **10; 20; 50; 100; 200; 500; 1000; 5000**. В этом случае на POS-терминале будут показаны следующие диапазоны. Любые диапазоны, в которых в наборе результатов отсутствуют продукты, будут отображаться серым цветом.

    - Меньше чем 10
    - 10 – 20
    - 20 – 50
    - 50 – 100
    - 100 – 200
    - 200 – 500
    - 500 и более

![Настройки фильтра атрибутов](media/AttributeFilterSettings.PNG)

## <a name="attribute-groups"></a>Группы атрибутов

После того как атрибуты определены, они могут быть назначены группам атрибутов. *Группа атрибутов* используется для группирования отдельных атрибутов компонентов или субкомпонентов в модели конфигурации продукта. Атрибут может быть включен не в одну, а в несколько групп атрибутов. Группы атрибутов могут помочь пользователям настраивать продукты, так как разные варианты выбора располагаются в конкретном контексте. Группы атрибутов можно назначить категориям или каналам.

Можно также задать значения по умолчанию для атрибутов, включенных в группу атрибутов. Например, можно добавить атрибут для цвета в группу атрибутов и выбрать значение **Синий** в качестве значения атрибута по умолчанию. В этом случае при добавлении группы атрибутов к продукту торговли, который включает цвет как один из его атрибутов, **Синий** отображается как цвет по умолчанию для этого продукта.

![Группы атрибутов](media/AttributeGroup.png)

### <a name="create-an-attribute-group"></a>Создание группы атрибутов

1. Выполните вход в клиент бэк-офиса в качестве директора по сбыту.
2. Перейдите в раздел **Управление сведениями о продукте** &gt; **Настройка** &gt; **Категории и атрибуты** &gt; **Группы атрибутов**.
3. Создайте группу атрибутов с именем **Модные солнцезащитные очки**.
4. Добавьте следующие атрибуты: **Форма линзы** и **Марка солнцезащитных очков**.

### <a name="assign-attribute-groups-to-categories"></a>Назначение групп атрибутов категориям

Одна или несколько групп атрибутов могут быть связаны с узлами категорий в следующих типах иерархий категорий: иерархия продукции Commerce, иерархия навигационных категорий канала и иерархия категорий дополнительной продукции. Затем при классификации продуктов они наследуют атрибуты, входящие в группы атрибутов.

![Иерархия продукции — группы атрибутов продукта](media/AGRetailProdHierarchy.PNG)

Выполните следующие действия, чтобы назначить группы атрибутов категориям в иерархии продукции Commerce.

1. Выполните вход в клиент бэк-офиса в качестве директора по сбыту.
2. Выберите **Retail и Commerce** &gt; **Управление категориями и продуктами** &gt; **Иерархия продуктов Commerce**.
3. Выберите **Иерархия навигации по модным продуктам**.
4. В разделе **Мужская одежда**, выберите категорию **Брюки**, а затем на экспресс-вкладке **Группы атрибутов продукта** добавьте группу атрибутов с именем **Мужской ремень**.
5. Выберите категорию **Модные солнцезащитные очки** и проверьте новые атрибуты в группе атрибутов **Модные солнцезащитные очки**, выбрав **Просмотр атрибутов**.

    В группе атрибутов должны отображаться новые атрибуты **Форма линз** и **Марка солнцезащитных очков**.

6. В разделе **Мужская одежда** выберите категорию **Брюки** и проверьте группу атрибутов **Мужской ремень**, выбрав пункт **Просмотр атрибутов**.

    В группе атрибутов должны отображаться атрибуты **Марка мужского ремня**, **Материал ремня** и **Размер ремня**.

> [!NOTE]
> Эта процедура может также использоваться для назначения групп атрибутов категориям в иерархии навигационных категорий канала и иерархии дополнительных категорий продукции. На шаге 2 используйте следующие пути перехода:
>
> - Retail и Commerce &gt; Управление категориями и продуктами &gt; Навигационные категории каналов
> - Retail и Commerce &gt; Управление категориями и продуктами &gt; Дополнительные категории продуктов

### <a name="assign-attribute-groups-to-stores"></a>Назначение групп атрибутов магазинам

С одним или несколькими магазинами в иерархии категорий магазинов можно связать одну или несколько групп атрибутов. Затем ,после обогащения продуктов путем добавления конкретных магазинов, продукты наследуют атрибуты, входящие в группы атрибутов.

1. Выполните вход в клиент бэк-офиса в качестве директора по сбыту.
2. Перейдите в раздел **Retail и Commerce** &gt; **Настройка канала** &gt; **Категории каналов и атрибуты продуктов**.
3. Назначьте группы атрибутов каналу "Хьюстон":

    1. Выберите канал **Хьюстон**.
    2. На экспресс-вкладке **Группа атрибутов** выберите **Добавить**, затем в поле **Имя** выберите **SharePointProvisionedProductAttributeGroup**.
    3. Снова выберите **Добавить**, затем в поле **Имя** выберите **Мужской ремень**.
    4. Снова выберите **Добавить**, затем в поле **Имя** выберите **Модные солнцезащитные очки**.

        > [!NOTE]
        > Параметр позволяет указать, что этот канал должен наследовать группы атрибутов из своего родительского канала в иерархии. Если для параметра **Наследовать** задано значение **Да**, дочерний узел канала наследует все группы атрибутов и все атрибуты из этих групп атрибутов.

4. Включите атрибуты, чтобы они были доступны в канале "Хьюстон":

    1. В области действий выберите **Задать метаданные атрибута**.
    2. Выберите узел категории **Мода**, затем на экспресс-вкладке **Атрибуты продуктов канала** выберите **Включить атрибут** для каждого атрибута.
    3. Выберите узел категории **Модные аксессуары**, затем выберите категорию **Модные солнцезащитные очки**, и затем на экспресс-вкладке **Атрибуты продуктов канала** выберите **Включить атрибут** для каждого атрибута.
    4. Выберите узел категории **Мужская одежда**, затем выберите категорию **Брюки**, и затем на экспресс-вкладке **Атрибуты продуктов канала** выберите **Включить атрибут** для каждого атрибута.

![Категории каналов и атрибуты продуктов — группы атрибутов](media/CCPAttrGrp.png)

## <a name="overriding-attribute-values"></a>Переопределение значений атрибутов

Значения по умолчанию атрибутов можно переопределять для отдельных продуктов на уровне продукта. Значения по умолчанию можно также переопределять для отдельных продуктов в конкретных каталогах, предназначенных для конкретных каналов.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Переопределение значений атрибутов для конкретного продукта

1. Выполните вход в клиент бэк-офиса в качестве директора по сбыту.
2. Выберите **Retail и Commerce** &gt; **Управление категориями и продуктами** &gt; **Используемые продукты по категориям**.
3. Выберите узел категории **Мода** &gt; **Модные аксессуары** &gt; **Модные солнцезащитные очки**.
4. Выберите требуемый продукт в сетке. Затем в область действий на вкладке **Продукт** в группе **Настройка** выберите **Атрибуты продукта**.
5. Выберите атрибут в левой области, затем обновите его значение в правой области.

![Страница сведений о продукте — группы атрибутов продукта](media/ProdDetailsProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-catalog"></a>Переопределение значений атрибутов продуктов в каталоге

1. Выполните вход в клиент бэк-офиса в качестве директора по сбыту.
2. Выберите **Retail и Commerce** &gt; **Управление каталогами** &gt; **Все каталоги**.
3. Выберите каталог **Fabrikam Base Catalog**.
4. Выберите узел категории **Мода** &gt; **Модные аксессуары** &gt; **Модные солнцезащитные очки**.
5. На экспресс-вкладке **Продукты** выберите требуемый продукт, затем выберите **Атрибуты** над сеткой продукции.
6. В следующих экспресс-вкладках обновите значения обязательных атрибутов:

    - СМИ общих продуктов
    - Общие атрибуты продуктов
    - Канал СМИ
    - Атрибуты продуктов канала

    > [!NOTE]
    > Если совместно используемые носители продукта и атрибуты продукта создаются, они применяются для всех продуктов.

![Группы атрибутов продукта из каталога](media/CatalogProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-channel"></a>Переопределение значений атрибутов продуктов в канале

1. Выполните вход в клиент бэк-офиса в качестве директора по сбыту.
2. Перейдите в раздел **Retail и Commerce** &gt; **Настройка канала** &gt; **Категории каналов и атрибуты продуктов**.
3. Выберите канал **Хьюстон**.
4. На экспресс-вкладке **Продукты** выберите требуемый продукт, затем выберите **Атрибуты** над сеткой продукции.

    > [!NOTE]
    > Если никакие продукты не доступны, добавьте продукты, выбрав **Добавить** на экспресс-вкладке **Продукты**, затем выбрав необходимые продукты в диалоговом окне **Добавить продукты**.

5. В следующих экспресс-вкладках обновите значения обязательных атрибутов:

    - СМИ общих продуктов
    - Общие атрибуты продуктов
    - Канал СМИ
    - Атрибуты продуктов канала

    > [!NOTE]
    > Если совместно используемые носители продукта и атрибуты продукта создаются, они применяются для всех продуктов.