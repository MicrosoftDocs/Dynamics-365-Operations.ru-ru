--- 
title: "Настройка иерархии категорий закупаемой продукции"
description: "В этой процедуре показано, как создавать новые узлы в иерархии категорий закупаемой продукции, а также как настроить категорию закупаемой продукции для использования в процессе закупки."
author: mkirknel
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b9897b1184e8159b20a45d4cedbba56baef31a3c
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="862be-103">Настройка иерархии категорий закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="862be-103">Set up a procurement category hierarchy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="862be-104">В этой процедуре показано, как создавать новые узлы в иерархии категорий закупаемой продукции, а также как настроить категорию закупаемой продукции для использования в процессе закупки.</span><span class="sxs-lookup"><span data-stu-id="862be-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="862be-105">Эти задачи обычно выполняются менеджером по закупкам.</span><span class="sxs-lookup"><span data-stu-id="862be-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="862be-106">Для начала этой процедуры должна существовать иерархия категорий закупаемой продукции типа "Закупка".</span><span class="sxs-lookup"><span data-stu-id="862be-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="862be-107">При использовании компании демонстрационных данных эту процедуру можно выполнять в компании USMF.</span><span class="sxs-lookup"><span data-stu-id="862be-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="862be-108">Добавление новой категории закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="862be-108">Add a new procurement category</span></span>
1. <span data-ttu-id="862be-109">Перейдите "Закупки и источники" > ..</span><span class="sxs-lookup"><span data-stu-id="862be-109">Go to Procurement and sourcing > ..</span></span> <span data-ttu-id="862be-110">> "Категории закупаемой продукции".</span><span class="sxs-lookup"><span data-stu-id="862be-110">> Procurement categories.</span></span>
2. <span data-ttu-id="862be-111">Щелкните "Изменить иерархию категорий".</span><span class="sxs-lookup"><span data-stu-id="862be-111">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="862be-112">Текущая иерархия категорий закупаемой продукции отображается в левой части страницы.</span><span class="sxs-lookup"><span data-stu-id="862be-112">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="862be-113">Вам предстоит внести изменения в эту иерархию.</span><span class="sxs-lookup"><span data-stu-id="862be-113">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="862be-114">Щелкните "Новый узел категории".</span><span class="sxs-lookup"><span data-stu-id="862be-114">Click New category node.</span></span>
    * <span data-ttu-id="862be-115">Система по умолчанию выбирает верхний узел.</span><span class="sxs-lookup"><span data-stu-id="862be-115">The system selects the top node by default.</span></span> <span data-ttu-id="862be-116">Если вы выполняете эту процедуру как руководство по задаче, вы можете нажать кнопку "Разблокировать" и выбрать для вставки нового узла другой родительский узел.</span><span class="sxs-lookup"><span data-stu-id="862be-116">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="862be-117">После этого снова заблокируйте руководство по задаче и щелкните "Новый узел категории".</span><span class="sxs-lookup"><span data-stu-id="862be-117">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="862be-118">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="862be-118">In the Name field, type a value.</span></span>
5. <span data-ttu-id="862be-119">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="862be-119">In the Description field, type a value.</span></span>
6. <span data-ttu-id="862be-120">В поле "Понятное имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="862be-120">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="862be-121">Понятное имя указывать необязательно.</span><span class="sxs-lookup"><span data-stu-id="862be-121">The friendly name is optional.</span></span> <span data-ttu-id="862be-122">Оно будет отображаться в поисках категорий вместе с именем категории.</span><span class="sxs-lookup"><span data-stu-id="862be-122">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="862be-123">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="862be-123">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="862be-124">Добавление продуктов в новую категорию закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="862be-124">Add products to your new procurement category</span></span>
1. <span data-ttu-id="862be-125">Перейдите "Закупки и источники" > ..</span><span class="sxs-lookup"><span data-stu-id="862be-125">Go to Procurement and sourcing > ..</span></span> <span data-ttu-id="862be-126">> "Категории закупаемой продукции".</span><span class="sxs-lookup"><span data-stu-id="862be-126">> Procurement categories.</span></span>
    * <span data-ttu-id="862be-127">Выберите только что добавленный узел.</span><span class="sxs-lookup"><span data-stu-id="862be-127">Select the node you just added.</span></span> <span data-ttu-id="862be-128">Если вы выполняете эту процедуру как руководство по задаче, вам может потребоваться разблокировать руководство по задаче, чтобы выбрать узел.</span><span class="sxs-lookup"><span data-stu-id="862be-128">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="862be-129">Переключите развертывание раздела "Продукты".</span><span class="sxs-lookup"><span data-stu-id="862be-129">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="862be-130">Щелкните "Добавить", чтобы связать продукты с категорией закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="862be-130">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="862be-131">Выберите карточку продукта, которую требуется добавить в категорию закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="862be-131">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="862be-132">Щелкните стрелку, чтобы выбрать продукт.</span><span class="sxs-lookup"><span data-stu-id="862be-132">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="862be-133">Выберите еще один продукт для добавления в категорию закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="862be-133">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="862be-134">Щелкните стрелку, чтобы выбрать продукт.</span><span class="sxs-lookup"><span data-stu-id="862be-134">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="862be-135">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="862be-135">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="862be-136">Добавление утвержденных и предпочтительных поставщиков</span><span class="sxs-lookup"><span data-stu-id="862be-136">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="862be-137">Переключите развертывание раздела "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="862be-137">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="862be-138">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="862be-138">Click Add.</span></span>
    * <span data-ttu-id="862be-139">Вы можете добавить поставщика в категорию закупаемой продукции и указать, является ли поставщик предпочтительным для этой категории или просто утвержденным для нее.</span><span class="sxs-lookup"><span data-stu-id="862be-139">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="862be-140">При удалении поставщика из категории исторические проводки по поставщику в категории не удаляются.</span><span class="sxs-lookup"><span data-stu-id="862be-140">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="862be-141">Найдите поставщика, которого требуется добавить в категорию.</span><span class="sxs-lookup"><span data-stu-id="862be-141">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="862be-142">Щелкните стрелку, чтобы выбрать поставщика.</span><span class="sxs-lookup"><span data-stu-id="862be-142">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="862be-143">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="862be-143">Click OK.</span></span>
6. <span data-ttu-id="862be-144">Выберите строку поставщика, которого необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="862be-144">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="862be-145">В поле "Статус поставщика" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="862be-145">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="862be-146">Параметр выбора поставщика в правиле политики категорий управляет тем, какие поставщики доступны в заявках на покупку — предпочтительные, утвержденные или все.</span><span class="sxs-lookup"><span data-stu-id="862be-146">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="862be-147">Добавление в категорию дополнительной информации</span><span class="sxs-lookup"><span data-stu-id="862be-147">Add additional information to the category</span></span>
1. <span data-ttu-id="862be-148">Переключите развертывание раздела "Выбор групп критериев оценки поставщика".</span><span class="sxs-lookup"><span data-stu-id="862be-148">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="862be-149">Эта вкладка позволяет определить критерии, по которым должны оцениваться поставщики в категории закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="862be-149">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="862be-150">Чтобы это сделать, нужно щелкнуть "Добавить", а затем выбрать группу оценки поставщиков, содержащую требуемые критерии.</span><span class="sxs-lookup"><span data-stu-id="862be-150">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="862be-151">Переключите развертывание раздела "Анкеты".</span><span class="sxs-lookup"><span data-stu-id="862be-151">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="862be-152">Эта вкладка позволяет добавить анкеты, которые будут присутствовать на заявке, если тип операций установлен в значение "Заявка".</span><span class="sxs-lookup"><span data-stu-id="862be-152">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="862be-153">В этом случае инициатор запроса должен будет заполнить анкету, прежде чем отправлять заявку на определенный продукт или продукты в категории закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="862be-153">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="862be-154">Переключите развертывание раздела "Налоговые группы номенклатур".</span><span class="sxs-lookup"><span data-stu-id="862be-154">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="862be-155">В поле "Налоговая группа номенклатур" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="862be-155">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="862be-156">Выбор налоговой группы.</span><span class="sxs-lookup"><span data-stu-id="862be-156">Select a sales tax group.</span></span>
6. <span data-ttu-id="862be-157">Переключите развертывание раздела "Страница категории".</span><span class="sxs-lookup"><span data-stu-id="862be-157">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="862be-158">Страницы категорий создаются на странице "Иерархия категорий".</span><span class="sxs-lookup"><span data-stu-id="862be-158">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="862be-159">Они содержат информацию о категории закупаемой продукции, например информацию о типе продуктов в категории, изображения продуктов в категории или объявления, например, о скидках в категории.</span><span class="sxs-lookup"><span data-stu-id="862be-159">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="862be-160">Информация на странице категории отображается в заявках на покупку.</span><span class="sxs-lookup"><span data-stu-id="862be-160">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="862be-161">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="862be-161">Close the page.</span></span>


