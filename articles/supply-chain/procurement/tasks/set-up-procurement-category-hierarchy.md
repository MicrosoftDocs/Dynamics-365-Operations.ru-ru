---
title: Настройка иерархии категорий закупаемой продукции
description: В этой процедуре показано, как создавать новые узлы в иерархии категорий закупаемой продукции, а также как настроить категорию закупаемой продукции для использования в процессе закупки.
author: mkirknel
manager: AnnBe
ms.date: 06/21/2019
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
ms.openlocfilehash: d7010a1c612b9b3884c675f578657d951da06c38
ms.sourcegitcommit: 25fe679b73663fda6b5b3c32646026d0993a9f00
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/12/2019
ms.locfileid: "1995290"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="9c488-103">Настройка иерархии категорий закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="9c488-103">Set up a procurement category hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9c488-104">В этой процедуре показано, как создавать новые узлы в иерархии категорий закупаемой продукции, а также как настроить категорию закупаемой продукции для использования в процессе закупки.</span><span class="sxs-lookup"><span data-stu-id="9c488-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="9c488-105">Эти задачи обычно выполняются менеджером по закупкам.</span><span class="sxs-lookup"><span data-stu-id="9c488-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="9c488-106">Для начала этой процедуры должна существовать иерархия категорий закупаемой продукции типа "Закупка".</span><span class="sxs-lookup"><span data-stu-id="9c488-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="9c488-107">При использовании компании демонстрационных данных эту процедуру можно выполнять в компании USMF.</span><span class="sxs-lookup"><span data-stu-id="9c488-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="9c488-108">Добавление новой категории закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="9c488-108">Add a new procurement category</span></span>
1. <span data-ttu-id="9c488-109">Выберите **Область переходов > Модули > Закупки и источники > Коносамент > Категории закупаемой продукции**.</span><span class="sxs-lookup"><span data-stu-id="9c488-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="9c488-110">На панели операций выберите **Изменить иерархию категорий**.</span><span class="sxs-lookup"><span data-stu-id="9c488-110">On the action pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="9c488-111">Текущая иерархия категорий закупаемой продукции отображается в левой части страницы.</span><span class="sxs-lookup"><span data-stu-id="9c488-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="9c488-112">Вам предстоит внести изменения в эту иерархию.</span><span class="sxs-lookup"><span data-stu-id="9c488-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="9c488-113">На панели операций выберите **Новый узел категории**.</span><span class="sxs-lookup"><span data-stu-id="9c488-113">On the action pane, select **New category node**.</span></span> <span data-ttu-id="9c488-114">Система по умолчанию выбирает верхний узел.</span><span class="sxs-lookup"><span data-stu-id="9c488-114">The system selects the top node by default.</span></span> <span data-ttu-id="9c488-115">Если вы выполняете эту процедуру как руководство по задаче, вы можете нажать кнопку "Разблокировать" и выбрать для вставки нового узла другой родительский узел.</span><span class="sxs-lookup"><span data-stu-id="9c488-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="9c488-116">После этого снова заблокируйте руководство по задаче и щелкните "Новый узел категории".</span><span class="sxs-lookup"><span data-stu-id="9c488-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="9c488-117">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9c488-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="9c488-118">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9c488-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="9c488-119">В поле **Понятное имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9c488-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="9c488-120">Понятное имя указывать необязательно.</span><span class="sxs-lookup"><span data-stu-id="9c488-120">The friendly name is optional.</span></span> <span data-ttu-id="9c488-121">Оно будет отображаться в поисках категорий вместе с именем категории.</span><span class="sxs-lookup"><span data-stu-id="9c488-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="9c488-122">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="9c488-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="9c488-123">Добавление продуктов в новую категорию закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="9c488-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="9c488-124">Перейдите в раздел **Закупки и источники > Коносамент > Категории закупаемой продукции**.</span><span class="sxs-lookup"><span data-stu-id="9c488-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="9c488-125">Выберите только что добавленный узел.</span><span class="sxs-lookup"><span data-stu-id="9c488-125">Select the node you just added.</span></span> <span data-ttu-id="9c488-126">Если вы выполняете эту процедуру как руководство по задаче, вам может потребоваться разблокировать руководство по задаче, чтобы выбрать узел.</span><span class="sxs-lookup"><span data-stu-id="9c488-126">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="9c488-127">Переключите развертывание раздела **Продукты**.</span><span class="sxs-lookup"><span data-stu-id="9c488-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="9c488-128">Щелкните **Добавить**, чтобы связать продукты с категорией закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="9c488-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="9c488-129">Выберите продукт, которую требуется добавить в категорию закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="9c488-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="9c488-130">Выберите стрелку для добавления продукта в таблицу **Выбрано**.</span><span class="sxs-lookup"><span data-stu-id="9c488-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="9c488-131">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9c488-131">Select **OK**.</span></span>
