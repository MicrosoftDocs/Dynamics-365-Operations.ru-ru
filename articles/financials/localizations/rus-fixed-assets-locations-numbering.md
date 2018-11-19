---
title: "Настройка расположений основных средств и нумерация (Россия)"
description: "В этом разделе описывается настройка расположения и нумерации для основного средства в России."
author: ShylaThompson
manager: AnnBe
ms.date: 10/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.search.industry: 
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: 77d54fe01075e125eae738fb4f8fc46d31ebaa09
ms.openlocfilehash: cabd98cdfd4217c3221708465c6ac99a6ed8b273
ms.contentlocale: ru-ru
ms.lasthandoff: 10/23/2018

---

# <a name="set-up-fixed-asset-locations-and-numbering-russia"></a><span data-ttu-id="91162-103">Настройка расположений основных средств и нумерация (Россия)</span><span class="sxs-lookup"><span data-stu-id="91162-103">Set up fixed asset locations and numbering (Russia)</span></span>

[!include [banner](../includes/banner.md)]

## <a name="set-up-a-fixed-asset-location"></a><span data-ttu-id="91162-104">Настройка местоположения ОС</span><span class="sxs-lookup"><span data-stu-id="91162-104">Set up a fixed asset location</span></span> 

<span data-ttu-id="91162-105">Местоположения определяется для основных средств и используются, чтобы рассчитывать начисления амортизации.</span><span class="sxs-lookup"><span data-stu-id="91162-105">Locations are defined for fixed assets and are used to calculate depreciation accrual.</span></span> <span data-ttu-id="91162-106">В зависимости от местоположения ОС вычисленная сумма амортизации относится или на производственные затраты продукта, или на счет ГК.</span><span class="sxs-lookup"><span data-stu-id="91162-106">Depending on the fixed asset location, the calculated depreciation amount is allocated either to the production cost of the product or to a ledger account.</span></span>

<span data-ttu-id="91162-107">Необходимо указать местоположение ОС, прежде чем приобрести основное средство.</span><span class="sxs-lookup"><span data-stu-id="91162-107">You must define the location of a fixed asset before you acquire the fixed asset.</span></span> <span data-ttu-id="91162-108">При перемещении основного средства из одного местоположения в другое можно создать транзакцию для регистрации перемещения средства.</span><span class="sxs-lookup"><span data-stu-id="91162-108">If you're transferring a fixed asset from one location to another, you can create a transfer transaction to register the transfer of the asset.</span></span>

<span data-ttu-id="91162-109">Можно использовать страницу **Местоположение ОС** для настройки местоположения ОС и указания подразделения компании, которому принадлежит ОС.</span><span class="sxs-lookup"><span data-stu-id="91162-109">You can use the **FA location** page to set up a fixed asset location and specify the company division that the asset belongs to.</span></span>

1. <span data-ttu-id="91162-110">Выберите **Основные средства (Россия)** \> **Настройка** \> **Местоположение**, чтобы открыть страницу **Местоположение ОС**.</span><span class="sxs-lookup"><span data-stu-id="91162-110">Select **Fixed assets (Russia)** \> **Setup** \> **Location** to open the **FA location** page.</span></span>
2. <span data-ttu-id="91162-111">Выберите **Создать**, чтобы создать местоположение ОС.</span><span class="sxs-lookup"><span data-stu-id="91162-111">Select **New** to create a fixed asset location.</span></span>
3. <span data-ttu-id="91162-112">В поле **Местоположение** введите код местоположения.</span><span class="sxs-lookup"><span data-stu-id="91162-112">In the **Location** field, enter a location code.</span></span> <span data-ttu-id="91162-113">В поле **Имя** введите описание местоположения.</span><span class="sxs-lookup"><span data-stu-id="91162-113">In the **Name** field, enter a description for the location.</span></span>
4. <span data-ttu-id="91162-114">Если местоположение ОС отличается от головного офиса компании, в поле **Код отдельного подразделения** выберите отдельное подразделение.</span><span class="sxs-lookup"><span data-stu-id="91162-114">If the fixed asset location is somewhere other than the company's head office, in the **Separate division ID** field, select a separate division.</span></span> <span data-ttu-id="91162-115">Если специально не указать обособленное подразделение, то местоположение ОС будет в головном офисе.</span><span class="sxs-lookup"><span data-stu-id="91162-115">If you don't specify a separate division, the location of the fixed asset is the head office.</span></span> <span data-ttu-id="91162-116">Если выбранное подразделение независимо, для параметра **Независимое** автоматически устанавливается значение **Да** (**[Настройка подразделения](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/rus-set-up-division/articles/financials/localizations/rus-company-divisions.md)**).</span><span class="sxs-lookup"><span data-stu-id="91162-116">If the selected division is independent, the **Independent** option is automatically set to **Yes** (**[Division setup](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/rus-set-up-division/articles/financials/localizations/rus-company-divisions.md)**).</span></span> 
5. <span data-ttu-id="91162-117">На экспресс-вкладке **Профили разноски по ОС** выберите **Создать** для создания строки.</span><span class="sxs-lookup"><span data-stu-id="91162-117">On the **Fixed asset posting profiles** FastTab, select **New** to create a line.</span></span>
7. <span data-ttu-id="91162-118">В поле **Группировки** выберите группировку для профиля разноски ОС:</span><span class="sxs-lookup"><span data-stu-id="91162-118">In the **Groupings** field, select the grouping for the fixed asset posting profile:</span></span>

    - <span data-ttu-id="91162-119">**Таблица** — профиль разноски группируется по выбранному ОС.</span><span class="sxs-lookup"><span data-stu-id="91162-119">**Table** – The posting profile is grouped by the selected fixed asset.</span></span>
    - <span data-ttu-id="91162-120">**Группа** — профиль разноски группируется по группе амортизации.</span><span class="sxs-lookup"><span data-stu-id="91162-120">**Group** – The posting profile is grouped by the depreciation group.</span></span>
    - <span data-ttu-id="91162-121">**Все** — профиль разноски группируется по всем основным средствам.</span><span class="sxs-lookup"><span data-stu-id="91162-121">**All** – The posting profile is grouped by all fixed assets.</span></span>
    - <span data-ttu-id="91162-122">**Учет** — профиль разноски группируется по модели стоимости.</span><span class="sxs-lookup"><span data-stu-id="91162-122">**Accounting** – The posting profile is grouped by the value model.</span></span>

8. <span data-ttu-id="91162-123">В поле **Связь счета** выберите группу амортизации, основное средство или модель стоимости, для которых используется профиль разноски.</span><span class="sxs-lookup"><span data-stu-id="91162-123">In the **Account relation** field, select the depreciation group, fixed asset, or value model that the posting profile is used for.</span></span>
9. <span data-ttu-id="91162-124">В поле **Счет ГК** выберите счет ГК для разноски проводок основных средств.</span><span class="sxs-lookup"><span data-stu-id="91162-124">In the **Main account** field, select the ledger account to use to post the fixed asset transactions.</span></span>
10. <span data-ttu-id="91162-125">В поле **Счет для аморт.премии** выберите счет ГК, который будет использоваться для разноски премии амортизации для основных средств, если премия амортизации применяется.</span><span class="sxs-lookup"><span data-stu-id="91162-125">In the **Account for depr.bonus** field, select the ledger account to use to post the depreciation bonus for the fixed asset, if a depreciation bonus applies.</span></span>

## <a name="set-up-fixed-asset-numbering"></a><span data-ttu-id="91162-126">Настройка нумерации основных средств</span><span class="sxs-lookup"><span data-stu-id="91162-126">Set up fixed asset numbering</span></span>

<span data-ttu-id="91162-127">Имеется два варианта для назначения номеров основным средствам:</span><span class="sxs-lookup"><span data-stu-id="91162-127">You have two options for assigning numbers to fixed assets:</span></span>

- <span data-ttu-id="91162-128">**Ручной выбор** — этот параметр подходит для компании, которая имеет несколько основных средств.</span><span class="sxs-lookup"><span data-stu-id="91162-128">**Manual selection** – This option is appropriate for a company that has few fixed assets.</span></span> <span data-ttu-id="91162-129">Настройка не является обязательной для ручного выбора.</span><span class="sxs-lookup"><span data-stu-id="91162-129">No setup is required for manual selection.</span></span>
- <span data-ttu-id="91162-130">**Автоматическая нумерация основных средств, которая базируется на группе ОС** — этот параметр подходит для компании, которая имеет много основных средств.</span><span class="sxs-lookup"><span data-stu-id="91162-130">**Automatic numbering of fixed assets that is based on the fixed asset group** – This option is appropriate for a company that has many fixed assets.</span></span> <span data-ttu-id="91162-131">На странице **Группы ОС** можно создать много номеров счетов или групп для основных средств и присоединить номерную серию к каждой группе (**Основные средства (Россия)** \> **Настройка** \> **Группы ОС**).</span><span class="sxs-lookup"><span data-stu-id="91162-131">On the **FA groups** page, you can create many account/group numbers for fixed assets and attach a number sequence to each group (**Fixed assets (Russia)** \> **Setup** \> **FA groups**).</span></span> <span data-ttu-id="91162-132">Необходимо указать номерную серию по умолчанию при настройке основных средств.</span><span class="sxs-lookup"><span data-stu-id="91162-132">You must specify a default number sequence when you set up fixed assets.</span></span>

### <a name="set-up-automatic-numbering-of-all-fixed-assets-from-one-default-number-sequence"></a><span data-ttu-id="91162-133">Настройка автоматической нумерации всех ОС из одной номерной серии по умолчанию</span><span class="sxs-lookup"><span data-stu-id="91162-133">Set up automatic numbering of all fixed assets from one default number sequence</span></span>

1. <span data-ttu-id="91162-134">Выберите **Администрирование организации** \> **Номерные серии** \> **Номерные серии** и создайте номерную серию по умолчанию, используемую для нумерации основных средств.</span><span class="sxs-lookup"><span data-stu-id="91162-134">Select **Organization administration** \> **Number sequences** \> **Number sequences**, and create a default number sequence that is used to number fixed assets.</span></span>
2. <span data-ttu-id="91162-135">Выберите **Основные средства (Россия)** \> **Настройка** \> **Параметры**, чтобы открыть страницу **Параметры основных средств**.</span><span class="sxs-lookup"><span data-stu-id="91162-135">Select **Fixed assets (Russia)** \> **Setup** \> **Parameters** to open the **Fixed asset parameters** page.</span></span>
3. <span data-ttu-id="91162-136">На вкладке **Номерные серии** выберите код номерной серии, который будет использоваться для автоматического создания номера ОС.</span><span class="sxs-lookup"><span data-stu-id="91162-136">On the **Number sequences** tab, select a number sequence code, which is used for automatic creation of fixed asset number</span></span>
4. <span data-ttu-id="91162-137">На вкладке **Основные средства** задайте для параметра **Автонумерация ОС** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="91162-137">On the **Fixed assets** tab, set the **Autonumeration FA** option to **Yes**.</span></span> 

<span data-ttu-id="91162-138">Если для параметра **Автонумерация ОС** установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="91162-138">If **Autonumeration FA** option is set to **Yes**.</span></span> <span data-ttu-id="91162-139">Затем при создании основного средства на странице **Основные средства** (**Основные средства (Россия)** \> **Обычные** \> **Основные средства**) автоматически вводится следующий номер в серии в поле **Инвентарный номер ОС**.</span><span class="sxs-lookup"><span data-stu-id="91162-139">then when you create a fixed asset on the **Fixed assets** page (**Fixed assets (Russia)** \> **Common** \> **Fixed assets**), the next number in the sequence is automatically entered in the **FA inventory number** field.</span></span>

### <a name="set-up-automatic-numbering-of-fixed-assets-that-is-based-on-the-fixed-asset-group"></a><span data-ttu-id="91162-140">Настройка автоматической нумерации основных средств, которая основана на группе основных средств</span><span class="sxs-lookup"><span data-stu-id="91162-140">Set up automatic numbering of fixed assets that is based on the fixed asset group</span></span>

1. <span data-ttu-id="91162-141">Выберите **Основные средства (Россия)** \> **Настройка** \> **Группы ОС**.</span><span class="sxs-lookup"><span data-stu-id="91162-141">Select **Fixed assets (Russia)** \> **Setup** \> **FA groups**.</span></span>
2. <span data-ttu-id="91162-142">Установите флажок **Автонумерация ОС** для выбранной группы основных средств, затем выберите соответствующую номерную серию в поле **Серия автоматической нумерации**.</span><span class="sxs-lookup"><span data-stu-id="91162-142">Select the **Autonumeration FA** check box for the selected fixed asset group, and then select the appropriate number sequence in the **FA autonumbering sequence** field.</span></span>

<span data-ttu-id="91162-143">Эта номерная серия используется для всех ОС, назначенных группе ОС.</span><span class="sxs-lookup"><span data-stu-id="91162-143">This number sequence is used for all fixed assets that are assigned to the fixed asset group.</span></span>

> [!NOTE]
> <span data-ttu-id="91162-144">Чтобы создать группу основных средств, выберите **Создать**, затем введите нужные сведения.</span><span class="sxs-lookup"><span data-stu-id="91162-144">To create a fixed asset group, select **New**, and then enter the required details.</span></span>

## <a name="create-bar-codes-from-fixed-asset-numbers"></a><span data-ttu-id="91162-145">Создание штрих-кодов из номеров основных средств</span><span class="sxs-lookup"><span data-stu-id="91162-145">Create bar codes from fixed asset numbers</span></span>

1. <span data-ttu-id="91162-146">Выберите **Основные средства (Россия)** \> **Периодические операции** \> **Формирование штрих-код из инв. номера ОС**.</span><span class="sxs-lookup"><span data-stu-id="91162-146">Select **Fixed assets (Russia)** \> **Periodic** \> **Create barcodes from FA inventory number**.</span></span>
2. <span data-ttu-id="91162-147">На экспресс-вкладке **Включаемые записи** выберите **Фильтр**, затем в диалоговом окне **Активы** введите критерии, которые используются для выбора основных средств.</span><span class="sxs-lookup"><span data-stu-id="91162-147">On the **Records to include** FastTab, select **Filter**, and then, in the **Assets** dialog box, enter the criteria that are used to select fixed assets.</span></span> <span data-ttu-id="91162-148">Затем выберите **OK**, чтобы вернуться в диалоговое окно **Формирование штрих-код из инв. номера ОС**.</span><span class="sxs-lookup"><span data-stu-id="91162-148">Then select **OK** to return to the **Create barcodes from FA inventory number** dialog box.</span></span>
4. <span data-ttu-id="91162-149">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="91162-149">Select **OK**.</span></span> <span data-ttu-id="91162-150">Если не указан штрих-код для основного средства, значение, указанное в поле **Инвентарный номер ОС** появится в поле **Штрих-код** на странице **Основные средства** (**Основные средства (Россия)** \> **Обычные** \> **Основные средства**).</span><span class="sxs-lookup"><span data-stu-id="91162-150">If you haven't specified a bar code for the fixed asset, the value that you specified in the **FA inventory number** field appears in the **Bar code** field on the **Fixed assets** page (**Fixed assets (Russia)** \> **Common** \> **Fixed assets**).</span></span>

