---
title: "Кросс-докинг из производственных заказов в дебаркадеры отгрузки | Microsoft Docs"
description: "В этом разделе описывается, как управлять процессом кросс-докинга материала, который принят из производственной линии в транспортный док отгрузки."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 0b5541b6752da0c73e4309951ecabc0793f24289
ms.contentlocale: ru-ru
ms.lasthandoff: 06/20/2017

---

# <a name="cross-docking-from-production-orders-to-outbound-docks"></a>Кросс-докинг из производственных заказов в дебаркадеры отгрузки

В этом разделе описывается, как управлять процессом кросс-докинга материала, который принят из производственной линии в транспортный док отгрузки.

<a name="introduction"></a>Приветствие
------------

Кросс-докинг из производства в место отгрузки относится к производителям, которые производят большие объемы и в идеале хотят отгрузить готовую продукцию, как только она принята из производственной линии. Целью является отгрузить продукты в центры распределения, которые физически расположены рядом с желаемым местом клиента, а не создавать запасы на объекте производства.

Если нет немедленного спроса на продукцию, ее необходимо разместить на складах на объекте производства. Этот процесс называется также *рациональный кросс-докинг*, который означает, что если имеется спрос на отгрузку продукта, такую возможность следует использовать вместо перемещения продукта из внутреннего хранилища.

В следующем примере показаны три варианта потока, который начинается по завершению производственного потока (2).

Продукт принят в выходное местоположение производства (3) и водитель погрузчика забирает палету в этом местоположении (3).

-   Если есть запланированное мероприятие (6) для перемещения продукта из производства (1) в центр распределения (7), система скажет водителю грузовика разместить палету у двери (4).
-   Если для двери уже назначен прицеп, водителю грузовика будет сказано загрузить продукт непосредственно в прицеп.
-   При отсутствии запланированного мероприятия по перемещению продукта, водителю погрузчика будет сказано отвезти продукт в местоположение на внутреннем складе (5).

[![](./media/scenario1.png)](./media/scenario1.png)

## <a name="configure-cross-docking"></a>Настройка кросс докинга
Кросс-докинг настраивается в **политиках работы**. Политика работы включает тип заказа на выполнение работ, местоположение и продукт. В следующем примере кросс-докинг настраивается для продукта X и местоположения Y.

#### <a name="work-order-types"></a>Типы заказов на выполнение работ

-   Тип заказа на выполнение работ: отложенная готовая продукция
-   Метод создания работы: кросс-докинг
-   Имя политики кросс-докинга: заказы на перемещение

#### <a name="inventory-locations"></a>Места хранения

-   Склад: 51
-   Местоположение: Y

#### <a name="products"></a>Товары

-   Номер номенклатуры: X

В настоящее время кросс-докинг можно настроить только двух типов заказов на выполнение работ:

-   Готовая продукция разгружена
-   Размещение побочных и попутных продуктов

В **политике кросс-докинга** определяется, какие типы документов применимы для кросс докинга. В настоящее время поддерживаемым типом документа является только **Заказы на перемещение**. В следующем примере показана конфигурация политики кросс докинга.

### <a name="cross-docking-policy-name-transfer-order"></a>Имя политики кросс-докинга: заказ на перемещение

-   Порядковый номер: 10
-   Тип заказа на выполнение работ: выдача на перемещение
-   Для спроса кросс-докинга требуется местонахождение: false
-   Стратегия кросс-докинга: дата и время

### <a name="sequence-number"></a>Порядковый номер

**Порядковый номер** указывает приоритет типа документа. В настоящее время поддерживаемым типом документа является только **Выдача на перемещение**. Таким образом, порядковый номер будет обоснованным только тогда, когда поддерживаются дополнительные типы заказов на выполнение работ.

### <a name="cross-docking-policy"></a>Политика кросс-докинга

Политика кросс-докинга также устанавливает политику для определения приоритетов спроса по заказу на перемещение. Например если несколько заказов на перемещение существует для одного продукта, запланированная дата и время, заданные для загрузки и связанные с заказом на перемещение, определяют приоритет между заказами. Запланированные дату и время можно задать непосредственно для загрузки или их можно задать в **графике встречи**, связанном с загрузкой. Определение приоритетов задается стратегией кросс-докинга. В настоящее время существует только одна стратегия: **Дата и время**.

### <a name="cross-docking-demand-requires-location"></a>Для спроса кросс-докинга требуется местонахождение

В политике кросс-докинга, можно настроить критерий требования у заказов на перемещение наличия назначенного местоположения, чтобы кросс-докинг был обоснован. Этот критерий задается в поле **Для спроса кросс-докинга требуется местонахождение**. Местоположение в графике встречи, связанное с загрузкой, используется как конечное местоположение для товаров кросс-докинга. Конечное расположение для товаров кросс-докинга определяется директивой местоположения для **Выдача на перемещение** для типа заказа на выполнение работ **Разместить**. Может оказаться полезным задать поле **Для спроса кросс-докинга требуется местонахождение** в сценарии, где готовая продукция должна быть подвергнута кросс-докингу только в том случае, если прицепу назначена дверь. При этом сценарии товары перемещаются непосредственно из производства в прицеп. При назначении прицепа для двери пользователь назначит местоположение для графика встречи и таким образом сделает местоположение применимым для кросс докинга. В следующих разделах описаны два примера.

#### <a name="scenario-1--cross-docking-from-production-to-transfer-orders"></a>Сценарий 1. Кросс-докинг из производства в заказы на перемещение

После принятия продукта в производстве он перемещается в местоположение двери, где он загружается в грузовик и перемещается в центр распределения. Используйте USMF компании.

1.  Включите новую номерную серию для кросс докинга. Выберите страницу **Номерные серии** и нажмите кнопку **Создать**. Мастер поможет выполнить процесс.
2.  Создайте политику кросс-докинга. Выберите страницу **Политика кросс-докинга** и создайте новую политику с именем **Кросс-докинга в заказ на перемещение**. Обратите внимание, что тип заказа на выполнение работ, который можно выбрать, только **Выдача на перемещение**, и единственная стратегия кросс-докинга — **Дата и время**.
3.  Создайте политику работы. Выберите страницу **Политики работы** страницы и создайте новую политику работы с именем **Cross Dock L0101**.
4.  Настройте загрузки, чтобы они автоматически создавались для заказов на перемещение. В параметрах склада настройте загрузки, чтобы они создавались автоматически при создании заказов на перемещение. Загрузка является обязательным условием для обоснования заказа на перемещение для кросс-докинга.
5.  Настройте сопоставление загрузок номенклатур. Выберите страницу **Сопоставление загрузки номенклатуры** и настройте стандартный шаблон загрузки для номенклатурной группы **CarAudio**. Это сопоставление будет автоматически вставлять шаблон нагрузки в нагрузку при создании заказа на перемещение.
6.  Создайте заказ на перемещение. Создайте заказ на перемещение для кода номенклатуры L0101. Количество = 20.
7.  Запустите заказ на перемещение от рабочего места планирования загрузки. На вкладке **Отгрузка** выберите пункт меню для рабочего места планирования загрузки и в меню **Запуск** строки загрузки выберите **Запуск на склад**. Теперь для заказа на перемещение существует строка открытой волны типа **Выдача на перемещение**.
8.  Создайте производственный заказ. Выберите страницу со списком **Производственный заказ** и создайте производственный заказ для продукта L0101. Количество = 20. Оцените и запустите производственный заказ. Обратите внимание, что в поле **Разнести отгрузочную накладную** остается значение **Нет**.
9.  Примите с мобильного устройства. Перейдите в портала мобильного устройства и выберите пункт меню **Приемка и размещение**. Теперь примите L0101 с мобильного устройства. Обратите внимание, что местоположение размещения — **BAYDOOR**. Это расположение определяется по директиве местоположения **Выдача на перемещение** для типа заказа на выполнение работ **Разместить**. Также обратите внимание на то, работа типа **Выдача на перемещение** была создана и завершена. Перейдите к подробным сведениям по работе заказа на перемещение для проверки работы.
10. Теперь попробуйте запустить еще 20 штук по производственному заказу, а затем попробуйте принять 20 штук с помощью мобильного устройства. В этот раз местоположение **LP-001** будет предложено местоположение размещения. Это расположение определяется из директивы местоположения для **Готовая продукция разгружена**. Эта директива расположения используется, поскольку нет возможности для кросс-докинга. Заказ на перемещение для LP-001 был полностью выполнен первым мероприятием кросс-докинга.

Работа типа **Готовая продукция разгружена** была создана и обработана.

#### <a name="scenario-2---cross-docking-from-production-to-transfer-orders-with-an-appointment-schedule"></a>Сценарий 2. Кросс-докинг из производства для заказов на перемещение с графиком встречи

После принятия продукта на производстве он перемещается в местоположение двери, которое определяется по графику встречи для местоположений дверей. Используйте USMF компании.

1.  Измените политику кросс-докинга. Измените политику кросс-докинга, созданную в сценарии 1, установив флажок **Для спроса кросс-докинга требуется местонахождение**.
2.  Создайте новый заказ на перемещение.
3.  Откройте **Рабочее место планирования загрузки**.
4.  В рабочем месте планирования загрузки откройте раздел **Загрузки** и выберите **График встречи** в меню **Транспортировка**, чтобы создать новый график встречи. Обратите внимание, что в графике встречи есть ссылка на заказ на перемещение в поле **Номер заказа**. В поле **Плановая дата и время начала в местонахождении** можно задать дату и время встречи. Эти дата и время будут использоваться, когда спрос кросс-докинга будет приоритетным в процессе кросс-докинга. Дата и время, заданные в этом поле, обновят поле **Планируемые дата и время отгрузки груза** при соответствующей загрузке. Местоположение на экспресс-вкладке **Детали отгрузки** определяет местоположение, куда отгружается заказ на перемещение.
5.  На **Рабочем месте планирования загрузки** осуществляется выпуск на склад.
6.  Создайте производственный заказ для кода номенклатуры **L0101** и задайте статус **Начато** с количеством 20.
7.  Примите с мобильного устройства.
8.  Перейдите в портал мобильного устройства и выберите пункт меню **Приемка и размещение**.
9.  Примите код номенклатуры **L0101** с мобильного устройства. Обратите внимание, что местоположение размещения теперь — **BAYDOOR 2**. Это местоположение определяется из графика встречи, а не из директивы местоположения **Приход переноса**.

### <a name="additional-information"></a>Дополнительные сведения

-   Сценарий кросс-докинга поддерживается для партии и номенклатур, контролируемых серийными номерами, с аналитиками партии и серийными номерами, определенными выше и снизу от местоположения в иерархии резервирования.
-   Количество, которое является принятым, не может быть разделено на спрос заказа на перемещение, который меньше. Например, если 20 штук принимаются и есть заказ на перемещение на 5 штук, заказ на перемещение не будет считаться применимым для кросс-докинга.


