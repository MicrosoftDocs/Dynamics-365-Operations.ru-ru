---
title: Преобразование асинхронных клиентов в синхронных клиентов
description: В этой статье объясняется, как преобразовывать асинхронные клиенты в синхронных клиентов в Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 0ce4906816deab8824b1079a34489e55651c0e03
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884399"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>Преобразование асинхронных клиентов в синхронных клиентов

[!include [banner](includes/banner.md)]

В этой статье объясняется, как преобразовывать асинхронные клиенты в синхронных клиентов в Microsoft Dynamics 365 Commerce.

Чтобы преобразовывать асинхронные клиенты в синхронных клиентов, выполните следующие действия.

1. В Commerce Headquarters выполните **P-задание**, чтобы отправить асинхронные клиенты в Commerce Headquarters.
1. Запустите задание **Синхронизация клиентов и деловых партнеров из асинхронного режима**, чтобы создать коды счетов клиентов. (Это задание ранее называлось **Синхронизация клиентов и деловых партнеров из асинхронного режима**.)
1. Выполните задание **1010**, чтобы синхронизировать коды счета нового клиента с каналами.

Если заказ ссылается на асинхронного клиента или адрес, который еще не был синхронизирован с Commerce Headquarters, клиент или адрес будут синхронизированы как часть пакетного задания **Синхронизация заказов**. Если кассовая проводка ссылается на асинхронного клиента или адрес, синхронизация клиента или адреса производится до разноски на конец дня (EOD).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Управление клиентами в магазинах](customer-mgmt-stores.md)

[Асинхронный режим создания клиента](async-customer-mode.md)

[Атрибуты заказчика](dev-itpro/customer-attributes.md)

[Исключение автономных данных](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
