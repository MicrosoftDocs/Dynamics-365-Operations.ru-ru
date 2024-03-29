---
title: Терминология учета затрат
description: В этой статье определяются ключевые термины, используемые в модуле "Учет затрат".
author: aprilolson
ms.date: 08/31/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostAccountingLedger
audience: Application User
ms.reviewer: twheeloc
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5827ad66b9eedaab88dbda97c1ebbcd15f6d9ac8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881943"
---
# <a name="cost-accounting-terminology"></a>Терминология учета затрат

[!include [banner](../includes/banner.md)]

В этой статье определяются ключевые термины, используемые в модуле "Учет затрат".

**База распределения**

База распределения используется для количественного измерения операций, например используемого машинного времени, потребленных киловатт-часов или занимаемой площади. Она используется в качестве базы для распределения затрат между одним или несколькими объектами затрат.

**Учет затрат**

Учет затрат позволяет вам собирать данные из различных источников, таких как ГК, вспомогательные книги, бюджеты и статистическая информация. Затем вы можете анализировать, суммировать и оценивать данные по затратам, чтобы руководство могло принимать оптимальные решения для обновления цен, бюджетов, управления затратами и т. д. Исходные данные, которые используются для анализа затрат, обрабатываются независимо в учете затрат. Поэтому обновления в учете затрат не влияют на исходные данные. Однако при сборе данных по затратам из различных источников и особенно при импорте счетов ГК из главной книги в качестве элементов затрат, возникает дублирование данных, поскольку одни и те же данные существуют как в главной книге, так и в модуле учета затрат. Это дублирование необходимо, поскольку вы используете финансовое управление для внешней отчетности, а учет затрат — для внутренней отчетности.

**Книга учета затрат**

Определяется календарем, валютой и аналитикой элементов затрат; управляет процессы и политики для измерения затрат. 

**Запись себестоимости**

Записи цены являются результатом перемещения через соединители данных из записей ГК, распределений затрат и разнесенных записей затрат в журналах затрат.

**Объект затрат**

Объект любого типа, выбранный для управления затратами. Затраты или выручка разносятся либо непосредственно, либо распределяются по объектам затрат. Некоторые типичные объекты затрат:

-  Товары
-  Проекты
-  Отделы
-  Места возникновения затрат

Руководство использует объекты затраты для определения количественной меры затрат, но также и для проведения анализа прибыльности.

**Элемент затрат**

Используется в качестве функции для отслеживания и классификации затрат. Имеется два типа элементов затрат: первичные и вторичные.

Элементы первичных затрат представляют поток затрат из финансового учета в модуль "Учет затрат". Структура элемента затрат обычно соответствует структуре счета прибылей и убытков в главной книге, где элемент затрат может соответствовать счету ГК. Не все счета ГК необходимо представлять в виде элементов затрат, в зависимости от требований компании. 

Элементы вторичных затрат представляют внутренний поток затрат, поскольку эти затраты используются только в модуле "Учет затрат". Они используются в правилах свертки затрат для агрегирования затрат в содержательные интервалы, используемые при расчете накладных расходов. 

**Классификация затрат**

Классификация затрат группирует затраты в соответствии с их общим характеристикам. Например, затраты могут быть сгруппированы по элементами, возможности отслеживания и поведению.

-   **По элементам** — материалы, труд и накладные расходы.
-   **По возможности отслеживания** — прямые затраты и косвенные затраты. Прямые затраты назначаются непосредственно объектам затрат. Косвенные затраты невозможно напрямую проследить до объектов затрат. Косвенные затраты распределяются объектам затрат.
-   **По поведению** — постоянные, переменные и полупеременные.

**Поведение затрат**

Поведение затрат классифицирует затраты согласно их поведению по отношению к изменениям в ключевые бизнес-мероприятиях. Чтобы эффективно контролировать затраты, руководство должно понимать поведение затрат. Существует три типа поведения затрат: постоянные, переменные и полупеременной.

- **Постоянные затраты** — Постоянные затраты представляют собой затраты, которые не изменяются в краткосрочной перспективе, независимо от изменений в уровне активности. Например, постоянные затраты могут быть основными эксплуатационными расходами компании, такими как аренда, которая не изменится, даже если уровень активности увеличивается или уменьшается.

- **Переменные затраты** — Переменные затраты изменяются согласно изменению уровня активности. Например, определенные затраты на основные материалы связаны с каждым продаваемым продуктом. Чем больше продуктов продано, тем больше затраты на основные материалы.

- **Полупеременные затраты** — Полупеременные затраты частично постоянные и частично переменные. Например, плата за доступ в Интернет включает в себя стандартный ежемесячный платеж за доступ и плату за широкополосный трафик. Стандартный ежемесячный платеж является постоянными затратами, тогда как плата за широкополосный трафик является переменными затратами.

**Единица управления затратами**

Единица учета затрат представляет структуру затрат. Структура определяет, как затраты движутся в иерархическом порядке между аналитиками объектов затрат и соответствующими им объектами затрат 

**Распространение затрат**

Используется для перераспределения затрат из одного объекта затрат на один или несколько других объектов затрат путем применения соответствующей базы распределения. Распространение затрат и распределение затрат отличаются тем, что распространение затрат всегда происходит на уровне элемента первичных затрат исходных затрат без взаимной обработки.

**Распределение затрат**

Используется для распределения сальдо объекта затрат на другие объекты затрат путем применения базы распределения. Finance поддерживает метод взаимного распределения. В методе взаимного распределения взаимные услуги, которыми обмениваются вспомогательные объекты затрат, полностью распознаются. Система автоматически определяет порядок выполнения распределения и повторяет его. Сальдо объекта затрат распределяется одной базой распределения. Поддерживаются распределения между аналитиками объектов затрат и их соответствующими элементами. Порядок распределения управляется единицей управления затратами.

**Политика распределения затрат**

Политика распределения затрат определяет суммы и количества, которые необходимо распределить. Правила распределения включают правила источника распределения, которые определяют распределяемые затраты и правила целей распределения, которые определяют, где выполняется распределение затрат. Например, все затраты на коммунальные услуги находятся в источнике распределения, который можно распределить среди различных подразделений в организации (то есть, среди целей распределения).

**Свертка затрат**

Правила свертки затрат предназначены для агрегирования затрат в содержательные интервалы. Уровень агрегирования определяется пользователем и предполагает назначение элемента вторичных затрат. Если свертка затрат не используется, каждый элемент затрат распределяется из одного объекта затрат на другой.

**Политика ставки затрат**

Ставка затрат используется для расчета цены на объект затрат. Чтобы понять элементы цены, вы определяете политики ставки затрат. Существует два типа ставки затрат: историческая ставка затрат и запланированная ставка затрат. Историческая ставка затрат представляет собой расчетную ставку, которая используется как коэффициент для базы распределения объекта затрат. Ставка рассчитывается на основе распределений затрат в предыдущий период. Запланированная ставка — это определяемая пользователем ставка.

**Иерархия аналитик**

Имеются две иерархии аналитик: иерархия категорий и иерархия классификации. Тип "Иерархия категоризации аналитик" используется для целей отчетности. Он поддерживает только аналитики элементов затрат. Тип "Иерархия классификации аналитик" используется для определения политик и целей отчетности. Он поддерживает все аналитики, например объекты затрат, элементы затрат и статистические аналитики. 

**Соединитель данных**

Модуль "Учет затрат" поддерживает интеграцию данных из систем-источников посредством набора соединителей данных. Доступны следующие соединители данных:

-  Импортированные проводки (уже настроенный)
-  Dynamics 365 Finance (уже настроенный)
-  Dynamics AX (требуется настройка)

**Примечание.** Соединитель данных "Импортированные проводки" основан на информационных объектах.

**Поставщик данных**

Большинство систем-источников могут предоставлять данные, которые соответствуют одному или нескольким источникам данных в модуле "Учет затрат". Чтобы сопоставить данные из исходных систем с источником данных в модуле "Учет затрат", необходимо настроить поставщик данных. В следующей таблице перечислены доступные поставщики данных для каждого соединителя данных и источника данных.

|  **Источники данных** |  **Соединитель данных "Импортированные проводки"** | **Соединитель данных Dynamics 365 Finance**  | **Соединитель данных Dynamics AX**  |
|---|---|---|---|
| Элементы аналитики элементов затрат  |  Да | Да  | Да  |
|  Элементы аналитики объектов затрат |  Да | Да  | Да  |
|  Элементы статистической аналитики | Да  | Нет  | Нет  |
|  Главная книга | Да  | Да  | Да  |
|  Записи бюджета  | Да  | Да  | Да  |
|  Статистические меры | Да  | Да  | Да  |

**Формула**

Базы распределения формулы позволяют определить дополнительные формулы для достижения правильной базу распределения. Можно вручную создать базы распределения формул. Чтобы определить формулу, можно использовать следующие операторы.

|  **Символы** | **Текст**  |
|---|---|
|  ( ) | Круглые скобки  |
|  < |  Меньше |
|  > |  Больше |
|  + |  Сложение |
|  – |  Вычитание |
| *  | Умножение  |

Традиционные операторы IF не поддерживаются. Тем не менее можно создавать выписки и проверять,выполняются ли они.

|  **Проверка оператора** | **Результат**  |
|---|---|
|  a > b| Истина  |
|  a > b |  Ложь |

**Накладные расходы**

Накладные расходы представляют собой текущее расходы на работу компании. Это затрат, которые нельзя напрямую связать с определенными бизнес-мероприятиями. Ниже приведены несколько примеров накладных расходов.

-   Расходы на учет
-   Амортизации
-   Страхование
-   Интересы
-   Судебные сборы
-   Налоги
-   Затраты на коммунальные услуги

**Ставка накладных расходов**

Ставки определяются для каждого объекта затрат и элемента затрат. Существует два типа ставок: финансового периода и определяемые пользователем. Ставки финансового периода рассчитываются путем расчета накладных расходов. Ставка конкретного пользователя определяется пользователем и может использоваться для распределения затрат между объектами затрат по заранее определенной ставке в расчете накладных расходов.

**Опубликован**

Если значение этого поля — "Да", пользователь, которому назначена одна из следующих ролей, может просматривать отчет в рабочей области "Учет затрат":

-  Диспетчер учета затрат
-  Бухгалтер, учитывающий затраты
-  Младший бухгалтер по учету затрат
-  Контролер объектов затрат

Если значение этого поля — "Нет", только пользователи, которым назначена одна из следующих ролей, могут просматривать отчет в рабочей области "Учет затрат":

-  Диспетчер учета затрат
-  Бухгалтер, учитывающий затраты
-  Младший бухгалтер по учету затрат

**Статистическая аналитика**

Статистическая аналитика и ее элементы используются для регистрации и контроля немонетарных записей в модуле "Учет затрат". Элементы статистической аналитики можно использовать для двух целей:

-  В качестве базы распределения в таких политиках, как распределение затрат и распределение стоимости.
-  Для отчетности по потреблению немонетарных ресурсов.

Статистическая аналитика — это выражение количества или суммы операций, которое может использоваться в качестве основы для распределений или расчета ставок. Она создается вручную или импортируется из исходных систем. Примеры статистических аналитик включают число сотрудников, количество лицензированного ПО на каждом устройстве, расход энергии каждой машиной или площадь для центра затрат.

**Оператор**

Отчеты представляют собой представления для менеджеров, ответственных за контроль затрат. Отчеты определяются контролером затрат и дают быстрое общее представление о фактических затратах, бюджетных затратах и отклонениях. При необходимости менеджер может дополнительно детализировать сведения. Чтобы гарантировать, что менеджеры просматривают только данные, за которые они отвечают, данные, отображаемые в отчете, контролируются правилами доступа.

**Версия**

Версии используются для моделирования, просмотра и сравнения различных результатов. По умолчанию все фактические затраты просматриваются в одной базовой версии, известной как *фактическая*. Для бюджетов и расчетов можно работать с любым требуемым количеством версий. Например, можно импортировать бюджетные данные в исходную версию, а затем скорректировать бюджет в пересмотренной версии. Для расчетов можно создать несколько версий. В этих различных версиях можно затем создать расчеты с помощью различных правил расчета, которые будут применены для распределения затрат.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
