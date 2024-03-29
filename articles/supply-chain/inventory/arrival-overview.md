---
title: Обзор прибытия
description: В этой статье представлена информация о функции обзора прибытия. Страница обзора прибытия является частью этой функции и представляет обзор всех номенклатур, прибытие которых ожидается в качестве входящих номенклатур.
author: yufeihuang
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverview, WMSArrivalOverviewProfile, WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "274363"
- intro-internal
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 8118db9469c01c43b23c64ee383ac1d383a0ba7a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874082"
---
# <a name="arrival-overview"></a>Обзор прибытия

[!include [banner](../includes/banner.md)]

В этой статье представлена информация о функции обзора прибытия. Страница обзора прибытия является частью этой функции и представляет обзор всех номенклатур, прибытие которых ожидается в качестве входящих номенклатур.

Страница **Обзор прибытия** представляет обзор всех ожидаемых входящих номенклатур. На ней также отображаются прибытия, которые можно инициализировать на основании обзора. Эта статья посвящена процессу получения.

## <a name="business-scenario"></a>Бизнес-сценарий
Рассмотрим следующий сценарий во входящих процессах.

[![Бизнес-сценарий.](./media/arrival-overview-scenario.png)](./media/arrival-overview-scenario.png)

Сотрудник приемки Сэмми хочет узнать, что ожидается к прибытию на текущий день. На странице **Обзор прибытия** Сэмми может посмотреть обзор текущих задач и грубую оценку количества, объема, веса, различных типов заказов и т. д. Позже поставка прибывает на один из дебаркадеров приемки, и Сэмми получает список поставки. На странице **Обзор прибытия** Сэмми может выполнять следующие задачи.

-   Найти соответствующий приходный ордер и зарегистрировать поступление как **В обработке**. Автоматически создаются строки, которые необходимы для регистрации, и приход можно контролировать, даже если проводки еще не была разнесены как **Зарегистрировано**.
-   Откройте соответствующую ссылку журнала прибытия (то есть, журнал **Прибытие номенклатуры** или журнал **Получение из производства**) и найдите журналы, готовые для обновления поступления продуктов.

## <a name="arrival-overview-page"></a>Страница обзора прибытия
Чтобы открыть страницу **Обзор прибытия**, щелкните **Управление запасами** &gt; **Входящие заказы** &gt; **Обзор прибытия**. Можно просмотреть список заказов, получение которых ожидается. Обзор разделен на заголовок и строки. Сведения заголовка группируются по типу заказа, ожидаемой дате поступления и пункту назначения поставки. При выборе строки заголовка для прибытия все строки сведений, связанные со ссылкой поступления, выбираются для прибытия в части подробных сведений строки на этой странице. После разноски всех соответствующих строк журнала эта информация не отображается.

### <a name="arrival-overview-profiles"></a>Профили обзора прибытия

Страница **Обзор прибытия** представляет обзор ожидаемых номенклатур и дату ожидаемого прибытия. В процессе прибытия можно использовать несколько наборов личных параметров. Отдельные пользователи могут определить свои собственные настройки на странице **Профили обзора прибытия**.

### <a name="set-up-item-arrival"></a>Настройка прибытия номенклатуры

В данном примере Сэмми хочет настроить новый компьютер в местоположении, который будет использоваться для получения готовой продукции, полученной из производства на сайте 1. На странице **Профили обзора прибытия** Сэмми создает новую настройку, которая называется **Производство на сайте 1** и задает следующие параметры.

1.  На экспресс-вкладке **Параметры прибытия** в группе полей **Диапазон** введите сведения об интервале дней и складах, которые требуется включить в обзор.
2.  На экспресс-вкладке **Параметры прибытия** в группе полей **Журнал** введите склад приемки, местоположение и имя журнала (прибытие номенклатуры/получение из производства).
3.  На экспресс-вкладке **Сведения о запросе прибытия** в группе полей **Сайт** в поле **Ограничить по сайту** введите сайт для ограничения отображаемых элементов в области обзора.
4.  На экспресс-вкладке **Сведения о запросе прибытия** в группе полей **Показанные типы проводок** задайте для параметра **Производственные заказы** значение **Да**.
5.  На экспресс-вкладке **Сведения о запросе прибытия** в группе **Разное** задайте для параметра **Обновить при запуске** значение **Да**, если представление должно автоматически обновляться при запуске. Задайте для параметра **Обновлять при изменении диапазона** значение **Да**, если представление должно автоматически обновляться при изменении значений диапазона.

В этом примере в поле **Имя профиля обзор прибытия** на экспресс-вкладке **Параметры прибытия** страницы **Обзор прибытия** установлено значение **Производство на сайте 1**.

### <a name="prerequisites-for-arrival-journals"></a>Предварительные требования для журналов прибытия

Чтобы автоматически создавать журналы прибытия со страницы **Обзор прибытия**, необходимо определить соответствующие сведения в группе полей **Журнал** на экспресс-вкладке **Параметры прибытия**.

-   Необходимо указать имя журнала при создании журнала.

[![Указание имени журнала.](./media/arrival-overview-journal.png)](./media/arrival-overview-journal.png)

-   Если задать значения в полях **Склад** и **Местоположение**, эти значения используются в строках журнала. Если не указать значения, система использует значения из аналитики, которая указана в складских проводках.

#### <a name="items-that-are-received-from-one-expected-receipt-order"></a>Номенклатуры, которые получены из одного ожидаемого приходного ордера

На экспресс-вкладке **Поступления** Сэмми выбирает строку, затем нажимает **Начать прибытие**. Все связанные строки, которые находятся в указанном диапазоне и имеют количество для регистрации, автоматически выбираются. Создается журнал прихода номенклатуры, который содержит соответствие между ожидаемым приходным ордером и журналом. Количество автоматически инициализируется во всех строках, которые были созданы.

#### <a name="items-that-are-received-from-more-than-one-expected-receipt-order"></a>Номенклатуры, которые получены из нескольких ожидаемых приходных ордеров

На экспресс-вкладке **Поступления** Сэмми выбирает несколько строк, затем нажимает **Начать прибытие**. Создается журнал прихода номенклатуры, который содержит соответствие между всеми ожидаемыми приходными ордерами и журналом. Все строки создаются для одного заголовка журнала прибытия номенклатуры, и количество инициализируется автоматически.

### <a name="receive-items-from-one-or-more-expected-receipt-orders"></a>Получение номенклатур получены из одного или нескольких ожидаемых приходных ордеров

#### <a name="view-information"></a>Просмотр сведений

Для получения обзора ожидаемых приходов в интервале дат Сэмми вводит следующие сведения в поля на экспресс-вкладке **Параметры прибытия** страницы **Обзор прибытия**, затем щелкает **Обновить** для обновления этого представления:

-   Имя профиля обзора прибытия: **Запрос**
-   Показать строки: **Все**
-   Дней назад: (Пусто)
-   Дней вперед: **0**
-   Склады: **GW, MW**

Сэмми может просмотреть следующую информацию:

-   Все связанные приходные ордера для данной системной даты и неограниченного числа дней в прошлом от нее (интервал **InventTrans.StatusDate**), а также поступления для складов GW и MW, независимо от статуса.
-   Подробные сведения о строке для более чем одного ордера. Сэмми может выбрать несколько строк заголовка в обзоре и щелкнуть **Показать все выбранные** для просмотра всех соответствующих сведений о строках для всех выбранных заказов.
-   Информация о конкретном заказе на покупку. Чтобы отобразить только сведения, относящиеся к конкретному номеру ссылки в обзоре, Сэмми может ввести номер счета в поле **Номер счета** и номер заказа в поле **Номер ссылки**.
-   Обзор задач регистрации, которые должны быть выполнены для всех строк заказа, для которых был создан журнала прихода номенклатур, но которые еще не были разнесены. Чтобы просмотреть эти сведения, Сэмми может выбрать **Выполняется** в поле **Показать строки**.

### <a name="update-journals"></a>Обновление журналов

Чтобы зарегистрировать одну или несколько строк заказа, которые необходимо обработать, Сэмми может выбрать строки в сетке обзора или в сетке строк, затем нажать выбрать **Журналы** &gt; **Показать прибытия по приходам**. Отображаются заголовки прибытия номенклатуры, которые соответствуют строкам. Для обновления поступления продуктов по заказу на покупку для зарегистрированных номенклатур Сэмми может использовать заголовки журнала прибытия номенклатуры, готовые для обновления. Чтобы получить доступ к этим заголовкам журнала прибытия номенклатуры, он щелкает **Журналы** &gt; **Готовые журналы поступлений продуктов**. Отображаются все строки заголовка, готовые для обновления поступления продуктов в указанном диапазоне склада. (Заголовок строки, которые будут отображаться, не связаны с интервалом дней.)

### <a name="start-an-arrival-registration"></a>Запуск регистрации прибытия

Выбрав несколько строк на странице **Обзор прибытия**, Сэмми может запустить прибытие нескольких ссылок прихода. Когда он выбирает строку из обзора приходов, выбираются сведения из соответствующей строки. Если количество для регистрации существует, доступна кнопка **Начать прибытие**. Сэмми может использовать два метода для запуска регистрации прибытия:

-   Отфильтровать страницу таким образом, чтобы отобразить только те записи, которые соответствуют определенным условиям в поле **Ссылка на поставщика**, отсканировать ссылочный номер поставщика, например штрих-код транспортной накладной.
-   В части обзора или части сведений страницы **Обзор прибытия** вручную выберите или отмените выбор записей для регистрации прибытия. Затем, когда Сэмми нажимает кнопку **Начать прибытие**, выбранные записи автоматически создаются в журнале прибытия номенклатуры. Эти записи включают сведения о строке, и все уникальные данные полей назначены.

## <a name="update-arrival-information-and-process-a-product-receipt"></a>Обновление сведений о приходе и обработка поступления продуктов
После регистрации всех товаров начальник склада или менеджер по закупкам может обновить полученные номенклатуры в поступлении продуктов, добавляя физическую стоимость. Чтобы обновить сведения о приходе и разнести поступление продуктов, выполните следующие действия.

1.  Щелкните **Управление запасами** &gt; **Входящие заказы** &gt; **Обзор прибытия**.
2.  На странице **Обзор прибытия** щелкните **Журналы** &gt; **Готовые журналы поступлений продуктов** для отображения списка журналов, готовых для обновления поступления продуктов.
3.  Выбор журналов, которые должны быть обновлены, затем щелкните **Функции** &gt; **Поступление продуктов**.
4.  На странице **Разноска** введите номер поступления продуктов, если он еще не доступен в журнале, и нажмите кнопку **OK** для обработки поступления продуктов.

## <a name="summary"></a>Сводка
Страница **Обзор прибытия** может помочь менеджеру склада и складским работникам получить обзор ожидаемой работы, которая должна быть выполнена в рамках процесса обработки поступлений. Эту страницу можно также использоваться для запуска процесса прибытия номенклатуры, позволяя гарантировать, что номенклатуры отслеживаются при первом поступлении на склад.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]