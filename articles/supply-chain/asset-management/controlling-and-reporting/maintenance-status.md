---
title: Статус обслуживания
description: В этом разделе объясняется, как рассчитать статус обслуживания в модуле "Управление активами".
author: josaw1
manager: tfehr
ms.date: 08/23/2019
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
ms.openlocfilehash: fbe2b3fd9ce63c34aedb790583dea572d3d9b079
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205486"
---
# <a name="maintenance-status"></a><span data-ttu-id="a1210-103">Статус обслуживания</span><span class="sxs-lookup"><span data-stu-id="a1210-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a1210-104">В управлении активами можно выполнить обзорный расчет за определенный период для новых, активных и завершенных запросов на обслуживание, заказов на работу и мероприятий по простою из-за обслуживания для конкретного периода.</span><span class="sxs-lookup"><span data-stu-id="a1210-104">In Asset Management, you can make an overview calculation for a specific period for new, active, and completed maintenance requests, work orders, and maintenance downtime activities.</span></span> <span data-ttu-id="a1210-105">Можно также просмотреть число выполненных оценок условий для того же периода.</span><span class="sxs-lookup"><span data-stu-id="a1210-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="a1210-106">Используйте этот расчет для получения обзора рабочей нагрузки для входящих и завершенных запросов обслуживания и заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="a1210-106">Use this calculation to get an overview of workload for incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="a1210-107">Выполнение расчета статуса обслуживания</span><span class="sxs-lookup"><span data-stu-id="a1210-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="a1210-108">Щелкните **Управление активами** > **Запросы** > **Статус обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="a1210-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="a1210-109">В диалоговом окне **Статус обслуживания** выберите диапазон времени, для которого необходимо выполнить расчет, в полях **Начальная дата** и **Конечная дата**.</span><span class="sxs-lookup"><span data-stu-id="a1210-109">In the **Calculate status** dialog, select the time range that you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="a1210-110">Можно использовать поле **Уровень**, чтобы указать, насколько подробными должны быть строки обслуживания относительно функциональных местоположений.</span><span class="sxs-lookup"><span data-stu-id="a1210-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> 

  <span data-ttu-id="a1210-111">Например, если вставить число "1" в это поле, и имеется структура функциональных местоположений с несколькими уровнями, все строки обслуживания для функционального местоположения будут показаны на верхнем уровне, и поэтому статус по строке может быть добавлен из функциональных местоположений, расположенных на более низком уровне.</span><span class="sxs-lookup"><span data-stu-id="a1210-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> 
  
  <span data-ttu-id="a1210-112">Если вставить число "0" в поле **Уровень**, будет выведен подробный результат, отображающий все строки обслуживания на всех уровнях функциональных местоположений, к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="a1210-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="a1210-113">Нажмите **ОК**, чтобы начать расчет.</span><span class="sxs-lookup"><span data-stu-id="a1210-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="a1210-114">Щелкните кнопки **Группировать по...**, чтобы отобразить необходимый уровень детализации для расчета.</span><span class="sxs-lookup"><span data-stu-id="a1210-114">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="a1210-115">Выбранные кнопки **Группировать по...** выделяются.</span><span class="sxs-lookup"><span data-stu-id="a1210-115">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="a1210-116">Нажимайте кнопку, чтобы активировать или деактивировать ее.</span><span class="sxs-lookup"><span data-stu-id="a1210-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="a1210-117">Не забудьте нажать кнопку **Обновить** для обновления вычислений при каждом внесении изменений путем активации или деактивации кнопок **Группировать по** или путем выполнения расчета для нового периода.</span><span class="sxs-lookup"><span data-stu-id="a1210-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="a1210-118">Щелкните **Статус**, если необходимо создать новый расчет статуса обслуживания.</span><span class="sxs-lookup"><span data-stu-id="a1210-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="a1210-119">Результаты, отображаемые в **Статус обслуживания**, включают только запросы на обслуживание и заказы на работу, имеющие фактические дату и время начала.</span><span class="sxs-lookup"><span data-stu-id="a1210-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="a1210-120">Дата и время окончания могут быть пустыми.</span><span class="sxs-lookup"><span data-stu-id="a1210-120">End date and time may be blank.</span></span>

## <a name="example-1"></a><span data-ttu-id="a1210-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a1210-121">Example 1</span></span>

<span data-ttu-id="a1210-122">На приведенном ниже снимке экрана активизированы кнопки **Год** и **Месяц**.</span><span class="sxs-lookup"><span data-stu-id="a1210-122">In the screenshot below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="a1210-123">Выбрав эти параметры **Группировать по**, вы получаете общий обзор ежемесячной рабочей нагрузки и пропускной способности, связанный с запросами на обслуживание и заказами на работу.</span><span class="sxs-lookup"><span data-stu-id="a1210-123">With these **Group by** options selected, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![Пример месячной рабочей нагрузки](media/13-controlling-and-reporting.png)

## <a name="example-2"></a><span data-ttu-id="a1210-125">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a1210-125">Example 2</span></span>

<span data-ttu-id="a1210-126">На приведенном ниже снимке экрана были добавлены сведения о функциональных местоположениях.</span><span class="sxs-lookup"><span data-stu-id="a1210-126">In the screenshot below, information about functional locations has been added.</span></span> <span data-ttu-id="a1210-127">Теперь можно сравнить рабочую нагрузку и пропускную способность между функциональными местоположениями, которые могут представлять географические местоположения, фабрики или рабочие области.</span><span class="sxs-lookup"><span data-stu-id="a1210-127">Now it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![Пример месячной нагрузки с функциональными местоположениями](media/14-controlling-and-reporting.png)

