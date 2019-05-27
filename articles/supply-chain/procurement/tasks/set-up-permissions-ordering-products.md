---
title: Настройка разрешений на заказ продуктов от имени другого сотрудника
description: В этой процедуре показано, как предоставить работникам разрешение на подготовку заявок на покупку от имени других работников.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35688d191cef06cc15251a6e10a2e8c9afb0e08b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571871"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="5ee57-103">Настройка разрешений на заказ продуктов от имени другого сотрудника</span><span class="sxs-lookup"><span data-stu-id="5ee57-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5ee57-104">В этой процедуре показано, как предоставить работникам разрешение на подготовку заявок на покупку от имени других работников.</span><span class="sxs-lookup"><span data-stu-id="5ee57-104">This procedure shows how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="5ee57-105">Другими словами, "составитель" заявки на покупку может создать заявку для другого "инициатора запроса".</span><span class="sxs-lookup"><span data-stu-id="5ee57-105">In other words, a purchase requisition “preparer” can create a requisition for another “requester.”</span></span> <span data-ttu-id="5ee57-106">В этой процедуре показано, как предоставить работнику разрешение на заказ номенклатур и услуг в различных юридических лицах или операционных единицах.</span><span class="sxs-lookup"><span data-stu-id="5ee57-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="5ee57-107">Обычно эти задачи выполняет менеджер по закупкам.</span><span class="sxs-lookup"><span data-stu-id="5ee57-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="5ee57-108">Чтобы выполнить эту процедуру, можно использовать компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="5ee57-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="5ee57-109">Предоставление разрешения на ввод заявок на покупку от имени другого работника</span><span class="sxs-lookup"><span data-stu-id="5ee57-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="5ee57-110">Перейдите в раздел "Закупки и источники" > "Настройка" > "Политики" > "Разрешения для заявок на покупку".</span><span class="sxs-lookup"><span data-stu-id="5ee57-110">Go to Procurement and sourcing > Setup > Policies > Purchase requisition permissions.</span></span>
    * <span data-ttu-id="5ee57-111">Убедитесь, что в поле "Текущее представление" выбрано значение "По составителю".</span><span class="sxs-lookup"><span data-stu-id="5ee57-111">Make sure that the Current view field is set to By preparer.</span></span>  <span data-ttu-id="5ee57-112">В списке в левой области отображаются лица, которым может быть предоставлено разрешение на подготовку заявок от имени других лиц.</span><span class="sxs-lookup"><span data-stu-id="5ee57-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="5ee57-113">Выберите лицо, которому требуется предоставить разрешение (составитель).</span><span class="sxs-lookup"><span data-stu-id="5ee57-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="5ee57-114">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5ee57-114">Click Add.</span></span>
4. <span data-ttu-id="5ee57-115">Найдите и выберите лицо, которого требуется добавить как инициатора запроса.</span><span class="sxs-lookup"><span data-stu-id="5ee57-115">Find and select the person to add as a requester.</span></span>
    * <span data-ttu-id="5ee57-116">Инициатор запроса — это лицо, от имени которого составитель может создавать заявки.</span><span class="sxs-lookup"><span data-stu-id="5ee57-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    * <span data-ttu-id="5ee57-117">В поле "Авторизация" выберите "Специальные настройки", если пользователь должен иметь возможность создавать заявки на покупку от имени выбранного работника.</span><span class="sxs-lookup"><span data-stu-id="5ee57-117">In the Authorization field, select Specific if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="5ee57-118">Выберите "Отчетность", если составитель также должен иметь возможность создавать заявки на покупку от имени всех работников, которые подотчетны данному работнику.</span><span class="sxs-lookup"><span data-stu-id="5ee57-118">Select Reporting if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="5ee57-119">В моле "Действует" введите дату.</span><span class="sxs-lookup"><span data-stu-id="5ee57-119">In the Effective field, enter a date.</span></span>
6. <span data-ttu-id="5ee57-120">В поле "Истечение срока" введите дату.</span><span class="sxs-lookup"><span data-stu-id="5ee57-120">In the Expiration field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="5ee57-121">Просмотр составителей, которые имеют разрешение на создание заявок на покупку от имени выбранного работника</span><span class="sxs-lookup"><span data-stu-id="5ee57-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="5ee57-122">В поле "Текущее представление" выберите "По инициатору запроса".</span><span class="sxs-lookup"><span data-stu-id="5ee57-122">In the Current view field, select 'By requester'.</span></span>
    * <span data-ttu-id="5ee57-123">В этом представлении отображается список составителей, которым выдано разрешение на создание заявок на покупку от имени выбранного работника.</span><span class="sxs-lookup"><span data-stu-id="5ee57-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="5ee57-124">Используйте экспресс-фильтр для поиска работника, добавленного как инициатор запроса.</span><span class="sxs-lookup"><span data-stu-id="5ee57-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="5ee57-125">Выберите инициатора запроса.</span><span class="sxs-lookup"><span data-stu-id="5ee57-125">Select the requester.</span></span>
    * <span data-ttu-id="5ee57-126">В списке составителей отображаются лица, имеющие разрешение на заказ номенклатур от имени инициатора запроса, выбранного в левой области.</span><span class="sxs-lookup"><span data-stu-id="5ee57-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>   <span data-ttu-id="5ee57-127">Здесь можно добавить дополнительных составителей.</span><span class="sxs-lookup"><span data-stu-id="5ee57-127">You can add additional preparers here.</span></span>   <span data-ttu-id="5ee57-128">Это представление также позволяет предоставить инициатору запроса разрешение на создание заявок в юридических лицах и операционных единицах, которые не являются основными операционными единицами или юридическим лицом этого лица.</span><span class="sxs-lookup"><span data-stu-id="5ee57-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  

