---
title: Автоматическое создание заказов на обслуживание
description: Можно создать заказы на сервисное обслуживание, на основе соглашения о сервисном обслуживании на период действия соглашения на сервисное обслуживание.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08fb7363ab87fd6a7f3d38406e72b1f542dc2c2a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436217"
---
# <a name="automatically-create-service-orders"></a><span data-ttu-id="43def-103">Автоматическое создание заказов на обслуживание</span><span class="sxs-lookup"><span data-stu-id="43def-103">Automatically create service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="43def-104">Можно создать заказы на сервисное обслуживание, на основе соглашения о сервисном обслуживании на период действия соглашения на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="43def-104">You can generate service orders that are based on a service agreement for the valid period of the service agreement.</span></span>

<span data-ttu-id="43def-105">Заказы на сервисное обслуживание, генерируемые на основании соглашений на сервисное обслуживание, присоединяются к соглашению на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="43def-105">The service orders that you generate from a service agreement are all attached to the service agreement.</span></span>

<span data-ttu-id="43def-106">Заказы на обслуживание генерируются автоматически по следующим настройкам:</span><span class="sxs-lookup"><span data-stu-id="43def-106">Service orders are generated automatically from the following settings:</span></span>

  - <span data-ttu-id="43def-107">Интервал соглашения на сервисное обслуживание, настроенный в строках соглашения на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="43def-107">The service agreement interval that is set up in the service agreement lines.</span></span> <span data-ttu-id="43def-108">Интервал соглашения на сервисное обслуживание определяет частоту, с которой создаются строки заказа на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="43def-108">The service agreement interval indicates the frequency that service-order lines are created.</span></span> <span data-ttu-id="43def-109">Дополнительные сведения см. в разделе [Диапазоны сервисного обслуживания](service-intervals.md).</span><span class="sxs-lookup"><span data-stu-id="43def-109">For more information, see [Service intervals](service-intervals.md).</span></span>

  - <span data-ttu-id="43def-110">Период обслуживания, указываемый в полях **Дата начала** и **Дата окончания** и в форме **Создать заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="43def-110">The period that you specify to define the service period in the **From date** and **To date** fields in the **Create service orders** form.</span></span> <span data-ttu-id="43def-111">Дополнительные сведения см. в разделе [Автоматическое создание заказов на обслуживание](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="43def-111">For more information, see [Create service orders automatically](create-service-orders-automatically.md).</span></span>

  - <span data-ttu-id="43def-112">Параметр **Объединение заказов на сервисное обслуживание** в заголовке соглашения о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="43def-112">The **Combine service orders** option on the service agreement header.</span></span> <span data-ttu-id="43def-113">Этот параметр определяет, созданы ли строки заказа на сервисное обслуживание из соглашения на сервисное обслуживание, объединяет заказы на сервисное обслуживание по сотруднику, задаче сервисного обслуживания, объекту сервисного обслуживания или соглашению на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="43def-113">This option defines whether service order lines generated from a service agreement, combines service orders according to employee, service task, service object, or service agreement.</span></span> <span data-ttu-id="43def-114">Дополнительные сведения см. в разделе [Объединение заказов на сервисное обслуживание](combine-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="43def-114">For more information, see [Combine service orders](combine-service-orders.md).</span></span>

  - <span data-ttu-id="43def-115">Параметр **Окно времени** в строке соглашения о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="43def-115">The **Time window** option on the service agreement line.</span></span> <span data-ttu-id="43def-116">Окна времени определяют, как далеко можно передвинуть строку заказа на сервисное обслуживание относительно ее рассчитанной даты.</span><span class="sxs-lookup"><span data-stu-id="43def-116">The time window defines how far a service order line can move with regard to its calculated date.</span></span> <span data-ttu-id="43def-117">Дополнительные сведения см. в разделе [Окна времени](time-windows.md).</span><span class="sxs-lookup"><span data-stu-id="43def-117">For more information, see [Time windows](time-windows.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="43def-118">Если день, указанный для заказа на сервисное обслуживание, не открыт в календаре, выбранном в форме <STRONG>Параметры управления сервисным обслуживанием</STRONG>, вы получите сообщение о конфликте календарей.</span><span class="sxs-lookup"><span data-stu-id="43def-118">If the day that is specified for a service order is not open in the calendar that you have selected in the <STRONG>Service management parameters</STRONG> form, a message will indicate that there is a calendar conflict.</span></span> <span data-ttu-id="43def-119">Это сообщение можно игнорировать, и заказ на сервисное обслуживание будет создан даже в том случае, если указанный день в календаре закрыт.</span><span class="sxs-lookup"><span data-stu-id="43def-119">You can safely ignore the message; the service order will be created, even though the day is closed on the calendar.</span></span></P>

## <a name="example-1"></a><span data-ttu-id="43def-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="43def-120">Example 1</span></span>

<span data-ttu-id="43def-121">Соглашение о сервисном обслуживании действует с 1 января 2012 г. до 31 декабря 2012 г.</span><span class="sxs-lookup"><span data-stu-id="43def-121">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="43def-122">Если период сервисное обслуживания, указанный в форме **Создать заказы на сервисное обслуживание** начинается с 1 ноября 2012 г. и заканчивается 1 февраля 2013 г., заказы на сервисное обслуживание создаются начиная с 1 ноября 2012 г. до 31 декабря 2012 г.</span><span class="sxs-lookup"><span data-stu-id="43def-122">If the service period that you specify in the **Create service orders** form is from November 1, 2012 until February 1, 2013, service orders are created from November 1, 2012 until December 31, 2012.</span></span>

## <a name="example-2"></a><span data-ttu-id="43def-123">Пример 2</span><span class="sxs-lookup"><span data-stu-id="43def-123">Example 2</span></span>

<span data-ttu-id="43def-124">Соглашение о сервисном обслуживании действует с 1 января 2012 г. до 31 декабря 2012 г.</span><span class="sxs-lookup"><span data-stu-id="43def-124">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="43def-125">К соглашению прикреплено две строки соглашения о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="43def-125">Two service agreement lines are attached to the service agreement.</span></span> <span data-ttu-id="43def-126">Первая строка соглашения о сервисном обслуживании имеет дату начала 2 января 2012 г. и дату окончания 1 марта 2012 г.</span><span class="sxs-lookup"><span data-stu-id="43def-126">The first service agreement line has a starting date on January 2, 2012 and an ending date on March 1, 2012.</span></span> <span data-ttu-id="43def-127">Вторая строка соглашения о сервисном обслуживании имеет дату начала 1 апреля 2012 г. и дату окончания 31 декабря 2012 г.</span><span class="sxs-lookup"><span data-stu-id="43def-127">The second service agreement line has a starting date on April 1, 2012 and an ending date on December 31, 2012.</span></span> <span data-ttu-id="43def-128">Можно указать период в форме **Создать заказы на сервисное обслуживание** начиная с 1 октября 2012 г. до 31 декабря 2012 г.</span><span class="sxs-lookup"><span data-stu-id="43def-128">You specify a period in the **Create service orders** form that is from October 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="43def-129">Таким образом, заказы на обслуживание создаются только по второй строке соглашения, так как даты начала и окончания первой строки лежат ранее периода, указанного для заказа на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="43def-129">Therefore, service orders are generated only for the second agreement line, because the starting date and ending date of the first agreement line are before the period that you specified for the service order.</span></span>

  


