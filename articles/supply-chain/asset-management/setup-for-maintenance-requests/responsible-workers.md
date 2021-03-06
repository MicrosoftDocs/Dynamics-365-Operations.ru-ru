---
title: Ответственные специалисты по обслуживанию
description: В этом разделе описан порядок настройки ответственных специалистов по обслуживанию в «Управлении активами».
author: johanhoffmann
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkerResponsible
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1330aa04a57809ff34dcca9791f8fb0a93c8d71
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808456"
---
# <a name="responsible-maintenance-workers"></a>Ответственные специалисты по обслуживанию

[!include [banner](../../includes/banner.md)]

 

Ответственные специалисты по обслуживанию могут быть связаны с типами активов, активами, функциональными местоположениями, категориями типов заданий обслуживания, типами заданий обслуживания, вариантами типов заданий обслуживания и сделками. Они могут быть использованы в заказах на работу и запросах на обслуживание, чтобы указать предпочтение в отношении специалиста по обслуживанию, который должен нести ответственность за заказ на работу. (Однако эти специалисты по обслуживанию не обязательно являются теми же работниками, которые должны выполнять заказ на работу). Использование этой функциональности является необязательным. Например, она может использоваться для выбора ответственных работников или групп работников для конкретных типов работ или рабочих областей.

Во время жизненного цикла заказа на работу или жизненного цикла запроса на обслуживание ответственные специалисты по обслуживанию могут быть изменены или обновлены. Это изменение или обновление может быть связано, например, с изменением состояния жизненного цикла запроса на обслуживание или состоянием жизненного цикла заказа на работу.

Настройка на странице **Ответственные специалисты по обслуживанию** *не* используется при планировании заказа на работу.

> [!NOTE]
> В «Управлении активами» можно также настроить *предпочтительных* специалистов по обслуживанию, которые могут быть выделены для заказов на работу во время планирования заказа на работу.

Прежде чем вы сможете настроить ответственных специалистов по обслуживанию, необходимо настроить специалистов и группы специалистов по обслуживанию, которые должны быть доступны для выбора. Для получения информации о том, как настроить специалистов и группы специалистов по обслуживанию, см. в разделе [Специалисты и группы специалистов по обслуживанию](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-responsible-maintenance-workers"></a>Настройка ответственных специалистов по обслуживанию

1. Выберите **Управление активами** \> **Настройка** \> **Работники** \> **Ответственные специалисты по обслуживанию**.
2. Выберите **Создать**, чтобы создать запись.
3. Сначала создайте ответственного специалиста по обслуживанию по умолчанию или настройку группы ответственных специалистов по обслуживанию, где вы задаете только поле **Группа ответственных специалистов по обслуживанию** и/или поле **Ответственный специалист по обслуживанию**. Оставьте оставшиеся поля пустыми. Эта настройка по умолчанию будет использоваться при планировании заказа на работу, если никакая другая, более конкретная комбинация не соответствует содержимому заказа на работу.

    > [!NOTE]
    > При создании запроса на обслуживание, когда ответственный специалист по обслуживанию или группа ответственных специалистов по обслуживанию доступны для выбора на странице **Все запросы на обслуживание**, «Управление активами» проходит через все записи ответственных специалистов по обслуживанию для проверки на возможное совпадение. Она всегда проверяет наиболее конкретные комбинации в первую очередь. Другими словами, «Управление активами» сначала проверяет соответствие для поля **Торговля**. Если совпадение не найдено, оно проверяет соответствие для поля **Вариант типа задания обслуживания**. Если совпадение не найдено, оно проверяет соответствие для поля **Тип задания обслуживания** и т.д. Как вы можете видеть в макете страницы, это поведение означает, что, чтобы найти наиболее конкретную комбинацию, «Управление активами» проверяет каждую запись справа налево на совпадение (сначала **Торговля**, затем **Вариант типа задания обслуживания**, затем **Тип задания обслуживания**, затем **Категория типа задания обслуживания**, затем **Функциональное местоположение**, затем **Актив**, и наконец **Тип актива**). Если совпадение не найдено, используется запись по умолчанию, которая не имеет выбора в этих семи полях.

На следующем рисунке показан пример страницы **Ответственные специалисты по обслуживанию**.

![Страница ответственных специалистов по обслуживанию](media/08-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]