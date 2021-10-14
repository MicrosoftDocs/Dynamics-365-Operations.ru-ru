---
title: Внутрихолдинговая конвертация валют
description: В этой теме описывается преобразование валют для внутрихолдинговых проводок
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 540849003d532ef2f0905c18332d9cb82a04cf7c
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548502"
---
# <a name="intercompany-currency-conversions"></a>Внутрихолдинговая конвертация валют

[!include [banner](../../includes/banner.md)]

Когда коды валют на исходном заказе на продажу и внутрихолдинговом заказе на покупку различаются, производится конвертация следующих полей, если включена синхронизация:

- **Цена за ед. изм.**
- **Накладные расходы на продажи** или **Накладные расходы по покупкам**
- **Скидка**
- **Многострочная скидка**

Эти поля затем синхронизируются со строкой внутрихолдингового заказа на продажу.

Однако, поскольку валюта внутрихолдингового заказа на покупку и валюта внутрихолдингового заказа на продажу всегда синхронизируются, синхронизация следующих полей выполняется без преобразования валют:

- **Цена за ед. изм.**
- **Накладные расходы на продажи** или **Накладные расходы по покупкам**
- **Скидка**
- **Процент скидки**
- **Многострочная скидка**
- **Многострочная скидка в процентах**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
