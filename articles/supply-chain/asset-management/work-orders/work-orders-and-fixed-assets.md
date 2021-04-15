---
title: Заказы на работу и основные средства
description: В этом разделе рассматриваются заказы на работу и основные средства в модуле "Управление активами".
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 65adcd07f1649b2e4eb2e2528507bb15631782ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816732"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="4d76e-103">Заказы на работу и основные средства</span><span class="sxs-lookup"><span data-stu-id="4d76e-103">Work orders and fixed assets</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="4d76e-104">В управлении активами активы могут быть связаны с основными средствами, и для этих активов можно создавать заказы на работу.</span><span class="sxs-lookup"><span data-stu-id="4d76e-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="4d76e-105">Если вы используете эту функцию, вы можете получить полный обзор основных средств, соответствующих инвестиционных проектов и затрат, зарегистрированных для инвестиционных проектов, в модуле **Управление и учет по проектам** и в модуле **Основные средства** в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4d76e-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs that are registered on the investment projects in the **Project management and accounting** and **Fixed assets** modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="4d76e-106">Поле **Номер ОС** задается в проекте задания по заказу на работу только в том случае, если в качестве типа проекта в проекте задания по заказу на работу выбран тип **Инвестиция**.</span><span class="sxs-lookup"><span data-stu-id="4d76e-106">The **Fixed asset number** field on the work order job project is set only if **Investment** is selected as the project type on the work order job project.</span></span>

<span data-ttu-id="4d76e-107">На приведенном ниже рисунке показана связь между инвестиционным проектом в модуле **Управление и учет по проектам** и проектом "Задание заказа на работу".</span><span class="sxs-lookup"><span data-stu-id="4d76e-107">The illustration below shows the relation between an investment project in the **Project management and accounting** module and a work order job project.</span></span>

![Рисунок 1](media/24-work-orders.png)

<span data-ttu-id="4d76e-109">Следующая процедура описывает связь между активами, заказами на работу, проектами заданий заказов на работу и основными средствами.</span><span class="sxs-lookup"><span data-stu-id="4d76e-109">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="4d76e-110">Вы создаете актив, который вы связываете с основными средствами.</span><span class="sxs-lookup"><span data-stu-id="4d76e-110">You create an asset that you relate to a fixed asset.</span></span>

![Рисунок 2](media/25-work-orders.png)

2. <span data-ttu-id="4d76e-112">При настройке типов заказов на работу на странице **Типы заказов на работу**(**Управление активами** > **Настройка** > **Заказы на работу** > **Типы заказов на работу**) создается тип заказа на работу для обработки инвестиций.</span><span class="sxs-lookup"><span data-stu-id="4d76e-112">When you set up work order types on the **Work order types** page (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="4d76e-113">См. также [Типы заказов на работу](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="4d76e-113">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![Рисунок 3](media/26-work-orders.png)

3. <span data-ttu-id="4d76e-115">При настройке групп проектов заказов на работу на вкладке **Группа проектов** страницы **Настройка заказа на работу по проекту** (**Управление активами** > **Настройка** > **Заказы на работу** > **Настройка проекта**) создается связь между типом заказа на работу, используемым для инвестиций, и группой проектов, созданной для инвестиций на странице **Группы проектов** в модуле **Управление и учет по проектам** (**Управление и учет по проектам** > **Настройка** > **Разноска** > **Группы проектов**).</span><span class="sxs-lookup"><span data-stu-id="4d76e-115">When you set up work order project groups on the **Project group** tab of the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**), you create a relation between the work order type that is used for investments and the project group that was created for investments on the **Project groups** page in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![Рисунок 4](media/27-work-orders.png)

4. <span data-ttu-id="4d76e-117">При создании заказа на работу, связанного с основных средств, следует выбрать тип заказа на работу, используемый для обработки инвестиций, например, **Инвестиции**.</span><span class="sxs-lookup"><span data-stu-id="4d76e-117">When you create a work order that is related to a fixed asset, you select the work order type that is used to handle investments, such as **Investment**.</span></span>

5. <span data-ttu-id="4d76e-118">При создании заказа на работу связанный тип заказа на работу отображается на странице **Все заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="4d76e-118">When the work order is created, the related work order type is shown on the **All work orders** page.</span></span>

![Рисунок 5](media/28-work-orders.png)

6. <span data-ttu-id="4d76e-120">При создании заказа на работу проект, связанный с этим заказом на работу, создается на странице **Все проекты** в модуле **Управление и учет по проектам** (**Управление и учет по проектам** > **Проекты** > **Все проекты**).</span><span class="sxs-lookup"><span data-stu-id="4d76e-120">When the work order is created, the project that is related to the work order is created on the **All projects** page in the **Project management and accounting** module (**Project management and accounting** > **Projects** > **All projects**).</span></span> <span data-ttu-id="4d76e-121">Чтобы просмотреть сведения, связанные с проектом, выберите ссылку в поле **код проекта** на вкладке **Общие** на экспресс-вкладке **Сведения по строке** в представление сведений на странице **все заказы на работу** в модуле **Управление активами** (**Управление активами** > **Общие** > **Заказы на работу** > **Все заказы на работу**).</span><span class="sxs-lookup"><span data-stu-id="4d76e-121">To view project-related information, select the link in the **Project ID** field on the **General** tab on the **Line details** FastTab in the details view of the **All work orders** page in the **Asset management** module (**Asset management** > **Commom** > **Work orders** > **All work orders**).</span></span>

![Рисунок 6](media/29-work-orders.png)

7. <span data-ttu-id="4d76e-123">Чтобы просмотреть обзор проектов, связанных с основными средствами, выберите **Основные средства** > **Основные средства** > **Основные средства**, а затем в поле **Номер ОС** выберите ссылку для ОС, чтобы открыть подробное представление.</span><span class="sxs-lookup"><span data-stu-id="4d76e-123">To see an overview of the projects associated with a fixed asset, select **Fixed assets** > **Fixed assets** > **Fixed assets**, and then, in the **Fixed asset number** field, select the link for the fixed asset to open the details view.</span></span> <span data-ttu-id="4d76e-124">Разверните панель **Связанные сведения** в правой части страницы и выберите экспресс-вкладку **связанные проекты**.</span><span class="sxs-lookup"><span data-stu-id="4d76e-124">Expand the **Related information** pane on the right side of the page, and select the **Associated projects** FastTab.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]