---
title: Создание связей задач обслуживания
description: Можно связывать задачи обслуживания с соглашениями о сервисном обслуживании или заказами на сервисное обслуживание для описания задачи сервисного обслуживания, которая должна быть выполнена для соглашения или заказа.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e50b4322c65097ab4f8aba9c36e4d5e6cc4c01b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436161"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="dfb6a-103">Создание связей задач обслуживания</span><span class="sxs-lookup"><span data-stu-id="dfb6a-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dfb6a-104">Можно связывать задачи обслуживания с соглашениями о сервисном обслуживании или заказами на сервисное обслуживание для описания задачи сервисного обслуживания, которая должна быть выполнена для соглашения или заказа.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="dfb6a-105">Эта информация доступна техническим специалистам и клиентам.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="dfb6a-106">Создание связи с соглашением на обслуживание</span><span class="sxs-lookup"><span data-stu-id="dfb6a-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="dfb6a-107">Щелкните **Управление сервисным обслуживанием** \> **Общее** \> **Соглашения на обслуживание** \> **Соглашения на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-107">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="dfb6a-108">Выберите существующее соглашение или создайте новое.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="dfb6a-109">На панели операций нажмите кнопку **Задачи сервисного обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-109">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="dfb6a-110">В форме **Задачи сервисного обслуживания** нажмите CTRL+N, чтобы создать новую строку, затем выберите задачу сервисного обслуживания из списка **Задача сервисного обслуживания**, чтобы присоединить задачу сервисного обслуживания к соглашению о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-110">On the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="dfb6a-111">На вкладке **Описание** введите в поле свободного текстового формата внутренние или внешние описания примечаний.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="dfb6a-112">Закройте форму, чтобы сохранить запись.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-112">Close the form to save the record.</span></span>

<span data-ttu-id="dfb6a-113">Повторяйте эту процедуру, пока не будут созданы все необходимые связи задач обслуживания для данного соглашения на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="dfb6a-114">Теперь эти задачи обслуживания можно определять в прикрепленных строках соглашения.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="dfb6a-115">Связь с задачами обслуживания, создаваемая в соглашении на обслуживание, доступна из всех заказов на обслуживание, присоединенных к соглашению на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="dfb6a-116">Создание связи с заказом на обслуживание</span><span class="sxs-lookup"><span data-stu-id="dfb6a-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="dfb6a-117">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Заказы на сервисное обслуживание** \> **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="dfb6a-118">Выберите существующий заказ на обслуживание или создайте новый.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="dfb6a-119">На панели операций нажмите кнопку **Задачи сервисного обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-119">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="dfb6a-120">В форме **Задачи сервисного обслуживания** нажмите CTRL+N, чтобы создать новую строку, затем выберите задачу сервисного обслуживания из списка **Задача сервисного обслуживания**, чтобы присоединить задачи сервисного обслуживания к заказу на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-120">From the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="dfb6a-121">На вкладке **Описание** введите в поле свободного текстового формата внутренние или внешние описания примечаний.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="dfb6a-122">Закройте форму, чтобы сохранить запись.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-122">Close the form to save the record.</span></span>

<span data-ttu-id="dfb6a-123">Повторяйте эту процедуру до тех пор, пока не будут созданы все необходимые связи задач обслуживания для данного заказа на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="dfb6a-124">Теперь при создании строк заказа на обслуживание можно выбирать задачу обслуживания, для которой создана связь.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="dfb6a-125">Связи задач обслуживания, созданные для заказа на обслуживание, доступны для определенного заказа на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="dfb6a-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="dfb6a-126">См. также</span><span class="sxs-lookup"><span data-stu-id="dfb6a-126">See also</span></span>

[<span data-ttu-id="dfb6a-127">Обзор задач сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="dfb6a-127">Service tasks overview</span></span>](service-tasks.md)


  


