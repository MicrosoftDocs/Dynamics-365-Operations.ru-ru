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
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="f5793-103">Устранение неполадок предложений по продажам</span><span class="sxs-lookup"><span data-stu-id="f5793-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="f5793-104">В этом разделе описывается устранение проблем, которые могут встретиться при работе с предложениями по продаже.</span><span class="sxs-lookup"><span data-stu-id="f5793-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="f5793-105">Невозможно изменить количество продаж по предложению по продажам для номенклатуры обслуживания.</span><span class="sxs-lookup"><span data-stu-id="f5793-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f5793-106">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="f5793-106">Issue description</span></span>

<span data-ttu-id="f5793-107">При попытке задать количество для продажи (поле **SalesQty**) для номенклатуры типа *Сервис* в строке предложения по продажам будет выведено следующее сообщение: "Обновление не разрешено для поля количества".</span><span class="sxs-lookup"><span data-stu-id="f5793-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f5793-108">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="f5793-108">Issue resolution</span></span>

<span data-ttu-id="f5793-109">Невозможно задать количество для продажи для продуктов, которые являются номенклатурами обслуживания.</span><span class="sxs-lookup"><span data-stu-id="f5793-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="f5793-110">Например, если вы предлагаете услугу по установке номенклатуры, нет смысла записывать количество, поскольку отсутствует физическая номенклатура.</span><span class="sxs-lookup"><span data-stu-id="f5793-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="f5793-111">Имеется только услуга.</span><span class="sxs-lookup"><span data-stu-id="f5793-111">There is only a service.</span></span>

