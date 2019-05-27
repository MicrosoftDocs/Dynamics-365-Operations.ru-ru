---
title: Настройка политик работы склада (приложение, май 2016 г.)
description: Процессы склада не всегда включают работу склада.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34b4255c85bb53f7e238b60559890571070953a6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569087"
---
# <a name="set-up-warehouse-work-policies-application-may-2016"></a><span data-ttu-id="994f4-103">Настройка политик работы склада (приложение, май 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="994f4-103">Set up warehouse work policies (Application, May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="994f4-104">Процессы склада не всегда включают работу склада.</span><span class="sxs-lookup"><span data-stu-id="994f4-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="994f4-105">Определяя политику работы, можно предотвратить создание работы для комплектации сырья и размещения готовой продукции для набора продуктов в определенных местонахождениях.</span><span class="sxs-lookup"><span data-stu-id="994f4-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="994f4-106">В качестве компании с демонстрационными данными для создания этой записи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="994f4-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="994f4-107">Для выполнения этого руководства по задаче требуется приложение Dynamics AX 7.0.1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="994f4-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="994f4-108">Перейдите в раздел "Управление складом" > "Настройка" > "Работа" > "Политики работы".</span><span class="sxs-lookup"><span data-stu-id="994f4-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="994f4-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="994f4-109">Click New.</span></span>
3. <span data-ttu-id="994f4-110">В поле "Имя политики работы" введите "Не работа размещения".</span><span class="sxs-lookup"><span data-stu-id="994f4-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="994f4-111">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="994f4-111">Click Save.</span></span>
5. <span data-ttu-id="994f4-112">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="994f4-112">Click Add.</span></span>
6. <span data-ttu-id="994f4-113">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="994f4-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="994f4-114">В поле "Тип заказа на выполнение работ" выберите "Размещение готовой продукции".</span><span class="sxs-lookup"><span data-stu-id="994f4-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="994f4-115">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="994f4-115">Click Add.</span></span>
9. <span data-ttu-id="994f4-116">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="994f4-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="994f4-117">В поле "Тип заказа на выполнение работ" выберите "Размещение побочного и сопутствующего продуктов".</span><span class="sxs-lookup"><span data-stu-id="994f4-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="994f4-118">Разверните раздел "Места хранения".</span><span class="sxs-lookup"><span data-stu-id="994f4-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="994f4-119">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="994f4-119">Click Add.</span></span>
13. <span data-ttu-id="994f4-120">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="994f4-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="994f4-121">В списке "Склад" введите "51".</span><span class="sxs-lookup"><span data-stu-id="994f4-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="994f4-122">В поле "Местонахождение" введите или выберите "001".</span><span class="sxs-lookup"><span data-stu-id="994f4-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="994f4-123">Разверните раздел "Продукты".</span><span class="sxs-lookup"><span data-stu-id="994f4-123">Expand the Products section.</span></span>
17. <span data-ttu-id="994f4-124">В поле "Выбор продукта" выберите "Выбрано".</span><span class="sxs-lookup"><span data-stu-id="994f4-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="994f4-125">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="994f4-125">Click Add.</span></span>
19. <span data-ttu-id="994f4-126">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="994f4-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="994f4-127">В поле "Код номенклатуры" введите или выберите "L0101".</span><span class="sxs-lookup"><span data-stu-id="994f4-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="994f4-128">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="994f4-128">Click Save.</span></span>

