---
title: Утверждение поставщиков для определенных категорий закупаемой продукции
description: В этой теме объясняется, как утвердить поставщиков для определенных категорий закупок в Dynamics 365 Supply Chain Management.
author: mkirknel
manager: AnnBe
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 135b3a6bea2c0a8940550299504139551c9c3559
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147511"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="4421c-103">Утверждение поставщиков для определенных категорий закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="4421c-103">Approve vendors for specific procurement categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4421c-104">В этой теме объясняется, как утвердить поставщиков для определенных категорий закупок в Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4421c-104">This topic explains how to approve vendors for specific procurement categories in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="4421c-105">После создания заявки на покупку может потребоваться выбрать утвержденного или предпочтительного поставщика в зависимости от настроек политик закупок.</span><span class="sxs-lookup"><span data-stu-id="4421c-105">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="4421c-106">В этой процедуре показано, как указать, что поставщик является утвержденным или предпочтительным для определенной категории закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="4421c-106">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="4421c-107">Эта задача обычно выполняется специалистом по закупкам.</span><span class="sxs-lookup"><span data-stu-id="4421c-107">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="4421c-108">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="4421c-108">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="4421c-109">В область переходов выберите **Модули > Закупки и источники > Поставщики > Все поставщики**.</span><span class="sxs-lookup"><span data-stu-id="4421c-109">In the navigation pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="4421c-110">Выберите поставщика, которого требуется установить как утвержденного или предпочтительного поставщика для категории.</span><span class="sxs-lookup"><span data-stu-id="4421c-110">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="4421c-111">На панели операций выберите **Общее**.</span><span class="sxs-lookup"><span data-stu-id="4421c-111">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="4421c-112">Выберите **Категории**.</span><span class="sxs-lookup"><span data-stu-id="4421c-112">Select **Categories**.</span></span>
5. <span data-ttu-id="4421c-113">Выберите **Добавить категорию**.</span><span class="sxs-lookup"><span data-stu-id="4421c-113">Select **Add category**.</span></span>
6. <span data-ttu-id="4421c-114">В поле **Категория** выберите **АКСЕССУАРЫ ДЛЯ ОФИСА И НАСТОЛЬНЫЕ КАНЦЕЛЯРСКИЕ ПРИНАДЛЕЖНОСТИ (АКСЕССУАРЫ ДЛЯ ОФИСА И НАСТОЛЬНЫЕ КАНЦЕЛЯРСКИЕ ПРИНАДЛЕЖНОСТИ)**.</span><span class="sxs-lookup"><span data-stu-id="4421c-114">In the **Category** field, select **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.</span></span>
7. <span data-ttu-id="4421c-115">В поле **Статус категории поставщика** выберите **Предпочтительный**.</span><span class="sxs-lookup"><span data-stu-id="4421c-115">In the **Vendor category status** field, select **Preferred**.</span></span> <span data-ttu-id="4421c-116">Можно указать несколько предпочтительных поставщиков для категории.</span><span class="sxs-lookup"><span data-stu-id="4421c-116">It's possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="4421c-117">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="4421c-117">Select **Save**.</span></span>
9. <span data-ttu-id="4421c-118">В области перехода выберите **Модули > Закупки и источники > Категории закупаемой продукции**.</span><span class="sxs-lookup"><span data-stu-id="4421c-118">In the navigation pane, go to **Modules > Procurement and sourcing > Procurement categories**.</span></span>
10. <span data-ttu-id="4421c-119">В дереве выберите **КОРПОРАТИВНЫЕ КАТЕГОРИИ ЗАКУПАЕМОЙ ПРОДУКЦИИ\АКСЕССУАРЫ ДЛЯ ОФИСА И НАСТОЛЬНЫЕ КАНЦЕЛЯРСКИЕ ПРИНАДЛЕЖНОСТИ**.</span><span class="sxs-lookup"><span data-stu-id="4421c-119">In the tree, select **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.</span></span>
11. <span data-ttu-id="4421c-120">Разверните раздел **Поставщики**.</span><span class="sxs-lookup"><span data-stu-id="4421c-120">Expand the **Vendors** section.</span></span> <span data-ttu-id="4421c-121">Убедитесь, что выбранный поставщик отображается как предпочтительный поставщик для категории "Аксессуары для офиса и настольные канцелярские принадлежности".</span><span class="sxs-lookup"><span data-stu-id="4421c-121">Check if the vendor that you selected appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="4421c-122">Если вы выполняете эту процедуру как руководство по задаче, может потребоваться выбрать кнопку **Разблокировать**, чтобы включить возможность прокрутки вниз списка поставщиков.</span><span class="sxs-lookup"><span data-stu-id="4421c-122">If you're running this procedure as a task guide, you may have to select the **Unlock** button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="4421c-123">Также можно добавить предпочтительных и утвержденных поставщиков на этой странице.</span><span class="sxs-lookup"><span data-stu-id="4421c-123">It's also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="4421c-124">В дереве разверните узел **АКСЕССУАРЫ ДЛЯ ОФИСА И НАСТОЛЬНЫЕ КАНЦЕЛЯРСКИЕ ПРИНАДЛЕЖНОСТИ** и выберите **Ножницы**.</span><span class="sxs-lookup"><span data-stu-id="4421c-124">In the tree, expand **OFFICE AND DESK ACCESSORIES** and select **Scissors**.</span></span>
13. <span data-ttu-id="4421c-125">Выберите **Нет** в поле **Наследование поставщиков из родительской категории:**.</span><span class="sxs-lookup"><span data-stu-id="4421c-125">Select **No** in the **Inherit vendors from parent category:** field.</span></span>
14. <span data-ttu-id="4421c-126">Выберите **Да** в поле **Наследование поставщиков из родительской категории:**.</span><span class="sxs-lookup"><span data-stu-id="4421c-126">Select **Yes** in the **Inherit vendors from parent category:** field.</span></span>

