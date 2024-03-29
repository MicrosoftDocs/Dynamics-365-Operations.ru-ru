---
title: Настройка метода платежа для счета клиента для сайтов электронной коммерции B2B
description: В этой статье описывается, как настроить метод платежа для счета клиента в Microsoft Dynamics 365 Commerce. Также описывается, как кредитные лимиты влияют на запись платежей в кредит на сайтах электронной коммерции бизнес-бизнес (B2B).
author: josaw1
ms.date: 04/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: RetailOperations
ms.openlocfilehash: b8424920c3a177e01b71fc1c288b7acdd97ef191
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272026"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Настройка метода платежа для счета клиента для сайтов электронной коммерции B2B

[!include [banner](../../includes/banner.md)]

В этой статье описывается, как настроить метод платежа для счета клиента в Microsoft Dynamics 365 Commerce. Также описывается, как кредитные лимиты влияют на запись платежей в кредит на сайтах электронной коммерции бизнес-бизнес (B2B).

Продавцы могут принимать различные типы платежей в обмен на продукты и услуги, которые они продают по каналу электронной коммерции. Каждый тип платежа, принимаемый розничным магазином, нужно настроить в Dynamics 365 Commerce в процессе настройки системы. Метод платежа для счета клиента (или "в кредит") должен поддерживаться на сайтах электронной коммерции B2B. 

## <a name="prerequisites"></a>Необходимые условия

1. Добавьте метод платежа для счета клиента в Commerce Headquarters.
2. Свяжите метод оплаты для счета клиента с каналом электронной коммерции.
3. Убедитесь, что свойство **Разрешить в кредит** включено для клиентов в разделе **Retail и Commerce \> Клиенты \> Все клиенты \> Значения платежа по умолчанию** в Commerce Headquarters.

    > [!NOTE]
    > Если для всех клиентов разрешено использование метода платежа в кредит, можно установить для свойства **Разрешить в кредит** значение **Да** для клиента по умолчанию в канале, который связан с сайтом B2B. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Включение метода платежа для счета клиента в конструкторе сайта Commerce 

Чтобы включить метод платежа для счета клиента в конструкторе сайта Commerce, выполните следующие действия.

1. Перейдите к разделу **Параметры сайта \> Расширения**.
1. Установите для свойства **Включить платежи со счета клиента** значение **Включено для клиентов B2B**. 
1. Выберите **Сохранить и опубликовать**.

> [!NOTE]
> Новые параметры сайта вступят в силу только после обновления файла app.settings.json. Дополнительные сведения см. в разделе [Обновления пакета SDK и библиотеки модулей](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>Включение метода платежа для счета клиента на странице оформления заказа для сайта электронной коммерции B2B

Чтобы включить метод платежа для счета клиента на странице оформления заказа для сайта электронной коммерции B2B, выполните следующие действия.

1. В конструкторе сайтов Commerce найдите и измените страницу или фрагмент оформления заказа, содержащий модуль оформления заказа для сайта электронной коммерции B2B.
1. В области **Контейнер раздела оформления заказа** выберите **Добавить модуль**, затем добавьте модуль **Платеж со счета клиента**.
1. Расположите модуль **Платеж со счета клиента**, выбрав многоточие (**...**), затем выберите **Вверх** или **Вниз** по мере необходимости.
1. Выберите **Сохранить**, выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Проверка того, что метод платежа со счета клиента был включен и опубликован

Чтобы проверить, что метод платежа со счета клиента был включен и опубликован, выполните следующие действия.

1. Войдите на сайт электронной коммерции.
1. Добавьте продукты в корзину.
1. Перейдите на страницу оформления заказа. Должен отобразиться новый метод платежа **Счет клиента**.

## <a name="work-with-credit-limits"></a>Работа с кредитными лимитами

Когда возможности для платежей по счетам клиентов включены на сайте B2B, в организациях обычно требуется отобразить сведения о кредитных лимитах и сальдо кредитного лимита в процессе записи заказов. Кредитный лимит для клиента определяется свойством **Кредитный лимит** на экспресс-вкладке **Кредит и сборы** записи клиента в Commerce Headquarters. Однако в случае B2B-сценариев за заказ, который размещает клиент, часто должна быть выставлена накладная на счет организации, к которой принадлежит клиент. Таким образом, необходимо установить для свойства **Счет для накладной** на экспресс-вкладке **Накладная и поставка** записи клиенте значение кода счета клиента организации. Затем, когда клиент размещает заказ на сайте B2B, накладная по заказу выставляется организации. Сайт B2B будет также использовать кредитный лимит организации вместо кредитного лимита, определенного в записи клиента.

Расчет и сальдо кредитного лимита, которые показаны на сайте B2B, зависят от настройки свойства **Тип кредитного лимита** в Commerce Headquarters. Местоположение этого свойства изменяется в зависимости от того, активирована ли функция **Управление кредитом** в рабочей области **Управление функциями**:

- Если функция **Управление кредитом** включена, свойство находится на экспресс-вкладке **Кредитные лимиты** в пункте **Кредит и сбор задолженностей \> Настройка \> Параметры кредита и сбора задолженности \> Кредит**. 
- Если функция **Управление кредитом** отключена, свойство находится в разделе **Кредитоспособность** в пункте **Расчеты с клиентами \> Настройка \> Параметры модуля расчетов с клиентами \> Кредитоспособность**.

Свойство **Тип кредитного лимита** поддерживает значения **Нет**, **Сальдо**, **Сальдо + отборочная накладная или поступление продуктов**, а также **Сальдо + все**. Дополнительные сведения об этих значениях см. в разделе [Значения типа кредитного лимита](/dynamics365/supply-chain/sales-marketing/credit-limits-customers).

> [!NOTE]
> Рекомендуется настроить для свойства **Тип кредитного лимита** значение **Сальдо + отборочная накладная или лист продукции**, чтобы открытые заказы на продажу не участвовали в расчете сальдо. Затем, если клиенты размещают будущие заказы, им не придется беспокоиться о том, что эти заказы будут влиять на текущее сальдо.

Другое свойство, которое влияет на заказ в кредит, — это свойство **Обязательный кредитный лимит**, расположенное на экспресс-вкладке **Кредит и сборы** в записи клиента. Установив для этого свойства значение **Да** для определенных клиентов, можно заставить систему проверять их кредитный лимит, даже если свойство **Тип кредитного лимита** имеет значение **Нет**, чтобы указать, что кредитный лимит не должен проверяться ни для какого клиента.

В настоящее время клиент, использующий метод платежа в кредит, не может заплатить больше чем остаток кредита для заказа. Например, если оставшееся кредитное сальдо клиента равно $1 000, но сумма заказа равна $1 200, клиент может заплатить только $1 000 с помощью метода "в кредит". Для выплаты сальдо клиент должен использовать другой способ оплаты. В будущих выпусках конфигурация Commerce позволит пользователям тратить больше своих кредитных лимитов при размещении заказов.

В модуле **Кредит и сборы** имеются новые возможности управления кредитами. Чтобы включить эти возможности, включите функцию **Управление кредитом** в рабочей области **Управление функциями**. Одна из новых возможностей включает блокировку заказов на продажу на основе правил блокировки. Персонаж "менеджер по кредитам" может затем выпустить или отклонить эти заказы после дальнейшего анализа. Однако возможность блокировки заказов на продажу не применима к заказам Commerce, так как часто заказы на продажу имеют предоплату и функция **Управление кредитами** не полностью поддерживает сценарии предоплаты. 

Вне зависимости от того, активирована ли функция **Управление кредитом**, если сальдо клиента превышает кредитный лимит во время выполнения заказа, заказы на продажу не блокируются. Вместо этого в Commerce создается предупреждение или сообщение об ошибке, в зависимости от значения поля **Сообщение при превышении кредитного лимита** на экспресс-вкладке **Кредитные лимиты**.

Свойство **Исключение из управления кредитом**, которое предотвращает блокировку заказов на продажу в Commerce, находится в заголовке заказа на продажу (**Розничная торговля и коммерция \> Клиенты \> Все заказы на продажу**). Если это свойство имеет значение **Да** (по умолчанию) для заказов на продажу в Commerce, заказы будут исключены из рабочего процесса блокировки в управлении кредитами. Несмотря на то, что свойство имеет имя **Исключить из управления кредитом**, указанный кредитный лимит по-прежнему будет использоваться во время выполнения заказа. Заказы просто не блокируются.

Возможность блокировки заказов на продажу в Commerce на основе правил блокировки планируется для будущих выпусков Commerce. Пока она не поддерживается, если вы хотите, чтобы заказы на продажу в Commerce принудительно проходили через новые потоки управления кредитом, можно настроить следующие файлы XML в решении Visual Studio. В файлах измените логику таким образом, чтобы флаг **CredManExcludeSalesOrder** был установлен в значение **Нет**. Таким образом, по умолчанию для заказов на продажу в Commerce в свойстве **Исключить из управления кредитом** будет по умолчанию установлено значение **Нет**.

- RetailCreateCustomerOrderExtensions_CredMan_Extension.xml
- RetailCallCenterOrderExtensions_CredMan_Extension.xml

Если флаг **CredManExcludeSalesOrder** имеет значение **Нет** и клиент B2B может купить из магазинов с помощью приложения POS, разноска кассовых проводок может быть нарушена. Например, имеется правило блокировки для типа оплаты наличными, а клиент B2B приобрел некоторые номенклатуры в магазине, используя наличные средства. В этом случае на итоговый заказ на продажу не будет успешно выставлена накладная, поскольку заказ будет заблокирован. Таким образом, разноска будет неудачной. По этой причине рекомендуется выполнять сквозное тестирование после реализации этой настройки.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка сайта электронной коммерции B2B](set-up-b2b-site.md)

[Управление деловыми партнерами B2B с помощью иерархий клиентов](partners-customer-hierarchies.md)

[Управление пользователями деловых партнеров на сайтах электронной коммерции B2B](manage-b2b-users.md)

[Настройка лимитов количества продуктов для сайтов электронной коммерции B2B](quantity-limits.md)

[Обновления SDK и библиотеки модулей](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
