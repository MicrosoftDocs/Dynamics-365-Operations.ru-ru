---
title: "Системные и пользовательские ограничения таблиц"
description: "В этой статье рассматриваются два типа ограничений таблицы для компонентов в модели конфигурации продукта — определяемые пользователем и определяемые системой. Ограничения таблицы представляют собой матрицы разрешенных комбинаций атрибутов, где каждая строка определяет один набор возможных значений атрибутов."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 4da560ca3cce5a28edd2a00506f825d5d88ef0f3
ms.contentlocale: ru-ru
ms.lasthandoff: 02/07/2018

---

# <a name="system-defined-and-user-defined-table-constraints"></a><span data-ttu-id="859f2-104">Системные и пользовательские ограничения таблиц</span><span class="sxs-lookup"><span data-stu-id="859f2-104">System-defined and user-defined table constraints</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="859f2-105">В этой статье рассматриваются два типа ограничений таблицы для компонентов в модели конфигурации продукта — определяемые пользователем и определяемые системой.</span><span class="sxs-lookup"><span data-stu-id="859f2-105">This article explains the two types of table constraints for components in a product configuration model -  user-defined and system-defined.</span></span> <span data-ttu-id="859f2-106">Ограничения таблицы представляют собой матрицы разрешенных комбинаций атрибутов, где каждая строка определяет один набор возможных значений атрибутов.</span><span class="sxs-lookup"><span data-stu-id="859f2-106">Table constraints represent matrices of the allowed attribute combinations, where each row defines one set of possible attribute values.</span></span>

<span data-ttu-id="859f2-107">Ограничения таблиц представляют собой матрицы сочетаний атрибутов, который разрешены для компонентов в модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="859f2-107">Table constraints represent matrices of the combinations of attributes that are allowed for components in a product configuration model.</span></span> <span data-ttu-id="859f2-108">Каждая строка в таблице определяет один комплект возможных значений атрибутов.</span><span class="sxs-lookup"><span data-stu-id="859f2-108">Each row in the table defines one set of possible attribute values.</span></span> <span data-ttu-id="859f2-109">В модели конфигурации продукта можно объявить два типа ограничений:</span><span class="sxs-lookup"><span data-stu-id="859f2-109">You can declare two types of constraints in a product configuration model:</span></span>

-   <span data-ttu-id="859f2-110">**Ограничение для выражения** — создайте выражение, которое определяет отношения между атрибутами, чтобы при конфигурации продукта можно была выбрать только совместимые значения.</span><span class="sxs-lookup"><span data-stu-id="859f2-110">**Expression constraint** – Create an expression that defines relations between attributes to guarantee that only compatible values can be selected during product configuration.</span></span>
-   <span data-ttu-id="859f2-111">**Ограничение таблицы** — создание таблицы, которая определяет все комбинации, разрешенные для определенного набора атрибутов.</span><span class="sxs-lookup"><span data-stu-id="859f2-111">**Table constraint** – Create a table that defines all the combinations that are allowed for a specified set of attributes.</span></span> <span data-ttu-id="859f2-112">Два Типа ограничений таблицы доступны: пользовательские ограничения таблицы и системные ограничения таблицы.</span><span class="sxs-lookup"><span data-stu-id="859f2-112">Two types of table constraints are available: user-defined table constraints and system-defined table constraints.</span></span>

<span data-ttu-id="859f2-113">В этой статье описываются ограничения таблицы, которые пользователями и системой определены для компонентов в модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="859f2-113">This article describes user-defined and system-defined table constraints for components in a product configuration model.</span></span>

## <a name="user-defined-table-constraints"></a><span data-ttu-id="859f2-114">Пользовательские ограничения таблицы</span><span class="sxs-lookup"><span data-stu-id="859f2-114">User-defined table constraints</span></span>
<span data-ttu-id="859f2-115">Пользовательские ограничения таблицы — это тип матрицы, который может использоваться для описания комбинаций для значений атрибутов, которые определяются типами атрибута.</span><span class="sxs-lookup"><span data-stu-id="859f2-115">A user-defined table constraint is a type of matrix that is used to describe the combinations of attribute values that are defined by attribute types.</span></span> <span data-ttu-id="859f2-116">Например, если вы делаете динамики, можно включить столбцы для отделки корпуса и передней решетки в пользовательское ограничение таблицы.</span><span class="sxs-lookup"><span data-stu-id="859f2-116">For example, if you produce speakers, you can include columns for the cabinet finish and the front grill in the user-defined table constraint.</span></span> <span data-ttu-id="859f2-117">Тип атрибута для отделки корпуса имеет четыре значения, и тип атрибута для передней решетки имеет три значения.</span><span class="sxs-lookup"><span data-stu-id="859f2-117">The attribute type for the cabinet finish has four values, and the attribute type for the front grill has three values.</span></span> <span data-ttu-id="859f2-118">Поэтому если ограничения не используются, возможно 4 × 3 = 12 комбинаций.</span><span class="sxs-lookup"><span data-stu-id="859f2-118">Therefore, if constraints aren't used, there are 4 × 3 = 12 possible combinations.</span></span> <span data-ttu-id="859f2-119">Однако в этом примере допускается только шесть комбинаций, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="859f2-119">However, in this example, only six combinations are allowed, as shown in the following table.</span></span> <span data-ttu-id="859f2-120">Эта информация отображается на вкладке **Разрешенные комбинации** на странице **Изменить ограничение таблицы**.</span><span class="sxs-lookup"><span data-stu-id="859f2-120">This information is displayed on the **Allowed combinations** tab on the **Edit table constraint** page.</span></span>

| <span data-ttu-id="859f2-121">Отделка корпуса</span><span class="sxs-lookup"><span data-stu-id="859f2-121">Cabinet finish</span></span> | <span data-ttu-id="859f2-122">Передняя решетка</span><span class="sxs-lookup"><span data-stu-id="859f2-122">Front grill</span></span> |
|----------------|-------------|
| <span data-ttu-id="859f2-123">Черный</span><span class="sxs-lookup"><span data-stu-id="859f2-123">Black</span></span>          | <span data-ttu-id="859f2-124">Черный</span><span class="sxs-lookup"><span data-stu-id="859f2-124">Black</span></span>       |
| <span data-ttu-id="859f2-125">Черный</span><span class="sxs-lookup"><span data-stu-id="859f2-125">Black</span></span>          | <span data-ttu-id="859f2-126">Металл</span><span class="sxs-lookup"><span data-stu-id="859f2-126">Metal</span></span>       |
| <span data-ttu-id="859f2-127">Дуб</span><span class="sxs-lookup"><span data-stu-id="859f2-127">Oak</span></span>            | <span data-ttu-id="859f2-128">Черный</span><span class="sxs-lookup"><span data-stu-id="859f2-128">Black</span></span>       |
| <span data-ttu-id="859f2-129">Палисандр</span><span class="sxs-lookup"><span data-stu-id="859f2-129">Rosewood</span></span>       | <span data-ttu-id="859f2-130">Белый</span><span class="sxs-lookup"><span data-stu-id="859f2-130">White</span></span>       |
| <span data-ttu-id="859f2-131">Белый</span><span class="sxs-lookup"><span data-stu-id="859f2-131">White</span></span>          | <span data-ttu-id="859f2-132">Черный</span><span class="sxs-lookup"><span data-stu-id="859f2-132">Black</span></span>       |
| <span data-ttu-id="859f2-133">Белый</span><span class="sxs-lookup"><span data-stu-id="859f2-133">White</span></span>          | <span data-ttu-id="859f2-134">Белый</span><span class="sxs-lookup"><span data-stu-id="859f2-134">White</span></span>       |

<span data-ttu-id="859f2-135">Пользовательские ограничения таблицы определяются статическим вводов в таблицу, который действует так же, как ограничение выражения.</span><span class="sxs-lookup"><span data-stu-id="859f2-135">User-defined table constraints are defined by static table input that works the same way as an expression constraint.</span></span> <span data-ttu-id="859f2-136">При использовании пользовательских ограничений таблицы, преимущество в том, что таблицы часто бывает проще создать, понимать и поддерживать, чем длинные ограничения выражения.</span><span class="sxs-lookup"><span data-stu-id="859f2-136">When you use a user-defined table constraint, the advantage is that tables are often easier to create, understand, and maintain than long expression constraints.</span></span>

## <a name="system-defined-table-constraints"></a><span data-ttu-id="859f2-137">Определенные системой ограничения таблицы</span><span class="sxs-lookup"><span data-stu-id="859f2-137">System-defined table constraints</span></span>
<span data-ttu-id="859f2-138">Системой определенное ограничение таблицы создает динамическое сопоставление между типом атрибута и полем в таблице.</span><span class="sxs-lookup"><span data-stu-id="859f2-138">A system-defined table constraint creates a dynamic mapping between an attribute type and a field in a table.</span></span> <span data-ttu-id="859f2-139">Когда определенное системой ограничение таблицы включено в модель конфигурации продукта, сопоставление гарантирует, что данные в таблице отображаются вместо значений типа атрибута.</span><span class="sxs-lookup"><span data-stu-id="859f2-139">When a system-defined table constraint is included in a product configuration model, the mapping guarantees that the data in the table is shown instead of the values of the attribute type.</span></span> <span data-ttu-id="859f2-140">Результатом является динамическое ограничение, поскольку содержимое таблицы может быть изменено (например, другими модулями).</span><span class="sxs-lookup"><span data-stu-id="859f2-140">The result is a dynamic constraint, because the table contents can be modified (for example, by other modules).</span></span>  

<span data-ttu-id="859f2-141">При создании системой определенного ограничения таблицы, вы выбираете таблицу, при желании определяет запрос, который необходимо использовать, а затем связываете типы атрибутов с полями в выбранной таблице.</span><span class="sxs-lookup"><span data-stu-id="859f2-141">When you create a system-defined table constraint, you select a table, optionally define the query to use, and then associate attribute types to the fields in the selected table.</span></span> <span data-ttu-id="859f2-142">Типы полей должны соответствовать типам типов атрибута.</span><span class="sxs-lookup"><span data-stu-id="859f2-142">The types of fields must match the types of attribute types.</span></span>  

<span data-ttu-id="859f2-143">Прежде чем ограничение таблицы может начать действовать в модели конфигурации продукта, ограничение таблицы необходимо включить в ограничение на одном из компонентов модели.</span><span class="sxs-lookup"><span data-stu-id="859f2-143">Before a table constraint can take effect on a product configuration model, the table constraint must be included in a constraint on one of the model's components.</span></span> <span data-ttu-id="859f2-144">Процедура заключается в том, чтобы создать новое ограничение, выбрать тип ограничения таблицы, затем выбрать определение ограничения таблицы для использования.</span><span class="sxs-lookup"><span data-stu-id="859f2-144">The procedure is to create a new constraint, select the table constraint type, and then select the table constraint definition to use.</span></span> <span data-ttu-id="859f2-145">В заключение все поля в ограничении таблицы необходимо составить атрибутам в модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="859f2-145">Finally, all fields in the table constraint must be mapped to attributes in the product configuration model.</span></span>

<a name="see-also"></a><span data-ttu-id="859f2-146">См. также</span><span class="sxs-lookup"><span data-stu-id="859f2-146">See also</span></span>
--------

[<span data-ttu-id="859f2-147">Основные понятия моделей конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="859f2-147">Key concepts in product configuration models</span></span>](product-configuration-models.md)




