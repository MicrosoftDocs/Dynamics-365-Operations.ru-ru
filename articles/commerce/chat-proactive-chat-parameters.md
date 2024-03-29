---
title: Параметры упреждающего чата модуля чата Commerce
description: В этой статье описываются параметры упреждающего чата модулей чата Commerce в Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: f3cff89a25ff84414e7fdd32cbb26404c2080187
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691077"
---
# <a name="commerce-chat-module-proactive-chat-parameters"></a>Параметры упреждающего чата модуля чата Commerce

[!include [banner](includes/banner.md)]

В этой статье описываются параметры упреждающего чата в чате Commerce с многоканальным взаимодействием для Customer Service чатом Commerce с модулями чата Power Virtual Agents в Microsoft Dynamics 365 Commerce.

## <a name="proactive-chat-properties"></a>Свойства упреждающего чата

Свойства упреждающего чата находятся в области свойств в чате Commerce с модулями многоканального взаимодействия для Customer Service и чата Commerce с Power Virtual Agents в конструкторе сайтов Commerce.

> [!NOTE]
> По умолчанию все перечисленные здесь свойства упреждающего чата являются пустыми. Рекомендуется получить дополнительные сведения об этих свойствах и настраивать их только по мере необходимости. Этот подход позволяет сократить число ошибочно запускаемых упреждающих чатов.

### <a name="proactive-chat"></a>Упреждающий чат

| Понятное имя | Описание | Значение по умолчанию |
|---------------|-------------|---------------|
| Включено | Активно привлекать клиентов на основе других триггеров. | Отключено |
| Приветствие в чате | Сообщение приветствия, которое используется при запуске упреждающего чата. | Пустой |

### <a name="wait-time-proactive-chat"></a>Время ожидания (упреждающий чат)

| Понятное имя | Описание |
|---------------|-------------|
| Время ожидания (с) | Время (в секундах), затрачиваемое пользователями сайта на страницу сайта перед запуском упреждающего чата. |
| Приветствие в чате | Сообщение приветствия, которое используется при запуске упреждающего чата. |

### <a name="number-of-page-visits-proactive-chat"></a>Число посещений страниц (упреждающий чат)

| Понятное имя | Описание |
|---------------|-------------|
| Число посещений страниц | Число посещений страниц до запуска упреждающего чата. Пользователи сайта должны сначала принять приглашение в баннере подтверждения файлов cookie. |
| Приветствие в чате | Сообщение приветствия, которое используется при запуске упреждающего чата. |

### <a name="specific-pages-proactive-chat"></a>Отдельные страницы (упреждающий чат)

| Понятное имя | Описание |
|---------------|-------------|
| Страницы | Список страниц, которые будут запускать упреждающий чат после их посещения. |
| Приветствие в чате | Сообщение приветствия, которое используется при запуске упреждающего чата. |

### <a name="from-specific-pages-proactive-chat"></a>С конкретных страниц (упреждающий чат)

| Понятное имя | Описание |
|---------------|-------------|
| Страницы | Список страниц, которые будут запускать упреждающий чат, когда пользователи уходят с них. |
| Приветствие в чате | Сообщение приветствия, которое используется при запуске упреждающего чата. |

### <a name="specific-countryregion-proactive-chat"></a>Конкретная страна или регион (упреждающий чат)

| Понятное имя | Описание |
|---------------|-------------|
| Код страны | Пользователи, посещение которых осуществляется из указанных стран или регионов, запускают упреждающий чат. Коды стран/регионов должны состоять из двух прописных букв (например, **US**). |
| Приветствие в чате | Сообщение приветствия, которое используется при запуске упреждающего чата. |

### <a name="date-range-proactive-chat"></a>Диапазон дат (упреждающий чат)

| Понятное имя | Описание |
|---------------|-------------|
| Дата начала (дд/мм/гггг) | Дата, на которую или после которой будет запущен упреждающий чат. |
| Дата окончания (дд/мм/гггг) | Дата, на которую или перед которой будет запущен упреждающий чат. |
| Приветствие в чате | Сообщение приветствия, которое используется при запуске упреждающего чата. |

### <a name="total-amount-in-cart-proactive-chat"></a>Общая сумма в корзине (упреждающий чат)

| Понятное имя | Описание |
|---------------|-------------|
| Минимум | Минимальная денежная сумма (включительно) в корзине, которая будет запускать упреждающий чат при посещении пользователем страницы корзины. |
| Максимум | Максимальная денежная сумма (включительно) в корзине, которая будет запускать упреждающий чат при посещении пользователем страницы корзины. |
|Приветствие в чате | Сообщение приветствия, которое используется при запуске упреждающего чата. |

### <a name="total-number-of-items-in-cart-proactive-chat"></a>Общее количество номенклатур в корзине (упреждающий чат)

| Понятное имя | Описание |
|---------------|-------------|
| Минимум | Минимальное количество номенклатур (включительно) в корзине, при котором будет запускаться упреждающий чат при посещении пользователем страницы корзины. |
| Максимум | Максимальное количество номенклатур (включительно) в корзине, при котором будет запускаться упреждающий чат при посещении пользователем страницы корзины. |
| Приветствие в чате | Сообщение приветствия, которое используется при запуске упреждающего чата. |

### <a name="specific-products-in-cart-proactive-chat"></a>Отдельные продукты в корзине (упреждающий чат)

| Понятное имя | Описание |
|---------------|-------------|
| Коды продуктов/SKU | Список кодов продуктов/единиц складского учета (SKU), которые будут вызывать упреждающий чат при посещении пользователем страницы корзины. |
| Приветствие в чате | Сообщение приветствия, которое используется при запуске упреждающего чата. |

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор функций чата Commerce](commerce-chat-overview.md)

[Модуль чата Commerce с многоканальным взаимодействием для Customer Service](commerce-chat-module.md)

[Модуль чата Commerce с Power Virtual Agents](chat-module-pva.md)
