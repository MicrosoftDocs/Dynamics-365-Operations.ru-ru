---
title: "Группы объектов сервисного обслуживания"
description: "Группы объектов удобно использовать для сортировки и фильтрации данных по объектам в отчетах и статистике."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: fa503ac82286099a0eafc7034d169e165b538e2c
ms.contentlocale: ru-ru
ms.lasthandoff: 02/21/2018

---

# <a name="service-object-groups"></a><span data-ttu-id="078a0-103">Группы объектов сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="078a0-103">Service object groups</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="078a0-104">Группы объектов удобно использовать для сортировки и фильтрации данных по объектам в отчетах и статистике.</span><span class="sxs-lookup"><span data-stu-id="078a0-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="078a0-105">Например, можно сгруппировать объекты по географическому местоположению или по типу.</span><span class="sxs-lookup"><span data-stu-id="078a0-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="078a0-106">Группирование по географическому местоположению</span><span class="sxs-lookup"><span data-stu-id="078a0-106">Group by geographical location</span></span>

<span data-ttu-id="078a0-107">Этот метод группирования можно использовать, чтобы показать местоположение различных объектов, обслуживаемых вашей компанией.</span><span class="sxs-lookup"><span data-stu-id="078a0-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="078a0-108">Группирование объектов по географическому местоположению также может быть полезно, если, к примеру, необходимо идентифицировать объекты, которые ваша компания уже обслуживает в конкретной стране/регионе.</span><span class="sxs-lookup"><span data-stu-id="078a0-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="078a0-109">пример</span><span class="sxs-lookup"><span data-stu-id="078a0-109">Example</span></span>

<span data-ttu-id="078a0-110">В ваш сервисный центр позвонил клиент из Бельгии и желает заключить Соглашение о сервисном обслуживании объекта ABC.</span><span class="sxs-lookup"><span data-stu-id="078a0-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="078a0-111">Вы привязали группу объектов по географическому местоположению, Бельгия, ко всем объектам, которые обслуживаются в Бельгии.</span><span class="sxs-lookup"><span data-stu-id="078a0-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="078a0-112">С помощью этой группы в качестве фильтра, можно быстро найти, имеется ли уже запись для ABC в программе или ли необходимо настроить новый объект.</span><span class="sxs-lookup"><span data-stu-id="078a0-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="078a0-113">Группирование по типу</span><span class="sxs-lookup"><span data-stu-id="078a0-113">Group by type</span></span>

<span data-ttu-id="078a0-114">Этот метод группирования можно использовать, чтобы показать, какие типы объектов обслуживаются вашей компанией.</span><span class="sxs-lookup"><span data-stu-id="078a0-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="078a0-115">Группирование объектов по типу также может быть полезно, если, к примеру, необходимо создать новый объект на базе аналогичных объектов, уже существующих в программе.</span><span class="sxs-lookup"><span data-stu-id="078a0-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="078a0-116">пример</span><span class="sxs-lookup"><span data-stu-id="078a0-116">Example</span></span>

<span data-ttu-id="078a0-117">Звонит клиент и хочет заключить Соглашение о сервисном обслуживании установки кондиционирования воздуха, HIJ.</span><span class="sxs-lookup"><span data-stu-id="078a0-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="078a0-118">У вас еще нет записи для этой установки.</span><span class="sxs-lookup"><span data-stu-id="078a0-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="078a0-119">Однако вы уже настроили группу объектов "Кондиционеры воздуха", и вы привязали эту группу ко всем объектам кондиционирования воздуха.</span><span class="sxs-lookup"><span data-stu-id="078a0-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="078a0-120">Таким образом, можно быстро найти и определить все другие установки кондиционирования воздуха и использовать сведения из шаблонов из этих объектов, чтобы создать строки Соглашения о сервисном обслуживании для HIJ.</span><span class="sxs-lookup"><span data-stu-id="078a0-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="078a0-121">Используя группы объектов таким образом, можно быстро настроить новые объекты и определить Задачи сервисного обслуживания, которые должны выполняться на них.</span><span class="sxs-lookup"><span data-stu-id="078a0-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 




