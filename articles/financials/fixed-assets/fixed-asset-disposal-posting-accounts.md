---
title: "Счета разноски удаления ОС"
description: "В этом разделе описывается, как настроить счета разноски ГК для выбытия основных средств."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bfed7657649f938c3d436468891d40d4194b555d
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="4a24b-103">Счета разноски удаления ОС</span><span class="sxs-lookup"><span data-stu-id="4a24b-103">Fixed asset disposal posting accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4a24b-104">В этом разделе описывается, как настроить счета разноски ГК для выбытия основных средств.</span><span class="sxs-lookup"><span data-stu-id="4a24b-104">This topic explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="4a24b-105">На странице профилей оприходования основных фондов на экспресс-вкладке "Счета ГК" выберите "Выбытие - продажа" и "Выбытие - демонтаж", чтобы настроить разноски в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="4a24b-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="4a24b-106">Для обоих типов проводок счет ГК кредитуется для значения выбытия основного средства.</span><span class="sxs-lookup"><span data-stu-id="4a24b-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="4a24b-107">Дебет разносится на корреспондентский счет, который может быть, например, банковским счетом.</span><span class="sxs-lookup"><span data-stu-id="4a24b-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="4a24b-108">Если основное средство продается клиенту, используется счет клиента вместо корреспондентского счета.</span><span class="sxs-lookup"><span data-stu-id="4a24b-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="4a24b-109">Щелкните "Выбытие", затем щелкните "Продажа" или "Отходы", затем настройте подробные счета, чтобы реверсировать остаточную стоимость основного средства.</span><span class="sxs-lookup"><span data-stu-id="4a24b-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="4a24b-110">Вы можете также ввести информацию в поля "Сумма к разноске" и "Тип суммы реализации" на странице "Параметры выбытия".</span><span class="sxs-lookup"><span data-stu-id="4a24b-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="4a24b-111">Проводка по выбытию средства в пуле низкой стоимости уменьшает остаточную стоимость пула низкой стоимости только на выбывшее количество.</span><span class="sxs-lookup"><span data-stu-id="4a24b-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="4a24b-112">В любом случае, если продажа основного средства превышает остаточную стоимость малоценных средств, остаточная стоимость будет приравнена к нулю.</span><span class="sxs-lookup"><span data-stu-id="4a24b-112">However, when the sale of an asset exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>






