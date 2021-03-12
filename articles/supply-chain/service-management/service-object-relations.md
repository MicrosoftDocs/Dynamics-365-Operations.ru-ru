---
title: Связи объектов обслуживания
description: Можно создать для объектов обслуживания связи между объектом обслуживания и соглашением на обслуживание или заказом на обслуживание.
author: ShylaThompson
manager: tfehr
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 913b3c30bf972de7cc3dde73280e4f2f2be38507
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974343"
---
# <a name="service-object-relations"></a><span data-ttu-id="e16e7-103">Связи объектов обслуживания</span><span class="sxs-lookup"><span data-stu-id="e16e7-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e16e7-104">Можно создать для объектов обслуживания связи между объектом обслуживания и соглашением на обслуживание или заказом на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="e16e7-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="e16e7-105">При создании связи, объект обслуживания присоединяется к соглашению на обслуживание или к заказу на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="e16e7-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="e16e7-106">После создания связи можно присоединить объект обслуживания к любым строкам соглашения о сервисном обслуживании или заказа на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="e16e7-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="e16e7-107">Шаблоны спецификаций</span><span class="sxs-lookup"><span data-stu-id="e16e7-107">Template BOMs</span></span>

<span data-ttu-id="e16e7-108">Также можно указать шаблон спецификации для связи объектов.</span><span class="sxs-lookup"><span data-stu-id="e16e7-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="e16e7-109">Шаблон спецификации — это спецификация объекта, обслуживание которого выполняется.</span><span class="sxs-lookup"><span data-stu-id="e16e7-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="e16e7-110">Если в ходе визита с целью обслуживания вы произвели замену комплектующей детали объекта обслуживания, это изменение можно зарегистрировать в спецификации обслуживания, используя форму "Объекты обслуживания".</span><span class="sxs-lookup"><span data-stu-id="e16e7-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="e16e7-111">Пример</span><span class="sxs-lookup"><span data-stu-id="e16e7-111">Example</span></span>

<span data-ttu-id="e16e7-112">Вы создаете соглашение на обслуживание двух лифтов на территории объекта клиента.</span><span class="sxs-lookup"><span data-stu-id="e16e7-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="e16e7-113">Соглашение о сервисном обслуживании имеет идентификатор SAL-001.</span><span class="sxs-lookup"><span data-stu-id="e16e7-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="e16e7-114">Лифты настроены как объекты EL-S/1000 и EL-L/1000 в форме "Объекты обслуживания".</span><span class="sxs-lookup"><span data-stu-id="e16e7-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="e16e7-115">Вы присоединяете объекты обслуживания (EL-S/1000 и EL-L/1000) к соглашению о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="e16e7-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="e16e7-116">Требуется зарегистрировать изменения в спецификации объекта обслуживания, поскольку производится замена комплектующих деталей объекта, с этой целью спецификация обслуживания присоединяется к связи объектов обслуживания, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e16e7-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="e16e7-117">Объект обслуживания</span><span class="sxs-lookup"><span data-stu-id="e16e7-117">Service object</span></span> | <span data-ttu-id="e16e7-118">Связь — Соглашение о сервисном обслуживании</span><span class="sxs-lookup"><span data-stu-id="e16e7-118">Relation – Service agreement</span></span> | <span data-ttu-id="e16e7-119">Спецификация обслуживания</span><span class="sxs-lookup"><span data-stu-id="e16e7-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="e16e7-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="e16e7-120">EL-S/1000</span></span>      | <span data-ttu-id="e16e7-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="e16e7-121">ID SAL-001</span></span>                   | <span data-ttu-id="e16e7-122">BOM-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="e16e7-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="e16e7-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="e16e7-123">EL-L/1000</span></span>      | <span data-ttu-id="e16e7-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="e16e7-124">ID SAL-001</span></span>                   | <span data-ttu-id="e16e7-125">BOM-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="e16e7-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="e16e7-126">Поскольку для данного соглашения имеются связи объектов обслуживания, теперь можно создать строки соглашения о сервисном обслуживании с данными объектами, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e16e7-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="e16e7-127">Тип проводки</span><span class="sxs-lookup"><span data-stu-id="e16e7-127">Transaction type</span></span> | <span data-ttu-id="e16e7-128">Категория</span><span class="sxs-lookup"><span data-stu-id="e16e7-128">Category</span></span>           | <span data-ttu-id="e16e7-129">Объект обслуживания</span><span class="sxs-lookup"><span data-stu-id="e16e7-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="e16e7-130">Часы</span><span class="sxs-lookup"><span data-stu-id="e16e7-130">Hour</span></span>             | <span data-ttu-id="e16e7-131">Инвентаризация</span><span class="sxs-lookup"><span data-stu-id="e16e7-131">Inspection</span></span>         | <span data-ttu-id="e16e7-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="e16e7-132">EL-S/1000</span></span>      |
| <span data-ttu-id="e16e7-133">Часы</span><span class="sxs-lookup"><span data-stu-id="e16e7-133">Hour</span></span>             | <span data-ttu-id="e16e7-134">Очистка редуктора</span><span class="sxs-lookup"><span data-stu-id="e16e7-134">Gear box cleaning</span></span>  | <span data-ttu-id="e16e7-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="e16e7-135">EL-S/1000</span></span>      |
| <span data-ttu-id="e16e7-136">Номенклатура</span><span class="sxs-lookup"><span data-stu-id="e16e7-136">Item</span></span>             | <span data-ttu-id="e16e7-137">Очищающие материалы</span><span class="sxs-lookup"><span data-stu-id="e16e7-137">Cleaning materials</span></span> | <span data-ttu-id="e16e7-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="e16e7-138">EL-S/1000</span></span>      |
| <span data-ttu-id="e16e7-139">Часы</span><span class="sxs-lookup"><span data-stu-id="e16e7-139">Hour</span></span>             | <span data-ttu-id="e16e7-140">Инвентаризация</span><span class="sxs-lookup"><span data-stu-id="e16e7-140">Inspection</span></span>         | <span data-ttu-id="e16e7-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="e16e7-141">EL-L/1000</span></span>      |
| <span data-ttu-id="e16e7-142">Часы</span><span class="sxs-lookup"><span data-stu-id="e16e7-142">Hour</span></span>             | <span data-ttu-id="e16e7-143">Очистка редуктора</span><span class="sxs-lookup"><span data-stu-id="e16e7-143">Gearbox cleaning</span></span>   | <span data-ttu-id="e16e7-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="e16e7-144">EL-L/1000</span></span>      |
| <span data-ttu-id="e16e7-145">Номенклатура</span><span class="sxs-lookup"><span data-stu-id="e16e7-145">Item</span></span>             | <span data-ttu-id="e16e7-146">Очищающие материалы</span><span class="sxs-lookup"><span data-stu-id="e16e7-146">Cleaning materials</span></span> | <span data-ttu-id="e16e7-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="e16e7-147">EL-L/1000</span></span>      |

<span data-ttu-id="e16e7-148">Во время визита с целью обслуживания пришлось заменить редуктор лифта EL-S/1000.</span><span class="sxs-lookup"><span data-stu-id="e16e7-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="e16e7-149">Для замены комплектующей детали объекта можно получить доступ к конструктору спецификаций, используя связь объектов обслуживания, которую вы настроили для текущего соглашения на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="e16e7-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="e16e7-150">Доступ к конструктору спецификаций с использованием связи объектов обслуживания</span><span class="sxs-lookup"><span data-stu-id="e16e7-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="e16e7-151">Соглашения на обслуживание</span><span class="sxs-lookup"><span data-stu-id="e16e7-151">Service agreements</span></span>
2. <span data-ttu-id="e16e7-152">Дважды щелкните соглашение о сервисном обслуживание или нажмите "Соглашение о сервисном обслуживании", чтобы создать новое соглашение о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="e16e7-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="e16e7-153">Перейдите на вкладку "Настройка".</span><span class="sxs-lookup"><span data-stu-id="e16e7-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="e16e7-154">Щелкните "Объекты обслуживания", чтобы присоединить шаблон спецификации к соглашению о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="e16e7-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="e16e7-155">В форме "Объекты обслуживания" нажмите кнопку "Конструктор", чтобы открыть форму конструктора и изменить шаблон спецификаций.</span><span class="sxs-lookup"><span data-stu-id="e16e7-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="e16e7-156">Автоматически созданные заказы на обслуживание</span><span class="sxs-lookup"><span data-stu-id="e16e7-156">Automatically created service orders</span></span>

<span data-ttu-id="e16e7-157">При автоматическом создании заказов на обслуживание по соглашению о сервисном обслуживании связи объектов обслуживания в соглашении также создаются и в заказах на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="e16e7-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>

