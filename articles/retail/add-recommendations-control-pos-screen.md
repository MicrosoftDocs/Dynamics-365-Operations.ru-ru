---
title: "Добавление элемента управления рекомендациями на странице проводки на устройстве POS"
description: "В этом разделе описывается, как добавить элемент управления рекомендациями на экране проводки устройства POS, используя конструктор макета экрана в Microsoft Dynamics 365 for Retail."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 47ad5dc8fd698f6f543c6a48e2c7eb01d4e148e6
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a><span data-ttu-id="314e3-103">Добавление элемента управления рекомендациями на странице проводки на устройстве POS</span><span class="sxs-lookup"><span data-stu-id="314e3-103">Add a recommendations control to the transaction page on a POS device</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="314e3-104">В этом разделе описывается, как добавить элемент управления рекомендациями на экране проводки устройства POS, используя конструктор макета экрана в Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="314e3-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="314e3-105">При использовании Microsoft Dynamics 365 for Retail можно отображать рекомендации по продукту на устройстве POS.</span><span class="sxs-lookup"><span data-stu-id="314e3-105">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="314e3-106">*Рекомендации* представляют собой номенклатуры, в которых ваш клиент может быть заинтересован на основе его истории покупок, номенклатур в списке планируемых покупок и номенклатур, приобретенных другими клиентами в Интернете и в физических магазинах.</span><span class="sxs-lookup"><span data-stu-id="314e3-106">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="314e3-107">Чтобы отобразить рекомендации по продуктам необходимо добавить элемент управления на экран проводки, используя конструктор макета экрана.</span><span class="sxs-lookup"><span data-stu-id="314e3-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="314e3-108">Откройте конструктор макета</span><span class="sxs-lookup"><span data-stu-id="314e3-108">Open Layout designer</span></span>
1.  <span data-ttu-id="314e3-109">Перейдите в раздел **Розничная торговля** &gt; **Настройка канала** &gt; **Настройка POS** &gt; **POS** &gt; **Макеты экрана**.</span><span class="sxs-lookup"><span data-stu-id="314e3-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="314e3-110">Используйте экспресс-фильтр для поиска экрана, на который требуется добавить элемент управления.</span><span class="sxs-lookup"><span data-stu-id="314e3-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="314e3-111">Например, выполните фильтрацию по полю **Код макета экрана**, используя значение "F2CP16:9M".</span><span class="sxs-lookup"><span data-stu-id="314e3-111">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="314e3-112">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="314e3-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="314e3-113">Например, выберите "Имя: F2CP16:9M Код макета экрана: F2CP16:9M".</span><span class="sxs-lookup"><span data-stu-id="314e3-113">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="314e3-114">Нажмите **Конструктор макета**.</span><span class="sxs-lookup"><span data-stu-id="314e3-114">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="314e3-115">Следуйте инструкциям на экране для запуска конструктора макета.</span><span class="sxs-lookup"><span data-stu-id="314e3-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="314e3-116">В ответ на запрос учетных данных следует ввести те же учетные данные, которые были использованы при запуске конструктора макета со страницы **Макеты экрана**.</span><span class="sxs-lookup"><span data-stu-id="314e3-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="314e3-117">После входа отображается страница, аналогичная приведенной ниже.</span><span class="sxs-lookup"><span data-stu-id="314e3-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="314e3-118">Макет будет отличаться в зависимости от настроек, которые были сделаны в хранилище.</span><span class="sxs-lookup"><span data-stu-id="314e3-118">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="314e3-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Выберите вариант отображения</span><span class="sxs-lookup"><span data-stu-id="314e3-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="314e3-120">Доступны два варианта конфигурации.</span><span class="sxs-lookup"><span data-stu-id="314e3-120">There are two configurations options available.</span></span> <span data-ttu-id="314e3-121">Выберите вариант, который лучше всего подходит для вашего хранилища, и следуйте оставшимся инструкциям, чтобы завершить настройку элемента управления.</span><span class="sxs-lookup"><span data-stu-id="314e3-121">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="314e3-122">Имеется две возможности:</span><span class="sxs-lookup"><span data-stu-id="314e3-122">The two options are:</span></span>
-   <span data-ttu-id="314e3-123">Рекомендации отображаются всегда.</span><span class="sxs-lookup"><span data-stu-id="314e3-123">Recommendations are always visible.</span></span>
-   <span data-ttu-id="314e3-124">Вкладка **Рекомендации** отображается в сетке в правой части экрана.</span><span class="sxs-lookup"><span data-stu-id="314e3-124">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="314e3-125">Чтобы рекомендации отображались всегда</span><span class="sxs-lookup"><span data-stu-id="314e3-125">To make recommendations always visible</span></span>

1.  <span data-ttu-id="314e3-126">Уменьшите высоту области подробных сведений о строках проводки, чтобы ее высота была равна высоте панели клиента слева.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="314e3-126">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="314e3-127">Из левого меню перетащите элемент управления рекомендаций в зону между областью сведений строки проводки и сеткой кнопок в нижней центральной части экрана проводок.</span><span class="sxs-lookup"><span data-stu-id="314e3-127">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="314e3-128">Измените размер элемента управления, чтобы он помещался в этой области.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="314e3-128">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="314e3-129">Нажмите кнопку **X**, чтобы сохранить конструктор макетов и выйти из него.</span><span class="sxs-lookup"><span data-stu-id="314e3-129">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="314e3-130">В Dynamics 365 for Retail перейдите в раздел **Розничная торговля** &gt; **ИТ розничной торговли** &gt; **График распределения**.</span><span class="sxs-lookup"><span data-stu-id="314e3-130">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="314e3-131">В списке выберите **1090, Регистры**.</span><span class="sxs-lookup"><span data-stu-id="314e3-131">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="314e3-132">Щелкните **Запустить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="314e3-132">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="314e3-133">Добавление вкладки "Рекомендации" в сетку кнопок в правой части экрана</span><span class="sxs-lookup"><span data-stu-id="314e3-133">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="314e3-134">Щелкните правой кнопкой мыши пустое пространство под последней вкладкой в сетке кнопок, находящейся в правой части страницы.</span><span class="sxs-lookup"><span data-stu-id="314e3-134">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="314e3-135">Щелкните **Настройка**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="314e3-135">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="314e3-136">Нажмите **Создать вкладку**.</span><span class="sxs-lookup"><span data-stu-id="314e3-136">Click **New tab**.</span></span>
4.  <span data-ttu-id="314e3-137">Найдите новую вкладку, которая была добавлена.</span><span class="sxs-lookup"><span data-stu-id="314e3-137">Find the new tab that you just added.</span></span> <span data-ttu-id="314e3-138">Может потребоваться выполнить прокрутку вниз.</span><span class="sxs-lookup"><span data-stu-id="314e3-138">You may need to scroll down.</span></span>
5.  <span data-ttu-id="314e3-139">В раскрывающемся списке **Содержание** выберите **Рекомендуемые продукты**.</span><span class="sxs-lookup"><span data-stu-id="314e3-139">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="314e3-140">[![Рис.-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="314e3-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="314e3-141">В **Метка** введите имя для вкладки рекомендаций. Например, введите "Рекомендуемые продукты".</span><span class="sxs-lookup"><span data-stu-id="314e3-141">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="314e3-142">В поле **Изображение** выберите изображение, которое должно появляться на вкладке.</span><span class="sxs-lookup"><span data-stu-id="314e3-142">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="314e3-143">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="314e3-143">Click **OK**.</span></span> <span data-ttu-id="314e3-144">Новая вкладка отображается в сетке кнопок.</span><span class="sxs-lookup"><span data-stu-id="314e3-144">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="314e3-145">Нажмите кнопку **X**, чтобы сохранить конструктор макетов и выйти из него.</span><span class="sxs-lookup"><span data-stu-id="314e3-145">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="314e3-146">В Dynamics 365 for Retail перейдите в раздел **Розничная торговля** &gt; **ИТ розничной торговли** &gt; **График распределения**.</span><span class="sxs-lookup"><span data-stu-id="314e3-146">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="314e3-147">В списке выберите **1090, Регистры**.</span><span class="sxs-lookup"><span data-stu-id="314e3-147">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="314e3-148">Щелкните **Запустить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="314e3-148">Click **Run now**.</span></span>


<a name="see-also"></a><span data-ttu-id="314e3-149">См. также</span><span class="sxs-lookup"><span data-stu-id="314e3-149">See also</span></span>
--------

[<span data-ttu-id="314e3-150">Обзор персональных рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="314e3-150">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




