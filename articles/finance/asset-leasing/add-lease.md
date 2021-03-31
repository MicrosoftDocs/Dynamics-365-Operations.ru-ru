---
title: Добавление или копирование аренд (предварительная версия)
description: В этой теме описывается порядок создания новой аренды путем ввода сведений для нее в модуль аренды активов или копирования информации из существующей аренды.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 325a1b7948f3cb8033fa93b7c36f1f1f6b7dbb27
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220019"
---
# <a name="add-or-copy-leases-preview"></a><span data-ttu-id="f82cf-103">Добавление или копирование аренд (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="f82cf-103">Add or copy leases (Preview)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f82cf-104">В этом разделе описывается создание аренды с нуля в модуле аренды активов, а также создание аренды путем копирования существующей аренды.</span><span class="sxs-lookup"><span data-stu-id="f82cf-104">This topic explains how to create a lease from scratch in Asset leasing, and also how to create a lease by copying an existing lease.</span></span> <span data-ttu-id="f82cf-105">Процесс создания аренды с нуля включает ввод сведений для новой аренды и последующее создание графика аренды.</span><span class="sxs-lookup"><span data-stu-id="f82cf-105">The process for creating a lease from scratch involves entering information for the new lease and then creating a lease schedule.</span></span> <span data-ttu-id="f82cf-106">После настройки по крайней мере одной аренды может быть проще скопировать информацию из существующей аренды, а затем изменить эту информацию, как требуется для создания новой аренды.</span><span class="sxs-lookup"><span data-stu-id="f82cf-106">After at least one lease has been set up, you might find it easier to copy the information from an existing lease and then edit that information as you require to create a new lease.</span></span>

## <a name="create-a-lease"></a><span data-ttu-id="f82cf-107">Создание аренды</span><span class="sxs-lookup"><span data-stu-id="f82cf-107">Create a lease</span></span>

<span data-ttu-id="f82cf-108">Выполните следующие действия для создания аренды в модуле аренды активов.</span><span class="sxs-lookup"><span data-stu-id="f82cf-108">Follow these steps to create a lease in Asset leasing.</span></span>

1. <span data-ttu-id="f82cf-109">На странице **Сводка по аренде** в области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f82cf-109">On the **Lease summary** page, on the Action Pane, select **New**.</span></span>
2. <span data-ttu-id="f82cf-110">Введите информацию об аренде.</span><span class="sxs-lookup"><span data-stu-id="f82cf-110">Enter the lease information.</span></span> <span data-ttu-id="f82cf-111">Обязательные поля имеют красные границы.</span><span class="sxs-lookup"><span data-stu-id="f82cf-111">Fields that are required have red borders.</span></span>

## <a name="create-a-lease-schedule"></a><span data-ttu-id="f82cf-112">Создание графика аренды</span><span class="sxs-lookup"><span data-stu-id="f82cf-112">Create a lease schedule</span></span>

<span data-ttu-id="f82cf-113">По завершении ввода информации для аренды необходимо выполнить следующие действия, чтобы создать график аренды.</span><span class="sxs-lookup"><span data-stu-id="f82cf-113">After you've finished entering information for the lease, follow these steps to create a lease schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="f82cf-114">Финансовые аналитики могут изменяться в зависимости от пользовательских финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="f82cf-114">The financial dimensions might change based on any custom financial dimensions.</span></span>

1. <span data-ttu-id="f82cf-115">Выберите **Создать расписания** для создания книг аренды.</span><span class="sxs-lookup"><span data-stu-id="f82cf-115">Select **Create schedules** to generate the lease books.</span></span> <span data-ttu-id="f82cf-116">Книги аренды включают платежи, амортизацию, амортизацию и графики расходов.</span><span class="sxs-lookup"><span data-stu-id="f82cf-116">The lease books include the payment, amortization, depreciation, and expense schedules.</span></span>
2. <span data-ttu-id="f82cf-117">Для получения доступа к книгам аренды и просмотра вновь созданных расписаний выберите вкладку **Книги**.</span><span class="sxs-lookup"><span data-stu-id="f82cf-117">To access the lease books and view the newly created schedules, select the **Books** tab.</span></span>

    <span data-ttu-id="f82cf-118">На странице **Сведения о книге** показано, как учитывается аренда в книгах, которые были назначены ей.</span><span class="sxs-lookup"><span data-stu-id="f82cf-118">The **Book details** page shows how the lease is accounted for by the books that have been allocated to it.</span></span> <span data-ttu-id="f82cf-119">Отсюда можно просмотреть графики аренды.</span><span class="sxs-lookup"><span data-stu-id="f82cf-119">From here, you can view the lease schedules.</span></span>

    <span data-ttu-id="f82cf-120">График оплаты содержит входные данные со вкладки **Строки графика оплаты** на странице **Добавить аренду**.</span><span class="sxs-lookup"><span data-stu-id="f82cf-120">The payment schedule contains the inputs from the **Payment schedule lines** tab on the **Add lease** page.</span></span> <span data-ttu-id="f82cf-121">Все равно можно изменить каждую сумму платежа и переменный платеж.</span><span class="sxs-lookup"><span data-stu-id="f82cf-121">You can still change each payment amount and variable payment.</span></span> <span data-ttu-id="f82cf-122">Арендное обязательство рассчитывается на основе измененного графика оплаты.</span><span class="sxs-lookup"><span data-stu-id="f82cf-122">The lease liability is calculated based on the modified payment schedule.</span></span>

4. <span data-ttu-id="f82cf-123">После завершения просмотра графика оплаты выберите **Подтвердить график**.</span><span class="sxs-lookup"><span data-stu-id="f82cf-123">After you've finished reviewing the payment schedule, select **Confirm schedule**.</span></span> <span data-ttu-id="f82cf-124">После подтверждения этого расписания аренда больше не будет доступна для редактирования.</span><span class="sxs-lookup"><span data-stu-id="f82cf-124">After the schedule is confirmed, the lease is no longer available for editing.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f82cf-125">Срок аренды автоматически рассчитывается системой из строк графика оплаты на странице **Добавить аренду**.</span><span class="sxs-lookup"><span data-stu-id="f82cf-125">The system automatically calculates the lease term from the payment schedule lines on the **Add lease** page.</span></span>
    >
    > <span data-ttu-id="f82cf-126">Чтобы рассчитать срок аренды в месяцах, система находит разницу между датой начала и датой окончания для конкретной строки графика оплаты.</span><span class="sxs-lookup"><span data-stu-id="f82cf-126">To calculate the lease term in months, the system finds the difference between the start date and the end date for a specific payment schedule line.</span></span> <span data-ttu-id="f82cf-127">Затем она перемещается к следующей строке графика оплаты и находит разницу снова.</span><span class="sxs-lookup"><span data-stu-id="f82cf-127">It then moves to the next payment schedule line and finds the difference again.</span></span> <span data-ttu-id="f82cf-128">И наконец, система суммирует все суммы для определения срока аренды в месяцах.</span><span class="sxs-lookup"><span data-stu-id="f82cf-128">Finally, the system sums all the amounts to determine the lease term in months.</span></span>

5. <span data-ttu-id="f82cf-129">Для просмотра расчетных процентных расходов для периода откройте страницу **График амортизации обязательств**.</span><span class="sxs-lookup"><span data-stu-id="f82cf-129">To view the calculated period interest expenses, open the **Liability amortization schedule** page.</span></span> <span data-ttu-id="f82cf-130">Чтобы просмотреть рассчитанную прямолинейным метод амортизацию, откройте страницу **График амортизации актива**.</span><span class="sxs-lookup"><span data-stu-id="f82cf-130">To view calculated straight-line depreciation, open the **Asset depreciation schedule** page.</span></span>
6. <span data-ttu-id="f82cf-131">После завершения просмотра рассчитанной суммы можно создать запись журнала первоначального признания на странице **Первоначальное признание**.</span><span class="sxs-lookup"><span data-stu-id="f82cf-131">After you've finished reviewing the calculated amount, you can create the initial recognition journal entry on the **Initial recognition** page.</span></span> <span data-ttu-id="f82cf-132">Вы получаете сообщение о том, что журнал был создан.</span><span class="sxs-lookup"><span data-stu-id="f82cf-132">You receive a message that states that the journal has been created.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f82cf-133">Запись журнала не разносится в главную книгу до тех пор, пока запись не будет разнесена вручную.</span><span class="sxs-lookup"><span data-stu-id="f82cf-133">The journal entry isn't posted to General ledger until you manually post the entry.</span></span>

7. <span data-ttu-id="f82cf-134">Чтобы просмотреть предлагаемую запись первоначального признания перед разноской, выберите **Журнал аренды активов**.</span><span class="sxs-lookup"><span data-stu-id="f82cf-134">To review the proposed initial recognition entry before you post it, select **Asset leasing journal**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f82cf-135">Журнал аренды активов невозможно создать вручную.</span><span class="sxs-lookup"><span data-stu-id="f82cf-135">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="f82cf-136">Он автоматически создается при создании расписаний аренды.</span><span class="sxs-lookup"><span data-stu-id="f82cf-136">It's automatically created when lease schedules are created.</span></span>

8. <span data-ttu-id="f82cf-137">После того как вы завершили просмотр записи журнала первоначального признания и готовы к его разноске, выберите **Разнести**, чтобы признать право на использование (ФПП) актива и арендное обязательство в главной книге.</span><span class="sxs-lookup"><span data-stu-id="f82cf-137">When you've finished reviewing the initial recognition journal entry and are ready to post it, select **Post** to recognize the right-of-use (ROU) asset and lease liability in General ledger.</span></span>

## <a name="copy-a-lease"></a><span data-ttu-id="f82cf-138">Копирование аренды</span><span class="sxs-lookup"><span data-stu-id="f82cf-138">Copy a lease</span></span>

<span data-ttu-id="f82cf-139">Аренда актива позволяет копировать сведения аренды для создания новой аренды с такой же информацией.</span><span class="sxs-lookup"><span data-stu-id="f82cf-139">Asset leasing lets you copy the details of a lease to create a new lease that has the same information.</span></span> <span data-ttu-id="f82cf-140">После этого можно изменить поля аренды перед созданием графиков для скопированной аренды.</span><span class="sxs-lookup"><span data-stu-id="f82cf-140">You can then change the lease fields before you create the schedules for the copied lease.</span></span>

1. <span data-ttu-id="f82cf-141">На странице **Сводка по аренде** выберите аренду для копирования, а затем на панели операций выберите **Копировать аренду**.</span><span class="sxs-lookup"><span data-stu-id="f82cf-141">On the **Lease summary** page, select the lease to copy, and then, on the Action Pane, select **Copy lease**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f82cf-142">Если параметр **Вручную** отключен для номерной серии для кодов аренды, следующий номер в последовательности автоматически создается в качестве кода аренды копируемой аренды.</span><span class="sxs-lookup"><span data-stu-id="f82cf-142">If the **Manual** parameter is turned off for the number sequence for lease IDs, the next number in the sequence is automatically generated as the lease ID of the copied lease.</span></span> <span data-ttu-id="f82cf-143">Если включен параметр **Вручную**, появится сообщение с предложением ввести код аренды перед началом копирования аренды.</span><span class="sxs-lookup"><span data-stu-id="f82cf-143">If the **Manual** parameter is turned on, you receive a message that prompts you to enter the lease ID before you proceed to copy the lease.</span></span>

2. <span data-ttu-id="f82cf-144">Выберите **Копировать**.</span><span class="sxs-lookup"><span data-stu-id="f82cf-144">Select **Copy**.</span></span> <span data-ttu-id="f82cf-145">Сведения об аренде из выбранной аренды копируются в новую аренду.</span><span class="sxs-lookup"><span data-stu-id="f82cf-145">The lease details from the selected lease are copied to a new lease.</span></span> <span data-ttu-id="f82cf-146">После этого можно изменить сведения о новой аренде перед ее сохранением и создать графики аренды.</span><span class="sxs-lookup"><span data-stu-id="f82cf-146">You can then edit the details of the new lease before you save it and create the lease schedules.</span></span>

## <a name="asset-leasing-journal"></a><span data-ttu-id="f82cf-147">Журнал аренды активов</span><span class="sxs-lookup"><span data-stu-id="f82cf-147">Asset leasing journal</span></span>

<span data-ttu-id="f82cf-148">Все записи журнала, созданные в модуле аренды активов, содержатся в журнале аренды активов.</span><span class="sxs-lookup"><span data-stu-id="f82cf-148">All journal entries that are created in Asset leasing are contained in the Asset leasing journal.</span></span> <span data-ttu-id="f82cf-149">На странице **Журнал аренды активов** (**Аренда активов \> Записи журналов \> Журнал аренды активов**) можно выполнять фильтрацию по статусу разноски, просматривать отдельные записи в журнале и операции и разносить неразнесенные записи журнала.</span><span class="sxs-lookup"><span data-stu-id="f82cf-149">On the **Asset leasing journal** page (**Asset leasing \> Journal entries \> Asset leasing journal**), you can filter by posting status, view specific journal entries and the vouchers, and post unposted journal entries.</span></span>

> [!NOTE]
> <span data-ttu-id="f82cf-150">Журнал аренды активов невозможно создать вручную.</span><span class="sxs-lookup"><span data-stu-id="f82cf-150">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="f82cf-151">Он автоматически создается при создании расписаний аренды.</span><span class="sxs-lookup"><span data-stu-id="f82cf-151">It's automatically created when lease schedules are created.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]