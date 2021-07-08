---
title: Создание заранее определенных вариантов продукта
description: В этой процедуре показано, как создать варианты продукта для шаблона продукта с использованием комбинаций аналитик продукта.
author: t-benebo
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 442a5f5b321833c170cfecc4069e62a1254605cd
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270488"
---
# <a name="predefined-product-variants"></a><span data-ttu-id="97472-103">Заранее определенные варианты продукта</span><span class="sxs-lookup"><span data-stu-id="97472-103">Predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a><span data-ttu-id="97472-104">Пример сценария: создание предопределенных вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="97472-104">Example scenario: Create predefined product variants</span></span>

<span data-ttu-id="97472-105">В этом примере сценария показано, как создать варианты продукта для шаблона продукта с использованием комбинаций аналитик продукта.</span><span class="sxs-lookup"><span data-stu-id="97472-105">This example scenario shows how to create product variants for a product master using a combinations of product dimensions.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="97472-106">Сделать демонстрационные данные доступными</span><span class="sxs-lookup"><span data-stu-id="97472-106">Make demo data available</span></span>

<span data-ttu-id="97472-107">Для выполнения этого сценария с помощью предложенных здесь значений необходимо установить демонстрационные данные, а также необходимо выбрать юридическое лицо *USMF*.</span><span class="sxs-lookup"><span data-stu-id="97472-107">To follow this scenario using the values suggested here, you must have demo data installed, and you must select the *USMF* legal entity.</span></span>

### <a name="step-1-create-a-product-master"></a><span data-ttu-id="97472-108">Шаг 1. Создание шаблона продукта</span><span class="sxs-lookup"><span data-stu-id="97472-108">Step 1: Create a product master</span></span>

<span data-ttu-id="97472-109">Создание шаблона продукта:</span><span class="sxs-lookup"><span data-stu-id="97472-109">To create a product master:</span></span>

1. <span data-ttu-id="97472-110">Перейдите в раздел **Управление сведениями о продукте > Продукты > Шаблоны продукта**.</span><span class="sxs-lookup"><span data-stu-id="97472-110">Go to **Product information management > Products > Product masters**.</span></span>
1. <span data-ttu-id="97472-111">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="97472-111">Select **New**.</span></span>
1. <span data-ttu-id="97472-112">Если поле **Номер продукта** еще не отображает номер, введите значение.</span><span class="sxs-lookup"><span data-stu-id="97472-112">If the **Product number** field doesn't already show a number, then enter a value.</span></span> <span data-ttu-id="97472-113">Это необходимо, только если для этого поля не была настроена номерная серия.</span><span class="sxs-lookup"><span data-stu-id="97472-113">This is only required if no number sequence has been set for this field.</span></span>
1. <span data-ttu-id="97472-114">В поле **Название продукта** введите название.</span><span class="sxs-lookup"><span data-stu-id="97472-114">Enter a name in the **Product name** field.</span></span>
1. <span data-ttu-id="97472-115">В поле **Группа аналитик продуктов** выберите группу аналитик продуктов *SizeCol* (размер и цвет).</span><span class="sxs-lookup"><span data-stu-id="97472-115">In the **Product dimension group** field, select the product dimension group *SizeCol* (Size and Color).</span></span>
1. <span data-ttu-id="97472-116">Нажмите **ОК**, чтобы создать и открыть новый шаблон продукта.</span><span class="sxs-lookup"><span data-stu-id="97472-116">Select **OK** to create and open the new product master.</span></span>

### <a name="step-2-add-product-dimensions"></a><span data-ttu-id="97472-117">Шаг 2. Добавление аналитик продукта</span><span class="sxs-lookup"><span data-stu-id="97472-117">Step 2: Add product dimensions</span></span>

<span data-ttu-id="97472-118">В этом примере показано, как ввести аналитики продукта вручную.</span><span class="sxs-lookup"><span data-stu-id="97472-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="97472-119">Можно также выбрать размер, цвет или группу стилей, включающую значения аналитик продукта, которые необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="97472-119">You can also choose to select a size, color, or style group that includes the product dimension values you want to use.</span></span>

<span data-ttu-id="97472-120">Добавление аналитик продукта:</span><span class="sxs-lookup"><span data-stu-id="97472-120">To add product dimensions:</span></span>

1. <span data-ttu-id="97472-121">При открытом новом шаблоне продукта выберите **Аналитики продукта** в области действий.</span><span class="sxs-lookup"><span data-stu-id="97472-121">With your new product master still open, select **Product dimensions** on the Action Pane.</span></span>
1. <span data-ttu-id="97472-122">Откройте вкладку **Размер** и выберите **Создать** на панели инструментов, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="97472-122">Open the **Size** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="97472-123">Выполните следующие настройки для новой строки:</span><span class="sxs-lookup"><span data-stu-id="97472-123">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="97472-124">**Размер:** выберите значение размера.</span><span class="sxs-lookup"><span data-stu-id="97472-124">**Size:** Select a size value.</span></span>
    - <span data-ttu-id="97472-125">**Имя:** введите имя для размера.</span><span class="sxs-lookup"><span data-stu-id="97472-125">**Name:** Enter a name for the size.</span></span>
1. <span data-ttu-id="97472-126">Выберите **Создать** на панели инструментов и добавьте второй размер в сетку с новым **Размер** и **Имя**.</span><span class="sxs-lookup"><span data-stu-id="97472-126">Select **New** on the toolbar and add a second size to the grid with a new **Size** and **Name**.</span></span>
1. <span data-ttu-id="97472-127">Откройте вкладку **Цвета** и выберите **Создать** на панели инструментов, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="97472-127">Open the **Colors** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="97472-128">Выполните следующие настройки для новой строки:</span><span class="sxs-lookup"><span data-stu-id="97472-128">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="97472-129">**Цвет:** выберите значение цвета.</span><span class="sxs-lookup"><span data-stu-id="97472-129">**Color:** Select a color value.</span></span>
    - <span data-ttu-id="97472-130">**Имя:** введите имя для цвета.</span><span class="sxs-lookup"><span data-stu-id="97472-130">**Name:** Enter a name for the color.</span></span>
1. <span data-ttu-id="97472-131">Выберите **Создать** на панели инструментов и добавьте второй цвет в сетку с новым **Цвет** и **Имя**.</span><span class="sxs-lookup"><span data-stu-id="97472-131">Select **New** on the toolbar and add a second color to the grid with a new **Color** and **Name**.</span></span>
1. <span data-ttu-id="97472-132">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="97472-132">Select **Save**.</span></span>
1. <span data-ttu-id="97472-133">Закройте страницу, чтобы вернуться в новый шаблон продукта.</span><span class="sxs-lookup"><span data-stu-id="97472-133">Close the page to return to your new product master.</span></span>

### <a name="step-3-generate-product-variants"></a><span data-ttu-id="97472-134">Шаг 3. Создание вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="97472-134">Step 3: Generate product variants</span></span>

> [!NOTE]
> <span data-ttu-id="97472-135">В этом разделе описывается создание вариантов продукта, когда функция *Улучшения страницы предложений вариантов* не активирована.</span><span class="sxs-lookup"><span data-stu-id="97472-135">This section describes how to generate product variants when the *Variant suggestions page improvements* feature isn't enabled.</span></span> <span data-ttu-id="97472-136">В следующем разделе приводятся сведения о создании вариантов продукта, когда эта функция доступна.</span><span class="sxs-lookup"><span data-stu-id="97472-136">See the next section for details about how to generate product variants when that feature is available.</span></span>

<span data-ttu-id="97472-137">Создание вариантов продукта:</span><span class="sxs-lookup"><span data-stu-id="97472-137">To generate product variants:</span></span>

1. <span data-ttu-id="97472-138">При открытом новом шаблоне продукта выберите **Варианты продукта** в области действий.</span><span class="sxs-lookup"><span data-stu-id="97472-138">With your new product master still open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="97472-139">Выберите **Предложения варианта** в области действий.</span><span class="sxs-lookup"><span data-stu-id="97472-139">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="97472-140">Система создает список со всеми возможными комбинациями размеров и цветов, определенных для продукта.</span><span class="sxs-lookup"><span data-stu-id="97472-140">The system generates a list with all possible combinations of the sizes and colors you defined for the product.</span></span> <span data-ttu-id="97472-141">Выберите **Выбрать все** на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="97472-141">Select **Select all** on the toolbar.</span></span>
    - <span data-ttu-id="97472-142">В этом примере выбраны все возможные варианты.</span><span class="sxs-lookup"><span data-stu-id="97472-142">In this example, select all of the possible variants.</span></span> <span data-ttu-id="97472-143">Если требуется использовать только подмножество возможных комбинаций аналитик продукта, установите флажки только для тех полей, которые необходимы.</span><span class="sxs-lookup"><span data-stu-id="97472-143">If you only want to use a subset of the possible product dimension combinations, select only the required check boxes as needed.</span></span>  
1. <span data-ttu-id="97472-144">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="97472-144">Select **Create**.</span></span>
1. <span data-ttu-id="97472-145">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="97472-145">Select **Save**.</span></span>

## <a name="improved-variant-suggestions"></a><span data-ttu-id="97472-146">Улучшенные предложения вариантов</span><span class="sxs-lookup"><span data-stu-id="97472-146">Improved variant suggestions</span></span>

<span data-ttu-id="97472-147">Функция *Усовершенствования страницы предложения вариантов* позволяет улучшить страницу **Предложения вариантов**, чтобы решить проблемы с производительностью и удобством использования для компаний с большим количеством комбинаций аналитик продукта.</span><span class="sxs-lookup"><span data-stu-id="97472-147">The *Variant suggestions page improvements* feature improves the **Variant suggestions** page to address performance and usability issues for companies that have a high number of product dimension combinations.</span></span> <span data-ttu-id="97472-148">Усовершенствованный процесс выбора значений аналитики продукта, для которых создается предложение вариантов, значительно ускоряет и упрощает определение и выпуск соответствующего набора вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="97472-148">The enhanced process for selecting the product dimension values for which to generate variant suggestions makes it faster and easier to identify and release the relevant set of product variants.</span></span>

<span data-ttu-id="97472-149">Эта функция добавляет следующие усовершенствования:</span><span class="sxs-lookup"><span data-stu-id="97472-149">The following improvements are added by this feature:</span></span>

- <span data-ttu-id="97472-150">**Отложенное создание предложений вариантов**: страница **Предложения вариантов** больше не отображает предложения при первом открытии.</span><span class="sxs-lookup"><span data-stu-id="97472-150">**Deferred generation of variant suggestions:** The **Variant suggestions** page no longer shows suggestions when you first open it.</span></span> <span data-ttu-id="97472-151">Вместо этого необходимо явно выбрать нужные значения, а затем нажать кнопку **Предложить** для создания комбинаций.</span><span class="sxs-lookup"><span data-stu-id="97472-151">Instead, you must explicitly choose which values you will need and then select the **Suggest** button to generate the combinations.</span></span> <span data-ttu-id="97472-152">Это делает процесс более видимым и интерактивным.</span><span class="sxs-lookup"><span data-stu-id="97472-152">This makes the process more visible and interactive.</span></span>
- <span data-ttu-id="97472-153">**Выбор значений аналитик:** при наличии большого количества значений аналитик обычно необходимо создать предложения вариантов, включающие только некоторые из них (например, при внедрении нового набора цветов или стилей).</span><span class="sxs-lookup"><span data-stu-id="97472-153">**Selection of dimensions values:** When you have many dimension values, you are typically interested in generating variant suggestions that include just a few of them (such as when introducing a new set of colors or styles).</span></span> <span data-ttu-id="97472-154">Улучшенная структура позволяет выбрать значения аналитик, для которых требуется создать предложения вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="97472-154">With the improved design, you can select the dimension values for which you want to generate product variant suggestions.</span></span> <span data-ttu-id="97472-155">Это значительно увеличивает соответствие предлагаемых вариантов и повышает производительность и системы, и пользователя.</span><span class="sxs-lookup"><span data-stu-id="97472-155">This greatly increases the relevance of the suggested variants and improves both system performance and user productivity.</span></span>

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a><span data-ttu-id="97472-156">Включение функции улучшений страницы предложений вариантов</span><span class="sxs-lookup"><span data-stu-id="97472-156">Turn on the Variant suggestions page improvements feature</span></span>

<span data-ttu-id="97472-157">Прежде чем использовать функцию *Улучшения страницы предложений вариантов*, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="97472-157">Before you can use *Variant suggestions page improvements* feature, it must be turned on in your system.</span></span> <span data-ttu-id="97472-158">Администраторы могут использовать параметры [управления компонентами](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения.</span><span class="sxs-lookup"><span data-stu-id="97472-158">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="97472-159">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="97472-159">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="97472-160">**Модуль:** *Управление сведениями о продукте*</span><span class="sxs-lookup"><span data-stu-id="97472-160">**Module:** *Product information management*</span></span>
- <span data-ttu-id="97472-161">**Название функции:** *улучшения страницы предложений вариантов*</span><span class="sxs-lookup"><span data-stu-id="97472-161">**Feature name:** *Variant suggestions page improvements*</span></span>

### <a name="work-with-the-improved-variant-suggestions"></a><span data-ttu-id="97472-162">Работа с усовершенствованными предложениями вариантов</span><span class="sxs-lookup"><span data-stu-id="97472-162">Work with the improved variant suggestions</span></span>

<span data-ttu-id="97472-163">Для создания предложений вариантов продукта, когда функция *Улучшения страницы предложений вариантов* включена:</span><span class="sxs-lookup"><span data-stu-id="97472-163">To generate product variant suggestions when the *Variant suggestions page improvements* feature is enabled:</span></span>

1. <span data-ttu-id="97472-164">Откройте или создайте шаблон продукта и добавьте в него необходимые аналитики продукта, как это описано в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="97472-164">Open or create a product master and add the required product dimensions to it, as described in the previous section.</span></span>
1. <span data-ttu-id="97472-165">При открытом шаблоне продукта выберите **Варианты продукта** в области действий.</span><span class="sxs-lookup"><span data-stu-id="97472-165">With the product master open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="97472-166">Выберите **Предложения варианта** в области действий.</span><span class="sxs-lookup"><span data-stu-id="97472-166">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="97472-167">Выберите значения, которые необходимо использовать для каждой аналитики.</span><span class="sxs-lookup"><span data-stu-id="97472-167">Select the values that you want to use for each of the dimensions.</span></span>
1. <span data-ttu-id="97472-168">На верхней панели инструментов выберите **Предложить**.</span><span class="sxs-lookup"><span data-stu-id="97472-168">On the top toolbar, select **Suggest**.</span></span>
1. <span data-ttu-id="97472-169">Система создает список со всеми возможными комбинациями выбранных размеров и цветов.</span><span class="sxs-lookup"><span data-stu-id="97472-169">The system generates a list with all possible combinations of the sizes and colors you selected.</span></span> <span data-ttu-id="97472-170">На экспресс-вкладке **Предлагаемые варианты** установите флажок для каждой комбинации аналитики продукта, которую необходимо использовать, или выберите **Выбрать все** на панели инструментов, чтобы выбрать все из них.</span><span class="sxs-lookup"><span data-stu-id="97472-170">On the **Suggested variants** FastTab, select the check box for each product dimension combination that you want to use, or select **Select all** on the toolbar to select all of them.</span></span>  
1. <span data-ttu-id="97472-171">Выберите **Создать**, чтобы добавить варианты в текущий шаблон продукта.</span><span class="sxs-lookup"><span data-stu-id="97472-171">Select **Create** to add the variants to the current product master.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
