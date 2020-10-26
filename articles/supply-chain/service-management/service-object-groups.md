---
title: Группы объектов сервисного обслуживания
description: Группы объектов удобно использовать для сортировки и фильтрации данных по объектам в отчетах и статистике.
author: ShylaThompson
manager: tfehr
ms.date: 05/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4438487fa234cf093b557bca9455717b2cd3ca0b
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979240"
---
# <a name="service-object-groups"></a><span data-ttu-id="57793-103">Группы объектов сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="57793-103">Service object groups</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57793-104">Группы объектов удобно использовать для сортировки и фильтрации данных по объектам в отчетах и статистике.</span><span class="sxs-lookup"><span data-stu-id="57793-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="57793-105">Например, можно сгруппировать объекты по географическому местоположению или по типу.</span><span class="sxs-lookup"><span data-stu-id="57793-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="57793-106">Группирование по географическому местоположению</span><span class="sxs-lookup"><span data-stu-id="57793-106">Group by geographical location</span></span>

<span data-ttu-id="57793-107">Этот метод группирования можно использовать, чтобы показать местоположение различных объектов, обслуживаемых вашей компанией.</span><span class="sxs-lookup"><span data-stu-id="57793-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="57793-108">Группирование объектов по географическому местоположению также может быть полезно, если, к примеру, необходимо идентифицировать объекты, которые ваша компания уже обслуживает в конкретной стране/регионе.</span><span class="sxs-lookup"><span data-stu-id="57793-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="57793-109">пример</span><span class="sxs-lookup"><span data-stu-id="57793-109">Example</span></span>

<span data-ttu-id="57793-110">В ваш сервисный центр позвонил клиент из Бельгии и желает заключить Соглашение о сервисном обслуживании объекта ABC.</span><span class="sxs-lookup"><span data-stu-id="57793-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="57793-111">Вы привязали группу объектов по географическому местоположению, Бельгия, ко всем объектам, которые обслуживаются в Бельгии.</span><span class="sxs-lookup"><span data-stu-id="57793-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="57793-112">С помощью этой группы в качестве фильтра, можно быстро найти, имеется ли уже запись для ABC в программе или ли необходимо настроить новый объект.</span><span class="sxs-lookup"><span data-stu-id="57793-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="57793-113">Группирование по типу</span><span class="sxs-lookup"><span data-stu-id="57793-113">Group by type</span></span>

<span data-ttu-id="57793-114">Этот метод группирования можно использовать, чтобы показать, какие типы объектов обслуживаются вашей компанией.</span><span class="sxs-lookup"><span data-stu-id="57793-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="57793-115">Группирование объектов по типу также может быть полезно, если, к примеру, необходимо создать новый объект на базе аналогичных объектов, уже существующих в программе.</span><span class="sxs-lookup"><span data-stu-id="57793-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="57793-116">пример</span><span class="sxs-lookup"><span data-stu-id="57793-116">Example</span></span>

<span data-ttu-id="57793-117">Звонит клиент и хочет заключить Соглашение о сервисном обслуживании установки кондиционирования воздуха, HIJ.</span><span class="sxs-lookup"><span data-stu-id="57793-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="57793-118">У вас еще нет записи для этой установки.</span><span class="sxs-lookup"><span data-stu-id="57793-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="57793-119">Однако вы уже настроили группу объектов "Кондиционеры воздуха", и вы привязали эту группу ко всем объектам кондиционирования воздуха.</span><span class="sxs-lookup"><span data-stu-id="57793-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="57793-120">Таким образом, можно быстро найти и определить все другие установки кондиционирования воздуха и использовать сведения из шаблонов из этих объектов, чтобы создать строки Соглашения о сервисном обслуживании для HIJ.</span><span class="sxs-lookup"><span data-stu-id="57793-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="57793-121">Используя группы объектов таким образом, можно быстро настроить новые объекты и определить Задачи сервисного обслуживания, которые должны выполняться на них.</span><span class="sxs-lookup"><span data-stu-id="57793-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 

## <a name="create-service-object-groups"></a><span data-ttu-id="57793-122">Создание групп объектов обслуживания</span><span class="sxs-lookup"><span data-stu-id="57793-122">Create service object groups</span></span>

<span data-ttu-id="57793-123">Создание групп, которые можно назначить объектам сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="57793-123">Create groups that you can assign service objects to.</span></span> <span data-ttu-id="57793-124">Объекты сервисного обслуживания — это складируемые номенклатуры и другие продукты, для которых выполняется сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="57793-124">Service objects are inventory items and other products for which services are performed.</span></span> <span data-ttu-id="57793-125">Сгруппировав объекты сервисного обслуживания, можно создать отчеты для подобных и связанных объектов сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="57793-125">By grouping service objects, you can create reports for similar and related service objects.</span></span> <span data-ttu-id="57793-126">Например, группа объектов сервисного обслуживания может состоять из двух объектов сервисного обслуживания, один из которых является комплектом, а второй — услугой по установке этого комплекта.</span><span class="sxs-lookup"><span data-stu-id="57793-126">For example, a service object group might consist of two service objects: One service object is a kit, and the second service object is the service to install the kit.</span></span>

<span data-ttu-id="57793-127">Чтобы создать группы объектов сервисного обслуживания, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="57793-127">To create service object groups, follow these steps:</span></span>

1. <span data-ttu-id="57793-128">Щелкните **Управление сервисным обслуживанием > Настройка > Объекты сервисного обслуживания > Группы объектов сервисного обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="57793-128">Click **Service management > Setup > Service objects > Service object groups**.</span></span>

2. <span data-ttu-id="57793-129">Щелкните **Создать**, чтобы создать новую группу объектов сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="57793-129">Click **New** to create a new service object group.</span></span>

3. <span data-ttu-id="57793-130">Введите уникальное имя группы объектов обслуживания и (по желанию) ее описание.</span><span class="sxs-lookup"><span data-stu-id="57793-130">Enter a unique name for the service object group and, optionally, a description.</span></span>

<span data-ttu-id="57793-131">Назначить объекты сервисного обслуживания группе можно с помощью формы **Объекты сервисного обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="57793-131">You can assign service objects to the group by using the **Service objects** form.</span></span> 

## <a name="see-also"></a><span data-ttu-id="57793-132">См. также</span><span class="sxs-lookup"><span data-stu-id="57793-132">See also</span></span>

[<span data-ttu-id="57793-133">Создание объектов обслуживания</span><span class="sxs-lookup"><span data-stu-id="57793-133">Create service objects</span></span>](create-service-objects.md)


