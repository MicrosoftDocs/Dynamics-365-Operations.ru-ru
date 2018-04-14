---
title: "Обновление использования одного ваучера и переоценки в валюте"
description: "Некоторые организации вводят журналы, содержащие один ваучер, который имеет несколько клиентов или поставщиков, при этом они также выполняют процесс переоценки расчетов с клиентами или расчетов с поставщиками в иностранной валюте. В этом разделе описаны шаги, которые такие организации должны выполнить при обновлении до Microsoft Dynamics 365 for Operations версии 1611."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 84b295440db6cad74d919eb7bbdd41651b9825e9
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a><span data-ttu-id="c65dd-104">Обновление использования одного ваучера и переоценки в валюте</span><span class="sxs-lookup"><span data-stu-id="c65dd-104">Single voucher and currency revaluation upgrade</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="c65dd-105">Некоторые организации вводят журналы, содержащие один ваучер, который имеет несколько клиентов или поставщиков, при этом они также выполняют процесс переоценки расчетов с клиентами или расчетов с поставщиками в иностранной валюте.</span><span class="sxs-lookup"><span data-stu-id="c65dd-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="c65dd-106">В этом разделе описаны шаги, которые такие организации должны выполнить при обновлении до Microsoft Dynamics 365 for Operations версии 1611.</span><span class="sxs-lookup"><span data-stu-id="c65dd-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="c65dd-107">Выполните эти шаги при обновлении до Microsoft Dynamics 365 for Operations версии 1611.</span><span class="sxs-lookup"><span data-stu-id="c65dd-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="c65dd-108">Перед обновлением до Dynamics 365 for Operations выполните процессы переоценки в иностранной валюте для расчетов с клиентами и расчетов с поставщиками.</span><span class="sxs-lookup"><span data-stu-id="c65dd-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="c65dd-109">В поле **Метод** установите значение **Дата накладной**.</span><span class="sxs-lookup"><span data-stu-id="c65dd-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="c65dd-110">Создается проводка переоценки, которая реверсирует последнюю переоценки в иностранной валюте.</span><span class="sxs-lookup"><span data-stu-id="c65dd-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="c65dd-111">Таким образом открытые проводки оцениваются в их исходной валюте учета.</span><span class="sxs-lookup"><span data-stu-id="c65dd-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="c65dd-112">Выполните обновление до Dynamics 365 for Operations версии 1611.</span><span class="sxs-lookup"><span data-stu-id="c65dd-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="c65dd-113">Снова выполните процессы переоценки в иностранной валюте для расчетов с поставщиками и расчетов с клиентами.</span><span class="sxs-lookup"><span data-stu-id="c65dd-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="c65dd-114">На этот раз задайте в поле **Метод** значение **Стандартный**.</span><span class="sxs-lookup"><span data-stu-id="c65dd-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="c65dd-115">Создается новая проводка переоценки на основании текущих валютных курсов.</span><span class="sxs-lookup"><span data-stu-id="c65dd-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="c65dd-116">Эта проводка записывает нереализованные прибыли и убытки на правильный итоговый счет ГК.</span><span class="sxs-lookup"><span data-stu-id="c65dd-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>





