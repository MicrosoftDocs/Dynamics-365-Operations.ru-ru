---
title: Создание проводки по аренде и окончании аренды основных средств (Россия)
description: В этом разделе описан порядок аренды основных средств и последующего возврат переданного в аренду средства в Microsoft Dynamics 365 for Finance and Operations в России.
author: ShylaThompson
manager: AnnBe
ms.date: 01/18/2019
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
ms.openlocfilehash: 23aecfc534a45459c36d5f3757bfb2a1d71b046b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "371749"
---
# <a name="create-a-fixed-asset-lease-and-a-return-from-lease-transaction-russia"></a><span data-ttu-id="1a77c-103">Создание проводки по аренде и окончании аренды основных средств (Россия)</span><span class="sxs-lookup"><span data-stu-id="1a77c-103">Create a fixed asset lease and a return from lease transaction (Russia)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a77c-104">Можно зарегистрировать аренду основного средства и последующий возврат переданного в аренду основного средства.</span><span class="sxs-lookup"><span data-stu-id="1a77c-104">You can register the lease of a fixed asset and the subsequent return of the leased asset.</span></span> <span data-ttu-id="1a77c-105">Таким образом можно записывать проводки для целей ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="1a77c-105">In this way, you can record the transactions for historical purposes.</span></span>

## <a name="lease-a-fixed-asset"></a><span data-ttu-id="1a77c-106">Передача основного средства в аренду</span><span class="sxs-lookup"><span data-stu-id="1a77c-106">Lease a fixed asset</span></span>

1. <span data-ttu-id="1a77c-107">Перейдите в раздел **Основные средства (Россия)** \> **Общие** \> **Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="1a77c-107">Go to **Fixed assets (Russia)** \> **Common** \> **Fixed assets**.</span></span>
2. <span data-ttu-id="1a77c-108">Выберите основное средство для сдачи в аренду, а затем, на панели действий на вкладке **ОС** в группе **История** выберите **Аренда** для открытия страницы **Сданные в аренду ОС**.</span><span class="sxs-lookup"><span data-stu-id="1a77c-108">Select the fixed asset to lease, and then, on the Action Pane, on the **Fixed asset** tab, in the **History** group, select **Lease** to open the **FA leased** page.</span></span>
3. <span data-ttu-id="1a77c-109">Создайте новую строку.</span><span class="sxs-lookup"><span data-stu-id="1a77c-109">Create a new line.</span></span>
4. <span data-ttu-id="1a77c-110">В поле **Дата передачи в аренду** выберите дату, когда основное средство было передано в аренду.</span><span class="sxs-lookup"><span data-stu-id="1a77c-110">In the **Date of lease** field, select the date when the fixed asset was leased out.</span></span>
5. <span data-ttu-id="1a77c-111">В поле **Ожидаемая дата возврата** выберите плановую дату возврата.</span><span class="sxs-lookup"><span data-stu-id="1a77c-111">In the **Expected return date** field, select the planned return date.</span></span>
6. <span data-ttu-id="1a77c-112">В поле **Арендатор** введите имя получателя арендуемого актива.</span><span class="sxs-lookup"><span data-stu-id="1a77c-112">In the **Leaseholder** field, enter the name of the lessee.</span></span>
7. <span data-ttu-id="1a77c-113">В поле **Расположение** выберите расположение передаваемого в аренду основного средства.</span><span class="sxs-lookup"><span data-stu-id="1a77c-113">In the **Location** field, select the location of the leased fixed asset.</span></span>
8. <span data-ttu-id="1a77c-114">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1a77c-114">Close the page.</span></span>
9. <span data-ttu-id="1a77c-115">Откройте **Основные средства (Россия)** \> **Журналы** \> **Журнал ОС**.</span><span class="sxs-lookup"><span data-stu-id="1a77c-115">Go to **Fixed assets (Russia)** \> **Journals** \> **FA journal**.</span></span>
10. <span data-ttu-id="1a77c-116">Создайте новый журнал.</span><span class="sxs-lookup"><span data-stu-id="1a77c-116">Create a new journal.</span></span>
11. <span data-ttu-id="1a77c-117">В поле **Имя** выберите имя журнала.</span><span class="sxs-lookup"><span data-stu-id="1a77c-117">In the **Name** field, select a journal name.</span></span>
12. <span data-ttu-id="1a77c-118">В поле **Описание** просмотрите или измените описание журнала.</span><span class="sxs-lookup"><span data-stu-id="1a77c-118">In the **Description** field, view or modify the description of the journal.</span></span>
13. <span data-ttu-id="1a77c-119">Выберите **Строки**, чтобы открыть страницу **Ваучер журнала**, чтобы можно было создавать проводки по основным средствам.</span><span class="sxs-lookup"><span data-stu-id="1a77c-119">Select **Lines** to open the **Journal voucher** page, so that you can create fixed asset transactions.</span></span>
14. <span data-ttu-id="1a77c-120">Выберите **Создать**, чтобы открыть диалоговое окно **Добавление в журнал**.</span><span class="sxs-lookup"><span data-stu-id="1a77c-120">Select **New** to open the **Add to journal** dialog box.</span></span>
15. <span data-ttu-id="1a77c-121">В поле **Дата транзакции** введите дату для транзакции.</span><span class="sxs-lookup"><span data-stu-id="1a77c-121">In the **Transaction date** field, select the date of the transaction.</span></span> <span data-ttu-id="1a77c-122">Выбранная дата должна совпадать или быть позднее даты, выбранной в поле **Дата передачи в аренду** на странице **Сданные в аренду ОС**.</span><span class="sxs-lookup"><span data-stu-id="1a77c-122">The date that you select must be the same as or later than the date that you selected in the **Date of lease** field on the **FA leased** page.</span></span>
16. <span data-ttu-id="1a77c-123">В поле **Тип транзакции** выберите **Аренда**.</span><span class="sxs-lookup"><span data-stu-id="1a77c-123">In the **Transaction type** field, select **Lease**.</span></span>
17. <span data-ttu-id="1a77c-124">В поле **Инвентарный номер ОС** выберите инвентарный номер сданного в аренду основного средства.</span><span class="sxs-lookup"><span data-stu-id="1a77c-124">In the **FA inventory number** field, select the number of the leased fixed asset.</span></span>
18. <span data-ttu-id="1a77c-125">В поле **Модель учета** выберите модель учета для основного средства.</span><span class="sxs-lookup"><span data-stu-id="1a77c-125">In the **Value model** field, select a value model for the fixed asset.</span></span>
19. <span data-ttu-id="1a77c-126">В поле **Код основания** выберите код основания.</span><span class="sxs-lookup"><span data-stu-id="1a77c-126">In the **Reason code** field, select a reason code.</span></span>
20. <span data-ttu-id="1a77c-127">В поле **Комментарий к причине** просмотрите или измените причину сдачи основного средства в аренду.</span><span class="sxs-lookup"><span data-stu-id="1a77c-127">In the **Reason comment** field, view or modify the reason for leasing the fixed asset.</span></span>
21. <span data-ttu-id="1a77c-128">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1a77c-128">Select **OK**.</span></span> <span data-ttu-id="1a77c-129">В журнале появляются строки переданного в аренду основного средства.</span><span class="sxs-lookup"><span data-stu-id="1a77c-129">The lines for the leased fixed asset appear in the journal.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1a77c-130">Чтобы создать проводки для нескольких основных средств, можно также выбрать **Групповые операции** \> **Аренда** в области действий на странице **Операция журнала**.</span><span class="sxs-lookup"><span data-stu-id="1a77c-130">To create transactions for several fixed assets, you can select **Group operations** \> **Lease** on the Action Pane of the **Journal voucher** page.</span></span>

22. <span data-ttu-id="1a77c-131">Выберите **Проверить** \> **Проверить**, чтобы проверить проводку.</span><span class="sxs-lookup"><span data-stu-id="1a77c-131">Select **Validate** \> **Validate** to validate the transaction.</span></span>
23. <span data-ttu-id="1a77c-132">Выберите **Разнести** \> **Разнести**, чтобы разнести журнал.</span><span class="sxs-lookup"><span data-stu-id="1a77c-132">Select **Post** \> **Post** to post the journal.</span></span> <span data-ttu-id="1a77c-133">Создаются транзации основного средства и главной книги.</span><span class="sxs-lookup"><span data-stu-id="1a77c-133">Fixed asset and ledger transactions are created.</span></span>

    <span data-ttu-id="1a77c-134">На странице **Основные средства** состояние основного средства меняется с **В эксплуатации** на **Сдача в аренду**.</span><span class="sxs-lookup"><span data-stu-id="1a77c-134">On the **Fixed assets** page, the status of the fixed asset changes from **In operation** to **Lending**.</span></span>

## <a name="register-the-return-of-a-leased-fixed-asset"></a><span data-ttu-id="1a77c-135">Регистрация возврата переданного в аренду основного средства</span><span class="sxs-lookup"><span data-stu-id="1a77c-135">Register the return of a leased fixed asset</span></span>

<span data-ttu-id="1a77c-136">Возврат переданного в аренду основного средства регистрируется таким же образом, как и его передача в аренду.</span><span class="sxs-lookup"><span data-stu-id="1a77c-136">You can register the return of a leased fixed asset in the same way that you registered the lease.</span></span> <span data-ttu-id="1a77c-137">Создайте проводку возврат из аренды на странице **Журнал ОС**, затем проверьте дату возврата на страницах **Одалживаемые ОС** и **Журнальные проводки**.</span><span class="sxs-lookup"><span data-stu-id="1a77c-137">Create a return-from-lease transaction on the **FA journal** page, and then verify the return date on the **FA on loan** and **Journal transactions** pages.</span></span>

1. <span data-ttu-id="1a77c-138">Перейдите в раздел **Основные средства (Россия)** \> **Общие** \> **Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="1a77c-138">Go to **Fixed assets (Russia)** \> **Common** \> **Fixed assets**.</span></span>
2. <span data-ttu-id="1a77c-139">Выберите сданное в аренду основное средство для возврата, затем на панели действий на вкладке **ОС** в группе **История** выберите **Аренда** для открытия страницы **Сданные в аренду ОС**.</span><span class="sxs-lookup"><span data-stu-id="1a77c-139">Select the leased fixed asset to return, and then, on the Action Pane, on the **Fixed asset** tab, in the **History** group, select **Lease** to open the **FA leased** page.</span></span>
3. <span data-ttu-id="1a77c-140">Создайте новую строку.</span><span class="sxs-lookup"><span data-stu-id="1a77c-140">Create a new line.</span></span>
4. <span data-ttu-id="1a77c-141">В поле **Фактическая дата возврата** просмотрите или измените дату, затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1a77c-141">In the **Actual return date** field, view or modify the date, and then close the page.</span></span>
5. <span data-ttu-id="1a77c-142">Выполните шаги 9 – 21 из процедуры [Передача основного средства в аренду](#lease-a-fixed-asset).</span><span class="sxs-lookup"><span data-stu-id="1a77c-142">Follow steps 9 through 21 in the [Lease a fixed asset](#lease-a-fixed-asset) procedure.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1a77c-143">В диалоговом окне **Добавить в журнал** необходимо выбрать **Возврат из аренды** в поле **Тип транзакции**, чтобы создать проводу возврата из аренды.</span><span class="sxs-lookup"><span data-stu-id="1a77c-143">In the **Add to journal** dialog box, you must select **Return from lease** in the **Transaction type** field to create a return-from-lease transaction.</span></span>

6. <span data-ttu-id="1a77c-144">Выберите **Проверить** \> **Проверить**, чтобы проверить проводку.</span><span class="sxs-lookup"><span data-stu-id="1a77c-144">Select **Validate** \> **Validate** to validate the transaction.</span></span>
7. <span data-ttu-id="1a77c-145">Выберите **Разнести** \> **Разнести**, чтобы разнести журнал.</span><span class="sxs-lookup"><span data-stu-id="1a77c-145">Select **Post** \> **Post** to post the journal.</span></span> <span data-ttu-id="1a77c-146">Создаются транзации основного средства и главной книги.</span><span class="sxs-lookup"><span data-stu-id="1a77c-146">Fixed asset and ledger transactions are created.</span></span>

    <span data-ttu-id="1a77c-147">На странице **Основные средства** состояние основного средства меняется с **Сдача в аренду** на **В эксплуатации**.</span><span class="sxs-lookup"><span data-stu-id="1a77c-147">On the **Fixed assets** page, the status of the fixed asset changes from **Lending** to **In operation**.</span></span>

> [!TIP]
> <span data-ttu-id="1a77c-148">Транзакции передачи в аренду и возврата из аренды реверсируются тем же образом, что и транзакции по приобретению.</span><span class="sxs-lookup"><span data-stu-id="1a77c-148">Lease and return-from-lease transactions are reversed in the same way as acquisition transactions.</span></span>
