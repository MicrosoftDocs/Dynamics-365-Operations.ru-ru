---
title: Включить поиск заказов для гостевых оформлений
description: В этом разделе описывается, как включить поиск заказов для гостевых оформлений в Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 639ee670b83198423425d03dad308306c9eed25c
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674984"
---
# <a name="enable-order-lookup-for-guest-checkouts"></a>Включить поиск заказов для гостевых оформлений

[!include [banner](includes/banner.md)]

В этом разделе описывается, как включить поиск заказов для гостевых оформлений в Microsoft Dynamics 365 Commerce.

Функция поиска заказа для гостевых оформлений позволяет клиентам, которые делают покупки как гости, выполнять поиск по их заказам. Возможность поиска по заказам полезна, когда клиенты хотят выполнять такие действия, как проверка статуса выполнения продуктов в заказе, проверка адреса, по которому был отгружен заказ, изменение порядка поставки продукта или подтверждение магазина, из которого клиент заберет заказ.

Клиенты, которые размещают заказы как зарегистрированные пользователи, могут просматривать сведения о заказах, когда они вошли в систему, но клиенты, использующие гостевое оформление для размещения заказов, не могут. Однако когда функция поиска заказа для гостевых оформлений включена, она предоставляет форму, которую клиенты могут использовать для поиска заказов, которые они разместили как гости. В этой форме клиенты вводят код подтверждения заказа и (необязательно) адрес электронной почты, указанный при оформлении.

Кроме того, ссылка или кнопка, посылаемые клиенту непосредственно на страницу сведений о заказах, можно включить в любые транзакционные письма, связанные с заказами. Эта ссылка или кнопка будут работать для заказов, размещенных зарегистрированными пользователями и гостями.

## <a name="turn-on-necessary-features-in-commerce-headquarters"></a>Включите необходимые функции в модуле Commerce headquarters

Чтобы включить поиск заказов для гостевых оформлений, необходимо включить следующие функции в **Рабочие области \> Управление функциями** в Commerce Headquarters.

| Функция | Целевые назначения |
|---------|---------|
| Функция выбора сведений о порядке поиска анонимных пользователей Retail | Эта функция предоставляет интерфейс пользователя в параметрах Commerce, который позволяет включить API поиска заказов для пользователей, не прошедших проверку подлинности, и настроить отображение личных данных. |
| Включить создание более надежного кода ссылки на канал | Эта функция создает более защищенный 12-символьный код ссылки на канал (код подтверждения заказа), который может быть передан в строку запроса при поиске заказа. |
| Создать последовательный формат идентификаторов ссылок на каналы для всех каналов | Эта функция создает код ссылки на защищенный канал для заказов, размещенных на сайте электронной коммерции, розничном POS-терминале или в центре обработки вызовов. Прежде чем можно будет включить эту функцию, необходимо включить функцию **Включить создание более надежного кода ссылки на канал**. |

После включения функции **Функция выбора сведений о заказе для поиска анонимных пользователей Retail**, необходимо включить функцию API, которая поддерживает поиск заказов без проверки подлинности в Commerce Headquarters. Перейдите в раздел **Retail и Commerce \> Настройка центрального офиса \> Параметры \> Клиентские заказы**. На странице **Клиентские заказы** на экспресс-вкладке **Поиск заказов** установите для параметра **включить поиск заказов без проверки подлинности** значение **Да**, как показано на следующем рисунке.

## <a name="manage-the-display-of-personal-data"></a>Управление представлением личных данных

Экспресс-вкладка **Поиск заказов** на странице **Клиентские заказы** в Commerce headquarters включает в себя поле **включить личные данные в заказе гостя**, позволяющее управлять отображением личных сведений клиентам. Эти личные данные включают адрес доставки клиента и последние четыре цифры номера кредитной карты клиента. По умолчанию личные данные не отображаются для клиентов, когда включен поиск заказов без проверки подлинности. В следующей таблице описаны доступные параметры.

| Параметр | Результат |
|--------|--------|
| Никогда | Значение по умолчанию. Никакие личные данные не отображаются при поиске заказов. Когда зарегистрированные пользователи, вошедшие в систему, ищут заказ, который они создали во время входа в систему, они смогут просмотреть их личные данные. |
| Только гостевые заказы | Личные данные отображаются в поиске заказов для заказов, созданных клиентами в качестве гостей. Если заказ был создан зарегистрированным пользователем, он должен войти в систему, чтобы просмотреть личные данные. |
| Все заказы | Личные данные отображаются при любом поиске заказов. |

> [!NOTE]
> Эти параметры определяют, когда личные данные, такие как адрес клиента и последние четыре цифры номера кредитной карты клиента, отображаются анонимным гостям. Для обеспечения конфиденциальности зарегистрированных клиентов рекомендуется выбрать параметр **только заказы на гостя**. Однако наиболее безопасным вариантом является **никогда**.

После изменения значения поля **включить личные данные в заказе гостя** необходимо выполнить задание 1070 (**Настройка канала**) в Commerce headquarters, перейдя к **Retail и Commerce \> ИТ Retail и Commerce \> График распределения**.

## <a name="configure-the-order-lookup-module"></a>Настройка модуля поиска заказов

Модуль поиска заказов в библиотеке модуля Commerce используется для преобразования для просмотра формы, которую гости используют для поиска заказов. Модуль поиска заказов может быть включен в ячейку основного текста любой страницы, для которой не требуется вход клиента. Сведения о настройке модуля см. в разделе [модуль поиска заказов](order-lookup-module.md).

## <a name="additional-resources"></a>Дополнительные ресурсы

[модуль поиска заказов](order-lookup-module.md)

[Настройка профиля уведомлений по электронной почте](email-notification-profiles.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]