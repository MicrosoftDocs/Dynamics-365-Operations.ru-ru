---
title: "Добавление элемента управления рекомендациями на странице проводки на устройстве POS"
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: aa7d1e5392e4d3fa86bf62943cb4f5b5f4c7b383
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a><span data-ttu-id="1e5a8-103">Добавление элемента управления рекомендациями на странице проводки на устройстве POS</span><span class="sxs-lookup"><span data-stu-id="1e5a8-103">Add a recommendations control to the transaction page on a POS device</span></span>

[!INCLUDE [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="1e5a8-104">Мы удаляем текущую версию службы рекомендации продуктов, так как мы переработали эту функцию с использованием более эффективного алгоритма и новыми возможностями, предназначенными для розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="1e5a8-105">Подробнее см. в разделе [Удаленные или устаревшие функции](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span><span class="sxs-lookup"><span data-stu-id="1e5a8-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span> 

<span data-ttu-id="1e5a8-106">В этом разделе описывается, как добавить элемент управления рекомендациями на экране проводки устройства POS, используя конструктор макета экрана в Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="1e5a8-107">При использовании Microsoft Dynamics 365 for Retail можно отображать рекомендации по продукту на устройстве POS.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="1e5a8-108">*Рекомендации* представляют собой номенклатуры, в которых ваш клиент может быть заинтересован на основе его истории покупок, номенклатур в списке планируемых покупок и номенклатур, приобретенных другими клиентами в Интернете и в физических магазинах.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="1e5a8-109">Чтобы отобразить рекомендации по продуктам необходимо добавить элемент управления на экран проводки, используя конструктор макета экрана.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="1e5a8-110">Откройте конструктор макета</span><span class="sxs-lookup"><span data-stu-id="1e5a8-110">Open Layout designer</span></span>
1.  <span data-ttu-id="1e5a8-111">Перейдите в раздел **Розничная торговля** &gt; **Настройка канала** &gt; **Настройка POS** &gt; **POS** &gt; **Макеты экрана**.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="1e5a8-112">Используйте экспресс-фильтр для поиска экрана, на который требуется добавить элемент управления.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="1e5a8-113">Например, выполните фильтрацию по полю **Код макета экрана**, используя значение "F2CP16:9M".</span><span class="sxs-lookup"><span data-stu-id="1e5a8-113">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="1e5a8-114">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="1e5a8-115">Например, выберите "Имя: F2CP16:9M Код макета экрана: F2CP16:9M".</span><span class="sxs-lookup"><span data-stu-id="1e5a8-115">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="1e5a8-116">Нажмите **Конструктор макета**.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-116">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="1e5a8-117">Следуйте инструкциям на экране для запуска конструктора макета.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="1e5a8-118">В ответ на запрос учетных данных следует ввести те же учетные данные, которые были использованы при запуске конструктора макета со страницы **Макеты экрана**.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="1e5a8-119">После входа отображается страница, аналогичная приведенной ниже.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="1e5a8-120">Макет будет отличаться в зависимости от настроек, которые были сделаны в хранилище.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-120">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="1e5a8-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Выберите вариант отображения</span><span class="sxs-lookup"><span data-stu-id="1e5a8-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="1e5a8-122">Доступны два варианта конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-122">There are two configurations options available.</span></span> <span data-ttu-id="1e5a8-123">Выберите вариант, который лучше всего подходит для вашего хранилища, и следуйте оставшимся инструкциям, чтобы завершить настройку элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-123">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="1e5a8-124">Имеется две возможности:</span><span class="sxs-lookup"><span data-stu-id="1e5a8-124">The two options are:</span></span>
-   <span data-ttu-id="1e5a8-125">Рекомендации отображаются всегда.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-125">Recommendations are always visible.</span></span>
-   <span data-ttu-id="1e5a8-126">Вкладка **Рекомендации** отображается в сетке в правой части экрана.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-126">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="1e5a8-127">Чтобы рекомендации отображались всегда</span><span class="sxs-lookup"><span data-stu-id="1e5a8-127">To make recommendations always visible</span></span>

1.  <span data-ttu-id="1e5a8-128">Уменьшите высоту области подробных сведений о строках проводки, чтобы ее высота была равна высоте панели клиента слева.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="1e5a8-128">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="1e5a8-129">Из левого меню перетащите элемент управления рекомендаций в зону между областью сведений строки проводки и сеткой кнопок в нижней центральной части экрана проводок.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="1e5a8-130">Измените размер элемента управления, чтобы он помещался в этой области.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="1e5a8-130">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="1e5a8-131">Нажмите кнопку **X**, чтобы сохранить конструктор макетов и выйти из него.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-131">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="1e5a8-132">В Dynamics 365 for Retail перейдите в раздел **Розничная торговля** &gt; **ИТ розничной торговли** &gt; **График распределения**.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-132">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="1e5a8-133">В списке выберите **1090, Регистры**.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-133">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="1e5a8-134">Щелкните **Запустить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-134">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="1e5a8-135">Добавление вкладки "Рекомендации" в сетку кнопок в правой части экрана</span><span class="sxs-lookup"><span data-stu-id="1e5a8-135">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="1e5a8-136">Щелкните правой кнопкой мыши пустое пространство под последней вкладкой в сетке кнопок, находящейся в правой части страницы.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-136">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="1e5a8-137">Щелкните **Настройка**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="1e5a8-137">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="1e5a8-138">Нажмите **Создать вкладку**.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-138">Click **New tab**.</span></span>
4.  <span data-ttu-id="1e5a8-139">Найдите новую вкладку, которая была добавлена.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-139">Find the new tab that you just added.</span></span> <span data-ttu-id="1e5a8-140">Может потребоваться выполнить прокрутку вниз.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-140">You may need to scroll down.</span></span>
5.  <span data-ttu-id="1e5a8-141">В раскрывающемся списке **Содержание** выберите **Рекомендуемые продукты**.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-141">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="1e5a8-142">[![Рис.-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="1e5a8-142">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="1e5a8-143">В **Метка** введите имя для вкладки рекомендаций. Например, введите "Рекомендуемые продукты".</span><span class="sxs-lookup"><span data-stu-id="1e5a8-143">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="1e5a8-144">В поле **Изображение** выберите изображение, которое должно появляться на вкладке.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-144">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="1e5a8-145">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-145">Click **OK**.</span></span> <span data-ttu-id="1e5a8-146">Новая вкладка отображается в сетке кнопок.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-146">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="1e5a8-147">Нажмите кнопку **X**, чтобы сохранить конструктор макетов и выйти из него.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-147">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="1e5a8-148">В Dynamics 365 for Retail перейдите в раздел **Розничная торговля** &gt; **ИТ розничной торговли** &gt; **График распределения**.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-148">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="1e5a8-149">В списке выберите **1090, Регистры**.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-149">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="1e5a8-150">Щелкните **Запустить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="1e5a8-150">Click **Run now**.</span></span>


<a name="see-also"></a><span data-ttu-id="1e5a8-151">См. также</span><span class="sxs-lookup"><span data-stu-id="1e5a8-151">See also</span></span>
--------

[<span data-ttu-id="1e5a8-152">Обзор персональных рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="1e5a8-152">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




