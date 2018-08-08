---
title: "Создание заказов на обслуживание вручную"
description: "Заказы на обслуживание можно создавать вручную, используя соглашения на сервисное обслуживание или форму **Заказы на сервисное обслуживание**."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 9fbcdaa50a8f13247c13c1885cdb4ab7f5f39a47
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---

# <a name="create-service-orders-manually"></a><span data-ttu-id="143f9-103">Создание заказов на обслуживание вручную</span><span class="sxs-lookup"><span data-stu-id="143f9-103">Create service orders manually</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="143f9-104">Заказы на обслуживание можно создавать вручную, используя соглашения на сервисное обслуживание или форму **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="143f9-104">You can create service orders manually by using a service agreement or by using the **Service orders** form.</span></span> <span data-ttu-id="143f9-105">Заказ на обслуживание можно создать и из проекта.</span><span class="sxs-lookup"><span data-stu-id="143f9-105">You can also create a service order from a project.</span></span>

> [!TIP]
> <P><span data-ttu-id="143f9-106">Можно использовать автоматизированные процессы для создания заказов на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="143f9-106">You can use automated processes to create service orders.</span></span> 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a><span data-ttu-id="143f9-107">Создание заказа на сервисное обслуживание вручную из соглашения о сервисном обслуживании</span><span class="sxs-lookup"><span data-stu-id="143f9-107">Create a service order manually from a service agreement</span></span>

1.  <span data-ttu-id="143f9-108">Щелкните **Управление сервисным обслуживанием** \> **Общее** \> **Соглашения на обслуживание** \> **Соглашения на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="143f9-108">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="143f9-109">Выберите уже существующее соглашение на обслуживание или создайте новое.</span><span class="sxs-lookup"><span data-stu-id="143f9-109">Select a service agreement or create a new service agreement.</span></span>

3.  <span data-ttu-id="143f9-110">Перейдите на вкладку **Доставлять** и в группе **Создать** щелкните **Планируемые заказы на обслуживание**, чтобы открыть форму **Создать заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="143f9-110">Click the **Deliver** tab and in the **Create** group click **Planned service orders** to open the **Create service orders** form.</span></span>

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a><span data-ttu-id="143f9-111">Создание заказа на обслуживание вручную из формы "Заказы на обслуживание"</span><span class="sxs-lookup"><span data-stu-id="143f9-111">Create a service order manually in the Service orders form</span></span>

1.  <span data-ttu-id="143f9-112">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Заказы на сервисное обслуживание** \> **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="143f9-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="143f9-113">Нажмите комбинацию клавиш Ctrl+N, чтобы создать новый заказ на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="143f9-113">Press Ctrl+N to create a new service order.</span></span>

3.  <span data-ttu-id="143f9-114">Создайте строки заказа на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="143f9-114">Create service order lines for the service order.</span></span>

> [!NOTE]
> <P><span data-ttu-id="143f9-115">Если в форме <STRONG>Параметры управления сервисным обслуживанием</STRONG> установлен флажок <STRONG>Разрешить без соглашения о сервисном обслуживании</STRONG>, разноску проводок из строк заказа на обслуживание можно выполнять и не присоединяя заказ на обслуживание к соглашению на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="143f9-115">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="143f9-116">Если этот флажок снят, до выполнения разноски строк заказа на обслуживание необходимо присоединить созданный вручную заказ на облуживание к проекту.</span><span class="sxs-lookup"><span data-stu-id="143f9-116">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-a-project"></a><span data-ttu-id="143f9-117">Создание заказа на сервисное обслуживание из проекта</span><span class="sxs-lookup"><span data-stu-id="143f9-117">Create a service order from a project</span></span>

1.  <span data-ttu-id="143f9-118">Щелкните **Управление и учет по проектам** \> **Общее** \> **Проекты** \> **Все проекты**.</span><span class="sxs-lookup"><span data-stu-id="143f9-118">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="143f9-119">В форме **Проекты** в разделе **Панель операций** перейдите на вкладку **Панель операций** \> щелкните **Обслуживание** \> **Заказы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="143f9-119">In the **Projects** form, on the **Action pane**, click the **Manage** tab \> click **Service** \> **Service orders**.</span></span>

3.  <span data-ttu-id="143f9-120">Выполните предыдущую процедуру для создания заказа на обслуживание вручную в форме **Заказы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="143f9-120">Follow the previous procedure to create a service order manually in the **Service orders** form.</span></span> <span data-ttu-id="143f9-121">В поле **Код проекта** отображается ссылка на проект.</span><span class="sxs-lookup"><span data-stu-id="143f9-121">The **Project ID** field displays the project reference.</span></span>

> [!NOTE]
> <P><span data-ttu-id="143f9-122">Если в форме <STRONG>Параметры управления сервисным обслуживанием</STRONG> установлен флажок <STRONG>Разрешить без соглашения о сервисном обслуживании</STRONG>, разноску проводок из строк заказа на обслуживание можно выполнять и не присоединяя заказ на обслуживание к соглашению на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="143f9-122">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="143f9-123">Если этот флажок снят, до выполнения разноски строк заказа на обслуживание необходимо присоединить созданный вручную заказ на облуживание к проекту.</span><span class="sxs-lookup"><span data-stu-id="143f9-123">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-the-sales-order-form"></a><span data-ttu-id="143f9-124">Создание заказа на сервисное обслуживание из формы заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="143f9-124">Create a service order from the Sales order form</span></span>

<span data-ttu-id="143f9-125">Можно создать заказ на сервисное обслуживание из формы **Заказы на продажу** с помощью мастера **Создать новый заказ на обслуживание на основе заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="143f9-125">You can create a service order from the **Sales orders** form by using the **Create a new service order based on the sales order** wizard.</span></span>

1.  <span data-ttu-id="143f9-126">Выберите **Продажи и маркетинг** \> **Общее** \> **Заказы на продажу** \> **Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="143f9-126">Click **Sales and marketing** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="143f9-127">Откройте соответствующий заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="143f9-127">Open the relevant sales order.</span></span>

3.  <span data-ttu-id="143f9-128">На вкладке **Заказ на продажу** щелкните **Заказ на обслуживание**, чтобы запустить мастер **Создать новый заказ на обслуживание на основе заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="143f9-128">On the **Sales order** tab, click **Service order** to start the **Create a new service order based on the sales order** wizard.</span></span>

4.  <span data-ttu-id="143f9-129">Щелкните **Далее \>** и выполните следующие шаги на странице **Выбрать соглашение для заказа на обслуживание**:</span><span class="sxs-lookup"><span data-stu-id="143f9-129">Click **Next \>**, and then complete the following steps on the **Select agreement for service order** page:</span></span>
    
      - <span data-ttu-id="143f9-130">Используйте поле **Соглашение о сервисном обслуживании** для выбора соглашения о сервисном обслуживании, с которым будет связан новый заказ на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="143f9-130">Use the **Service agreement** field to select the service agreement with which the new service order should be associated.</span></span>
    
      - <span data-ttu-id="143f9-131">(Дополнительно) Используйте поле **Код проекта**, чтобы связать этот заказ на обслуживание с конкретным проектом.</span><span class="sxs-lookup"><span data-stu-id="143f9-131">Optional: Use the **Project ID** field to associate this service order with a particular project.</span></span>

5.  <span data-ttu-id="143f9-132">Щелкните **Далее \>** и выполните следующие шаги на странице **Создать заказ на обслуживание**:</span><span class="sxs-lookup"><span data-stu-id="143f9-132">Click **Next \>**, and then complete the following steps on the **Create service order** page:</span></span>
    
      - <span data-ttu-id="143f9-133">В поле **Предпочитаемое время обслуживания** введите дату и время начала для данной заявки на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="143f9-133">Enter a date and time for the service call to begin in the **Preferred service time** field.</span></span>
    
      - <span data-ttu-id="143f9-134">(Необязательно) Измените текст в поле **Описание**.</span><span class="sxs-lookup"><span data-stu-id="143f9-134">Optional: Modify the text in the **Description** field.</span></span> <span data-ttu-id="143f9-135">По умолчанию это поле содержит описание соглашения о сервисном обслуживании, выбранного на предыдущей странице.</span><span class="sxs-lookup"><span data-stu-id="143f9-135">By default, this field contains the description of the service agreement that you selected on the previous page.</span></span>
    
      - <span data-ttu-id="143f9-136">В поле **Ответственный** выберите идентификатор сотрудника, ответственного за это соглашение и, если имеется соответствующая информация, введите идентификатор предпочтительного для клиента технического специалиста по этой заявке на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="143f9-136">In the **Responsible** field, select the ID of the employee who is responsible for the agreement, and if you know what it is, enter the ID of the customer's preferred technician for the service call.</span></span>
    
      - <span data-ttu-id="143f9-137">В поле **Код контактного лица** выберите контактное лицо в компании клиента, с которым необходимо связаться относительно данного заказа на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="143f9-137">In the **Contact ID** field, select the person in the customer's company who should be contacted regarding this service order.</span></span>

6.  <span data-ttu-id="143f9-138">Щелкните **Далее \>**, а затем нажмите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="143f9-138">Click **Next \>**, and then click **Finish**.</span></span>


## <a name="see-also"></a><span data-ttu-id="143f9-139">См. также</span><span class="sxs-lookup"><span data-stu-id="143f9-139">See also</span></span>

[<span data-ttu-id="143f9-140">Заказы на обслуживание</span><span class="sxs-lookup"><span data-stu-id="143f9-140">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="143f9-141">Автоматическое создание заказов на сервисное обслуживание</span><span class="sxs-lookup"><span data-stu-id="143f9-141">Create service orders automatically</span></span>](create-service-orders-automatically.md)

<span data-ttu-id="143f9-142">[Создание заказов на обслуживание (форма класса)](https://technet.microsoft.com/en-us/library/aa553901\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="143f9-142">[Create service orders (class form)](https://technet.microsoft.com/en-us/library/aa553901\(v=ax.60\))</span></span> 


