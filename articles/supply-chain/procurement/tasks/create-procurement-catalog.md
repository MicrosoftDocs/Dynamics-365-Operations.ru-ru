--- 
title: "Создание каталога закупаемой продукции"
description: "В этом руководстве показано, как создать каталог закупаемой продукции."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: c031a6f52464595b1234584930e1230ac9e554bd
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="b3ee4-103">Создание каталога закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="b3ee4-103">Create a procurement catalog</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b3ee4-104">В этом руководстве показано, как создать каталог закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-104">This guide shows you how to create a procurement catalog.</span></span> <span data-ttu-id="b3ee4-105">Эта задача обычно выполняется специалистом по закупкам.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="b3ee4-106">Вы также узнаете, как сотрудники могут использовать каталог при создании заявки.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="b3ee4-107">Перед созданием каталога в системе должна существовать иерархия категорий закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="b3ee4-108">Иерархия наследуется новым каталогом вместе со всеми продуктами в иерархии.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="b3ee4-109">Это руководство можно использовать в компании с демонстрационными данными USMF, в которой доступна иерархия категорий закупаемой продукции, а также примеры, используемые в шагах процедуры.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="b3ee4-110">Убедитесь, что иерархия категорий закупаемой продукции существует.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="b3ee4-111">Перейдите в раздел "Закупки и источники" > "Категории закупаемой продукции".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-111">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="b3ee4-112">Иерархия категорий закупаемой продукции доступна в компании с демонстрационными данными USMF, и продукты добавлены в категорию "Оборудование для офиса/компьютеры".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the Office machines/Computers category.</span></span> <span data-ttu-id="b3ee4-113">Если вы выполняете эту процедуру как руководство по задаче, вам может потребоваться разблокировать руководство, чтобы пролистать категорию.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-113">If you’re running this procedure as a task guide, you’ll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="b3ee4-114">Если иерархия была недоступна, ее можно создать, нажав кнопку "Создать".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-114">If a hierarchy was not available, you’d create it by clicking New.</span></span> <span data-ttu-id="b3ee4-115">Это можно делать только один раз.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-115">This can only be done once.</span></span>  
2. <span data-ttu-id="b3ee4-116">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="b3ee4-117">Создание каталога</span><span class="sxs-lookup"><span data-stu-id="b3ee4-117">Create a catalog</span></span>
1. <span data-ttu-id="b3ee4-118">Перейдите в раздел "Закупки и источники" > "Каталоги" > "Каталоги закупаемой продукции".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-118">Go to Procurement and sourcing > Catalogs > Procurement catalogs.</span></span>
2. <span data-ttu-id="b3ee4-119">Щелкните "Создать каталог закупаемой продукции", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-119">Click New procurement catalog to open the drop dialog.</span></span>
3. <span data-ttu-id="b3ee4-120">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-120">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b3ee4-121">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-121">Click OK.</span></span>
5. <span data-ttu-id="b3ee4-122">В дереве разверните узел "КОРПОРАТИВНЫЕ КАТЕГОРИИ ЗАКУПАЕМОЙ ПРОДУКЦИИ".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-122">In the tree, expand 'CORP PROCUREMENT CATEGORIES'.</span></span>
6. <span data-ttu-id="b3ee4-123">В дереве разверните узел "ОФИСНОЕ ОБОРУДОВАНИЕ".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-123">In the tree, expand 'OFFICE MACHINES'.</span></span>
7. <span data-ttu-id="b3ee4-124">В дереве выберите узел "Компьютеры".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-124">In the tree, select 'Computers'.</span></span>
    * <span data-ttu-id="b3ee4-125">Продукты из категории закупаемой продукции отображаются в списке.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="b3ee4-126">Если необходимо добавить продукт в категорию, это можно сделать на странице "Иерархия категорий закупаемой продукции" или на странице "Сведения о номенклатуре".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-126">If you want to add a product to the category you need to do this on the Procurement category hierarchy page or on the Item details page.</span></span>  
    * <span data-ttu-id="b3ee4-127">Тип обновления по умолчанию определяет, будут ли новые продукты, добавленные в иерархию категорий закупаемой продукции, отображаться сразу же в каталоге.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-127">The Default update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="b3ee4-128">Если для типа обновления задано значение "Динамический", изменения будут отображаться незамедлительно.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-128">If the update type is set to Dynamic, changes are visible immediately.</span></span> <span data-ttu-id="b3ee4-129">Если для типа обновления задано значение "Статический", новые продукты будут отображаться только для пользователей, использующих каталог после повторной публикации каталога.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-129">If the update type is Static, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="b3ee4-130">Действие "Опубликовать" доступно в области действий в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-130">The Publish action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="b3ee4-131">Если продукты удаляются из иерархии категорий закупаемой продукции, изменение отображается немедленно независимо от значения в поле "Тип обновления по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the Default update type field.</span></span>  
8. <span data-ttu-id="b3ee4-132">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-132">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="b3ee4-133">Щелкните "Скрыть".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-133">Click Hide.</span></span>
10. <span data-ttu-id="b3ee4-134">В области действий щелкните "Навигация по категории".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-134">On the Action Pane, click Category navigation.</span></span>
11. <span data-ttu-id="b3ee4-135">Щелкните "Отключить".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-135">Click Disable.</span></span>
12. <span data-ttu-id="b3ee4-136">В области действий щелкните "Навигация по категории".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-136">On the Action Pane, click Category navigation.</span></span>
13. <span data-ttu-id="b3ee4-137">Нажмите кнопку Включить.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-137">Click Enable.</span></span>
14. <span data-ttu-id="b3ee4-138">Щелкните "Активировать каталог".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-138">Click Activate catalog.</span></span>
15. <span data-ttu-id="b3ee4-139">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-139">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="b3ee4-140">Отображение каталога</span><span class="sxs-lookup"><span data-stu-id="b3ee4-140">Make the catalog visible</span></span>
1. <span data-ttu-id="b3ee4-141">Перейдите в раздел "Закупки и источники" > "Настройка" > "Политики" > "Политики закупок".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-141">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="b3ee4-142">Выберите политику закупок USMF.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-142">Select Procurement Policy USMF.</span></span>
    * <span data-ttu-id="b3ee4-143">Необходимо выбрать политику закупок для юридического лица, с которым связан работник и в котором профиль пользователя может заказывать продукты.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-143">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="b3ee4-144">В компании с демонстрационными данными USMF администратор связан с работником Julia Funderburk, и она заказывает продукты в USMF по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-144">In the USMF demo data, the Admin user is connected to the worker called Julia Funderburk, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="b3ee4-145">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-145">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b3ee4-146">Выберите только что созданный каталог.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-146">Select the catalog that you’ve just created.</span></span>
5. <span data-ttu-id="b3ee4-147">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-147">Click OK.</span></span>
6. <span data-ttu-id="b3ee4-148">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-148">Close the page.</span></span>
7. <span data-ttu-id="b3ee4-149">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-149">Close the page.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="b3ee4-150">Использование каталога</span><span class="sxs-lookup"><span data-stu-id="b3ee4-150">Use the catalog</span></span>
1. <span data-ttu-id="b3ee4-151">Перейдите в раздел "Закупки и источники" > "Заявки на закупку" > "Все заявки на закупку".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-151">Go to Procurement and sourcing > Purchase requisitions > All purchase requisitions.</span></span>
2. <span data-ttu-id="b3ee4-152">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-152">Click New.</span></span>
3. <span data-ttu-id="b3ee4-153">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-153">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b3ee4-154">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-154">Click OK.</span></span>
5. <span data-ttu-id="b3ee4-155">Щелкните Добавить продукты.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-155">Click Add products.</span></span>
6. <span data-ttu-id="b3ee4-156">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b3ee4-157">Можно использовать иерархию категорий слева или фильтр вверху списка, чтобы отфильтровать продукты.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-157">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="b3ee4-158">Щелкните "Добавить в строки".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-158">Click Add to lines.</span></span>
8. <span data-ttu-id="b3ee4-159">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-159">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="b3ee4-160">Щелкните "Добавить в строки".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-160">Click Add to lines.</span></span>
10. <span data-ttu-id="b3ee4-161">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b3ee4-161">Click OK.</span></span>


