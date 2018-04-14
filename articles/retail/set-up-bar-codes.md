---
title: "Настройка штрих-кодов"
description: "В этой статье описывается, как использовать штрих-коды в Microsoft Dynamics 365 for Retail."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 099779707cb2b9b821085563b155976cd6ff8777
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-bar-codes"></a><span data-ttu-id="0fb82-103">Настройка штрих-кодов</span><span class="sxs-lookup"><span data-stu-id="0fb82-103">Set up bar codes</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="0fb82-104">В этой статье описывается, как использовать штрих-коды в Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="0fb82-104">This article describes how to use bar codes in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="0fb82-105">Штрихкоды можно использовать для приобретения и продажи продуктов, отслеживания вариантов продукции и настройки клиентов и сотрудников.</span><span class="sxs-lookup"><span data-stu-id="0fb82-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="0fb82-106">Можно также использовать штрихкоды для создания и подписи купонов, подарочных карт и кредитовых авизо.</span><span class="sxs-lookup"><span data-stu-id="0fb82-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="0fb82-107">Можно настроить розничные продукты так, чтобы они имели стандартные или специальные (внутренние) штрихкоды.</span><span class="sxs-lookup"><span data-stu-id="0fb82-107">You can set up retail products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="0fb82-108">Продукты могут иметь несколько штрихкодов.</span><span class="sxs-lookup"><span data-stu-id="0fb82-108">Products can have more than one bar code.</span></span> <span data-ttu-id="0fb82-109">Например, продукт может иметь несколько штрих-кодов, если он поставляется разными производителями или если он имеет варианты по размеру, стилю или цвету.</span><span class="sxs-lookup"><span data-stu-id="0fb82-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="0fb82-110">Штрихкоды могут включать массу или стоимость продукта.</span><span class="sxs-lookup"><span data-stu-id="0fb82-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="0fb82-111">Маски штрихкодов — это шаблоны, используемые для создания штрихкодов.</span><span class="sxs-lookup"><span data-stu-id="0fb82-111">Bar code masks are templates that are used to create bar codes.</span></span> <span data-ttu-id="0fb82-112">**Примечание.** Назначение уникального штрих-кода каждой комбинации вариантов позволяет программе определять продаваемый вариант номенклатуры при сканировании штрих-кода.</span><span class="sxs-lookup"><span data-stu-id="0fb82-112">**Note:** If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="0fb82-113">Можно также собирать и просматривать статистику о продажах по вариантам.</span><span class="sxs-lookup"><span data-stu-id="0fb82-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="0fb82-114">Каждой группе размеров, цветов и стилей можно назначить уникальное число, которое определяет эту группу в штрих-коде.</span><span class="sxs-lookup"><span data-stu-id="0fb82-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="0fb82-115">Dynamics 365 for Retail использует маску штрих-кода для автоматического создания штрих-кодов для каждого варианта комбинации.</span><span class="sxs-lookup"><span data-stu-id="0fb82-115">Dynamics 365 for Retail uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="0fb82-116">Эта функция окажется полезной при наличии нескольких размеров, цветов и стилей, потому что с добавлением каждого кода варианта число комбинаций значительно увеличивается.</span><span class="sxs-lookup"><span data-stu-id="0fb82-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="0fb82-117">Если эта функция не используется, штрих-коды необходимо назначать каждой комбинации, представляющей вариант продукта, вручную.</span><span class="sxs-lookup"><span data-stu-id="0fb82-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span> <span data-ttu-id="0fb82-118">Штрих-коды можно создавать вручную или автоматически.</span><span class="sxs-lookup"><span data-stu-id="0fb82-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="0fb82-119">Для того, чтобы создать штрих-коды, завершите следующие задачи в порядке, в котором они перечислены.</span><span class="sxs-lookup"><span data-stu-id="0fb82-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1.  <span data-ttu-id="0fb82-120">[Настройка символов маски штрих-кода](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="0fb82-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2.  <span data-ttu-id="0fb82-121">[Настройка масок штрих-кодов](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="0fb82-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3.  <span data-ttu-id="0fb82-122">Настройка параметров штрих-кодов.</span><span class="sxs-lookup"><span data-stu-id="0fb82-122">Configure bar code setups.</span></span>
4.  <span data-ttu-id="0fb82-123">Создание штрих-кодов для продуктов.</span><span class="sxs-lookup"><span data-stu-id="0fb82-123">Create bar codes for products.</span></span>


<a name="see-also"></a><span data-ttu-id="0fb82-124">См. также</span><span class="sxs-lookup"><span data-stu-id="0fb82-124">See also</span></span>
--------

[<span data-ttu-id="0fb82-125">Настройка масок штрих-кодов</span><span class="sxs-lookup"><span data-stu-id="0fb82-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)




