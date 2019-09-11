---
title: Заказы на работу и основные средства
description: В этом разделе рассматриваются заказы на работу и основные средства в модуле "Управление активами".
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f03b7fa073c4e5338b7b5681ba7b8c9fe00a657b
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875855"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="c4380-103">Заказы на работу и основные средства</span><span class="sxs-lookup"><span data-stu-id="c4380-103">Work orders and fixed assets</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="c4380-104">В управлении активами активы могут быть связаны с основными средствами, и для этих активов можно создавать заказы на работу.</span><span class="sxs-lookup"><span data-stu-id="c4380-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="c4380-105">Если вы используете эту функцию, вы можете получить полный обзор основных средств, соответствующих инвестиционных проектов и затрат, зарегистрированных для инвестиционных проектов, в модуле **Управление и учет по проектам** и в модуле **Основные средства** в Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c4380-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs registered on the investment projects in the **Project management and accounting** module and the **Fixed assets** module in Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="c4380-106">Поле **Инвентарный номер ОС** заполняется в проекте задания по заказу на работу только в том случае, если в качестве типа проекта в проекте задания по заказу на работу выбран тип "Инвестиция".</span><span class="sxs-lookup"><span data-stu-id="c4380-106">The **Fixed asset number** field is only filled out on the work order job project if type "Investment" is selected as the project type on the work order job project.</span></span>

![Рисунок 1](media/24-work-orders.png)

<span data-ttu-id="c4380-108">Следующая процедура описывает связь между активами, заказами на работу, проектами заданий заказов на работу и основными средствами.</span><span class="sxs-lookup"><span data-stu-id="c4380-108">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="c4380-109">Вы создаете актив, которые вы связываете с основным средством, как показано на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="c4380-109">You create an asset that you relate to a fixed asset, as shown in the figure below.</span></span>

![Рисунок 2](media/25-work-orders.png)

2. <span data-ttu-id="c4380-111">При настройке типов заказов на работу (**Управление активами** > **Настройка** > **Заказы на работу** > **Типы заказов на работу**) создается тип заказа на работу для обработки инвестиций.</span><span class="sxs-lookup"><span data-stu-id="c4380-111">When you set up work order types (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="c4380-112">См. также [Типы заказов на работу](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="c4380-112">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![Рисунок 3](media/26-work-orders.png)

3. <span data-ttu-id="c4380-114">При настройке групп проектов заказов на работу (**Управление активами** > **Настройка** > **Заказы на работу** > **Настройка проекта** > ссылка **Группа проектов**) создается связь между типом заказа на работу, используемым для инвестиций, и группой проектов, созданной для инвестиций в модуле **Управление и учет по проектам** (**Управление и учет по проектам** > **Настройка** > **Разноска** > **Группы проектов**).</span><span class="sxs-lookup"><span data-stu-id="c4380-114">When you set up work order project groups (**Asset management** > **Setup** > **Work orders** > **Project setup** > **Project group** link), you create a relation between the work order type used for investments and the project group created for investments in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![Рисунок 4](media/27-work-orders.png)

4. <span data-ttu-id="c4380-116">При создании заказа на работу, связанного с объектом основных средств, следует выбрать тип рабочего заказа, используемый для обработки инвестиций, например, "Инвестиции".</span><span class="sxs-lookup"><span data-stu-id="c4380-116">When you create a work order that relates to a fixed asset object, you select the work order type used for handling investments, for example, "Investment".</span></span>

5. <span data-ttu-id="c4380-117">При создании заказа на работу связанный тип заказа на работу отображается в разделе **Все заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="c4380-117">When the work order is created, the related work order type is shown in **All work orders**.</span></span>

![Рисунок 5](media/28-work-orders.png)

6. <span data-ttu-id="c4380-119">При создании заказа на работу проект, связанный с этим заказом на работу, создается в модуле **Управление и учет по проектам** > **Все проекты**.</span><span class="sxs-lookup"><span data-stu-id="c4380-119">When the work order is created, the project related to the work order is created in **Project management and accounting** > **All projects**.</span></span> <span data-ttu-id="c4380-120">Можно просмотреть связанные с проектом сведения, щелкнув ссылку **Код проекта** в заказе на работу (в модуле **Управление активами** откройте заказ на работу в представлении сведений > экспресс-вкладку **Сведения по строке** > вкладку **Общие** > поле **Код проекта**).</span><span class="sxs-lookup"><span data-stu-id="c4380-120">You can see project-related information by clicking the **Project ID** link on the work order (in **Asset management**, open the work order in Details view > **Line details** FastTab > **General** tab > **Project ID** field).</span></span>

![Рисунок 6](media/29-work-orders.png)

7. <span data-ttu-id="c4380-122">В разделе **Основные средства** можно просмотреть обзор проектов, связанных с основными средствами (**Основные средства** > **Основные средства** > **Основные средства** щелкните основное средство в поле **Инвентарный номер ОС** > просмотрите содержимое области **Связанные сведения** > раздел **Связанные проекты**).</span><span class="sxs-lookup"><span data-stu-id="c4380-122">In **Fixed assets**, you are able to see an overview of the projects associated with a fixed asset (**Fixed assets** > **Fixed assets** > **Fixed assets** > click on the fixed asset in the **Fixed asset number** field > view the contents in the **Related information** pane > **Associated projects** section).</span></span>

