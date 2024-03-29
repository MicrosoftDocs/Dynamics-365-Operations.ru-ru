---
title: Инженерные версии и категории технологических продуктов
description: В этой статье приводятся сведения о концепции инженерных версий. Инженерные версии гарантируют, что различные состояния продукта и его данные остаются текущими и ясными, и что они могут быть визуализированы в системе.
author: t-benebo
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgLookupDynastring, EngChgProductVersionNumberRule, EngChgEcmProductRoute, EngChgEcmRequestProducts, EngChgEcmProductRoute, EngChgEcmProductPreview,EngChgEcmProductBOMItemIdLookup, EngChgEcmProductBOMConsistOf, EngChgEcmProductCreate, EngChgEcmProductLookup, EngChgProductVersionPrCompany, ngChgProductTypeLookup, EngChgProductType, EngChgProductItemPart, EngChgProductItem, EngChgEcmCategory, EngChgEcmBomDesignerEditBom, EngChgEcmBomDesigner, EngChgEcmBOMCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a98ead81a61ceac2ed721848847164f76e758f80
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872075"
---
# <a name="engineering-versions-and-engineering-product-categories"></a>Инженерные версии и категории технологических продуктов

[!include [banner](../includes/banner.md)]

По многим причинам инженерные продукты развиваются в течение жизненного цикла продукта. Например, можно внести изменения, чтобы улучшить удобство обслуживания продукта, изменить компонент, поскольку он больше не предлагается поставщиком, учесть новые аналитические сведения или исправить ошибки в первоначальном дизайне. Кроме того, имеется множество причин, почему эти изменения должны быть сохранены как часть текущего продукта, таким образом, что предыдущие данные не перезаписываются. Вот некоторые из этих причин:

- Вам необходимо отслеживать продукт в том виде, в котором он был произведен и доставлен клиентам в предыдущих состояниях жизненного цикла.
- Необходимо время для подготовки к утверждению и применению изменений.
- При каждом изменении необходимо иметь отметку времени, и необходимо обеспечить возможность доставки ранее произведенных продуктов отдельно друг от друга.

*Инженерные версии* гарантируют, что различные состояния продукта и его данные остаются текущими и ясными, и что они могут быть визуализированы в системе. Эта концепция позволяет поддержать целостность, блокировать спецификацию для производства, устранять изменчивость и легко определять изменения.

Как правило, правило *форма-соответствие-функция* применяется для определения, требуется ли изменение нового продукта, новая версия или обновление существующей версии. Каждый из трех терминов в названии данного правила относится к конкретному аспекту части, что позволяет инженерам сопоставлять части их потребностям. Правило "форма-соответствие-функция" позволяет повысить гибкость изменений конструкции, поскольку для изменения части необходимо наличие минимальной документации и затрат на разработку, при условии, что в системе поддерживаются соответствие, формат и функция продукта.

- **Соответствие** подразумевает возможность части или функции соединяться, сопрягать или присоединяться к другой функции или частью сборки. Соответствие позволяет части удовлетворять требованиям к отклонениям в сборке, чтобы быть полезной.
- **Форма** относится к характеристикам части или сборки, таким как внешние размеры, вес, размер и внешний вид. Форма представляет собой аспект, на который максимально влияет эстетический выбор инженера. Она включает корпус, шасси и панель управления, которые становятся наружным "лицом" продукта.
- **Функция** является критерием, который выполняется, когда часть эффективно и надежно выполняет свою декларированную функцию. Например, в электронном продукте функция может зависеть от используемых твердотельных компонентов, а также от программного или аппаратного обеспечения. Часто она может также зависеть от особенностей выбранного корпуса. Две наиболее частые причины, по которым корпус не соответствует критерию функции, являются неправильный размер или размещение отверстий, а также неправильная или отсутствующая маркировка. 

## <a name="engineering-versions"></a>Версии разработки

При использовании инжиниринговых продуктов у каждого продукта имеется по крайней мере одна инженерная версия. При создании инженерного продукта автоматически создается исходная инженерная версия. В каждой из инженерных версий хранятся относящиеся к проектированию данные, относящиеся к этой версии. Ниже приведены несколько примеров таких данных:

- Номер версии и номер предыдущей версии (если применимо)
- Даты начала и окончания действия
- Статус активности версии продукта, который указывает, может ли данная версия выпускаться и использоваться в проводках (Для получения дополнительных сведений см. раздел [Готовность продукта](product-readiness.md).)
- Инжиниринговая компания, которая создала и владеет продуктом (Дополнительные сведения см. в разделе [Инжиниринговые компании и правила владения данными](engineering-org-data-ownership-rules.md).)
- Сопутствующие технологические документы, такие как руководство по сборке, инструкции пользователя, изображения и ссылки
- Инженерные атрибуты (Дополнительные сведения см. в разделе [Инженерные атрибуты и поиск инженерных атрибутов](engineering-attributes-and-search.md).)
- Спецификации для технологических продуктов
- Формулы для продуктов непрерывного производства
- Технические маршруты

Можно обновить эти данные в существующей версии или создать новую версию, используя *заказ на техническое изменение*. (Дополнительные сведения см. в разделе [Управление изменениями в технологических продуктах](engineering-change-management.md).) При создании новой версии продукта система копирует все данные, связанные с проектированием, в эту новую версию. Затем можно изменить данные для этой новой версии. Таким образом можно отслеживать отдельные данные для каждой из последовательных версий. Для сравнения различий между последовательными инженерными версиями проверьте заказ на технические изменения, включающий типы изменений, которые указывают все изменения.

Как было указано, при создании инженерного продукта автоматически создается исходная инженерная версия. Номер версии для этой версии соответствует правилу нумерации версий, определенному в категории разработки продукта. Для перехода к последующей версии необходимо добавить продукт в заказ на техническое изменение в виде строки, а в поле **Влияние** должно быть выбрано значение *Новая версия*. В заказ на техническое изменение будут включены сведения об изменении от текущей версии до следующей версии.

Обратите внимание, что в каждый момент времени инженерный продукт может находиться только в одном заказе на техническое изменение. Это ограничение обеспечивает точность данных и помогает избежать перекрытия или противоречивых изменений в продукте. Также обратите внимание, что поле **Инженер** в представлении **Заголовок** заказа на технические изменения показывает инженера, который несет ответственность за этот заказ на изменение. Если инженер принадлежит к рабочей группе, которая определена в системе, в поле **Ответственный** отображается лидер этой рабочей группы.

## <a name="track-versions-in-transactions"></a>Отслеживание версий в проводках

При использовании управления техническими изменениями основная информация о продукте всегда включает одну или несколько технологических версий. При настройке инженерных продуктов можно выбрать, является ли данная инженерная версия также частью *логистических проводок*. (Дополнительные сведения см. в разделе [Настройка категорий технологических продуктов](#product-category) ниже в этой статье.) Если влияние на логистику имеет значение, оно различается для каждого продукта и компании. В некоторых случаях используется только последняя версия продукта. Таким образом, при вводе новой версии предыдущая версия больше использоваться не может. В других случаях предыдущая версия требуется в логистических транзакциях для преодоления следующих проблем:

- Отдел снабжения должен отгружать две части продукта клиенту. В этом случае необходимо решить, следует ли разрешить отгружать две разных версии.
- Позже выяснилось, что происходит проблема, и что она связана с конкретным изменением. В этом случае может оказаться полезным определить, какая именно версия была отгружена в каждом заказе.
- Компании обычно хотят отгружать сначала старые версии, чтобы вывести их из запасов. Этот подход, особенно для продуктов с небольшим объемом, часто может управляться путем определения дат действия новой версии относительно прогноза о том, когда запасы старой версии будут исчерпаны. Однако в некоторых случаях это сравнение может оказаться недоступным или вы можете счесть, что неопределенность прогноза уровня запасов будет слишком высокой.

Решение о том, следует ли отображать версии в запасах, зависит от таких факторов, как ранее упомянутые, а также от практики компании и других соображений, относящихся к каждой компании. Можно указать поведение для *категории технологических продуктов*. Затем оно применяется ко всем продуктам, созданным из этой категории, для всех компаний, в которые выпущен этот продукт.

Для продуктов, которые настроены таким образом, чтобы они имели влияние на логистику, в каждой проводке должна быть указана инженерная версия. Хотя система предложит *последнюю активную версию*, можно выбирать из всех активных версий, доступных для компании. Для продуктов, которые не настроены таким образом, чтобы они имели влияние на логистику, в каждой проводке не указывается инженерная версия. Однако система использует последнюю активную версию. Например, при добавлении продукта в производственную спецификацию используется последняя версия, и при выполнении сводного планирования предполагается использование последней версии.

## <a name="set-up-engineering-product-categories"></a><a name="product-category"></a>Настройка категорий технологических продуктов

Категория технологических продуктов предоставляет основу для создания конкретного инженерного продукта. Каждая категория устанавливает набор значений и политик по умолчанию. Поэтому при создании технологического продукта сначала следует выбрать категорию, из которой он будет создан.

Обратите внимание, что новый тип иерархии категорий (*иерархия инженерных продуктов*) настраивается автоматически. Категории можно создать вручную, перейдя к пункту **Управление техническими изменениями \> Настройка \> Сведения о категории инженерного продукта**.

Каждая категория технологических продуктов устанавливает поведение по умолчанию для технологических продуктов, созданных на основе этой категории. После создания технологического продукта изменить его категорию технологического продукта невозможно. Однако если выбрать некорректную категорию, можно удалить продукт, а затем создать его повторно.

При создании категории технологического продукта изменение следующих параметров запрещено:

- Инженерная компания
- Тип продукта
- Подтип продукта
- Группа аналитик продуктов
- Технология конфигурации
- Правило номера версии

Другие параметры могут наследовать значения по умолчанию, настроенные для категории технологических продуктов. Однако согласно системным правилам эти значения можно изменить.

Для работы с категориями технологических продуктов перейдите к пункту **Управление техническими изменениями \> Настройка \> Сведения о категории инженерного продукта**. Затем выполните одно из следующих действий.

- Чтобы создать новую категорию, в области действий выберите **Создать**, затем настройте поля, как описано в следующих подразделах.
- Чтобы изменить существующую категорию, выберите ее на панели списка, выберите **Правка** на панели операций, затем задайте поля, как описано в следующих подразделах.
- Чтобы удалить существующую категорию, выберите ее на панели списка, затем выберите **Удалить** на панели операций.

### <a name="header"></a>Верхний колонтитул

Задайте следующие поля в заголовке категории технологических продуктов.

| Поле | описание |
|---|---|
| Наименование | Введите имя для категории технологических продуктов. |
| Инженерная компания | Выберите инженерную компанию, в которой можно создать продукты из данной категории технологических продуктов и в которой можно их обслуживать. |

### <a name="details-fasttab"></a>Экспресс-вкладка сведений

Задайте следующие поля на экспресс-вкладке **Сведения** категории технологических продуктов.

| Поле | описание |
|---|---|
| Тип продукта | Выберите, применяется ли категория к продуктам или услугам. |
| Тип производства | Это поле отображается только в том случае, если включено [управление изменениями формул](manage-formula-changes.md) в системе. Выберите тип производства, к которому применяется категория технологического продукта:<ul><li>**Номенклатура планирования** — эта инженерная категория используется для управления изменением формулы для номенклатуры планирования. Номенклатуры планирования используют формулы. Они похожи на номенклатуры формул, но они используются для производства только сопутствующих и побочных продуктов, но не готовой продукции. В процессе производства используются формулы.</li><li>**Спецификация** — данная инженерная категория используется для управления технологическими продуктами, которые не используют формулы и обычно (но не обязательно) включают спецификации.</li><li>**Формула** — эта инженерная категория используется для управления изменением формулы для готовых продуктов. Эти номенклатуры будут иметь формулу, но не спецификацию. В процессе производства используются формулы.</li></ul> |
| Учет в двух единицах измерения | Этот параметр отображается только в том случае, если включено [управление изменениями формул](manage-formula-changes.md) в системе. Он доступен только в том случае, если в поле **Тип производства** установлено значение *Номенклатура планирования* или *Формула*. Установите для этого параметра значение *Да*, если данная инженерная категория будет использоваться для управления номенклатурами, требующими поддержки учета в двух единицах измерения. |
| Отслеживание версий в проводках | Выберите, следует ли отмечать версию продукта по всем проводкам (влияние на логистику). Например, при отслеживании версии в проводках каждый заказ на продажу покажет, какая версия продукта была продана в этом заказе на продажу. Если не отслеживать версию в проводках, заказы на продажу не будут показывать, какая конкретно версия была продана. Вместо этого они всегда отображают последнюю версию.<ul><li>Если для этого параметра установлено значение *Да*, для продукта создается шаблон продукта, и каждая версия продукта будет иметь вариант, использующий аналитику продукта *версия*. В поле **Подтип продукта** автоматически устанавливается значение *Шаблон продукта* и в поле **Группа аналитик продуктов** необходимо выбрать группу аналитик продукта, в которой активна аналитика *версия*. Будут отображены только группы аналитик продукта, в которых *версия* является активной аналитикой. Можно создать новые группы аналитик продуктов, нажав кнопку **Изменить** (символ карандаша).</li><li>Если этот параметр имеет значение *Нет*, аналитика продукта *версия* использоваться не будет. Затем можно выбрать, нужно ли создать продукт или шаблон продукта, в котором используются другие аналитики.</li></ul><p>Этот параметр часто используется для продуктов, имеющих разницу в затратах между версиями, или с продуктами, для которых в отношении клиента применяются разные условия. Таким образом, важно указать, какая версия использовалась в каждой проводке.</p> |
| Подтип продукта | Выберите, будет ли категория содержать продукты или шаблоны продукта. Для шаблонов продукта будут использоваться аналитики продукта.
| Группа аналитик продуктов | Параметр **Отслеживать версии в проводках** помогает выбрать группу аналитик продукта. Если указано, что необходимо отслеживать версию в проводках, будут отображены группы аналитик продукта, в которых используется аналитика *версия*. В противном случае будут отображены только группы аналитик продукта, в которых аналитика *версия* не используется. |
| Состояние жизненного цикла продукта при создании | Настройте состояние жизненного цикла продукта по умолчанию, которое должен иметь инженерный продукт, когда он будет создан впервые. Дополнительные сведения см. в разделе [Состояния жизненного цикла продукта и проводки](product-lifecycle-state-transactions.md). |
| Правило номера версии | Выберите правило нумерации версий, которые применяются к категории:<ul><li>**Вручную** — вы выбираете номер версии для каждой новой версии.</li><li>**Автоматически** — система устанавливает номер версии на основе определенного вами формата. При настройке формата используйте знак решетки (\#) для представления цифры и любой другой символ для представления постоянного значения. Например, если определить формат как *V-\#\#*, первая версия будет иметь вид "V-01", вторая версия будет иметь вид "V-02" и так далее.</li><li>**Список** — система берет следующий номер из заранее определенного списка определяемых пользователем значений.</li></ul> |
| Принудительно использовать дату вступления в силу | Выберите, должны ли даты срока действия инженерных версий быть непрерывными, или они могут быть с пропусками или перекрытиями. Этот параметр влияет на способ использования полей **Действует с** и **Действует до** для каждой инженерной версии, к которой относится данная категория.<ul><li>Если этот параметр имеет значение *Да*, для каждой версии должно быть указано значение **Действует с**, и ни перекрытия, ни разрывы между версиями не допускаются. Диапазон дат для каждой инженерной версии непосредственно соединяется с предыдущей и следующей инженерной версией, если они существуют. В этом случае всегда используется последняя версия, и более старые версии не используются.</li><li>Если этот параметр имеет значение **Нет**, ограничения на поля даты действия для инженерных версий отсутствуют, а также разрешаются перекрытия и зазоры. В этом случае несколько версий могут быть активными в одно и то же время, и можно работать с любой активной версией.</li></ul><p>Этот параметр также влияет на спецификации и маршруты, связанные с версией продукта. Дополнительные сведения см. в разделе [Подключение спецификаций и маршрутов к инженерным версиям](#boms-routes) далее в этой статье.</p> |
| Использовать номенклатуру правила нумерации | Установите для этого параметра значение *Да*, чтобы включить правила для определения номера продукта с помощью номерных серий, имен и значений инженерных атрибутов, а также текстовых констант в качестве сегментов. Чтобы создать или изменить правила, нажмите кнопку **Изменить**. |
| Использовать номенклатуру правила наименования | Установите для этого параметра значение *Да*, чтобы включить правила для определения имени с помощью имен инженерных атрибутов, значений инженерных атрибутов, а также текстовых констант в качестве сегментов. Чтобы создать или изменить правила, нажмите кнопку **Изменить**. |
| Использовать номенклатуру правила описания | Установите для этого параметра значение *Да*, чтобы включить правила для определения описания с помощью имен инженерных атрибутов, значений инженерных атрибутов, а также текстовых констант в качестве сегментов. Чтобы создать или изменить правила, нажмите кнопку **Изменить**. |

### <a name="attributes-fasttab"></a>Экспресс-вкладка "Атрибуты"

Используйте сетку на экспресс-вкладке **Атрибуты** для настройки инженерных атрибутов, которые применяются к продуктам, принадлежащим к данной категории. Сведения о порядке создания инженерных атрибутов см. в разделе [Инженерные атрибуты и поиск инженерных атрибутов](engineering-attributes-and-search.md).

Кнопки на экспресс-вкладке **Атрибуты** используются для добавления, удаления и упорядочивания атрибутов в сетке.

При изменении выбора атрибутов для инженерной категории и наличии уже существующих продуктов, которые основаны на этой категории, необходимо решить, следует ли применять изменения к этим продуктам. Если требуется, чтобы существующие продукты отражали изменения, выберите **Обновить существующие продукты** на экспресс-вкладке **Атрибуты**.

Для каждой строки, добавляемой в сетку, установите следующие поля.

| Поле | описание |
|---|---|
| Наименование | Выберите атрибут, который требуется добавить. |
| Значение | Выберите значение по умолчанию для атрибута. |
| Обязательная аналитика | Выберите, является ли атрибут обязательным, что означает, что пользователи должны указать допустимое значение для атрибута, прежде чем они смогут сохранить продукт. Результат этой настройки слегка отличается в зависимости от типа данных выбранного атрибута, как определено в следующем списке.<ul><li>**Логическое значение** — установите значение *Да*, чтобы потребовать, чтобы атрибут имел значение *Да* (система не будет разрешать сохранить продукт, у которого значение атрибута равно *Нет*). Установите для этого параметра значение *Нет*, чтобы принимать значение *Да* или *Нет*. (Атрибуты типа *Логическое значение* не могут иметь пустое значение.)</li><li>**Целое или десятичное значение** — установите значение *Да*, чтобы потребовать от пользователей вводить ненулевое значение для данного атрибута. Установите для этого параметра значение *Нет*, чтобы разрешить пользователям сохранение с нулевым значением.  (Атрибуты этих типов не могут иметь пустое значение.)</li><li>**Список** — списки имеют тип данных *Текст*, но также включает заранее определенный список возможных значений. Таким образом, невозможно ввести пустое значение для атрибутов этого типа, так что этот параметр не оказывает влияния и является только информационным.</li><li>**Все остальные типы данных** — установите значение *Да*, чтобы сделать атрибут обязательным. Установите значение *Нет*, чтобы разрешить пользователям сохранять продукт, не указывая значение для этого атрибута.</li></ul> |
| Атрибут партии | Выберите, должен ли атрибут распространяться с помощью функции пакетной обработки. |

### <a name="readiness-policy-fasttab"></a>Экспресс-вкладка политика готовности

Поле **Политика готовности продукта** используется для выбора политики готовности, которая должна применяться к продуктам, созданным на основе этой инженерной категории. Дополнительные сведения см. в разделе [Готовность продуктов](product-readiness.md).

> [!NOTE]
> Поле **Политика готовности продукта** несколько отличается, если включена функция *Проверки готовности продукта* в системе. (Эта функция позволяет применять политики готовности к стандартным \[неинженерным\] продуктам.) Дополнительные сведения см. в разделе [Назначение политик готовности для стандартных и технологических продуктов](product-readiness.md#assign-policy).

### <a name="release-policy-fasttab"></a>Экспресс-вкладка политики выпуска

Поле **Политика выпуска продукта** используется для выбора политики выпуска, которая применяется к продуктам, относящимся к этой категории. Дополнительные сведения см. в разделе [Структуры выпуска продуктов](release-product-structure.md).

## <a name="connect-boms-and-routes-to-engineering-versions"></a><a name="boms-routes"></a>Подключение спецификаций и маршрутов к инженерным версиям

Настройка параметра **Принудительно применять срок действия** важна для подключения спецификаций и маршрутов к каждой из технологических версий. Можно активировать несколько спецификаций или маршрутов по каждому продукту только в том случае, если имеется разница в одном из следующих параметров:

- Аналитика продукта
- Количество
- Место
- Даты вступления в силу

Инженерные спецификации и маршруты создаются из инженерной версии, в которой они применяются. Они могут быть распознаны с помощью флажка **Управляется инжинирингом**. При работе с инженерными спецификациями и маршрутами их обычно нельзя проектировать, используя различные количества. Кроме того, обычно не проектируются разные спецификации для каждого сайта. Кроме того, для инженерных спецификаций и маршрутов даты действия всегда берутся из технологической версии. Таким образом, инженерная версия, ее спецификация и ее маршрут будут иметь одинаковые даты действия.

Для продуктов, в которых используется аналитика продукта *версия* (вместе с влиянием на операции логистики), версия также добавляется к спецификациям и маршрутам. Это поведение позволяет отличать спецификации и маршруты последовательных версий, независимо от настройки **Принудительно применять срок действия**.

Для продуктов, в которых не используется аналитика продукта *версия* (без влияния на операции логистики), версия не добавляется к спецификациям или маршрутам. Таким образом, различия между спецификациями и маршрутами последовательных версий не будет. В этом случае настоятельно рекомендуется установить для параметра **Принудительно применять срок действия** значение *Да*. Таким образом можно предотвратить перекрытие технологических версий, а также активировать спецификацию и маршрут более новой версии без предварительной деактивации спецификации и маршрута предыдущей версии. Если в этом случае задать для параметра **Принудительно применять срок действия** значение *Да*, необходимо вручную отключить спецификации и маршруты старых версий, прежде чем можно будет активировать последнюю версию.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
