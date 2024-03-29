---
title: Потребности в номенклатуре для заказа на сервисное обслуживание
description: В этой статье описывается потребность в номенклатуре для заказа на сервисное обслуживание.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 376cda6bbe1800611e6f24c347b9035469a30a14
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015182"
---
# <a name="service-order-item-requirements"></a>Потребности в номенклатуре для заказа на сервисное обслуживание

[!include [banner](../includes/banner.md)]

Можно создать заказ на сервисное обслуживание, чтобы отслеживать и управлять услугами, которые предоставляются вашим клиентам. Если необходимо зарезервировать определенные номенклатуры для Заказа на сервисное обслуживание, можно создать потребность в складской номенклатуре для него. Потребность в номенклатуре можно сразу потребить из запасов или она может запустить производственный заказ для номенклатуры.

Используя потребность в номенклатуре вместо проводки с номенклатурой, можно запланировать поставку перед самым моментом использования данной номенклатуры, создать заказ на покупку, включить номенклатуру в схему коммерческих соглашений, и использовать потребность в номенклатуре при планировании производства.

Потребности в номенклатуре для заказов на обслуживание обрабатываются с помощью проекта. Для создания потребности в номенклатуре в заказе на сервисное обслуживание заказ на обслуживание необходимо присоединить к проекту.

Как только создается потребность в номенклатуре для заказа на сервисное обслуживание, ее можно просмотреть в разделе **Проект** как отдельный заказ на сервисное обслуживание или через форму **Заказ на продажу**.

## <a name="view-an-item-requirement-from-a-service-order"></a>Просмотр потребности в номенклатуре из заказа на обслуживание

1. Перейдите к пункту **Управление сервисным обслуживанием** \> **Заказы на обслуживание** \> **Заказы на обслуживание**.
1. Выберите **Подготовить к отправке** и затем выберите **Потребность в номенклатуре**, чтобы открыть форму **Потребности в номенклатуре**.
1. Выберите вкладку **Проект** и проверьте поле **Заказ на продажу**, чтобы просмотреть заказы на сервисное обслуживание потребности в номенклатуре.

## <a name="delete-service-orders-with-item-requirements"></a>Удаление заказов на обслуживание с потребностями в номенклатуре

Если для заказа на обслуживание создана потребность в номенклатуре, удалить заказ на обслуживание невозможно. Для удаления заказа на обслуживание необходимо предварительно удалить потребность в номенклатуре.

1. Перейдите к пункту **Управление сервисным обслуживанием** \> **Заказы на обслуживание** \> **Заказы на обслуживание**.
1. Выберите **Подготовить к отправке** и затем выберите **Потребность в номенклатуре**, чтобы открыть форму **Потребности в номенклатуре**. В этой форме перечислены потребности в номенклатуре, созданные по этому заказу на обслуживание.
1. Выберите потребность в номенклатуре для удаления, а затем выберите **Удалить**.

–или–

1. Перейдите в раздел **Управление и учет по проектам** \> **Проекты** \> **Все проекты**.
1. Откройте проект с заказом на сервисное обслуживание, в котором создается потребность в номенклатуре.
1. В форме **Проекты** в правой области выберите **Потребности в номенклатуре**. В форме **Потребности в номенклатуре** будут перечислены все потребности в номенклатуре, связанные с выбранным проектом.
1. Выберите потребность в номенклатуре для удаления, а затем выберите **Удалить**.

## <a name="see-also"></a>См. также

[Потребности в номенклатуре (форма)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))



[!INCLUDE[footer-include](../../includes/footer-banner.md)]