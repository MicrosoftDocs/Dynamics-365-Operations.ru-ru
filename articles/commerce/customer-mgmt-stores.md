---
title: Управление клиентами в магазинах
description: В этом разделе описывается, как предприятия розничной торговли могут активировать возможности управления клиентом на POS-терминале в Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: dd17593d84a8bf262712a84b11829f8ec6c49049
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097216"
---
# <a name="customer-management-in-stores"></a>Управление клиентами в магазинах

[!include [banner](includes/banner.md)]

В этом разделе описывается, как предприятия розничной торговли могут активировать возможности управления клиентом на POS-терминале в Microsoft Dynamics 365 Commerce.

Важно, чтобы сотрудники магазина могли создавать и изменять записи клиентов в POS. Таким образом, они могут регистрировать обновления информации о клиенте, такие как адрес электронной почты, номер телефона и адрес. Эта информация полезна в таких нисходящих системах, как маркетинг, потому что эффективность этих систем зависит от точности данных их клиентов.

С помощью продавцов-консультантов процесс создания клиентов может быть инициирован из двух точек входа POS. Они могут выбрать кнопку, которая сопоставлена с операцией **Добавить клиента**, или же они могут выбрать **создать клиента** на панели приложений на странице результатов поиска. В обоих случаях появляется диалоговое окно **создать клиента**, в котором продавцы-консультанты могут ввести необходимые сведения о клиенте, такие как имя клиента, адрес электронной почты, номер телефона, адрес и любые дополнительные сведения, относящиеся к данному бизнесу. Для записи дополнительной информации можно использовать атрибуты клиента, связанные с данным клиентом. Дополнительные сведения об атрибутах клиентов см. в разделе [атрибуты клиентов](dev-itpro/customer-attributes.md).

Продавцы могут также регистрировать дополнительные адреса электронной почты и телефонные номера. Кроме того, они могут регистрировать параметры клиента по получению маркетинговой информации с помощью дополнительных адресов электронной почты или телефонных номеров. Чтобы эта функция была доступна, необходимо включить функцию **Сбор нескольких адресов электронной почты и телефонных номеров и согласие на маркетинг для этих контактов** в рабочей области **Управление функциями** в Commerce headquarters (**Системное администрирование \> Рабочие области \> Управление функциями**).

## <a name="default-customer-properties"></a>Свойства клиента по умолчанию

Предприятия розничной торговли могут использовать страницу **Все магазины** в Commerce headquarters (**Retail и Commerce \> Каналы \> Магазины**), чтобы связать клиента по умолчанию с каждым магазином. Затем Commerce копирует свойства, которые определены для клиента по умолчанию, во все создаваемые записи о клиентах. Например, в диалоговом окне **Создание клиента** отображаются свойства, которые наследуются от клиента по умолчанию, связанного с магазином. Эти свойства включают **тип клиента**, **группу клиентов**, **параметр получения чеков**, **электронную почту для чеков**, **валюту** и **язык**. Любые **назначения** (группировка клиентов) также наследуются из клиента по умолчанию. Однако **финансовые аналитики** наследуются из группы клиентов, связанной с клиентом по умолчанию, а не с самого клиента по умолчанию.

> [!NOTE]
> Значение **электронная почта для чеков** копируется из клиента по умолчанию только в том случае, если для вновь созданных клиентов не указан код электронной почты для чеков. Это означает, что если код электронной почты для чеков присутствует в клиенте по умолчанию, то все клиенты, созданные на веб-сайте электронной коммерции, получат такой же код электронной почты для чеков, так как нет пользовательского интерфейса для захват кода электронной почты для чеков из клиента. Рекомендуется оставлять поле **электронная почта для чеков** пустым для клиента по умолчанию в магазине и использовать его только в том случае, если имеется бизнес-процесс, который зависит от адреса электронной почты для чеков. 

Продавцы-консультанты могут регистрировать несколько адресов для клиента. Имя и номер телефона клиента наследуются из контактной информации, связанной с каждым адресом. Экспресс-вкладка **адреса** записи клиента включает поле **цели**, которое могут изменять продавцы-консультанты. Если типом клиента является **Человек**, значением по умолчанию является **Домашний**. Если типом клиента является **Организация**, значением по умолчанию является **Бизнес**. Другие значения, которые поддерживает данное поле, включают **домашний**, **офис** и **почтовый ящик**. Значение поля **страна** для адреса наследуется из основного адреса, который указан на странице **операционная единица** в Commerce headquarters в **Администрирование организации \> Организации \> Операционные единицы**.

## <a name="sync-customers-and-async-customers"></a>Синхронные клиенты и асинхронные клиенты

в Commerce имеется два режима создания клиентов: синхронные и асинхронные. По умолчанию клиенты создаются синхронно. Другими словами, они создаются в Commerce headquarters в реальном времени. Режим создания синхронных клиентов является полезным, поскольку новые клиенты сразу же могут осуществлять поиск по каналам. Однако у него также есть недостаток. Поскольку он генерирует вызовы [Commerce Data Exchange: служба реального времени](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) в Commerce headquarters, производительность может быть нарушена, если будет выполнено много звонков для создания клиентов одновременно.

Если в параметре **Создание клиента в асинхронном режиме** установлено значение **Да** в профиле функциональности магазина (**Retail и Commerce \> Настройка канала \> Настройка интернет-магазина \> Профили функциональности**), вызовы службы реального времени не используются для создания записей клиентов в базе данных канала. Режим асинхронного создания клиентов не влияет на производительность Commerce Headquarters. Временный глобальный уникальный идентификатор (GUID) назначается каждой новой записи асинхронного клиента и используется в качестве идентификатора счета клиента. Этот GUID не отображается для пользователей POS. Вместо этого эти пользователи будут видеть **ожидающие синхронизации** в качестве кода счета клиента. Хотя эта конфигурация вынуждает создавать клиентов асинхронно, обратите внимание, что изменения записей клиентов выполняются синхронно.

### <a name="convert-async-customers-to-sync-customers"></a>Преобразование асинхронных клиентов в синхронных

Чтобы преобразовать асинхронных клиентов в синхронных, необходимо сначала выполнить P-задание, чтобы отправлять асинхронные клиенты в Commerce Headquarters. Затем запустите задание **синхронизация клиентов и деловых партнеров из асинхронного режима**, чтобы создать коды счетов клиентов. Наконец, выполните задание **1010**, чтобы синхронизировать коды счета нового клиента с каналами.

### <a name="async-customer-limitations"></a>Ограничения асинхронных клиентов

Функциональность асинхронных клиентов в настоящее время имеет следующие ограничения:

- Записи асинхронных клиентов нельзя изменить, пока клиент не будет создан в Commerce headquarters, а новый код счета клиента был синхронизирован с каналом обратно.
- Назначения не могут быть связаны с асинхронными клиентами. Таким образом, новые асинхронные клиенты не наследуют назначения от клиента по умолчанию.
- Карты лояльности не могут быть выпущены для асинхронных клиентов, если только новый код счета клиента не был синхронизирован с каналом обратно.
- Дополнительные адреса электронной почты и номера телефонов не могут регистрироваться для асинхронных клиентов.

### <a name="customer-creation-in-pos-offline-mode"></a>Создание клиента в автономном режиме POS

Если POS переходит в автономный режим, и включен режим создания асинхронного клиента, новые записи клиентов создаются асинхронно. Если POS переходит в автономный режим, и отключен режим создания асинхронного клиента, система автоматически переключается на режим создания асинхронного клиента. Другими словами, записи клиентов могут создаваться асинхронно, даже если режим создания асинхронных клиентов отключен. Поэтому администраторы Commerce headquarters должны создать и запланировать повторяющееся пакетное задание для P-задания, задание **Синхронизация клиентов и деловых партнеров из асинхронного режима** и задание **1010**, чтобы преобразовать всех асинхронных клиентов в синхронных клиентов в Commerce Headquarters.

> [!NOTE]
> Если параметр **Фильтрация общих таблиц данных о клиентах** имеет значение **Да** на странице **схема канала Commerce** (**Retail и Commerce \> Настройка Headquarters \> планировщик Commerce \> Группа базы данных канала**), записи клиентов не создаются в автономном режиме POS. Дополнительные сведения см. в разделе [Исключение автономных данных](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Атрибуты заказчика](dev-itpro/customer-attributes.md)

[Исключение автономных данных](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
