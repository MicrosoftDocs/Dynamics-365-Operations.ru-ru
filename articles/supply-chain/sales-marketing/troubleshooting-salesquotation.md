---
title: Устранение неполадок предложений по продажам
description: В этом разделе описывается устранение проблем, которые могут встретиться при работе с предложениями по продаже.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 09529ba729170be7281e2ae04008d3ba4a58e060
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824758"
---
# <a name="troubleshoot-sales-quotations"></a>Устранение неполадок предложений по продажам

В этом разделе описывается устранение проблем, которые могут встретиться при работе с предложениями по продаже.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>Невозможно изменить количество продаж по предложению по продажам для номенклатуры обслуживания.

### <a name="issue-description"></a>Описание проблемы

При попытке задать количество для продажи (поле **SalesQty**) для номенклатуры типа *Сервис* в строке предложения по продажам будет выведено следующее сообщение: "Обновление не разрешено для поля количества".

### <a name="issue-resolution"></a>Устранение проблемы

Невозможно задать количество для продажи для продуктов, которые являются номенклатурами обслуживания. Например, если вы предлагаете услугу по установке номенклатуры, нет смысла записывать количество, поскольку отсутствует физическая номенклатура. Имеется только услуга.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]