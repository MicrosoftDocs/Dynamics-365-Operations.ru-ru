---
title: Категории затрат, используемые в учете управлении производством и управлении проектом
description: Некоторые типы производственных работ могут применяться к оценкам времени и отчетам проекта. В этой статье представлена информация о категориях затрат, которые необходимо определить для этих типов производственных работ для целей производства и для целей проекта.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCategory
audience: Application User
ms.reviewer: kamaybac
ms.custom: 78253
ms.assetid: cfdd58a0-8afa-4a6f-a208-a76e2c162429
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 59bf9c165af83aeb66586adc2d2bfc1bb5068601
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967866"
---
# <a name="cost-categories-used-in-production-control-and-project-management-accounting"></a><span data-ttu-id="de74c-104">Категории затрат, используемые в учете управлении производством и управлении проектом</span><span class="sxs-lookup"><span data-stu-id="de74c-104">Cost categories used in Production control and Project management accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de74c-105">Некоторые типы производственных работ могут применяться к оценкам времени и отчетам проекта.</span><span class="sxs-lookup"><span data-stu-id="de74c-105">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="de74c-106">В этой статье представлена информация о категориях затрат, которые необходимо определить для этих типов производственных работ для целей производства и для целей проекта.</span><span class="sxs-lookup"><span data-stu-id="de74c-106">This article provides information about the cost categories that you must define for these types of production work for production and project purposes.</span></span>

<span data-ttu-id="de74c-107">Некоторые типы производственных работ могут применяться к оценкам времени и отчетам проекта.</span><span class="sxs-lookup"><span data-stu-id="de74c-107">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="de74c-108">В этом случае категория затрат необходима для целей производства и для целей проекта.</span><span class="sxs-lookup"><span data-stu-id="de74c-108">In this case, a cost category is required for production and project purposes.</span></span> <span data-ttu-id="de74c-109">При использовании категории затрат в производстве и в проектах должна быть определена дополнительная информация, относящаяся к проекту.</span><span class="sxs-lookup"><span data-stu-id="de74c-109">When a cost category is used in production and projects, additional project-related information must be defined.</span></span> <span data-ttu-id="de74c-110">Например, почасовые затраты, связанные с проектом, могут отличаться от почасовых затрат, связанных с производством.</span><span class="sxs-lookup"><span data-stu-id="de74c-110">For example, the hourly costs that are associated with projects can differ from the hourly costs that are associated with production.</span></span> <span data-ttu-id="de74c-111">Можно использовать страницу **Категории затрат** для определения категории затрат, которая используется в учете управления производством и управление проектами.</span><span class="sxs-lookup"><span data-stu-id="de74c-111">You can use the **Cost categories** page to define a cost category that is used in Production control and Project management accounting.</span></span> 

<span data-ttu-id="de74c-112">**Примечание.** В учете затрат имеется странице **Категории проекта**, но она не имеет отношения к функции, описываемой в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="de74c-112">**Note:** Cost accounting has a **Project categories** page, but this page has no relationship to the functionality that is described in this topic.</span></span> <span data-ttu-id="de74c-113">При использовании категории затрат в проектах странице **Категории затрат** содержит дополнительные вкладки, содержащие дополнительные сведения, относящиеся к проекту.</span><span class="sxs-lookup"><span data-stu-id="de74c-113">When you use a cost category in projects, the **Cost categories** page has additional tabs that show additional project-related information.</span></span> <span data-ttu-id="de74c-114">Эти сведения включают группу категорий, свойство строки и счета ГК, назначенные категории затрат.</span><span class="sxs-lookup"><span data-stu-id="de74c-114">This information includes the category group, a line property, and ledger accounts that are assigned to the cost category.</span></span>

-   <span data-ttu-id="de74c-115">Категория затрат должна быть назначена группе категорий, поддерживающей проводки, относящиеся к типу **Часы**.</span><span class="sxs-lookup"><span data-stu-id="de74c-115">The cost category must be assigned to a category group that supports a transaction type of **Hours**.</span></span>
-   <span data-ttu-id="de74c-116">Свойство строки указывает используемую по умолчанию информацию о порядке отнесения на проект зарегистрированного времени.</span><span class="sxs-lookup"><span data-stu-id="de74c-116">The line property indicates default information about how reported time can be charged to a project.</span></span>
-   <span data-ttu-id="de74c-117">Обычно счета главной книги, связанные с затратами и продажами, определяются для группы категорий, назначенной категории затрат.</span><span class="sxs-lookup"><span data-stu-id="de74c-117">Typically, the ledger accounts that are related to costs and sales are defined for the category group that is assigned to the cost category.</span></span> <span data-ttu-id="de74c-118">Однако определенные счета могут быть определены для отдельной категории затрат.</span><span class="sxs-lookup"><span data-stu-id="de74c-118">However, specific accounts can be defined for an individual cost category.</span></span>

<span data-ttu-id="de74c-119">Дополнительные кнопки на странице **Категории затрат** обеспечивают доступ к связанной с проектом информации по выбранной категории затрат.</span><span class="sxs-lookup"><span data-stu-id="de74c-119">Additional buttons on the **Cost categories** page let you access project-related information about a selected cost category.</span></span> <span data-ttu-id="de74c-120">Например, можно просмотреть связанные с проектом проводки, определить сотрудников или проекты, определить почасовые затраты и цены продажи, а также просмотреть отчеты.</span><span class="sxs-lookup"><span data-stu-id="de74c-120">For example, you can view project-related transactions, define employees or projects, define hourly costs and sales prices, and view reports.</span></span>



