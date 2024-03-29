---
title: Настройка каналов центра обработки вызовов
description: В этой статье приводятся сведения об обработке заказов для центров обработки вызовов с помощью Dynamics 365 Commerce.
author: josaw1
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCROrderParameters, MCRSalesTableOrderHistory, SalesOrderProcessingWorkspace
audience: Application User
ms.reviewer: josaw
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c6d21385d956534c799af5b9e20a54c9970da368
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854879"
---
# <a name="set-up-call-center-channels"></a>Настройка каналов центра обработки вызовов

[!include [banner](includes/banner.md)]

Компания может определить несколько каналов центра обработки вызовов в Dynamics 365 Commerce. Каналы центра обработки вызовов настраиваются в пункте **Retail и Commerce** \> **Каналы** \> **Центры обработки вызовов** \> **Все центры обработки вызовов**, и они являются специфическими для юридического лица.

При создании нового канала центра обработки вызовов ему систематически назначается код операционной единицы. Так как центры обработки вызовов создаются как операционные единицы, пользователи могут связать канал центра обработки вызовов с различными функциями Commerce, такими как ассортимент, каталоги и определенные режимы доставки.

Каналу центра обработки вызовов может быть настроен склад по умолчанию. Затем при создании заказов на продажу в данном канале склад по умолчанию вводится автоматически в заголовке заказа на продажу, если не был определен другой склад для клиента, выбранного для заказа на продажу. В этом случае по умолчанию вводится склад этого клиента.

Пользователи должны быть привязаны к каналу центра обработки вызовов, чтобы использовать возможности центра обработки вызовов. Любой заказ на продажу, который пользователь создает, автоматически связывается с каналом центра обработки вызов этого пользователя. В настоящее время один пользователь не может быть связан с нескольким каналам центра обработки вызовов одновременно.

Профиль уведомлений по электронной почте можно также настроить для канала центра обработки вызовов. Профиль определяет набор шаблонов электронной почты, используемый при отправке сообщений электронной почты клиентам, которые размещают заказы через этот канала центра обработки вызовов. Триггеры электронной почты можно настроить на системные события, такие как размещение заказа или отгрузка заказа.

Прежде чем можно будет правильно обрабатывать продажи через канал центра обработки вызовов, правильные [способы оплаты](/dynamics365/unified-operations/retail/work-with-payments) и режимы доставки должны быть определены для канала.

На уровне канала центра обработки вызовов можно определить другие значения по умолчанию, которые относятся к финансовым аналитикам, которые будут связаны с заказами, созданными по этому каналу.

## <a name="options-for-order-processing-behavior"></a>Параметры для поведения обработки заказов

Три параметра в конфигурации центра обработки вызовов оказывают значительное влияние на функциональные возможности и функции, которые доступны для заказов на продажу, которые были созданы через этот центр обработки вызовов: **Включить заполнение заказа**, **Включить прямые продажи** и **Включить управление ценами заказов**.

### <a name="enable-order-completion"></a>Включить заполнение заказа

Параметр **Включить заполнение заказа** в канале центра обработки вызовов оказывает значительное влияние на поток обработки заказов для заказов на продажу, введенных для этого канала. Когда этот параметр включен, все заказы на продажу должны проходить через набор правил проверки, прежде чем они могут быть подтверждены. Вы запускаете эти правила, выбрав кнопку **Выполнить**, которая добавляется на панель действий страницы заказа на продажу. Все заказы на продажу, которые были созданы с включенным параметром **Включить заполнение заказа**, должны пройти через процесс завершения заказа. Этот процесс обеспечивает принудительное выполнение записи платежа и логики проверки платежа. Помимо принудительного выполнения платежа, процесс размещения заказа может запускать [проверки на мошенничество](/dynamics365/unified-operations/retail/set-up-fraud-alerts), которые настроены в системе. Заказы, не прошедшие проверки платежа или мошенничества, приостанавливаются и не могут быть выпущены для дальнейшей обработки (например, комплектации или отгрузки) до устранения ошибки, которая вызвала приостановку.

Когда включен параметр **Включить заполнение заказа** для канала центра обработки вызовов, если номенклатуры строки вводятся в заказ на продажу и пользователь канала пытается закрыть или форму заказа на продажу или уйти с нее, не выбрав предварительно **Выполнить**, система обеспечивает принудительное выполнение процесса выполнения заказа, открыв страницу сводных сведений о заказе на продажу и потребовав, чтобы пользователь правильно разместил заказ. Если заказ невозможно правильно разместить вместе с платежом, пользователь может использовать функцию [приостановки заказа](/dynamics365/unified-operations/retail/work-with-order-holds) для приостановки заказа. Если пользователь пытается отменить заказ, он должен правильно отменить его, используя функцию "Отменить" или функцию "Удалить", в зависимости от функции, которая разрешена настройками безопасности пользователя.

Если параметр **Включить заполнение заказа** включена для канала центра обработки вызовов, поле **Статус оплаты** будет отслеживаться в заказе. Система вычисляет **Статус оплаты** при размещении заказа на продажу. Только заказы с утвержденным статусом оплаты разрешены для перемещения по системе для дополнительных действий по обработке, таких как комплектация и отгрузка. Если платежи отклонены, включается флаг **не обрабатывать** на подробном состоянии заказа, что блокирует заказ до устранения проблемы с платежом.

Кроме того, если параметр **Включить заполнение заказа** включен, когда пользователи создают заказы на продажу и находятся в режиме ввода номенклатуры строки, поле **Источник** будет доступно в основном заголовке заказа на продажу. Поле **Источник** используется для записи [кода источника каталога](/dynamics365/unified-operations/retail/call-center-catalogs) в сценарии продажи по прямому маркетингу. Этот код может затем использоваться для специальных цен и рекламных акций.

Даже если параметр **Включить заполнение заказа** отключен, пользователи по-прежнему могут применить код источника к заказу на продажу. Однако им необходимо сначала открыть сведения заголовка заказа на продажу, чтобы получить доступ к полю **Источник**. Другими словами, потребуется несколько дополнительных щелчков. Это поведение применяется к таким функциям, как выполнение отгрузки и ускоренные заказы. Эти возможности доступны для всех заказов, которые были созданы в центре обработки вызовов. Однако когда параметр **Включить заполнение заказа** включен, пользователи могут видеть конфигурацию этих функций в заголовке заказа на продажу, когда они находятся в представлении записи строки. Им не требуется переходить в сведения заголовка заказа на продажу для поиска соответствующих параметров и полей.

> [!NOTE]
> Когда активирована функция **Платежи по заказам Commerce многоканального взаимодействия** кнопка **Включить заполнение заказа** центра обработки звонков будет скрыта в центральном офисе на экспресс-вкладке **Общее** вашего канала в **Розничная торговля и коммерция \> Каналы \> Центры обработки звонков**.

### <a name="enable-direct-selling"></a>Включить прямые продажи

Если параметр **Включить прямые продажи** включен для канала центра обработки вызовов, пользователи могут воспользоваться преимуществами функций продажи более дорогого продукта и перекрестных продаж в Commerce. В этом случае всплывающие окна появляются во время ввода заказа и предлагают другие продукты, которые пользователь центра обработки вызовов может предложить клиенту. Предлагаемые продукты основаны на продукты, который был только что заказан в строке заказа на продажу. В настоящее время предложения по продаже более дорогого продукта или перекрестным продажам настраиваются на уровне номенклатуры для продуктов или каталогов. Если параметр **Включить прямые продажи** отключен для канала центра обработки вызовов, всплывающие окна не появляются во время ввода заказа, даже если допустимые варианты более дорогого продукта или перекрестные продажи были определены для заказанной номенклатуры.

Когда параметр **Включить прямые продажи** включен, также включены функции сценариев и изображений страницы ввода заказа на продажу. В этом случае панель сведений доступна в правой части страницы во время ввода заказа. Эта панель может показывать сценарии, которые относятся к общему процессу ввод заказа, код исходного каталога, который был применен, или сценарии, которые относятся к номенклатурам, которые заказываются. Кроме того, на панели изображений может отображаться изображение продукта для заказываемых номенклатур, если изображение было определено для номенклатуры в настройках продукта.

### <a name="enable-order-price-control"></a>Включить управление ценами заказов

Когда включен параметр **Включить управление ценами заказов**, только уполномоченные пользователи могут изменить цену продажи номенклатуры во время ввода заказа. Изменения должны быть в заданных пределах. Пользователи, у которых нет соответствующих прав, должны вместо этого отправить запрос на изменение цены. Запрос будет обработан через системный workflow-процесс для проверки и утверждения.

## <a name="channel-users"></a>Пользователи канала

При определении канала центра обработки вызовов необходимо связать пользователей канала с центром обработки вызовов. В противном случае центр обработки вызовов не будет использоваться в системе. Когда пользователи входят в Commerce и вводят заказы на продажу или заказы на возврат на странице, которая относится к вводу заказа, их идентификатор пользователя проверяется по конфигурации канала центра обработки вызовов. Если пользователь связан с определенным каналом центра обработки вызовов, заказы, которые пользователь создает, наследуют характеристики и значения по умолчанию этого канала.

По умолчанию флаг **Продажа** в заголовке заказа на продажу включен для всех заказов, создаваемых пользователями этого центра обработки вызовов. Заказы могут затем воспользоваться преимуществами предусмотренных в системе функций ценообразования и рекламных акций, специфических для коммерции.


Пользователей, которые не связаны с каналом центра обработки вызовов, используют стандартные функции ввода заказа Microsoft Dynamics 365 Finance. Заказы, которые эти пользователи вводят через форму ввода заказа на продажу, не определяются системой как заказы Commerce. Кроме того, на эти заказы, введенные такими пользователями, не будут распространяться никакие правила обработки для завершения заказа, логика ценообразования или другие проверки заказа, которые могут быть определены в конфигурации канала центра обработки вызовов или в системных параметрах центра обработки вызовов.

После того как вы завершили настройку канала центра обработки вызова и определили пользователей, чтобы помочь обеспечить требуемое поведение системы, убедитесь, что все необходимые параметры центра обработки вызовов определены в **Retail и Commerce** \> **Настройка канала** \> **Настройка центра обработки вызовов** \> **Параметры центра обработки вызовов**. Убедитесь, что также определены связанные номерные серии.

> [!NOTE]
> Для использования функциональности центра обработки вызовов необходимо включить ключ конфигурации для **Несколько получателей**. Этот ключ конфигурации можно найти в ключах **Конфигурация торговли** в **Администрирование системы**\> **Настройка** \> **Конфигурация лицензии**. Это необходимо из-за функций центра обработки вызовов, которые выполняют различные проверки на основе адреса поставки, настроенного на уровне строки заказа на продажу. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
