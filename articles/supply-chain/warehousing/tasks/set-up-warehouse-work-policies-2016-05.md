--- 
title: "Настройка политик работы склада"
description: "Процессы склада не всегда включают работу склада."
author: johanhoffmann
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b7d579ca7e2b9ca8cbead74b2c2ababfd142f171
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-warehouse-work-policies"></a><span data-ttu-id="f02ab-103">Настройка политик работы склада</span><span class="sxs-lookup"><span data-stu-id="f02ab-103">Set up warehouse work policies</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f02ab-104">Процессы склада не всегда включают работу склада.</span><span class="sxs-lookup"><span data-stu-id="f02ab-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="f02ab-105">Определяя политику работы, можно предотвратить создание работы для комплектации сырья и размещения готовой продукции для набора продуктов в определенных местонахождениях.</span><span class="sxs-lookup"><span data-stu-id="f02ab-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="f02ab-106">В качестве компании с демонстрационными данными для создания этой записи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="f02ab-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="f02ab-107">Для выполнения этого руководства по задаче требуется приложение Dynamics AX 7.0.1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="f02ab-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="f02ab-108">Перейдите в раздел "Управление складом" > "Настройка" > "Работа" > "Политики работы".</span><span class="sxs-lookup"><span data-stu-id="f02ab-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="f02ab-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f02ab-109">Click New.</span></span>
3. <span data-ttu-id="f02ab-110">В поле "Имя политики работы" введите "Не работа размещения".</span><span class="sxs-lookup"><span data-stu-id="f02ab-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="f02ab-111">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f02ab-111">Click Save.</span></span>
5. <span data-ttu-id="f02ab-112">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f02ab-112">Click Add.</span></span>
6. <span data-ttu-id="f02ab-113">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="f02ab-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="f02ab-114">В поле "Тип заказа на выполнение работ" выберите "Размещение готовой продукции".</span><span class="sxs-lookup"><span data-stu-id="f02ab-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="f02ab-115">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f02ab-115">Click Add.</span></span>
9. <span data-ttu-id="f02ab-116">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="f02ab-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="f02ab-117">В поле "Тип заказа на выполнение работ" выберите "Размещение побочного и сопутствующего продуктов".</span><span class="sxs-lookup"><span data-stu-id="f02ab-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="f02ab-118">Разверните раздел "Места хранения".</span><span class="sxs-lookup"><span data-stu-id="f02ab-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="f02ab-119">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f02ab-119">Click Add.</span></span>
13. <span data-ttu-id="f02ab-120">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="f02ab-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="f02ab-121">В списке "Склад" введите "51".</span><span class="sxs-lookup"><span data-stu-id="f02ab-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="f02ab-122">В поле "Местонахождение" введите или выберите "001".</span><span class="sxs-lookup"><span data-stu-id="f02ab-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="f02ab-123">Разверните раздел "Продукты".</span><span class="sxs-lookup"><span data-stu-id="f02ab-123">Expand the Products section.</span></span>
17. <span data-ttu-id="f02ab-124">В поле "Выбор продукта" выберите "Выбрано".</span><span class="sxs-lookup"><span data-stu-id="f02ab-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="f02ab-125">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f02ab-125">Click Add.</span></span>
19. <span data-ttu-id="f02ab-126">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="f02ab-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="f02ab-127">В поле "Код номенклатуры" введите или выберите "L0101".</span><span class="sxs-lookup"><span data-stu-id="f02ab-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="f02ab-128">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f02ab-128">Click Save.</span></span>


