---
title: Окна времени
description: Окна времени можно использовать для оптимизации планирования строк заказа на обслуживание.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f64718e6a96cacc005644cbf4286e743111c02f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996510"
---
# <a name="time-windows"></a><span data-ttu-id="58935-103">Окна времени</span><span class="sxs-lookup"><span data-stu-id="58935-103">Time windows</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="58935-104">Окна времени можно использовать для оптимизации планирования строк заказа на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="58935-104">You can use time windows to optimize the scheduling of service order lines.</span></span> <span data-ttu-id="58935-105">Вы можете настроить систему, чтобы она автоматически создавала заказы на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="58935-105">You can set up the system so that it automatically creates service orders.</span></span> <span data-ttu-id="58935-106">На основе критериев, заданных временным окном, можно подключить столько строк заказа на обслуживание, сколько возможно, к наименьшему возможному число заказов на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="58935-106">Based on the criteria specified by a time window, you can connect as many service order lines as possible to as few service orders as possible.</span></span>

<span data-ttu-id="58935-107">Окна времени определяют, как далеко можно передвинуть строку заказа на обслуживание относительно ее рассчитанной даты.</span><span class="sxs-lookup"><span data-stu-id="58935-107">Time windows specify how far a service order line can move from its calculated date.</span></span> <span data-ttu-id="58935-108">Дата, рассчитанная как дата, на которую была запланирована строка заказа на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="58935-108">The calculated date is the date when the service order line was scheduled to occur.</span></span> <span data-ttu-id="58935-109">Дата основана на настройках интервала и периода обслуживания, указанных на странице **Создать заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="58935-109">The date is based on its interval setting and the service period that you defined in the **Create service orders** page.</span></span> <span data-ttu-id="58935-110">Окно времени определяется с использованием значений в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="58935-110">You define a time window by using the values in the following table.</span></span>

| <span data-ttu-id="58935-111">Метод</span><span class="sxs-lookup"><span data-stu-id="58935-111">Method</span></span> | <span data-ttu-id="58935-112">описание</span><span class="sxs-lookup"><span data-stu-id="58935-112">Description</span></span>                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58935-113">Неделя</span><span class="sxs-lookup"><span data-stu-id="58935-113">Week</span></span>   | <span data-ttu-id="58935-114">Дату выполнения этой строки заказа на обслуживание можно переместить на любой открытый день в пределах той недели, к которой относится исходная рассчитанная дата.</span><span class="sxs-lookup"><span data-stu-id="58935-114">The date that the service order line can be moved to any open day in the same week as the initial calculated date.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="58935-115">Месяц</span><span class="sxs-lookup"><span data-stu-id="58935-115">Month</span></span>  | <span data-ttu-id="58935-116">Дату выполнения этой строки заказа на обслуживание можно переместить на любой открытый день в пределах того месяца, к которому относится исходная рассчитанная дата.</span><span class="sxs-lookup"><span data-stu-id="58935-116">The date that the service order line can be moved to any open day in the same month as the initial calculated date.</span></span> <span data-ttu-id="58935-117">Например, рассчитанная дата для строки заказа на обслуживание имеет значение 15 февраля 2017 г.</span><span class="sxs-lookup"><span data-stu-id="58935-117">For example, the calculated date for a service order line is February 15, 2017.</span></span> <span data-ttu-id="58935-118">Строку заказа на обслуживание можно запланировать на любой рабочий день между 1 февраля и 28 февраля 2017 г.</span><span class="sxs-lookup"><span data-stu-id="58935-118">The service order line can be scheduled for any weekday between February 1 and February 28, 2017.</span></span> |
| <span data-ttu-id="58935-119">Руководство</span><span class="sxs-lookup"><span data-stu-id="58935-119">Manual</span></span> | <span data-ttu-id="58935-120">Определяется максимальное количество дней до или после исходной рассчитанной даты, на которое можно переместить эту строку заказа на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="58935-120">You define the maximum number of days before or after the initial calculated date that the service order line can be moved.</span></span>                                                                                                                                                                           |

<span data-ttu-id="58935-121">Если для строки соглашения на обслуживание не задано окно времени, то строка заказа на обслуживание, являющаяся производной от этого соглашения на обслуживание, должна быть выполнена именно в ту дату, на которую эта строка была первоначально запланирована.</span><span class="sxs-lookup"><span data-stu-id="58935-121">If you do not specify a time window for a service agreement line, the service order line that is derived from the service agreement must be on the exact date for which it was originally scheduled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58935-122">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="58935-122">Related topics</span></span>

[<span data-ttu-id="58935-123">Создание окон времени</span><span class="sxs-lookup"><span data-stu-id="58935-123">Create time windows</span></span>](create-time-windows.md)

