---
title: Исключение продуктов, имеющих определенные состояния жизненного цикла продукта
description: В этой теме объясняется, как исключать продукты на основе их состояния жизненного цикла при использовании функции оптимизации планирования.
author: ChristianRytt
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7028a509aa884589958542f7ec627d69dffcfcec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839255"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a><span data-ttu-id="b3983-103">Исключение продуктов, имеющих определенные состояния жизненного цикла продукта</span><span class="sxs-lookup"><span data-stu-id="b3983-103">Exclude products that have specific product lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b3983-104">Выпущенные продукты и выпущенные версии продуктов включают поле **Состояние жизненного цикла продукта**.</span><span class="sxs-lookup"><span data-stu-id="b3983-104">Released products and released product versions include a **Product lifecycle state** field.</span></span> <span data-ttu-id="b3983-105">Это поле позволяет контролировать, помимо прочего, какие продукты включаются в сводное планирование.</span><span class="sxs-lookup"><span data-stu-id="b3983-105">This field lets you control, among other things, which products are included during master planning.</span></span> <span data-ttu-id="b3983-106">Можно добавлять, удалять и изменять состояния жизненного цикла, как это необходимо, перейдя в пункт **Управление сведениями о продукте \> Настройка \> Состояние жизненного цикла продукта**.</span><span class="sxs-lookup"><span data-stu-id="b3983-106">You can add, remove, and edit lifecycle states as required by going to **Product information management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="b3983-107">Для каждого состояния жизненного цикла продукта установите для параметра **Активен для планирования** значение *Да*, если продукты, имеющие это состояние, должны быть включены во время сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="b3983-107">For each product lifecycle state, set the **Is active for planning** option to *Yes* if products that have that state should be included during master planning.</span></span> <span data-ttu-id="b3983-108">Если для параметра установлено значение *Нет*, связанные продукты и варианты будут исключены из всего сводного планирования и всех расчетов на уровне спецификации.</span><span class="sxs-lookup"><span data-stu-id="b3983-108">When the option is set to *No*, the associated products and variants will be excluded from all master planning and all calculations at the bill of materials (BOM) level.</span></span>

<span data-ttu-id="b3983-109">Выпущенные продукты и варианты, у которых поле **Состояние жизненного цикла продукта** оставлено пустым, рассматриваются как имеющие состояние жизненного цикла продукта, в котором для параметра **Активен для планирования** выбрано значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="b3983-109">Released products and variants where the **Product lifecycle state** field is left blank are treated as though they have a product lifecycle state where the **Is active for planning** option is set to *Yes*.</span></span> <span data-ttu-id="b3983-110">Другими словами, они будут включены во время сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="b3983-110">In other words, they will be included during master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="b3983-111">Чтобы избежать ненужных предложений по поставкам, настоятельно рекомендуется связать все устаревшие выпущенные продукты и варианты с состоянием жизненного цикла продукта, в котором для параметра **Активен для планирования** выбрано значение *Нет*.</span><span class="sxs-lookup"><span data-stu-id="b3983-111">To help avoid unnecessary supply suggestions, we strongly recommend that you associate all obsolete released products and variants with a product lifecycle state where the **Is active for planning** option is set to *No*.</span></span> <span data-ttu-id="b3983-112">Этот подход особенно важен при работе с вариантами конфигурации продукта, которые не могут быть повторно использованы, так как это поможет предотвратить потери.</span><span class="sxs-lookup"><span data-stu-id="b3983-112">This approach is especially important when you work with product configuration variants that aren't reusable, because it will help prevent waste.</span></span>

## <a name="related-resources"></a><span data-ttu-id="b3983-113">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b3983-113">Related resources</span></span>

<span data-ttu-id="b3983-114">Дополнительные сведения о состояниях жизненного цикла продуктов см. в разделе [Обзор состояний жизненного цикла продуктов](../../pim/product-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="b3983-114">For more information about product lifecycle states, see [Product lifecycle state overview](../../pim/product-lifecycle.md).</span></span>

<span data-ttu-id="b3983-115">Подробные сведения, включающие шаги по использованию состояний жизненного цикла продукта для исключения продуктов из сводного планирования и расчетов на уровне спецификации, см. в разделе [Создание состояния жизненного цикла продукта для исключения продуктов из сводного планирования](../../pim/tasks/exclude-products-master-planning.md).</span><span class="sxs-lookup"><span data-stu-id="b3983-115">For detailed information that includes steps for using product lifecycle states to exclude products from master planning and BOM-level calculations, see [Create a product lifecycle state to exclude products from Master planning](../../pim/tasks/exclude-products-master-planning.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]