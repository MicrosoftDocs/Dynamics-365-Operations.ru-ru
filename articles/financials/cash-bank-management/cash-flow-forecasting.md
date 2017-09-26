---
title: "Прогнозирование движения денежных средств"
description: "В этом разделе представлен обзор процесса прогноза движения денежных средств. Здесь также объясняется, как прогноз движения денежных средств интегрируется с другими модулями в системе."
author: saraschi
manager: AnnBe
ms.date: 05/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: sarasch
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 3abf4b151b177095b71d44e9a6c9fd8541eaa64e
ms.openlocfilehash: a8ccd99431178c3cb4e73e7cd199de8e0845d716
ms.contentlocale: ru-ru
ms.lasthandoff: 06/14/2017

---

# <a name="cash-flow-forecasting"></a>Прогнозирование движения денежных средств

[!include[banner](../includes/banner.md)]

Инструменты прогноза движения денежных средств для анализа будущих потоков денежных средств и определения потребности в валюте можно использовать для оценки будущей потребности компании в наличных деньгах. Чтобы получить прогноз движения денежных средств, необходимо выполнить следующие действия:

- Определите и составьте список всех счетов денежных средств. Счета денежных средств — это счета компании для наличных денег или эквивалентов денежных средств.
- Настроить прогнозы по проводкам, влияющим на счета денежных средств компании.

После выполнения этих задач можно рассчитать и проанализировать прогнозы движения денежных средств и будущие потребности в валюте.

## <a name="cash-flow-forecasting-integration"></a>Интеграция прогноза движения денежных средств

Прогноз движения денежных средств интегрируется с модулями "Главная книга", "Расчеты с клиентами", "Расчеты с поставщиками", "Бюджетирование и управление запасами". Процесс прогнозирования использует сведения о проводке, введенной в системе, и процесс расчета прогнозирует ожидаемое влияние денежных средств каждой проводки. Следующие типы проводок учитываются при расчете движения денежных средств.

- **Заказы на продажу**, по которым еще не были выставлены накладные и которые приводят к физическим или финансовым продажам.
- **Заказы на покупку**, по которым еще не были выставлены накладные, и которые приводят к физическим или финансовым покупкам.
- **Расчеты с клиентами** — открытые проводки клиента (накладные, которые еще не оплачены).
- **Расчеты с поставщиками** — открытые проводки по поставщику (накладные, которые еще не оплачены).
- **Проводки ГК**,, в которых указано, что будущая разноска будет выполнена.
- **Записи бюджетного регистра**, выбранные для прогнозов движения денежных средств.
- **Прогнозы спроса** — строки модели прогноза запасов, выбранные для прогнозов движения денежных средств.
- **Прогнозы поставки** — строки модели прогноза запасов, выбранные для прогнозов движения денежных средств.

Несмотря на то что не существует прямой интеграции с управлением и учетом по проектам, существует несколько способов, чтобы включить проводки по проекту в прогноз движения денежных средств. Разнесенные накладные по проекту включаются в прогноз как часть открытых проводок по клиенту. Инициированные проектом заказы на продажу и заказы на покупку включены в прогноз как открытые заказы после их ввода в системе. Можно также перемещать прогнозы проекта в модель бюджета ГК. Затем эта модель бюджета ГК включается в прогноз движения денежных средств как часть записей регистра бюджета.

## <a name="configuration"></a>Конфигурация

Для настройки процесса прогноза движения денежных средств используйте страницу **Настройка прогноза движения денежных средств**. На этой странице указываются счета денежных средств для отслеживания и поведение прогнозирования по умолчанию для каждой области.

### <a name="general-ledger"></a>Главная книга

Необходимо сначала определить счета денежных средств, которые требуется отслеживать для прогноза движения денежных средств. Как правило, эти счета денежных средств — счета ГК, которые связаны с банковскими счетами, которые будут получать и выплачивать денежные средства. На странице **Настройка прогноза движения денежных средств** на вкладке **Главная книга** выберите счета ГК, чтобы включить их для прогнозирования. Если банковский счет был связан со счетом ГК на странице **Банковский счет**, он будет отображаться в поле **Банковский счет**.

Можно настроить зависимый прогноз движения денежных средств для счета ГК, который содержит проводки, непосредственно связанные с проводками в другом счете ГК. Каждая строка, которая добавляется в разделе **Зависимые счета** создает сумму прогноза движения денежных средств в зависимом счете ГК. Эта сумма представляет собой процент от сумм движения денежных средств по выбранному основному счету ГК.

Сначала задайте поле **Счет ГК** для основного счета ГК, где ожидаются первоначальные проводки. Настройте поле **Зависимый счет ГК** для счета, на который повлияет первоначальная проводка по основному счету ГК. Задайте соответствующие значения в других полях в строке. Можно изменить значение, отображаемое в поле **Процент**, чтобы отразить влияние основного счета ГК на зависимый счет ГК. Для прогноза продаж или покупок выберите значение **Условия оплаты**, которое является типичным для большинства клиентов или поставщиков. Настройте поле **Тип разноски** для ожидаемого типа разноски, связанного с прогнозом движения денежных средств.

### <a name="accounts-payable"></a>Расчеты с поставщиками

Можно рассчитать прогноз для покупок с использованием параметров настройки на вкладке **Расчеты с поставщиками** страницы **Настройка прогноза движения денежных средств**. Перед настройкой прогнозирования движения денежных средств для расчетов с поставщиками необходимо настроить условия оплаты, группы поставщиков и профили разноски поставщиков.

В разделе **Значения по умолчанию для прогноза по закупкам** можно выбрать поведение при покупке по умолчанию для прогнозирования движения денежных средств. Три поля определяют времени влияния денежных средств: **Время между датой доставки и датой накладной**, **Условия оплаты** и **Время между сроком накладной и датой платежа**. Прогноз будет использовать значение по умолчанию для поля **Условия оплаты**, только если значение не указано в проводке. Используйте условия оплаты для описания наиболее типичного числа дней для каждой части процесса.

Поле **Счета денежных средств для платежей** определяет счет денежных средств, который чаще всего используется для платежей. Используйте поле **Процент от суммы для распределения в прогноз движения денежных средств** для указания, следует ли использовать процент от суммы во время прогнозирование. Оставьте это поле пустым, если суммы полной проводки должны использоваться при прогнозировании.

Можно переопределить настройку по умолчанию для поля **Время между сроком накладной и датой платежа** для конкретных групп поставщиков. Прогноз будет использовать значение по умолчанию из раздела **Значения по умолчанию для прогноза по закупкам**, если не указано другое значение для группы поставщиков, связанной с поставщиком по проводке. Чтобы переопределить значение по умолчанию, выберите группу поставщиков и задайте новое значение для поля **Время покупки**.

Можно переопределить настройку по умолчанию для поля **Счет денежных средств** для конкретных профилей разноски по поставщикам. Прогноз будет использовать значение по умолчанию из раздела **Значения по умолчанию для прогноза по закупкам**, если не указан другой счет денежных средств для профиля разности, связанного с поставщиком по проводке. Чтобы переопределить значение по умолчанию, выберите профиль разноски, а затем укажите счет денежных средств, который должен быть затронут.

### <a name="accounts-receivable"></a>Расчеты с клиентами

Можно рассчитать прогноз для продаж с использованием параметров настройки на вкладке **Расчеты с клиентами** страницы **Настройка прогноза движения денежных средств**. Перед настройкой прогнозирования движения денежных средств для расчетов с клиентами необходимо настроить условия оплаты, группы клиентов и профили разноски клиентов.

В разделе **Значения по умолчанию для прогноза по продажам** можно выбрать поведение при продаже по умолчанию для прогнозирования движения денежных средств. Три поля определяют времени влияния денежных средств: **Время между датой отгрузки и датой накладной**, **Условия оплаты** и **Время между сроком накладной и датой платежа**. Прогноз будет использовать значение по умолчанию для поля **Условия оплаты**, только если значение не указано в проводке. Используйте условия оплаты для описания наиболее типичного числа дней для каждой части процесса. 

Поле **Счета денежных средств для платежей** определяет счет денежных средств, который чаще всего используется для платежей. Используйте поле **Процент от суммы для распределения в прогноз движения денежных средств** для указания, следует ли использовать процент от суммы во время прогнозирование. Оставьте это поле пустым, если суммы полной проводки должны использоваться при прогнозировании.

Можно переопределить настройку по умолчанию для поля **Время между сроком накладной и датой платежа** для конкретных групп клиентов. Прогноз будет использовать значение по умолчанию из раздела **Значения по умолчанию для прогноза по продажам**, если не указано другое значение для группы клиентов, связанной с клиентом по проводке. Чтобы переопределить значение по умолчанию, выберите группу клиентов и задайте новое значение для поля **Время продажи**.

Можно переопределить настройку по умолчанию для поля **Счет денежных средств** для конкретных профилей разноски по клиентам. Прогноз будет использовать значение по умолчанию из раздела **Значения по умолчанию для прогноза по продажам**, если не указан другой счет денежных средств для профиля разности, связанного с клиентом по проводке. Чтобы переопределить значение по умолчанию, выберите профиль разноски, а затем укажите счет денежных средств, который должен быть затронут.

### <a name="budgeting"></a>Бюджетирование

Бюджеты, созданные на основе бюджетных моделей, можно включать в прогнозы движения денежных средств. На вкладке **Бюджетирование** на странице **Настройка прогноза движения денежных средств** выберите бюджетные модели для включения в прогноз. По умолчанию новые записи регистра бюджета включаются в прогнозы после активации бюджетной модели для прогнозирования движения денежных средств. Включение в прогнозирование движений денежных средств можно перезаписать для отдельных записей регистра бюджета.

### <a name="inventory-management"></a>Управление запасами

Прогнозы предложения и спроса запасов могут быть включены в прогнозы движения денежных средств. На вкладке **Управление запасами** на странице **Настройка прогноза движения денежных средств** выберите модель прогноза для включения в прогноз движения денежных средств. Включение в прогнозирование движений денежных средств можно перезаписать для отдельных строк прогноза предложения и спроса.

### <a name="calculation"></a>Расчет

Перед просмотром аналитики по прогнозам движения денежных средств необходимо запустить процесс расчета движения денежных средств. Процесс вычисления спроецирует будущее влияние денежных средств проводок, которые были введены.

Рассчитайте прогноз движения денежных средств на странице **Рассчитать прогнозы движения денежных средств**. Можно рассчитать либо полный, либо пошаговый прогноз движения денежных средств. 

- Чтобы очистить все проводки прогноза движения денежных средств и сделать перерасчет, задайте в поле **Метод расчета прогноза движения денежных средств** значение **Итого**. Рекомендуется использовать этот подход, если вы еще не обновляли прогнозы движения денежных средств в течение длительного времени. 
- Для обновления существующих данных по движению денежных средств только для новых проводок задайте в поле **Метод расчета прогноза движения денежных средств** значение **Создать**. На странице будет указана дата последнего выполнения расчета движения денежных средств.

Можно также использовать пакетную обработку для прогнозирования движения денежных средств. Чтобы гарантировать, что аналитика прогнозирования регулярно обновляется, настройте повторяющийся процесс пакетной обработки для расчета прогноза движения денежных средств.

### <a name="reporting"></a>Отчетность

После расчета прогноза движения денежных средств необходимо обновить связанные с объектом сведения для аналитических отчетов. На странице **Хранилище объектов** выберите измерение **Агрегат LedgerCovLiquidityMeasurement**, а затем щелкните **Обновить**.

Существует две рабочих области, которые содержат данные прогноза движения денежных средств. Одна рабочая область содержит данные для всех компаний, а другая — данные только для текущей компании.

Доступ к рабочей области для всех компаний управляется с помощью полномочия **Просмотр рабочей области движения денежных средств всех компаний**. По умолчанию рабочая область **Обзор кассы — все компании** доступна для следующих ролей:

- Генеральный директор
- Финансовый директор
- Финансовый контролер

Доступ к рабочей области для текущей компании управляется только с помощью полномочия **Просмотр рабочей области движения денежных средств текущей компании**. По умолчанию рабочая область **Обзор кассы — текущая компания** доступна для следующих ролей:

- Бухгалтер
- Главный бухгалтер
- Супервизор по учету
- Менеджер по расчету с поставщиками
- Менеджер по расчету с клиентами

В рабочей области **Обзор кассы — все компании** показана аналитика прогнозирования движения денежных средств в валюте системы. Валюта системы и тип валютного курса системы, которые используются для аналитики, определяются на странице **Параметры системы**. Эта рабочая область содержит обзор прогнозирования движения денежных средств и сальдо банковского счета для всех компаний. Диаграмма поступления и расхода денежных содержит обзор прогнозируемого движения денежных средств и сальдо в валюте системы, вместе с подробными сведениями о прогнозируемых проводках. Можно также просмотреть прогнозируемое сальдо по валюте.

В рабочей области **Обзор кассы — текущая компания** показана аналитика прогнозирования движения денежных средств в валюте компании, заданной по умолчанию. Валюта по умолчанию, используемая для аналитики, определена на странице **Главная книга**. Эта рабочая область содержит обзор прогнозирования движения денежных средств и сальдо банковского счета для текущей компании. Диаграмма поступления и расхода денежных содержит обзор прогнозируемого движения денежных средств и сальдо в валюте учета, вместе с подробными сведениями о прогнозируемых проводках. Можно также просмотреть прогнозируемое сальдо по валюте.

Дополнительные сведения об аналитике прогноза движения денежных средств см. тему обзора денежных средств содержимого Power BI.

Кроме того, можно просмотреть данные прогноза движения денежных средств для конкретных счетов, заказов и номенклатур на следующих страницах:

- **Пробный баланс**: выберите **Прогнозы движения денежных средств** для просмотра будущего движения денежных средств для выбранного счета ГК.
- **Все заказы на продажу**: на вкладке **Накладная** выберите **Прогнозы движения денежных средств** для просмотра прогнозируемого влияния денежных средств по выбранному заказу на продажу.
- **Все заказы на покупку**: на вкладке **Накладная** выберите **Прогнозы движения денежных средств** для просмотра прогнозируемого влияния денежных средств по выбранному заказу на покупку.
- **Прогноз поставки**: выберите **Прогнозы движения денежных средств** для просмотра будущего движения денежных средств, которое связано с выбранным прогнозом поставки номенклатуры.
- **Прогноз спроса**: выберите **Прогнозы движения денежных средств** для просмотра будущего движения денежных средств, которое связано с выбранным прогнозом спроса номенклатуры.

