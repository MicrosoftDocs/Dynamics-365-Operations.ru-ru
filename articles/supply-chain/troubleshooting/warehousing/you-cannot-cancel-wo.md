---
title: Отмена работы, выполняемой пользователем, невозможна
description: Отмена работы, выполняемой пользователем, невозможна
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924409"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a><span data-ttu-id="6b081-103">Отмена работы, выполняемой пользователем, невозможна</span><span class="sxs-lookup"><span data-stu-id="6b081-103">You can't cancel work that is on a user</span></span>

<span data-ttu-id="6b081-104">Код ошибки: WAX708</span><span class="sxs-lookup"><span data-stu-id="6b081-104">Error code: WAX708</span></span>

## <a name="symptoms"></a><span data-ttu-id="6b081-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="6b081-105">Symptoms</span></span>

<span data-ttu-id="6b081-106">Система отобразит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="6b081-106">The system shows the following error message:</span></span>

> <span data-ttu-id="6b081-107">Нельзя отменить работу, которая отведена пользователю.</span><span class="sxs-lookup"><span data-stu-id="6b081-107">You cannot cancel work that is on a user.</span></span>

## <a name="cause"></a><span data-ttu-id="6b081-108">Причина</span><span class="sxs-lookup"><span data-stu-id="6b081-108">Cause</span></span>

<span data-ttu-id="6b081-109">Работа заблокирована пользователем и не может быть отменена.</span><span class="sxs-lookup"><span data-stu-id="6b081-109">The work is locked by a user and can't be canceled.</span></span> <span data-ttu-id="6b081-110">Чтобы подтвердить это, откройте код работы, а затем откройте вкладку **Общее**. Если работа заблокирована, в поле **Статус работы** будет указано значение *Выполняется*, а в поле **Кем заблокировано** — код пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b081-110">To confirm this, open the work ID and then open the **General** tab. If the work is locked, the **Work status** field will be set to *In progress*, and the **Locked by** field will be set to a user ID.</span></span>

## <a name="resolution"></a><span data-ttu-id="6b081-111">Приказ</span><span class="sxs-lookup"><span data-stu-id="6b081-111">Resolution</span></span>

<span data-ttu-id="6b081-112">Чтобы отменить работу, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6b081-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="6b081-113">Перейдите **Управление складом \> Периодические задачи \> Очистка \> Отмена работы**.</span><span class="sxs-lookup"><span data-stu-id="6b081-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="6b081-114">В поле **Код работы** укажите код работы, которую необходимо отменить.</span><span class="sxs-lookup"><span data-stu-id="6b081-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="6b081-115">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6b081-115">Select **OK**.</span></span>
1. <span data-ttu-id="6b081-116">Выберите **Да** для подтверждения того, что вы хотите отменить работу.</span><span class="sxs-lookup"><span data-stu-id="6b081-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="6b081-117">Дополнительные сведения см. в разделе [Отмена работы склада для обработки исключений](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="6b081-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
