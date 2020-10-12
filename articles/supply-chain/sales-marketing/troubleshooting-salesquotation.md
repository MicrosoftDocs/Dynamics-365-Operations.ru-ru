---
title: Устранение неполадок предложений по продажам
description: В этом разделе описывается устранение проблем, которые могут встретиться при работе с предложениями по продаже.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 67610a833be132399b2d47ae8c6b27119be9ce95
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834415"
---
# <a name="troubleshoot-sales-quotations"></a>Устранение неполадок предложений по продажам

В этом разделе описывается устранение проблем, которые могут встретиться при работе с предложениями по продаже.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>Невозможно изменить количество продаж по предложению по продажам для номенклатуры обслуживания.

### <a name="issue-description"></a>Описание проблемы

При попытке задать количество для продажи (поле **SalesQty**) для номенклатуры типа *Сервис* в строке предложения по продажам будет выведено следующее сообщение: "Обновление не разрешено для поля количества".

### <a name="issue-resolution"></a>Устранение проблемы

Невозможно задать количество для продажи для продуктов, которые являются номенклатурами обслуживания. Например, если вы предлагаете услугу по установке номенклатуры, нет смысла записывать количество, поскольку отсутствует физическая номенклатура. Имеется только услуга.

