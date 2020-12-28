---
title: Накладные расходы управления транспортировкой
description: В этой теме объясняется, как накладные расходы, формируемые транспортировкой, должны быть связаны с кодом накладных расходов.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2b703d770c7f9ea684716368cf1e7dbe5fec8710
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/29/2020
ms.locfileid: "4436508"
---
# <a name="transportation-management-miscellaneous-charges"></a><span data-ttu-id="22961-103">Накладные расходы управления транспортировкой</span><span class="sxs-lookup"><span data-stu-id="22961-103">Transportation management miscellaneous charges</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22961-104">Как и с любыми накладными расходами, накладные расходы, формируемые транспортировкой, должны быть связаны с кодом накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="22961-104">As with all miscellaneous charges, transportation-generated charges must be associated with a charge code.</span></span> <span data-ttu-id="22961-105">В противном случае они не будут добавляться обратно в заказ в качестве накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="22961-105">Otherwise, they won't be added back to the order as a miscellaneous charge.</span></span> <span data-ttu-id="22961-106">**Код накладных расходов** определяет порядок учета накладных расходов по отношению к заказу и строке заказа, в которую они добавляются.</span><span class="sxs-lookup"><span data-stu-id="22961-106">The **Charges code** determines how the charge is accounted for in relation to the order and order line where it is added.</span></span>

<span data-ttu-id="22961-107">Перейдите в раздел **Управление транспортировкой > Настройка > Расчет ставок > Накладные расходы**, чтобы определить критерии квалификации, определяющие, когда определенный **Код накладных расходов** применяется к накладным расходам.</span><span class="sxs-lookup"><span data-stu-id="22961-107">Go to **Transportation management > Setup > Rating > Miscellaneous charges** to define the qualifying criteria that determine when a specific **Charges code** is applied to a charge.</span></span>

<span data-ttu-id="22961-108">Для каждого соответствующего параметра **Модуль накладных расходов** (*Клиент* и *Поставщик*) должна быть по крайней мере одна настройка, где для параметра **Тип накладных расходов** задано значение *Нет*.</span><span class="sxs-lookup"><span data-stu-id="22961-108">You should have at least one setup for each relevant **Charges module** setting (*Customer* and *Vendor*) where the **Miscellaneous charge type** is set to *None*.</span></span> <span data-ttu-id="22961-109">Если она отсутствует, накладные расходы *не будут* добавлены в заказ.</span><span class="sxs-lookup"><span data-stu-id="22961-109">If this is missing, the miscellaneous charge will *not* be added to the order.</span></span>
