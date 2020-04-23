---
title: Создание каталога закупаемой продукции
description: В этом разделе объясняется, как создать каталог закупаемой продукции.
author: mkirknel
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20966291ce6297561514ce9d9f7e945859997351
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205879"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="7bc6f-103">Создание каталога закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="7bc6f-103">Create a procurement catalog</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7bc6f-104">В этом разделе объясняется, как создать каталог закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-104">This topic explains how to create a procurement catalog.</span></span> <span data-ttu-id="7bc6f-105">Эта задача обычно выполняется специалистом по закупкам.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="7bc6f-106">Вы также узнаете, как сотрудники могут использовать каталог при создании заявки.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="7bc6f-107">Перед созданием каталога в системе должна существовать иерархия категорий закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="7bc6f-108">Иерархия наследуется новым каталогом вместе со всеми продуктами в иерархии.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="7bc6f-109">Это руководство можно использовать в компании с демонстрационными данными USMF, в которой доступна иерархия категорий закупаемой продукции, а также примеры, используемые в шагах процедуры.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="7bc6f-110">Убедитесь, что иерархия категорий закупаемой продукции существует.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="7bc6f-111">Выберите **область переходов > Модули > Закупки и источники > Категории закупаемой продукции**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-111">Go to **navigation pane > Modules > Procurement and sourcing > Procurement categories**.</span></span> <span data-ttu-id="7bc6f-112">Иерархия категорий закупаемой продукции доступна в компании с демонстрационными данными USMF, и продукты добавлены в категорию **Оборудование для офиса/компьютеры**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the **Office machines/Computers** category.</span></span> <span data-ttu-id="7bc6f-113">Если вы выполняете эту процедуру как руководство по задаче, вам может потребоваться разблокировать руководство, чтобы пролистать категорию.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-113">If you're running this procedure as a task guide, you'll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="7bc6f-114">Если иерархия была недоступна, ее можно создать, нажав кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-114">If a hierarchy was not available, you'd create it by clicking **New**.</span></span> <span data-ttu-id="7bc6f-115">Это можно делать только один раз.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-115">This can only be done once.</span></span>  
2. <span data-ttu-id="7bc6f-116">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="7bc6f-117">Создание каталога</span><span class="sxs-lookup"><span data-stu-id="7bc6f-117">Create a catalog</span></span>
1. <span data-ttu-id="7bc6f-118">Выберите **область переходов > Модули > Закупки и источники > Каталоги > Каталоги закупаемой продукции**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-118">Go to **navigation pane > Modules > Procurement and sourcing > Catalogs > Procurement catalogs**.</span></span>
2. <span data-ttu-id="7bc6f-119">Выберите **Создать каталог закупаемой продукции**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-119">Select **New procurement catalog** to open the drop dialog.</span></span>
3. <span data-ttu-id="7bc6f-120">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-120">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="7bc6f-121">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-121">Select **OK**.</span></span>
5. <span data-ttu-id="7bc6f-122">В дереве разверните узел **КОРПОРАТИВНЫЕ КАТЕГОРИИ ЗАКУПАЕМОЙ ПРОДУКЦИИ**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-122">In the tree, expand **CORP PROCUREMENT CATEGORIES**.</span></span>
6. <span data-ttu-id="7bc6f-123">В дереве разверните узел **ОФИСНОЕ ОБОРУДОВАНИЕ**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-123">In the tree, expand **OFFICE MACHINES**.</span></span>
7. <span data-ttu-id="7bc6f-124">В дереве выберите узел **Компьютеры**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-124">In the tree, select **Computers**.</span></span>

  - <span data-ttu-id="7bc6f-125">Продукты из категории закупаемой продукции отображаются в списке.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="7bc6f-126">Если необходимо добавить продукт в категорию, это можно сделать на странице **Иерархия категорий закупаемой продукции** или на странице **Сведения о номенклатуре**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-126">If you want to add a product to the category you need to do this on the **Procurement category hierarchy** page or on the **Item details** page.</span></span>  
  - <span data-ttu-id="7bc6f-127">Тип обновления **По умолчанию** определяет, будут ли новые продукты, добавленные в иерархию категорий закупаемой продукции, отображаться сразу же в каталоге.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-127">The **Default** update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="7bc6f-128">Если для типа обновления задано значение **Динамический**, изменения будут отображаться незамедлительно.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-128">If the update type is set to **Dynamic**, changes are visible immediately.</span></span> <span data-ttu-id="7bc6f-129">Если для типа обновления задано значение **Статический**, новые продукты будут отображаться только для пользователей, использующих каталог после повторной публикации каталога.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-129">If the update type is **Static**, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="7bc6f-130">Действие **Опубликовать** доступно в области действий в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-130">The **Publish** action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="7bc6f-131">Если продукты удаляются из иерархии категорий закупаемой продукции, изменение отображается немедленно независимо от значения в поле типа обновления **По умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the **Default** update type field.</span></span>  

8. <span data-ttu-id="7bc6f-132">На панели действий выберите **Навигация по категории** и убедитесь, что выбрано значение **Включить**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-132">On the Action Pane, select **Category navigation** and ensure that **Enable** is selected.</span></span>
9. <span data-ttu-id="7bc6f-133">Выберите **Активировать каталог**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-133">Select **Activate catalog**.</span></span>
10. <span data-ttu-id="7bc6f-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-134">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="7bc6f-135">Отображение каталога</span><span class="sxs-lookup"><span data-stu-id="7bc6f-135">Make the catalog visible</span></span>
1. <span data-ttu-id="7bc6f-136">Выберите **область навигации > Модули > Закупки и источники > Настройка > Политики > Политики закупок**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-136">Go to **navigation pane > Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="7bc6f-137">Выберите **Политика закупок USMF**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-137">Select **Procurement Policy USMF**.</span></span> <span data-ttu-id="7bc6f-138">Необходимо выбрать политику закупок для юридического лица, с которым связан работник и в котором профиль пользователя может заказывать продукты.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-138">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="7bc6f-139">В компании с демонстрационными данными USMF администратор связан с работником **Julia Funderburk**, и она заказывает продукты в USMF по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-139">In the USMF demo data, the Admin user is connected to the worker called **Julia Funderburk**, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="7bc6f-140">Выберите только что созданный каталог.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-140">Select the catalog that you've just created.</span></span>
4. <span data-ttu-id="7bc6f-141">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-141">Select **OK**.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="7bc6f-142">Использование каталога</span><span class="sxs-lookup"><span data-stu-id="7bc6f-142">Use the catalog</span></span>
1. <span data-ttu-id="7bc6f-143">Перейдите в **область перехода > Модули > Закупки и источники > Заявки на покупку > Все заявки на покупку**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-143">Go to **navigation pane > Modules > Procurement and sourcing > Purchase requisitions > All purchase requisitions**.</span></span>
2. <span data-ttu-id="7bc6f-144">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-144">Select **New**.</span></span>
3. <span data-ttu-id="7bc6f-145">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-145">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="7bc6f-146">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-146">Select **OK**.</span></span>
5. <span data-ttu-id="7bc6f-147">Выберите **Добавить продукты**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-147">Select **Add products**.</span></span>
6. <span data-ttu-id="7bc6f-148">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-148">In the list, find and select the desired record.</span></span> <span data-ttu-id="7bc6f-149">Можно использовать иерархию категорий слева или фильтр вверху списка, чтобы отфильтровать продукты.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-149">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="7bc6f-150">Выберите **Добавить в строки**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-150">Select **Add to lines**.</span></span>
8. <span data-ttu-id="7bc6f-151">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7bc6f-151">Select **OK**.</span></span>

