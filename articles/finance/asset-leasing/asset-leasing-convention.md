---
title: Соглашения по аренде активов
description: В этом разделе описываются соглашения для аренды активов.
author: moaamer
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e6450438a6e8c594590df3cc4502895913f50d01
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842402"
---
# <a name="asset-leasing-conventions"></a><span data-ttu-id="334f8-103">Соглашения по аренде активов</span><span class="sxs-lookup"><span data-stu-id="334f8-103">Asset leasing conventions</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="334f8-104">В этом разделе описываются соглашения для аренды активов.</span><span class="sxs-lookup"><span data-stu-id="334f8-104">This topic describes conventions for leased assets.</span></span> <span data-ttu-id="334f8-105">Соглашения по аренде используются для определения даты начала книги аренды.</span><span class="sxs-lookup"><span data-stu-id="334f8-105">Leasing conventions are used to determine the commencement date of a lease book.</span></span> <span data-ttu-id="334f8-106">Если соглашение по аренде имеет значение **Нет**, дата начала совпадает с начальной датой аренды (то есть, со значением поля **Дата начала аренды**).</span><span class="sxs-lookup"><span data-stu-id="334f8-106">If the leasing convention is set to **None**, the commencement date is the same as the start date for the lease (that is, the value of the **Lease start date** field).</span></span> <span data-ttu-id="334f8-107">Если соглашение по аренде настроено на **Полный месяц**, дата начала — это первый день месяца, на который приходится начальная дата аренды.</span><span class="sxs-lookup"><span data-stu-id="334f8-107">If the leasing convention is set to **Full month**, the commencement date is the first day of the month that the lease's start date falls in.</span></span>

<span data-ttu-id="334f8-108">Дата начала определяет начальную дату периода для амортизации обязательств и графиков амортизации актива.</span><span class="sxs-lookup"><span data-stu-id="334f8-108">The commencement date determines the start date of the period for the liability amortization and asset depreciation schedules.</span></span> <span data-ttu-id="334f8-109">Расходы на уплату процентов и расходы на амортизацию разносятся на дату окончания периода соответствующих расписаний.</span><span class="sxs-lookup"><span data-stu-id="334f8-109">Interest expenses and depreciation expenses are posted on the period end date of the corresponding schedules.</span></span> <span data-ttu-id="334f8-110">Начальное признание и запись журнала корректировки разносятся на дату начала.</span><span class="sxs-lookup"><span data-stu-id="334f8-110">The initial recognition and adjustment journal entry are posted on the commencement date.</span></span>

> [!NOTE]
> <span data-ttu-id="334f8-111">Функцию для соглашений по аренде необходимо включить через механизм управления функциями.</span><span class="sxs-lookup"><span data-stu-id="334f8-111">The feature for leasing conventions must be turned on through Feature Management.</span></span> <span data-ttu-id="334f8-112">В рабочей области **Управление функциями** найдите и выберите функцию, которая называется **Соглашение по аренде для аренды актива**, затем выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="334f8-112">In the **Feature management** workspace, find and select the feature that is named **Leasing convention for asset leasing** feature, and then select **Enable now**.</span></span>

<span data-ttu-id="334f8-113">Соглашения по аренде назначаются настройке для книги аренды активов.</span><span class="sxs-lookup"><span data-stu-id="334f8-113">Leasing conventions are assigned to the setup for a lease asset book.</span></span>

<span data-ttu-id="334f8-114">Чтобы просмотреть или назначить соглашение по аренде, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="334f8-114">To view or assign the leasing convention, follow these steps.</span></span>

1. <span data-ttu-id="334f8-115">Перейдите в раздел **Аренда активов \> Настройка \> Книги аренды**.</span><span class="sxs-lookup"><span data-stu-id="334f8-115">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="334f8-116">В поле **Соглашение по аренде** выберите одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="334f8-116">In the **Leasing convention** field, select one of the following values.</span></span>

    | <span data-ttu-id="334f8-117">Соглашение об аренде</span><span class="sxs-lookup"><span data-stu-id="334f8-117">Leasing convention</span></span> | <span data-ttu-id="334f8-118">описание</span><span class="sxs-lookup"><span data-stu-id="334f8-118">Description</span></span> |
    |--------------------|-------------|
    | <span data-ttu-id="334f8-119">Не допускается</span><span class="sxs-lookup"><span data-stu-id="334f8-119">None</span></span>               | <span data-ttu-id="334f8-120">Амортизация обязательств и графики амортизации актива начинаются с даты начала аренды, так как дата начала совпадает с начальной датой аренды.</span><span class="sxs-lookup"><span data-stu-id="334f8-120">The liability amortization and asset depreciation schedules start on the lease's start date, because the commencement date equals the lease's start date.</span></span> <span data-ttu-id="334f8-121">Дата окончания на один месяц позже.</span><span class="sxs-lookup"><span data-stu-id="334f8-121">The end date is one month later.</span></span> <span data-ttu-id="334f8-122">Это соглашение по аренде не гарантирует, что процент будет разнесен в последний день каждого месяца.</span><span class="sxs-lookup"><span data-stu-id="334f8-122">This leasing convention doesn't guarantee that the interest will be posted on the last day of each month.</span></span> |
    | <span data-ttu-id="334f8-123">Полный месяц</span><span class="sxs-lookup"><span data-stu-id="334f8-123">Full month</span></span>         | <span data-ttu-id="334f8-124">Для аренд с датой начала, которая указана в любое время в течение месяца, амортизация обязательств и график амортизации актива начинают начислять расходы на первый день этого месяца.</span><span class="sxs-lookup"><span data-stu-id="334f8-124">For leases that have a start date that occurs at any time during the month, the liability amortization and asset depreciation schedules start to accrue expenses on the first day of that month.</span></span> <span data-ttu-id="334f8-125">Это соглашение по аренде гарантирует, что процент начисляется в последний день каждого месяца для всего месяца.</span><span class="sxs-lookup"><span data-stu-id="334f8-125">This leasing convention ensures that interest is accrued on the last day of each month for the whole month.</span></span> |

3. <span data-ttu-id="334f8-126">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="334f8-126">Select **Save**.</span></span>

<span data-ttu-id="334f8-127">При создании аренды дата начала каждой книги автоматически вводится на основе начальной даты, введенной для аренды, и соглашения по аренде, которое указано для книги.</span><span class="sxs-lookup"><span data-stu-id="334f8-127">When a lease is created, the commencement date of each book is automatically entered based on the start date that is entered for the lease and the leasing convention that is specified for the book.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]