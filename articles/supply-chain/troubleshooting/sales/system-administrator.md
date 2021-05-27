---
title: Системные администраторы не могут отменить удержания заказов, поскольку они не авторизованы
description: Системные администраторы не могут отменить удержания заказов, поскольку они не авторизованы.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026864"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a><span data-ttu-id="fe69c-103">Системные администраторы не могут отменить удержания заказов, поскольку они не авторизованы</span><span class="sxs-lookup"><span data-stu-id="fe69c-103">System administrators can't clear order holds because they aren't authorized</span></span>

<span data-ttu-id="fe69c-104">Номер статьи базы знаний: 4614642</span><span class="sxs-lookup"><span data-stu-id="fe69c-104">KB number: 4614642</span></span>

## <a name="symptoms"></a><span data-ttu-id="fe69c-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="fe69c-105">Symptoms</span></span>

<span data-ttu-id="fe69c-106">Системные администраторы не могут очищать удержания заказов на продажу, если только у них нет особой роли, назначенной в коде удержания заказа.</span><span class="sxs-lookup"><span data-stu-id="fe69c-106">System administrators can't clear sales order holds unless they have the specific role that is assigned in the order hold code.</span></span>

## <a name="resolution"></a><span data-ttu-id="fe69c-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="fe69c-107">Resolution</span></span>

<span data-ttu-id="fe69c-108">Доступ к некоторым операциям, таким как удержания клирингового заказа на продажу, управляется настройкой бизнес-политики.</span><span class="sxs-lookup"><span data-stu-id="fe69c-108">Access to some operations, such as clearing sales order holds, is driven by the setup of a business policy.</span></span> <span data-ttu-id="fe69c-109">Обычно системным администраторам не разрешается выполнять операции такого типа.</span><span class="sxs-lookup"><span data-stu-id="fe69c-109">System administrators aren't typically allowed to perform operations of this type.</span></span> 

<span data-ttu-id="fe69c-110">Чаще доступ к выполнению определенной задачи осуществляется с помощью бизнес-политик, и только отдельные лица в организации утверждаются для выполнения этой задачи.</span><span class="sxs-lookup"><span data-stu-id="fe69c-110">More often, access to perform a specific task is governed by business policies, and only specific persons in an organization are approved to perform that task.</span></span> <span data-ttu-id="fe69c-111">Примерами могут служить утверждения, являющиеся результатом утверждения рабочего процесса, и отдельные задачи, которые являются результатом настройки рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="fe69c-111">Examples include approvals that are the result of workflow approvals and specific tasks that are the result of a workflow configuration.</span></span>

<span data-ttu-id="fe69c-112">Хотя ни один из рабочих процессов не связан с удержанием заказов, принцип аналогичен.</span><span class="sxs-lookup"><span data-stu-id="fe69c-112">Although no workflow is associated with order holds, the principle is similar.</span></span> <span data-ttu-id="fe69c-113">Соответствующая роль определяет конкретную группу лиц в организации, имеющих право очищать удержания заказов.</span><span class="sxs-lookup"><span data-stu-id="fe69c-113">A relevant role designates the specific group of people in an organization who have the right to clear order holds.</span></span> <span data-ttu-id="fe69c-114">Это право не обязательно предоставлять всем администраторам, поскольку этот подход нарушает определенную бизнес-политику.</span><span class="sxs-lookup"><span data-stu-id="fe69c-114">This right should not necessarily be granted to all administrators, because that approach violates the defined business policy.</span></span>
