---
title: Невозможно обновить прогнозируемые затраты на единицу измерения при импорте записей прогноза спроса
description: При использовании сущностей данных для импорта записей прогноза спроса себестоимость для существующих записей не обновляется, чтобы они соответствовали импортируемым данным.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026851"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a><span data-ttu-id="5f43e-103">Невозможно обновить прогнозируемые затраты на единицу измерения при импорте записей прогноза спроса</span><span class="sxs-lookup"><span data-stu-id="5f43e-103">You can't update the forecasted unit cost when you import demand forecast records</span></span>

<span data-ttu-id="5f43e-104">Номер статьи базы знаний: 4614109</span><span class="sxs-lookup"><span data-stu-id="5f43e-104">KB number: 4614109</span></span>

## <a name="symptoms"></a><span data-ttu-id="5f43e-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="5f43e-105">Symptoms</span></span>

<span data-ttu-id="5f43e-106">При использовании сущностей данных для импорта записей прогноза спроса значение **Прогнозируемые затраты на единицу измерения** для существующих записей не обновляется, чтобы они соответствовали импортируемым данным.</span><span class="sxs-lookup"><span data-stu-id="5f43e-106">When you use data entities to import demand forecast records, the **Forecasted unit cost** value for existing records isn't updated so that it matches the imported data.</span></span>

## <a name="cause"></a><span data-ttu-id="5f43e-107">Причина</span><span class="sxs-lookup"><span data-stu-id="5f43e-107">Cause</span></span>

<span data-ttu-id="5f43e-108">**Прогнозируемые затраты на единицу измерения** является полем только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5f43e-108">**Forecasted unit cost** is a read-only field.</span></span> <span data-ttu-id="5f43e-109">Значение основано на затраты на единицу измерения продукта и не может быть задано непосредственно при импорте.</span><span class="sxs-lookup"><span data-stu-id="5f43e-109">The value is based on the product unit cost and can't be set directly through import.</span></span>

## <a name="resolution"></a><span data-ttu-id="5f43e-110">Приказ</span><span class="sxs-lookup"><span data-stu-id="5f43e-110">Resolution</span></span>

<span data-ttu-id="5f43e-111">Так как поле доступно только для чтения, для него нельзя импортировать значения.</span><span class="sxs-lookup"><span data-stu-id="5f43e-111">Because the field is read only, you can't import values for it.</span></span> <span data-ttu-id="5f43e-112">Значение будет вычисляться в соответствии с существующей бизнес-логикой.</span><span class="sxs-lookup"><span data-stu-id="5f43e-112">The value will be calculated according to the existing business logic.</span></span>
