---
title: В номенклатуре не может быть спецификаций или формул
description: При попытке утвердить заказ в ходе проверки номенклатуры выводится сообщение об ошибке. Это указывает, что номенклатура не может иметь спецификацию или формулу.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294164"
---
# <a name="item-cant-have-a-bom-or-formula"></a><span data-ttu-id="217e2-104">В номенклатуре не может быть спецификаций или формул</span><span class="sxs-lookup"><span data-stu-id="217e2-104">Item can't have a BOM or formula</span></span>

<span data-ttu-id="217e2-105">Код ошибки: PRO2614</span><span class="sxs-lookup"><span data-stu-id="217e2-105">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="217e2-106">Симптомы</span><span class="sxs-lookup"><span data-stu-id="217e2-106">Symptoms</span></span>

<span data-ttu-id="217e2-107">При попытке утвердить заказ в ходе проверки номенклатуры выводится следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="217e2-107">When you try to firm an order, you receive the following error message during item validation:</span></span>

> <span data-ttu-id="217e2-108">Номенклатура не может иметь спецификацию или формулу</span><span class="sxs-lookup"><span data-stu-id="217e2-108">Item cannot have a BOM or formula</span></span>

## <a name="resolution"></a><span data-ttu-id="217e2-109">Решение</span><span class="sxs-lookup"><span data-stu-id="217e2-109">Resolution</span></span>

<span data-ttu-id="217e2-110">Номенклатуры, имеющие спецификацию или формулу, должны быть типа *Номенклатура планирования*, *Спецификация* или *Формула*.</span><span class="sxs-lookup"><span data-stu-id="217e2-110">Items that have a bill of materials (BOM) or formula must be of the *Planning item*, *BOM*, or *formula* type.</span></span> <span data-ttu-id="217e2-111">Чтобы изменить тип номенклатуры, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="217e2-111">To change the type of an item, follow these steps.</span></span>

1. <span data-ttu-id="217e2-112">Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="217e2-112">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="217e2-113">Откройте соответствующий продукт.</span><span class="sxs-lookup"><span data-stu-id="217e2-113">Open the relevant product.</span></span>
1. <span data-ttu-id="217e2-114">На экспресс-вкладке **Инженер** задайте поле **Тип производства** как *Планирование номенклатуры*, *Спецификация* или *Формула*.</span><span class="sxs-lookup"><span data-stu-id="217e2-114">On the **Engineer** FastTab, set the **Production type** field to *Planning item*, *BOM*, or *formula*.</span></span>
