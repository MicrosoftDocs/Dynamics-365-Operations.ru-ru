---
title: Сделать готовую продукцию физически доступной до разноски по журналам
description: Когда произведенная номенклатура принята, она регистрируется в качестве доступной для дальнейшей физической обработки и разносится в один или несколько журналов. В этой статье описывается, как отложить разноску по журналам, разрешая их обработку пакетным заданием в очереди сообщений.
author: johanhoffmann
ms.date: 08/02/2022
ms.topic: article
ms.search.form: ProdParameters, JmgProdParameters, InventLocation, JmgMES3PMessageProcessorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-08-02
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: ee767a5d7c3dca2681861802ae42d7a07217c54d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689349"
---
# <a name="make-finished-goods-physically-available-before-posting-to-journals"></a>Сделать готовую продукцию физически доступной до разноски по журналам

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Когда работник принимает произведенную номенклатуру, система регистрирует ее доступность для дальнейшей физической обработки (например, для отгрузки или размещения на складе). В ходе этого процесса также производится разноска в один или несколько журналов (например, журнал принятых, журнал листов подбора и журнал карты маршрута). Если необходимо обеспечить физическую доступность номенклатур, прежде чем все разноски будут обработаны, можно настроить в системе отсрочку разноски по журналам. Отложенные разноски затем обрабатываются пакетным заданием, которое выполняет их обработку, когда позволяют системные ресурсы.

На следующем рисунке показано, как процессы для журналов разноски вызываются как с отложенной разноской, так и без нее.

![Процесс приемки с отложенной разноской по журналам и без нее.](media/deferred-posting-flowchart.png "Процесс приемки с отложенной разноской по журналам и без нее")

## <a name="turn-on-deferred-journal-posting-for-your-system"></a>Включение в системе отложенной разноски по журналам

Прежде чем использовать отложенную разноску по журналам, необходимо включить ее в системе. Администраторы могут использовать рабочую область [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения. В рабочей области **Управление функциями** эта функция перечисляется следующими способами:

- **Модуль:** *Управление производством*
- **Название функции** *(Предварительная версия) Сделать готовую продукцию физически доступной до разноски по журналам*

## <a name="set-up-journal-posting-options-for-reporting-as-finished"></a>Настройка параметров разноски по журналам для приемки

Работники могут осуществлять приемку номенклатур с помощью любого из перечисленных ниже клиентов.

- Веб-клиент
- Мобильное приложение Warehouse Management
- Интерфейс выполнения производственного цеха

Веб-клиент использует ту же конфигурацию метода разноски, что и мобильное приложение Warehouse Management. Однако метод разноски, используемый интерфейсом выполнения производственного цеха, необходимо настраивать отдельно.

### <a name="set-journal-posting-options-for-the-web-client-and-the-warehouse-management-mobile-app"></a>Настройка параметров разноски журнала для веб-клиента и мобильного приложения Warehouse Management

В мобильном приложении работники осуществляют приемку номенклатур, открывая пункт меню мобильного устройства, в котором пункт **Процесс создания работы** имеет значение *Приемка* или *Приемка и размещение*. В веб-клиенте работники осуществляют приемку номенклатур со страницы списка **Все производственные заказы** или со страницы **Производственный заказ (сведения)**. Можно настроить метод по умолчанию для всей компании, также настроить необходимое переопределение для склада.

Используйте описанную ниже процедуру для настройки метода разноски по умолчанию на уровне компании для приемки номенклатуры из веб-клиента или из мобильного приложения Warehouse Management.

1. Перейдите в раздел **Управление производством \> Настройка \> Параметры управления производством**.
1. На вкладке **Журналы** в разделе **Журнал приемки** выберите в поле **Метод разноски** одно из следующих значений:

    - *Немедленно* — при приемке номенклатуры система полностью обрабатывает все соответствующие разноски по журналам, прежде чем отметить готовую номенклатуру как физическая доступную.
    - *Отложено* — при приемке номенклатуры система отмечает готовую номенклатуру как физическая доступную и добавляет разноску по журналам в очередь сообщений. Система отмечает готовую номенклатуру как физически доступную, не дожидаясь полной обработки разносок.

Описанная ниже процедура используется для настройки переопределений для конкретного склада для метода разноски по умолчанию, который настроен на странице **Параметры управления производством**.

1. Перейдите в раздел **Управление складом \> Настройка \> Разделение запасов \> Склады**.
1. Выберите склад, который необходимо настроить.
1. На панели операций выберите **Правка**.
1. На экспресс-вкладке **Склад** в разделе **Производственные заказы** выберите в поле **Метод разноски** одно из приведенных ниже значений.

    - *Наследовать* — выбранный склад наследует настройку со страницы **Параметры управления производством**.
    - *Немедленно* — при приемке номенклатуры система полностью обрабатывает все соответствующие разноски по журналам, прежде чем отметить готовую номенклатуру как физическая доступную.
    - *Отложено* — при приемке номенклатуры система отмечает готовую номенклатуру как физическая доступную и добавляет разноску по журналам в очередь сообщений. Система отмечает готовую номенклатуру как физически доступную, не дожидаясь полной обработки разносок.

### <a name="set-journal-posting-options-for-the-production-floor-execution-interface"></a>Настройка параметров разноски по журналам для интерфейса выполнения производственного цеха

Используйте описанную ниже процедуру для настройки метода разноски, который используется при приемке номенклатур из интерфейса выполнения производственного цеха.

1. Перейдите в раздел **Управление производством \> Настройка \> Управление производством \> Значения по умолчанию для производственного заказа**.
1. На вкладке **Приемка** в разделе **Журнал приемки** выберите в поле **Метод разноски** одно из приведенных ниже значений.

    - *Немедленно* — при приемке номенклатуры система полностью обрабатывает все соответствующие разноски по журналам, прежде чем отметить готовую номенклатуру как физическая доступную.
    - *Отложено* — при приемке номенклатуры система отмечает готовую номенклатуру как физическая доступную и добавляет разноску по журналам в очередь сообщений. Система отмечает готовую номенклатуру как физически доступную, не дожидаясь полной обработки разносок.

## <a name="schedule-the-message-processor-batch-job-to-process-deferred-postings"></a>Планирование пакетного задания обработчика сообщений для обработки отложенных разносок

Пакетное задание обработчика сообщений отвечает за обработку разносок по журналам после их помещения в очередь. Чтобы обеспечить обработку разносок журналов, необходимо настроить выполнение этого задания через равные промежутки времени. Используйте описанную ниже процедуру настройки необходимого пакетного задания.

1. Перейдите в раздел **Администрирование системы \> Обработчик сообщений \> Обработчик сообщений**.
1. На экспресс-вкладке **Параметры** выберите в поле **Очередь сообщений** значение *Рабочая*.
1. На экспресс-вкладке **Выполнять в фоновом режиме** установите для параметра **Пакетная обработка** значение *Да*. Затем настройте повторяющийся график и другие параметры, если это необходимо. Эти настройки работают точно так же, как и в других видах [фоновых задач](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) в Microsoft Dynamics 365 Supply Chain Management.

## <a name="track-the-progress-of-your-deferred-postings"></a>Отслеживание хода выполнения отложенных разносок

Отложенные разноски журнала ставятся в очередь как *сообщения обработчика сообщений*, ожидающие обработки *обработчиком сообщений*. Обработчик сообщений необходимо настроить для запуска в качестве запланированного пакетного задания. Для просмотра сообщений отложенной разноски, которые были или будут обработаны обработчиком сообщений, перейдите в поле **Управление производством \> Производственные заказы \> Отложенная разноска производственного заказа**.

### <a name="message-grid-columns-and-filters"></a>Столбцы и фильтры сетки сообщений

Можно использовать поля в верхней части страницы **Отложенная разноска производственного заказа**, чтобы найти нужные вам конкретные сообщения.

Доступны следующие фильтры:

- **Тип сообщения** — укажите тип сообщений, которые будут отображаться в сетке.
- **Состояние сообщения** — укажите состояние сообщений, которые будут отображаться в сетке. Ниже перечислены возможные состояния.

    - *В очереди* — сообщение готово для обработки обработчиком сообщений.
    - *Обработано* — сообщение успешно обработано обработчиком сообщений.
    - *Отменено* — последняя попытка обработки сообщения завершилась неудачей, после чего оно было отменено пользователем.
    - *Не выполнено* — последняя попытка обработки сообщения завершилась неудачей. Система трижды повторит попытку отправки сообщений с ошибкой. После этого сообщение будет оставлено в состоянии *Сбой*. Обратите внимание, что сообщение нельзя отменить или изменить вручную, пока не будут произведены эти три попытки.

- **Содержимое сообщения** — этот фильтр выполняет полнотекстовый поиск содержимого сообщения. (Содержимое сообщения не показывается в сетке.) Фильтр воспринимает большинство специальных символов (таких как, например, дефисы) как пробелы и воспринимает все пробелы как логические операторы ИЛИ. Например, если при поиске определенного идентификатора `journalid` ввести *USMF-123456* в качестве значения фильтра, система найдет все сообщения, содержащие "USMF" или "123456". В этом случае список результатов может быть длинным. Таким образом, лучше ввести только *123456*, поскольку это приведет к получению более конкретных результатов.

Кроме того, можно отсортировать и отфильтровать список, выбрав один из заголовков столбцов и введя критерии в раскрывающемся диалоговом окне.

### <a name="view-the-message-log-message-content-and-details"></a>Просмотр журнала сообщений, содержимого сообщения и сведений

Подробные сведения о сообщении можно найти, выбрав его в сетке, а затем открыв вкладку **Журнал** или **Необработанное содержимое** в сетке сообщения, где отображается каждое событие обработки.

Панель инструментов на вкладке **Журнал** содержит следующие кнопки:

- **Журнал** — нажмите эту кнопку, чтобы отобразить результаты обработки. Эта кнопка особенно полезна в том случае, когда **результат обработки** сообщения имеет значение *сбой* и необходимо выяснить причины сбоя обработки.
- **Набор** — несколько операций обработки сообщений могут быть выполнены в рамках одного пакетного процесса. Нажмите эту кнопку, чтобы просмотреть подробные данные. Например, можно просмотреть, существуют ли зависимости, которые требуют обрабатывать некоторые сообщения в определенной последовательности.

### <a name="manually-process-or-cancel-a-message"></a>Обработка или отмена сообщения вручную

При необходимости можно вручную обработать или отменить сообщение (в зависимости от его текущего состояния). Выберите сообщение в сетке, а затем выберите команду **Обработать** или **Отменить** на панели операций.

### <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Настройка бизнес-событий для доставки оповещений по невыполненным результатам обработки

Вы можете настроить [бизнес-события](../../fin-ops-core/dev-itpro/business-events/home-page.md), уведомляющие о сбое обработки. Перейдите в раздел **Администрирование системы \> Настройка \> Бизнес-события \> Каталог бизнес-событий** и активируйте бизнес-событие с названием *Сообщение обработчика сообщений обработано*.

В ходе процесса активации вам предлагается указать, относится ли событие к одному юридическому лицу или применяется ко всем юридическим лицам. Кроме того, предлагается ввести **Имя конечной точки**. Это значение следует определить в первую очередь.

> [!NOTE]
> Если для поля **Когда бизнес-событие происходит** задано значение *Microsoft Power Automate* (а не *HTTPS*, например), **Имя конечной точки** будет автоматически создано в Supply Chain Management на основе настройки *Microsoft Power Automate*.
