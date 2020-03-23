---
title: Обзор заданий импорта и экспорта данных
description: Для создания заданий импорта и экспорта данных и управления ими служит рабочая область "Управление данными".
author: Sunil-Garg
manager: AnnBe
ms.date: 09/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87b852a73268251241cd66a07d7e4f4720706c0d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184562"
---
# <a name="data-import-and-export-jobs-overview"></a>Обзор заданий импорта и экспорта данных

[!include [banner](../includes/banner.md)]

Для создания заданий импорта и экспорта данных и управления ими служит рабочая область **Управление данными**. По умолчанию процесс импорта и экспорта данных создает промежуточную таблицу для каждого объекта в целевой базе данных. Промежуточные таблицы позволяют проверить, очистить или преобразовать данные перед перемещением.

> [!NOTE]
> В этом разделе предполагается, что вы знакомы с [информационными объектами](data-entities.md).

## <a name="data-importexport-process"></a>Процесс импорта/экспорта данных
Ниже приведены шаги, необходимые для импорта или экспорта данных.

1. Создание задания импорта или экспорта, что предполагает выполнение следующих задач:

    - Определение категории проекта.
    - Определение объектов для импорта или экспорта.
    - Определение формата данных для задания.
    - Определение последовательности объектов, чтобы они обрабатывались в виде логических групп и в порядке, которые имеет какой-либо смысл.
    - Определение того, следует ли использовать промежуточные таблицы.

2. Проверка правильности сопоставления исходных данных и целевых данных.
3. Проверка параметров безопасности для задания импорта или экспорта.
4. Запуск задания импорта или экспорта.
5. Проверка правильности выполнения задания путем просмотра истории задания.
6. Очистка промежуточных таблиц.

В остальных разделах этой темы приведены дополнительные сведения о каждом шаге процесса.

> [!NOTE]
> Чтобы обновить форму импорта и экспорта данных для просмотра последних данных о ходе выполнения, используйте значок обновления формы. Обновление на уровне браузера не рекомендуется, поскольку оно прерывает все задания импорта и экспорта, которые не выполняются в пакете.

## <a name="create-an-import-or-export-job"></a>Создание задания импорта или экспорта
Задание импорта или экспорта данных можно запустить один раз или несколько раз.

### <a name="define-the-project-category"></a>Определение категории проекта
Рекомендуем подойти к выбору категории проекта для задания импорта или экспорта со всей тщательностью. Категории проекта помогают управлять связанными заданиями.

### <a name="identify-the-entities-to-import-or-export"></a>Определение объектов для импорта или экспорта
Можно добавить в задание импорта или экспорта конкретные объекты или выбрать шаблон для применения. Шаблоны заполняют задание списком объектов. Действие **Применить шаблон** становится доступным после присвоения заданию имени и сохранения задания.

### <a name="set-the-data-format-for-the-job"></a>Определение формата данных для задания
При выборе объекта необходимо выбрать формат данных, которые будут экспортированы или импортированы. Форматы определяются с помощью плитки **Настройка источников данных**. Формат исходных данных представляет собой комбинацию параметров **Тип**, **Формат файла**, **Разделитель строк** и **Разделитель столбцов**. Имеются также другие атрибуты, но эти являются ключевыми для понимания. В следующей таблице перечислены допустимые сочетания.

| Формат файла            | Разделитель строк/столбцов                       | Стиль XML                 |
|------------------------|--------------------------------------------|---------------------------|
| Excel                  | Excel                                      | \-Неприменимо-                     |
| XML                    | \-Неприменимо-                                      | XML-элемент XML-атрибут |
| С разделителями, фиксированная ширина | Запятая, точкой с запятой, символ табуляции, вертикальная черта, двоеточие | \-Неприменимо-                     |

### <a name="sequence-the-entities"></a>Определение последовательности объектов
Задать последовательность объектов можно в шаблоне данных или в заданиях импорта и экспорта. При запуске задания, которое содержит несколько информационных объектов, необходимо убедиться, что информационные объекты следуют в правильном порядке. Последовательность объектов задается главным образом для учета всех функциональных зависимостей между объектами. Если объекты не имеют никаких функциональных зависимостей, их можно импортировать или экспортировать параллельно.

#### <a name="execution-units-levels-and-sequences"></a>Единицы выполнения, уровни и порядковые номера
Единица выполнения, уровень в единице выполнения и порядковый номер объекта помогают управлять порядком, в котором экспортируются или импортируются данные.

- Объекты в различных единицах выполнения обрабатываются параллельно.
- В каждой единице выполнения объекты обрабатываются параллельно, если они имеют один и тот же уровень.
- На каждом уровне объекты обрабатываются в соответствии с их порядковым номером на данном уровне.
- После завершения обработки одного уровня обрабатывается следующий уровень.

#### <a name="resequencing"></a>Изменение последовательности
Изменить последовательность объектом может понадобиться в следующих ситуациях:

- Если для всех ваших изменений используется только одно задание, вы можете использовать команды изменения последовательности для оптимизации времени выполнения всего задания. В этих случаях можно использовать единицу выполнения для представления модуля, уровень для представления функциональной области в модуле, а порядковый номер для представления объекта. При таком подходе можно работать между модулями в параллельном режиме, но в пределах модуля все равно работать в определенной последовательности. Чтобы гарантировать успешное выполнение параллельных операций, необходимо учитывать все зависимости.
- Если используется несколько заданий данных (например, по одному заданию для каждого модуля), задание последовательности может влиять на уровень и порядковый номер для оптимального выполнения.
- Если зависимости отсутствуют вообще, вы можете задать последовательность объектов в различных единицах выполнения для максимальной оптимизации.

Меню **Изменение последовательности** доступно, когда выбрано несколько объектов. Изменять последовательность можно по единицам измерения, уровням или порядковым номерам. Можно задать приращение для изменения последовательности выбранных объектов. Единица, уровень и/или порядковый номер, выбранный для каждого объекта, обновляется на заданное значение приращения.

#### <a name="sorting"></a>Сортировка
Для просмотра списка объектов в порядке последовательности можно использовать параметр **Сортировать по**.

### <a name="truncating"></a>Сокращение
Для импорта проектов можно сократить записи в объектах до проведения импорта. Это полезно, если записи должна быть импортирована в чистой набор таблиц. Эта настройка по умолчанию отключен.

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a>Проверка правильности сопоставления исходных данных и целевых данных
Сопоставление — это функция, которая применяется и к заданиям импорта, и к заданиям экспорта.

- В контексте задания импорта сопоставление описывает, какие столбцы в исходном файле становятся столбцами в промежуточной таблице. Таким образом система может определить, в какой столбец в промежуточной таблице должны копироваться данные того или иного столбца в исходном файле должны копироваться.
- В контексте задания экспорта сопоставление описывает, какие столбцы промежуточной таблицы (т. е. источника) становятся столбцами в целевом файле.

Если имена столбцов в промежуточной таблице и файле совпадают, система устанавливает сопоставления автоматически на основании имен. Однако, если имена различаются, столбцы не сопоставляются автоматически. В этих случаях необходимо выполнить сопоставление, выбрав команду **Просмотр карты** в объекте в задании данных.

Доступно два представления сопоставления: **Визуализация сопоставления**, которое используется по умолчанию, и **Сведения о сопоставлении**. Красной звездочкой (\*) обозначаются все обязательные поля в объекте. Эти поля должны быть сопоставлены, прежде чем вы сможете работать с объектом. Работая с объектом, вы можете отменить сопоставление других полей, если необходимо. Чтобы отменить сопоставление поля, выберите поле в столбце **Объект** или в столбце **Источник**, а затем выберите **Удалить выбор**. Выберите **Сохранить**, чтобы сохранить изменения, а затем закройте страницу, чтобы вернуться в проект. Эту же процедуру можно использовать для изменения сопоставления полей между источником и промежуточной таблицей после импорта.

Сопоставление на странице можно сгенерировать, выбрав **Создать сопоставление источника**. Сгенерированное сопоставление ведет себя как автоматическое сопоставление. Следовательно, все несопоставленные поля необходимо сопоставить вручную.

![Сопоставление данных](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a>Проверка параметров безопасности для задания импорта или экспорта
Доступ к рабочей области **Управление данными** можно ограничить, чтобы пользователи, не являющиеся администраторами, имели доступ только к определенным заданиям данных. Доступ к заданию данных подразумевает полный доступ к истории выполнения этого задания и доступ к промежуточной таблице. Следовательно, при создании задания данных необходимо проследить за тем, чтобы были заданы надлежащие параметры управления доступом.

### <a name="secure-a-job-by-roles-and-users"></a>Ограничение доступа к заданию по ролям и пользователям
Меню **Применимые роли** служит для ограничения доступа к заданию одной или несколькими ролями безопасности. Доступ к заданию будут иметь только пользователи с этими ролями.

Также можно ограничить доступ к заданию конкретным набором пользователей. Предоставление доступа к заданию по отдельным пользователям, а не по ролям обеспечивает более высокий уровень контроля, если роли назначено несколько пользователей.

### <a name="secure-a-job-by-legal-entity"></a>Ограничение доступа к заданию по юридическому лицу
Задания данных по природе своей являются глобальными. Таким образом, при создании и использовании задания данных в юридическом лице это задание будет видно другим юридическим лицам в системе. В некоторых сценариях такое предусмотренное по умолчанию поведение является предпочтительным. Например, в организации, которая импортирует накладные посредством информационных объектов, может существовать централизованная группа обработки накладных, отвечающая за устранение ошибок в накладных по всем подразделениям организации. В этом случае централизованной группе обработки накладных полезно иметь доступ к заданиям импорта накладных из всех юридических лиц. Следовательно, предусмотренное по умолчанию поведение соответствует требованиям с точки зрения юридических лиц.

Однако в организации также могут быть отдельные группы обработки накладных для каждого юридического лица. В таком случае команда в юридическом лице должна иметь доступ только к заданию импорта накладных в своем собственном юридическом лице. Для удовлетворения этого требования можно настроить контроль доступа к заданиям данных по юридическому лицу с помощью меню **Применимые юридические лица** внутри задания данных. По завершении конфигурирования пользователи смогут видеть только задания, доступные в юридическом лице, в которое они в данный момент вошли. Чтобы просмотреть задания в другом юридическом лице, пользователю понадобится перейти в это юридическое лицо.

Доступ к заданию можно ограничить по ролям, пользователям и юридическому лицу одновременно.

## <a name="run-the-import-or-export-job"></a>Запуск задания импорта или экспорта
Можно запустить задание однократно, нажав кнопку **Импорт** или **Экспорт** после определения задания. Чтобы настроить повторяющееся задание, нажмите кнопку **Создать повторяющееся задание данных**.

> [!NOTE]
> Задания импорта или экспорта могут выполняться асинхронно с помощью кнопки **Импорт** или **Экспорт**. Для асинхронного запуска используется асинхронная платформа, которая отличается от платформы пакетной обработки. Однако как и платформа пакетной обработки, асинхронная платформа также выполняет регулирование и поэтому задание может выполняться не сразу. Задания также могут выполняться синхронно при выборе команды **Импортировать сейчас** или **Экспортировать сейчас**. Это запускает задание немедленно и полезно, если асинхронный или пакетный режим не запускается из-за регулирования. Задания могут также выполняться в пакете при выборе параметра **Пакетная обработка**. Пакетные ресурсы обычно подвергаются регулированию, поэтому пакетное задание может начаться не сразу. Асинхронный вариант полезен, когда пользователи взаимодействуют непосредственно с интерфейсом пользователя и не являются опытными пользователями, чтобы понимать планирования пакетной обработки. Использование пакетной обработки является альтернативным вариантом, если большие объемы должны быть импортированы или экспортированы. Пакетные задания можно запланировать для выполнения в определенной пакетной группе, благодаря чему обеспечивает больший контроль с точки зрения балансировки нагрузки. Если асинхронные и пакетные задания оба подвергаются регулирования из-за высокой загрузки ресурсов в системе, то имеется вариант немедленного выполнения — можно использовать синхронную версию импорта и экспорта. Синхронный вариант начнется немедленно и будет блокировать пользовательский интерфейс, поскольку он выполняется синхронно. Окно браузера должно оставаться открытым во время выполнения синхронной операции.

## <a name="validate-that-the-job-ran-as-expected"></a>Проверка правильности выполнения задания
Для исследования и устранения неполадок и в заданиях импорта, и в заданиях экспорта ведется история задания. Запуски задания в ней упорядочены по временным диапазонам.

![Диапазоны в истории задания](./media/dixf-job-history.md.png)

По каждому запуску задания фиксируются следующие подробности:

- Сведения о выполнении
- Журнал выполнения

Сведения о выполнении отражают состояние каждого информационного объекта, обработанного заданием. Таким образом можно быстро найти следующую информацию:

- Какие объекты были обработаны.
- Сколько записей в каждом объекте было успешно обработано, а сколько обработать не удалось.
- Записи промежуточной таблицы для каждого объекта.

Промежуточные данные можно загрузить в виде файла для заданий экспорта и в виде пакета для задания импорта и экспорта.

Из сведений о выполнении можно также открыть журнал выполнения.

## <a name="clean-up-the-staging-tables"></a>Очистка промежуточных таблиц
Начиная с обновления платформы Platform update 29 эта функциональность объявлена устаревшей. Она заменена новой версией функциональности очистки истории заданий, которая объясняется ниже.

Очистить промежуточные таблицы можно с помощью функции **Очистка промежуточных данных** в рабочей области **Управление данными**. Для выбора того, какие записи должны быть удалены из тех или иных промежуточных таблиц, можно использовать следующие варианты:

- **Объект** — если указан только объект, удаляются все записи из промежуточной таблицы этого объекта. Выбирайте этот вариант, чтобы удалить все данные для объекта по всем проектам данных и всем заданиям.
- **Код задания** — если указан только код задания, все записи для всех объектов в выбранном задании удаляются из соответствующих промежуточных таблиц.
- **Проекты данных** — если только выбран проект данных, удаляются все записи для всех объектов и во всех заданиях для выбранного проекта данных.

Можно также сочетать эти варианты для дальнейшего ограничения удаляемого набора записей.

## <a name="job-history-clean-up-available-in-platform-update-29-and-later"></a>Очистка истории заданий (доступно в обновлении платформы Platform update 29 и позднее)

Функциональность очистки истории заданий в управлении данными должна использоваться для планирования периодической очистки истории выполнения. Эта функциональность заменяет предыдущую функцию очистки промежуточной таблицы, которая теперь устарела. Следующие таблицы будут очищены в процессе очистки.

-   Все промежуточные таблицы

-   DMFSTAGINGVALIDATIONLOG

-   DMFSTAGINGEXECUTIONERRORS

-   DMFSTAGINGLOGDETAIL

-   DMFSTAGINGLOG

-   DMFDEFINITIONGROUPEXECUTIONHISTORY

-   DMFEXECUTION

-   DMFDEFINITIONGROUPEXECUTION

Функциональность должна быть включена в управлении функциями, а затем будет доступна из меню **Управление данными \> Очистка истории заданий**.

### <a name="scheduling-parameters"></a>Параметры планирования

При планировании процесса очистки необходимо указать следующие параметры для определения критериев очистки.

-   **Количество дней для сохранения истории** — этот параметр используется для контроля объема сохраняемой истории выполнения. Указывается как число дней. Когда задание очистки запланировано как повторяющееся пакетное задание, эта настройка будет действовать как постоянно скользящее окно, таким образом, всегда оставляя историю для определенного количества дней нетронутыми, но удаляя остальные данные. Значение по умолчанию — 7 дней.

-   **Количество часов для выполнения задания** — в зависимости от объема очищаемой истории, общее время выполнения задания по очистке может варьироваться от нескольких минут до нескольких часов. Поскольку очистка упомянутых таблиц должна быть выполнена, когда в системе нет других действий по управлению данными, становится важным убедиться, что задание очистки выполняется и завершается до начала бизнес-деятельности.

    Максимальное время выполнения может быть указано, установив максимальное ограничение на количество часов, которые задание должно выполняться, с помощью этого параметра. Логика очистки проходит по одному идентификатору выполнения задания за раз в хронологическом порядке, начиная с самого старого, для очистки связанной истории выполнения. Она перестанет подбирать новые идентификаторы выполнения для очистки, когда оставшаяся длительно выполнения будет находиться в пределах последних 10% от указанной длительности. В некоторых случаях ожидается, что работа по очистке будет продолжена и после указанного максимального времени. Это будет в значительной степени зависеть от количества удаляемых записей для текущего идентификатора выполнения, который был запущен до достижения порога 10%. Начавшаяся очистка должна быть завершена для обеспечения целостности данных, что означает, что очистка будет продолжаться, несмотря на превышение указанного лимита. Когда это завершено, новые идентификаторы выполнения не подбираются и выполняется задания очистки завершается. Оставшаяся история выполнения, которая не была очищена из-за недостаточного времени выполнения, будет выбрана при следующем запланированном выполнении задания. Значение по умолчанию и минимальное значение для этого параметра устанавливаются равными 2 часам.

-   **Повторяющееся пакетное** — задание очистки может быть выполнено в виде одноразового ручного выполнения или также может быть запланировано для повторного выполнения в пакете. Пакет может быть запланирован с помощью параметров **Выполнять в фоновом режиме**, что является стандартной настройкой пакетного выполнения.