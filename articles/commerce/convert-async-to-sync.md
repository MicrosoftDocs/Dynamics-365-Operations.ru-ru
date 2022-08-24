---
title: Преобразование асинхронных клиентов в синхронных клиентов
description: В этой статье объясняется, как преобразовывать асинхронные клиенты в синхронных клиентов в Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: b442bfc0685706359771e4d9e2729565d3652a60
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278201"
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
