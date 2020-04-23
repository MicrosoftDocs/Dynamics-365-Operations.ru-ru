---
title: Создание заказов на работу
description: В этом разделе описывается, как создавать заказы на работу в модуле "Управление активами".
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f94f8bc20753e38ce1cb6eccdfbc85c2e491ffad
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206135"
---
# <a name="creating-work-orders"></a><span data-ttu-id="6edfd-103">Создание заказов на работу</span><span class="sxs-lookup"><span data-stu-id="6edfd-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6edfd-104">После планирования заданий профилактического обслуживания следующим шагом будет создание заказов на работу для этих заданий.</span><span class="sxs-lookup"><span data-stu-id="6edfd-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="6edfd-105">Это делается в одном из графиков обслуживания.</span><span class="sxs-lookup"><span data-stu-id="6edfd-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="6edfd-106">Запланированные задания в графике обслуживания могут иметь различные типы ссылок:</span><span class="sxs-lookup"><span data-stu-id="6edfd-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="6edfd-107">Тип ссылки</span><span class="sxs-lookup"><span data-stu-id="6edfd-107">Reference type</span></span> | <span data-ttu-id="6edfd-108">Описание</span><span class="sxs-lookup"><span data-stu-id="6edfd-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6edfd-109">Планы обслуживания</span><span class="sxs-lookup"><span data-stu-id="6edfd-109">Maintenance plans</span></span>     | <span data-ttu-id="6edfd-110">Задание профилактического обслуживания должно основываться на типах планов обслуживания "Время" или "Счетчик".</span><span class="sxs-lookup"><span data-stu-id="6edfd-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="6edfd-111">Циклы обслуживания</span><span class="sxs-lookup"><span data-stu-id="6edfd-111">Maintenance rounds</span></span>    | <span data-ttu-id="6edfd-112">Задания профилактического обслуживания, содержащие несколько активов, требующих подобного типа обслуживания.</span><span class="sxs-lookup"><span data-stu-id="6edfd-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="6edfd-113">Запрос на обслуживание</span><span class="sxs-lookup"><span data-stu-id="6edfd-113">Maintenance request</span></span>   | <span data-ttu-id="6edfd-114">Запрос, созданный вручную для обслуживания или ремонта актива, который может быть преобразован в заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="6edfd-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="6edfd-115">Щелкните **Управление активами** > **Общее** > **Весь график обслуживания**, **Открыть строки графика обслуживания** или **Открыть пулы графиков обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="6edfd-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="6edfd-116">Выберите запланированные задания обслуживание, для которых необходимо создать заказ на работу, и щелкните **Заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="6edfd-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="6edfd-117">В диалоговом окне **Создание заказов на работу** общее количество часов прогноза для выбранных строк отображается в поле **Прогноз часов обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="6edfd-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="6edfd-118">В разделе **Параметры** выберите количество заказов на работу, которые должны быть созданы.</span><span class="sxs-lookup"><span data-stu-id="6edfd-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="6edfd-119">Можно создать один заказ на работу для каждой строки графика обслуживания или несколько заказов на работу на основе выбранных значений в разделе **Один заказ на работу на**.</span><span class="sxs-lookup"><span data-stu-id="6edfd-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="6edfd-120">Выберите **Тип заказа на работу**, который будет использоваться для всех создаваемых заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="6edfd-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="6edfd-121">На приведенном ниже рисунке показан пример диалогового окна **Создание заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="6edfd-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![Рисунок 1](media/18-preventive-maintenance.png)

5. <span data-ttu-id="6edfd-123">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="6edfd-123">Click **OK**.</span></span> <span data-ttu-id="6edfd-124">Создан один или несколько заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="6edfd-124">One or more work orders are created.</span></span>

