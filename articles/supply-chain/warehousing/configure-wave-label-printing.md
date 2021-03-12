---
title: Настройка и использование печати этикеток волны
description: В этой теме описывается печать этикеток волны и объясняется, как ее настроить.
author: GarmMSFT
manager: PJacobse
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 862987b8ccdc4272bdd404e78391ad447bc290b3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996359"
---
# <a name="set-up-and-use-wave-label-printing"></a><span data-ttu-id="8e031-103">Настройка и использование печати этикеток волны</span><span class="sxs-lookup"><span data-stu-id="8e031-103">Set up and use wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e031-104">Печать этикеток волны предлагает альтернативный подход к печати этикеток с помощью нового метода шага волны, который позволяет создавать и печатать этикетки непосредственно из шаблона волны при выполнении волны.</span><span class="sxs-lookup"><span data-stu-id="8e031-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="8e031-105">Поэтому этикетки будут доступны до того, когда работники запускают заказ на работу на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="8e031-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="8e031-106">Работники могут затем закрепить требуемые этикетки при комплектации, а не после комплектации.</span><span class="sxs-lookup"><span data-stu-id="8e031-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="8e031-107">В функции печати этикеток волны используется язык программирования Zebra (ZPL) для создания макета этикеток.</span><span class="sxs-lookup"><span data-stu-id="8e031-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="8e031-108">Макет этикетки разделяется на три раздела (верхний колонтитул, основной текст и нижний колонтитул), чтобы иметь возможность использовать этикетки с повторяющейся структурой.</span><span class="sxs-lookup"><span data-stu-id="8e031-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="8e031-109">Шаблоны этикеток волны указывают системе, какую структуру наклеек использовать.</span><span class="sxs-lookup"><span data-stu-id="8e031-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="8e031-110">Пользователи могут указать используемый принтер.</span><span class="sxs-lookup"><span data-stu-id="8e031-110">Users can specify which printer is used.</span></span> <span data-ttu-id="8e031-111">Они также могут печатать этикетки на нескольких принтерах одновременно, по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="8e031-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="8e031-112">На странице **История этикеток волны** отображается запись всех этикеток, которые были созданы с помощью этой настройки.</span><span class="sxs-lookup"><span data-stu-id="8e031-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="8e031-113">Можно печатать этикетки и разбирать их на основе заголовков работ, можно печатать этикетки-разделители для каждого заголовка работы, а также печатать этикетки содержимого контейнеров, этикетки коробок и другие похожие этикетки.</span><span class="sxs-lookup"><span data-stu-id="8e031-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="8e031-114">Эта функция не заменяет существующие функции печати этикеток на основе маршрутизации документов.</span><span class="sxs-lookup"><span data-stu-id="8e031-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="8e031-115">Печать этикеток волны предлагает следующие усовершенствования:</span><span class="sxs-lookup"><span data-stu-id="8e031-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="8e031-116">Печать этикеток в соответствии с количеством упаковок в одной строке работы без использования контейнеризации.</span><span class="sxs-lookup"><span data-stu-id="8e031-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="8e031-117">("Упаковка" — это единица измерения, которая указана в строках группы упорядочения единиц.)</span><span class="sxs-lookup"><span data-stu-id="8e031-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="8e031-118">Печать нескольких различных последовательностей этикеток (например, этикеток коробок и палет).</span><span class="sxs-lookup"><span data-stu-id="8e031-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="8e031-119">Включение перечисления этикеток (например, 1/124, 2/124,... 124/124) и указание диапазона перечисления (например, строка работы, строка загрузки или отгрузка).</span><span class="sxs-lookup"><span data-stu-id="8e031-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="8e031-120">Создание и печать кода транспортной накладной на этикетках перед созданием транспортной накладной.</span><span class="sxs-lookup"><span data-stu-id="8e031-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="8e031-121">Создание уникального порядкового кода контейнера отгрузки (SSCC) для каждой упаковки и включение его в каждую этикетку.</span><span class="sxs-lookup"><span data-stu-id="8e031-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="8e031-122">Создание GS1-совместимых номерных серий для кодов транспортных накладных и кодов SSCC.</span><span class="sxs-lookup"><span data-stu-id="8e031-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="8e031-123">Повторная печать этикеток с мобильных устройств и с расширенного клиента.</span><span class="sxs-lookup"><span data-stu-id="8e031-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="8e031-124">Аннулирование этикеток (например, в случае недостатка для комплектации) и их повторная печать.</span><span class="sxs-lookup"><span data-stu-id="8e031-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="8e031-125">Очистите журнал этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="8e031-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="8e031-126">Улучшения в макетах маршрутизации документов являются общими для макетов маршрутизации документов и макетов этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="8e031-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="8e031-127">(Дополнительные сведения см. в разделе [Макет маршрутизации документов для грузомест](../warehousing/document-routing-layout-for-license-plates.md).)</span><span class="sxs-lookup"><span data-stu-id="8e031-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="8e031-128">Эти улучшения повышают эффективность маркировки упаковок перед погрузкой на палеты.</span><span class="sxs-lookup"><span data-stu-id="8e031-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="8e031-129">Они особенно полезны компаниям, которые осуществляют отгрузку крупным розничным продавцам, которые автоматически подтверждают приемку по заказам путем сканирования каждой упаковки отдельно.</span><span class="sxs-lookup"><span data-stu-id="8e031-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="8e031-130">Сценарии конфигурации, описанные в этом разделе, можно реализовать отдельно или в сочетании, в зависимости от бизнес-требований.</span><span class="sxs-lookup"><span data-stu-id="8e031-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="8e031-131">Можно разработать несколько шаблонов этикеток волны, которые работают последовательно (как показано в сценарии 3).</span><span class="sxs-lookup"><span data-stu-id="8e031-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="8e031-132">Например, можно использовать сценарий 1 для печати этикеток и сценарий 2 для печати этикеток палет (если размер и компоновка палет в запасах различаются).</span><span class="sxs-lookup"><span data-stu-id="8e031-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="8e031-133">Включение функции печати этикеток волны</span><span class="sxs-lookup"><span data-stu-id="8e031-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="8e031-134">Прежде чем использовать функцию *Печать этикеток волны*, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="8e031-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="8e031-135">Администраторы могут использовать рабочую область [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="8e031-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="8e031-136">В этом случае функция указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8e031-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="8e031-137">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="8e031-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="8e031-138">**Имя функции:** *Печать этикеток волны*</span><span class="sxs-lookup"><span data-stu-id="8e031-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="8e031-139">Случай 1. Печать этикеток волны, в которой создается одна этикетка волны</span><span class="sxs-lookup"><span data-stu-id="8e031-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="8e031-140">В этом сценарии показано, как компания может печатать этикетки отгрузки для крупного розничного продавца, который автоматически подтверждает приемку заказов путем сканирования каждой упаковки отдельно.</span><span class="sxs-lookup"><span data-stu-id="8e031-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="8e031-141">В этом сценарии показан сквозной поток.</span><span class="sxs-lookup"><span data-stu-id="8e031-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="8e031-142">Сделать демонстрационные данные доступными</span><span class="sxs-lookup"><span data-stu-id="8e031-142">Make demo data available</span></span>

<span data-ttu-id="8e031-143">Для выполнения этого сценария необходимо установить демонстрационные данные, а также необходимо выбрать юридическое лицо **USMF**.</span><span class="sxs-lookup"><span data-stu-id="8e031-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="8e031-144">Убедитесь, что доступен метод этикеток волны</span><span class="sxs-lookup"><span data-stu-id="8e031-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="8e031-145">Возможно, придется повторно создать методы обработки волны, чтобы сделать доступным метод печати этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="8e031-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="8e031-146">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Методы обработки волн**.</span><span class="sxs-lookup"><span data-stu-id="8e031-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="8e031-147">Убедитесь, что **waveLabelPrinting** есть в списке.</span><span class="sxs-lookup"><span data-stu-id="8e031-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="8e031-148">Если его нет, выберите **Повторно создать методы** на панели операций, чтобы добавить его.</span><span class="sxs-lookup"><span data-stu-id="8e031-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="8e031-149">Настройка шаблона волны</span><span class="sxs-lookup"><span data-stu-id="8e031-149">Configure a wave template</span></span>

<span data-ttu-id="8e031-150">Шаблоны волн позволяют связывать отдельные экземпляры методов волны с соответствующим шаблоном этикетки волны.</span><span class="sxs-lookup"><span data-stu-id="8e031-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="8e031-151">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Шаблоны волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="8e031-152">Выберите шаблон, например **62 Отгрузка по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="8e031-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="8e031-153">На экспресс-вкладке **Методы** переместите метод **Печать этикеток волны** в столбец **Выбранные методы**.</span><span class="sxs-lookup"><span data-stu-id="8e031-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="8e031-154">В столбце **Выбранные методы** выберите метод **Печать этикеток волны** и задайте для его поля **Код шага волны** значение *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="8e031-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="8e031-155">Дополнительные сведения о кодах шага волны см. в разделе [Коды шагов волны](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8e031-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="8e031-156">Создание макета этикеток волны</span><span class="sxs-lookup"><span data-stu-id="8e031-156">Create a wave label layout</span></span>

<span data-ttu-id="8e031-157">Макет этикетки определяет, какая информация печатается на этикетке и как она была размещается. Здесь вводится код ZPL, который отправляется на принтер.</span><span class="sxs-lookup"><span data-stu-id="8e031-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="8e031-158">Перейдите в раздел **Управление складом \> Настройка \> Маршрутизация документов \> Печать этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="8e031-159">Создайте запись со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="8e031-160">**Код макета этикетки:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="8e031-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="8e031-161">**Описание:** *Упаковка (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="8e031-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="8e031-162">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8e031-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="8e031-163">В области действий выберите **Параметры строки этикетки волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="8e031-164">Будет открыта страница **Параметры строки этикетки волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="8e031-165">Здесь можно настроить динамическую часть этикетки.</span><span class="sxs-lookup"><span data-stu-id="8e031-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="8e031-166">Добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-167">**Код строки:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="8e031-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="8e031-168">**Имя таблицы строк:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="8e031-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="8e031-169">**Положение начала строки:** *0*</span><span class="sxs-lookup"><span data-stu-id="8e031-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="8e031-170">В этом поле определяется вертикальная позиция, с которой строка будет начинаться на этикетке.</span><span class="sxs-lookup"><span data-stu-id="8e031-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="8e031-171">**Высота строки:** *0*</span><span class="sxs-lookup"><span data-stu-id="8e031-171">**Row height:** *0*</span></span>

        <span data-ttu-id="8e031-172">Это поле определяет высоту каждой строки (в пунктах) в соответствии со стандартом ZPL.</span><span class="sxs-lookup"><span data-stu-id="8e031-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="8e031-173">Высота строки является положительной для горизонтальных этикеток и отрицательных для вертикальных этикеток.</span><span class="sxs-lookup"><span data-stu-id="8e031-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="8e031-174">Поскольку в данном примере имеется только одна строка, можно установить значение равным *0* (нулю).</span><span class="sxs-lookup"><span data-stu-id="8e031-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="8e031-175">**Строк на странице:** *1*</span><span class="sxs-lookup"><span data-stu-id="8e031-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="8e031-176">В этом поле определяется число строк, которое может быть напечатано на каждой этикетке.</span><span class="sxs-lookup"><span data-stu-id="8e031-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="8e031-177">Эта настройка приведет к печати отдельной этикетки ZPL для каждой записи в таблице этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="8e031-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="8e031-178">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8e031-178">Close the page.</span></span>
1. <span data-ttu-id="8e031-179">На панели операций выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="8e031-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="8e031-180">В диалоговом окне редактора запросов на вкладке **Диапазон** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-181">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="8e031-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="8e031-182">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="8e031-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="8e031-183">**Поле:** *Тип работы*</span><span class="sxs-lookup"><span data-stu-id="8e031-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="8e031-184">**Критерии:** *Комплектации*</span><span class="sxs-lookup"><span data-stu-id="8e031-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="8e031-185">Этот запрос гарантирует, что в этикетке будут печататься только строки работа типа "Комплектация", а не строки типа "Размещение".</span><span class="sxs-lookup"><span data-stu-id="8e031-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="8e031-186">Если необходимо распечатать код транспортной накладной, на вкладке **Объединения** выберите таблицу **Строки работ** и присоедините к ней таблицу **Отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="8e031-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="8e031-187">Закройте диалоговое окно редактора запросов.</span><span class="sxs-lookup"><span data-stu-id="8e031-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="8e031-188">На экспресс-вкладке **Макет текста принтера** имеется три раздела для написания кода принтера: **Раздел заголовка**, **Раздел текста** и **Раздел нижнего колонтитула**.</span><span class="sxs-lookup"><span data-stu-id="8e031-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="8e031-189">В разделе **Раздел заголовка** в поле **Заголовок этикетки** введите код для требуемого заголовка.</span><span class="sxs-lookup"><span data-stu-id="8e031-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="8e031-190">Например, при использовании принтеров Zebra можно использовать следующий код.</span><span class="sxs-lookup"><span data-stu-id="8e031-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="8e031-191">В разделе **Раздел текста** в поле **Текст этикетки** введите код ZPL для требуемого текста.</span><span class="sxs-lookup"><span data-stu-id="8e031-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="8e031-192">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="8e031-192">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="8e031-193">В разделе **Раздел текста** в поле **Нижний колонтитул этикетки** введите код ZPL для требуемого нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="8e031-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="8e031-194">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="8e031-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="8e031-195">При этой настройке будет напечатана одна копия каждой этикетки.</span><span class="sxs-lookup"><span data-stu-id="8e031-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="8e031-196">Если требуется больше копий (например, одна копия для каждой из сторон палеты), установите значение **n** для раздела **\^PQn** в нижнем колонтитуле равным требуемому числу копий.</span><span class="sxs-lookup"><span data-stu-id="8e031-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="8e031-197">Например, чтобы напечатать четыре копии каждой этикетки, укажите **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="8e031-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="8e031-198">Теперь этикетка готова к использованию.</span><span class="sxs-lookup"><span data-stu-id="8e031-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="8e031-199">Создание типа этикеток волны</span><span class="sxs-lookup"><span data-stu-id="8e031-199">Create a wave label type</span></span>

<span data-ttu-id="8e031-200">Типы этикеток волн используются для связывания шаблонов этикеток волн с единицей в строках группы последовательностей единиц.</span><span class="sxs-lookup"><span data-stu-id="8e031-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="8e031-201">Перейдите в раздел **Управление складом \> Настройка \> Маршрутизация документов \> Типы этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="8e031-202">Добавьте тип этикетки волны со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="8e031-203">**Тип этикетки:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="8e031-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="8e031-204">**Описание:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="8e031-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="8e031-205">Настройка групп упорядочения единиц</span><span class="sxs-lookup"><span data-stu-id="8e031-205">Set up unit sequence groups</span></span>

<span data-ttu-id="8e031-206">Затем настройте группу упорядочения единиц для типа этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="8e031-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="8e031-207">Перейдите в раздел **Управление складом \> Настройка \> Склад \> Группы упорядочения единиц**.</span><span class="sxs-lookup"><span data-stu-id="8e031-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="8e031-208">Выберите группу **штука, ящик, палета**.</span><span class="sxs-lookup"><span data-stu-id="8e031-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="8e031-209">Для строки **Ящик** введите в поле **Тип уровня волны** значение *Упаковка*.</span><span class="sxs-lookup"><span data-stu-id="8e031-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="8e031-210">Создание шаблона этикеток волны</span><span class="sxs-lookup"><span data-stu-id="8e031-210">Create a wave label template</span></span>

<span data-ttu-id="8e031-211">Затем создайте шаблон этикетки волны для типа этикеток волн.</span><span class="sxs-lookup"><span data-stu-id="8e031-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="8e031-212">Перейдите в раздел **Управление складом \> Настройка \> Маршрутизация документов \> Шаблоны этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="8e031-213">Добавьте шаблон этикетки волны, затем задайте следующие значения в заголовке:</span><span class="sxs-lookup"><span data-stu-id="8e031-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="8e031-214">**Наименование шаблона этикетки:** *Этикетки для упаковки*</span><span class="sxs-lookup"><span data-stu-id="8e031-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="8e031-215">**Описание:** *Этикетки для упаковки*</span><span class="sxs-lookup"><span data-stu-id="8e031-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="8e031-216">**Код шага волны:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="8e031-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="8e031-217">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="8e031-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="8e031-218">На экспресс-вкладке **Общие** задайте в поле **Тип этикетки волны** значение *Упаковка*.</span><span class="sxs-lookup"><span data-stu-id="8e031-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="8e031-219">На экспресс-вкладке **Сведения шаблона этикетки волны** добавьте новую строку со следующими настройками:</span><span class="sxs-lookup"><span data-stu-id="8e031-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-220">**Код макета этикетки:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="8e031-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="8e031-221">**Имя принтера:** выберите подходящий принтер ZPL.</span><span class="sxs-lookup"><span data-stu-id="8e031-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="8e031-222">**Выполнение запроса:** *Да* (Этот параметр не является обязательным, но рекомендуется для достижения оптимальной производительности.)</span><span class="sxs-lookup"><span data-stu-id="8e031-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="8e031-223">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8e031-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="8e031-224">Необязательно: если вы настраиваете дизайн этикеток для определенного клиента, необходимо создать запрос, чтобы найти учетную запись клиента.</span><span class="sxs-lookup"><span data-stu-id="8e031-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="8e031-225">На экспресс-вкладке **Сведения шаблона этикетки волны** выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="8e031-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="8e031-226">Затем в диалоговом окне редактора запросов на вкладке **Диапазон** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-227">**Таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="8e031-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="8e031-228">**Производная таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="8e031-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="8e031-229">**Поле:** *Номер учетной записи*</span><span class="sxs-lookup"><span data-stu-id="8e031-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="8e031-230">**Критерии:** введите соответствующий номер учетной записи клиента.</span><span class="sxs-lookup"><span data-stu-id="8e031-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="8e031-231">После завершения нажмите кнопку **OK**, чтобы закрыть диалоговое окно редактора запросов.</span><span class="sxs-lookup"><span data-stu-id="8e031-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="8e031-232">На панели операций выберите **Изменить запрос**, чтобы открыть диалоговое окно редактора запросов для всего шаблона этикетки.</span><span class="sxs-lookup"><span data-stu-id="8e031-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="8e031-233">В диалоговом окне редактора запросов на вкладке **Сортировка** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-234">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="8e031-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="8e031-235">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="8e031-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="8e031-236">**Поле:** *Код строки загрузки ссылки (ИД записи)*</span><span class="sxs-lookup"><span data-stu-id="8e031-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="8e031-237">**Направление поиска:** *Восходящее*</span><span class="sxs-lookup"><span data-stu-id="8e031-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="8e031-238">Выберите **ОК**, чтобы закрыть диалоговое окно редактора запроса.</span><span class="sxs-lookup"><span data-stu-id="8e031-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="8e031-239">В окне сообщение будет предложено подтвердить операцию сброса группы.</span><span class="sxs-lookup"><span data-stu-id="8e031-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="8e031-240">Выберите **Да** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="8e031-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="8e031-241">В области действий выберите **Группа шаблонов этикеток волн**.</span><span class="sxs-lookup"><span data-stu-id="8e031-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="8e031-242">В диалоговом окне **Группа шаблонов этикеток волн** выберите строку, в которой поле **Имя поля ссылки** имеет значение *Код строки загрузки ссылки*, затем установите флажок **Код сборки этикетки** для этой строки.</span><span class="sxs-lookup"><span data-stu-id="8e031-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id*, and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8e031-243">Эта настройка создаст одну последовательность этикеток ("Упаковка 1 из X") для каждой строки загрузки в волне, независимо от настройки группировки работ.</span><span class="sxs-lookup"><span data-stu-id="8e031-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="8e031-244">Эта последовательность этикеток может быть распечатана в макете этикеток.</span><span class="sxs-lookup"><span data-stu-id="8e031-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="8e031-245">Настройка расширений номерной серии</span><span class="sxs-lookup"><span data-stu-id="8e031-245">Configure number sequence extensions</span></span>

<span data-ttu-id="8e031-246">Расширения номерных серий управляют GS1-соответствием для определенных номерных серий.</span><span class="sxs-lookup"><span data-stu-id="8e031-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="8e031-247">Эта настройка не является обязательной для текущего сценария.</span><span class="sxs-lookup"><span data-stu-id="8e031-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="8e031-248">Дополнительные сведения и инструкции по настройке см. в разделе [Настройка расширений номерных серий](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="8e031-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="8e031-249">Создание заказа на продажу и выпуск его на склад</span><span class="sxs-lookup"><span data-stu-id="8e031-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="8e031-250">Перейдите в раздел **Продажи и маркетинг \> Заказ на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="8e031-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="8e031-251">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="8e031-252">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="8e031-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8e031-253">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="8e031-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="8e031-254">Добавьте две строки заказа на продажу со следующими настройками:</span><span class="sxs-lookup"><span data-stu-id="8e031-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="8e031-255">Строка заказа на продажу 1:</span><span class="sxs-lookup"><span data-stu-id="8e031-255">Sales order line 1:</span></span>

        - <span data-ttu-id="8e031-256">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="8e031-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="8e031-257">**Количество:** *9024*</span><span class="sxs-lookup"><span data-stu-id="8e031-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="8e031-258">**Единица измерения:** *шт.* (9024 шт. = 376 коробок = 47 палет)</span><span class="sxs-lookup"><span data-stu-id="8e031-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="8e031-259">Строка заказа на продажу 2:</span><span class="sxs-lookup"><span data-stu-id="8e031-259">Sales order line 2:</span></span>

        - <span data-ttu-id="8e031-260">**Код номенклатуры:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="8e031-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="8e031-261">**Количество:** *9016*</span><span class="sxs-lookup"><span data-stu-id="8e031-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="8e031-262">**Единица измерения:** *шт.* (9016 шт. = 322 коробки = 46 палет)</span><span class="sxs-lookup"><span data-stu-id="8e031-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="8e031-263">Представленные здесь номенклатуры и количества являются только примерами.</span><span class="sxs-lookup"><span data-stu-id="8e031-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="8e031-264">Они должны использовать ранее определенную группу последовательности единиц измерения, подходящие преобразования единиц измерения из *шт.* в *коробки* и в *палеты*, для которых должны быть запасы на складе *62*.</span><span class="sxs-lookup"><span data-stu-id="8e031-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="8e031-265">Дополнительные сведения см. в разделе [Единицы измерения и политики хранения](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="8e031-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="8e031-266">Выберите строку заказа на продажу 1.</span><span class="sxs-lookup"><span data-stu-id="8e031-266">Select sales order line 1.</span></span> <span data-ttu-id="8e031-267">Затем в разделе **Строка заказа на продажу** в меню **Запасы** выберите **Резервирования**.</span><span class="sxs-lookup"><span data-stu-id="8e031-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="8e031-268">На странице **Резервирование** в области действий выберите **Зарезервировать лот**, затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8e031-268">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="8e031-269">Повторите шаги 4 и 5 для строки заказа на продажу 2.</span><span class="sxs-lookup"><span data-stu-id="8e031-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="8e031-270">На панели операций на вкладке **Склад** выберите вариант **Выпустить на склад**.</span><span class="sxs-lookup"><span data-stu-id="8e031-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="8e031-271">Имеют место следующие события:</span><span class="sxs-lookup"><span data-stu-id="8e031-271">The following events occur:</span></span>

    - <span data-ttu-id="8e031-272">Система обрабатывает созданную отгрузку, используя шаблон, содержащий шаг печати этикеток.</span><span class="sxs-lookup"><span data-stu-id="8e031-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="8e031-273">Макет этикетки будет использоваться для определения формата этикетки, а результатом будет этикетка, которая печатается на принтере, выбранном в шаблоне этикетки.</span><span class="sxs-lookup"><span data-stu-id="8e031-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="8e031-274">Этикетки волны создаются и печатаются.</span><span class="sxs-lookup"><span data-stu-id="8e031-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="8e031-275">Число этикеток будет равно количеству коробок (в данном примере 376 этикеток коробок для строки 1 и 322 этикетки коробок для строки 2).</span><span class="sxs-lookup"><span data-stu-id="8e031-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="8e031-276">Для отгрузок создается новый код транспортной накладной.</span><span class="sxs-lookup"><span data-stu-id="8e031-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="8e031-277">Если настроены расширения номерной серии, коды этикеток волны будут соответствовать формату номера **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="8e031-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="8e031-278">На следующих страницах можно просматривать и перепечатывать этикетки волны.</span><span class="sxs-lookup"><span data-stu-id="8e031-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="8e031-279">На панели операций на каждой странице на вкладке **Отгрузки** в группе **Связанные сведения** выберите **Этикетки волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="8e031-280">Все отгрузки \> Сведения об отгрузках</span><span class="sxs-lookup"><span data-stu-id="8e031-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="8e031-281">Все загрузки \> Сведения о загрузках</span><span class="sxs-lookup"><span data-stu-id="8e031-281">All loads \> Load details</span></span>
- <span data-ttu-id="8e031-282">Все волны</span><span class="sxs-lookup"><span data-stu-id="8e031-282">All waves</span></span>
- <span data-ttu-id="8e031-283">Этикетки волны</span><span class="sxs-lookup"><span data-stu-id="8e031-283">Wave labels</span></span>
- <span data-ttu-id="8e031-284">История этикеток волны</span><span class="sxs-lookup"><span data-stu-id="8e031-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="8e031-285">Сценарий 2. Печать этикеток для контейнеризации (без записей этикеток волны)</span><span class="sxs-lookup"><span data-stu-id="8e031-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="8e031-286">Этот сценарий позволяет печатать этикетки волны, когда используется контейнеризация для автоматического разбиения номенклатур на коробки и, таким образом, не требуется запись этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="8e031-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="8e031-287">В этом случае идентификатор контейнера выступает в качестве местозаполнителя для SSCC.</span><span class="sxs-lookup"><span data-stu-id="8e031-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="8e031-288">Ниже приведены основные различия между этим сценарием и сценарием 1:</span><span class="sxs-lookup"><span data-stu-id="8e031-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="8e031-289">**Шаблоны этикеток волны:** вы не будете выбирать тип этикеток волны для шаблона волны, и при этом не требуется группирование сборки этикеток.</span><span class="sxs-lookup"><span data-stu-id="8e031-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="8e031-290">В противном случае будет настроен шаблон этикетки волны и ссылка на шаблон волны аналогично описанию в сценарии 1.</span><span class="sxs-lookup"><span data-stu-id="8e031-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="8e031-291">Чтобы не допустить создания этикеток волны, необходимо оставить поле типа этикеток волны пустым.</span><span class="sxs-lookup"><span data-stu-id="8e031-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="8e031-292">**Макет этикеток волны:** вы настроите параметры строки макета этикеток волны для строк работы вместо записей этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="8e031-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="8e031-293">Необходимо настроить параметр строки для макета этикеток, используя таблицу **WHSWorkLine** вместо таблицы **WHSWaveLabel**.</span><span class="sxs-lookup"><span data-stu-id="8e031-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="8e031-294">Параметр **Строк на странице** определяет количество строк, которое будет иметь раздел текста.</span><span class="sxs-lookup"><span data-stu-id="8e031-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="8e031-295">Эта конфигурация также подходит для бизнес-сценариев, в которых несколько различных номенклатур упаковываются в одну маркированную коробку или на палету, и этот процесс упаковки может быть определен при помощи создания работы (например, работы, сгруппированной по отгрузке).</span><span class="sxs-lookup"><span data-stu-id="8e031-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="8e031-296">В этом сценарии показан сквозной поток.</span><span class="sxs-lookup"><span data-stu-id="8e031-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="8e031-297">Сделать демонстрационные данные доступными</span><span class="sxs-lookup"><span data-stu-id="8e031-297">Make demo data available</span></span>

<span data-ttu-id="8e031-298">Для выполнения этого сценария необходимо установить демонстрационные данные, а также необходимо выбрать юридическое лицо **USMF**.</span><span class="sxs-lookup"><span data-stu-id="8e031-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="8e031-299">Убедитесь, что доступен метод этикеток волны</span><span class="sxs-lookup"><span data-stu-id="8e031-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="8e031-300">Возможно, придется повторно создать методы обработки волны, чтобы сделать доступным метод печати этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="8e031-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="8e031-301">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Методы обработки волн**.</span><span class="sxs-lookup"><span data-stu-id="8e031-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="8e031-302">Убедитесь, что **waveLabelPrinting** есть в списке.</span><span class="sxs-lookup"><span data-stu-id="8e031-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="8e031-303">Если его нет, выберите **Повторно создать методы** на панели операций, чтобы добавить его.</span><span class="sxs-lookup"><span data-stu-id="8e031-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="8e031-304">Настройка шаблона волны</span><span class="sxs-lookup"><span data-stu-id="8e031-304">Set up a wave template</span></span>

<span data-ttu-id="8e031-305">Шаблоны волн позволяют связывать отдельные экземпляры методов волны с соответствующим шаблоном этикетки волны.</span><span class="sxs-lookup"><span data-stu-id="8e031-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="8e031-306">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Шаблоны волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="8e031-307">Выберите шаблон, например **63 Контейнеризация**.</span><span class="sxs-lookup"><span data-stu-id="8e031-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="8e031-308">На экспресс-вкладке **Методы** переместите метод **Печать этикеток волны** в столбец **Выбранные методы**.</span><span class="sxs-lookup"><span data-stu-id="8e031-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="8e031-309">В столбце **Выбранные методы** выберите метод **Печать этикеток волны** и задайте для его поля **Код шага волны** значение *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="8e031-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="8e031-310">Дополнительные сведения о кодах шага волны см. в разделе [Коды шагов волны](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8e031-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="8e031-311">Создание макета этикеток волны</span><span class="sxs-lookup"><span data-stu-id="8e031-311">Create a wave label layout</span></span>

1. <span data-ttu-id="8e031-312">Перейдите в раздел **Управление складом \> Настройка \> Маршрутизация документов \> Печать этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="8e031-313">Создайте запись со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="8e031-314">**Код макета этикетки:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="8e031-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="8e031-315">**Описание:** *Упаковка (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="8e031-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="8e031-316">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8e031-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="8e031-317">В области действий выберите **Параметры строки этикетки волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="8e031-318">Будет открыта страница **Параметры строки этикетки волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="8e031-319">Здесь можно настроить динамическую часть этикетки.</span><span class="sxs-lookup"><span data-stu-id="8e031-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="8e031-320">Добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-321">**Код строки:** *WorkLine*</span><span class="sxs-lookup"><span data-stu-id="8e031-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="8e031-322">**Имя таблицы строк:** *WHSWorkLine*</span><span class="sxs-lookup"><span data-stu-id="8e031-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="8e031-323">**Положение начала строки:** *500*</span><span class="sxs-lookup"><span data-stu-id="8e031-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="8e031-324">В этом поле определяется вертикальная позиция, с которой строка будет начинаться на этикетке.</span><span class="sxs-lookup"><span data-stu-id="8e031-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="8e031-325">**Высота строки:** *-50*</span><span class="sxs-lookup"><span data-stu-id="8e031-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="8e031-326">Это поле определяет высоту каждой строки.</span><span class="sxs-lookup"><span data-stu-id="8e031-326">This field defines the height of each row.</span></span> <span data-ttu-id="8e031-327">Высота строки является положительной для горизонтальных этикеток и отрицательных для вертикальных этикеток.</span><span class="sxs-lookup"><span data-stu-id="8e031-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="8e031-328">**Строк на странице:** *5*</span><span class="sxs-lookup"><span data-stu-id="8e031-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="8e031-329">В этом поле определяется число строк, которое может быть напечатано на каждой этикетке.</span><span class="sxs-lookup"><span data-stu-id="8e031-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="8e031-330">При этой настройке будет распечатано несколько этикеток ZPL на работу, где каждая страница может содержать до пяти строк работы.</span><span class="sxs-lookup"><span data-stu-id="8e031-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="8e031-331">Например, если для контейнера, имеющего 12 строк, печатается этикетка, будут распечатаны три этикетки.</span><span class="sxs-lookup"><span data-stu-id="8e031-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="8e031-332">Если требуется напечатать отдельную этикетку для каждой строки комплектации, установите значение *1*.</span><span class="sxs-lookup"><span data-stu-id="8e031-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="8e031-333">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8e031-333">Close the page.</span></span>
1. <span data-ttu-id="8e031-334">На панели операций выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="8e031-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="8e031-335">В диалоговом окне редактора запросов на вкладке **Диапазон** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-336">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="8e031-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="8e031-337">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="8e031-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="8e031-338">**Поле:** *Тип работы*</span><span class="sxs-lookup"><span data-stu-id="8e031-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="8e031-339">**Критерии:** *Комплектации*</span><span class="sxs-lookup"><span data-stu-id="8e031-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="8e031-340">Если необходимо распечатать код транспортной накладной, на вкладке **Объединения** выберите таблицу **Строки работ** и присоедините к ней таблицу **Отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="8e031-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="8e031-341">Закройте диалоговое окно редактора запросов.</span><span class="sxs-lookup"><span data-stu-id="8e031-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="8e031-342">На экспресс-вкладке **Макет текста принтера** имеется три раздела для написания кода принтера: **Раздел заголовка**, **Раздел текста** и **Раздел нижнего колонтитула**.</span><span class="sxs-lookup"><span data-stu-id="8e031-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="8e031-343">В разделе **Раздел заголовка** в поле **Заголовок этикетки** введите код для требуемого заголовка.</span><span class="sxs-lookup"><span data-stu-id="8e031-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="8e031-344">Например, при использовании принтеров Zebra можно использовать следующий код.</span><span class="sxs-lookup"><span data-stu-id="8e031-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="8e031-345">В разделе **Раздел текста** в поле **Текст этикетки** введите код ZPL для требуемого текста.</span><span class="sxs-lookup"><span data-stu-id="8e031-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="8e031-346">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="8e031-346">Here is an example.</span></span>

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="8e031-347">В разделе **Раздел текста** в поле **Нижний колонтитул этикетки** введите код ZPL для требуемого нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="8e031-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="8e031-348">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="8e031-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="8e031-349">При этой настройке будет напечатана одна копия каждой этикетки.</span><span class="sxs-lookup"><span data-stu-id="8e031-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="8e031-350">Если требуется больше копий (например, одна копия для каждой из сторон палеты), установите значение **n** для раздела **\^PQn** в нижнем колонтитуле равным требуемому числу копий.</span><span class="sxs-lookup"><span data-stu-id="8e031-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="8e031-351">Например, чтобы напечатать четыре копии каждой этикетки, укажите **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="8e031-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="8e031-352">Теперь этикетка готова к использованию.</span><span class="sxs-lookup"><span data-stu-id="8e031-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="8e031-353">Создание шаблона этикеток волны</span><span class="sxs-lookup"><span data-stu-id="8e031-353">Create a wave label template</span></span>

1. <span data-ttu-id="8e031-354">Перейдите в раздел **Управление складом \> Настройка \> Маршрутизация документов \> Шаблоны этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="8e031-355">Добавьте шаблон этикетки волны, затем задайте следующие значения в заголовке:</span><span class="sxs-lookup"><span data-stu-id="8e031-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="8e031-356">**Наименование шаблона этикетки:** *Этикетки для контейнеров*</span><span class="sxs-lookup"><span data-stu-id="8e031-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="8e031-357">**Описание:** *Этикетки для контейнеров*</span><span class="sxs-lookup"><span data-stu-id="8e031-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="8e031-358">**Код шага волны:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="8e031-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="8e031-359">**Склад:** *63*</span><span class="sxs-lookup"><span data-stu-id="8e031-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="8e031-360">На экспресс-вкладке **Сведения шаблона этикетки волны** добавьте строку со следующими настройками:</span><span class="sxs-lookup"><span data-stu-id="8e031-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-361">**Код макета этикетки:** *Контейнер*</span><span class="sxs-lookup"><span data-stu-id="8e031-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="8e031-362">**Имя принтера:** выберите подходящий принтер ZPL.</span><span class="sxs-lookup"><span data-stu-id="8e031-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="8e031-363">**Выполнение запроса:** *Да* (Этот параметр не является обязательным, но рекомендуется для достижения оптимальной производительности.)</span><span class="sxs-lookup"><span data-stu-id="8e031-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="8e031-364">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8e031-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="8e031-365">Необязательно: если вы настраиваете дизайн этикеток для определенного клиента, необходимо создать запрос, чтобы найти учетную запись клиента.</span><span class="sxs-lookup"><span data-stu-id="8e031-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="8e031-366">На экспресс-вкладке **Сведения шаблона этикетки волны** выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="8e031-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="8e031-367">Затем в диалоговом окне редактора запросов на вкладке **Диапазон** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-368">**Таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="8e031-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="8e031-369">**Производная таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="8e031-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="8e031-370">**Поле:** *Номер учетной записи*</span><span class="sxs-lookup"><span data-stu-id="8e031-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="8e031-371">**Критерии:** введите соответствующий номер учетной записи клиента.</span><span class="sxs-lookup"><span data-stu-id="8e031-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="8e031-372">После завершения нажмите кнопку **OK**, чтобы закрыть диалоговое окно редактора запросов.</span><span class="sxs-lookup"><span data-stu-id="8e031-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="8e031-373">Настройка расширений номерной серии</span><span class="sxs-lookup"><span data-stu-id="8e031-373">Configure number sequence extensions</span></span>

<span data-ttu-id="8e031-374">Расширения номерных серий управляют GS1-соответствием для определенных номерных серий.</span><span class="sxs-lookup"><span data-stu-id="8e031-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="8e031-375">Эта настройка не является обязательной для текущего сценария.</span><span class="sxs-lookup"><span data-stu-id="8e031-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="8e031-376">Дополнительные сведения и инструкции по настройке см. в разделе [Настройка расширений номерных серий](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="8e031-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="8e031-377">Создание заказа на продажу и выпуск его на склад</span><span class="sxs-lookup"><span data-stu-id="8e031-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="8e031-378">Перейдите в раздел **Продажи и маркетинг \> Заказ на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="8e031-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="8e031-379">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="8e031-380">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="8e031-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8e031-381">**Склад:** *63*</span><span class="sxs-lookup"><span data-stu-id="8e031-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="8e031-382">Добавьте пять строк заказа на продажу:</span><span class="sxs-lookup"><span data-stu-id="8e031-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="8e031-383">Строка заказа на продажу 1:</span><span class="sxs-lookup"><span data-stu-id="8e031-383">Sales order line 1:</span></span>

        - <span data-ttu-id="8e031-384">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="8e031-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="8e031-385">**Количество:** *10*</span><span class="sxs-lookup"><span data-stu-id="8e031-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="8e031-386">Строка заказа на продажу 2:</span><span class="sxs-lookup"><span data-stu-id="8e031-386">Sales order line 2:</span></span>

        - <span data-ttu-id="8e031-387">**Код номенклатуры:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="8e031-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="8e031-388">**Количество:** *20*</span><span class="sxs-lookup"><span data-stu-id="8e031-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="8e031-389">Строка заказа на продажу 3:</span><span class="sxs-lookup"><span data-stu-id="8e031-389">Sales order line 3:</span></span>

        - <span data-ttu-id="8e031-390">**Код номенклатуры:** *L0006*</span><span class="sxs-lookup"><span data-stu-id="8e031-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="8e031-391">**Количество:** *20*</span><span class="sxs-lookup"><span data-stu-id="8e031-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="8e031-392">Строка заказа на продажу 4:</span><span class="sxs-lookup"><span data-stu-id="8e031-392">Sales order line 4:</span></span>

        - <span data-ttu-id="8e031-393">**Код номенклатуры:** *L0100*</span><span class="sxs-lookup"><span data-stu-id="8e031-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="8e031-394">**Количество:** *40*</span><span class="sxs-lookup"><span data-stu-id="8e031-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="8e031-395">Строка заказа на продажу 5:</span><span class="sxs-lookup"><span data-stu-id="8e031-395">Sales order line 5:</span></span>

        - <span data-ttu-id="8e031-396">**Код номенклатуры:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="8e031-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="8e031-397">**Количество:** *50*</span><span class="sxs-lookup"><span data-stu-id="8e031-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="8e031-398">Представленные здесь номенклатуры и количества являются только примерами.</span><span class="sxs-lookup"><span data-stu-id="8e031-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="8e031-399">Они должны иметь запасы на указанном складе.</span><span class="sxs-lookup"><span data-stu-id="8e031-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="8e031-400">Выберите строку заказа на продажу 1.</span><span class="sxs-lookup"><span data-stu-id="8e031-400">Select sales order line 1.</span></span> <span data-ttu-id="8e031-401">Затем в разделе **Строка заказа на продажу** в меню **Запасы** выберите **Резервирования**.</span><span class="sxs-lookup"><span data-stu-id="8e031-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="8e031-402">На странице **Резервирование** в области действий выберите **Зарезервировать лот**, затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8e031-402">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="8e031-403">Повторите шаги 4 и 5 для каждой дополнительной строки заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="8e031-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="8e031-404">На панели операций на вкладке **Склад** выберите вариант **Выпустить на склад**.</span><span class="sxs-lookup"><span data-stu-id="8e031-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="8e031-405">Имеют место следующие события:</span><span class="sxs-lookup"><span data-stu-id="8e031-405">The following events occur:</span></span>

    - <span data-ttu-id="8e031-406">Система обрабатывает созданную отгрузку, используя шаблон, содержащий шаг печати этикеток.</span><span class="sxs-lookup"><span data-stu-id="8e031-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="8e031-407">Макет этикетки будет использоваться для определения формата этикетки, а конечным результатом будет этикетка, которая содержит пять строк и печатается на принтере, выбранном в шаблоне этикетки.</span><span class="sxs-lookup"><span data-stu-id="8e031-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="8e031-408">Для отгрузок создается новый код транспортной накладной.</span><span class="sxs-lookup"><span data-stu-id="8e031-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="8e031-409">Если настроены расширения номерной серии, коды этикеток волны будут соответствовать формату номера **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="8e031-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="8e031-410">Эти этикетки волны можно перепечатать, перейдя в раздел **Управление складом \> Запросы и отчеты \> История этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="8e031-411">Сценарий 3. Печать этикеток волны для многоуровневых этикеток</span><span class="sxs-lookup"><span data-stu-id="8e031-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="8e031-412">В этом сценарии показано, как использовать функции печати этикеток волны, когда складские процессы требуют наличия нескольких уровней этикеток отгрузки.</span><span class="sxs-lookup"><span data-stu-id="8e031-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="8e031-413">Например, может требоваться печатать отдельные этикетки для коробок и палет, а разделительная этикетка должна быть распечатана для всей отгрузки.</span><span class="sxs-lookup"><span data-stu-id="8e031-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="8e031-414">Разделительные этикетки представляют собой отдельный тип этикетки, который может использоваться в качестве разделителя между рулонами и контейнерами, например этикетки для кода отгрузки и штрихкода, чтобы можно было легко отсортировать этикетки после их печати.</span><span class="sxs-lookup"><span data-stu-id="8e031-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="8e031-415">Основное различие между конфигурацией этого сценария и конфигурацией сценария 1, помимо того, что включены разделительные этикетки, состоит в том, что несколько типов этикеток волны должны быть связаны с шаблонами этикеток волны и строками группы последовательности единиц.</span><span class="sxs-lookup"><span data-stu-id="8e031-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="8e031-416">Для выполнения этой настройки в этом сценарии настраиваются следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="8e031-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="8e031-417">**Методы обработки волн:** вы пометите метод этикеток волны как "повторяемый", добавите его два (или более) раз в шаблон волн и зададите другие коды шагов волны.</span><span class="sxs-lookup"><span data-stu-id="8e031-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="8e031-418">**Шаблоны этикеток волны:** вы настроите шаблоны этикеток волны и свяжите их с шаблоном волны.</span><span class="sxs-lookup"><span data-stu-id="8e031-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="8e031-419">Каждый шаблон этикетки волны имеет свой собственный тип этикетки волны.</span><span class="sxs-lookup"><span data-stu-id="8e031-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="8e031-420">**Макеты этикеток волны:** будет создано несколько макетов этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="8e031-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="8e031-421">Для каждого "уровня" этикеток будет использоваться отдельный макет этикеток, а также будет макет разделительной этикетки.</span><span class="sxs-lookup"><span data-stu-id="8e031-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="8e031-422">В этом сценарии показан сквозной поток.</span><span class="sxs-lookup"><span data-stu-id="8e031-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="8e031-423">Сделать демонстрационные данные доступными</span><span class="sxs-lookup"><span data-stu-id="8e031-423">Make demo data available</span></span>

<span data-ttu-id="8e031-424">Для выполнения этого сценария необходимо установить демонстрационные данные, а также необходимо выбрать юридическое лицо **USMF**.</span><span class="sxs-lookup"><span data-stu-id="8e031-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="8e031-425">Настройка метода обработки волны</span><span class="sxs-lookup"><span data-stu-id="8e031-425">Set up a wave process method</span></span>

1. <span data-ttu-id="8e031-426">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Методы обработки волн**.</span><span class="sxs-lookup"><span data-stu-id="8e031-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="8e031-427">Убедитесь, что **waveLabelPrinting** есть в списке.</span><span class="sxs-lookup"><span data-stu-id="8e031-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="8e031-428">Если его нет, выберите **Повторно создать методы** на панели операций, чтобы добавить его.</span><span class="sxs-lookup"><span data-stu-id="8e031-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="8e031-429">Для метода **waveLabelPrinting** установите флажок **Сделать метод повторяемым**.</span><span class="sxs-lookup"><span data-stu-id="8e031-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="8e031-430">Настройка шаблона волны</span><span class="sxs-lookup"><span data-stu-id="8e031-430">Set up a wave template</span></span>

1. <span data-ttu-id="8e031-431">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Шаблоны волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="8e031-432">Выберите шаблон, например **62 Отгрузка по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="8e031-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="8e031-433">На экспресс-вкладке **Методы** переместите метод **Печать этикеток волны** в столбец **Выбранные методы**.</span><span class="sxs-lookup"><span data-stu-id="8e031-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="8e031-434">В столбце **Выбранные методы** назначьте значение **Код шага волны**, например *Коробка*, для метода **Печать этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton*, to the **Wave label printing** method.</span></span> <span data-ttu-id="8e031-435">Дополнительные сведения о кодах шага волны см. в разделе [Коды шагов волны](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8e031-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="8e031-436">Переместите метод **Печать этикеток волны** в столбец **Выбранные методы** второй раз.</span><span class="sxs-lookup"><span data-stu-id="8e031-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="8e031-437">В столбце **Выбранные методы** назначьте другое значение **Код шага волны**, например *Палета*, для второго метода **Печать этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet*, to the second **Wave label printing** method.</span></span> <span data-ttu-id="8e031-438">Дополнительные сведения о кодах шага волны см. в разделе [Коды шагов волны](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8e031-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="8e031-439">Создание трех макетов этикеток волны</span><span class="sxs-lookup"><span data-stu-id="8e031-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="8e031-440">Перейдите в раздел **Управление складом \> Настройка \> Маршрутизация документов \> Печать этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="8e031-441">Создайте запись со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="8e031-442">**Код макета этикетки:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="8e031-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="8e031-443">**Описание:** *Упаковка (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="8e031-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="8e031-444">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8e031-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="8e031-445">В области действий выберите **Параметры строки этикетки волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="8e031-446">Будет открыта страница **Параметры строки этикетки волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="8e031-447">Здесь можно настроить динамическую часть этикетки.</span><span class="sxs-lookup"><span data-stu-id="8e031-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="8e031-448">Добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-449">**Код строки:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="8e031-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="8e031-450">**Имя таблицы строк:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="8e031-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="8e031-451">**Положение начала строки:** *0*</span><span class="sxs-lookup"><span data-stu-id="8e031-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="8e031-452">В этом поле определяется вертикальная позиция, с которой строка будет начинаться на этикетке.</span><span class="sxs-lookup"><span data-stu-id="8e031-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="8e031-453">**Высота строки:** *0*</span><span class="sxs-lookup"><span data-stu-id="8e031-453">**Row height:** *0*</span></span>

        <span data-ttu-id="8e031-454">Это поле определяет высоту каждой строки (в пунктах) в соответствии со стандартом ZPL.</span><span class="sxs-lookup"><span data-stu-id="8e031-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="8e031-455">Высота строки является положительной для горизонтальных этикеток и отрицательных для вертикальных этикеток.</span><span class="sxs-lookup"><span data-stu-id="8e031-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="8e031-456">Поскольку в данном примере имеется только одна строка, можно установить значение равным *0* (нулю).</span><span class="sxs-lookup"><span data-stu-id="8e031-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="8e031-457">**Строк на странице:** *1*</span><span class="sxs-lookup"><span data-stu-id="8e031-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="8e031-458">В этом поле определяется число строк, которое может быть напечатано на каждой этикетке.</span><span class="sxs-lookup"><span data-stu-id="8e031-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="8e031-459">Эта настройка приведет к печати отдельной этикетки ZPL для каждой записи в таблице этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="8e031-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="8e031-460">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8e031-460">Close the page.</span></span>
1. <span data-ttu-id="8e031-461">На панели операций выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="8e031-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="8e031-462">В диалоговом окне редактора запросов на вкладке **Диапазон** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-463">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="8e031-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="8e031-464">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="8e031-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="8e031-465">**Поле:** *Тип работы*</span><span class="sxs-lookup"><span data-stu-id="8e031-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="8e031-466">**Критерии:** *Комплектации*</span><span class="sxs-lookup"><span data-stu-id="8e031-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="8e031-467">Этот запрос гарантирует, что в этикетке будут печататься только строки работа типа "Комплектация", а не строки типа "Размещение".</span><span class="sxs-lookup"><span data-stu-id="8e031-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="8e031-468">Если необходимо распечатать код транспортной накладной, на вкладке **Объединения** выберите таблицу **Строки работ** и присоедините к ней таблицу **Отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="8e031-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="8e031-469">Закройте диалоговое окно редактора запросов.</span><span class="sxs-lookup"><span data-stu-id="8e031-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="8e031-470">На экспресс-вкладке **Макет текста принтера** имеется три раздела для написания кода принтера: **Раздел заголовка**, **Раздел текста** и **Раздел нижнего колонтитула**.</span><span class="sxs-lookup"><span data-stu-id="8e031-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="8e031-471">В разделе **Раздел заголовка** в поле **Заголовок этикетки** введите код для требуемого заголовка.</span><span class="sxs-lookup"><span data-stu-id="8e031-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="8e031-472">Например, при использовании принтеров Zebra можно использовать следующий код.</span><span class="sxs-lookup"><span data-stu-id="8e031-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="8e031-473">В разделе **Раздел текста** в поле **Текст этикетки** введите код ZPL для требуемого текста.</span><span class="sxs-lookup"><span data-stu-id="8e031-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="8e031-474">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="8e031-474">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="8e031-475">В разделе **Раздел текста** в поле **Нижний колонтитул этикетки** введите код ZPL для требуемого нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="8e031-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="8e031-476">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="8e031-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="8e031-477">При этой настройке будет напечатана одна копия каждой этикетки.</span><span class="sxs-lookup"><span data-stu-id="8e031-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="8e031-478">Если требуется больше копий (например, одна копия для каждой из сторон палеты), установите значение **n** для раздела **\^PQn** в нижнем колонтитуле равным требуемому числу копий.</span><span class="sxs-lookup"><span data-stu-id="8e031-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="8e031-479">Например, чтобы напечатать четыре копии каждой этикетки, укажите **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="8e031-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="8e031-480">Первая этикетка готова к использованию.</span><span class="sxs-lookup"><span data-stu-id="8e031-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="8e031-481">Создайте вторую запись макета со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="8e031-482">**Код макета этикетки:** *Палета*</span><span class="sxs-lookup"><span data-stu-id="8e031-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="8e031-483">**Описание:** *Палета*</span><span class="sxs-lookup"><span data-stu-id="8e031-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="8e031-484">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8e031-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="8e031-485">В области действий выберите **Параметры строки этикетки волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="8e031-486">Будет открыта страница **Параметры строки этикетки волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="8e031-487">Здесь можно настроить динамическую часть этикетки.</span><span class="sxs-lookup"><span data-stu-id="8e031-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="8e031-488">Добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-489">**Код строки:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="8e031-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="8e031-490">**Имя таблицы строк:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="8e031-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="8e031-491">**Положение начала строки:** *0*</span><span class="sxs-lookup"><span data-stu-id="8e031-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="8e031-492">В этом поле определяется вертикальная позиция, с которой строка будет начинаться на этикетке.</span><span class="sxs-lookup"><span data-stu-id="8e031-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="8e031-493">**Высота строки:** *0*</span><span class="sxs-lookup"><span data-stu-id="8e031-493">**Row height:** *0*</span></span>

        <span data-ttu-id="8e031-494">Это поле определяет высоту каждой строки (в пунктах) в соответствии со стандартом ZPL.</span><span class="sxs-lookup"><span data-stu-id="8e031-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="8e031-495">Высота строки является положительной для горизонтальных этикеток и отрицательных для вертикальных этикеток.</span><span class="sxs-lookup"><span data-stu-id="8e031-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="8e031-496">Поскольку в данном примере имеется только одна строка, можно установить значение равным *0* (нулю).</span><span class="sxs-lookup"><span data-stu-id="8e031-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="8e031-497">**Строк на странице:** *1*</span><span class="sxs-lookup"><span data-stu-id="8e031-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="8e031-498">В этом поле определяется число строк, которое может быть напечатано на каждой этикетке.</span><span class="sxs-lookup"><span data-stu-id="8e031-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="8e031-499">Эта настройка приводит к печати отдельной этикетки ZPL для каждой записи в таблице этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="8e031-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="8e031-500">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8e031-500">Close the page.</span></span>
1. <span data-ttu-id="8e031-501">На панели операций выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="8e031-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="8e031-502">В диалоговом окне редактора запросов на вкладке **Диапазон** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-503">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="8e031-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="8e031-504">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="8e031-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="8e031-505">**Поле:** *Тип работы*</span><span class="sxs-lookup"><span data-stu-id="8e031-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="8e031-506">**Критерии:** *Комплектации*</span><span class="sxs-lookup"><span data-stu-id="8e031-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="8e031-507">Этот запрос гарантирует, что в этикетке будут печататься только строки работа типа "Комплектация", а не строки типа "Размещение".</span><span class="sxs-lookup"><span data-stu-id="8e031-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="8e031-508">Если необходимо распечатать код транспортной накладной, на вкладке **Объединения** выберите таблицу **Строки работ** и присоедините к ней таблицу **Отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="8e031-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="8e031-509">Закройте диалоговое окно редактора запросов.</span><span class="sxs-lookup"><span data-stu-id="8e031-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="8e031-510">На экспресс-вкладке **Макет текста принтера** имеется три раздела для написания кода принтера: **Раздел заголовка**, **Раздел текста** и **Раздел нижнего колонтитула**.</span><span class="sxs-lookup"><span data-stu-id="8e031-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="8e031-511">В разделе **Раздел заголовка** в поле **Заголовок этикетки** введите код для требуемого заголовка.</span><span class="sxs-lookup"><span data-stu-id="8e031-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="8e031-512">Например, при использовании принтеров Zebra можно использовать следующий код.</span><span class="sxs-lookup"><span data-stu-id="8e031-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="8e031-513">В разделе **Раздел текста** в поле **Текст этикетки** введите код ZPL для требуемого текста.</span><span class="sxs-lookup"><span data-stu-id="8e031-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="8e031-514">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="8e031-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="8e031-515">В разделе **Раздел текста** в поле **Нижний колонтитул этикетки** введите код ZPL для требуемого нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="8e031-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="8e031-516">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="8e031-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="8e031-517">При этой настройке будет напечатана одна копия каждой этикетки.</span><span class="sxs-lookup"><span data-stu-id="8e031-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="8e031-518">Если требуется больше копий (например, одна копия для каждой из сторон палеты), установите значение **n** для раздела **\^PQn** в нижнем колонтитуле равным требуемому числу копий.</span><span class="sxs-lookup"><span data-stu-id="8e031-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="8e031-519">Например, чтобы напечатать четыре копии каждой этикетки, укажите **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="8e031-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="8e031-520">Вторая этикетка готова к использованию.</span><span class="sxs-lookup"><span data-stu-id="8e031-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="8e031-521">Создайте третью запись макета со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="8e031-522">**Код макета этикетки:** *Разделитель*</span><span class="sxs-lookup"><span data-stu-id="8e031-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="8e031-523">**Описание:** *Разделительная этикетка*</span><span class="sxs-lookup"><span data-stu-id="8e031-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="8e031-524">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8e031-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="8e031-525">На экспресс-вкладке **Макет текста принтера** имеется три раздела для написания кода принтера: **Раздел заголовка**, **Раздел текста** и **Раздел нижнего колонтитула**.</span><span class="sxs-lookup"><span data-stu-id="8e031-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="8e031-526">В разделе **Раздел заголовка** в поле **Заголовок этикетки** введите код ZPL для требуемого заголовка.</span><span class="sxs-lookup"><span data-stu-id="8e031-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="8e031-527">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="8e031-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="8e031-528">На этот раз текст не требуется.</span><span class="sxs-lookup"><span data-stu-id="8e031-528">This time, no body is required.</span></span> <span data-ttu-id="8e031-529">Таким образом, просто введите необходимый текст в раздел **Нижний колонтитул**.</span><span class="sxs-lookup"><span data-stu-id="8e031-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="8e031-530">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="8e031-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="8e031-531">Третья этикетка готова к использованию.</span><span class="sxs-lookup"><span data-stu-id="8e031-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8e031-532">Эта третья этикетка представляет собой разделительную этикетку, которая будет использоваться в качестве разделителя для рулонов этикеток.</span><span class="sxs-lookup"><span data-stu-id="8e031-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="8e031-533">Создание двух типов этикеток волны</span><span class="sxs-lookup"><span data-stu-id="8e031-533">Create two wave label types</span></span>

1. <span data-ttu-id="8e031-534">Перейдите в раздел **Управление складом \> Настройка \> Маршрутизация документов \> Типы этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="8e031-535">Создайте запись со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="8e031-536">**Тип этикетки:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="8e031-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="8e031-537">**Описание:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="8e031-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="8e031-538">Создайте вторую запись со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="8e031-539">**Тип этикетки:** *Палета*</span><span class="sxs-lookup"><span data-stu-id="8e031-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="8e031-540">**Описание:** *Палета*</span><span class="sxs-lookup"><span data-stu-id="8e031-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="8e031-541">Настройка групп упорядочения единиц</span><span class="sxs-lookup"><span data-stu-id="8e031-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="8e031-542">Перейдите в раздел **Управление складом \> Настройка \> Склад \> Группы упорядочения единиц**.</span><span class="sxs-lookup"><span data-stu-id="8e031-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="8e031-543">Выберите или создайте группу **шт., коробка, палета**.</span><span class="sxs-lookup"><span data-stu-id="8e031-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="8e031-544">Для строки **Ящик** введите в поле **Тип уровня волны** значение *Упаковка*.</span><span class="sxs-lookup"><span data-stu-id="8e031-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="8e031-545">Для строки **Палета** введите в поле **Тип уровня волны** значение *Палета*.</span><span class="sxs-lookup"><span data-stu-id="8e031-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="8e031-546">Создание шаблонов этикеток волны</span><span class="sxs-lookup"><span data-stu-id="8e031-546">Create wave label templates</span></span>

1. <span data-ttu-id="8e031-547">Перейдите в раздел **Управление складом \> Настройка \> Маршрутизация документов \> Шаблоны этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="8e031-548">Создайте шаблон этикеток со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="8e031-549">**Наименование шаблона этикетки:** *Этикетки для упаковки*</span><span class="sxs-lookup"><span data-stu-id="8e031-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="8e031-550">**Описание:** *Этикетки для упаковки*</span><span class="sxs-lookup"><span data-stu-id="8e031-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="8e031-551">**Код шага волны:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="8e031-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="8e031-552">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="8e031-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="8e031-553">На экспресс-вкладке **Общее** в поле **Тип этикеток волны** выберите значение, например, *Упаковка*.</span><span class="sxs-lookup"><span data-stu-id="8e031-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="8e031-554">На экспресс-вкладке **Сведения шаблона этикетки волны** добавьте строку со следующими настройками:</span><span class="sxs-lookup"><span data-stu-id="8e031-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-555">**Код макета этикетки:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="8e031-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="8e031-556">**Имя принтера:** выберите подходящий принтер ZPL.</span><span class="sxs-lookup"><span data-stu-id="8e031-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="8e031-557">**Выполнение запроса:** *Да* (Этот параметр не является обязательным, но рекомендуется для достижения оптимальной производительности.)</span><span class="sxs-lookup"><span data-stu-id="8e031-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="8e031-558">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8e031-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="8e031-559">Необязательно: если вы настраиваете дизайн этикеток для определенного клиента, необходимо создать запрос, чтобы найти учетную запись клиента.</span><span class="sxs-lookup"><span data-stu-id="8e031-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="8e031-560">На экспресс-вкладке **Сведения шаблона этикетки волны** выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="8e031-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="8e031-561">Затем в диалоговом окне редактора запросов на вкладке **Диапазон** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-562">**Таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="8e031-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="8e031-563">**Производная таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="8e031-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="8e031-564">**Поле:** *Номер учетной записи*</span><span class="sxs-lookup"><span data-stu-id="8e031-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="8e031-565">**Критерии:** введите соответствующий номер учетной записи клиента.</span><span class="sxs-lookup"><span data-stu-id="8e031-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="8e031-566">После завершения нажмите кнопку **OK**, чтобы закрыть диалоговое окно редактора запросов.</span><span class="sxs-lookup"><span data-stu-id="8e031-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="8e031-567">На панели операций выберите **Изменить запрос**, чтобы открыть диалоговое окно редактора запросов для всего шаблона этикетки.</span><span class="sxs-lookup"><span data-stu-id="8e031-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="8e031-568">В диалоговом окне редактора запросов на вкладке **Сортировка** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-569">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="8e031-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="8e031-570">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="8e031-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="8e031-571">**Поле:** *Код строки загрузки ссылки (ИД записи)*</span><span class="sxs-lookup"><span data-stu-id="8e031-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="8e031-572">**Направление поиска:** *Восходящее*</span><span class="sxs-lookup"><span data-stu-id="8e031-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="8e031-573">Добавьте вторую строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-574">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="8e031-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="8e031-575">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="8e031-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="8e031-576">**Поле:** *Код отгрузки*</span><span class="sxs-lookup"><span data-stu-id="8e031-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="8e031-577">**Направление поиска:** *Восходящее*</span><span class="sxs-lookup"><span data-stu-id="8e031-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="8e031-578">Выберите **ОК**, чтобы закрыть диалоговое окно редактора запроса.</span><span class="sxs-lookup"><span data-stu-id="8e031-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="8e031-579">В окне сообщение будет предложено подтвердить операцию сброса группы.</span><span class="sxs-lookup"><span data-stu-id="8e031-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="8e031-580">Выберите **Да** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="8e031-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="8e031-581">В области действий выберите **Группа шаблонов этикеток волн**.</span><span class="sxs-lookup"><span data-stu-id="8e031-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="8e031-582">В диалоговом окне **Группа шаблонов этикеток волны** для строки, в которой для поля **Имя поля ссылки** указано значение *Код отгрузки*, установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8e031-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="8e031-583">**Печатать разделительную этикетку:** установите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="8e031-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="8e031-584">**Код макета этикетки:** выберите разделительную этикетку.</span><span class="sxs-lookup"><span data-stu-id="8e031-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="8e031-585">(Например, выберите макет этикетки *Разделитель*, созданной ранее в этом сценарии.)</span><span class="sxs-lookup"><span data-stu-id="8e031-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="8e031-586">**Имя принтера:** выберите принтер для разделительной этикетки.</span><span class="sxs-lookup"><span data-stu-id="8e031-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="8e031-587">(Обычно для задачи разделения рулонов этикеток следует выбирать тот же принтер, что и выбранный на экспресс-вкладка **Сведения о шаблоне этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="8e031-588">Однако возможны и другие сценарии.)</span><span class="sxs-lookup"><span data-stu-id="8e031-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="8e031-589">Для строки, в которой поле **Имя поля ссылки** имеет значение *Код строки загрузки ссылки*, установите флажок **Код сборки этикетки**.</span><span class="sxs-lookup"><span data-stu-id="8e031-589">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8e031-590">Эта настройка создаст одну последовательность этикеток ("Упаковка 1 из X") для каждой строки загрузки в волне, независимо от настройки группировки работ.</span><span class="sxs-lookup"><span data-stu-id="8e031-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="8e031-591">Эта последовательность этикеток может быть распечатана в макете этикеток.</span><span class="sxs-lookup"><span data-stu-id="8e031-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="8e031-592">Кроме того, этикетки для различных отгрузок будут отделены выбранной разделительной этикеткой.</span><span class="sxs-lookup"><span data-stu-id="8e031-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="8e031-593">Выберите **ОК**, чтобы закрыть диалоговое окно **Группа шаблонов этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="8e031-594">Создайте второй шаблон этикеток со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="8e031-595">**Наименование шаблона этикетки:** *Этикетки для палет*</span><span class="sxs-lookup"><span data-stu-id="8e031-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="8e031-596">**Описание:** *Этикетки для палет*</span><span class="sxs-lookup"><span data-stu-id="8e031-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="8e031-597">**Код шага волны:** *Палета*</span><span class="sxs-lookup"><span data-stu-id="8e031-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="8e031-598">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="8e031-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="8e031-599">На экспресс-вкладке **Общее** в поле **Тип этикеток волны** выберите значение, например, *Палета*.</span><span class="sxs-lookup"><span data-stu-id="8e031-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="8e031-600">На экспресс-вкладке **Сведения шаблона этикетки волны** добавьте строку со следующими настройками:</span><span class="sxs-lookup"><span data-stu-id="8e031-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-601">**Код макета этикетки:** *Палета*</span><span class="sxs-lookup"><span data-stu-id="8e031-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="8e031-602">**Имя принтера:** выберите подходящий принтер ZPL.</span><span class="sxs-lookup"><span data-stu-id="8e031-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="8e031-603">**Выполнение запроса:** *Да* (Этот параметр не является обязательным, но рекомендуется для достижения оптимальной производительности.)</span><span class="sxs-lookup"><span data-stu-id="8e031-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="8e031-604">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8e031-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="8e031-605">Необязательно: если вы настраиваете дизайн этикеток для определенного клиента, необходимо создать запрос, чтобы найти учетную запись клиента.</span><span class="sxs-lookup"><span data-stu-id="8e031-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="8e031-606">На экспресс-вкладке **Сведения шаблона этикетки волны** выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="8e031-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="8e031-607">Затем в диалоговом окне редактора запросов на вкладке **Диапазон** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-608">**Таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="8e031-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="8e031-609">**Производная таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="8e031-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="8e031-610">**Поле:** *Номер учетной записи*</span><span class="sxs-lookup"><span data-stu-id="8e031-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="8e031-611">**Критерии:** введите соответствующий номер учетной записи клиента.</span><span class="sxs-lookup"><span data-stu-id="8e031-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="8e031-612">После завершения нажмите кнопку **OK**, чтобы закрыть диалоговое окно редактора запросов.</span><span class="sxs-lookup"><span data-stu-id="8e031-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="8e031-613">На панели операций выберите **Изменить запрос**, чтобы открыть диалоговое окно редактора запросов для всего шаблона этикетки.</span><span class="sxs-lookup"><span data-stu-id="8e031-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="8e031-614">В диалоговом окне редактора запросов на вкладке **Сортировка** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-615">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="8e031-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="8e031-616">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="8e031-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="8e031-617">**Поле:** *Код строки загрузки ссылки (ИД записи)*</span><span class="sxs-lookup"><span data-stu-id="8e031-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="8e031-618">**Направление поиска:** *Восходящее*</span><span class="sxs-lookup"><span data-stu-id="8e031-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="8e031-619">Добавьте вторую строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="8e031-620">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="8e031-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="8e031-621">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="8e031-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="8e031-622">**Поле:** *Код отгрузки*</span><span class="sxs-lookup"><span data-stu-id="8e031-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="8e031-623">**Направление поиска:** *Восходящее*</span><span class="sxs-lookup"><span data-stu-id="8e031-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="8e031-624">Выберите **ОК**, чтобы закрыть диалоговое окно редактора запроса.</span><span class="sxs-lookup"><span data-stu-id="8e031-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="8e031-625">В окне сообщение будет предложено подтвердить операцию сброса группы.</span><span class="sxs-lookup"><span data-stu-id="8e031-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="8e031-626">Выберите **Да** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="8e031-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="8e031-627">В области действий выберите **Группа шаблонов этикеток волн**.</span><span class="sxs-lookup"><span data-stu-id="8e031-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="8e031-628">В диалоговом окне **Группа шаблонов этикеток волны** для строки, в которой для поля **Имя поля ссылки** указано значение *Код отгрузки*, установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8e031-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="8e031-629">**Печатать разделительную этикетку:** установите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="8e031-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="8e031-630">**Код макета этикетки:** выберите разделительную этикетку.</span><span class="sxs-lookup"><span data-stu-id="8e031-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="8e031-631">(Например, выберите макет этикетки *Разделитель*, созданной ранее в этом сценарии.)</span><span class="sxs-lookup"><span data-stu-id="8e031-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="8e031-632">**Имя принтера:** выберите принтер для разделительной этикетки.</span><span class="sxs-lookup"><span data-stu-id="8e031-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="8e031-633">(Обычно для задачи разделения рулонов этикеток следует выбирать тот же принтер, что и выбранный на экспресс-вкладка **Сведения о шаблоне этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="8e031-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="8e031-634">Однако возможны и другие сценарии.)</span><span class="sxs-lookup"><span data-stu-id="8e031-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="8e031-635">Для строки, в которой поле **Имя поля ссылки** имеет значение *Код строки загрузки ссылки*, установите флажок **Код сборки этикетки**.</span><span class="sxs-lookup"><span data-stu-id="8e031-635">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8e031-636">Эта настройка создаст одну последовательность этикеток ("Упаковка 1 из X") для каждой строки загрузки в волне, независимо от настройки группировки работ.</span><span class="sxs-lookup"><span data-stu-id="8e031-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="8e031-637">Эта последовательность этикеток может быть распечатана в макете этикеток.</span><span class="sxs-lookup"><span data-stu-id="8e031-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="8e031-638">Кроме того, этикетки для различных отгрузок будут отделены выбранной разделительной этикеткой.</span><span class="sxs-lookup"><span data-stu-id="8e031-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="8e031-639">Настройка расширений номерной серии</span><span class="sxs-lookup"><span data-stu-id="8e031-639">Configure number sequence extensions</span></span>

<span data-ttu-id="8e031-640">Расширения номерных серий управляют GS1-соответствием для определенных номерных серий.</span><span class="sxs-lookup"><span data-stu-id="8e031-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="8e031-641">Эта настройка не является обязательной для текущего сценария.</span><span class="sxs-lookup"><span data-stu-id="8e031-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="8e031-642">Дополнительные сведения и инструкции по настройке см. в разделе [Настройка расширений номерных серий](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="8e031-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="8e031-643">Создание заказа на продажу и выпуск его на склад</span><span class="sxs-lookup"><span data-stu-id="8e031-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="8e031-644">Перейдите в раздел **Продажи и маркетинг \> Заказ на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="8e031-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="8e031-645">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="8e031-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="8e031-646">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="8e031-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8e031-647">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="8e031-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="8e031-648">Добавьте две строки заказа на продажу:</span><span class="sxs-lookup"><span data-stu-id="8e031-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="8e031-649">Строка заказа на продажу 1:</span><span class="sxs-lookup"><span data-stu-id="8e031-649">Sales order line 1:</span></span>

        - <span data-ttu-id="8e031-650">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="8e031-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="8e031-651">**Количество:** *9024*</span><span class="sxs-lookup"><span data-stu-id="8e031-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="8e031-652">**Единица измерения:** *шт.* (9024 шт. = 376 коробок = 47 палет)</span><span class="sxs-lookup"><span data-stu-id="8e031-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="8e031-653">Строка заказа на продажу 2:</span><span class="sxs-lookup"><span data-stu-id="8e031-653">Sales order line 2:</span></span>

        - <span data-ttu-id="8e031-654">**Код номенклатуры:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="8e031-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="8e031-655">**Количество:** *9016*</span><span class="sxs-lookup"><span data-stu-id="8e031-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="8e031-656">**Единица измерения:** *шт.* (9016 шт. = 322 коробки = 46 палет)</span><span class="sxs-lookup"><span data-stu-id="8e031-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="8e031-657">Представленные здесь номенклатуры и количества являются только примерами.</span><span class="sxs-lookup"><span data-stu-id="8e031-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="8e031-658">Они должны использовать ранее определенную группу последовательности единиц измерения, подходящие преобразования единиц измерения из *шт.* в *коробки* и в *палеты*, для которых должны быть запасы на складе *62*.</span><span class="sxs-lookup"><span data-stu-id="8e031-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="8e031-659">Дополнительные сведения см. в разделе [Единицы измерения и политики хранения](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="8e031-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="8e031-660">Выберите строку заказа на продажу 1.</span><span class="sxs-lookup"><span data-stu-id="8e031-660">Select sales order line 1.</span></span> <span data-ttu-id="8e031-661">Затем в разделе **Строка заказа на продажу** в меню **Запасы** выберите **Резервирования**.</span><span class="sxs-lookup"><span data-stu-id="8e031-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="8e031-662">На странице **Резервирование** в области действий выберите **Зарезервировать лот**, затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8e031-662">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="8e031-663">Повторите шаги 4 и 5 для строки заказа на продажу 2.</span><span class="sxs-lookup"><span data-stu-id="8e031-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="8e031-664">На панели операций на вкладке **Склад** выберите вариант **Выпустить на склад**.</span><span class="sxs-lookup"><span data-stu-id="8e031-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="8e031-665">Имеют место следующие события:</span><span class="sxs-lookup"><span data-stu-id="8e031-665">The following events occur:</span></span> 

    - <span data-ttu-id="8e031-666">Система обрабатывает созданную отгрузку, используя шаблон, содержащий шаг печати этикеток.</span><span class="sxs-lookup"><span data-stu-id="8e031-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="8e031-667">Макет этикетки будет использоваться для определения формата этикетки, а результатом будет этикетка, которая печатается на принтере, выбранном в шаблоне этикетки.</span><span class="sxs-lookup"><span data-stu-id="8e031-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="8e031-668">Этикетки волны создаются и печатаются.</span><span class="sxs-lookup"><span data-stu-id="8e031-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="8e031-669">Число этикеток равно числу коробок (в данном примере 376 этикеток коробок для строки 1, 322 этикетки коробок для строки 2, 47 этикеток палет для строки 1, 47 этикеток палет для строки 2 и две разделительных этикетки с кодом отгрузки).</span><span class="sxs-lookup"><span data-stu-id="8e031-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="8e031-670">Для отгрузок создается новый код транспортной накладной.</span><span class="sxs-lookup"><span data-stu-id="8e031-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="8e031-671">Если настроены расширения номерной серии, коды этикеток волны будут соответствовать формату номера **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="8e031-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="8e031-672">На следующих страницах можно просматривать и перепечатывать этикетки волны:</span><span class="sxs-lookup"><span data-stu-id="8e031-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="8e031-673">Все отгрузки \> Сведения об отгрузках</span><span class="sxs-lookup"><span data-stu-id="8e031-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="8e031-674">Все загрузки \> Сведения о загрузках</span><span class="sxs-lookup"><span data-stu-id="8e031-674">All loads \> Load details</span></span>
- <span data-ttu-id="8e031-675">Все волны</span><span class="sxs-lookup"><span data-stu-id="8e031-675">All waves</span></span>
- <span data-ttu-id="8e031-676">Этикетки волны</span><span class="sxs-lookup"><span data-stu-id="8e031-676">Wave labels</span></span>
- <span data-ttu-id="8e031-677">История этикеток волны</span><span class="sxs-lookup"><span data-stu-id="8e031-677">Wave label history</span></span>

<span data-ttu-id="8e031-678">Для большинства из этих страниц можно найти соответствующую функцию, выбрав **Этикетки волны** в группе **Связанные сведения** на вкладке **Отгрузки** в области действий.</span><span class="sxs-lookup"><span data-stu-id="8e031-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>
