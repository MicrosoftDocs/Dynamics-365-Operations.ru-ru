---
title: Настройка канала центра обработки вызовов
description: В этой статье описывается, как создать канал центра обработки вызовов в Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: cc9c43db73092d35aa88b507b0418fcc892d1a76
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282939"
---
# <a name="set-up-a-call-center-channel"></a>Настройка канала центра обработки вызовов


[!include [banner](includes/banner.md)]

В этой статье описывается, как создать канал центра обработки вызовов в Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Обзор


В Dynamics 365 Commerce центр обработки вызовов — это тип канала Commerce, который можно определить в приложении. Определение канала для объектов центра обработки вызовов позволяет системе связывать отдельные данные и обработку заказов по умолчанию с заказами на продажу. Хотя компания может определить несколько каналов обработки вызовов в Commerce, важно отметить, что отдельный пользователь может быть связан только с одним каналом обработки вызовов. 

Перед созданием нового канала центра обработки вызовов убедитесь, что вы соблюдаете [Необходимые условия для настройки каналов](channels-prerequisites.md).

## <a name="create-and-configure-a-new-call-center-channel"></a>Создание и настройка нового канала центра обработки вызовов

Чтобы создать и настроить новый канал центра обработки вызовов, выполните следующие действия.

1. В области переходов откройте раздел **Розничная торговля и коммерция \> Каналы \> Центры обработки вызовов \> Все центры обработки вызовов**.
1. В области действий выберите **Создать**.
1. Вставьте имя для нового канала в поле **Имя**.
1. Выберите подходящее **Юридическое лицо** из раскрывающегося списка.
1. Выберите подходящее местоположение **Склад** из раскрывающегося списка. Это местоположение будет использоваться по умолчанию в заказах на продажу, созданных для данного канала центра обработки вызовов, если на уровне клиента или номенклатуры не определено никаких других значений по умолчанию.
1. В поле **Клиент по умолчанию** укажите допустимый клиент по умолчанию. Эти данные используются для помощи в автоматическом заполнении значений по умолчанию при создании новых записей клиентов. При создании заказов в центре обработки вызовов не рекомендуется создавать заказы для клиента по умолчанию.
1. В поле **Профиль уведомлений по электронной почте** укажите допустимый профиль уведомлений по электронной почте. По мере создания и обработки заказов в центре обработки вызовов профиль уведомлений по электронной почте используется для запуска автоматических оповещений с помощью электронной почты для клиентов с информацией о статусе их заказов.
1. Предоставьте код информации **Переопределение цены**. Возможно, для этого сначала потребуется создать код информации. Этот информационный код предоставляет набор кодов причин, из которых пользователю будет предложено выбрать при использования функции переопределения цены в заказе центра обработки вызовов.
1. Введите код информации **Код удержания**. Возможно, для этого сначала потребуется создать код информации. Этот информационный код предоставляет набор необязательных кодов причин, из которых пользователю будет предложено выбрать при переводе заказа в состояние ожидания.
1. Введите код информации **Кредит**. Возможно, для этого сначала потребуется создать код информации. Этот информационный код предоставляет набор кодов причин, из которых пользователь может выбирать при использовании функции кредита по заказу центра обработки вызовов, и предоставляет клиентам различные способы возврата для причин обслуживания клиентов.
1. Необязательно: настройте финансовые аналитики на экспресс-вкладке **Финансовые аналитики**. Введенные здесь аналитики будут использоваться по умолчанию для любого заказа на продажу, созданного в этом канале центра обработки вызовов.
1. Нажмите кнопку **Сохранить**.

На следующем рисунке показано создание нового канала центра обработки вызовов.

![Новый канал центра обработки вызовов.](media/channel-setup-callcenter-1.png)

На следующем рисунке показан пример канала центра обработки вызовов.

![Пример канала центра обработки вызовов.](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Дополнительная настройка канала

Дополнительные задачи, необходимые для настройки канала центра обработки вызовов, включают настройку способов оплаты и способов поставки.

На следующем рисунке показаны варианты настройки **Режимы поставки** и **Способы оплаты** на вкладке **Настройка**.

![Дополнительные действия по настройке канала центра обработки вызовов.](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Настройка способов оплаты

Для настройки способов оплаты выполните следующие действия для каждого типа платежа, поддерживаемого в этом канале. Пользователям потребуется выбрать из заранее определенных способов оплаты, чтобы связать их с каналом центра обработки вызовов. Перед настройкой методов платежа для центра обработки вызовов сначала настройте основные методы оплаты в пункте **Retail и Commerce \> Настройка канала \> Способы оплаты \> Способы оплаты**.

1. На панели операций выберите вкладку **Настройка**, а затем выберите **Способы оплаты**.
1. В области действий выберите **Создать**.
1. В области переходов выберите метод оплаты из доступных предварительно определенных платежей.
1. Настройте дополнительные параметры, необходимые для типа оплаты. Для кредитных карт, подарочных сертификатов или карточек постоянного клиента дополнительная настройка необходима путем выбора функции **Настройка карты**. 
1. Настройте соответствующие счета разноски для типа платежа в разделе **Разноска**.
1. В области операций щелкните **Сохранить**.

На следующем рисунке показан пример способы наличной оплаты.

![Пример способов оплаты.](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a>Настройка способов поставки

Настроенные способы поставки можно просмотреть, выбрав **Способы поставки** на вкладке **Настройка** на **панели операций**.  

Чтобы изменить или добавить режим доставки, который должен быть связан с каналом центра обработки вызовов, выполните следующие действия.

1. В форме режимов поставки центра обработки вызовов выберите **Управление режимами доставки**
1. В области действий выберите **Создать**, чтобы создать новый способ поставки, или выберите существующий режим.
1. В разделе **Каналы розничной торговли** щелкните **Добавить строку**, чтобы добавить канал центра обработки вызовов. Добавление каналов с помощью узлов организации вместо добавления каждого канала по отдельности может ускорить добавление каналов.
1. Убедитесь, что режим доставки был настроен с данными на экспресс-вкладке **Продукты** и на экспресс-вкладке **Адреса**. Если для данного способа поставки нет допустимых продуктов или адресов поставки, выбор этого параметра в процессе ввода заказов приведет к ошибкам.
1. После внесения каких-либо изменений в конфигурации доставки режима центра обработки вызовов необходимо выполнить задание **Обработка режимов доставки**, чтобы развернуть матрицу изменений. Это задание можно найти , перейдя к пункту **Retail и Commerce \> ИТ Retail и Commerce \> Обработка режимов доставки**.

На следующем рисунке показан пример режима поставки.

![Настройка способов поставки.](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a>Настройка пользователей канала

Чтобы создать заказ на продажу, связанный с каналом центра обработки вызовов из Commerce Headquarters, пользователь, создающий заказ на продажу, должен быть связан с каналом центра обработки вызовов. Пользователь не может вручную связать заказ на продажу, созданный в модуле Commerce Headquarters, с каналом центра обработки вызовов. Связь является систематической и основана на пользователе и взаимосвязи пользователя с каналом центра обработки вызовов. Пользователь может быть связан только с одним каналом центра обработки вызовов.

1. На панели операций выберите вкладку **Канал**, затем выберите **Пользователи канала**.
1. В области действий выберите **Создать**.
1. Выберите существующий **Идентификатор пользователя** из раскрывающегося списка выбора, чтобы связать этого пользователя с каналом центра обработки вызовов

Когда после выполнения настройки пользователей канала пользователь создает новый заказ на продажу, связанный в Commerce Headquarters, заказ на продажу будет связан со связанным с ним каналом центра обработки вызовов. Любые конфигурации для этого канала будут систематически применены к заказу на продажу. Пользователь может проверить, с каким каналом центра обработки вызовов связан заказ на продажу, просмотрев ссылку на имя канала в заголовке заказа на продажу.


### <a name="set-up-price-groups"></a>Настройка ценовых групп

Ценовые группы необязательны, но если они используются, могут управлять тем, какие цены продажи будут предложены клиентам, которые размещают заказы в канале центра обработки вызовов. Если ценовая группа не была настроена для клиента или если группы цен по каталогу не применяются к заказу на продажу (используя поле **Идентификатор исходного кода** в заголовке заказа центра обработки вызовов), то для поиска цен номенклатур используется ценовая группа канала. Если ценовая группа не найдена в канале центра обработки вызовов, используются основные цены номенклатур по умолчанию. 

Чтобы настроить ценовую группу, выполните следующие действия.

1. На панели операций щелкните вкладку **Канал**, затем выберите **Ценовые группы**.
1. В области операций щелкните **Создать**.
1. Выберите **Розничная ценовая группа** в раскрывающемся списке выбора.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Необходимые условия для настройки каналов](channels-prerequisites.md)

[Функциональность продажи центра обработки вызовов](call-center-functionality.md)

[Настройка параметров обработки заказов центра обработки вызовов](set-up-order-processing-options.md)

[Каталоги центра обработки вызовов](call-center-catalogs.md)

[Настройка оповещений о мошенничестве и работа с ними](set-up-fraud-alerts.md)

[Настройка программ непрерывности для центров обработки вызовов](set-up-continuity-program.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
