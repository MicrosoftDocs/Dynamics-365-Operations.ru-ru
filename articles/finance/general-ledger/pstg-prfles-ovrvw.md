---
title: Обзор профилей разноски
description: В этой теме объясняется, как использовать профили разноски для всех приложений Microsoft Dynamics 365.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9ad33d9a34bc449b81ec6d02a78b9ca1653aca5
ms.sourcegitcommit: 96f936267d3f314f06da6ce6f809eba2ec3b205f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2022
ms.locfileid: "8018387"
---
# <a name="posting-profiles-overview"></a>Обзор профилей разноски

В приложениях для финансов и операций термины *профили разноски* используются для описания конфигураций, которые управляют тем, как счета субкниги преобразуются в счета ГК, чтобы их можно было использовать в проводках, разнесенных в главную книгу. Например, они определяют, как клиент конвертируется в счет ГК расчетов с клиентами при разноске накладной.

Для некоторых модулей и функций имеется страница со словами "профиль разноски" в названии (например, **Профиль разноски клиента** или **Профиль разноски поставщика**). Кроме того, у некоторых модулей есть несколько вариантов настройки разноски главной книги для проводок, которые создаются из субкниги. Например, в модуле **Управление производством** можно настроить разноску по производственной группе, ресурсу или группе ресурсов.

Обратите внимание, что для многих типов проводок имеется альтернатива профилям разноски: определения разносок. Для поддерживаемых документов можно использовать определения разноски вместо профилей разноски для классификации счетов ГК и финансовых аналитик для записей учета. Если планируется использовать бюджетные обязательства или предварительные бюджетные обязательства, для определения счетов для записей учета необходимо определение разноски.

Прежде чем настраивать профили разноски, определения разносок или страницу **Счета для автоматических проводок**, необходимо настроить план счетов на странице **Главная книга** в юридическом лице, которое требуется настроить.

## <a name="posting-types"></a>Типы разноски

В приложениях для финансов и операций тип разноски используется для определения общей категории для дебета или кредита. Эта категория не зависит от счета ГК в главной книге. В главной книге имеются типы разноски для каждого дебета или кредита.

Один ваучер может иметь один или несколько типов разноски. Например, проводка, разносимая с помощью общего журнала, в которой счет и корр. счет настроены на значение **Главная книга**, будет иметь тип разноски **Журнал ГК** как для дебета, так и для кредита. И наоборот, накладная поставщика будет иметь несколько типов разноски. Эти типы разноски будут включать одну строку для сальдо поставщика и дополнительные строки для корреспондирующей записи, например **Журнал ГК**.

Вы можете просмотреть тип разноски в поле **Тип разноски** на вкладке **Общие** страницы **Проводки ваучера**.

> [!TIP]
> Можно использовать панель инструментов **Персонализация**, чтобы добавить поле **Тип разноски** в сетку на вкладку **Обзор** или переместить его. Таким образом можно сделать это поле более легким для доступа или просмотра при просмотре операций.

## <a name="detail-settings-for-a-posting-profile"></a>Подробные параметры для профиля разноски 

При настройке профилей разноски поле **Код счета** определяет уровень настройки. Доступны следующие параметры: **Таблица**, **Группа** и **Все**. Сопоставление прерывается после первого совпадения, а порядок — от самого конкретного уровня к наименее конкретному уровню. Хотя в некоторых случаях поле **Код счета** может иметь слегка отличающееся имя, поведение и функция этого поля остаются теми же. Например, профиль разноски запасов включает поле **Код номенклатуры** и поле **Код счета**. Оба поля имеют значения **Таблица**, **Группа** и **Все**.

Если поле **Счет ГК** не заполнено для профиля разноски, а счет ГК не настроен на странице **Счета для автоматической проводки** или на странице, специфической для модуля или функции, при разноске проводки, использующей данный тип разноски, будет получено сообщение об ошибке. Обычно выводится сообщение "Не удается найти счет для \[типа разноски\]".

### <a name="table-value"></a>Таблица значений

Значение **Таблица** ссылается на главную запись, связанную с профилем разноски. Каждая запись таблицы специфична для одного значения. Это значение задается в поле, которое появляется после поля **Код счета**. Обычно это поле имеет имя **Счет** или **Номер счета/группы**. Точное имя варьируется в зависимости от того, на какой странице оно отображается.

Например, если вы работаете с профилем разноски клиента, значение **Таблица** представляет конкретного клиента. Таким образом, если выбрано значение **Таблица** в поле **Код счета**, необходимо выбрать номер клиента в поле **Номер счета/группы**.

Значение **Таблица** представляет наиболее конкретный тип записи. Это значение всегда используется системой, даже если настроена другая запись, в которой выбрано значение **Группа** или **Все**. Это значение также переопределяет любые значения, которые были созданы как значения по умолчанию на странице **Счета для автоматических проводок**.

Мы не рекомендуем использовать значение **Таблица** в качестве основного механизма управления профилями разноски, так как проблемы качества данных могут возникнуть, если для каждой основной записи данных используется отдельный профиль разноски. Также сложно вести и выверять отдельный профиль разноски для каждой записи справочника. Вместо этого это значение должно использоваться для управления исключениями в профилях разноски.

### <a name="group-value"></a>Значение "Группа"

Значение **Группа** указывает на запись группировки, поддерживаемую главной записью, которая связана с профилем разноски. Каждая запись группы специфична для одного значения. Это значение задается в поле, которое появляется после поля **Код счета**. Обычно это поле имеет имя **Счет** или **Номер счета/группы**. Точное имя варьируется в зависимости от того, на какой странице оно отображается.

Для использования значения **Группа** сначала требуется настроить группу и связать ее с одной или несколькими записями для данного счета. Значение **Группа** менее конкретно, чем значение **Таблица**, но более специфическое, чем значение **Все**. Если для таблицы не настроена никакая запись, система пытается найти запись для группы, к которой принадлежит запись.

Например, если вы работаете с профилем разноски клиента, и выбрано значение **Группа** в поле **Код счета**, необходимо выбрать группу клиентов в поле **Номер счета/группы**. Необходимо предварительно определить группы клиентов на странице **Группа клиентов**, а при создании клиента необходимо указать группу клиентов.

Если необходимо отследить несколько счетов ГК для данного типа разноски, рекомендуется использовать значение **Группа**. Например, имеется три счета ГК модуля расчетов с клиентами: один для обычных клиентов, один для сотрудников и один для внутрихолдинговой продажи. В этом случае рекомендуется создать три группы клиентов для сегментирования клиентов. Затем сопоставьте каждую группу клиентов с правильным счетом ГК в профиле разноски клиента. В следующей таблице показаны три группы клиентов для данного примера.

| Группа клиентов | Имя | Описание |
|----------------|------|-------------|
| EXT | Внешний клиент | Эта группа используется для всех стандартных внешних клиентов. |
| EMP | Сотрудники | Эта группа используется для всех сотрудников, осуществляющих закупку в организации. |
| INT | Внутрихолдинговые продажи | Эта группа используется для всех счетов внутрихолдинговых клиентов, которые используются с интеграцией заказов на продажу и покупку. |

В профиле разноски затем настраиваются три строки. В каждой строке выберите значение **Группа** и связанный счет ГК.

### <a name="all-value"></a>Значение "Все"

Значение **Все** указывает, что параметры применяются ко всем записям. Если в поле **Код счета** выбрано значение **Все**, поле **Номер счета/группы** будет недоступно, и вы не сможете выбрать определенную запись, к которой будет применяться данная конфигурация.

Значение **Все** является наименее конкретным значением. Оно используется только в том случае, если система не может найти соответствие для значения **Таблица** или **Группа**. Следует выбрать значение **Все**, если имеется только один счет ГК для конкретного типа разноски.

Например, при работе с профилем разноски клиента указанные счета ГК применяются ко всем остальным клиентам и группам клиентов, у которых нет записи для определенной таблицы (клиента) или группы (группы клиентов).

### <a name="category"></a>Категория

Профили разноски запасов имеют дополнительное значение, которое относится к категории продаж или категории закупок. Это значение напоминает значение **Таблица** в том, что оно применяется только к конкретной категории продаж или покупок.

### <a name="default-value"></a>Значение по умолчанию

Если вы не создаете запись для типа разноски в профиле разноски, когда поле **Код счета** имеет значение **Все**, и система не может найти соответствующую запись профиля разноски для значения **Группа** или **Таблица**, система возвращает значение по умолчанию, которое может быть определено на странице **Счета для автоматических проводок**. Дополнительные сведения см. в разделе [Счета для автоматических проводок](accounts-for-auto-transactions.md).

## <a name="clearing-accounts"></a>Клиринговые счета

Понятие *клиринговый счет* часто используется в бухгалтерском учете. Некоторые типы разноски в приложениях Microsoft Dynamics 365 являются клиринговыми счетами. Иными словами, при разноске другой проводки сальдо в счете очищаются или реверсируются. Например, при разноске поступления продуктов заказа на покупку сумма оцененных затрат на продукты, а также налог и накладные расходы в строках заказа на покупку, разносятся на тип разноски начисления покупки в качестве задолженности. Позже, когда выставляется накладная по заказу на покупку, сальдо реверсируется от типа разноски по начислению покупки, а затем перемещается в коммерческий счет расчетов с поставщиками.

## <a name="additional-resources"></a>Дополнительные ресурсы

Многие модули в Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce и Dynamics 365 Project Operations имеют профиль разноски или дополнительные конфигурации, которые управляют тем, как работает разноска в главную книгу. Следующие разделы используются для получения дополнительных сведений о профилях разноски и настройках разноски в каждом модуле:

- [Счета для автоматических проводок](accounts-for-auto-transactions.md)
- [Разноска расчетов с поставщиками](accts-payble-posting.md)
- [Разноска расчетов с клиентами](accts-recvble-posting.md)
- [Разноска аренды активов](../asset-leasing/set-up-lease-posting-accts.md)
- Разноска управления активами (скоро)
- Управление банком и кассовыми операциями (скоро)
- Счета разноски переоценки в валюте (скоро)
- Разноска управления расходами (скоро)
- [Профиль разноски по ОС](../fixed-assets/tasks/set-up-fixed-asset-posting-profiles.md)
- Разноска внутрихолдингового учета (скоро)
- Профиль разноски запасов (скоро)
- [Разноска стоимости на складе](../../supply-chain/landed-cost/costing-parameters-setup.md)
- [Обзор определений разносок](posting-definitions.md)
- Разноска управления производством (скоро)
- Разноска управления и учета по проектам (скоро)
- Разноска управления услугами (скоро)
- Разноска налога (скоро)
- Разноска времени и посещаемости (скоро)
- Разноска управления транспортировкой (скоро)
- Профили разноски управления ретробонусами (скоро)