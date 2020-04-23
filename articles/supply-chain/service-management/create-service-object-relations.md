---
title: Создание связей объектов обслуживания
description: В этом разделе описывается, как создать связи объектов сервисного обслуживания для соглашения о сервисном обслуживании и заказа на сервисное обслуживание.
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
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab5de850ef40c26e447b96d8f42ccf83fb490818
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202775"
---
# <a name="create-service-object-relations"></a><span data-ttu-id="f7b73-103">Создание связей объектов обслуживания</span><span class="sxs-lookup"><span data-stu-id="f7b73-103">Create service object relations</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f7b73-104">В этом разделе описывается, как создать связи объектов сервисного обслуживания для соглашения о сервисном обслуживании и заказа на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="f7b73-104">This topic describes how to create service object relations for a service agreement and a service order.</span></span> <span data-ttu-id="f7b73-105">При создании связи объекта сервисного обслуживания объект сервисного обслуживания связывается с соглашением о сервисном обслуживании или заказом на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="f7b73-105">When you a create service object relation, you associate the service object to a service agreement or service order.</span></span> <span data-ttu-id="f7b73-106">Когда клиент запрашивает обслуживание номенклатуры, которая является объектом сервисного обслуживания, можно выбрать объект сервисного обслуживания из списка связей объектов сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="f7b73-106">When a customer requests service for an item that is a service object, you can select the service object from the list of service object relations.</span></span>

## <a name="create-a-service-object-relation-for-a-service-agreement"></a><span data-ttu-id="f7b73-107">Создание связи объекта сервисного обслуживания для соглашения о сервисном обслуживании</span><span class="sxs-lookup"><span data-stu-id="f7b73-107">Create a service object relation for a service agreement</span></span>

<span data-ttu-id="f7b73-108">Выполните следующие действия, чтобы создать связь объекта сервисного обслуживания для соглашения о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="f7b73-108">Use the following steps to create a service object relation for a service agreement:</span></span>

1.  <span data-ttu-id="f7b73-109">Щелкните **Управление сервисным обслуживанием** \> **Общее** \> **Соглашения на обслуживание** \> **Соглашения на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="f7b73-109">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="f7b73-110">В списке **Соглашения о сервисном обслуживании** выберите существующее соглашение о сервисном обслуживании или нажмите кнопку **Создать**, чтобы создать новое соглашение о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="f7b73-110">In the **Service agreements** list, select an existing service agreement, or click **New** to create a new service agreement.</span></span>

3.  <span data-ttu-id="f7b73-111">В форме **Соглашения о сервисном обслуживании** в разделе **Панель операций** на вкладке **Соглашение о сервисном обслуживании** в группе **Связи** щелкните **Объекты сервисного обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="f7b73-111">In the **Service agreements** form, on the **Action Pane**, on the **Service agreement** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="f7b73-112">В форме **Объекты сервисного обслуживания** нажмите кнопку **Создать**, а затем выберите объект сервисного обслуживания для данного соглашения о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="f7b73-112">In the **Service objects** form, click **New**, and then select a service object for this service agreement.</span></span>

5.  <span data-ttu-id="f7b73-113">Чтобы назначить шаблон спецификации соглашению о сервисном обслуживании, щелкните **Функции**и выберите **Присоединение шаблона спецификации**.</span><span class="sxs-lookup"><span data-stu-id="f7b73-113">To assign a template bill of materials (BOM) to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="f7b73-114">В форме **Выбор шаблона спецификации** в поле **Шаблон спецификации** выберите шаблон.</span><span class="sxs-lookup"><span data-stu-id="f7b73-114">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 

## <a name="create-a-service-object-relation-for-a-service-order"></a><span data-ttu-id="f7b73-115">Создание связи объекта сервисного обслуживания для заказа на сервисное обслуживание</span><span class="sxs-lookup"><span data-stu-id="f7b73-115">Create a service object relation for a service order</span></span>

<span data-ttu-id="f7b73-116">Выполните следующие действия, чтобы создать связь объекта сервисного обслуживания для заказа на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="f7b73-116">Use the following steps to create a service object relation for a service order:</span></span>

1.  <span data-ttu-id="f7b73-117">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Заказы на сервисное обслуживание** \> **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="f7b73-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="f7b73-118">В списке **Заказы на сервисное обслуживание** выберите существующий заказ на сервисное обслуживание или создайте новый.</span><span class="sxs-lookup"><span data-stu-id="f7b73-118">In the **Service orders** list, select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="f7b73-119">В форме **Заказы на сервисное обслуживание** в разделе **Панель операций** на вкладке **Заказ на сервисное обслуживание** в группе **Связи** щелкните **Объекты сервисного обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="f7b73-119">In the **Service orders** form, on the **Action Pane**, on the **Service order** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="f7b73-120">В форме **Объекты сервисного обслуживания** нажмите кнопку **Создать**, а затем выберите объект сервисного обслуживания для данного объекта сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="f7b73-120">In the **Service objects** form, click **New**, and then select a service object for this service order.</span></span>

5.  <span data-ttu-id="f7b73-121">Чтобы назначить шаблон спецификации соглашению о сервисном обслуживании, щелкните **Функции**и выберите **Присоединение шаблона спецификации**.</span><span class="sxs-lookup"><span data-stu-id="f7b73-121">To assign a template BOM to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="f7b73-122">В форме **Выбор шаблона спецификации** в поле **Шаблон спецификации** выберите шаблон.</span><span class="sxs-lookup"><span data-stu-id="f7b73-122">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 


## <a name="see-also"></a><span data-ttu-id="f7b73-123">См. также</span><span class="sxs-lookup"><span data-stu-id="f7b73-123">See also</span></span>

[<span data-ttu-id="f7b73-124">Обзор объектов сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="f7b73-124">Service objects overview</span></span>](service-objects.md)

[<span data-ttu-id="f7b73-125">Связи объектов сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="f7b73-125">Service object relations</span></span>](service-object-relations.md)

[<span data-ttu-id="f7b73-126">Шаблоны спецификаций</span><span class="sxs-lookup"><span data-stu-id="f7b73-126">Template BOMs</span></span>](template-boms.md)

  


