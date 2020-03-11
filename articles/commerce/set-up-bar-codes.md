---
title: Настройка штрих-кодов
description: В этой статье описывается, как использовать штрих-коды в Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 52801e0d09b1d7da50719966700ca45275d702f7
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057286"
---
# <a name="set-up-bar-codes"></a><span data-ttu-id="520a4-103">Настройка штрих-кодов</span><span class="sxs-lookup"><span data-stu-id="520a4-103">Set up bar codes</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="520a4-104">В этой статье описывается, как использовать штрих-коды в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="520a4-104">This article describes how to use bar codes in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="520a4-105">Штрихкоды можно использовать для приобретения и продажи продуктов, отслеживания вариантов продукции и настройки клиентов и сотрудников.</span><span class="sxs-lookup"><span data-stu-id="520a4-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="520a4-106">Можно также использовать штрихкоды для создания и подписи купонов, подарочных карт и кредитовых авизо.</span><span class="sxs-lookup"><span data-stu-id="520a4-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="520a4-107">Можно настроить продукты так, чтобы они имели стандартные или специальные (внутренние) штрихкоды.</span><span class="sxs-lookup"><span data-stu-id="520a4-107">You can set up products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="520a4-108">Продукты могут иметь несколько штрихкодов.</span><span class="sxs-lookup"><span data-stu-id="520a4-108">Products can have more than one bar code.</span></span> <span data-ttu-id="520a4-109">Например, продукт может иметь несколько штрих-кодов, если он поставляется разными производителями или если он имеет варианты по размеру, стилю или цвету.</span><span class="sxs-lookup"><span data-stu-id="520a4-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="520a4-110">Штрихкоды могут включать массу или стоимость продукта.</span><span class="sxs-lookup"><span data-stu-id="520a4-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="520a4-111">Маски штрихкодов — это шаблоны, используемые для создания штрихкодов.</span><span class="sxs-lookup"><span data-stu-id="520a4-111">Bar code masks are templates that are used to create bar codes.</span></span>

> [!NOTE]
> <span data-ttu-id="520a4-112">Назначение уникального штрих-кода каждой комбинации вариантов позволяет программе определять продаваемый вариант номенклатуры при сканировании штрих-кода.</span><span class="sxs-lookup"><span data-stu-id="520a4-112">If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="520a4-113">Можно также собирать и просматривать статистику о продажах по вариантам.</span><span class="sxs-lookup"><span data-stu-id="520a4-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="520a4-114">Каждой группе размеров, цветов и стилей можно назначить уникальное число, которое определяет эту группу в штрих-коде.</span><span class="sxs-lookup"><span data-stu-id="520a4-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="520a4-115">Commerce использует маску штрих-кода для автоматического создания штрих-кодов для каждой комбинации вариантов.</span><span class="sxs-lookup"><span data-stu-id="520a4-115">Commerce uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="520a4-116">Эта функция окажется полезной при наличии нескольких размеров, цветов и стилей, потому что с добавлением каждого кода варианта число комбинаций значительно увеличивается.</span><span class="sxs-lookup"><span data-stu-id="520a4-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="520a4-117">Если эта функция не используется, штрих-коды необходимо назначать каждой комбинации, представляющей вариант продукта, вручную.</span><span class="sxs-lookup"><span data-stu-id="520a4-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span>

<span data-ttu-id="520a4-118">Штрих-коды можно создавать вручную или автоматически.</span><span class="sxs-lookup"><span data-stu-id="520a4-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="520a4-119">Для того, чтобы создать штрих-коды, завершите следующие задачи в порядке, в котором они перечислены.</span><span class="sxs-lookup"><span data-stu-id="520a4-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1. <span data-ttu-id="520a4-120">[Настройка символов маски штрих-кода](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="520a4-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2. <span data-ttu-id="520a4-121">[Настройка масок штрих-кодов](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="520a4-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3. <span data-ttu-id="520a4-122">Настройка параметров штрих-кодов.</span><span class="sxs-lookup"><span data-stu-id="520a4-122">Configure bar code setups.</span></span>
4. <span data-ttu-id="520a4-123">Создание штрих-кодов для продуктов.</span><span class="sxs-lookup"><span data-stu-id="520a4-123">Create bar codes for products.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="520a4-124">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="520a4-124">Additional resources</span></span>

[<span data-ttu-id="520a4-125">Настройка масок штрихкодов</span><span class="sxs-lookup"><span data-stu-id="520a4-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)
