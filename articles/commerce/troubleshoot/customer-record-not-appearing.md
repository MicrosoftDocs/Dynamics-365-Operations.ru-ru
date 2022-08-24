---
title: Записи клиентов не отображаются в Commerce headquarters
description: В этой статье содержатся указания по устранению неполадок, которые могут помочь, когда записи о клиентах не появляются сразу в Commerce Headquarters.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: f1ad1f45abbc95cbf6d41b3c8681db781c6c9d23
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268847"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a>Записи клиентов не отображаются в Commerce headquarters

[!include [banner](../../includes/banner.md)]

В этой статье содержатся указания по устранению неполадок, которые могут помочь, когда записи о клиентах не появляются сразу в Commerce Headquarters.

## <a name="description"></a>описание

При создании новой записи клиента с помощью потока регистрации в витрине электронной коммерции соответствующая запись клиента сразу же отображается в Commerce Headquarters.

## <a name="resolution"></a>Приказ

### <a name="disable-customer-creation-in-async-mode"></a>Отключение создания клиентов в асинхронном режиме

> [!IMPORTANT]
> Если вы отключите создание асинхронного клиента, это может повлиять на производительность системы, поскольку создание каждой записи приведет к созданию запроса в реальном времени для Commerce Headquarters. Кроме того, если Commerce headquarters не работает (например, во время потоков обслуживания), все новые потоки создания клиентов создадут ошибки.

Чтобы отключить создание клиентов в асинхронном режиме в Commerce headquarters, выполните следующие действия.

1. Перейдите в раздел **Retail и Commerce \> Настройка канала \> Настройка интернет-магазина \> Профили функциональности**.
1. Если вы еще не используете профиль функциональности для своего интернет-канала, создайте его.
1. Убедитесь, что для параметра **Создание клиента в асинхронном режиме** выбрано значение **нет**.
1. Перейдите в раздел **Retail и Commerce \> Каналы \> Интернет-магазины**.
1. Выберите интернет-магазин, для которого требуется отключить создание асинхронного клиента.
1. На вкладке **Общие** убедитесь, что в поле **Профиль функциональности** установлен профиль функциональности, используемый для интернет-канала.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка клиента B2C в Commerce](../set-up-b2c-tenant.md)
