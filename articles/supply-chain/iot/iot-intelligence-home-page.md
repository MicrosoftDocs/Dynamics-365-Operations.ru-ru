---
title: Домашняя страница бизнес-аналитики Интернета вещей
description: В этой теме содержатся ссылки на сведения о бизнес-аналитике Интернета вещей.
author: johanhoffmann
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2386d71fde8196304fde846cbff4cd45d1edc834
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674431"
---
# <a name="iot-intelligence-home-page"></a>Домашняя страница бизнес-аналитики Интернета вещей

[!include [banner](../../includes/banner.md)]

> [!IMPORTANT]
> Эта функция сейчас доступна только для следующих стран/регионов:
>
> - US (Соединенные Штаты Америки)
> - EU (Европейский союз)
> - AU (Австралия)
> - CA (Канада)
> - UK (Соединенное Королевство)

Бизнес-аналитика Интернета вещей — надстройка для Microsoft Dynamics 365 Supply Chain Management. Он интегрирует сигналы Интернета вещей (IoT) с данными в Supply Chain Management для создания практической аналитики.

Бизнес-аналитика Интернета вещей поддерживает следующие сценарии:

- **Задержки производства** — этот сценарий сравнивает фактическое время цикла с плановым временем цикла. Supply Chain Management уведомляет вас, когда производство не было по плану, чтобы можно было повысить эффективность работы и избежать задержек заказов.
- **Простой оборудования** — этот сценарий сравнивает измеренное время доступности с параметрами, заданными пользователем. Supply Chain Management уведомляет вас при превышении порога простоя, чтобы можно было выполнить такие действия, как перепланирование производственного заказа на работу или создание заказа на работу для обслуживания.
- **Качество продукта** — этот сценарий сравнивает показания датчика, такие как влажность и температура, с определенной пользователем метрикой качества. Supply Chain Management уведомляет пользователя при возникновении отклонения, чтобы можно было обрабатывать стандарты качества и минимизировать отходы.

На следующем рисунке показано взаимодействие центра Интернета вещей Azure, бизнес-аналитики Интернета вещей и Supply Chain Management.

![Центр Интернета вещей, бизнес-аналитика Интернета вещей и Supply Chain Management.](media/iot_intelligence.png)

<!-- KFM: hide setup info for now

## Setup

You can set up and configure IoT Intelligence without writing any code. Here are the basic steps.

1. [Set up Azure resources](iot-azure-setup.md) – Create an IoT hub, a Redis cache, and a key vault that can be accessed from Supply Chain Management.
2. [Message schema formats for IoT Hub](iot-schema-format.md) – Configure your devices to send messages to IoT Hub, and define the JavaScript Object Notation (JSON) message format.
3. In Feature Management, enable the IoT Intelligence feature flag. 
4. [Install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Install the add-in in LCS, and configure the Azure secrets.
5. [Set up metrics](iot-metrics-setup.md) – Set up metrics in Supply Chain Management.
6. [Scenario setup](iot-scenario-setup.md) – Set up the scenarios in Supply Chain Management.

-->

## <a name="tracking-and-maintenance"></a>Отслеживание и обслуживание

- [Мониторинг сценариев в Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
- [Отключение сценария](iot-scenario-setup.md#disable-a-scenario)
- [Изменение запущенного сценария аналитики Интернета вещей](iot-management.md#modify-a-running-iot-intelligence-scenario)
- [Параметры моделирования](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]