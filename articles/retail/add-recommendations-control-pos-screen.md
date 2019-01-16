---
title: "Добавление элемента управления рекомендациями на экране проводки на устройствах POS"
description: "В этом разделе описывается, как добавить элемент управления рекомендациями на экране проводки устройства POS, используя конструктор макета экрана в Microsoft Dynamics 365 for Retail."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 213b47422a5e31c2cfc2d173b8c7d9efdecc7568
ms.contentlocale: ru-ru
ms.lasthandoff: 01/04/2019

---

# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="c7e81-103">Добавление элемента управления рекомендациями на экране проводки на устройствах POS</span><span class="sxs-lookup"><span data-stu-id="c7e81-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="c7e81-104">Мы удаляем текущую версию службы рекомендации продуктов, так как мы переработали эту функцию с использованием более эффективного алгоритма и новыми возможностями, предназначенными для розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="c7e81-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="c7e81-105">Подробнее см. в разделе [Удаленные или устаревшие функции](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span><span class="sxs-lookup"><span data-stu-id="c7e81-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span>

<span data-ttu-id="c7e81-106">В этом разделе описывается, как добавить элемент управления рекомендациями на экране проводки устройства POS, используя конструктор макета экрана в Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="c7e81-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="c7e81-107">При использовании Microsoft Dynamics 365 for Retail можно отображать рекомендации по продукту на устройстве POS.</span><span class="sxs-lookup"><span data-stu-id="c7e81-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="c7e81-108">*Рекомендации* представляют собой номенклатуры, в которых ваш клиент может быть заинтересован на основе его истории покупок, номенклатур в списке планируемых покупок и номенклатур, приобретенных другими клиентами в Интернете и в физических магазинах.</span><span class="sxs-lookup"><span data-stu-id="c7e81-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="c7e81-109">Чтобы отобразить рекомендации по продуктам необходимо добавить элемент управления на экран проводки, используя конструктор макета экрана.</span><span class="sxs-lookup"><span data-stu-id="c7e81-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="c7e81-110">Откройте конструктор макета</span><span class="sxs-lookup"><span data-stu-id="c7e81-110">Open Layout designer</span></span>

1. <span data-ttu-id="c7e81-111">Перейдите в раздел **Розничная торговля** &gt; **Настройка канала** &gt; **Настройка POS** &gt; **POS** &gt; **Макеты экрана**.</span><span class="sxs-lookup"><span data-stu-id="c7e81-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="c7e81-112">Используйте экспресс-фильтр для поиска экрана, на который требуется добавить элемент управления.</span><span class="sxs-lookup"><span data-stu-id="c7e81-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="c7e81-113">Например, выполните фильтрацию по полю **Код макета экрана**, используя значение "F2CP16:9M".</span><span class="sxs-lookup"><span data-stu-id="c7e81-113">For example, filter on the **Screen layout ID** field using a value of 'F2CP16:9M'.</span></span>
3. <span data-ttu-id="c7e81-114">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c7e81-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="c7e81-115">Например, выберите "Имя: F2CP16:9M Код макета экрана: F2CP16:9M".</span><span class="sxs-lookup"><span data-stu-id="c7e81-115">For example, select 'Name: F2CP16:9M Screen Layout ID: F2CP16:9M'.</span></span>
4. <span data-ttu-id="c7e81-116">Нажмите **Конструктор макета**.</span><span class="sxs-lookup"><span data-stu-id="c7e81-116">Click **Layout designer**.</span></span>
5. <span data-ttu-id="c7e81-117">Следуйте инструкциям на экране для запуска конструктора макета.</span><span class="sxs-lookup"><span data-stu-id="c7e81-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="c7e81-118">В ответ на запрос учетных данных следует ввести те же учетные данные, которые были использованы при запуске конструктора макета со страницы **Макеты экрана**.</span><span class="sxs-lookup"><span data-stu-id="c7e81-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="c7e81-119">После входа отображается страница, аналогичная приведенной ниже.</span><span class="sxs-lookup"><span data-stu-id="c7e81-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="c7e81-120">Макет будет отличаться в зависимости от настроек, которые были сделаны в хранилище.</span><span class="sxs-lookup"><span data-stu-id="c7e81-120">The layout will be different depending on the customizations that were made for your store.</span></span>

    <span data-ttu-id="c7e81-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="c7e81-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="c7e81-122">Выберите параметр отображения</span><span class="sxs-lookup"><span data-stu-id="c7e81-122">Choose a display option</span></span>

<span data-ttu-id="c7e81-123">Доступны два варианта конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c7e81-123">There are two configurations options available.</span></span> <span data-ttu-id="c7e81-124">Выберите вариант, который лучше всего подходит для вашего хранилища, и следуйте оставшимся инструкциям, чтобы завершить настройку элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c7e81-124">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="c7e81-125">Имеется две возможности:</span><span class="sxs-lookup"><span data-stu-id="c7e81-125">The two options are:</span></span>

- <span data-ttu-id="c7e81-126">Рекомендации отображаются всегда.</span><span class="sxs-lookup"><span data-stu-id="c7e81-126">Recommendations are always visible.</span></span>
- <span data-ttu-id="c7e81-127">Вкладка **Рекомендации** отображается в сетке в правой части экрана.</span><span class="sxs-lookup"><span data-stu-id="c7e81-127">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="c7e81-128">Задайте, чтобы рекомендации отображались всегда</span><span class="sxs-lookup"><span data-stu-id="c7e81-128">Make recommendations always visible</span></span>

1. <span data-ttu-id="c7e81-129">Уменьшите высоту области подробных сведений о строках проводки, чтобы ее высота была равна высоте панели клиента слева.</span><span class="sxs-lookup"><span data-stu-id="c7e81-129">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>

    <span data-ttu-id="c7e81-130">[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="c7e81-130">[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="c7e81-131">Из левого меню перетащите элемент управления рекомендаций в зону между областью сведений строки проводки и сеткой кнопок в нижней центральной части экрана проводок.</span><span class="sxs-lookup"><span data-stu-id="c7e81-131">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="c7e81-132">Измените размер элемента управления, чтобы он помещался в этой области.</span><span class="sxs-lookup"><span data-stu-id="c7e81-132">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="c7e81-133">[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="c7e81-133">[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>

3. <span data-ttu-id="c7e81-134">Нажмите кнопку **X**, чтобы сохранить конструктор макетов и выйти из него.</span><span class="sxs-lookup"><span data-stu-id="c7e81-134">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="c7e81-135">В Dynamics 365 for Retail перейдите в раздел **Розничная торговля** &gt; **ИТ розничной торговли** &gt; **График распределения**.</span><span class="sxs-lookup"><span data-stu-id="c7e81-135">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="c7e81-136">В списке выберите  **1090, Регистры**.</span><span class="sxs-lookup"><span data-stu-id="c7e81-136">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="c7e81-137">Щелкните **Запустить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="c7e81-137">Click **Run now**.</span></span>

### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="c7e81-138">Добавление вкладки "Рекомендации" в сетку кнопок в правой части экрана</span><span class="sxs-lookup"><span data-stu-id="c7e81-138">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="c7e81-139">Щелкните правой кнопкой мыши пустое пространство под последней вкладкой в сетке кнопок, находящейся в правой части страницы.</span><span class="sxs-lookup"><span data-stu-id="c7e81-139">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2. <span data-ttu-id="c7e81-140">Щелкните  **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="c7e81-140">Click **Customize**.</span></span>

    <span data-ttu-id="c7e81-141">[![Рис.-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="c7e81-141">[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="c7e81-142">Нажмите **Создать вкладку**.</span><span class="sxs-lookup"><span data-stu-id="c7e81-142">Click **New tab**.</span></span>
4. <span data-ttu-id="c7e81-143">Найдите новую вкладку, которая была добавлена.</span><span class="sxs-lookup"><span data-stu-id="c7e81-143">Find the new tab that you just added.</span></span> <span data-ttu-id="c7e81-144">Может потребоваться выполнить прокрутку вниз.</span><span class="sxs-lookup"><span data-stu-id="c7e81-144">You may need to scroll down.</span></span>
5. <span data-ttu-id="c7e81-145">В раскрывающемся списке **Содержание** выберите **Рекомендуемые продукты**.</span><span class="sxs-lookup"><span data-stu-id="c7e81-145">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="c7e81-146">[![Рис.-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="c7e81-146">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="c7e81-147">В **Метка** введите имя для вкладки рекомендаций. Например, введите "Рекомендуемые продукты".</span><span class="sxs-lookup"><span data-stu-id="c7e81-147">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="c7e81-148">В поле **Изображение** выберите изображение, которое должно появляться на вкладке.</span><span class="sxs-lookup"><span data-stu-id="c7e81-148">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="c7e81-149">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7e81-149">Click **OK**.</span></span> <span data-ttu-id="c7e81-150">Новая вкладка отображается в сетке кнопок.</span><span class="sxs-lookup"><span data-stu-id="c7e81-150">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="c7e81-151">Нажмите кнопку **X**, чтобы сохранить конструктор макетов и выйти из него.</span><span class="sxs-lookup"><span data-stu-id="c7e81-151">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="c7e81-152">В Dynamics 365 for Retail перейдите в раздел **Розничная торговля** &gt; **ИТ розничной торговли** &gt; **График распределения**.</span><span class="sxs-lookup"><span data-stu-id="c7e81-152">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="c7e81-153">В списке выберите **1090, Регистры**.</span><span class="sxs-lookup"><span data-stu-id="c7e81-153">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="c7e81-154">Щелкните **Запустить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="c7e81-154">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c7e81-155">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c7e81-155">Additional resources</span></span>

[<span data-ttu-id="c7e81-156">Обзор персонализированных рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="c7e81-156">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)

