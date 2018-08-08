---
title: "Использование кодов оснований этапов"
description: "Код причины используется для указания причин отмены соглашения об уровне обслуживания (SLA) или превышения лимита времени выполнения заказа на обслуживания, предусмотренного SLA."
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 33fa7e5f08f09fe109d0507d686315d01e043928
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---


# <a name="use-stage-reason-codes"></a><span data-ttu-id="138b3-103">Использование кодов оснований этапов</span><span class="sxs-lookup"><span data-stu-id="138b3-103">Use stage reason codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="138b3-104">Код причины используется для указания причин отмены соглашения об уровне обслуживания (SLA) или превышения лимита времени выполнения заказа на обслуживания, предусмотренного SLA.</span><span class="sxs-lookup"><span data-stu-id="138b3-104">You use a reason code to indicate why a service level agreement (SLA) has been canceled, or why a service order has exceeded the time limit that is you define in the SLA.</span></span>

<span data-ttu-id="138b3-105">Можно также указать, что код причины является обязательным при отмене SLA или при превышении лимита времени, заданного в SLA для заказа на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="138b3-105">You can also specify that a reason code is required when an SLA is canceled, or when the time limit exceeds the time that is specified in the SLA for the service order.</span></span>

<span data-ttu-id="138b3-106">Если требуется указать код причины, необходимо ввести код причины в перечисленных ниже ситуациях.</span><span class="sxs-lookup"><span data-stu-id="138b3-106">If you have specified that a reason code is required, you must enter a reason code in the following situations:</span></span>

  - <span data-ttu-id="138b3-107">Заказ на обслуживание перешел на стадию, где отсчет времени по условиям SLA для заказа на обслуживание прекращается.</span><span class="sxs-lookup"><span data-stu-id="138b3-107">When a service order is moved to a stage that stops time recording against the SLA for the service order.</span></span>

  - <span data-ttu-id="138b3-108">Выход из заказа на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="138b3-108">When the service order is signed off.</span></span>

  - <span data-ttu-id="138b3-109">Регистрация времени прекращается вручную.</span><span class="sxs-lookup"><span data-stu-id="138b3-109">When time recording is manually stopped.</span></span>

## <a name="set-up-reason-codes"></a><span data-ttu-id="138b3-110">Настройка кодов причин</span><span class="sxs-lookup"><span data-stu-id="138b3-110">Set up reason codes</span></span>

1.  <span data-ttu-id="138b3-111">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Заказы на обслуживание** \> **Коды причин этапов**.</span><span class="sxs-lookup"><span data-stu-id="138b3-111">Click **Service management** \> **Setup** \> **Service orders** \> **Stage reason codes**.</span></span>

2.  <span data-ttu-id="138b3-112">В форме **Коды причин этапов** щелкните **Создать**, чтобы создать новый код причины.</span><span class="sxs-lookup"><span data-stu-id="138b3-112">In the **Stage reason codes** form, click **New** to create a new reason code.</span></span>

3.  <span data-ttu-id="138b3-113">В поле **Код причины этапа** введите уникальный код причины этапа.</span><span class="sxs-lookup"><span data-stu-id="138b3-113">In the **Stage reason code** field, enter a unique stage reason code.</span></span>

4.  <span data-ttu-id="138b3-114">В поле **Описание** введите описание кода причины этапа.</span><span class="sxs-lookup"><span data-stu-id="138b3-114">In the **Description** field, enter a description of the stage reason code.</span></span>

5.  <span data-ttu-id="138b3-115">Закройте форму, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="138b3-115">Close the form to save your changes.</span></span>

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a><span data-ttu-id="138b3-116">Требование кода причины при отмене соглашения об уровне обслуживания</span><span class="sxs-lookup"><span data-stu-id="138b3-116">Require reason codes when a service level agreement is canceled</span></span>

1.  <span data-ttu-id="138b3-117">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Параметры управления сервисным обслуживанием**.</span><span class="sxs-lookup"><span data-stu-id="138b3-117">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="138b3-118">В форме **Параметры управления сервисным обслуживанием** перейдите по ссылке **Общий** и установите флажок **Код основания при отмене**.</span><span class="sxs-lookup"><span data-stu-id="138b3-118">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on canceling** check box.</span></span>

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a><span data-ttu-id="138b3-119">Требование кода причины при превышении лимита времени, установленного соглашением об уровне обслуживания</span><span class="sxs-lookup"><span data-stu-id="138b3-119">Require reason codes when the a service order exceeds the time limit that is set by the service level agreement</span></span>

1.  <span data-ttu-id="138b3-120">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Параметры управления сервисным обслуживанием**.</span><span class="sxs-lookup"><span data-stu-id="138b3-120">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="138b3-121">В форме **Параметры управления сервисным обслуживанием** перейдите по ссылке **Общий** и установите флажок **Код основания при превышении по времени**.</span><span class="sxs-lookup"><span data-stu-id="138b3-121">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on exceeding time** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="138b3-122">См. также</span><span class="sxs-lookup"><span data-stu-id="138b3-122">See also</span></span>

[<span data-ttu-id="138b3-123">Начало и остановка записи времени в заказе на обслуживание</span><span class="sxs-lookup"><span data-stu-id="138b3-123">Start and stop time recording on a service order</span></span>](start-and-stop-time-recording-on-a-service-order.md)

  



