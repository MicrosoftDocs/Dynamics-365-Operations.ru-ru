---
title: "Настройка интервалов обслуживания"
description: "Интервал обслуживания определяет частоту, с которой строки заказа на обслуживание создаются для строк соглашения на обслуживание при автоматическом создании заказов на обслуживание."
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementinterval
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2b9146fe032e3ee248085713437faf5b9b219f9d
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-service-intervals"></a><span data-ttu-id="9271b-103">Настройка интервалов обслуживания</span><span class="sxs-lookup"><span data-stu-id="9271b-103">Set up service intervals</span></span>  

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="9271b-104">Интервал обслуживания определяет частоту, с которой строки заказа на обслуживание создаются для строк соглашения на обслуживание при автоматическом создании заказов на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9271b-104">Service interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders.</span></span>

1. <span data-ttu-id="9271b-105">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Соглашения на обслуживание** \> **Диапазоны сервисного обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="9271b-105">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="9271b-106">Создайте новый интервал сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9271b-106">Create a new service interval.</span></span>
3. <span data-ttu-id="9271b-107">Введите код и описание диапазона сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9271b-107">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="9271b-108">В поле **Диапазон** выберите диапазон.</span><span class="sxs-lookup"><span data-stu-id="9271b-108">In the **Range** field, select the range.</span></span>
5. <span data-ttu-id="9271b-109">В поле **Частота** введите частоту.</span><span class="sxs-lookup"><span data-stu-id="9271b-109">In the **Frequency** field, type the frequency.</span></span> <span data-ttu-id="9271b-110">Частота — это множитель, на который необходимо умножить диапазон, чтобы получить интервал соглашения о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="9271b-110">The frequency is the factor by which you must multiply the range to obtain the interval for a service agreement.</span></span>
6. <span data-ttu-id="9271b-111">Нажмите комбинацию клавиш **Alt+S**, чтобы сохранить интервал сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9271b-111">Press **Alt+S** to save the service interval.</span></span>

## <a name="example"></a><span data-ttu-id="9271b-112">Пример</span><span class="sxs-lookup"><span data-stu-id="9271b-112">Example</span></span>

<span data-ttu-id="9271b-113">Предположим, необходимо создать 10-дневный интервал сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9271b-113">You want to create a service interval of 10 days.</span></span>

<span data-ttu-id="9271b-114">**Создание 10-дневного интервала сервисного обслуживания**</span><span class="sxs-lookup"><span data-stu-id="9271b-114">**Create a 10-day service interval**</span></span>

1. <span data-ttu-id="9271b-115">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Соглашения на обслуживание** \> **Диапазоны сервисного обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="9271b-115">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="9271b-116">Создайте новый интервал сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9271b-116">Create a new service interval.</span></span>
3. <span data-ttu-id="9271b-117">Введите код и описание диапазона сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9271b-117">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="9271b-118">В поле **Диапазон** выберите **Ежедневно**.</span><span class="sxs-lookup"><span data-stu-id="9271b-118">In the **Range** field, select **Daily**.</span></span>
5. <span data-ttu-id="9271b-119">В поле **Частота** введите значение 10.</span><span class="sxs-lookup"><span data-stu-id="9271b-119">In the **Frequency** field, type 10.</span></span>
6. <span data-ttu-id="9271b-120">Нажмите комбинацию клавиш **Alt+S**, чтобы сохранить интервал сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9271b-120">Press **Alt+S** to save the service interval.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9271b-121">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="9271b-121">Related topics</span></span>

[<span data-ttu-id="9271b-122">Интервалы обслуживания</span><span class="sxs-lookup"><span data-stu-id="9271b-122">Service intervals</span></span>](service-intervals.md)  
