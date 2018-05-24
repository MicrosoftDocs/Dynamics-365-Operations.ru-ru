---
title: "Начало и остановка записи времени в заказе на обслуживание"
description: "Начало и остановка записи времени в заказе на обслуживание."
author: YuyuScheller
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ba962dddcdda4d772dd7e6c08f7adb326be21271
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="start-and-stop-time-recording-on-a-service-order"></a><span data-ttu-id="dcbdf-103">Начало и остановка записи времени в заказе на обслуживание</span><span class="sxs-lookup"><span data-stu-id="dcbdf-103">Start and stop time recording on a service order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="dcbdf-104">Данная процедура используется для запуска и остановки записи времени для заказа на сервисное обслуживание, для которого определено соглашение об условиях обслуживания.</span><span class="sxs-lookup"><span data-stu-id="dcbdf-104">Use this procedure to start and stop time recording for a service order for which a service level agreement is defined.</span></span>

## <a name="start-time-recording"></a><span data-ttu-id="dcbdf-105">Начало записи времени</span><span class="sxs-lookup"><span data-stu-id="dcbdf-105">Start time recording</span></span>

1.  <span data-ttu-id="dcbdf-106">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Заказы на сервисное обслуживание** \> **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="dcbdf-106">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="dcbdf-107">Перейдите на вкладку **Заказ на сервисное обслуживание**. В разделе **Панель операций**, в группе **Соглашение об уровне обслуживания** щелкните **Начать**.</span><span class="sxs-lookup"><span data-stu-id="dcbdf-107">Click the **Service order** tab. On the **Action Pane**, in the **Service level agreement** group, click **Start**.</span></span>

3.  <span data-ttu-id="dcbdf-108">Введите дату и время, когда запись времени должна быть начата.</span><span class="sxs-lookup"><span data-stu-id="dcbdf-108">Enter the date and time that the time recording should be started.</span></span>

## <a name="stop-time-recording"></a><span data-ttu-id="dcbdf-109">Прекращение учета времени</span><span class="sxs-lookup"><span data-stu-id="dcbdf-109">Stop time recording</span></span>

1.  <span data-ttu-id="dcbdf-110">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Заказы на сервисное обслуживание** \> **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="dcbdf-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="dcbdf-111">Перейдите на вкладку **Заказ на сервисное обслуживание**. В разделе **Панель операций**, в группе **Соглашение об уровне обслуживания** щелкните **Остановить**.</span><span class="sxs-lookup"><span data-stu-id="dcbdf-111">Click the **Service order** tab. On the **Action Pane**, in the **Service level agreement** group, click **Stop**.</span></span>

3.  <span data-ttu-id="dcbdf-112">Введите дату и время, когда запись времени должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="dcbdf-112">Enter the date and time that the time recording should be stopped.</span></span>

4.  <span data-ttu-id="dcbdf-113">Выберите **Добавить причину отзыва**, а затем выберите код причины в списке **Код причины этапа**, чтобы указать причину остановки записи времени.</span><span class="sxs-lookup"><span data-stu-id="dcbdf-113">Select **Add a revocation reason**, and select a reason code in the **Stage reason code** list to provide a reason for stopping the time recording.</span></span>


> [!NOTE]
> <P><span data-ttu-id="dcbdf-114">Если в форме <STRONG>Параметры управления сервисным обслуживанием</STRONG> выбрано <STRONG>Код основания при превышении по времени</STRONG>, необходимо указать код причины, прежде чем можно будет остановить запись времени.</span><span class="sxs-lookup"><span data-stu-id="dcbdf-114">If <STRONG>Reason code on exceeding time</STRONG> is selected in the <STRONG>Service management parameters</STRONG> form, you must provide a reason code before you can stop the time recording.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="dcbdf-115">См. также</span><span class="sxs-lookup"><span data-stu-id="dcbdf-115">See also</span></span>

<span data-ttu-id="dcbdf-116">[Начало учета времени SLA (форма)](https://technet.microsoft.com/en-us/library/hh242297\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="dcbdf-116">[Start SLA time recording (form)](https://technet.microsoft.com/en-us/library/hh242297\(v=ax.60\))</span></span>

<span data-ttu-id="dcbdf-117">[Прекращение учета времени SLA (форма)](https://technet.microsoft.com/en-us/library/hh242241\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="dcbdf-117">[Stop SLA time recording (form)](https://technet.microsoft.com/en-us/library/hh242241\(v=ax.60\))</span></span>

  



