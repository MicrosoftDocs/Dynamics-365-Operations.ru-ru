---
title: Форматы схем для сообщений центра Интернета вещей
description: В этом разделе описывается разработка схемы сообщений, которую можно использовать в аналитике Интернета вещей.
author: robinarh
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ecf4a70d69d24ea75f5448339057e7017cb93af
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/19/2021
ms.locfileid: "7652072"
---
# <a name="schema-formats-for-iot-hub-messages"></a>Форматы схем для сообщений центра Интернета вещей

[!include [banner](../../includes/banner.md)]

В этом разделе описывается разработка схемы сообщений, которую можно использовать в аналитике Интернета вещей.

## <a name="message-requirements"></a>Требования к сообщениям

Ниже перечислены правила, которые применяются для мониторинга сообщений в аналитике Интернета вещей:

+ Схемы сообщений должны быть в формате нотации объектов JavaScript (JSON).
+ Свойство UNIX **timestamp**, значение которого выражается в миллисекундах (мс), должно присутствовать в сообщении центра Интернета вещей Microsoft Azure.
+ Сообщение отслеживается только в том случае, если оно содержит все свойства, определенные в настройке сценария. Например, если задать свойства **id**, **timestamp** и **value**, отслеживается следующее сообщение.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    }
    ```

    Это сообщение не отслеживается, поскольку отсутствует свойство **value**.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
    }
    ```

+ Аналитика Интернета вещей игнорирует свойства в сообщении, которые не были определены в конфигурации сценария. Например, если задать свойства **id**, **timestamp** и **value**, аналитика Интернета вещей отслеживает следующие сообщения.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
        "machine" : "Machine1225",
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
         "activity": "PartOut"
    },
    ```

+ Аналитика Интернета вещей автоматически игнорирует сообщения, которые не соответствуют критериям конфигурации сценария.
+ Можно определять и использовать несколько типов схем сообщений.
+ Должна быть определена не каждый тип схем сообщений. Должны быть определены только схемы, которые будут использоваться для сценариев аналитики Интернета вещей.

## <a name="id-value-pair-schema"></a>Схема пар код-значение

Пара код-значение является общим шаблоном для схем сообщений аналитики Интернета вещей. Используя пару код-значение, можно гарантировать, что схема сообщений одинакова для всех сценариев. Например, это сообщение для сценария **Простой оборудования** или **Задержки производства**.

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

Ниже приводится сообщение для сценария **Качество продукта**.

```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

Оба предыдущих сообщения содержат свойства **id** и **value**. Значения **id** могут быть сопоставлены в таблице **Значения данных сигнала** во время настройки сценария. Для сценария **Простой оборудования** будет сопоставлено значение **IoTInt.Machine1225.PartOut**. Для сценария **Качество продукта** будет сопоставлено значение **IoTInt.Machine1225.Temperature**.

Дополнительные сведения см. в [документации по центру Интернета вещей Azure](/azure/iot-hub/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]