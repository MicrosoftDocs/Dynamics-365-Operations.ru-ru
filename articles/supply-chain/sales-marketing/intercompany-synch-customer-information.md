---
title: Синхронизация сведений о внутрихолдинговых клиентах
description: В этой статье описывается синхронизация сведений о клиентах для внутрихолдинговых заказов
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: a3a67c9bcf93f88375d2d4d78d87175200626d50
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897526"
---
# <a name="synchronize-intercompany-customer-information"></a>Синхронизация сведений о внутрихолдинговых клиентах

[!include [banner](../../includes/banner.md)]

Информация по клиенту синхронизируется, если поле **Сведения о клиенте** активируется, когда создается заказ на продажу, или при внесении изменений в данные клиента, код поставщика или номер заявки клиента.

Можно в любой момент изменить значение в этих полях синхронизации. Однако определить, требуется ли копировать это значение в другие внутрихолдинговые заказы, можно только путем выбора этого параметра. Если активировано поле **Сведения о клиенте** во внутрихолдинговом заказе на продажу, изменение в этом заказе синхронизируется с внутрихолдинговым заказом на покупку. Если также активировано поле **Сведения о клиенте** во внутрихолдинговом заказе на покупку, этот заказ также синхронизируется с исходным заказом на продажу.

> [!NOTE]
> Если активировано поле **Сведения о клиенте** как во внутрихолдинговом заказе на продажу, так и во внутрихолдинговом заказе на покупку, обновления, сделанные одним лицом в одной компании, отменяются обновлениями, сделанными другим лицом в другой компании в том же самом заказе.

Рекомендуется активировать поле **Сведения о клиенте** во внутрихолдинговом заказе на покупку. Это включает синхронизацию между исходным заказом на продажу и внутрихолдинговым заказом на покупку и синхронизацию из внутрихолдингового заказа на покупку во внутрихолдинговый заказ на продажу.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
