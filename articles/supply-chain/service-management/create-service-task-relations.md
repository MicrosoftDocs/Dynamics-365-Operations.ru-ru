---
title: "Создание связей задач обслуживания"
description: "Можно связывать задачи обслуживания с соглашениями о сервисном обслуживании или заказами на сервисное обслуживание для описания задачи сервисного обслуживания, которая должна быть выполнена для соглашения или заказа."
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
ms.openlocfilehash: 2aa0e5200ff2a6822e631c72124335e2dc556c14
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---

# <a name="create-service-task-relations"></a><span data-ttu-id="9a206-103">Создание связей задач обслуживания</span><span class="sxs-lookup"><span data-stu-id="9a206-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a206-104">Можно связывать задачи обслуживания с соглашениями о сервисном обслуживании или заказами на сервисное обслуживание для описания задачи сервисного обслуживания, которая должна быть выполнена для соглашения или заказа.</span><span class="sxs-lookup"><span data-stu-id="9a206-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="9a206-105">Эта информация доступна техническим специалистам и клиентам.</span><span class="sxs-lookup"><span data-stu-id="9a206-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="9a206-106">Создание связи с соглашением на обслуживание</span><span class="sxs-lookup"><span data-stu-id="9a206-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="9a206-107">Щелкните **Управление сервисным обслуживанием** \> **Общее** \> **Соглашения на обслуживание** \> **Соглашения на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="9a206-107">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="9a206-108">Выберите существующее соглашение или создайте новое.</span><span class="sxs-lookup"><span data-stu-id="9a206-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="9a206-109">На панели операций нажмите кнопку **Задачи сервисного обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="9a206-109">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="9a206-110">В форме **Задачи сервисного обслуживания** нажмите CTRL+N, чтобы создать новую строку, затем выберите задачу сервисного обслуживания из списка **Задача сервисного обслуживания**, чтобы присоединить задачу сервисного обслуживания к соглашению о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="9a206-110">On the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="9a206-111">На вкладке **Описание** введите в поле свободного текстового формата внутренние или внешние описания примечаний.</span><span class="sxs-lookup"><span data-stu-id="9a206-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="9a206-112">Закройте форму, чтобы сохранить запись.</span><span class="sxs-lookup"><span data-stu-id="9a206-112">Close the form to save the record.</span></span>

<span data-ttu-id="9a206-113">Повторяйте эту процедуру, пока не будут созданы все необходимые связи задач обслуживания для данного соглашения на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9a206-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="9a206-114">Теперь эти задачи обслуживания можно определять в прикрепленных строках соглашения.</span><span class="sxs-lookup"><span data-stu-id="9a206-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="9a206-115">Связь с задачами обслуживания, создаваемая в соглашении на обслуживание, доступна из всех заказов на обслуживание, присоединенных к соглашению на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9a206-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="9a206-116">Создание связи с заказом на обслуживание</span><span class="sxs-lookup"><span data-stu-id="9a206-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="9a206-117">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Заказы на сервисное обслуживание** \> **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="9a206-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="9a206-118">Выберите существующий заказ на обслуживание или создайте новый.</span><span class="sxs-lookup"><span data-stu-id="9a206-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="9a206-119">На панели операций нажмите кнопку **Задачи сервисного обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="9a206-119">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="9a206-120">В форме **Задачи сервисного обслуживания** нажмите CTRL+N, чтобы создать новую строку, затем выберите задачу сервисного обслуживания из списка **Задача сервисного обслуживания**, чтобы присоединить задачи сервисного обслуживания к заказу на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9a206-120">From the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="9a206-121">На вкладке **Описание** введите в поле свободного текстового формата внутренние или внешние описания примечаний.</span><span class="sxs-lookup"><span data-stu-id="9a206-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="9a206-122">Закройте форму, чтобы сохранить запись.</span><span class="sxs-lookup"><span data-stu-id="9a206-122">Close the form to save the record.</span></span>

<span data-ttu-id="9a206-123">Повторяйте эту процедуру до тех пор, пока не будут созданы все необходимые связи задач обслуживания для данного заказа на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9a206-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="9a206-124">Теперь при создании строк заказа на обслуживание можно выбирать задачу обслуживания, для которой создана связь.</span><span class="sxs-lookup"><span data-stu-id="9a206-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="9a206-125">Связи задач обслуживания, созданные для заказа на обслуживание, доступны для определенного заказа на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9a206-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="9a206-126">См. также</span><span class="sxs-lookup"><span data-stu-id="9a206-126">See also</span></span>

[<span data-ttu-id="9a206-127">Задачи обслуживания</span><span class="sxs-lookup"><span data-stu-id="9a206-127">Service tasks</span></span>](service-tasks.md)


  



