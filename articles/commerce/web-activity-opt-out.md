---
title: Отказ от сбора событий веб-активности
description: В этом разделе объясняется, как можно разрешить посетителям вашего сайта отказаться от сбора событий веб-активности в Microsoft Dynamics 365 Commerce.
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2c396060017db6d7ce830b350f242d3097876e50
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012321"
---
# <a name="opt-out-of-web-activity-event-collection"></a>Отказ от сбора событий веб-активности
[!include [banner](includes/banner.md)]

В этом разделе объясняется, как предоставить клиентам возможность отказаться от сбора событий веб-активности в Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Обзор

Dynamics 365 Commerce позволяет администраторам сайтов анализировать веб-активность пользователей их сайтов электронной коммерции. Таким образом, они могут лучше понять, как используются их сайты, и они могут оптимизировать сайты для обеспечения улучшенного взаимодействия с пользователями и выполнения бизнес-задач.


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>Способы для администраторов реализовать функции отказа

У администраторов есть три способа реализации функции отказа.

### <a name="opt-out-on-behalf-of-users"></a>Отказ от имени пользователей

В управлении учетными записями в центральном офисе Commerce (HQ), администраторы могут выполнить отказ от имени пользователей.

1. В клиенте HQ на странице **все клиенты** выполните поиск и выберите клиента.
1. На странице сведения о клиенте на экспресс-вкладке **Retail** в разделе **Безопасность** установите для параметра **не отслеживать веб-активность** значение **Да**.

    ![Параметры конфиденциальности](media/Disablepersonalizationpart2.png)

1. Выберите **Сохранить** и закройте страницу.

### <a name="module-based-opt-out-experience"></a>Функция отказа на основе модуля

Администраторы могут позволить прошедшим аутентификацию пользователям отказаться от сбора событий веб-активности самостоятельно. Чтобы обеспечить такой отказ, добавьте на страницы профиля учетной записи клиента модуль отказа для пользователя.

### <a name="custom-extensions"></a>Настраиваемые расширения

Администраторы могут создавать свои собственные расширения для управления отказами пользователей. Дополнительные сведения см. в разделе [API вызова Retail Server](e-commerce-extensibility/call-retail-server-apis.md) и [Расширяемость канала продаж через Интернет](e-commerce-extensibility/overview.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]