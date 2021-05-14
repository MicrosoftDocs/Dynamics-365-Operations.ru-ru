---
title: Неправильное значение поля в TaxTrans
description: В этой теме содержатся сведения об устранении недопустимых значений полей в TaxTrans.
author: bijian
manager: beya
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 97f9bb24d32180f2fccb69c5a13e2aa0349c1ee4
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947696"
---
# <a name="incorrect-field-value-in-taxtrans"></a><span data-ttu-id="79b21-103">Неправильное значение поля в TaxTrans</span><span class="sxs-lookup"><span data-stu-id="79b21-103">Incorrect field value in TaxTrans</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79b21-104">Если значение поля в **TaxTrans** неверное, воспользуйтесь сведениями из этого раздела, чтобы попытаться решить проблему.</span><span class="sxs-lookup"><span data-stu-id="79b21-104">If a field value in **TaxTrans** is incorrect, use the information in this topic to try to resolve the issue.</span></span>

## <a name="overview-of-values"></a><span data-ttu-id="79b21-105">Обзор значений</span><span class="sxs-lookup"><span data-stu-id="79b21-105">Overview of values</span></span>
<span data-ttu-id="79b21-106">В следующем списке показано, как **TaxTrans**, **TaxUncommitted** и **TmpTaxWorkTrans** являются похожими наборами данных, но работают по-разному.</span><span class="sxs-lookup"><span data-stu-id="79b21-106">The following list shows how **TaxTrans**, **TaxUncommitted**, and **TmpTaxWorkTrans** are similar data sets, but in work differently.</span></span>

  - <span data-ttu-id="79b21-107">**TaxTrans** является окончательным результатом разнесенных проводок налога, которые сохранены в базе данных.</span><span class="sxs-lookup"><span data-stu-id="79b21-107">**TaxTrans** is the final posted tax transaction result persisted in the database.</span></span>
  - <span data-ttu-id="79b21-108">**TaxUncommitted** — это промежуточный рассчитанный налоговый результат, сохраненный в базе данных (если применимо), который будет использоваться в дальнейшем при разноске.</span><span class="sxs-lookup"><span data-stu-id="79b21-108">**TaxUncommitted** is the intermediate calculated tax result persisted in the database (if applicable), which will be used later in posting.</span></span>
  - <span data-ttu-id="79b21-109">**TmpTaxWorkTrans** — это временный вычисленный результат в таблице в памяти (тип таблицы = InMemory).</span><span class="sxs-lookup"><span data-stu-id="79b21-109">**TmpTaxWorkTrans** is the temporary calculated tax result in the in-memory table (Table Type = InMemory).</span></span>

<span data-ttu-id="79b21-110">Если вы обнаружили основную причину неправильного столбца **TaxTrans**, вы также обнаружили основную причину неправильного столбца **TaxUncommitted** или **TmpTaxWorkTrans**.</span><span class="sxs-lookup"><span data-stu-id="79b21-110">If you find the root cause of an incorrect **TaxTrans** column, you've also found the root cause of an incorrect **TaxUncommitted** or **TmpTaxWorkTrans** column.</span></span> <span data-ttu-id="79b21-111">Это объясняется тем, что три столбца копируются друг с другом.</span><span class="sxs-lookup"><span data-stu-id="79b21-111">This is because the three columns are copied from each other.</span></span>

<span data-ttu-id="79b21-112">Обычно в процессе расчета налога создается **TmpTaxWorkTrans**, а затем создается, если применимо, **TaxUncommitted**.</span><span class="sxs-lookup"><span data-stu-id="79b21-112">Typically, during tax calculation, **TmpTaxWorkTrans** is generated, and then, if applicable, **TaxUncommitted** is generated.</span></span> <span data-ttu-id="79b21-113">При разноске налога создается **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="79b21-113">During tax posting, **TaxTrans** is generated.</span></span>


## <a name="add-breakpoints"></a><span data-ttu-id="79b21-114">Добавление точек останова</span><span class="sxs-lookup"><span data-stu-id="79b21-114">Add breakpoints</span></span>
<span data-ttu-id="79b21-115">Выполните следующие шаги, чтобы добавить точки останова:</span><span class="sxs-lookup"><span data-stu-id="79b21-115">To add breakpoints, complete the following steps:</span></span> 

1. <span data-ttu-id="79b21-116">Добавьте расширения и точки останова в *insert()* и *update()* в расширениях, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="79b21-116">Add extensions and breakpoints in *insert()* and *update()* in the extensions as shown below.</span></span>

     - <span data-ttu-id="79b21-117">**TaxTrans**</span><span class="sxs-lookup"><span data-stu-id="79b21-117">**TaxTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="79b21-118">**TaxUncommitted**</span><span class="sxs-lookup"><span data-stu-id="79b21-118">**TaxUncommitted**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="79b21-119">**TmpTaxWorkTrans**</span><span class="sxs-lookup"><span data-stu-id="79b21-119">**TmpTaxWorkTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. <span data-ttu-id="79b21-120">Иди же можно добавлять точки останова непосредственно, когда **TaxUncommitted** не включен.</span><span class="sxs-lookup"><span data-stu-id="79b21-120">Alternatively, you can add breakpoints directly when **TaxUncommitted** is not included.</span></span>

     - <span data-ttu-id="79b21-121">*TaxTrans.insert()*, *TaxTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="79b21-121">*TaxTrans.insert()*, *TaxTrans.update()*</span></span>
     - <span data-ttu-id="79b21-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="79b21-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span></span>

## <a name="reproduce-and-debug"></a><span data-ttu-id="79b21-123">Воспроизведение и отладка</span><span class="sxs-lookup"><span data-stu-id="79b21-123">Reproduce and debug</span></span>

<span data-ttu-id="79b21-124">После задания точек останова во время отладки видны все изменения сохранения данных.</span><span class="sxs-lookup"><span data-stu-id="79b21-124">After the breakpoints are set, every data persistency change is visible during debugging.</span></span> <span data-ttu-id="79b21-125">Чтобы найти основную причину неправильного столбца в **TaxTrans**, **TaxUncommitted** или **TmpTaxWorkTrans**, проверьте и обратите внимание на следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="79b21-125">To find the root cause of an incorrect column of **TaxTrans**, **TaxUncommitted**, or **TmpTaxWorkTrans**, review and note the following items:</span></span>

- <span data-ttu-id="79b21-126">Последняя точка останова, в которой столбец является правильным.</span><span class="sxs-lookup"><span data-stu-id="79b21-126">The last breakpoint where the column is correct.</span></span>
- <span data-ttu-id="79b21-127">Первая точка останова, в которой столбец является неправильным.</span><span class="sxs-lookup"><span data-stu-id="79b21-127">The first breakpoint where the column is incorrect.</span></span>
- <span data-ttu-id="79b21-128">Что происходит между этими двумя точками.</span><span class="sxs-lookup"><span data-stu-id="79b21-128">What happens in between those two points.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="79b21-129">Определение существования настройки</span><span class="sxs-lookup"><span data-stu-id="79b21-129">Determine whether customization exists</span></span>
<span data-ttu-id="79b21-130">Если вы выполнили шаги в предыдущих разделах, но не смогли решить проблему, определите, существует ли настройка.</span><span class="sxs-lookup"><span data-stu-id="79b21-130">If you've completed the steps in the previous sections but have not been able to resolve the issue, determine whether customization exists.</span></span> <span data-ttu-id="79b21-131">Если настройка не существует, обратитесь в службу поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="79b21-131">If no customization exists, contact Microsoft Support for assistance.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

