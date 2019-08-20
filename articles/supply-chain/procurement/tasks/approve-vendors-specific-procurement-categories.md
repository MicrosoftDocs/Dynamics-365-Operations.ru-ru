---
title: Утверждение поставщиков для определенных категорий закупаемой продукции
description: После создания заявки на покупку может потребоваться выбрать утвержденного или предпочтительного поставщика в зависимости от настроек политик закупок.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: eec50e2e8f08fabb64f89c17159b97ba770026f8
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836348"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="ad9bf-103">Утверждение поставщиков для определенных категорий закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="ad9bf-103">Approve vendors for specific procurement categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ad9bf-104">После создания заявки на покупку может потребоваться выбрать утвержденного или предпочтительного поставщика в зависимости от настроек политик закупок.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-104">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="ad9bf-105">В этой процедуре показано, как указать, что поставщик является утвержденным или предпочтительным для определенной категории закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-105">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="ad9bf-106">Эта задача обычно выполняется специалистом по закупкам.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-106">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="ad9bf-107">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-107">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="ad9bf-108">Перейдите в раздел "Закупки и источники" > "Поставщики" > "Все поставщики".</span><span class="sxs-lookup"><span data-stu-id="ad9bf-108">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="ad9bf-109">Выберите поставщика, которого требуется установить как утвержденного или предпочтительного поставщика для категории.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-109">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="ad9bf-110">В области действий щелкните "Общие".</span><span class="sxs-lookup"><span data-stu-id="ad9bf-110">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="ad9bf-111">Щелкните "Категории".</span><span class="sxs-lookup"><span data-stu-id="ad9bf-111">Click Categories.</span></span>
5. <span data-ttu-id="ad9bf-112">Щелкните "Добавить категорию".</span><span class="sxs-lookup"><span data-stu-id="ad9bf-112">Click Add category.</span></span>
6. <span data-ttu-id="ad9bf-113">В поле "Категория" выберите "АКСЕССУАРЫ ДЛЯ ОФИСА И НАСТОЛЬНЫЕ КАНЦЕЛЯРСКИЕ ПРИНАДЛЕЖНОСТИ (АКСЕССУАРЫ ДЛЯ ОФИСА И НАСТОЛЬНЫЕ КАНЦЕЛЯРСКИЕ ПРИНАДЛЕЖНОСТИ).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-113">In the Category field, select OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES).</span></span>
7. <span data-ttu-id="ad9bf-114">В поле "Статус категории поставщика" выберите "Предпочтительный".</span><span class="sxs-lookup"><span data-stu-id="ad9bf-114">In the Vendor category status field, select 'Preferred'.</span></span>
    * <span data-ttu-id="ad9bf-115">Можно указать несколько предпочтительных поставщиков для категории.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-115">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="ad9bf-116">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="ad9bf-116">Click Save.</span></span>
9. <span data-ttu-id="ad9bf-117">Перейдите в раздел "Закупки и источники" > "Категории закупаемой продукции".</span><span class="sxs-lookup"><span data-stu-id="ad9bf-117">Go to Procurement and sourcing > Procurement categories.</span></span>
10. <span data-ttu-id="ad9bf-118">В дереве выберите "КОРПОРАТИВНЫЕ КАТЕГОРИИ ЗАКУПАЕМОЙ ПРОДУКЦИИ\АКСЕССУАРЫ ДЛЯ ОФИСА И НАСТОЛЬНЫЕ КАНЦЕЛЯРСКИЕ ПРИНАДЛЕЖНОСТИ".</span><span class="sxs-lookup"><span data-stu-id="ad9bf-118">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES'.</span></span>
11. <span data-ttu-id="ad9bf-119">Разверните раздел "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="ad9bf-119">Expand the Vendors section.</span></span>
    * <span data-ttu-id="ad9bf-120">Убедитесь, что выбранный поставщик отображается как предпочтительный поставщик для категории "Аксессуары для офиса и настольные канцелярские принадлежности".</span><span class="sxs-lookup"><span data-stu-id="ad9bf-120">Check if the vendor that you selected  appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="ad9bf-121">Если вы выполняете эту процедуру как руководство по задаче, может потребоваться нажать кнопку "Разблокировать", чтобы включить возможность прокрутки вниз списка поставщиков.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-121">If you’re running this procedure as a task guide, you may have to click the Unlock button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="ad9bf-122">Также можно добавить предпочтительных и утвержденных поставщиков на этой странице.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-122">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="ad9bf-123">В дереве разверните узел "АКСЕССУАРЫ ДЛЯ ОФИСА И НАСТОЛЬНЫЕ КАНЦЕЛЯРСКИЕ ПРИНАДЛЕЖНОСТИ".</span><span class="sxs-lookup"><span data-stu-id="ad9bf-123">In the tree, expand 'OFFICE AND DESK ACCESSORIES'.</span></span>
13. <span data-ttu-id="ad9bf-124">В дереве выберите узел "Ножницы".</span><span class="sxs-lookup"><span data-stu-id="ad9bf-124">In the tree, select 'Scissors'.</span></span>
14. <span data-ttu-id="ad9bf-125">Выберите "Нет" в поле "Наследование поставщиков из родительской категории:".</span><span class="sxs-lookup"><span data-stu-id="ad9bf-125">Select No in the Inherit vendors from parent category: field.</span></span>
15. <span data-ttu-id="ad9bf-126">Выберите "Да" в поле "Наследование поставщиков из родительской категории:".</span><span class="sxs-lookup"><span data-stu-id="ad9bf-126">Select Yes in the Inherit vendors from parent category: field.</span></span>

