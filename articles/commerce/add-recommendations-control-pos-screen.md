---
title: Добавление рекомендаций на экран проводки
description: В этом разделе описывается, как добавить элемент управления рекомендациями на экране проводки устройства POS, используя конструктор макета экрана в Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 760e6e093dbe0ba6b2781f90af7fbb614c492b93
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454587"
---
# <a name="add-recommendations-to-the-transaction-screen"></a><span data-ttu-id="e5fa5-103">Добавление рекомендаций на экран проводки</span><span class="sxs-lookup"><span data-stu-id="e5fa5-103">Add recommendations to the transaction screen</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="e5fa5-104">В этом разделе описывается, как добавить элемент управления рекомендациями на экране проводки устройства POS, используя конструктор макета экрана в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="e5fa5-105">Дополнительные сведения о рекомендациях продуктов см. в разделе [Документация по рекомендациям продуктов в POS-терминалах](product.md).</span><span class="sxs-lookup"><span data-stu-id="e5fa5-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="e5fa5-106">При использовании Commerce можно отображать рекомендации по продукту на устройстве POS.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-106">You can display product recommendations on your POS device when you use Commerce.</span></span> <span data-ttu-id="e5fa5-107">Чтобы отобразить рекомендации по продуктам необходимо добавить элемент управления на экран проводки, используя конструктор макета экрана.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="e5fa5-108">Откройте конструктор макета</span><span class="sxs-lookup"><span data-stu-id="e5fa5-108">Open Layout designer</span></span>

1. <span data-ttu-id="e5fa5-109">Перейдите в раздел **Retail и Commerce** &gt; **Настройка канала** &gt; **Настройка POS** &gt; **POS** &gt; **Макеты экрана**.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-109">Go to **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="e5fa5-110">Используйте экспресс-фильтр для поиска экрана, на который требуется добавить элемент управления.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="e5fa5-111">Например, выполните фильтрацию по полю **Код макета экрана**, используя значение **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="e5fa5-112">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="e5fa5-113">Например, выберите **Имя: F2CP16:9M Код макета экрана: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="e5fa5-114">Нажмите **Конструктор макета**.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="e5fa5-115">Следуйте инструкциям на экране для запуска конструктора макета.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="e5fa5-116">В ответ на запрос учетных данных следует ввести те же учетные данные, которые были использованы при запуске конструктора макета со страницы **Макеты экрана**.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="e5fa5-117">После входа отображается страница, аналогичная приведенной ниже.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="e5fa5-118">Макет будет отличаться в зависимости от настроек, которые были сделаны в хранилище.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="e5fa5-119">[![Конструктор макета](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="e5fa5-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="e5fa5-120">Выберите параметр отображения</span><span class="sxs-lookup"><span data-stu-id="e5fa5-120">Choose a display option</span></span>

<span data-ttu-id="e5fa5-121">Доступны два варианта конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-121">There are two configurations options available.</span></span> <span data-ttu-id="e5fa5-122">Выберите вариант, который лучше всего подходит для вашего хранилища, и следуйте оставшимся инструкциям, чтобы завершить настройку элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="e5fa5-123">Имеется две возможности:</span><span class="sxs-lookup"><span data-stu-id="e5fa5-123">The two options are:</span></span>

- <span data-ttu-id="e5fa5-124">Рекомендации отображаются всегда.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="e5fa5-125">Вкладка **Рекомендации** отображается в сетке в правой части экрана.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="e5fa5-126">Задайте, чтобы рекомендации отображались всегда</span><span class="sxs-lookup"><span data-stu-id="e5fa5-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="e5fa5-127">Уменьшите высоту области подробных сведений о строках проводки, чтобы ее высота была равна высоте панели клиента слева.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="e5fa5-128">[![Высота области сведений строк проводок уменьшена](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="e5fa5-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="e5fa5-129">Из левого меню перетащите элемент управления рекомендаций в зону между областью сведений строки проводки и сеткой кнопок в нижней центральной части экрана проводок.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="e5fa5-130">Измените размер элемента управления, чтобы он помещался в этой области.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="e5fa5-131">[![Элемент управления рекомендаций добавлен к макету](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="e5fa5-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="e5fa5-132">Нажмите кнопку **X**, чтобы сохранить конструктор макетов и выйти из него.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="e5fa5-133">В Commerce перейдите в раздел **Retail и Commerce** &gt; **ИТ Retail и Commerce** &gt; **График распределения**.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-133">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="e5fa5-134">В списке выберите **1090, Регистры**.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="e5fa5-135">Щелкните **Запустить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="e5fa5-136">Добавление вкладки "Рекомендации" в сетку кнопок в правой части экрана</span><span class="sxs-lookup"><span data-stu-id="e5fa5-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="e5fa5-137">Щелкните правой кнопкой мыши пустое пространство под последней вкладкой в сетке кнопок, находящейся в правой части страницы.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="e5fa5-138">Щелкните **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-138">Click **Customize**.</span></span>

    <span data-ttu-id="e5fa5-139">[![Диалоговое окно "Настройка" — элемент управления вкладки](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="e5fa5-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="e5fa5-140">Нажмите **Создать вкладку**.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-140">Click **New tab**.</span></span>
4. <span data-ttu-id="e5fa5-141">Найдите новую вкладку, которая была добавлена.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-141">Find the new tab that you just added.</span></span> <span data-ttu-id="e5fa5-142">Может потребоваться выполнить прокрутку вниз.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="e5fa5-143">В раскрывающемся списке **Содержание** выберите **Рекомендуемые продукты**.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="e5fa5-144">[![Выбор рекомендуемых продуктов в поле содержания](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="e5fa5-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="e5fa5-145">В **Метка** введите имя для вкладки рекомендаций. Например, введите "Рекомендуемые продукты".</span><span class="sxs-lookup"><span data-stu-id="e5fa5-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="e5fa5-146">В поле **Изображение** выберите изображение, которое должно появляться на вкладке.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="e5fa5-147">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-147">Click **OK**.</span></span> <span data-ttu-id="e5fa5-148">Новая вкладка отображается в сетке кнопок.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="e5fa5-149">Нажмите кнопку **X**, чтобы сохранить конструктор макетов и выйти из него.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="e5fa5-150">В Commerce перейдите в раздел **Retail и Commerce** &gt; **ИТ Retail и Commerce** &gt; **График распределения**.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-150">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="e5fa5-151">В списке выберите **1090, Регистры**.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="e5fa5-152">Щелкните **Запустить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="e5fa5-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e5fa5-153">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e5fa5-153">Additional resources</span></span>

[<span data-ttu-id="e5fa5-154">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="e5fa5-154">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="e5fa5-155">Включение Azure Data Lake Storage в среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e5fa5-155">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="e5fa5-156">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="e5fa5-156">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="e5fa5-157">Включение персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="e5fa5-157">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="e5fa5-158">Отказ от персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="e5fa5-158">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="e5fa5-159">Добавление рекомендаций по продуктам в POS</span><span class="sxs-lookup"><span data-stu-id="e5fa5-159">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="e5fa5-160">Корректировка результатов рекомендаций на основе искусственного интеллекта и машинного обучения</span><span class="sxs-lookup"><span data-stu-id="e5fa5-160">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="e5fa5-161">Создание контролируемых рекомендаций вручную</span><span class="sxs-lookup"><span data-stu-id="e5fa5-161">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="e5fa5-162">Создание рекомендаций с помощью демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="e5fa5-162">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="e5fa5-163">Вопросы и ответы по рекомендациям по продуктам</span><span class="sxs-lookup"><span data-stu-id="e5fa5-163">Product recommendations FAQ</span></span>](faq-recommendations.md)
