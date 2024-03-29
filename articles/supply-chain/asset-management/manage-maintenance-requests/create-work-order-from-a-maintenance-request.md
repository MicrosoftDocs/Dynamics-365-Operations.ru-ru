---
title: Создание заказов на работу из запросов на обслуживание
description: В этой статье объясняется, как создавать заказы на работу из запросов на обслуживание в управлении активами.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bb54ec3466086afbd87a023a40e346a6a3464c98
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017184"
---
# <a name="create-work-orders-from-maintenance-requests"></a>Создание заказов на работу из запросов на обслуживание

[!include [banner](../../includes/banner.md)]

 


После создания запросов на техническое обслуживание можно легко преобразовать их в заказы на работу. Эта статья описывает самый быстрый способ работы с запросами на техническое обслуживание, обновления нескольких запросов на техническое обслуживание одновременно, а затем создания заказа на работу для нескольких запросов на техническое обслуживание одновременно. На странице **Активные запросы на обслуживание** или **Запросы на обслуживания для моего функционального местоположения** можно также работать с одним запросом на техническое обслуживание за раз и конвертировать один запрос на техническое обслуживание в заказ на работу.

> [!NOTE]
> Каждый запрос на техническое обслуживание может быть связан только с одним заказом на работу. Однако несколько запросов на техническое обслуживание могут быть включены в один заказ на работу, даже если запросы на техническое обслуживание имеют разные активы.

1. Выберите **Управление активами** \> **Запросы на обслуживание** \> **Все запросы на обслуживание**.
2. Прежде чем создать заказ на работу из запросов на техническое обслуживание, необходимо выбрать, как минимум, тип работы по техническому обслуживанию для запросов на обслуживание, а также вариант типа работы по техническому обслуживанию и торговлю, если эта информация актуальна. В представлении сетки можно легко обновить информацию для запроса на техническое обслуживание.
3. Когда вы будете готовы к созданию заказа на работу, выберите запросы на техническое обслуживание, чтобы включить в него.

    - При выборе нескольких запросов на обслуживание для преобразования в заказ на работу необходимо установить поле **Актив** и поле **Тип задания на обслуживание** перед созданием заказа на работу.
    - При выборе одного запроса на техническое обслуживание для преобразования в заказ на работу необходимо установить только поле **Актив**, прежде чем создавать заказ на работу. Однако при создании заказа на работу можно выбрать тип задания на обслуживание (и связанный с этим вариант типа задания на обслуживание и торговлю, если эта информация актуальна) в диалоговом окне **Создание заказа на работу**.

4. Выберите **Заказ на работу**.
5. В диалоговом окне **Создание заказа на работу** установите поля, затем выберите **OK**.

    Панель сообщений может уведомить вас о создании нового заказа на работу.

    Кроме того, при создании заказа на работу, основанного на запросе на техническое обслуживание, если актив, связанный с запросом на техническое обслуживание, включен в гарантийное соглашение, панель сообщений уведомляет вас о гарантийном соглашении.

6. Выберите **Управление активами** \> **Заказы на работу** \> **Все заказы на работу** и откройте новый заказ на работу.

    ![Открыть новый заказ на работу.](media/05-manage-maintenance-requests.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]