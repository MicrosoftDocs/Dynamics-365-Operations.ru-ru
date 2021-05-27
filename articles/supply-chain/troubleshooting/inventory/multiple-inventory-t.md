---
title: Несколько складских проводок для номеров партий, если отключено физическое обновление
description: Несколько складских проводок создаются после корректировки строки заказа на покупку для номенклатур, для которых параметр "при физическом обновлении" группы номеров партий имеет значение "нет".
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026861"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a><span data-ttu-id="d7988-103">Несколько складских проводок для номеров партий, если отключено физическое обновление</span><span class="sxs-lookup"><span data-stu-id="d7988-103">Multiple inventory transactions for batch numbers when On physical update is disabled</span></span>

<span data-ttu-id="d7988-104">Номер статьи базы знаний: 4613390</span><span class="sxs-lookup"><span data-stu-id="d7988-104">KB number: 4613390</span></span>

## <a name="symptoms"></a><span data-ttu-id="d7988-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="d7988-105">Symptoms</span></span>

<span data-ttu-id="d7988-106">Несколько складских проводок создаются после корректировки строки заказа на покупку для номенклатур, для которых параметр **При физическом обновлении** группы номеров партий имеет значение *Нет*.</span><span class="sxs-lookup"><span data-stu-id="d7988-106">Multiple inventory transactions are created after you adjust a purchase order line for items where the **On physical update** option of the batch number group is set to *No*.</span></span>

<span data-ttu-id="d7988-107">При создании номенклатуры, если параметр **При физическом обновлении** группы номеров партий имеет значение *Нет*, система автоматически создает новый номер партии при изменении количества в строке покупки и сохранении страницы заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="d7988-107">When you create an item where the **On physical update** option of the batch number group is set to *No*, the system automatically creates a new batch number if you modify a purchase line quantity and save the purchase order page.</span></span>

## <a name="resolution"></a><span data-ttu-id="d7988-108">Приказ</span><span class="sxs-lookup"><span data-stu-id="d7988-108">Resolution</span></span>

<span data-ttu-id="d7988-109">Параметр **При физическом обновлении** для групп номеров партий выполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d7988-109">The **On physical update** setting for batch number groups works in the following way:</span></span>

- <span data-ttu-id="d7988-110">Если для параметра установлено значение *Да*, новые номера партий создаются только после физического обновления (например, когда номенклатуры отгружаются или получаются).</span><span class="sxs-lookup"><span data-stu-id="d7988-110">When the option is set to *Yes*, new batch numbers are created only after a physical update (for example, when items are shipped or received).</span></span>
- <span data-ttu-id="d7988-111">Если для параметра установлено значение *Нет*, новый номер партии создается каждый раз при выполнении соответствующего обновления (например, при добавлении нового количества к заказу на покупку).</span><span class="sxs-lookup"><span data-stu-id="d7988-111">When the option is set to *No*, a new batch number is created every time that an applicable update occurs (for example, when a new quantity is added to a purchase order).</span></span>
