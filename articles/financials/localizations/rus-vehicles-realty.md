---
title: Транспортные средства и недвижимость как основные средства (Россия)
description: В этом разделе описан порядок настройки и использования транспортных средств и недвижимости в качестве основных средств для России.
author: ShylaThompson
manager: AnnBe
ms.date: 02/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.search.industry: ''
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: cffd72a5c83d4dc787898a64b9acc80f6599bf64
ms.sourcegitcommit: 385f3c53308e19077c846c7bfda0ed65be8467a5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2019
ms.locfileid: "403951"
---
# <a name="vehicles-and-realty-as-fixed-assets-russia"></a><span data-ttu-id="7b9d7-103">Транспортные средства и недвижимость как основные средства (Россия)</span><span class="sxs-lookup"><span data-stu-id="7b9d7-103">Vehicles and realty as fixed assets (Russia)</span></span>

[!include [banner](../includes/banner.md)]

## <a name="set-up-fixed-asset-parameters-for-vehicles-and-realty"></a><span data-ttu-id="7b9d7-104">Настройка параметров основного средства для транспортных средств и недвижимости</span><span class="sxs-lookup"><span data-stu-id="7b9d7-104">Set up fixed asset parameters for vehicles and realty</span></span>

<span data-ttu-id="7b9d7-105">Используйте страницу **Параметры основных средств** для настройки параметров для основных средств типов **Недвижимость** и **Транспортное средство**.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-105">Use the **Fixed asset parameters** page to set up parameters for fixed assets of the **Realty** and **Vehicle** types.</span></span> <span data-ttu-id="7b9d7-106">Можно также выбрать метод, который используется для определения начальной даты для расчета амортизации.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-106">You can also select the method that is used to determine the start date for the calculation of depreciation.</span></span>

1. <span data-ttu-id="7b9d7-107">Выберите **Основные средства (Россия)** \> **Настройка** \> **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-107">Select **Fixed assets (Russia)** \> **Setup** \> **Parameters**.</span></span>
2. <span data-ttu-id="7b9d7-108">На вкладке **Налоговая отчетность** в поле **Дата включения в налоговую базу** укажите, когда основное средство должно быть введено в налоговую базу налога на имущество:</span><span class="sxs-lookup"><span data-stu-id="7b9d7-108">On the **Tax reporting** tab, in the **Date of including in the tax base** field, specify when the fixed asset should be entered in tax base of the assessed register:</span></span>

    - <span data-ttu-id="7b9d7-109">**Даты ввода в эксплуатацию** — дата, когда основное средство введено в эксплуатацию.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-109">**Putting into operation date** – The date when the fixed asset is put to use.</span></span>
    - <span data-ttu-id="7b9d7-110">**Дата регистрации** — дата регистрации основного средства.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-110">**Date of the registration** – The registration date of the fixed asset.</span></span>

## <a name="register-realty-as-a-fixed-asset"></a><span data-ttu-id="7b9d7-111">Регистрация недвижимости как основного средства</span><span class="sxs-lookup"><span data-stu-id="7b9d7-111">Register realty as a fixed asset</span></span>

<span data-ttu-id="7b9d7-112">Перед вводом в эксплуатацию объекта недвижимости и расчетом амортизации необходимо зарегистрировать основное средство в регистрах налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-112">Before you put a realty fixed asset into operation and calculate depreciation, you must register the fixed asset in the assessed tax registers.</span></span> <span data-ttu-id="7b9d7-113">Используйте страницу **Основные средства** для регистрации основного средства типа **Недвижимость**.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-113">Use the **Fixed assets** page to register a fixed asset of the **Realty** type.</span></span>

1. <span data-ttu-id="7b9d7-114">Выберите **Основные средства (Россия)** \> **Общие** \> **Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-114">Select **Fixed assets (Russia)** \> **Common** \> **Fixed assets**.</span></span>
2. <span data-ttu-id="7b9d7-115">Выберите **Создать**, чтобы создать группу основных средств, затем введите нужные сведения.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-115">Select **New** to create a fixed asset, and enter the required details.</span></span>
3. <span data-ttu-id="7b9d7-116">На экспресс-вкладке **Общее** в поле **Тип** выберите **Недвижимость**.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-116">On the **General** FastTab, in the **Type** field, select **Realty**.</span></span>
4. <span data-ttu-id="7b9d7-117">На экспресс-вкладке **Техническая информация** в поле **Дата регистрации** выберите дату регистрации основного средства.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-117">On the **Technical information** FastTab, in the **Date of the registration** field, select the registration date of the fixed asset.</span></span>
   
5. <span data-ttu-id="7b9d7-118">В поле **Дата удаления из регистра** выберите дату, когда следует удалить актив из налогового реестра.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-118">In the **Removal from the register date** field, select the date when the asset should be removed from the tax register.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7b9d7-119">Поля **Дата регистрации** и **Дата удаления из регистра** доступны только в том случае, если вы выбрали **Недвижимость** или **Транспортное средство** в поле **Тип** на экспресс-вкладке **Общие**.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-119">The **Date of the registration** and **Removal from the register date** fields are available only if you selected **Realty** or **Vehicle** in the **Type** field on the **General** FastTab.</span></span>

6. <span data-ttu-id="7b9d7-120">На экспресс-вкладке **Налоговая отчетность** в разделе **Налог на имущество** в поле **Вид имущества** выберите тип актива.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-120">On the **Tax reporting** FastTab, in the **Assessed tax** section, in the **Asset kind** field, select the type of asset.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7b9d7-121">Раздел **Налог на имущество** недоступен, если выбрано значение **Транспортное средство** или **Земельный участок** в поле **Тип** на экспресс-вкладке **Общие**.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-121">The **Assessed tax** section isn't available if you selected **Vehicle** or **Ground area** in the **Type** field on the **General** FastTab.</span></span>

7. <span data-ttu-id="7b9d7-122">В поле **Налоговый код** выберите налоговый код для налога на имущество.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-122">In the **Sales tax code** field, select the sales tax code for the assessed tax.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7b9d7-123">Поле **Код налога** доступно только в том случае, если вы выбрали **1** или **3** в поле **Вид имущества**.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-123">The **Sales tax code** field is available only if you selected **1** or **3** in the **Asset kind** field.</span></span>

8. <span data-ttu-id="7b9d7-124">В поле **Освобождение от налога** выберите код налоговой льготы для транспортного налога.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-124">In the **Exemption from tax** field, select the tax benefit code for the transport tax.</span></span>

## <a name="set-up-the-depreciation-start-date-for-vehicles-and-realty"></a><span data-ttu-id="7b9d7-125">Настройка даты начала амортизации для транспортных средств и недвижимости</span><span class="sxs-lookup"><span data-stu-id="7b9d7-125">Set up the depreciation start date for vehicles and realty</span></span>

<span data-ttu-id="7b9d7-126">Используйте страницу **Амортизационные группы**, чтобы задать дату начала для амортизации основных средств типов **Недвижимость** и **Транспортное средство**.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-126">Use the **Depreciation groups** page to set up the start date for depreciation of fixed assets of the **Realty** and **Vehicle** types.</span></span> <span data-ttu-id="7b9d7-127">Амортизация рассчитывается на основе даты регистрации актива.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-127">Depreciation is calculated based on the registration date of the asset.</span></span> <span data-ttu-id="7b9d7-128">Если актив зарегистрирован после ввода в эксплуатацию, амортизация вычисляется с первого дня месяца регистрации.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-128">If an asset is registered after it's put into operation, depreciation is calculated from the first day of the month of registration.</span></span> <span data-ttu-id="7b9d7-129">Если актив зарегистрирован до ввода в эксплуатацию, амортизация вычисляется с первого дня месяца после ввода актива в эксплуатацию.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-129">If an asset is registered before it's put into operation, depreciation is calculated from the first day of the month after the asset is put into operation.</span></span>

1. <span data-ttu-id="7b9d7-130">Выберите **Основные средства (Россия)** \> **Настройка** \> **Группы амортизации**.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-130">Select **Fixed assets (Russia)** \> **Setup** \> **Depreciation groups**.</span></span>
2. <span data-ttu-id="7b9d7-131">Создайте группу амортизации, затем введите требуемую информацию.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-131">Create a depreciation group, and enter the required details.</span></span>
3. <span data-ttu-id="7b9d7-132">На экспресс-вкладке **Общие** в поле **Дата начала начисления амортизации** выберите **Дата регистрации**, чтобы указать, что дату регистрации ОС следует использовать в качестве даты начала амортизации.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-132">On the **General** FastTab, in the **Depreciation start date** field, select **Date of the registration** to specify that the registration date of a fixed asset should be used as the depreciation start date.</span></span>

## <a name="depreciate-a-fixed-asset-by-using-a-fixed-asset-journal"></a><span data-ttu-id="7b9d7-133">Амортизация основного средства с помощью журнала основных средств</span><span class="sxs-lookup"><span data-stu-id="7b9d7-133">Depreciate a fixed asset by using a fixed asset journal</span></span>

<span data-ttu-id="7b9d7-134">После ввода в эксплуатацию основного средства типа **Транспортное средство** или **Недвижимость** можно использовать страницу **Журнал ОС**, чтобы начать амортизацию основного средства с даты регистрации.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-134">After you put a fixed asset of the **Vehicle** or **Realty** type into operation, you can use the **FA journal** page to start to depreciate the asset from the registration date.</span></span>

1. <span data-ttu-id="7b9d7-135">Выберите **Основные средства (Россия)** \> **Журналы** \> **Журнал ОС**.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-135">Select **Fixed assets (Russia)** \> **Journals** \> **FA journal**.</span></span>
2. <span data-ttu-id="7b9d7-136">Выберите **Создать**, чтобы создать журнал ОС.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-136">Select **New** to create a fixed asset journal.</span></span>
3. <span data-ttu-id="7b9d7-137">В поле **Имя** выберите имя журнала.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-137">In the **Name** field, select a journal name.</span></span>
4. <span data-ttu-id="7b9d7-138">В поле **Описание** введите описание журнала.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-138">In the **Description** field, enter a description of the journal.</span></span>
5. <span data-ttu-id="7b9d7-139">Выберите **Строки**, чтобы открыть страницу **Ваучер журнала**.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-139">Select **Lines** to open the **Journal voucher** page.</span></span>
6. <span data-ttu-id="7b9d7-140">Выберите **Создать**, чтобы создать строку журнала.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-140">Select **New** to create a journal line.</span></span>
7. <span data-ttu-id="7b9d7-141">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-141">Select **OK**.</span></span> <span data-ttu-id="7b9d7-142">Строка амортизации для модели стоимости, которая была зарегистрирована в счете основного средства, отображается на странице **Ваучер журнала**.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-142">The depreciation line for the value model that is registered in the fixed asset account is shown on the **Journal voucher** page.</span></span>
8. <span data-ttu-id="7b9d7-143">Выберите пункт меню **Проверка** \> **Проверка**, чтобы проверить транзакцию амортизации.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-143">Select **Validate** \> **Validate** to validate the depreciation transaction.</span></span>
9. <span data-ttu-id="7b9d7-144">Выберите **Разнести** \> **Разнести**, чтобы разнести транзакцию.</span><span class="sxs-lookup"><span data-stu-id="7b9d7-144">Select **Post** \> **Post** to post the transaction.</span></span>
