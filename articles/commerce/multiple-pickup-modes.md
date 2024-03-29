---
title: Включение нескольких режимов доставки самовывозом для заказов клиентов
description: В этой статье описываются функции в Microsoft Dynamics 365 Commerce, позволяющие создавать заказы клиентов для получения в магазине.
author: hhainesms
ms.date: 12/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: e4d8883b3dc1c4a0e12bcb00b6441f76d73da92e
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831593"
---
# <a name="enable-multiple-pickup-delivery-modes-for-customer-orders"></a>Включение нескольких режимов доставки самовывозом для заказов клиентов

[!include [banner](includes/banner.md)]


В Microsoft Dynamics 365 Commerce организации могут определить несколько способов доставки, которые покупатели или продавцы могут выбирать при создании заказа, которые покупатель сам получит в магазине. Таким образом, организации могут предоставлять своим покупателям несколько вариантов получения. Например, многие розничные продавцы теперь предлагают покупателям на выбор получение в магазине или получение в окне выдачи из автомобиля для своих заказов. Commerce поддерживает настройку этих разных режимов получения самовывозом. Пользователи могут воспользоваться преимуществами этих функций, создавая заказы клиентов в любом поддерживаемом канале Commerce (электронная коммерция, центр обработки вызовов или магазин).

## <a name="enable-and-configure-pickup-delivery-modes"></a>Включение и настройка режимов доставки самовывозом

Функция **Поддержка нескольких режимов доставки для самовывоза** в рабочей области **Управления функциями** в Commerce Headquarters стала обязательной и должна быть включена в среде.

Если ранее был определен режим доставки самовывозом на странице **Параметры Commerce**, этот режим появится в текущей конфигурации для режимов доставки самовывозом.

![Режимы доставки самовывозом на странице параметров Commerce.](media/multiplepickupparameter.png)

Можно определить несколько режимов поставки самовывозом в сетке **Способ доставки для самовывоза** в пункте **Параметры Commerce** > вкладка **Заказы клиентов** > экспресс-вкладка **Способы поставки**.  

Поля **Способ поставки "На вынос"** и **Электронный способ поставки**, а также параметр **Показывать только варианты режима перевозчика для заказов на доставку** были перемещены на эту экспресс-вкладку.

Прежде чем настраивать дополнительные режимы доставки для самовывоза, необходимо определить режимы доставки. На странице **Способы поставки** в Commerce Headquarters добавьте режимы доставки, которые должны рассматриваться как режимы доставки для самовывоза. Убедитесь, что все настройки завершены. Например, если вы предлагаете самовывоз из окна выдачи в качестве варианта доставки для интернет-покупателей в определенных магазинах, вам необходимо создать новый режим доставки для этой цели. Можно создать этот режим доставки, используя в качестве описания "самовывоз из окна выдачи". Затем необходимо убедиться, что режим доставки "самовывоз из окна выдачи" сопоставлен со всеми каналами Commerce, которые могут его предоставить, включая интернет-магазины, которые могут предложить этот вариант, и каналы отдельных магазинов, которые будут предлагать этот метод выполнения. Способы доставки также должны быть привязаны к продуктам. В этом примере, если имеются определенные продукты, для которых невозможна доставка "самовывоз из окна выдачи", необходимо обеспечить, чтобы эти номенклатуры были исключены. После завершения добавления любых новых режимов доставки выполните задание **Обработка способов поставки** для создания отношений между режимом поставки, каналами и номенклатурами. После завершения задания откройте страницу **График распределения** в Commerce Headquarters и запустите задание распределения **1120**, чтобы убедиться, что соответствующие базы данных каналов Commerce обновлены с учетом новой конфигурации способов поставки.

![Пример настройки способа поставки для самовывоза из окна выдачи.](media/pickupmodes.png)

После определения дополнительных режимов доставки добавьте их в сетку **Способы поставки самовывозом** на странице **Параметры Commerce**. Затем запустите соответствующие задания распределения, чтобы обновить соответствующие базы данных каналов Commerce изменениями конфигурации.

> [!NOTE]
> Кроме существующего режима доставки самовывозом, который копируется в сетку **Способ поставки "самовывоз"** при включении функции **Поддержка нескольких способов поставки для самовывоза**, следует настроить новые способы доставки для каждой дополнительной создаваемой конфигурации способа поставки самовывозом. При добавлении способов поставки в сетку **Способ поставки "самовывоз"** Commerce проверяет, не используются ли они уже в каких-либо активных строках продаж. Если найдены какие-либо открытые строки продаж, выводится сообщение об ошибке. Способы поставки не считаются способами доставки для самовывоза, пока не будут закрыты все открытые строки продаж, которые их используют (с выставленными счетами или отмененные).


### <a name="e-commerce-site-configurations"></a>Настройки сайта электронной коммерции

Когда включена функция **Поддержка нескольких способов поставки для самовывоза**, в следующих модулях на страницах электронной коммерции отображаются новые способы поставки самовывозом в соответствии с настройкой:

- Поле покупки
- Селектор магазина
- Корзина
- Сведения о вывозе
- Подтверждение заказа
- Сведения о заказе

Никаких дополнительных шагов на страницах электронной коммерции не требуется, чтобы сделать доступными способ поставки самовывозом.

## <a name="work-with-multiple-pickup-delivery-modes"></a>Работа с несколькими способами поставки самовывозом

Когда для канала доступно несколько способов поставки самовывозом, для клиентов предоставляется расширенный опыт, когда они покупают продукты, которые будут получены самовывозом. 

- В каналах электронной коммерции покупатели могут выбрать любой доступный способ поставки для самовывоза. Например, розничный продавец определяет два способа поставки при самовывозе (самовывоз из магазина и получение в окне выдачи), и оба они настраиваются в сетке **Способ поставки "самовывоз"**, и оба варианта действительны для канала выполнения заказа и продукта, приобретаемого покупателем в данный момент. В этом случае покупатель может выбрать предпочтительный способ поставки для самовывоза. Выбранный способ поставки самовывозом затем становится способом поставки, который связан со строкой заказа на продажу, когда заказ создается в Commerce Headquarters.

    ![Выбор параметра самовывоза в электронной коммерции.](media/pickupecommerce.png)

- В каналах магазина, если заказ клиента для самовывоза создается через приложение POS-терминала, продавцу предлагается выбрать один из доступных способов поставки для самовывоза, если они были настроены. Если только один допустимый способ поставки самовывозом доступен для канала и номенклатуры, продавцу не предлагается выбрать его. Вместо этого к строкам заказа автоматически применяется доступный способ поставки самовывозом.

    ![Выбор параметра самовывоза в приложении POS-терминала.](media/pickuppos.png)

- Когда пользователи создают заказы с самовывозом в каналах центра обработки вызовов, они могут вручную выбрать любой определенный способ поставки для самовывоза, который связан с каналом центра обработки вызовов. Затем система проверяет, можно ли использовать выбранный способ поставки самовывозом при заказе номенклатуры, которая привязывается к заказу. Если в каналах центра обработки вызовов выбран способ поставки самовывозом, строки заказа на продажу должны быть привязаны к допустимому складу магазина. Если в строке продаж центра обработки вызовов определен склад, не являющийся складом магазина, режим поставки самовывозом нельзя настроить для этой строки продаж.
- Продавец может использовать операцию **Вызов заказа** или **Выполнение заказов** в приложении POS-терминала для вызова списка заказов или строк заказа для самовывоза. Если продавец использует готовый фильтр поиска для отображения всех заказов, которые будут получены самовывозом в текущем магазине, запросы изменяются, чтобы гарантировать, что в результаты поиска включены все подходящие заказы, в которых используется любой способ поставки самовывозом. Пользователи POS-терминала могут также использовать существующие фильтры для уточнения списка заказов до определенного способа поставки самовывозом. Например, они могут показывать заказы только для самовывозом из окна выдачи.

    ![Фильтр для способов поставки самовывозом, примененный к списку вызванных заказов.](media/pickuprecallorder.png)

## <a name="considerations-for-distributed-order-management"></a>Соображения для распределенного управления заказами

Функции [распределенного управления заказами (DOM)](./dom.md) в Commerce игнорируют все строки продаж, помеченные для самовывоза из магазинов. Эти функции были обновлены, чтобы гарантировать, что строки продаж, связанные с настроенными способами поставки самовывозом, обходят логику DOM и не будут перераспределены на новый склад выполнения.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
