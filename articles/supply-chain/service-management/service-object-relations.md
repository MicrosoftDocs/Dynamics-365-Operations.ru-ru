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
ms.openlocfilehash: 82e25c162a33dd8e6e1a0cc4f215a8693fc1080b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5266063"
---
# <a name="service-object-relations"></a><span data-ttu-id="3d006-103">Связи объектов обслуживания</span><span class="sxs-lookup"><span data-stu-id="3d006-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d006-104">Можно создать для объектов обслуживания связи между объектом обслуживания и соглашением на обслуживание или заказом на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="3d006-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="3d006-105">При создании связи, объект обслуживания присоединяется к соглашению на обслуживание или к заказу на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="3d006-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="3d006-106">После создания связи можно присоединить объект обслуживания к любым строкам соглашения о сервисном обслуживании или заказа на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="3d006-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="3d006-107">Шаблоны спецификаций</span><span class="sxs-lookup"><span data-stu-id="3d006-107">Template BOMs</span></span>

<span data-ttu-id="3d006-108">Также можно указать шаблон спецификации для связи объектов.</span><span class="sxs-lookup"><span data-stu-id="3d006-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="3d006-109">Шаблон спецификации — это спецификация объекта, обслуживание которого выполняется.</span><span class="sxs-lookup"><span data-stu-id="3d006-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="3d006-110">Если в ходе визита с целью обслуживания вы произвели замену комплектующей детали объекта обслуживания, это изменение можно зарегистрировать в спецификации обслуживания, используя форму "Объекты обслуживания".</span><span class="sxs-lookup"><span data-stu-id="3d006-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="3d006-111">Пример</span><span class="sxs-lookup"><span data-stu-id="3d006-111">Example</span></span>

<span data-ttu-id="3d006-112">Вы создаете соглашение на обслуживание двух лифтов на территории объекта клиента.</span><span class="sxs-lookup"><span data-stu-id="3d006-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="3d006-113">Соглашение о сервисном обслуживании имеет идентификатор SAL-001.</span><span class="sxs-lookup"><span data-stu-id="3d006-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="3d006-114">Лифты настроены как объекты EL-S/1000 и EL-L/1000 в форме "Объекты обслуживания".</span><span class="sxs-lookup"><span data-stu-id="3d006-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="3d006-115">Вы присоединяете объекты обслуживания (EL-S/1000 и EL-L/1000) к соглашению о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="3d006-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="3d006-116">Требуется зарегистрировать изменения в спецификации объекта обслуживания, поскольку производится замена комплектующих деталей объекта, с этой целью спецификация обслуживания присоединяется к связи объектов обслуживания, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3d006-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="3d006-117">Объект обслуживания</span><span class="sxs-lookup"><span data-stu-id="3d006-117">Service object</span></span> | <span data-ttu-id="3d006-118">Связь — Соглашение о сервисном обслуживании</span><span class="sxs-lookup"><span data-stu-id="3d006-118">Relation – Service agreement</span></span> | <span data-ttu-id="3d006-119">Спецификация обслуживания</span><span class="sxs-lookup"><span data-stu-id="3d006-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="3d006-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="3d006-120">EL-S/1000</span></span>      | <span data-ttu-id="3d006-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="3d006-121">ID SAL-001</span></span>                   | <span data-ttu-id="3d006-122">BOM-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="3d006-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="3d006-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="3d006-123">EL-L/1000</span></span>      | <span data-ttu-id="3d006-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="3d006-124">ID SAL-001</span></span>                   | <span data-ttu-id="3d006-125">BOM-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="3d006-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="3d006-126">Поскольку для данного соглашения имеются связи объектов обслуживания, теперь можно создать строки соглашения о сервисном обслуживании с данными объектами, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3d006-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="3d006-127">Тип проводки</span><span class="sxs-lookup"><span data-stu-id="3d006-127">Transaction type</span></span> | <span data-ttu-id="3d006-128">Категория</span><span class="sxs-lookup"><span data-stu-id="3d006-128">Category</span></span>           | <span data-ttu-id="3d006-129">Объект обслуживания</span><span class="sxs-lookup"><span data-stu-id="3d006-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="3d006-130">Часы</span><span class="sxs-lookup"><span data-stu-id="3d006-130">Hour</span></span>             | <span data-ttu-id="3d006-131">Инвентаризация</span><span class="sxs-lookup"><span data-stu-id="3d006-131">Inspection</span></span>         | <span data-ttu-id="3d006-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="3d006-132">EL-S/1000</span></span>      |
| <span data-ttu-id="3d006-133">Часы</span><span class="sxs-lookup"><span data-stu-id="3d006-133">Hour</span></span>             | <span data-ttu-id="3d006-134">Очистка редуктора</span><span class="sxs-lookup"><span data-stu-id="3d006-134">Gear box cleaning</span></span>  | <span data-ttu-id="3d006-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="3d006-135">EL-S/1000</span></span>      |
| <span data-ttu-id="3d006-136">Номенклатура</span><span class="sxs-lookup"><span data-stu-id="3d006-136">Item</span></span>             | <span data-ttu-id="3d006-137">Очищающие материалы</span><span class="sxs-lookup"><span data-stu-id="3d006-137">Cleaning materials</span></span> | <span data-ttu-id="3d006-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="3d006-138">EL-S/1000</span></span>      |
| <span data-ttu-id="3d006-139">Часы</span><span class="sxs-lookup"><span data-stu-id="3d006-139">Hour</span></span>             | <span data-ttu-id="3d006-140">Инвентаризация</span><span class="sxs-lookup"><span data-stu-id="3d006-140">Inspection</span></span>         | <span data-ttu-id="3d006-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="3d006-141">EL-L/1000</span></span>      |
| <span data-ttu-id="3d006-142">Часы</span><span class="sxs-lookup"><span data-stu-id="3d006-142">Hour</span></span>             | <span data-ttu-id="3d006-143">Очистка редуктора</span><span class="sxs-lookup"><span data-stu-id="3d006-143">Gearbox cleaning</span></span>   | <span data-ttu-id="3d006-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="3d006-144">EL-L/1000</span></span>      |
| <span data-ttu-id="3d006-145">Номенклатура</span><span class="sxs-lookup"><span data-stu-id="3d006-145">Item</span></span>             | <span data-ttu-id="3d006-146">Очищающие материалы</span><span class="sxs-lookup"><span data-stu-id="3d006-146">Cleaning materials</span></span> | <span data-ttu-id="3d006-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="3d006-147">EL-L/1000</span></span>      |

<span data-ttu-id="3d006-148">Во время визита с целью обслуживания пришлось заменить редуктор лифта EL-S/1000.</span><span class="sxs-lookup"><span data-stu-id="3d006-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="3d006-149">Для замены комплектующей детали объекта можно получить доступ к конструктору спецификаций, используя связь объектов обслуживания, которую вы настроили для текущего соглашения на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="3d006-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="3d006-150">Доступ к конструктору спецификаций с использованием связи объектов обслуживания</span><span class="sxs-lookup"><span data-stu-id="3d006-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="3d006-151">Соглашения на обслуживание</span><span class="sxs-lookup"><span data-stu-id="3d006-151">Service agreements</span></span>
2. <span data-ttu-id="3d006-152">Дважды щелкните соглашение о сервисном обслуживание или нажмите "Соглашение о сервисном обслуживании", чтобы создать новое соглашение о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="3d006-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="3d006-153">Перейдите на вкладку "Настройка".</span><span class="sxs-lookup"><span data-stu-id="3d006-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="3d006-154">Щелкните "Объекты обслуживания", чтобы присоединить шаблон спецификации к соглашению о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="3d006-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="3d006-155">В форме "Объекты обслуживания" нажмите кнопку "Конструктор", чтобы открыть форму конструктора и изменить шаблон спецификаций.</span><span class="sxs-lookup"><span data-stu-id="3d006-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="3d006-156">Автоматически созданные заказы на обслуживание</span><span class="sxs-lookup"><span data-stu-id="3d006-156">Automatically created service orders</span></span>

<span data-ttu-id="3d006-157">При автоматическом создании заказов на обслуживание по соглашению о сервисном обслуживании связи объектов обслуживания в соглашении также создаются и в заказах на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="3d006-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]