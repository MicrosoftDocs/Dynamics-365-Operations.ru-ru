---
title: Настройка сценария для бизнес-аналитики Интернета вещей
description: В этой теме объясняется, как настроить сценарии для бизнес-аналитики Интернета вещей в Microsoft Dynamics 365 Supply Chain Management.
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 36be4a85dbbd28839afd45b6ed167b4c8181ae72
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909509"
---
# <a name="scenario-setup-for-iot-intelligence"></a>Настройка сценария для бизнес-аналитики Интернета вещей

[!include [banner](../../includes/banner.md)]

В этой теме объясняется, как настроить сценарии для бизнес-аналитики Интернета вещей в Microsoft Dynamics 365 Supply Chain Management. Перед настройкой сценариев необходимо [настроить Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).

В этом разделе можно настроить сценарий **простой оборудования**, чтобы создалось уведомление в Supply Chain Management при отключении компьютера. Кроме того, в этом разделе показано, как настроить сценарий **Качество продукта** таким образом, чтобы уведомление создавалось, если атрибут элемента выходит за пределы указанного диапазона, и как настроить сценарий **Задержки производства** таким образом, чтобы уведомление создавалось, если производительность производства падает ниже порогового значения.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Настройка сценария простой оборудования в Supply Chain Management

В сценарии **Простой оборудования** сопоставляется сигнал **PartOut** для порога оповещения оборудования. Наблюдение за оборудованием осуществляется только в том случае, если оно выбрано для сценария, и когда оно настроено на **Выполняется** в Supply Chain Management. Если время, прошедшее с момента последнего получения сигнала **PartOut** от оборудования, превышает порог оповещения, то уведомление **Оборудование не работает** запускается. Если оборудование все еще работает, при получении следующего сигнала **PartOut** запускается уведомление **Оборудование работает**. Если оборудование остается выключенным в течение 30 минут, будет запущено новое уведомление **Оборудование не работает**.

В сценарии **Простой оборудования** имеются следующие зависимости:

+ Оповещение может быть запущено только в том случае, если производственный заказ запущен на сопоставленном оборудовании.
+ Сигнал, представляющий сигнал **PartOut** сопоставленного оборудования, должен быть отправлен в Центр Интернета вещей, и уникальное имя свойства должно быть включено.
+ Свойство UNIX **timestamp**, значение которого выражается в миллисекундах (мс), должно присутствовать в сообщении Центра Интернета вещей Azure.

Выполните следующие действия, чтобы настроить сценарий.

1. Войдите в Supply Chain Management.
2. Включите флаг функции аналитики Интернета вещей. Дополнительные сведения см. в разделе [Обзор управления функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
3. Настройка метрик. Дополнительные сведения см. в [Как настроить метрики](iot-metrics-setup.md#configure-metrics).
4. Выберите **Управление производством \> Настройка \> Бизнес-аналитика Интернета вещей \> Управление сценариями**.
6. На плитке **Время простоя оборудования** выберите **Настроить**, чтобы открыть мастер настройки конфигурации.

   Первая страница в мастере является страницей **Определение схемы датчика оборудования**. На этой странице вам требуется настроить схему в Supply Chain Management так, чтобы она соответствовала формату нотации объектов JavaScript (JSON) в сообщениях Центра Интернета вещей. Можно определить несколько схем сообщений. Дополнительные сведения см. в разделе [форматы схем для сообщений Центра Интернета вещей](iot-schema-format.md). В данном примере полезная нагрузка сообщения содержит пакет сообщений, которые имеют следующий формат.

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. Добавьте строку в таблицу и задайте следующие значения:

    1. Установите поле **Имя схемы** на **Код**.
    2. Установите поле **Путь схемы** на **/полезная нагрузка\[\*\]/код**.
    3. Установите поле **Описание** на **Код сообщения**.

8. Добавьте еще одну строку в таблицу и задайте следующие значения:

    1. Установите поле **Имя схемы** на **Метка времени**.
    2. Установите поле **Путь схемы** на **/полезная нагрузка\[\*\]/метка времени**.
    3. Установите поле **Описание** на **Метка времени сообщения**.

9. Добавьте еще одну строку в таблицу и задайте следующие значения:

    1. Установите поле **Имя схемы** на **Значение**.
    2. Установите поле **Путь схемы** на **/полезная нагрузка\[\*\]/значение**.
    3. Установите поле **Описание** на **Значение сообщения**.

    > [!NOTE]
    > Вам не придется определять все свойства в сообщении. Определите только нужные вам свойства. В предыдущих шагах не была создана строка для параметра **Корневая метка времени**. Путь **корневой метки времени** должен быть **/метка времени**.

10. Выберите **Далее**, чтобы перейти на страницу **Сопоставление схемы датчика оборудования**.
11. В строке **Код ресурса оборудования** в поле **Имя схемы** выберите **Код**.
12. В строке для **времени UTC** в поле **Имя схемы** выберите **Метка времени**.
13. В строке для параметра **Сигнал произведенной части** в поле **Имя схемы** выберите **Значение**.
14. Выберите **Далее**, чтобы перейти на страницу **Конфигурация кода ресурса оборудования**.
15. Выполните эти шаги для сопоставления значений в сообщении Центра Интернета вещей с ресурсами Supply Chain Management.

    1. В таблице **Значения данных сигналов** добавьте новую строку. В поле **Значение** введите **IoTInt.Machine1225.PartOut**. Это значение поступает из свойства JSON **id** в сообщении Центра Интернета вещей.
    2. Нажмите **Сохранить**.
    3. В таблице **Сопоставление бизнес-записей** выберите **Создать**. Значение по умолчанию для поля **Тип бизнес-записей** заполняется автоматически, и его не нужно менять.
    4. В поле **Бизнес-запись** выберите ресурс оборудования Supply Chain Management, с которого отправляется значение этого сигнала.
    5. Нажмите **Сохранить**.
    6. Повторите эти шаги, чтобы добавить сопоставление новых бизнес-записей для **Machine1226**. Можно сопоставить несколько значений данных сигналов одной записи в Supply Chain Management.

16. Используйте столбец **Выбрано** для выбора оборудования, которое необходимо обработать. Нет необходимости определять все значения сигнала, и вам не требуется выбирать все оборудование.
17. Выберите **Далее**, чтобы перейти на страницу **Конфигурация сигнала произведенных частей**.
18. В таблице **Значения данных сигнала** добавьте строку и установите поле **Значение** в **Истина**. Это значение поступает из свойства JSON **value** в сообщении Центра Интернета вещей. Можно добавить столько значений, сколько необходимо для сценария.
19. Нажмите **Сохранить**.
20. Выберите **Далее**, чтобы перейти на страницу **Порог простоя оборудования**. В списке приведено оборудование, ранее сопоставленное со значениями сигналов. На этой странице вы определите пороговое значение, чтобы определить, отключено ли оборудование. Например, если установить пороговое значение **10**, Supply Chain Management будет создавать уведомление, если в течение 10 минут не поступило сигнала **PartOut** с оборудования.
21. Выберите **Далее**, чтобы перейти к странице **Включить сценарий**. Установите этот параметр, чтобы включить сценарий.
22. Выберите **Готово**.

Настройка сценария теперь завершена. Аналитика Интернета вещей автоматически начнет обрабатывать сообщения Центра Интернета вещей.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Настройка сценария качество продукта в Supply Chain Management

Сценарий **качество продукта** создает уведомление, если атрибут номенклатуры выходит за пределы указанного диапазона. Например, датчика отправляет вес каждой номенклатуры в Центр Интернета вещей. Если номенклатура слишком тяжелая или слишком легкая, в Supply Chain Management будет создано уведомление.

В сценарии **Качество продукции** имеются следующие зависимости:

+ Оповещение может срабатывать только в том случае, если производственный заказ должен выполняться на сопоставленном оборудовании и создавать продукт с сопоставленным атрибутом партии.
+ Сигнал, представляющий атрибут партии, должен быть отправлен в Центр Интернета вещей, и уникальное имя свойства должно быть включено.
+ Свойство UNIX **timestamp**, значение которого выражается в мс, должно присутствовать в сообщении Центра Интернета вещей.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Настройка сценария задержки производства в Supply Chain Management

Сценарий **задержки производства** создает уведомление, если пропускная способность производства падает ниже порогового значения. В этом случае сигнал **PartOut** для каждой произведенной номенклатуры направляется в Центр Интернета вещей. В Supply Chain Management задержка заказа рассчитывается на основе количества времени, в течение которого запланировано выполнение производственного заказа, количество номенклатур, которые должны быть произведены, количество времени, в течение которого было запущено задание, а также количества полученных сигналов **PartOut**. Уведомление о задержке создается, если число сигналов **PartOut** для задания оказывается ниже порогового значения.

В сценарии **Задержки производства** имеются следующие зависимости:

+ Оповещение может быть запущено только в том случае, если производственный заказ запущен на сопоставленном оборудовании.
+ Сигнал, представляющий сигнал **PartOut** сопоставленного оборудования, должен быть отправлен в Центр Интернета вещей Azure, и уникальное имя свойства должно быть включено.
+ Свойство UNIX **timestamp**, значение которого выражается в мс, должно присутствовать в сообщении Центра Интернета вещей.

## <a name="disable-a-scenario"></a>Отключение сценария

Для отключения сценария выполните следующие действия.

1. В Supply Chain Management перейдите к **Управление производством \> Настройка \> аналитика Интернета вещей \> Управление сценарием**.
2. На плитке для сценария выберите **Настройка**.
3. Выберите **Далее**, чтобы перейти к последней странице мастера.
4. Установите этот параметр, чтобы выключить сценарий.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]