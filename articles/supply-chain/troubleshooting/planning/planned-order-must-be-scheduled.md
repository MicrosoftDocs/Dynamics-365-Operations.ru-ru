---
title: Спланированный производственный заказ должен быть запланирован до утверждения
description: При попытке утверждения спланированного заказа выводится сообщение об ошибке, в котором указывается, что заказ должен быть запланирован до утверждения.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294168"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a><span data-ttu-id="05ab4-103">Спланированный производственный заказ должен быть запланирован до утверждения</span><span class="sxs-lookup"><span data-stu-id="05ab4-103">Planned production order must be scheduled before it can be firmed</span></span>

<span data-ttu-id="05ab4-104">Код ошибки: SYS309802</span><span class="sxs-lookup"><span data-stu-id="05ab4-104">Error code: SYS309802</span></span>

## <a name="symptoms"></a><span data-ttu-id="05ab4-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="05ab4-105">Symptoms</span></span>

<span data-ttu-id="05ab4-106">При попытке утвердить спланированный заказ выводится следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="05ab4-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="05ab4-107">Спланированный производственный заказ необходимо запланировать до его утверждения.</span><span class="sxs-lookup"><span data-stu-id="05ab4-107">The planned production order must be scheduled before it can be firmed.</span></span>

## <a name="cause"></a><span data-ttu-id="05ab4-108">Причина</span><span class="sxs-lookup"><span data-stu-id="05ab4-108">Cause</span></span>

<span data-ttu-id="05ab4-109">Запланированные даты начала и окончания не могут быть пустыми.</span><span class="sxs-lookup"><span data-stu-id="05ab4-109">The scheduled start and end dates can't be blank.</span></span>

## <a name="resolution"></a><span data-ttu-id="05ab4-110">Решение</span><span class="sxs-lookup"><span data-stu-id="05ab4-110">Resolution</span></span>

<span data-ttu-id="05ab4-111">Чтобы указать даты начала и окончания для спланированного заказа, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="05ab4-111">To specify start and end dates for the planned order, follow these steps.</span></span>

1. <span data-ttu-id="05ab4-112">Перейдите в раздел **Сводное планирование \> Сводное планирование \> Спланированные заказы**.</span><span class="sxs-lookup"><span data-stu-id="05ab4-112">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="05ab4-113">Откройте соответствующий спланированный заказ.</span><span class="sxs-lookup"><span data-stu-id="05ab4-113">Open the relevant planned order.</span></span>
1. <span data-ttu-id="05ab4-114">На экспресс-вкладке **Общие** в разделе **Запланировано** укажите даты в полях **Дата начала** и **Дата окончания**.</span><span class="sxs-lookup"><span data-stu-id="05ab4-114">On the **General** FastTab, in the **Scheduled** section, specify dates in the **Start date** and **End date** fields.</span></span>
