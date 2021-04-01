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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44ca8920619ff4b0ae45293c997a8c385cfbd091
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234905"
---
# <a name="create-service-object-relations"></a><span data-ttu-id="d1825-103">Создание связей объектов обслуживания</span><span class="sxs-lookup"><span data-stu-id="d1825-103">Create service object relations</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d1825-104">В этом разделе описывается, как создать связи объектов сервисного обслуживания для соглашения о сервисном обслуживании и заказа на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d1825-104">This topic describes how to create service object relations for a service agreement and a service order.</span></span> <span data-ttu-id="d1825-105">При создании связи объекта сервисного обслуживания объект сервисного обслуживания связывается с соглашением о сервисном обслуживании или заказом на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d1825-105">When you a create service object relation, you associate the service object to a service agreement or service order.</span></span> <span data-ttu-id="d1825-106">Когда клиент запрашивает обслуживание номенклатуры, которая является объектом сервисного обслуживания, можно выбрать объект сервисного обслуживания из списка связей объектов сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="d1825-106">When a customer requests service for an item that is a service object, you can select the service object from the list of service object relations.</span></span>

## <a name="create-a-service-object-relation-for-a-service-agreement"></a><span data-ttu-id="d1825-107">Создание связи объекта сервисного обслуживания для соглашения о сервисном обслуживании</span><span class="sxs-lookup"><span data-stu-id="d1825-107">Create a service object relation for a service agreement</span></span>

<span data-ttu-id="d1825-108">Выполните следующие действия, чтобы создать связь объекта сервисного обслуживания для соглашения о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="d1825-108">Use the following steps to create a service object relation for a service agreement:</span></span>

1.  <span data-ttu-id="d1825-109">Щелкните **Управление сервисным обслуживанием** \> **Общее** \> **Соглашения на обслуживание** \> **Соглашения на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="d1825-109">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="d1825-110">В списке **Соглашения о сервисном обслуживании** выберите существующее соглашение о сервисном обслуживании или нажмите кнопку **Создать**, чтобы создать новое соглашение о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="d1825-110">In the **Service agreements** list, select an existing service agreement, or click **New** to create a new service agreement.</span></span>

3.  <span data-ttu-id="d1825-111">В форме **Соглашения о сервисном обслуживании** в разделе **Панель операций** на вкладке **Соглашение о сервисном обслуживании** в группе **Связи** щелкните **Объекты сервисного обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="d1825-111">In the **Service agreements** form, on the **Action Pane**, on the **Service agreement** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="d1825-112">В форме **Объекты сервисного обслуживания** нажмите кнопку **Создать**, а затем выберите объект сервисного обслуживания для данного соглашения о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="d1825-112">In the **Service objects** form, click **New**, and then select a service object for this service agreement.</span></span>

5.  <span data-ttu-id="d1825-113">Чтобы назначить шаблон спецификации соглашению о сервисном обслуживании, щелкните **Функции** и выберите **Присоединение шаблона спецификации**.</span><span class="sxs-lookup"><span data-stu-id="d1825-113">To assign a template bill of materials (BOM) to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="d1825-114">В форме **Выбор шаблона спецификации** в поле **Шаблон спецификации** выберите шаблон.</span><span class="sxs-lookup"><span data-stu-id="d1825-114">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 

## <a name="create-a-service-object-relation-for-a-service-order"></a><span data-ttu-id="d1825-115">Создание связи объекта сервисного обслуживания для заказа на сервисное обслуживание</span><span class="sxs-lookup"><span data-stu-id="d1825-115">Create a service object relation for a service order</span></span>

<span data-ttu-id="d1825-116">Выполните следующие действия, чтобы создать связь объекта сервисного обслуживания для заказа на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d1825-116">Use the following steps to create a service object relation for a service order:</span></span>

1.  <span data-ttu-id="d1825-117">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Заказы на сервисное обслуживание** \> **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="d1825-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="d1825-118">В списке **Заказы на сервисное обслуживание** выберите существующий заказ на сервисное обслуживание или создайте новый.</span><span class="sxs-lookup"><span data-stu-id="d1825-118">In the **Service orders** list, select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="d1825-119">В форме **Заказы на сервисное обслуживание** в разделе **Панель операций** на вкладке **Заказ на сервисное обслуживание** в группе **Связи** щелкните **Объекты сервисного обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="d1825-119">In the **Service orders** form, on the **Action Pane**, on the **Service order** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="d1825-120">В форме **Объекты сервисного обслуживания** нажмите кнопку **Создать**, а затем выберите объект сервисного обслуживания для данного объекта сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="d1825-120">In the **Service objects** form, click **New**, and then select a service object for this service order.</span></span>

5.  <span data-ttu-id="d1825-121">Чтобы назначить шаблон спецификации соглашению о сервисном обслуживании, щелкните **Функции** и выберите **Присоединение шаблона спецификации**.</span><span class="sxs-lookup"><span data-stu-id="d1825-121">To assign a template BOM to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="d1825-122">В форме **Выбор шаблона спецификации** в поле **Шаблон спецификации** выберите шаблон.</span><span class="sxs-lookup"><span data-stu-id="d1825-122">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 


## <a name="see-also"></a><span data-ttu-id="d1825-123">См. также</span><span class="sxs-lookup"><span data-stu-id="d1825-123">See also</span></span>

[<span data-ttu-id="d1825-124">Обзор объектов сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="d1825-124">Service objects overview</span></span>](service-objects.md)

[<span data-ttu-id="d1825-125">Связи объектов сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="d1825-125">Service object relations</span></span>](service-object-relations.md)

[<span data-ttu-id="d1825-126">Шаблоны спецификаций</span><span class="sxs-lookup"><span data-stu-id="d1825-126">Template BOMs</span></span>](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]