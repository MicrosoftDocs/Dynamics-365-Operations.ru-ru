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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9a9cc821d2fe9accad1dae210271682cdd2ce4ba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232214"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="96301-103">Устранение неполадок предложений по продажам</span><span class="sxs-lookup"><span data-stu-id="96301-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="96301-104">В этом разделе описывается устранение проблем, которые могут встретиться при работе с предложениями по продаже.</span><span class="sxs-lookup"><span data-stu-id="96301-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="96301-105">Невозможно изменить количество продаж по предложению по продажам для номенклатуры обслуживания.</span><span class="sxs-lookup"><span data-stu-id="96301-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="96301-106">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="96301-106">Issue description</span></span>

<span data-ttu-id="96301-107">При попытке задать количество для продажи (поле **SalesQty**) для номенклатуры типа *Сервис* в строке предложения по продажам будет выведено следующее сообщение: "Обновление не разрешено для поля количества".</span><span class="sxs-lookup"><span data-stu-id="96301-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="96301-108">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="96301-108">Issue resolution</span></span>

<span data-ttu-id="96301-109">Невозможно задать количество для продажи для продуктов, которые являются номенклатурами обслуживания.</span><span class="sxs-lookup"><span data-stu-id="96301-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="96301-110">Например, если вы предлагаете услугу по установке номенклатуры, нет смысла записывать количество, поскольку отсутствует физическая номенклатура.</span><span class="sxs-lookup"><span data-stu-id="96301-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="96301-111">Имеется только услуга.</span><span class="sxs-lookup"><span data-stu-id="96301-111">There is only a service.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]