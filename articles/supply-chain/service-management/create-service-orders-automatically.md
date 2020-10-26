---
title: Автоматическое создание заказов на сервисное обслуживание
description: Заказы на сервисное обслуживание можно создавать для одного или нескольких соглашений о сервисном обслуживании.
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
ms.openlocfilehash: 914df1626b02110264b895e82dc9301f3aa0afce
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985126"
---
# <a name="create-service-orders-automatically"></a><span data-ttu-id="d4108-103">Автоматическое создание заказов на сервисное обслуживание</span><span class="sxs-lookup"><span data-stu-id="d4108-103">Create service orders automatically</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d4108-104">Заказы на сервисное обслуживание можно создавать для одного или нескольких соглашений о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="d4108-104">You can create service orders for one service agreement or for several service agreements.</span></span> <span data-ttu-id="d4108-105">После создания заказов их можно просмотреть в форме **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="d4108-105">When they are created, you can view your service orders in the **Service orders** form.</span></span>

<span data-ttu-id="d4108-106">Заказы на сервисное обслуживание можно создавать только на период действия соглашения о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="d4108-106">Service orders are created only for the valid period of the service agreement.</span></span> <span data-ttu-id="d4108-107">Если интервал, указанный в форме **Создать заказы на сервисное обслуживание**, приходится на период до начальной или конечной даты соглашения о сервисном обслуживании, заказы на сервисное обслуживание будут созданы только на ту часть периода, который находится в пределах дат соглашения о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="d4108-107">If the interval that you specify in the **Create service orders** form is before the starting date or after the ending date of the service agreement, service orders are created only for the part of the interval that is within the service agreement dates.</span></span>

<span data-ttu-id="d4108-108">При создании (вручную или автоматически) заказов на сервисное обслуживание из данной строки соглашения о сервисном обслуживании заказ на сервисное обслуживание должен попадать в интервал времени, определенный начальной и конечной датами для строки, кроме случаев, когда конечная дата в строке не указана.</span><span class="sxs-lookup"><span data-stu-id="d4108-108">When you create service orders manually or automatically from the service agreement line, the service order must be in the time interval that is defined by the starting and ending dates for the line, unless you do not specify an ending date on the line.</span></span>

## <a name="create-service-orders-automatically-for-a-service-agreement"></a><span data-ttu-id="d4108-109">Автоматическое создание заказов на обслуживание для соглашения на обслуживание</span><span class="sxs-lookup"><span data-stu-id="d4108-109">Create service orders automatically for a service agreement</span></span>

1.  <span data-ttu-id="d4108-110">Щелкните **Управление сервисным обслуживанием** \> **Общее** \> **Соглашения на обслуживание** \> **Соглашения на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="d4108-110">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="d4108-111">Выберите соглашение на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d4108-111">Select a service agreement.</span></span>

3.  <span data-ttu-id="d4108-112">Перейдите на вкладку **Доставлять** и щелкните **Планируемые заказы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="d4108-112">Click the **Deliver** tab, and then click **Planned service orders**.</span></span>

4.  <span data-ttu-id="d4108-113">Укажите даты в полях **Дата начала** и **Дата окончания**, чтобы определить период обслуживания.</span><span class="sxs-lookup"><span data-stu-id="d4108-113">Specify dates in the **From date** and **To date** fields to define the service period.</span></span>

5.  <span data-ttu-id="d4108-114">Установите флажок **Отобразить Infolog**, чтобы отобразить список созданных заказов на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d4108-114">Select the **Show Infolog** check box to display a list of the service orders that are created.</span></span>

6.  <span data-ttu-id="d4108-115">Выберите типы проводок в группе полей **Включить проводки вида**.</span><span class="sxs-lookup"><span data-stu-id="d4108-115">Select transaction types in the **Include transaction types** field group.</span></span> <span data-ttu-id="d4108-116">Типы проводок соответствуют строкам, созданным в соглашении на обслуживание, и для каждого из выбранных типов проводок создается несколько заказов на обслуживание, в зависимости от интервала обслуживания, указанного в строке соглашения на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d4108-116">The transaction types represent the lines that are created in the service agreement, and each transaction type that you select generates several service orders, depending on the service interval that is specified on the service agreement line.</span></span>

7.  <span data-ttu-id="d4108-117">Для создания заказов на сервисное обслуживание, которых не хватает в последовательной серии заказов на сервисное обслуживание, установите флажок **Непрерывная**.</span><span class="sxs-lookup"><span data-stu-id="d4108-117">To create any service orders that are missing from continuous series of service orders, select the **Continuous** check box.</span></span>

8.  <span data-ttu-id="d4108-118">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d4108-118">Click **OK**.</span></span>

## <a name="create-service-orders-automatically-for-several-service-agreements"></a><span data-ttu-id="d4108-119">Автоматическое создание заказов на обслуживание для нескольких соглашений на обслуживание</span><span class="sxs-lookup"><span data-stu-id="d4108-119">Create service orders automatically for several service agreements</span></span>

1.  <span data-ttu-id="d4108-120">Щелкните **Управление сервисным обслуживанием** \> **Периодические операции** \> **Заказы на сервисное обслуживание** \> **Создание заказов на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="d4108-120">Click **Service management** \> **Periodic** \> **Service orders** \> **Create service orders**.</span></span>

2.  <span data-ttu-id="d4108-121">Щелкните **Выбрать** и добавьте или удалите критерии, которые будут использоваться при создании заказов на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d4108-121">Click **Select** to make selections to add or remove criteria to use to create service orders.</span></span>

3.  <span data-ttu-id="d4108-122">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="d4108-122">Click **OK**.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4108-123">См. также</span><span class="sxs-lookup"><span data-stu-id="d4108-123">See also</span></span>

[<span data-ttu-id="d4108-124">Заказы на сервисное обслуживание</span><span class="sxs-lookup"><span data-stu-id="d4108-124">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="d4108-125">Автоматическое создание заказов на сервисное обслуживание</span><span class="sxs-lookup"><span data-stu-id="d4108-125">Automatically create service orders</span></span>](auto-create-service-orders.md)

  


