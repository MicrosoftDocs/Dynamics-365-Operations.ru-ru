---
title: Ведение основных средств (Россия)
description: В этом разделе объясняется, как отключить, повторно активировать и обновить основное средство в Microsoft Dynamics 365 for Finance and Operations в России.
author: ShylaThompson
manager: AnnBe
ms.date: 01/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 73a972ce667cbf7f5630007df99680b3aad08dfa
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556255"
---
# <a name="major-repair-and-temporarily-inactivation-fixad-assets-russia"></a><span data-ttu-id="64e18-103">Капитальный ремонт и временная деактивация основных средств (Россия)</span><span class="sxs-lookup"><span data-stu-id="64e18-103">Major repair and Temporarily inactivation fixad assets (Russia)</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="64e18-104">Если основное средство закрыто или неактивно в течение более чем трех месяцев, или если в течение более чем 12 месяцев производится его реконструкция, расчет амортизации приостанавливается.</span><span class="sxs-lookup"><span data-stu-id="64e18-104">If a fixed asset is closed down or inactive for more than three months, or if refurbishment of the asset is conducted for more than 12 months, calculation of depreciation is suspended.</span></span> <span data-ttu-id="64e18-105">Он возобновится после возврата основного средства в эксплуатацию.</span><span class="sxs-lookup"><span data-stu-id="64e18-105">It resumes when the fixed asset is put back into operation.</span></span>
<span data-ttu-id="64e18-106">Например, основное средство может быть отключено в случае капитальной модернизации.</span><span class="sxs-lookup"><span data-stu-id="64e18-106">For example, a fixed asset may be inactivated in the case of capital improvements.</span></span>
<span data-ttu-id="64e18-107">"Модификация оборудования" — это специальная категория активов, включающая капитальный ремонт, усовершенствование, технические обновления, достройки и приобретение дополнительного оборудования для ОС.</span><span class="sxs-lookup"><span data-stu-id="64e18-107">"Capital improvements" is a special asset category that includes capital renovations, improvements, technical updates, additional construction, and the acquisition of additional equipment for a fixed asset.</span></span> <span data-ttu-id="64e18-108">При выполнении модификации оборудования рассчитанная амортизация не пересчитывается.</span><span class="sxs-lookup"><span data-stu-id="64e18-108">When you update capital improvements, calculated depreciation isn't revalued.</span></span> <span data-ttu-id="64e18-109">Однако амортизированная стоимость и срок службы ОС меняются.</span><span class="sxs-lookup"><span data-stu-id="64e18-109">However, the depreciated cost and service life of the fixed asset are changed.</span></span>


## <a name="temporarily-inactivate-a-fixed-asset"></a><span data-ttu-id="64e18-110">Временная деактивация основного средства</span><span class="sxs-lookup"><span data-stu-id="64e18-110">Temporarily inactivate a fixed asset</span></span>

1. <span data-ttu-id="64e18-111">Выберите **Основные средства (Россия)** \> **Общие** \> **Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="64e18-111">Select **Fixed assets (Russia)** \> **Common** \> **Fixed assets**.</span></span>
2. <span data-ttu-id="64e18-112">Выберите временно деактивируемое основное средство.</span><span class="sxs-lookup"><span data-stu-id="64e18-112">Select the fixed asset to temporarily inactivate.</span></span> <span data-ttu-id="64e18-113">Статус основного средства в настоящее время **В эксплуатации**.</span><span class="sxs-lookup"><span data-stu-id="64e18-113">The status of the asset is currently **In operation**.</span></span>
3. <span data-ttu-id="64e18-114">В области действий на вкладке **ОС** в группе **История** выберите **Консервация** для открытия страницы **Консервация**.</span><span class="sxs-lookup"><span data-stu-id="64e18-114">On the Action Pane, on the **Fixed asset** tab, in the **History** group, select **Temporary closing-down** to open the **Temporary closing-down** page.</span></span>
4. <span data-ttu-id="64e18-115">В поле **Начальная дата** выберите дату деактивации, затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="64e18-115">In the **Start date** field, select the inactivation date, and then close the page.</span></span> <span data-ttu-id="64e18-116">Состояние основного средства обновляется на **Консервация**.</span><span class="sxs-lookup"><span data-stu-id="64e18-116">The status of the asset is updated to **Temporary closing-down**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="64e18-117">Когда основное средство имеет статус **Консервация**, амортизация не начисляется.</span><span class="sxs-lookup"><span data-stu-id="64e18-117">Depreciation isn't accrued while the status of a fixed asset is **Temporary closing-down**.</span></span>

## <a name="reactivate-a-fixed-asset"></a><span data-ttu-id="64e18-118">Повторная активация основного средства</span><span class="sxs-lookup"><span data-stu-id="64e18-118">Reactivate a fixed asset</span></span>

1. <span data-ttu-id="64e18-119">Выберите **Основные средства (Россия)** \> **Общие** \> **Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="64e18-119">Select **Fixed assets (Russia)** \> **Common** \> **Fixed assets**.</span></span>
2. <span data-ttu-id="64e18-120">Выберите основное средство со статусом **Консервация**.</span><span class="sxs-lookup"><span data-stu-id="64e18-120">Select the fixed asset that has a status of **Temporary closing-down**.</span></span>
3. <span data-ttu-id="64e18-121">В области действий на вкладке **ОС** в группе **История** выберите **Консервация** для открытия страницы **Консервация**.</span><span class="sxs-lookup"><span data-stu-id="64e18-121">On the Action Pane, on the **Fixed asset** tab, in the **History** group, select **Temporary closing-down** to open the **Temporary closing-down** page.</span></span>
4. <span data-ttu-id="64e18-122">В поле **Конечная дата** выберите дату повторной активации, затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="64e18-122">In the **Finish date** field, select the reactivation date, and then close the page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="64e18-123">Амортизация будет рассчитываться, начиная с даты, указанной в поле **Дата начала начисления амортизации** на странице **Группы амортизации**.</span><span class="sxs-lookup"><span data-stu-id="64e18-123">Depreciation is calculated from the date that is specified in the **Depreciation start date** field on the **Depreciation groups** page.</span></span>

## <a name="post-an-update-for-a-major-repair-of-a-fixed-asset"></a><span data-ttu-id="64e18-124">Разноска обновления для капитального ремонта основного средства</span><span class="sxs-lookup"><span data-stu-id="64e18-124">Post an update for a major repair of a fixed asset</span></span>

<span data-ttu-id="64e18-125">Необходимо выполнить следующие задачи, прежде чем можно будет разнести обновление капитального ремонта основного средства:</span><span class="sxs-lookup"><span data-stu-id="64e18-125">You must complete the following tasks before you can post an update for a major repair of a fixed asset:</span></span>

1. <span data-ttu-id="64e18-126">Создайте аналитику амортизации.</span><span class="sxs-lookup"><span data-stu-id="64e18-126">Create dimensions for depreciation.</span></span> <span data-ttu-id="64e18-127">Дополнительные сведения см. в разделе [Определение финансовых аналитик](../general-ledger/tasks/define-financial-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="64e18-127">For more information, see [Define financial dimensions](../general-ledger/tasks/define-financial-dimensions.md).</span></span>
2. <span data-ttu-id="64e18-128">Настройте коды причин.</span><span class="sxs-lookup"><span data-stu-id="64e18-128">Set up expense codes.</span></span> 
3. <span data-ttu-id="64e18-129">Настройте амортизационную премию.</span><span class="sxs-lookup"><span data-stu-id="64e18-129">Set up bonus depreciation.</span></span>
4. <span data-ttu-id="64e18-130">Настройте группы амортизации.</span><span class="sxs-lookup"><span data-stu-id="64e18-130">Set up depreciation groups.</span></span>

### <a name="create-a-journal-for-a-major-repair-of-a-fixed-asset"></a><span data-ttu-id="64e18-131">Создание журнала для капитального ремонта основного средства</span><span class="sxs-lookup"><span data-stu-id="64e18-131">Create a journal for a major repair of a fixed asset</span></span>

1. <span data-ttu-id="64e18-132">Выберите **Основные средства (Россия)** \> **Журналы** \> **Журнал ОС**.</span><span class="sxs-lookup"><span data-stu-id="64e18-132">Select **Fixed assets (Russia)** \> **Journals** \> **FA journal**.</span></span>
2. <span data-ttu-id="64e18-133">Создайте журнал основных средств (ОС).</span><span class="sxs-lookup"><span data-stu-id="64e18-133">Create a fixed asset (FA) journal.</span></span>
3. <span data-ttu-id="64e18-134">В поле **Имя** выберите имя журнала.</span><span class="sxs-lookup"><span data-stu-id="64e18-134">In the **Name** field, select a journal name.</span></span>
4. <span data-ttu-id="64e18-135">В поле **Описание** просмотрите или измените описание журнала.</span><span class="sxs-lookup"><span data-stu-id="64e18-135">In the **Description** field, view or modify the description of the journal.</span></span>
5. <span data-ttu-id="64e18-136">Выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="64e18-136">Select **Lines**.</span></span>
6. <span data-ttu-id="64e18-137">Создайте строку журнала.</span><span class="sxs-lookup"><span data-stu-id="64e18-137">Create a journal line.</span></span>
7. <span data-ttu-id="64e18-138">В поле **Дата транзакции** выберите дату для обновления транзакции.</span><span class="sxs-lookup"><span data-stu-id="64e18-138">In the **Transaction date** field, select the date to update the transaction on.</span></span>
8. <span data-ttu-id="64e18-139">В поле **Тип проводки** выберите **Капитальный ремонт**.</span><span class="sxs-lookup"><span data-stu-id="64e18-139">In the **Transaction type** field, select **Major repairs**.</span></span>
9. <span data-ttu-id="64e18-140">В поле **Инвентарный номер ОС** выберите номер основного средства.</span><span class="sxs-lookup"><span data-stu-id="64e18-140">In the **FA inventory number** field, select the fixed asset number.</span></span>
10. <span data-ttu-id="64e18-141">В поле **Модель стоимости** выберите модель стоимости основного средства.</span><span class="sxs-lookup"><span data-stu-id="64e18-141">In the **Value model** field, select the value model of the fixed asset.</span></span>
11. <span data-ttu-id="64e18-142">В поле **Код основания** выберите код основания.</span><span class="sxs-lookup"><span data-stu-id="64e18-142">In the **Reason code** field, select a reason code.</span></span>
12. <span data-ttu-id="64e18-143">В поле **Комментарий к причине** обновите причину капитального ремонта основного средства.</span><span class="sxs-lookup"><span data-stu-id="64e18-143">In the **Reason comment** field, update the reason for the major repair of the fixed asset.</span></span>
13. <span data-ttu-id="64e18-144">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="64e18-144">Select **OK**.</span></span> <span data-ttu-id="64e18-145">В журнале отображаются строки усовершенствования актива.</span><span class="sxs-lookup"><span data-stu-id="64e18-145">The improvement lines for the asset are shown in the journal.</span></span>
14. <span data-ttu-id="64e18-146">В поле **Описание** выберите текст проводки.</span><span class="sxs-lookup"><span data-stu-id="64e18-146">In the **Description** field, select transaction text.</span></span>
15. <span data-ttu-id="64e18-147">В поле **Дебет** или **Кредит** введите сумму транзакции.</span><span class="sxs-lookup"><span data-stu-id="64e18-147">In the **Debit** or **Credit** field, enter the transaction amount.</span></span>
16. <span data-ttu-id="64e18-148">В поле **Тип корр. счета** выберите тип корр. счета.</span><span class="sxs-lookup"><span data-stu-id="64e18-148">In the **Offset account type** field, select the type of offset account.</span></span>
17. <span data-ttu-id="64e18-149">В поле **Корр. счет** выберите номер корр. счета.</span><span class="sxs-lookup"><span data-stu-id="64e18-149">In the **Offset account** field, select the offset account number.</span></span>

    > [!TIP]
    > <span data-ttu-id="64e18-150">Можно также выбрать **Групповые операции** \> **Капитальный ремонт** в области действий, чтобы создать проводки для нескольких основных средств.</span><span class="sxs-lookup"><span data-stu-id="64e18-150">You can also select **Group operations** \> **Major repairs** on the Action Pane to create transactions for several fixed assets.</span></span>

18. <span data-ttu-id="64e18-151">В области действий выберите **Разнести** \> **Разнести**, чтобы разнести журнал.</span><span class="sxs-lookup"><span data-stu-id="64e18-151">On the Action Pane, select **Post** \> **Post** to post the journal.</span></span>

### <a name="update-a-value-model-for-a-fixed-asset"></a><span data-ttu-id="64e18-152">Обновление модели стоимости для ОС</span><span class="sxs-lookup"><span data-stu-id="64e18-152">Update a value model for a fixed asset</span></span>

1. <span data-ttu-id="64e18-153">Выберите **Основные средства (Россия)** \> **Общие** \> **Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="64e18-153">Select **Fixed assets (Russia)** \> **Common** \> **Fixed assets**.</span></span>
2. <span data-ttu-id="64e18-154">Выберите основное средство, затем на панели действий выберите **Модели стоимости**.</span><span class="sxs-lookup"><span data-stu-id="64e18-154">Select a fixed asset, and then, on the Action Pane, select **Value models**.</span></span>
3. <span data-ttu-id="64e18-155">В области действий выберите **История срока службы ОС**.</span><span class="sxs-lookup"><span data-stu-id="64e18-155">On the Action Pane, select **FA lifetime history**.</span></span>
4. <span data-ttu-id="64e18-156">Выберите **Создать**, а затем в поле **Дата** выберите дату изменения срока службы.</span><span class="sxs-lookup"><span data-stu-id="64e18-156">Select **New**, and then in the **Date** field, select the date of the lifetime change.</span></span>
5. <span data-ttu-id="64e18-157">В полях **Новый срок службы** и **Новый коэффициент** введите срок службы и коэффициент для ОС.</span><span class="sxs-lookup"><span data-stu-id="64e18-157">In the **New lifetime** and **New factor** fields, enter a lifetime and factor for the fixed asset.</span></span>
6. <span data-ttu-id="64e18-158">В полях **Метод амортизации** и **Подгруппа амортизации** выберите метод амортизации и подгруппу амортизации.</span><span class="sxs-lookup"><span data-stu-id="64e18-158">In the **Depreciation method** and **Depreciation subgroup** fields, select a depreciation method and subgroup.</span></span>
7. <span data-ttu-id="64e18-159">В поле **Код основания** выберите код основания.</span><span class="sxs-lookup"><span data-stu-id="64e18-159">In the **Reason code** field, select a reason code.</span></span>
8. <span data-ttu-id="64e18-160">В поле **Комментарий к причине** обновите причину проводки.</span><span class="sxs-lookup"><span data-stu-id="64e18-160">In the **Reason comment** field, update the reason for the transaction.</span></span>

> [!NOTE]
> <span data-ttu-id="64e18-161">Когда производится капитальный ремонт ОС, амортизационная премия может применяться к ОС после день проводки капитального ремонта или после него.</span><span class="sxs-lookup"><span data-stu-id="64e18-161">When major repair work is done on a fixed asset, bonus depreciation can be applied to the asset on or after the transaction date of the major repair.</span></span> <span data-ttu-id="64e18-162">Можно создать проводку капитального ремонта для ОС и можно указать амортизационную премию и начальную дату расчета премии.</span><span class="sxs-lookup"><span data-stu-id="64e18-162">You can create a transaction for a major repair of a fixed asset, and you can specify the bonus depreciation and bonus start date.</span></span> <span data-ttu-id="64e18-163">Начальная дата амортизационной премии может совпадать с датой проводки капитального ремонта или следующей датой амортизации.</span><span class="sxs-lookup"><span data-stu-id="64e18-163">The start date of the bonus depreciation can be the same as the transaction date of the major repair, or it can be the next depreciation date.</span></span>
