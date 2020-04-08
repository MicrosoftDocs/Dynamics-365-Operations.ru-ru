---
title: Доступ к финансовым и налоговым ссылочным данным
description: В этом разделе приводятся сведения о доступе к финансовым и налоговым справочным данным.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 50f906d62ad6f1e0b79c9c1bb6fcd373ba350c98
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172606"
---
# <a name="access-to-finance-and-tax-reference-data"></a><span data-ttu-id="eae46-103">Доступ к финансовым и налоговым ссылочным данным</span><span class="sxs-lookup"><span data-stu-id="eae46-103">Access to finance and tax reference data</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="eae46-104">Каждое предприятие работает с базовым набором финансовых данных, таких как год финансового календаря, валюта, в которой работает компания, счета, на которые поступают и с которых снимаются денежные средства для работы компании, налоговые ставки и переводы.</span><span class="sxs-lookup"><span data-stu-id="eae46-104">Every business works with a basic set of financial data, such as the fiscal calendar year, the currency that business is transacted in, the accounts that the money to run the business comes in to or goes out of, tax rates, and remittance.</span></span> <span data-ttu-id="eae46-105">Эти данные хранятся в приложениях Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="eae46-105">This data resides in Finance and Operations apps.</span></span> <span data-ttu-id="eae46-106">Однако они доступны для Common Data Service, чтобы приложения на основе модели в Microsoft Dynamics 365 могли иметь единый источник для финансовых и налоговых данных.</span><span class="sxs-lookup"><span data-stu-id="eae46-106">However, it's exposed to Common Data Service so that model-driven apps in Microsoft Dynamics 365 can have a single source for finance and tax data.</span></span> <span data-ttu-id="eae46-107">Таким образом, данные являются едиными для всей экосистемы бизнеса.</span><span class="sxs-lookup"><span data-stu-id="eae46-107">In this way, data is uniform across the business ecosystem.</span></span> 

<span data-ttu-id="eae46-108">Финансовые и налоговые данные интегрируются с использованием следующих сопоставлений:</span><span class="sxs-lookup"><span data-stu-id="eae46-108">Finance and tax data is integrated by using the following mappings:</span></span>

+ [<span data-ttu-id="eae46-109">Интегрированная книга учета</span><span class="sxs-lookup"><span data-stu-id="eae46-109">Integrated ledger</span></span>](ledger-mapping.md)
+ [<span data-ttu-id="eae46-110">Интегрированный налоговый справочник</span><span class="sxs-lookup"><span data-stu-id="eae46-110">Integrated tax master</span></span>](tax-mapping.md)
