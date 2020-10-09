---
title: Позиция кластера заполнена
description: В этом разделе содержится информация о функции заполненной позиции кластера. Эта функция предлагает альтернативу более жесткому принудительному выполнению правил перерывов в работе при использовании комплектации кластера, так как это позволяет увеличить предел ошибок в объемных ограничениях контейнеров или транспортной тары.
author: Mirzaab
manager: tfehr
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8d030afb568b158e6caf48b0044d595d6ec024f6
ms.sourcegitcommit: 06f64550b2043582de4018bdd3924fcc1fd5d310
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802222"
---
# <a name="cluster-position-full"></a>Позиция кластера заполнена

[!include [banner](../includes/banner.md)]

Функция *Позиция кластера заполнена* предлагает альтернативу более жесткому принудительному выполнению правил перерывов в работе при использовании комплектации кластера, так как это позволяет увеличить предел ошибок в объемных ограничениях контейнеров или транспортной тары. В общем случае не все номенклатуры в заказе на работу помещаются в выбранный контейнер. Работники склада, выполняющие комплектацию кластера, имеют мало вариантов в этом сценарии: они должны либо изменить контейнер на больший размер контейнера, либо работать со своим супервизором, чтобы найти другое решение.

Эта функция вводит возможность выполнения кнопки **Полный** на одном из рабочих блоков кластера. В предыдущих версиях этот параметр был доступен только для обычной комплектации заказа, а не для комплектации кластера. Однако эта функция отличается от стандартной кнопки **Полный** в том, что отменяет оставшуюся работу. Она не предлагает пользователю добавить другую ячейку в тот же кластер, и она не создает новую работу автоматически.

## <a name="turn-on-the-cluster-position-full-feature"></a>Включение функции "Позиция кластера заполнена"

Прежде чем использовать эту функцию, она должна быть включена в системе. Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения. В рабочей области **Управление функциями** эта функция перечисляется следующими способами:

- **Модуль:** *Управление складом*
- **Название функции:** *Позиция кластера заполнена*

## <a name="setup"></a>Настройка

В этом разделе приводятся инструкции, а также пример, в котором показано, как настроить и использовать функцию *Позиция кластера заполнена*.

### <a name="make-sample-data-available"></a>Сделать образцы данных доступными

Для работы с этими [примером сценария](#example-scenario) с помощью образцов записей и значений, указанных здесь, необходимо использовать систему, в которой установлены стандартные [демонстрационные данные](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Дополнительно перед началом необходимо выбрать юридическое лицо **USMF**.

Этот пример сценария можно также использовать в качестве руководства по работе с этой функцией в производственной системе. Однако в этом случае необходимо подставить собственные значения для описанных здесь параметров.

### <a name="cluster-profiles"></a>Профили кластера

Необходимо указать, должны ли коды кластера создаваться автоматически, сколько должно использоваться позиций, когда кластеры нарушаются, и как задается последовательность и выполняется проверка работы по комплектации.

1. Перейдите **Управление складом \> Настройка \> Мобильное устройство \> Профили кластера**.
1. В области списка выберите запись **Создать кластер**.
1. На экспресс-вкладке **Общие** проверьте следующие значения:

    - **Создать код кластера:** *Да*
    - **Активировать позиции:** *Да*
    - **Число позиций:** *2*
    - **Имя позиции:** *Числовое*
    - **Разделить кластер при:** *Размещение*
    - **Тип проверка сортировки:** *Скан позиции*

1. На экспресс-вкладке **Сортировка кластера**. Сетка должна быть пустой (то есть, она не должна содержать строк).

### <a name="work-templates"></a>Шаблоны работ

Необходимо определить, как создается работа комплектации для комплектации кластера.

1. Перейдите в раздел **Управление складом \> Настройка \> Работа \> Шаблоны работ**.
1. В верхней части страницы задайте для поля **Тип заказа на работу** значение *Заказы на продажу*.
1. Убедитесь, что следующие шаблоны работы из демонстрационных данных перечислены. Если они недоступны, выполнение сценария будет невозможно.

    - 61 Этап заказа на продажу
    - 61 Комплектация кластера заказа на продажу

### <a name="location-directives"></a>Директивы для мест хранения

Необходимо указать, откуда будут комплектоваться номенклатуры, и где они будут помещены.

1. Перейдите в раздел **Управление складом \> Настройка \> Директивы местонахождения**.
1. В заголовке списка задайте в поле **Тип заказа на работу** значение *Заказы на продажу*.
1. Убедитесь, что следующие директивы заказа на продажу из демонстрационных данных перечислены. Если они недоступны, выполнение сценария будет невозможно.

    - 61 Комплектация кластера
    - 61 Комплектация заказа на продажу

### <a name="mobile-device-menu-items"></a>Пункты меню мобильного устройства

Необходимо настроить пункт меню мобильного устройства для использования существующей работы под управлением комплектации кластера. В пункте меню мобильного устройства для комплектации кластера параметр **Разрешить разделение работы** должен быть включен, и должен быть добавлен класс работы *Комплектация заказа на продажу*.

1. Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Пункты меню мобильного устройства**.
1. В области списка выберите запись **Создать комплектацию кластера**.
1. Выберите **Правка** на панели операций.
1. На экспресс-вкладке **Общие** установите следующие значения.

    - **Кем управляется:** *Комплектация кластера*
    - **Создать грузоместо:** *Да*
    - **Разрешить разделение работы:** *Да*
    - **Код профиля кластера:** *Создать кластер*

    Примите для всех остальных полей значения по умолчанию.

1. На экспресс-вкладке **Классы работы** добавьте следующие две строки, как требуется:

    - Строка 1 (обычно содержится в демонстрационных данных):

        - **Код класса работы:** *Продажи* 
        - **Тип заказа на работу:** *Заказы на продажу*

    - Строка 2 (возможно, отсутствует в демонстрационных данных):

        - **Код класса работы:** *Комплектация заказа на продажу*
        - **Тип заказа на работу:** *Заказы на продажу*

1. Перейдите к пункту **Настройка подтверждения работы** на панели операций.
1. Выберите **Правка**.
1. Введите следующие значения в строке в сетке.
    - **Тип работы** - *Комплектация*
    - **Подтверждение продукта** - *Установите флажок*

1. Выберите **Сохранить** на панели операций и закройте страницу.

## <a name="create-picking-work"></a>Создать работы комплектации

Перед началом комплектации кластера необходимо создать некоторую исходящую работу. Профиль кластера, созданный ранее, определяет две позиции кластера. Поэтому для комплектации заказа на продажу должно быть создано по крайней мере два кода рабочих процессов. В этом случае проводки будут выполняться на складе *61*, и в них будут использоваться номенклатуры *L0101* и *T0100*. Демонстрационные данные должны иметь достаточное количество запасов в наличии для этих номенклатур. Убедитесь, что имеется достаточное количество запасов для выполнения проводок.

### <a name="create-sales-order-1"></a>Создание заказа на продажу 1

1. Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.
1. Выберите **Создать**, чтобы создать заказ на продажу 1.
1. В диалоговом окне **Создание заказа на продажу** установите следующие значения:

    - **Счет клиента:** *US-010*
    - **Склад:** *61*

1. Нажмите **ОК**.
1. Открывается новый заказ на продажу. На экспресс-вкладке **Строки заказа на продажу** добавьте строку со следующими параметрами:

    - **Код номенклатуры:** *T0100*
    - **Количество:** *5*

1. На экспресс-вкладке **Сведения о строке** на вкладке **Доставка** установите в поле **Подтвержденная дата отгрузки** текущую дату.
1. На экспресс-вкладке **Строки заказа на продажу** добавьте вторую строку со следующими параметрами:

    - **Код номенклатуры:** *L0101*
    - **Количество:** *20*

1. На экспресс-вкладке **Сведения о строке** на вкладке **Доставка** установите в поле **Подтвержденная дата отгрузки** текущую дату.
1. Для каждой только что добавленной строки выполните следующие действия, чтобы зарезервировать запасы:

    1. Выберите строку для резервирования.
    2. На экспресс-вкладке **Строки заказа на продажу** выберите **Запасы \> Резервирование**.
    3. На странице **Резервирование** на панели операций выберите **Резервирование лота** для резервирования запасов.
    4. Закройте страницу **Резервирование**.

1. На панели операций на вкладке **Склад** выберите вариант **Выпустить на склад**.

    Когда выпуск будет завершен, вы получите информационные сообщения, которые указывают коды волны и загрузки, которые были созданы.

### <a name="create-sales-order-2"></a>Создание заказа на продажу 2

1. Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.
1. Выберите **Создать**, чтобы создать заказ на продажу 2.
1. В диалоговом окне **Создание заказа на продажу** установите следующие значения:

    - **Счет клиента:** *US-011*
    - **Склад:** *61*

1. Нажмите **ОК**.
1. Открывается новый заказ на продажу. На экспресс-вкладке **Строки заказа на продажу** добавьте строку со следующими параметрами:

    - **Код номенклатуры:** *L0101*
    - **Количество:** *20*

1. На экспресс-вкладке **Сведения о строке** на вкладке **Доставка** установите в поле **Подтвержденная дата отгрузки** текущую дату.
1. На экспресс-вкладке **Строки заказа на продажу** добавьте вторую строку со следующими параметрами:

    - **Код номенклатуры:** *T0100*
    - **Количество:** *2*

1. На экспресс-вкладке **Сведения о строке** на вкладке **Доставка** установите в поле **Подтвержденная дата отгрузки** текущую дату.
1. Для каждой только что добавленной строки выполните следующие действия, чтобы зарезервировать запасы:

    1. Выберите строку для резервирования.
    2. На экспресс-вкладке **Строки заказа на продажу** выберите **Запасы \> Резервирование**.
    3. На странице **Резервирование** на панели операций выберите **Резервирование лота** для резервирования запасов.
    4. Закройте страницу **Резервирование**.

1. На панели операций на вкладке **Склад** выберите вариант **Выпустить на склад**.

    Когда выпуск будет завершен, вы получите информационные сообщения, которые указывают коды волны и загрузки, которые были созданы.

### <a name="get-work-ids-and-license-plate-numbers"></a>Получение кодов работ и номеров грузомест

Должны быть созданы два кода работ, каждая из которых содержит две строки комплектации. Выполните следующие действия, чтобы найти коды работ и назначения грузомест.

1. Перейдите в раздел **Управление складом \> Работа \> Сведения о работе**.
1. В сетке **Обзор** найдите столбец **Номер заказа** для двух только что созданных заказов на продажу. Для каждого заказа на продажу запишите соответствующий код работы.
1. Выберите строку для каждого заказа на продажу для отображения связанной информации в сетке **Строки**. Запишите местоположение, из которого будет комплектоваться каждая номенклатура.
1. Перейдите в раздел **Управление запасами \> Запросы и отчеты \> Список количества в наличии**.
1. На панели операций выберите **Аналитики**, чтобы открыть диалоговое окно **Отображение аналитики**.
1. Убедитесь, что установлены флажки **Грузоместо**, **Склад** и **Номер номенклатуры**, затем выберите **ОК**.
1. На панели **Фильтр** настройте следующие фильтры:

    - **Код номенклатуры** — **один из** — *L0101* и *T100*
    - **Склад** — **начинается с** — *61*

1. Запишите отображаемые значения **Грузоместо**.

## <a name="example-scenario"></a><a name="example-scenario"></a>Пример сценария

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a>Выполнение потока мобильных устройств — настройка подтверждения работы для продукта

1. Выполните вход в приложение склада как пользователь на складе *61*.
1. Выберите **Исходящие \> Создание комплектации кластера**.

    Отображается страница **ЗАДАЧА: назначение работы кластеру**.

1. Введите код работы для заказа на продажу 1, чтобы назначить его позиции кластера 1.
1. Выберите **ОК** (символ флажка).
1. Введите код работы для заказа на продажу 2, чтобы назначить его позиции кластера 2.
1. Выберите **ОК** (символ флажка).

    Открывается страница **ЗАДАЧА: создание комплектации кластера: комплектация** и отображается *Номенклатура L0101 2 палеты*.

Поскольку профиль кластера задает количество позиций равным 2, система автоматически направляет вас на первую консолидированную комплектацию: две палеты (PL) номенклатуры *L0101*.

В любой момент выполнения следующих шагов можно выбрать вкладку **Сведения**, чтобы просмотреть дополнительные сведения о задаче, такие как местоположение комплектации.

1. Задайте в поле **НОМЕНКЛАТУРА** значение *L0101*. Это подтверждает код номенклатуры, необходимый для этого пункта меню (вы настроили этот параметр ранее, выбрав **Настройка подтверждения работы** на странице **Пункт меню мобильного устройства** при создании этого пункта меню).
1. Введите номер грузоместа, связанной с номенклатурой в комплектуемом местоположении. Вы будете комплектовать две палеты.
1. Установите в поле **LP** значение *LP\_PICK\_01*.
1. Выберите **ОК** (символ флажка).

    Будет открыта страница **ЗАДАЧА: Сортировка: Создание комплектации кластера**. Здесь будут сортироваться две скомплектованные палеты в позицию комплектации. Эта позиция может быть транспортной тарой или контейнером, который используется для разделения скомплектованных запасов по заказам на продажу.

1. Просмотрите сведения, отображаемые для номенклатуры (*L0101*) и количества (*20* шт.), которые будут отсортированы в позиции 1 (для заказа на продажу 1).
1. Установите для поля **ПОЗИЦИЯ НД** значение *1*.
1. Выберите **ОК** (символ флажка).
1. Просмотрите сведения, отображаемые для номенклатуры (*L0101*) и количества (*20* шт.), которые будут отсортированы в позиции 2 (для заказа на продажу 2).
1. Установите для поля **ПОЗИЦИЯ НД** значение *2*.
1. Выберите **ОК** (символ флажка).

    Открывается страница **ЗАДАЧА: создание комплектации кластера: комплектация** и отображается *Номенклатура T0100 7 шт*.

В этом сценарии позиция 1 не может принять все количество номенклатур, которые должны быть скомплектованы для выполнения заказа на продажу 1. Позиция должна быть помечена как заполненная. В этом случае будет выполнена частичная комплектация для второй номенклатуры. Вторая номенклатура будет частично укомплектована для позиции 1, и будет создана новая работа с целью комплектации оставшегося количества для удовлетворения заказа.

1. Выберите кнопку меню (иногда называется "гамбургер" или "кнопка-гамбургер"), затем выберите **Позиция заполнена**.
1. Определите заполненную позиции и выберите значение *1*.
1. Выберите **ОК** (символ флажка).
1. Введите количество комплектации, которое еще нужно скомплектовать в позицию 1. Система может определить номер комплектуемой номенклатуры.
1. Введите *2*.
1. Выберите **ОК** (символ флажка).
1. Подтвердите код номенклатуры, чтобы завершить комплектацию оставшейся номенклатуры в позицию 2.
1. Задайте в поле **НОМЕНКЛАТУРА** значение *T0100*.
1. Выберите **ОК** (символ флажка).
1. Введите грузоместо, из которого осуществляется комплектация номенклатуры, задав в поле **LP** значение *LPREPL04*.
1. Выберите **ОК** (символ флажка).
1. Просмотрите сведения, отображаемые для номенклатуры (*T0100*) и количества (*2* шт.), которые будут отсортированы в позиции 2 (для заказа на продажу 2).
1. Установите для поля **ПОЗИЦИЯ НД** значение *2*.
1. Выберите **ОК** (символ флажка).
1. Просмотрите сведения, отображаемые для номенклатуры (*T0100*) и количества (*2* шт.), которые будут отсортированы в позиции 1 (для заказа на продажу 1).
1. Установите для поля **ПОЗИЦИЯ НД** значение *1*.
1. Выберите **ОК** (символ флажка).

    Будет открыта страница **ЗАДАЧА: Создание комплектации кластера: Размещение**.

В этом сценарии комплектация кластера завершена, и пользователь направляется на размещение скомплектованных номенклатур из позиции 1 и позиции 2 в промежуточном местоположении *STAGE01*.

1. Просмотрите сведения на странице. Она показывает, что общее количество *44* будет помещено в промежуточное местоположение.
1. Выберите **ОК** (символ флажка).

    Будет получено сообщение "Кластер завершен".

Теперь можно использовать пункт меню **Комплектация продаж** для комплектации оставшегося количества. Затем можно воспользоваться пунктом меню **Загрузка продаж**, чтобы переместить номенклатуры из промежуточного местоположения на погрузочный док.