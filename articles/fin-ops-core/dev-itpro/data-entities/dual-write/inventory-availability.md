---
title: Доступность запасов в двойной записи
description: В этой теме приводятся сведения о порядке проверки доступности запасов в случае двойной записи.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: a7bfe998d2d787203a507a831c171fc43b03fedc
ms.sourcegitcommit: cc9921295f26804259cc9ec5137788ec9f2a4c6f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "4839557"
---
# <a name="inventory-availability-in-dual-write"></a>Доступность запасов в двойной записи

[!include [banner](../../includes/banner.md)]

Используя доступность запасов, можно проверять запасы перед добавлением продукта на страницу **Предложения**, **Заказы** или **Накладные** в Microsoft Dynamics 365 Sales. Например, вы проверяете запасы и определяете дату выполнения как одну из ключевых задач в процессе [продажи перспективному клиенту](dual-write-prospect-to-cash.md).

Если запасов не хватает, можно оценить дату поставки на основе прогнозируемых приходов и расходов на складе. Можно также проверить информацию о доступных для заказа продуктов (ATP), в которой можно найти количество ATP по заранее определенной временной границе.

## <a name="on-hand-inventory"></a>Запасы в наличии

В Dynamics 365 Sales добавлена новая кнопка **Запасы в наличии** в заголовке страниц **Предложения**, **Заказы** и **Накладные**. При выборе этой кнопки появляется диалоговое окно, в котором можно указать компанию и продукт, для которого необходимо проверить запасы в наличии. В этом диалоговом окне отображаются те же сведения, что и в [Запасы в наличии](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

В диалоговом окне возвращаются сведения о запасах из Dynamics 365 Supply Chain Management. Эта информация содержит следующие количества:

- Количество в наличии
- Зарезервированное количество в наличии
- Доступное количество в наличии
- Заказанное количество
- Количество в заказе
- Зарезервированное заказанное количество
- Общее доступное количество

## <a name="atp-information"></a>Информация о "доступно для резервирования"

В Sales новая кнопка **Информация ATP** была добавлена в позиции строки на страницах **Предложения**, **Заказы** и **Накладные**. При выборе этой кнопки появляется диалоговое окно, в котором можно указать компанию, продукт, сайт запасов, склад запасов и количество заказа. В этом диалоговом окне используются те же настройки, что и описанные в разделе [Резервирование по заказам](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

Диалоговое окно возвращает сведения о доступности для резервирования из модуля Supply Chain Management. Эта информация содержит следующие количества:

- Количество "доступно для резервирования"
- Количество прихода
- Количество расходов
- Количество в наличии

## <a name="how-it-works"></a>Как это работает

При выборе кнопки **Запасы в наличии** на странице **Предложения с расценками**, **Заказы** или **Накладные** выполняется вызов двойной записи в режиме реального времени в интерфейс API **Запасы в наличии**. Интерфейс API рассчитывает запасы в наличии для данного продукта. Результат сохраняется в таблицах **InventCDSInventoryOnHandRequestEntity** и **InventCDSInventoryOnHandEntryEntity**, а затем записывается в Dataverse двойной записью. Для использования этих функциональных возможностей необходимо выполнить следующие две карты двойной записи. Пропустите начальную синхронизацию при выполнении карт.

- Записи запасов в наличии CDS (msdyn_inventoryonhandentries)
- Запросы запасов в наличии CDS (msdyn_inventoryonhandrequests)

## <a name="templates"></a>Шаблоны
Для доступа к данным запасов в наличии доступны следующие шаблоны.

Приложения Finance and Operations | Приложение для взаимодействия с клиентами | описание 
---|---|---
[Записи CDS запасов в наличии](#145) | msdyn_inventoryonhandentries |
[Запросы CDS запасов в наличии](#147) | msdyn_inventoryonhandrequests |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a>Записи запасов в наличии CDS (msdyn_inventoryonhandentries)

Этот шаблон синхронизирует данные между приложениями Finance and Operations и Dataverse.

Поле Finance and Operations | Тип сопоставления | Поле взаимодействия с клиентами | Значение по умолчанию
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a>Запросы запасов в наличии CDS (msdyn_inventoryonhandrequests)

Этот шаблон синхронизирует данные между приложениями Finance and Operations и Dataverse.

Поле Finance and Operations | Тип сопоставления | Поле взаимодействия с клиентами | Значение по умолчанию
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]