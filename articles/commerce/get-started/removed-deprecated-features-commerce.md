---
title: Удаленные или устаревшие функции Dynamics 365 Commerce
description: В этом разделе описываются возможности, который удалены или которые планируется удалить из Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: c47c5430a8f5d67e13c95db609a95d5ad66933ae
ms.sourcegitcommit: a8b6cd799eddaf5be9aec9ea3c2b55e2c3231652
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2020
ms.locfileid: "3335284"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Удаленные или устаревшие функции Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

В этом разделе описываются возможности, который удалены или которые планируется удалить из Dynamics 365 Commerce.

- *Удаленная* функция больше недоступна в продукте.
- *Устаревшая* функция не находится в активной разработке и может быть удалена в следующем обновлении.

Этот список поможет вам учитывать эти удаления и устаревания при своем собственном планировании. 

> [!NOTE]
> Подробные сведения об объектах в приложениях Finance and Operations можно найти в документе [Технический справочник по отчетам](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Можно сравнить различные версии этих отчетов, чтобы получить сведения об объектах, которые были изменены или были исключены в каждой версии приложений Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Функции, удаленные или устаревшие в выпуске Commerce 10.0.10
### <a name="pos-operation-803---picking-and-receiving"></a>Операций POS 803 — Комплектация и получение
|   |  |
|------------|--------------------|
| **Причина устаревания/удаления** | Операции комплектации и получения устарели в связи с новой архитектурой операций. |
| **Заменена другой функцией?**   | Да. Она заменяется двумя новыми операциями POS: Входящая операция (804) и исходящая операция (805).|
| **Затрагиваемые области продукта**         | Приложение POS |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устарело: с выпуска 10.0.10 операции комплектации и получения больше не будут получать новые обновления. В будущих выпусках для этих операций будут только исправляться критические ошибки. Всем клиентам рекомендуется перейти на новые [входящие операции](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) и [исходящие операции](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), которые еще долго будут поддерживаться в продукте. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Функции, удаленные или устаревшие в выпуске Commerce 10.0.7
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>API Commerce GetProductAvailabilities и GetAvailableInventoryNearby
|   |  |
|------------|--------------------|
| **Причина устаревания/удаления** | Новые оптимизированные API созданы для замены API GetProductAvailabilities и GetAvailableInventoryNearby. |
| **Заменена другой функцией?**   | Да: он заменен API GetEstimatedAvailabilty и GetEstimatedProductWarehouseAvailability. |
| **Затрагиваемые области продукта**         | SDK приложения электронной коммерции |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устарел: с выпуска 10.0.7 GetProductAvailabilities и GetAvailableInventoryNearby больше не будут развиваться. Организации, использующие эти API в развертываниях электронной коммерции, должны преобразовать их в новые API GetEstimatedAvailabilty и GetEstimatedProductWarehouseAvailability и включить [оптимизированную функцию расчета наличия продукта](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Предыдущие объявления об удаленных или устаревших функциях
Для получения дополнительных сведений о функциях, которые были удалены или устарели в предыдущих выпусках, см [Удаленные или устаревшие функции в предыдущих выпусках](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).
