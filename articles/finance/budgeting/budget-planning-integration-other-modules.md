---
title: Интеграция бюджетного планирования с другими модулями
description: Бюджетные планы можно создавать из нескольких разных ресурсов. Базовые элементы периодического процесса одинаковы для всех ресурсов.
author: panolte
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanGenerate
audience: Application User
ms.reviewer: kfend
ms.custom: 64443
ms.assetid: f9a94db5-906c-404a-9ca5-91528d67c490
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4fd57b06f1d630417c52a49b7f4f4ecfa71b08c
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711809"
---
# <a name="budget-planning-integration-with-other-modules"></a>Интеграция бюджетного планирования с другими модулями

[!include [banner](../includes/banner.md)]

 Бюджетные планы можно создавать из нескольких разных ресурсов. Базовые элементы периодического процесса одинаковы для всех ресурсов. 



## <a name="periodic-processes-for-generating-budget-plans"></a>Периодические процессы для создания бюджетных планов

Бюджетные планы можно создавать из следующих ресурсов.

-   Проводки ГК
-   Основные средства
-   Прогнозируемые должности
-   Прогнозы проекта
-   Прогнозы поставки
-   Прогнозы спроса
-   Записи бюджетного регистра
-   Другие бюджетные планы

Базовые элементы периодического процесса одинаковы для всех процессов. Вкладки позволяют определить источник данных, целевые атрибуты (бюджетного плана) и параметры выполнения процесса в фоновом режиме в виде пакетного процесса. В дальнейших разделах этой статьи описаны элементы, которые могут быть неочевидны в каждом из процессов.

### <a name="actions"></a>Действия

Для каждого процесса создания доступны три действия.

-   **Создать новый бюджетный план** создает новый план с атрибутами, выбранными в разделе **Цель**. Эти атрибуты не обязательно должны быть уникальными. Следовательно, два плана могут иметь одинаковое название и другие значения.
-   **Заменить существующий сценарий бюджетного плана** удаляет все данные в целевом бюджетном плане в выбранном сценарии бюджетного плана и создает новые строки, использующие выбранные исходные данные.
-   **Обновить существующий сценарий бюджетного плана и добавить новые данные** обновляет существующие строки целевого плана, соответствующие исходным строкам, и добавляет новые строки для новых данных. Соответствие основано на счете учета, дате, классе бюджета и разных других полях. Например, при создании бюджетных планов из прогнозируемых должностей номер должности — важное поле. Все строки с номером должности, который соответствует исходному номеру должности, заменяются новыми строками из источника.

### <a name="source"></a>Источник

Для всех процессов вкладка **Источник** позволяет фильтровать данные с помощью кнопки **Фильтр**. По умолчанию для каждого процесса в фильтр добавляются определенные поля. Например, для процесса **Создать бюджетный план из Главной книги** доступны категории **Счет учета** и **Счет ГК**. Они отображаются на странице создания. Все добавляемые в фильтр поля также добавляются на страницу, вместе со всеми добавляемыми критериями.

### <a name="target"></a>Цель

Вариант **Исторический** на вкладке **Цель** позволяет использовать даты из исходных данных в качестве даты вступления в силу в бюджетном плане. Как правило, дата вступления в силу должна быть в пределах бюджетного цикла плана. Если для параметра **Исторический** задано значение **Да**, используется дата (даже год) источника, так что прошлые даты можно использовать как основание для сравнения. Невозможно изменить исторические данные в бюджетном плане, поэтому для плана задается утвержденный статус workflow-процесса. Тем не менее, можно сбросить статус, если другие сценарии в плане требуют изменений.

Поле **Суммировать итог по** вверху страницы также определяет используемую дату. Это поле содержит общие суммы и (необязательно) задает дату вступления в силу равной первому дню финансового года или финансового периода. 

Многие поля на вкладке <strong>Цель</strong> становятся доступными для редактирования или только чтения в зависимости от выбираемого действия. При переходе от создания нового бюджетного плана к обновлению существующего плана поле **Имя бюджетного плана** становится недоступным, а поля, связанные с выбором существующего плана, — доступными. И на вкладке **Цель**, и на вкладке **Источник** поле **Книга учета** всегда недоступно, потому что значение определяется выбранным процессом бюджетного планирования. 

Поле **Класс бюджета** позволяет задать строки бюджетного плана в качестве проводок расхода или проводок дохода. Как правило, проводки дохода — это кредиты счета учета. Следовательно, они хранятся как отрицательные суммы. Как правило, эти проводки отображаются как отрицательные суммы в бюджетном плане. Однако добавляя класс бюджета как поле в макет плана, можно отобразить доход как положительные суммы.

### <a name="generation-rules"></a>Правила создания

Три поля обеспечивают дополнительную функциональность: **Коэффициент**, **Минимум** и **Правило** **округления**. 

Значение в поле **Коэффициент** умножается на исходную сумму, чтобы получить сумму в бюджетном плане. Затем можно вносить корректировки при создании строк бюджетного плана. Например, можно ввести значение **1.03** и обозначить им увеличение на 3 процента. Коэффициент должен быть положительным числом. 

Поле **Минимум** позволяет задать пороговую сумму для создания строки бюджетного плана. Если исходная сумма меньше этого числа, бюджетный план не создается. Значение **0,00** допускает все значения, но не ограничивает строки положительными величинами. (Отсутствие значения ограничивает строки положительными значениями. Отрицательные значения всегда включаются и обычно представляют кредитные записи.)

Поле **Правило округления** позволяет задать точность создаваемых строк бюджетного плана. Можно округлять суммы до ближайшего 1,00, 10,00, 100,00 и т. д. валюты.

## <a name="notes-for-specific-processes"></a>Примечания по конкретным процессам
### <a name="generate-budget-plan-from-general-ledger"></a>Создать бюджетный план на основе главной книги

При создании бюджетного плана из данных главной книги необходимо задать в поле **Суммировать итог по** значение **Финансовый год**, если для параметра **Исторический** задано значение **Нет**. Периоды и даты в источнике могут не соответствовать периодам и датам в целевой записи. Поскольку у процесса отсутствует надежный способ сопоставления этих значений, необходимо ограничить процесс первым значением года. 

В целевом объекте поле **Класс бюджета** имеет значение **Расход** или **Доход**. Эта настройка используется для выбора атрибута **Тип бюджета** для создаваемых строк, если счет ГК в строке имеет тип, отличный от **Доход** или **Расход**.

### <a name="generate-budget-plan-from-fixed-assets"></a>Создать бюджетный план из основных средств

Процесс **Создать бюджетный план из основных средств** не имеет механизмов для суммирования по периоду или дню. Кроме того, также отсутствует возможность установить план как исторический. Можно использовать этот периодический процесс для включения прогнозируемых проводок по основным средствам в планирование бюджета.

### <a name="generate-budget-plan-from-forecast-positions"></a>Создать бюджетный план на основе прогнозируемых должностей

Процесс **Создание бюджетного плана из позиций прогноза** назначает позицию исходного прогноза строке бюджетного плана. Можно просмотреть эту позицию, добавив позицию прогноза в качестве строки в макет бюджетного плана или воспользовавшись запросом **Строки бюджетного плана**. Если не нужно назначать позицию прогноза строкам бюджетного плана, задайте для параметра **Включить позицию в строку бюджетного плана** значение **Нет**.

Строки в бюджетном плане суммируются по счету ГК и позиции. Однако можно исключить номер позиции, чтобы строки суммировались только по счету ГК. На вкладке **Цель** задайте для параметра **Включить позицию в бюджетный план** значение **Нет**.

В поле **Сценарий эквивалентов полной занятости бюджетного плана** можно выбрать сценарий для включения числа эквивалентов полной занятости в план бюджета. Это поле ограничено сценариями типа "количество", которые включаются в макет целевого бюджетного плана. Если выбирается сценарий с эквивалентом полной занятости, необходимо также выбрать счет ГК для эквивалентов полной занятости. Этот счет используется для создания строк количества для бюджетного плана. 

Процесс планирования бюджета и сценарий бюджетного плана, выбранные в источнике, определяют целевые процесс и сценарий бюджетного плана. Поскольку эти атрибуты назначены позициям прогноза, они должны соответствовать бюджетному плану. Следовательно, эти атрибуты невозможно изменить в целевом объекте.

### <a name="generate-budget-plan-from-project-forecasts"></a>Создать бюджетный план на основе прогнозов проекта

Процесс **Создание бюджетного плана из прогнозов проекта**, такой как **Создание бюджетного плана из позиций прогноза**, позволяет включить количества по проекту (часы, расходы и номенклатуры) в сценарий количества. Эти два процесса имеют схожие фильтры для столбцов в макете бюджетного плана. 

На вкладке **Источник** три параметра в разделе **Включить выписку** определяют, какие строки бюджетного плана создаются. Эти параметры совпадают с доступными при создании записей бюджетного регистра непосредственно из прогнозов проекта. Задайте для параметра **Прибыли и убытки** значение **Да**, чтобы создать строки для затрат и доходов. Задайте для параметра **НЗП** значение **Да**, чтобы создать записи незавершенного производства. Задайте для параметра **Распределение зарплаты** значение **Да**, чтобы создать строки для корреспондирующих счетов зарплаты для почасовых проводок. 

Поле **Класс бюджета** отсутствует, поскольку класс бюджета (**Расход** или **Доход**) определяется источником. 

Можно использовать бюджеты проекта в качестве источника, выбрав модель прогноза, которая содержит суммы бюджета проекта. Помните,что бюджеты проекта создают записи прогноза проекта после утверждения.

Чтобы выбрать только затраты или доходы для строк бюджетного плана, воспользуйтесь фильтром, чтобы выбрать <strong>Обновления бюджета: тип суммы = затраты</strong>. Чтобы выбрать только один тип прогноза, воспользуйтесь фильтром, чтобы выбрать <strong>Обновления бюджета: тип проводки = *xxx</strong>*. 

Для создания сценария бюджетного плана можно использовать только одну модель прогноза. Если выполняется процесс для одной модели прогноза, а затем выполняется обновление и вы пытаетесь указать другую модель, первая модель будет перезаписана, если все выполняется в рамках одного проекта и счетов учета. Чтобы создать сценарий бюджетного плана из более, чем одной модели прогноза, создайте разные сценарии бюджетного плана и воспользуйтесь параметрами распределения, чтобы вместе добавить их в другой сценарий. 

Процесс **Создание бюджетного плана из прогнозов проекта** также назначает исходный проект строке бюджетного плана.

### <a name="generate-budget-plan-from-supply-forecast"></a>Создать бюджетный план на основе прогноза поставки

Параметры фильтрации источника в процессе **Создание бюджетного плана из прогноза поставки** были смоделированы после параметров в функции **Перенос бюджета закупок в ГК**, поскольку этот процесс и эта функция схожи.

### <a name="generate-budget-plan-from-demand-forecast"></a>Создание бюджетного плана из прогноза спроса

Для процесса **Создание бюджетного плана из прогноза спроса** можно задать параметр **Заказ на продажу** равным **Да**, чтобы создать строки дохода в бюджетном плане, задать параметр **Потребление** равным **Да**, чтобы создать строки затрат, либо задать оба параметра равными **Да**.

### <a name="generate-budget-plan-from-budget-register-entries"></a>Создать бюджетный план из записей регистра бюджета

Для процесса **Создание бюджетного плана из записей бюджетного регистра** в источнике необходимо задать одну вложенную модель, один код бюджета и один номер записи. Другими словами, можно создать строки бюджетного плана только для одной записи бюджетного регистра. Можно использовать дополнительные записи в том же бюджетном плане, выполнив процедуру по одному разу для каждой исходной записи.

### <a name="generate-budget-plan-from-budget-plan"></a>Создать бюджетный план на основе бюджетного плана

Для процесса **Создание бюджетного плана из бюджетного плана** дополнительный набор параметров на вкладке **Цель** позволяет назначать новые финансовые аналитики. Если выбрана финансовая аналитика, это значение будет использоваться для всех строк бюджетного плана. Поэтому можно использовать один бюджетный план как основу для других бюджетных планов, а также назначать, например, новым бюджетным планам другие отделы или места возникновения затрат.

## <a name="looking-back-from-the-budget-plan"></a>Бюджетный план: взгляд в прошлое
### <a name="budget-plans-by-dimension-set-inquiry"></a>Запрос бюджетных планов по набору аналитик

Запрос **Бюджетные планы по набору аналитик** включает несколько параметров, которые позволяют выполнять запрос, чтобы идентифицировать источник данных бюджетного плана. 

Выберите строку и щелкните **Строки бюджетного плана**, чтобы запустить запрос **Строки бюджетного плана**. Результаты фильтруются для значений аналитики выбранной строки. Можно применить дополнительные параметры. 

Используйте кнопки **Прогноз поставки** и **Прогноз спроса** для выполнения этих запросов. В обоих случаях запрос ищет строки прогноза, которые могли создать строки бюджетного плана. 

Доступен также дополнительный отчет **Прогнозируемые должности по бюджетному плану**. Этот отчет особенно полезен, если нужно определить, правильно ли была выделена позиция бюджетным планам.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
