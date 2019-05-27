---
title: Основные средства (Россия)
description: В этой теме содержится информация об управлении основными средствами для России.
author: ShylaThompson
manager: AnnBe
ms.date: 04/19/2019
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
ms.openlocfilehash: 1e85f8f2faf4c537d432124197ff6edf52180012
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1538369"
---
# <a name="fixed-assets-russia"></a><span data-ttu-id="5aa7a-103">Основные средства (Россия)</span><span class="sxs-lookup"><span data-stu-id="5aa7a-103">Fixed assets (Russia)</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5aa7a-104">Для управления основными средствами компании можно использовать страницу **Основные средства** для сохранения всей информации (как финансовой, так и не финансовой) об активах.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-104">To manage your company's fixed assets, you can use the **Fixed assets** page to store all information (both financial and non-financial) on assets.</span></span> <span data-ttu-id="5aa7a-105">В следующих примерах показаны типы финансовой информации, которая относится к основным средствам:</span><span class="sxs-lookup"><span data-stu-id="5aa7a-105">The following examples show the types of financial information that is related to fixed assets:</span></span>

-   <span data-ttu-id="5aa7a-106">Стоимость приобретения основного средства</span><span class="sxs-lookup"><span data-stu-id="5aa7a-106">Asset acquisition cost</span></span>
-   <span data-ttu-id="5aa7a-107">Корректировка стоимости</span><span class="sxs-lookup"><span data-stu-id="5aa7a-107">Cost adjustment</span></span>
-   <span data-ttu-id="5aa7a-108">Сумма амортизации основного средства</span><span class="sxs-lookup"><span data-stu-id="5aa7a-108">Asset depreciation amount</span></span>
-   <span data-ttu-id="5aa7a-109">Бюджет основного средства</span><span class="sxs-lookup"><span data-stu-id="5aa7a-109">Asset budget</span></span>
-   <span data-ttu-id="5aa7a-110">Информация по налогам</span><span class="sxs-lookup"><span data-stu-id="5aa7a-110">Tax information</span></span>

<span data-ttu-id="5aa7a-111">В следующих примерах показаны типы нефинансовой информации, которая относится к основным средствам:</span><span class="sxs-lookup"><span data-stu-id="5aa7a-111">The following examples show the types of non-financial information that is related to fixed assets:</span></span>

-   <span data-ttu-id="5aa7a-112">Техн. информация</span><span class="sxs-lookup"><span data-stu-id="5aa7a-112">Technical information</span></span>
-   <span data-ttu-id="5aa7a-113">Местоположение</span><span class="sxs-lookup"><span data-stu-id="5aa7a-113">Location</span></span>
-   <span data-ttu-id="5aa7a-114">Штриховые коды и инвентарные номера</span><span class="sxs-lookup"><span data-stu-id="5aa7a-114">Bar codes and inventory numbers</span></span>
-   <span data-ttu-id="5aa7a-115">Страхование</span><span class="sxs-lookup"><span data-stu-id="5aa7a-115">Insurance</span></span>
-   <span data-ttu-id="5aa7a-116">Связи между различными активами</span><span class="sxs-lookup"><span data-stu-id="5aa7a-116">Relationships between different assets</span></span>

## <a name="register-fixed-assets"></a><span data-ttu-id="5aa7a-117">Регистрация основных средств</span><span class="sxs-lookup"><span data-stu-id="5aa7a-117">Register fixed assets</span></span>

<span data-ttu-id="5aa7a-118">Перед созданием проводок для любого основного средства или нематериального актива необходимо сначала зарегистрировать запись актива и предоставить основную информацию о нем.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-118">Before you create transactions for any fixed or intangible asset, you must first register the asset record, and provide basic information about it.</span></span>

1. <span data-ttu-id="5aa7a-119">Для регистрации основного средства выберите **Основные средства (Россия)** \> **Основные** \> **Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-119">To register a fixed asset, select **Fixed Assets (Russia)** \> **Common** \> **Fixed Assets**.</span></span> <span data-ttu-id="5aa7a-120">Выберите **Создать**, чтобы создать новое основное средство.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-120">Select **New** to create a new fixed asset.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5aa7a-121">Можно создать новое основное средство, используя функцию копирования (кнопка **ОСНОВНОЕ СРЕДСТВО** \> **Копировать ОС**).</span><span class="sxs-lookup"><span data-stu-id="5aa7a-121">You can create a new fixed asset using the copy function (**FIXED ASSET** \> **Copy FA** button).</span></span> <span data-ttu-id="5aa7a-122">Система копирует выбранные основные средства со всеми его параметрами, но с другим инвентарным номером.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-122">The system copies the selected fixed asset with all its parameters, but with a different inventory number.</span></span>

![Вкладка "Общие" страницы ОС](media/RUS_FA_1%20General%20tab.JPG)

2. <span data-ttu-id="5aa7a-124">Заполните следующие поля на экспресс-вкладке **Общее**:</span><span class="sxs-lookup"><span data-stu-id="5aa7a-124">Fill in the following fields on the **General** FastTab:</span></span>

- <span data-ttu-id="5aa7a-125">**Группа ОС** — выберите группу основных средств, с которой должно быть связано основное средство.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-125">**FA group** - Select the fixed asset group the fixed asset should be related to.</span></span>

- <span data-ttu-id="5aa7a-126">**Инвентарный номер** — если автоматическая нумерация настроена в **Параметры основных средств** или для группы основных средств, сведения заполняются автоматически.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-126">**Inventory number** - If automatic numbering is set up in the **Fixed asset parameters** or for the fixed assets group, the information is filled in automatically.</span></span>

- <span data-ttu-id="5aa7a-127">**Имя** — введите название основного средства.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-127">**Name** - Enter the name of the fixed asset.</span></span>

- <span data-ttu-id="5aa7a-128">**Дата приобретения** — по умолчанию это поле заполняется автоматически текущей датой системы, но может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-128">**Acquisition date** - By default, this field is filled in automatically with the current system date but can be changed.</span></span>

- <span data-ttu-id="5aa7a-129">**Стоимость приобретения** — введите стоимость приобретения основных средств в основной валюте компании.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-129">**Acquisition cost** - Enter a fixed asset acquisition value in the company's home currency.</span></span> <span data-ttu-id="5aa7a-130">Если основные средства получены из модели РБП, отображается сумма накладной без налогов в основной валюте компании.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-130">If the fixed asset came from the deferrals model, the invoice amount without taxes in the company's home currency is displayed.</span></span>

- <span data-ttu-id="5aa7a-131">**Примечания** — введите любые дополнительные сведения об этом основном средстве.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-131">**Notes** - Enter any additional information about this fixed asset.</span></span>

- <span data-ttu-id="5aa7a-132">**Тип** — выбор типа основного средства.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-132">**Type** - Select a fixed asset type.</span></span> <span data-ttu-id="5aa7a-133">В зависимости от значения в этом поле другие поля активируются на экспресс-вкладках **Технические сведения** и **Налоговая отчетность**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-133">Depending on the value in this field, the different fields are activated on the **Technical Information** and **Tax Reporting** FastTabs.</span></span> <span data-ttu-id="5aa7a-134">Ниже приведены примеры типов основного средства.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-134">The following are examples of fixed asset types.</span></span> 

    - <span data-ttu-id="5aa7a-135">**Транспортное средство** — этот флажок устанавливается для отображения группы полей **Государственная регистрация** на экспресс-вкладке **Техническая информация**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-135">**Vehicle** - Select this for the **Government registration** field group to appear on the **Technical Information** FastTab.</span></span>

    - <span data-ttu-id="5aa7a-136">**Недвижимость** — этот флажок устанавливается, чтобы поле **Налоговая база** отображалось на экспресс-вкладке **Налоговая отчетность**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-136">**Realty** - Select this for the **Tax base** field to appear on the **Tax Reporting** FastTab.</span></span>

    - <span data-ttu-id="5aa7a-137">**Земельный участок** — этот флажок устанавливается для отображения поля **Дата начала строительства** на экспресс-вкладке **Техническая информация**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-137">**Ground area** - Select this for the **Start date of building** field to appear on the **Technical Information** FastTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5aa7a-138">Следующие типы не могут быть выбраны на странице **Основные средства**: МОС, Спецодежда, Спецоснастка.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-138">The following types cannot be selected on the **Fixed asset** page: NVFA, Working clothes, Special rigging.</span></span> <span data-ttu-id="5aa7a-139">Для этих типов имеются специальные страницы.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-139">There are special pages for these types.</span></span> <span data-ttu-id="5aa7a-140">Дополнительные сведения см. в разделах [Учет малоценных основных средств (МОС) для России](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/localizations/rus-not-valuable-assets) и [Учет спецодежды и спецоснастки для России](https://docs.microsoft.com/dynamics365/unified-operations/financials/localizations/rus-working-clothes-instruments-accounting).</span><span class="sxs-lookup"><span data-stu-id="5aa7a-140">For more information, see [Not valuable fixed assets (NVFAs) accounting for Russia](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/localizations/rus-not-valuable-assets) and [Working clothes/Special riggings accounting for Russia](https://docs.microsoft.com/dynamics365/unified-operations/financials/localizations/rus-working-clothes-instruments-accounting).</span></span>

- <span data-ttu-id="5aa7a-141">Группа полей **Страхование** — при необходимости заполните поля для страховки.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-141">**Insurance** field group – Fill in the fields for insurance, if needed.</span></span>

- <span data-ttu-id="5aa7a-142">**Флаг владения** — выберите соответствующее значение, по умолчанию это значение равно **Собственность**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-142">**Flag of ownership** - Select the appropriate value, by default the value is equal to **Ownership**.</span></span>

- <span data-ttu-id="5aa7a-143">**Штрих-код** — можно ввести штрих-код вручную или штрих-код может быть создан автоматически (то же, что и инвентарный номер актива).</span><span class="sxs-lookup"><span data-stu-id="5aa7a-143">**Bar code** - You can enter the bar code manually, or the bar code can be generated automatically (the same as the asset inventory number).</span></span> <span data-ttu-id="5aa7a-144">Для автоматического создания штрих-кода выберите **Штрих-код совпадает с инвентарным номером** в параметрах **Основные средства** (**Основные средства \> Основные средства** \> **Параметры**).</span><span class="sxs-lookup"><span data-stu-id="5aa7a-144">To generate a bar code automatically, select **Bar code equals inventory number** in the **Fixed assets** parameters (**Fixed Assets \> Fixed Assets** \> **Parameters**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="5aa7a-145">Поля **Местоположение** и **Код работника** заполняются автоматически при создании записи в списке страницы **Передача ОС**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-145">The **Location** and **Worker ID** fields are filled in automatically when you create a record in the **Transfer FA** page list.</span></span> <span data-ttu-id="5aa7a-146">(**Основные средства (Россия)** \> **Общее** \> **Основные средства**, нажмите **ОСНОВНОЕ СРЕДСТВО** \> **ИСТОРИЯ** \> **Перемещение**).</span><span class="sxs-lookup"><span data-stu-id="5aa7a-146">(**Fixed asset (Russia)** \> **Common** \> **Fixed assets**, click **FIXED ASSET** \> **HISTORY** \> **Transfer**).</span></span>

- <span data-ttu-id="5aa7a-147">**Выпуск/пробег** — введите размер предполагаемого производства или пробега основного средства, если профиль амортизации **Выпуск продукции/пробег** выбран для основного средства в поле **Модель учета**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-147">**Output/mileage** - Enter the size of assumed production/travel of the fixed asset if **Product output/mileage** depreciation profile is selected for FA in a **Value model**.</span></span> <span data-ttu-id="5aa7a-148">В этом случае необходимо ввести записи в список страницы **Выпуск продукции/пробег**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-148">In this case, you  should input records on the **Product Output/Mileage** page list.</span></span>

![Страница выпуска или пробега](media/RUS_FA_2%20Output_Mileage%20page.JPG)

3. <span data-ttu-id="5aa7a-150">Если основное средство включено в состав другого основного средства, выберите экспресс-вкладку **Структура**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-150">If a fixed asset is included in the composition of another fixed asset, select the **Structure** FastTab.</span></span> <span data-ttu-id="5aa7a-151">Выберите код основного средства в поле **Главное ОС**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-151">Select the fixed asset code in the **Main fixed asset** field.</span></span>

4. <span data-ttu-id="5aa7a-152">В поле **Структура ОС** все счета ОС, имеющие ссылку на этот актив, отображаются в главном ОС.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-152">In the **FA structure** field, all fixed asset accounts that have a reference to the asset are displayed in the main fixed asset.</span></span>

5. <span data-ttu-id="5aa7a-153">Выберите экспресс-вкладку **Покупка/продажа**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-153">Select the **Purchase/Sale** FastTab.</span></span> <span data-ttu-id="5aa7a-154">Отображаются сведения о покупке и продаже основного средства.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-154">Information about the purchase and sale of the fixed asset is displayed.</span></span>

## <a name="fixed-asset-value-models"></a><span data-ttu-id="5aa7a-155">Модели стоимости ОС</span><span class="sxs-lookup"><span data-stu-id="5aa7a-155">Fixed asset value models</span></span>

<span data-ttu-id="5aa7a-156">Выполните следующие действия, чтобы обновить или создать модели стоимости для основного средства.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-156">Follow these steps to update or create value models for the fixed asset.</span></span>

1. <span data-ttu-id="5aa7a-157">Выберите кнопку **Модели стоимости**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-157">Select the **Value Models** button.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5aa7a-158">Если модели стоимости настроены для группы основных средств, которой назначено основное средство (**Основные средства (Россия) \> Настройка \> Группы ОС**), то система автоматически создает модели стоимости, и можно обновлять значения полей.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-158">If value models are set up for the fixed asset group, which the fixed asset is assigned to (**Fixed asset (Russia) \> Setup \> FA groups**), then the system creates the value models automatically and you can update field values.</span></span>

2. <span data-ttu-id="5aa7a-159">Необходимо создать модель стоимости для каждого ОС, и настройки используются для регистрации проводки.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-159">You need to create a value model for each asset, and the settings are used to register a transaction.</span></span> <span data-ttu-id="5aa7a-160">Выберите **Создать** для создания новой строки.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-160">Select **New** to create a new line.</span></span> <span data-ttu-id="5aa7a-161">Заполните следующие поля на экспресс-вкладке **Общее**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-161">Fill in the following fields on the **General** FastTab.</span></span>

![Модель учета ОС](media/RUS_FA_3%20value%20models.JPG)

- <span data-ttu-id="5aa7a-163">**Модель стоимости** — выберите корд модели для основного средства.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-163">**Value model** - Select the model code for the asset.</span></span>

- <span data-ttu-id="5aa7a-164">**Амортизационные группы** — выберите группу амортизации в модели стоимости, к которой относится основное средство.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-164">**Depreciation groups** - Select a depreciation group within the value model that the fixed asset relates to.</span></span>

- <span data-ttu-id="5aa7a-165">**Методы амортизации** — выберите профиль амортизации.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-165">**Depreciation methods** - Select the depreciation profile.</span></span> <span data-ttu-id="5aa7a-166">По умолчанию отображается значение, заданное для группы амортизации, но его можно изменить.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-166">By default, the value specified for the depreciation group is displayed, but you can change it.</span></span>

- <span data-ttu-id="5aa7a-167">**Профиль разноски** — выберите профиль разноски, который будет использоваться в модели стоимости.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-167">**Posting profile** - Select the posting profile used in the value model.</span></span> <span data-ttu-id="5aa7a-168">По умолчанию значение основано на параметрах модели стоимости.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-168">By default, the value is based on the value model settings.</span></span>

- <span data-ttu-id="5aa7a-169">**Стоимость приобретения** — введите сумму приобретения основного средства.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-169">**Acquisition cost** - Enter the acquisition amount of the fixed asset.</span></span> <span data-ttu-id="5aa7a-170">Если проводка покупки актива была создана, отображается сумма проводки без налогов.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-170">If an asset purchase transaction has been created, the transaction amount without taxes is displayed.</span></span> <span data-ttu-id="5aa7a-171">Если валюта приобретения ОС отлична от валюты, настроенной для этой модели стоимости, валюты преобразуются на дату приобретения.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-171">If the fixed asset acquisition currency is different from the currency set up for this value model, the currencies are converted on the acquisition date.</span></span>

- <span data-ttu-id="5aa7a-172">**Дата начала амортизации** — выберите дату начала начисления амортизации.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-172">**Date of depreciation beginning** - Select the date to start accruing depreciation.</span></span> <span data-ttu-id="5aa7a-173">По умолчанию это поле заполняется в соответствии с настройкой, выбранной в поле **Группа амортизации**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-173">By default, this field is filled in according to the setting selected in the **Depreciation group**.</span></span> <span data-ttu-id="5aa7a-174">Если параметр **Дата начала амортизации** настроен как **С начала следующего месяца**, то это поле заполняется периодом, который следует за периодом приобретения.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-174">If the **Depreciation start date** parameter is set up as **Next month start**, then this field is filled in with the period that follows the period of acquisition.</span></span>

- <span data-ttu-id="5aa7a-175">**Валюта** — выберите валюту для модели стоимости для актива.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-175">**Currency** - Select a currency for the value model for the asset.</span></span> <span data-ttu-id="5aa7a-176">Отображается валюта по умолчанию из параметров модели стоимости.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-176">The default currency from the value model settings is displayed.</span></span>

- <span data-ttu-id="5aa7a-177">**Остаточная стоимость после списания** — введите остаток суммы ОС после списания.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-177">**Remains cost after writing-off** - Enter the remaining amount of the fixed asset after writing off.</span></span> <span data-ttu-id="5aa7a-178">Если значение заполнено, то остаточная стоимость, используемая в расчете амортизации, меньше значения в этом поле.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-178">If a value is filled in, then the book value used in the depreciation calculation is less than the value in this field.</span></span> <span data-ttu-id="5aa7a-179">После создания проводки списания сумма, равная стоимости остатков после списания, может быть разнесена на склад или на счет главной книги.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-179">After a writing-off transaction is created, an amount equal to the cost of remainders after writing off can be posted to the inventory or the general ledger account.</span></span>

- <span data-ttu-id="5aa7a-180">**Не блокировать** — установите для этого параметра значение **Да**, чтобы создать проводки амортизации для актива.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-180">**Don't lock** – Set this option to **Yes** to create depreciation transactions for the asset.</span></span> <span data-ttu-id="5aa7a-181">По умолчанию этот параметр имеет значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-181">By default, this option is set to **Yes**.</span></span>

- <span data-ttu-id="5aa7a-182">**Дата последней амортизации, Дата выбытия** и **Стоимость выбытия** — заполняется автоматически при создании проводок амортизации и списания.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-182">**Date of last depreciation, Disposal date** and **Disposal cost** – Filled in automatically when depreciation and writing-off transactions are created.</span></span>

3. <span data-ttu-id="5aa7a-183">Выберите экспресс-вкладку **Аналитика**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-183">Select the **Dimension** FastTab.</span></span> <span data-ttu-id="5aa7a-184">Выберите коды финансовой аналитики по умолчанию, которые будут регистрировать проводки для актива.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-184">Select the default finance dimension codes that will register transactions for the asset.</span></span>

4. <span data-ttu-id="5aa7a-185">Выберите экспресс-вкладку **Аренда** и заполните поле **Профиль разноски**, выберите профиль разноски, который используется для сдачи основных средств в аренду.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-185">Select the **Lease** FastTab and fill in the **Posting profile** field, select the posting profile used for fixed asset letting.</span></span> <span data-ttu-id="5aa7a-186">Если для основного средства следует создать проводку аренды, установите для параметра **Арендованное** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-186">If a letting transaction should be created for a fixed asset, set the **Leased** option to **Yes**.</span></span>

5. <span data-ttu-id="5aa7a-187">Выберите **Аналитика арендованного ОС**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-187">Select **Dimension of rented FA**.</span></span> <span data-ttu-id="5aa7a-188">Выберите коды аналитик, которые должны использоваться при учете для проводок с данным основным средством, когда оно сдается в аренду.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-188">Select the dimension codes that should be used when accounting for transactions of this fixed asset is let out.</span></span>

6. <span data-ttu-id="5aa7a-189">Выберите **Счета амортизации**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-189">Select **Depreciation accounts.**</span></span> <span data-ttu-id="5aa7a-190">На этой странице можно настроить сумму разноски амортизации ОС для счетов ГК в необходимых пропорциях по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-190">On this page you can configure the fixed asset depreciation posting amount for the general ledger accounts in the proportions required, as needed.</span></span> <span data-ttu-id="5aa7a-191">Это может потребоваться, например, чтобы вычислить амортизацию для здания, используемого для различных целей.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-191">You might need to do this, for example, to calculate the depreciation on a building used for various purposes.</span></span>

## <a name="inquiries-on-the-fixed-asset-page"></a><span data-ttu-id="5aa7a-192">Запросы на странице основных средств</span><span class="sxs-lookup"><span data-stu-id="5aa7a-192">Inquiries on the Fixed asset page</span></span>

### <a name="view-asset-transactions"></a><span data-ttu-id="5aa7a-193">Просмотр проводок активов</span><span class="sxs-lookup"><span data-stu-id="5aa7a-193">View asset transactions</span></span>

<span data-ttu-id="5aa7a-194">Выполните следующие действия, чтобы просмотреть проводки с основными средствами.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-194">Follow these steps to view the fixed asset transactions.</span></span>

1. <span data-ttu-id="5aa7a-195">Выберите **Основные средства (Россия) \> Основные средства \> Модели стоимости \> Проводки**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-195">Select **Fixed Assets (Russia) \> Fixed Assets \> Value models \> Transactions.**</span></span>

2. <span data-ttu-id="5aa7a-196">Все проводки с основными средствами, выполненные для модели стоимости, перечисляются на странице **Проводки ОС**, независимо от того, в каком модуле они были разнесены:</span><span class="sxs-lookup"><span data-stu-id="5aa7a-196">All fixed asset transactions, executed for the value model, are listed on the **FA transactions** page, regardless of which module they were posted in:</span></span>

- <span data-ttu-id="5aa7a-197">Модуль **Основные средства (Россия)**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-197">**Fixed asset (Russia)** module.</span></span>
- <span data-ttu-id="5aa7a-198">Модуль **Главная книга**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-198">**General ledger** module.</span></span>
- <span data-ttu-id="5aa7a-199">Модуль **Расчеты с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-199">**Account payable** module.</span></span>
- <span data-ttu-id="5aa7a-200">Модуль **Расчеты с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-200">**Account receivable** module.</span></span>

3.  <span data-ttu-id="5aa7a-201">На вкладках **Обзор** и **Общие** отображаются подробные сведения о проводках с основными средствами.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-201">On the **Overview** and **General** tabs, the fixed asset transaction details are displayed.</span></span>

### <a name="view-the-balance-of-an-asset"></a><span data-ttu-id="5aa7a-202">Просмотр баланса основного средства</span><span class="sxs-lookup"><span data-stu-id="5aa7a-202">View the balance of an asset</span></span>

<span data-ttu-id="5aa7a-203">Стоимость актива на конкретную дату отражает результаты всех проводок для актива.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-203">The value of an asset on a specific date reflects the results of all transactions for the asset.</span></span> <span data-ttu-id="5aa7a-204">Выполните следующие действия, чтобы просмотреть сальдо актива.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-204">Follow these steps to view the balance of an asset.</span></span>

1. <span data-ttu-id="5aa7a-205">Выберите **Основные средства (Россия)\> Общее \> Основные средства \> Модели стоимости**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-205">Select **Fixed Assets (Russia)\> Common \> Fixed Assets \> Value models**.</span></span>

2. <span data-ttu-id="5aa7a-206">Выберите модель учета, для которой необходимо просмотреть баланс.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-206">Select the value model to view the balance for.</span></span>

3. <span data-ttu-id="5aa7a-207">Выберите кнопку **Сальдо**.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-207">Select the **Balance** button.</span></span>

4. <span data-ttu-id="5aa7a-208">В поле **Дата проводки** ведите дату для баланса.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-208">In the **Transaction date** field, enter the date for the balance sheet.</span></span> <span data-ttu-id="5aa7a-209">По умолчанию используется текущая дата.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-209">The default date is the current date.</span></span>

5. <span data-ttu-id="5aa7a-210">Суммы на странице основных средств **Баланс по ОС** отображаются в валюте модели учета основных средств.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-210">The amounts on the fixed asset **Balance by FA** page are displayed in the currency of the fixed asset value model.</span></span> <span data-ttu-id="5aa7a-211">Если валюта модели учета отличается от валюты компании по умолчанию, валюта по умолчанию также отображается.</span><span class="sxs-lookup"><span data-stu-id="5aa7a-211">If the value model currency is different from the company's default currency, the default currency is also displayed.</span></span>

![Сальдо модели стоимости ОС](media/RUS_FA_4%20model%20balance.JPG)
