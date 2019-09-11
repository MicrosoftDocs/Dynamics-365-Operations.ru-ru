---
title: Запланированное выполнение
description: В этом разделе описывается запланированное выполнение в управлении активами.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8d9c8afc139c96e32efb3161d35fde685b8abcc5
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874678"
---
# <a name="scheduled-execution"></a><span data-ttu-id="89d59-103">Запланированное выполнение</span><span class="sxs-lookup"><span data-stu-id="89d59-103">Scheduled execution</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="89d59-104">Для настройки запланированного выполнения можно использовать уровни обслуживания заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="89d59-104">You can use work order service levels to set up scheduled execution.</span></span> <span data-ttu-id="89d59-105">(Дополнительные сведения о уровнях обслуживания заказов на работу см. в разделе [Уровень обслуживания и описание](service-level-and-description.md).) Запланированное выполнение предоставляет гибкие возможности планирования работы для специалистов по обслуживанию, так как можно настроить более подробные или менее детальные требования для интервала, в течение которого заказ на работу должен быть выполнен.</span><span class="sxs-lookup"><span data-stu-id="89d59-105">(For more information about work order service levels, see [Service level and description](service-level-and-description.md).) Scheduled execution provides flexibility in work planning for maintenance workers, because you can set up more detailed or less detailed requirements for the interval that a work order should be completed during.</span></span> <span data-ttu-id="89d59-106">Например, специалист по обслуживанию, который выполняет задание быстрее, чем ожидалось, на производственном оборудовании, может быть способен перейти на другое ближайшее задание, которое было запланировано на текущую неделю, но не обязательно на текущий день.</span><span class="sxs-lookup"><span data-stu-id="89d59-106">For example, a maintenance worker who completes a job faster than expected in a production facility might be able to move on to another nearby job that was planned for the current week but not necessarily for the current day.</span></span> <span data-ttu-id="89d59-107">Такой подход позволяет оптимизировать планирование работников и выполнение заданий.</span><span class="sxs-lookup"><span data-stu-id="89d59-107">This approach allows for optimization of worker planning and job completion.</span></span>

<span data-ttu-id="89d59-108">Настройка запланированного выполнения, которая относится к заказам на работу, может быть общей или специфической.</span><span class="sxs-lookup"><span data-stu-id="89d59-108">Scheduled execution setup, which is related to work orders, can be generic or specific.</span></span> <span data-ttu-id="89d59-109">Можно настроить универсальные строки, которые не ограничены конкретными типами заказов на работу, типами активов и т. д.</span><span class="sxs-lookup"><span data-stu-id="89d59-109">You can set up generic lines that aren't limited to specific work order types, asset types, and so on.</span></span> <span data-ttu-id="89d59-110">В качестве альтернативы можно создавать строки запланированного выполнения, которые применяются к конкретному типу заказа на работу, типу актива, типу задания обслуживания и т. д.</span><span class="sxs-lookup"><span data-stu-id="89d59-110">Alternatively, you can create scheduled execution lines that apply to a specific work order type, asset type, maintenance job type, and so on.</span></span>

1. <span data-ttu-id="89d59-111">Выберите **Управление активами** \> **Настройка** \> **Заказы на работу** \> **Запланированное выполнение**.</span><span class="sxs-lookup"><span data-stu-id="89d59-111">Select **Asset management** \> **Setup** \> **Work orders** \> **Scheduled execution**.</span></span>
2. <span data-ttu-id="89d59-112">Выберите **Создать**, чтобы создать строку запланированного выполнения.</span><span class="sxs-lookup"><span data-stu-id="89d59-112">Select **New** to create a scheduled execution line.</span></span>
3. <span data-ttu-id="89d59-113">Выберите нужные значения в полях **Функциональное местоположение**, **Тип заказа на работу**, **Тип актива**, **Производитель**, **Модель**, **Категория типов заданий на обслуживание**, **Тип заданий на обслуживание**, **Вариант типа задания на обслуживания** и **Специальность**.</span><span class="sxs-lookup"><span data-stu-id="89d59-113">In the **Functional location**, **Work order type**, **Asset type**, **Manufacturer**, **Model**, **Maintenance job type category**, **Maintenance job type**, **Maintenance job type variant**, and **Trade** fields, select values as you require.</span></span>
4. <span data-ttu-id="89d59-114">В поле **Уровень обслуживания** выберите уровень обслуживания задания на работу.</span><span class="sxs-lookup"><span data-stu-id="89d59-114">In the **Service level** field, select a work order service level.</span></span> <span data-ttu-id="89d59-115">Если вы оставляете это поле пустым, вы создаете самый общий тип строки запланированного выполнения.</span><span class="sxs-lookup"><span data-stu-id="89d59-115">If you leave this field blank, you make the most generic type of scheduled execution line.</span></span> <span data-ttu-id="89d59-116">Пример универсальной строки см. в первой записи на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="89d59-116">For an example of a generic line, see the first record in the illustration that follows.</span></span> <span data-ttu-id="89d59-117">Эта строка включает в себя все заказы на работу, для которых нет уровня обслуживания заказа на работу для планирования для определенной даты и времени.</span><span class="sxs-lookup"><span data-stu-id="89d59-117">That line enables all work orders that have no work order service level to be scheduled for a specific date and time.</span></span>
5. <span data-ttu-id="89d59-118">В поле **Запланированное выполнение** выберите интервал времени.</span><span class="sxs-lookup"><span data-stu-id="89d59-118">In the **Scheduled execution** field, select the time interval.</span></span>
6. <span data-ttu-id="89d59-119">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="89d59-119">Select **Save**.</span></span>

![Рисунок 1](media/20-setup-for-work-orders.png)