---
title: Записи клиентов не отображаются в Commerce headquarters
description: В этой статье содержатся указания по устранению неполадок, которые могут помочь, когда записи о клиентах не появляются сразу в Commerce Headquarters.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5cdc96c9829be4d34e9346b2c99d300c2349bc41
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876553"
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
