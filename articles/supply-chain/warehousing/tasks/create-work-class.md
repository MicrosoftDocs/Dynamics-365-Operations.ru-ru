--- 
title: "Создание класса работ"
description: "В этой процедуре показано, как настроить класс работы."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9a775366bdaecb59a375f245f7a4d17a659cab11
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-work-class"></a><span data-ttu-id="cfd55-103">Создание класса работ</span><span class="sxs-lookup"><span data-stu-id="cfd55-103">Create a work class</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cfd55-104">В этой процедуре показано, как настроить класс работы.</span><span class="sxs-lookup"><span data-stu-id="cfd55-104">This procedure shows you how to set up a work class.</span></span> <span data-ttu-id="cfd55-105">Классы работы используются для определения и/или ограничения типа строк заказа на работу, которые работник склада может обрабатывать на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="cfd55-105">Work classes are used to direct and/or limit the type of work order lines that a warehouse worker can process on a mobile device.</span></span> <span data-ttu-id="cfd55-106">Строки, которые может обрабатывать работник склада, определяются по классам работы, соответствующим пунктам меню мобильного устройства, доступ к которым имеет работник, и классу работы, указанному в строках работы.</span><span class="sxs-lookup"><span data-stu-id="cfd55-106">The lines that a worker can process are determined from the work classes on the mobile device menu items that the warehouse worker has access to and the work class that’s specified on the work lines.</span></span> <span data-ttu-id="cfd55-107">Классы работы можно также использовать для проверки местонахождения размещения для строки заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="cfd55-107">Work classes can also be used to validate the put location for a work order line.</span></span> <span data-ttu-id="cfd55-108">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="cfd55-108">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="cfd55-109">Эта процедура предназначена для менеджера склада.</span><span class="sxs-lookup"><span data-stu-id="cfd55-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="cfd55-110">Перейдите в раздел "Управление складом" > "Настройка" > "Работа" > "Классы работы".</span><span class="sxs-lookup"><span data-stu-id="cfd55-110">Go to Warehouse management > Setup > Work > Work classes.</span></span>
2. <span data-ttu-id="cfd55-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="cfd55-111">Click New.</span></span>
3. <span data-ttu-id="cfd55-112">В поле "Код класса работы" введите значение.</span><span class="sxs-lookup"><span data-stu-id="cfd55-112">In the Work class ID field, type a value.</span></span>
4. <span data-ttu-id="cfd55-113">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="cfd55-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cfd55-114">В поле "Тип заказа на выполнение работ" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="cfd55-114">In the Work order type field, select an option.</span></span>
6. <span data-ttu-id="cfd55-115">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="cfd55-115">Click New.</span></span>
7. <span data-ttu-id="cfd55-116">В поле "Тип местоположения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="cfd55-116">In the Location type field, type a value.</span></span>
    * <span data-ttu-id="cfd55-117">Если выбран тип местонахождения, это устанавливает ограничение на то, где могут быть размещены номенклатуры после их комплектации.</span><span class="sxs-lookup"><span data-stu-id="cfd55-117">If you select a location type, this sets a restriction on where items can be put after they’ve been picked.</span></span> <span data-ttu-id="cfd55-118">Этот параметр используется, когда директива места хранения пытается разрешить местонахождение, или если работник склада вручную предоставляет местонахождение для пункта меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="cfd55-118">This setting is used when a location directive tries to resolve the location, or if a warehouse worker manually provides the location for the mobile device menu item.</span></span>  
8. <span data-ttu-id="cfd55-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="cfd55-119">Close the page.</span></span>


