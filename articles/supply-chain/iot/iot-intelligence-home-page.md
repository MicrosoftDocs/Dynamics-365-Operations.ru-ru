---
title: Домашняя страница бизнес-аналитики Интернета вещей
description: В этой теме содержатся ссылки на сведения о бизнес-аналитике Интернета вещей.
author: robinarh
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: intro-internal
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f32cb5578f3c15a10f863980491a687f64312cd
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/19/2021
ms.locfileid: "7652071"
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

+ **Задержки производства** — этот сценарий сравнивает фактическое время цикла с плановым временем цикла. Supply Chain Management уведомляет вас, когда производство не было по плану, чтобы можно было повысить эффективность работы и избежать задержек заказов.
+ **Простой оборудования** — этот сценарий сравнивает измеренное время доступности с параметрами, заданными пользователем. Supply Chain Management уведомляет вас при превышении порога простоя, чтобы можно было выполнить такие действия, как перепланирование производственного заказа на работу или создание заказа на работу для обслуживания.
+ **Качество продукта** — этот сценарий сравнивает показания датчика, такие как влажность и температура, с определенной пользователем метрикой качества. Supply Chain Management уведомляет пользователя при возникновении отклонения, чтобы можно было обрабатывать стандарты качества и минимизировать отходы.

На следующем рисунке показано взаимодействие центра Интернета вещей Azure, бизнес-аналитики Интернета вещей и Supply Chain Management.

![Центр Интернета вещей, бизнес-аналитика Интернета вещей и Supply Chain Management.](media/iot_intelligence.png)

## <a name="setup"></a>Настройка

Можно настроить бизнес-аналитику Интернета вещей без написания какого-либо кода. Имеются основные шаги.

1. [Настройка ресурсов Azure](iot-azure-setup.md) — создание центра Интернета вещей, кэша Redis и хранилища ключей, к которым можно получить доступ из Supply Chain Management.
2. [Форматы схем сообщений для центра Интернета вещей](iot-schema-format.md) — настройка устройств на отправку сообщений в центр Интернета вещей и определение формата сообщений нотации объектов JavaScript (JSON).
3. В управлении функциями установите флажок бизнес-аналитики Интернета вещей. 
4. [Установите надстройку бизнес-аналитики Интернета вещей в Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) — установите надстройку в LCS и настройте секреты Azure.
5. [Настройка метрик](iot-metrics-setup.md) — настройте метрики в Supply Chain Management.
6. [Настройка сценария](iot-scenario-setup.md) — настройте сценарии в Supply Chain Management.

## <a name="tracking-and-maintenance"></a>Отслеживание и обслуживание

+ [Мониторинг сценариев в Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
+ [Отключение сценария](iot-scenario-setup.md#disable-a-scenario)
+ [Удаление надстройки](iot-lcs-setup.md#uninstall-addin)
+ [Изменение запущенного сценария аналитики Интернета вещей](iot-management.md#modify-a-running-iot-intelligence-scenario)
+ [Параметры моделирования](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]