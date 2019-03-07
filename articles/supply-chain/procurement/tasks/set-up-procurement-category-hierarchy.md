---
title: Настройка иерархии категорий закупаемой продукции
description: В этой процедуре показано, как создавать новые узлы в иерархии категорий закупаемой продукции, а также как настроить категорию закупаемой продукции для использования в процессе закупки.
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01809a8a3256342682d8a9cfb296a355310fe4ed
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "334527"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="ad907-103">Настройка иерархии категорий закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="ad907-103">Set up a procurement category hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ad907-104">В этой процедуре показано, как создавать новые узлы в иерархии категорий закупаемой продукции, а также как настроить категорию закупаемой продукции для использования в процессе закупки.</span><span class="sxs-lookup"><span data-stu-id="ad907-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="ad907-105">Эти задачи обычно выполняются менеджером по закупкам.</span><span class="sxs-lookup"><span data-stu-id="ad907-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="ad907-106">Для начала этой процедуры должна существовать иерархия категорий закупаемой продукции типа "Закупка".</span><span class="sxs-lookup"><span data-stu-id="ad907-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="ad907-107">При использовании компании демонстрационных данных эту процедуру можно выполнять в компании USMF.</span><span class="sxs-lookup"><span data-stu-id="ad907-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="ad907-108">Добавление новой категории закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="ad907-108">Add a new procurement category</span></span>
1. <span data-ttu-id="ad907-109">Перейдите в раздел "Закупки и источники" > "Категории закупаемой продукции".</span><span class="sxs-lookup"><span data-stu-id="ad907-109">Go to Procurement and sourcing > Procurement categories.</span></span>
2. <span data-ttu-id="ad907-110">Щелкните "Изменить иерархию категорий".</span><span class="sxs-lookup"><span data-stu-id="ad907-110">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="ad907-111">Текущая иерархия категорий закупаемой продукции отображается в левой части страницы.</span><span class="sxs-lookup"><span data-stu-id="ad907-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="ad907-112">Вам предстоит внести изменения в эту иерархию.</span><span class="sxs-lookup"><span data-stu-id="ad907-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="ad907-113">Щелкните "Новый узел категории".</span><span class="sxs-lookup"><span data-stu-id="ad907-113">Click New category node.</span></span>
    * <span data-ttu-id="ad907-114">Система по умолчанию выбирает верхний узел.</span><span class="sxs-lookup"><span data-stu-id="ad907-114">The system selects the top node by default.</span></span> <span data-ttu-id="ad907-115">Если вы выполняете эту процедуру как руководство по задаче, вы можете нажать кнопку "Разблокировать" и выбрать для вставки нового узла другой родительский узел.</span><span class="sxs-lookup"><span data-stu-id="ad907-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="ad907-116">После этого снова заблокируйте руководство по задаче и щелкните "Новый узел категории".</span><span class="sxs-lookup"><span data-stu-id="ad907-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="ad907-117">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ad907-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ad907-118">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ad907-118">In the Description field, type a value.</span></span>
6. <span data-ttu-id="ad907-119">В поле "Понятное имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ad907-119">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="ad907-120">Понятное имя указывать необязательно.</span><span class="sxs-lookup"><span data-stu-id="ad907-120">The friendly name is optional.</span></span> <span data-ttu-id="ad907-121">Оно будет отображаться в поисках категорий вместе с именем категории.</span><span class="sxs-lookup"><span data-stu-id="ad907-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="ad907-122">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="ad907-122">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="ad907-123">Добавление продуктов в новую категорию закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="ad907-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="ad907-124">Перейдите в раздел "Закупки и источники" > "Категории закупаемой продукции".</span><span class="sxs-lookup"><span data-stu-id="ad907-124">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="ad907-125">Выберите только что добавленный узел.</span><span class="sxs-lookup"><span data-stu-id="ad907-125">Select the node you just added.</span></span> <span data-ttu-id="ad907-126">Если вы выполняете эту процедуру как руководство по задаче, вам может потребоваться разблокировать руководство по задаче, чтобы выбрать узел.</span><span class="sxs-lookup"><span data-stu-id="ad907-126">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="ad907-127">Переключите развертывание раздела "Продукты".</span><span class="sxs-lookup"><span data-stu-id="ad907-127">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="ad907-128">Щелкните "Добавить", чтобы связать продукты с категорией закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="ad907-128">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="ad907-129">Выберите карточку продукта, которую требуется добавить в категорию закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="ad907-129">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="ad907-130">Щелкните стрелку, чтобы выбрать продукт.</span><span class="sxs-lookup"><span data-stu-id="ad907-130">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="ad907-131">Выберите еще один продукт для добавления в категорию закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="ad907-131">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="ad907-132">Щелкните стрелку, чтобы выбрать продукт.</span><span class="sxs-lookup"><span data-stu-id="ad907-132">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="ad907-133">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ad907-133">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="ad907-134">Добавление утвержденных и предпочтительных поставщиков</span><span class="sxs-lookup"><span data-stu-id="ad907-134">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="ad907-135">Переключите развертывание раздела "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="ad907-135">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="ad907-136">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="ad907-136">Click Add.</span></span>
    * <span data-ttu-id="ad907-137">Вы можете добавить поставщика в категорию закупаемой продукции и указать, является ли поставщик предпочтительным для этой категории или просто утвержденным для нее.</span><span class="sxs-lookup"><span data-stu-id="ad907-137">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="ad907-138">При удалении поставщика из категории исторические проводки по поставщику в категории не удаляются.</span><span class="sxs-lookup"><span data-stu-id="ad907-138">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="ad907-139">Найдите поставщика, которого требуется добавить в категорию.</span><span class="sxs-lookup"><span data-stu-id="ad907-139">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="ad907-140">Щелкните стрелку, чтобы выбрать поставщика.</span><span class="sxs-lookup"><span data-stu-id="ad907-140">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="ad907-141">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="ad907-141">Click OK.</span></span>
6. <span data-ttu-id="ad907-142">Выберите строку поставщика, которого необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="ad907-142">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="ad907-143">В поле "Статус поставщика" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="ad907-143">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="ad907-144">Параметр выбора поставщика в правиле политики категорий управляет тем, какие поставщики доступны в заявках на покупку — предпочтительные, утвержденные или все.</span><span class="sxs-lookup"><span data-stu-id="ad907-144">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="ad907-145">Добавление в категорию дополнительной информации</span><span class="sxs-lookup"><span data-stu-id="ad907-145">Add additional information to the category</span></span>
1. <span data-ttu-id="ad907-146">Переключите развертывание раздела "Выбор групп критериев оценки поставщика".</span><span class="sxs-lookup"><span data-stu-id="ad907-146">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="ad907-147">Эта вкладка позволяет определить критерии, по которым должны оцениваться поставщики в категории закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="ad907-147">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="ad907-148">Чтобы это сделать, нужно щелкнуть "Добавить", а затем выбрать группу оценки поставщиков, содержащую требуемые критерии.</span><span class="sxs-lookup"><span data-stu-id="ad907-148">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="ad907-149">Переключите развертывание раздела "Анкеты".</span><span class="sxs-lookup"><span data-stu-id="ad907-149">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="ad907-150">Эта вкладка позволяет добавить анкеты, которые будут присутствовать на заявке, если тип операций установлен в значение "Заявка".</span><span class="sxs-lookup"><span data-stu-id="ad907-150">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="ad907-151">В этом случае инициатор запроса должен будет заполнить анкету, прежде чем отправлять заявку на определенный продукт или продукты в категории закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="ad907-151">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="ad907-152">Переключите развертывание раздела "Налоговые группы номенклатур".</span><span class="sxs-lookup"><span data-stu-id="ad907-152">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="ad907-153">В поле "Налоговая группа номенклатур" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="ad907-153">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ad907-154">Выбор налоговой группы.</span><span class="sxs-lookup"><span data-stu-id="ad907-154">Select a sales tax group.</span></span>
6. <span data-ttu-id="ad907-155">Переключите развертывание раздела "Страница категории".</span><span class="sxs-lookup"><span data-stu-id="ad907-155">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="ad907-156">Страницы категорий создаются на странице "Иерархия категорий".</span><span class="sxs-lookup"><span data-stu-id="ad907-156">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="ad907-157">Они содержат информацию о категории закупаемой продукции, например информацию о типе продуктов в категории, изображения продуктов в категории или объявления, например, о скидках в категории.</span><span class="sxs-lookup"><span data-stu-id="ad907-157">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="ad907-158">Информация на странице категории отображается в заявках на покупку.</span><span class="sxs-lookup"><span data-stu-id="ad907-158">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="ad907-159">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ad907-159">Close the page.</span></span>

