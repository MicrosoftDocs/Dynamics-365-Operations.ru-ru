---
title: Параметры Sensor Data Intelligence
description: В этой статье приводятся сведения о параметрах конфигурации, доступных на странице Параметры аналитики данных датчиков.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreServiceParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 5240537e3a6526ceb35253b9e68f46b1753c6a37
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689382"
---
# <a name="sensor-data-intelligence-parameters"></a>Параметры Sensor Data Intelligence

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Страница **Параметры аналитики данных датчиков** содержит несколько параметров, которые можно использовать для настройки функции. Эти параметры включают в себя параметры подключения к Azure и параметр времени жизни сообщений с оповещениями, отправляемых пользователям в соответствии с измерениями датчика.

## <a name="read-and-change-connection-details-for-your-azure-iot-solution"></a>Чтение и изменение сведений о подключении для вашего решения Azure IoT

Обычно решение Azure IoT настраивается и подключается к Microsoft Dynamics 365 Supply Chain Management на странице **Развертывание и подключение ресурсов Azure**, которая поможет вам выполнить обе процедуры. (Дополнительные сведения см. в разделе [Развертывание решения Интернета вещей в Azure](sdi-deploy-iot-solution-on-azure.md).) Можно также просмотреть и изменить сведения о подключении в любое время Supply Chain Management, выполнив следующие действия.

1. Перейдите в раздел **Администрирование системы \> Настройка \> Аналитика данных датчиков \> Параметры аналитики данных датчиков**.
1. На вкладке **Временной ряд** в поле **Строка подключения хранилища метрик Redis** введите значение **Основной строки подключения (StackExchange.Redis)** для решения Azure IoT, к которому необходимо подключиться. Дополнительные сведения о поиске этого значения см. в разделе [Развертывание решения Интернета вещей в Azure](sdi-deploy-iot-solution-on-azure.md).
1. На вкладке **Интеграция** в поле **Идентификатор клиента приложения Azure AD** введите значение **Идентификатора клиента** для решения Azure IoT, к которому требуется подключиться. Дополнительные сведения о поиске этого значения см. в разделе [Развертывание решения Интернета вещей в Azure](sdi-deploy-iot-solution-on-azure.md).

## <a name="set-the-lifetime-of-alert-messages"></a>Установка времени жизни сообщений с оповещениями

Каждый раз, когда Аналитика данных датчиков обнаруживает ситуацию, требующую внимания пользователя, она отправляет уведомление соответствующему пользователю. Чтобы предотвратить накопление этих уведомлений в системе, следует настроить их срок действия на несколько дней.

1. Перейдите в раздел **Администрирование системы \> Настройка \> Аналитика данных датчиков \> Параметры аналитики данных датчиков**.
1. На вкладке **Уведомления** в поле **Число дней действия уведомления** введите количество дней, в течение которых будет храниться уведомление. По истечении указанного времени уведомление будет удалено.