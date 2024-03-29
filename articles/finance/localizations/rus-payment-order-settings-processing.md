---
title: Настройка и обработка платежных поручений для России
description: В этой статье объясняется, как настраивать и обрабатывать платежные поручения для России.
author: AdamTrukawka
ms.date: 10/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: atrukawk
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a3de9f5b6159e26577726a9f7ddfb2306a487afb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280628"
---
# <a name="set-up-and-process-payment-orders-for-russia"></a>Настройка и обработка платежных поручений для России

[!include [banner](../includes/banner.md)]

## <a name="setup-for-generating-payment-orders"></a>Настройка для формирования платежных поручений

Прежде чем формировать платежные поручения, необходимо настроить следующее:

- Настроить банки и банковские счета для компании. Дополнительные сведения см. в разделе [Локальные настройки и реквизиты для модуля "Банк"](rus-local-settings-requisites-bank-module.md).
- Настроить банковские счета поставщиков и банковские счета клиентов:

    1. На странице "Все клиенты" или "Все поставщики" выберите **Банковские счета** на вкладке **ПОСТАВЩИК**.
    2. Создайте банковский счет и введите все необходимые данные.
    3. В случае банковских счетов зарубежных клиентов или поставщиков на экспресс-вкладке **Общие** в разделе **Иностранный банк** в поле **Банковские группы** выберите код иностранного банка, в котором зарегистрирован банковский счет клиента. В поле **Номер банковского счета** введите номер иностранного банковского счета, на который будут поступать платежи. Наконец, в поле **SWIFT** введите SWIFT-код банка, получающего платежи.

    ![Банковский счет поставщика.](media/rus-vendor-bank-account-screenshot-5.jpg)

- Для формирования платежей поставщикам настройте способ оплаты в разделе **Расчеты с поставщиками \> Настройка платежей \> Способы оплаты**. Для формирования возвратов платежей клиентам настройте способ оплаты в разделе **Расчеты с клиентами \> Настройка платежей \> Способы оплаты**.
- Для печати платежных поручений в российских рублях в соответствии с форматом бумаги на странице **Способы оплаты** на экспресс-вкладке **Форматы файлов** в поле **Формат экспорта** выберите **Платежное поручение в рублях**. Для печати платежных поручений в иностранной валюте в соответствии с шаблоном конкретного банка в поле **Формат экспорта** выберите **Валютное платежное поручение**. (Шаблон для конкретного банка определяется в банковском счете).

## <a name="generate-a-payment-order-in-russian-rubles-for-a-payment-to-a-vendor"></a>Создание платежного поручения в российских рублях для платежа поставщику

### <a name="create-payment-order-lines"></a>Создание строк платежного поручения
Прежде чем формировать платежное поручение, необходимо создать строки платежного поручения.

1. Выберите **Расчеты с поставщиками \> Платежи \> Журнал платежей**.
2. Создайте журнал, а затем в области действий выберите **Строки**, чтобы открыть страницу **Платежи поставщикам**.
3. Создайте строку платежа поставщику.
4. В поле **Дата** укажите дату платежа.
5. В поле **Счет** выберите счет поставщика.
6. В поле **Текст проводки** введите описание проводки.
7. В поле **Дебет** введите сумму платежа.
8. В поле **Валюта** выберите код валюты.
9. В поле **Тип корр. счета** выберите тип выбранного счета.
10. В поле **Корр. счет** выберите корреспондентский счет для проводки.
11. В поле **Валюта** выберите код валюты.
12. В поле **Способ оплаты** выберите способ оплаты, который будет использоваться для поставщика.
13. В поле **Код договора** выберите регистрационный номер договора.
14. В полях **Налоговая группа** и **Налоговая группа номенклатур** выберите налоговые группы для вычисления НДС.
15. На вкладке **Банк** в поле **Тип банковской проводки** выберите тип проводки.
16. В поле **Идентификатор счета** выберите банковский счет получателя.

    > [!IMPORTANT]
    > Если платежное поручение создается для юридического лица поставщика, необходимо ввести счет поставщика в поле **Платежка на**. В этом случае бланк платежного поручения будет ссылаться на банк поставщика, указанный в поле **Платежка на**. Однако проводка будет произведена для поставщика, указанного в поле **Счета**.

17. На вкладке **Платежное поручение** в поле **Назначение платежа** введите текст, который должен быть отражен в платежном поручении.

    Если выбрать **НДС в платежном поручении** будет введен текст. Этот текст включает в себя сумму НДС в поле **Назначение платежа**.

19. Задайте следующие поля: **Очередность платежа**, **Код статуса**, **Код доходов бюджета**, **Основание платежа**, **Вид платежа**, **УИН**, а также поля в разделе **Период** (**Код периода**, **Номер периода**, **Год**, **Дата периода**). Эти значения будут напечатаны в соответствующих полях платежного поручения для поставщика или налогового органа.

    ![Платежи Поставщику.](media/rus-vendor-payments-screenshot-4.jpg)

### <a name="generate-a-payment-order"></a>Создание платежного поручения
После создания строк платежного поручения можно сформировать платежное поручение.

1. На странице **Платежи поставщикам** в области действий выберите **Создание платежей**, чтобы открыть диалоговое окно **Создание платежей**.
2. В поле **Способ оплаты** выберите способ оплаты. Другой вариант — в поле **Формат экспорта** выберите **Платежное поручение в рублях**.
3. В поле **Банковский счет** выберите банковский счет, с которого будет произведен платеж.
4. Выберите **OK**, чтобы открыть диалоговое окно **Настройка платежного поручения**. 
5. Установите для параметра **Документ** значение **Да**, чтобы напечатать платежное поручение, и установите для параметра **Текст доверенности** значение **Да**, чтобы напечатать текст.
6. Нажмите **ОК**. Создается платежное поручение, а статус платежа для соответствующей строки журнала платежей изменяется на **Отправлено**.

### <a name="void-a-payment-order"></a>Аннулирование платежного поручения

Аннулировать платежное поручение можно в журнале платежей. На странице **Платежи поставщикам** в области действий выберите **Функции \> Аннулировать п/п**. Статус оплаты строки журнала платежей для аннулированного платежа меняется на **Нет**, и аннулированное платежное поручение удаляется из реестра платежных поручений.

### <a name="reprint-a-payment-order"></a>Повторная печать платежного поручения

Платежное поручение можно напечатать повторно. На странице **Платежи поставщикам** в области действий выберите **Печать \> Печать платежного поручения**. Платежные поручения можно также повторно напечатать со страницы **Банковские проводки**. Выберите ваучер платежного поручения, затем выберите **Печать \> Платежное поручение**, чтобы распечатать документ.

### <a name="view-generated-payment-orders"></a>Просмотр сформированных платежных поручений

Сформированные платежные поручения можно просмотреть на странице **Реестр платежных поручений** (**Расчеты с поставщиками \> Запросы и отчеты \> Платеж \> Реестр платежных поручений**). На вкладке **Реквизиты** просмотрите информацию о плательщике и получателе.

## <a name="generate-a-payment-order-for-a-payment-return-to-a-customer"></a>Создание платежного поручения клиента для возврата платежа клиенту

Можно сформировать платежное поручение для возврата средств клиенту.

1. Выберите **Расчеты с клиентами \> Платежи \> Журнал платежей**.
2. Создайте журнал, а затем в области действий выберите **Строки**, чтобы открыть страницу **Платежи клиентов**.
3. Создайте строку платежа клиенту. Введите информацию так же, как при создании строки платежа поставщику ранее в этой статье.
4. На вкладке **Банк** в поле **Идентификатор счета** введите номер банковского счета, соответствующий счету клиента, который должен получить возврат платежа.
5. В поле **Платежка на** выберите счет клиента, который должен получить возврат платежа.
6. В области действий выберите **Функции \> Создание платежей**, чтобы создать платежное поручение.

Сформированные платежные поручения для клиентов можно просмотреть на странице **Реестр платежных поручений** (**Расчеты с клиентами \> Запросы и отчеты \> Платеж \> Реестр платежных поручений**). 


## <a name="review-registry-of-payment-orders"></a>Просмотр реестра платежных поручений

Отчет реестра платежных поручений содержит список платежных поручений для банковского счета за период. Этот отчет содержит следующие данные для каждого платежного поручения:

- Номер и дата
- Наименование и номер банковского счета контрагента
- Назн. плат.
- Сумма платежа и код валюты
- Статус платежа
- Примечание, указывающее, является ли платеж электронным

Чтобы запустить отчет, выполните следующие шаги.
1. Выберите **Расчеты с поставщиками > Запросы и отчеты > Платеж > Реестр платежных поручений** или **Расчеты с клиентами > Запросы > Платеж > Реестр платежных поручений**.
2. Щелкните **Печать > Реестр платежных поручений**.
3. Выберите **Начальная дата** и **Конечная дата**.
4. Определите следующие фильтры для платежных поручений: **Статус платежного поручения**, **Код валюты**, **Банковский счет** и примечание **Электронный платеж** (Все, Электронный, Печатная форма).
5. Щелкните **ОК**, чтобы создать отчет.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
