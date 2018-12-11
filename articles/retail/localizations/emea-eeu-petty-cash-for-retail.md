---
title: "Управление мелкими наличными деньгами для Retail для Восточной Европы"
description: "В этом разделе описывается, как настроить и использовать возможности управления кассой в Retail для Восточной Европы."
author: epopov
manager: annbe
ms.date: 10/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: 01239f0eff3e59f62188fca64f99e93be843d2e2
ms.openlocfilehash: c198cedba9268229dc1057711d9f16ca33acebac
ms.contentlocale: ru-ru
ms.lasthandoff: 10/24/2018

---

# <a name="petty-cash-management-for-retail-for-eastern-europe"></a>Управление мелкими наличными деньгами для Retail для Восточной Европы

[!include [banner](../includes/banner.md)]

Данная статья содержит сведения о локализации для Восточной Европы, специфичной для отрасли розничной торговли. 

В соответствии с требованиями бухгалтерской отчетности Восточной Европы можно настроить операции для наличных счетов, чтобы автоматизировать процессы, кассовые документы и кассовые отчеты. Дополнительные сведения см. в разделе [(EEUR) Настройка параметров управления кассами](https://docs.microsoft.com/en-us/dynamicsax-2012/appuser-itpro/eeur-set-up-parameters-for-cash-management). 

Продавцы могут принимать различные типы платежей в обмен на продукты и услуги, которые они продают. Хотя наличные деньги — наиболее распространенная форма оплаты, розничные магазины также могут принимать чеки, карты или ваучеры. В розничном POS-терминале наличные деньги, платежи по кредитным картам и другие платежи обрабатываются в операционной кассе.

С помощью функцию управления кассами в Retail можно выполнять следующие задачи:

- Создание кассы для выбранного способа оплаты для каждого розничного магазина.
- Использование кассовых журналов для разноски проводок по кассе и платежей клиентов, получаемые в розничном POS-терминале.
- Объединение проводок в строку отчета при разноске журнала операций розницы. Можно объединять сдачи наличных в сейф, инкассации, проводки по ваучерам, проводки удаления платежных средств, проводки внесения денежных средств, проводки доходов, проводки расходов, платежи клиентов, проводки по продажам и проводки возврата.

Все проводки, которые выполняются в розничном POS-терминале, разносятся с использованием журнала ГК. Можно воспользоваться журналами наличной оплаты, журналами платежей клиентов и общими журналами для создания и разноски отчетов. Дополнительные сведения см. в разделе [Создание, расчет и разноска журналов операций для розничного магазина](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/tasks/create-calculate-post-statement-retail-store).

На странице **Разнесенные журналы операций** в области действий можно выполнить следующие действия:
  - Выберите **Запросы > Журнал наличных платежей**, чтобы получить доступ к журналу наличных платежей, связанных с отчетом.
  - Выберите **Запросы > Общий журнал**, чтобы получить доступ к журналам ГК по отчету, за исключением платежей клиентов или кассовых платежей.

## <a name="set-up-for-cash-management-for-retail-pos"></a>Настройка управления денежными средствами для Retail POS

Необходимо выполнить следующую процедуру настройки, прежде чем можно будет использовать управление денежными средствами в модуле Retail:
- Настройте способ оплаты для каждого типа платежа, принимаемого продавцом, на странице **Способы оплаты**. Для разности проводок в Retail POS можно использовать различные методы оплаты. Дополнительные сведения о способах оплаты в Retail см. в разделе [Способы оплаты](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/payment-methods).

- Настройка розничных параметров кассовых операций.

- Настройка способа оплаты наличными в розничном магазине.

### <a name="set-up-retail-parameters-for-cash-operations"></a>Настройка розничных параметров кассовых операций

Можно настроить параметры для создания и разноски проводок по кассе в модуле Retail. Можно использовать журналы оплаты наличными, журналы платежей клиентов или общие журналы для разноски проводок по продажам и платежам в Retail POS. Можно объединять проводок с одинаковыми свойствами при разноске отчета. 

1. Перейдите в раздел **Розничная торговля > Настройка центрального офиса > Параметры > Параметры розничной торговли**. В левой области щелкните **Разноска**.

2. В области **Разноска** на экспресс-вкладке **Агрегирование** установите для параметра **Внесение/изъятие наличности** значение **Да**, чтобы объединять проводки удаления платежного средства или внесения остатка, связанные со строкой отчета, при разноске отчета. Проводка удаления платежного средства создается при изъятии наличности из ящика POS-терминала. Проводка внесения остатка создается при помещении наличности в ящик POS-терминала.

3. Включите отдельные параметры, перечисленные ниже, для суммирования проводок, связанных со строкой отчета, при разноске отчета:
   - **Инкассация** — суммируются банковские проводки.
   - **Сдача наличных средств в сейф** — суммируются сейфовые проводки.
   - **Проводки по доходам/расходам** — суммируются проводки по доходам или проводки по расходам.
   - **Проводки ваучера** — суммируются проводки по ваучерам.
   - **Платежи клиентов** — суммируются платежи клиентов.
   - **Продажи и возвраты** — суммируются проводки продаж и возвратов.

4. На экспресс-вкладке **Платежи** выберите наименование журнала по умолчанию для следующих параметров:
     - **Журнал платежей клиентов** — этот журнал используется для разноски оплаты клиентов.
     - **Журнал наличных платежей** — этот журнал используется для разноски наличных платежей.
     - **Общий журнал** — этот журнал используется для разноски проводок, не являющихся проводками оплаты клиентов или проводками наличной оплаты.

### <a name="set-up-a-payment-method-for-cash-payments-in-a-retail-store"></a>Настройка способа оплаты наличными в розничном магазине

Следующая процедура служит для настройки способа оплаты наличными в розничном магазине.

1. Перейдите в раздел **Розничная торговля > Розничные магазины > Все розничные магазины**.

2. На странице списка **Все розничные магазины** выберите магазин, для которого необходимо настроить способ оплаты.

3. На панели области действий на вкладке **Настройка** в группе **Настройка** щелкните **Способы оплаты**.

4. На странице **Способ оплаты** создайте или выберите способ оплаты. 

5. На экспресс-вкладке **Разноска** в группе полей **Счет** в поле **Тип счета** выберите **Кассовый счет**.

   > [!NOTE]
    > Можно выбрать **Кассовый счет** в поле **Тип счета** только в том случае, если выбрано значение **Обычная** или **Внесение/изъятие наличности** в поле **Функция**.

6. В поле **Номер счета** выберите номер кассового счета для способа оплаты.

7. В группе полей **Внесение/изъятие наличности** в поле **Корр. счет** выберите корр. счета для разноски проводок удаления платежного средства или ввода остатка для способа оплаты.

> [!NOTE]
> Необходимо настроить корр. счета как для способ оплаты наличными, так и для способа оплаты удаления платежного средства и ввода остатка для магазина. При этом создаются сбалансированные записи ГК для проводок удаления платежного средства и ввода остатка.
