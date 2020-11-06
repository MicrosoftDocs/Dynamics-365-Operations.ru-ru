---
title: Настройка и использование печати этикеток волны
description: В этой теме описывается печать этикеток волны и объясняется, как ее настроить.
author: GarmMSFT
manager: PJacobse
ms.date: 05/01/2020
ms.topic: configure-wave-label-printing
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 1f51ed9f05caede3d4f320ddb6b705e67df9aa1f
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016964"
---
# <a name="set-up-and-use-wave-label-printing"></a><span data-ttu-id="81c5f-103">Настройка и использование печати этикеток волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-103">Set up and use wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81c5f-104">Печать этикеток волны предлагает альтернативный подход к печати этикеток с помощью нового метода шага волны, который позволяет создавать и печатать этикетки непосредственно из шаблона волны при выполнении волны.</span><span class="sxs-lookup"><span data-stu-id="81c5f-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="81c5f-105">Поэтому этикетки будут доступны до того, когда работники запускают заказ на работу на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="81c5f-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="81c5f-106">Работники могут затем закрепить требуемые этикетки при комплектации, а не после комплектации.</span><span class="sxs-lookup"><span data-stu-id="81c5f-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="81c5f-107">В функции печати этикеток волны используется язык программирования Zebra (ZPL) для создания макета этикеток.</span><span class="sxs-lookup"><span data-stu-id="81c5f-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="81c5f-108">Макет этикетки разделяется на три раздела (верхний колонтитул, основной текст и нижний колонтитул), чтобы иметь возможность использовать этикетки с повторяющейся структурой.</span><span class="sxs-lookup"><span data-stu-id="81c5f-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="81c5f-109">Шаблоны этикеток волны указывают системе, какую структуру наклеек использовать.</span><span class="sxs-lookup"><span data-stu-id="81c5f-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="81c5f-110">Пользователи могут указать используемый принтер.</span><span class="sxs-lookup"><span data-stu-id="81c5f-110">Users can specify which printer is used.</span></span> <span data-ttu-id="81c5f-111">Они также могут печатать этикетки на нескольких принтерах одновременно, по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="81c5f-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="81c5f-112">На странице **История этикеток волны** отображается запись всех этикеток, которые были созданы с помощью этой настройки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="81c5f-113">Можно печатать этикетки и разбирать их на основе заголовков работ, можно печатать этикетки-разделители для каждого заголовка работы, а также печатать этикетки содержимого контейнеров, этикетки коробок и другие похожие этикетки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="81c5f-114">Эта функция не заменяет существующие функции печати этикеток на основе маршрутизации документов.</span><span class="sxs-lookup"><span data-stu-id="81c5f-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="81c5f-115">Печать этикеток волны предлагает следующие усовершенствования:</span><span class="sxs-lookup"><span data-stu-id="81c5f-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="81c5f-116">Печать этикеток в соответствии с количеством упаковок в одной строке работы без использования контейнеризации.</span><span class="sxs-lookup"><span data-stu-id="81c5f-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="81c5f-117">("Упаковка" — это единица измерения, которая указана в строках группы упорядочения единиц.)</span><span class="sxs-lookup"><span data-stu-id="81c5f-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="81c5f-118">Печать нескольких различных последовательностей этикеток (например, этикеток коробок и палет).</span><span class="sxs-lookup"><span data-stu-id="81c5f-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="81c5f-119">Включение перечисления этикеток (например, 1/124, 2/124,... 124/124) и указание диапазона перечисления (например, строка работы, строка загрузки или отгрузка).</span><span class="sxs-lookup"><span data-stu-id="81c5f-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="81c5f-120">Создание и печать кода транспортной накладной на этикетках перед созданием транспортной накладной.</span><span class="sxs-lookup"><span data-stu-id="81c5f-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="81c5f-121">Создание уникального порядкового кода контейнера отгрузки (SSCC) для каждой упаковки и включение его в каждую этикетку.</span><span class="sxs-lookup"><span data-stu-id="81c5f-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="81c5f-122">Создание GS1-совместимых номерных серий для кодов транспортных накладных и кодов SSCC.</span><span class="sxs-lookup"><span data-stu-id="81c5f-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="81c5f-123">Повторная печать этикеток с мобильных устройств и с расширенного клиента.</span><span class="sxs-lookup"><span data-stu-id="81c5f-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="81c5f-124">Аннулирование этикеток (например, в случае недостатка для комплектации) и их повторная печать.</span><span class="sxs-lookup"><span data-stu-id="81c5f-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="81c5f-125">Очистите журнал этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="81c5f-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="81c5f-126">Улучшения в макетах маршрутизации документов являются общими для макетов маршрутизации документов и макетов этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="81c5f-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="81c5f-127">(Дополнительные сведения см. в разделе [Макет маршрутизации документов для грузомест](../warehousing/document-routing-layout-for-license-plates.md).)</span><span class="sxs-lookup"><span data-stu-id="81c5f-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="81c5f-128">Эти улучшения повышают эффективность маркировки упаковок перед погрузкой на палеты.</span><span class="sxs-lookup"><span data-stu-id="81c5f-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="81c5f-129">Они особенно полезны компаниям, которые осуществляют отгрузку крупным розничным продавцам, которые автоматически подтверждают приемку по заказам путем сканирования каждой упаковки отдельно.</span><span class="sxs-lookup"><span data-stu-id="81c5f-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="81c5f-130">Сценарии конфигурации, описанные в этом разделе, можно реализовать отдельно или в сочетании, в зависимости от бизнес-требований.</span><span class="sxs-lookup"><span data-stu-id="81c5f-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="81c5f-131">Можно разработать несколько шаблонов этикеток волны, которые работают последовательно (как показано в сценарии 3).</span><span class="sxs-lookup"><span data-stu-id="81c5f-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="81c5f-132">Например, можно использовать сценарий 1 для печати этикеток и сценарий 2 для печати этикеток палет (если размер и компоновка палет в запасах различаются).</span><span class="sxs-lookup"><span data-stu-id="81c5f-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="81c5f-133">Включение функции печати этикеток волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="81c5f-134">Прежде чем использовать функцию *Печать этикеток волны* , она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="81c5f-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="81c5f-135">Администраторы могут использовать рабочую область [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="81c5f-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="81c5f-136">В этом случае функция указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="81c5f-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="81c5f-137">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="81c5f-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="81c5f-138">**Имя функции:** *Печать этикеток волны*</span><span class="sxs-lookup"><span data-stu-id="81c5f-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="81c5f-139">Случай 1. Печать этикеток волны, в которой создается одна этикетка волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="81c5f-140">В этом сценарии показано, как компания может печатать этикетки отгрузки для крупного розничного продавца, который автоматически подтверждает приемку заказов путем сканирования каждой упаковки отдельно.</span><span class="sxs-lookup"><span data-stu-id="81c5f-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="81c5f-141">В этом сценарии показан сквозной поток.</span><span class="sxs-lookup"><span data-stu-id="81c5f-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="81c5f-142">Сделать демонстрационные данные доступными</span><span class="sxs-lookup"><span data-stu-id="81c5f-142">Make demo data available</span></span>

<span data-ttu-id="81c5f-143">Для выполнения этого сценария необходимо установить демонстрационные данные, а также необходимо выбрать юридическое лицо **USMF**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="81c5f-144">Убедитесь, что доступен метод этикеток волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="81c5f-145">Возможно, придется повторно создать методы обработки волны, чтобы сделать доступным метод печати этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="81c5f-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="81c5f-146">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Методы обработки волн**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="81c5f-147">Убедитесь, что **waveLabelPrinting** есть в списке.</span><span class="sxs-lookup"><span data-stu-id="81c5f-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="81c5f-148">Если его нет, выберите **Повторно создать методы** на панели операций, чтобы добавить его.</span><span class="sxs-lookup"><span data-stu-id="81c5f-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="81c5f-149">Настройка шаблона волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-149">Configure a wave template</span></span>

<span data-ttu-id="81c5f-150">Шаблоны волн позволяют связывать отдельные экземпляры методов волны с соответствующим шаблоном этикетки волны.</span><span class="sxs-lookup"><span data-stu-id="81c5f-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="81c5f-151">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Шаблоны волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="81c5f-152">Выберите шаблон, например **62 Отгрузка по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="81c5f-153">На экспресс-вкладке **Методы** переместите метод **Печать этикеток волны** в столбец **Выбранные методы**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="81c5f-154">В столбце **Выбранные методы** выберите метод **Печать этикеток волны** и задайте для его поля **Код шага волны** значение *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="81c5f-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="81c5f-155">Дополнительные сведения о кодах шага волны см. в разделе [Коды шагов волны](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="81c5f-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="81c5f-156">Создание макета этикеток волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-156">Create a wave label layout</span></span>

<span data-ttu-id="81c5f-157">Макет этикетки определяет, какая информация печатается на этикетке и как она была размещается. Здесь вводится код ZPL, который отправляется на принтер.</span><span class="sxs-lookup"><span data-stu-id="81c5f-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="81c5f-158">Перейдите в раздел **Управление складом \> Настройка \> Маршрутизация документов \> Печать этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="81c5f-159">Создайте запись со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-160">**Код макета этикетки:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="81c5f-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="81c5f-161">**Описание:** *Упаковка (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="81c5f-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="81c5f-162">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="81c5f-163">В области действий выберите **Параметры строки этикетки волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="81c5f-164">Будет открыта страница **Параметры строки этикетки волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="81c5f-165">Здесь можно настроить динамическую часть этикетки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="81c5f-166">Добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-167">**Код строки:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="81c5f-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="81c5f-168">**Имя таблицы строк:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="81c5f-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="81c5f-169">**Положение начала строки:** *0*</span><span class="sxs-lookup"><span data-stu-id="81c5f-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="81c5f-170">В этом поле определяется вертикальная позиция, с которой строка будет начинаться на этикетке.</span><span class="sxs-lookup"><span data-stu-id="81c5f-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="81c5f-171">**Высота строки:** *0*</span><span class="sxs-lookup"><span data-stu-id="81c5f-171">**Row height:** *0*</span></span>

        <span data-ttu-id="81c5f-172">Это поле определяет высоту каждой строки (в пунктах) в соответствии со стандартом ZPL.</span><span class="sxs-lookup"><span data-stu-id="81c5f-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="81c5f-173">Высота строки является положительной для горизонтальных этикеток и отрицательных для вертикальных этикеток.</span><span class="sxs-lookup"><span data-stu-id="81c5f-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="81c5f-174">Поскольку в данном примере имеется только одна строка, можно установить значение равным *0* (нулю).</span><span class="sxs-lookup"><span data-stu-id="81c5f-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="81c5f-175">**Строк на странице:** *1*</span><span class="sxs-lookup"><span data-stu-id="81c5f-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="81c5f-176">В этом поле определяется число строк, которое может быть напечатано на каждой этикетке.</span><span class="sxs-lookup"><span data-stu-id="81c5f-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="81c5f-177">Эта настройка приведет к печати отдельной этикетки ZPL для каждой записи в таблице этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="81c5f-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="81c5f-178">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="81c5f-178">Close the page.</span></span>
1. <span data-ttu-id="81c5f-179">На панели операций выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="81c5f-180">В диалоговом окне редактора запросов на вкладке **Диапазон** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-181">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="81c5f-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="81c5f-182">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="81c5f-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="81c5f-183">**Поле:** *Тип работы*</span><span class="sxs-lookup"><span data-stu-id="81c5f-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="81c5f-184">**Критерии:** *Комплектации*</span><span class="sxs-lookup"><span data-stu-id="81c5f-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="81c5f-185">Этот запрос гарантирует, что в этикетке будут печататься только строки работа типа "Комплектация", а не строки типа "Размещение".</span><span class="sxs-lookup"><span data-stu-id="81c5f-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="81c5f-186">Если необходимо распечатать код транспортной накладной, на вкладке **Объединения** выберите таблицу **Строки работ** и присоедините к ней таблицу **Отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="81c5f-187">Закройте диалоговое окно редактора запросов.</span><span class="sxs-lookup"><span data-stu-id="81c5f-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="81c5f-188">На экспресс-вкладке **Макет текста принтера** имеется три раздела для написания кода принтера: **Раздел заголовка** , **Раздел текста** и **Раздел нижнего колонтитула**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="81c5f-189">В разделе **Раздел заголовка** в поле **Заголовок этикетки** введите код для требуемого заголовка.</span><span class="sxs-lookup"><span data-stu-id="81c5f-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="81c5f-190">Например, при использовании принтеров Zebra можно использовать следующий код.</span><span class="sxs-lookup"><span data-stu-id="81c5f-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

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

1. <span data-ttu-id="81c5f-191">В разделе **Раздел текста** в поле **Текст этикетки** введите код ZPL для требуемого текста.</span><span class="sxs-lookup"><span data-stu-id="81c5f-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="81c5f-192">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="81c5f-192">Here is an example.</span></span>

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

1. <span data-ttu-id="81c5f-193">В разделе **Раздел текста** в поле **Нижний колонтитул этикетки** введите код ZPL для требуемого нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="81c5f-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="81c5f-194">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="81c5f-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="81c5f-195">При этой настройке будет напечатана одна копия каждой этикетки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="81c5f-196">Если требуется больше копий (например, одна копия для каждой из сторон палеты), установите значение **n** для раздела **\^PQn** в нижнем колонтитуле равным требуемому числу копий.</span><span class="sxs-lookup"><span data-stu-id="81c5f-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="81c5f-197">Например, чтобы напечатать четыре копии каждой этикетки, укажите **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="81c5f-198">Теперь этикетка готова к использованию.</span><span class="sxs-lookup"><span data-stu-id="81c5f-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="81c5f-199">Создание типа этикеток волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-199">Create a wave label type</span></span>

<span data-ttu-id="81c5f-200">Типы этикеток волн используются для связывания шаблонов этикеток волн с единицей в строках группы последовательностей единиц.</span><span class="sxs-lookup"><span data-stu-id="81c5f-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="81c5f-201">Перейдите в раздел **Управление складом \> Настройка \> Маршрутизация документов \> Типы этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="81c5f-202">Добавьте тип этикетки волны со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-203">**Тип этикетки:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="81c5f-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="81c5f-204">**Описание:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="81c5f-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="81c5f-205">Настройка групп упорядочения единиц</span><span class="sxs-lookup"><span data-stu-id="81c5f-205">Set up unit sequence groups</span></span>

<span data-ttu-id="81c5f-206">Затем настройте группу упорядочения единиц для типа этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="81c5f-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="81c5f-207">Перейдите в раздел **Управление складом \> Настройка \> Склад \> Группы упорядочения единиц**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="81c5f-208">Выберите группу **штука, ящик, палета**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="81c5f-209">Для строки **Ящик** введите в поле **Тип уровня волны** значение *Упаковка*.</span><span class="sxs-lookup"><span data-stu-id="81c5f-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="81c5f-210">Создание шаблона этикеток волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-210">Create a wave label template</span></span>

<span data-ttu-id="81c5f-211">Затем создайте шаблон этикетки волны для типа этикеток волн.</span><span class="sxs-lookup"><span data-stu-id="81c5f-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="81c5f-212">Перейдите в раздел **Управление складом \> Настройка \> Маршрутизация документов \> Шаблоны этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="81c5f-213">Добавьте шаблон этикетки волны, затем задайте следующие значения в заголовке:</span><span class="sxs-lookup"><span data-stu-id="81c5f-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="81c5f-214">**Наименование шаблона этикетки:** *Этикетки для упаковки*</span><span class="sxs-lookup"><span data-stu-id="81c5f-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="81c5f-215">**Описание:** *Этикетки для упаковки*</span><span class="sxs-lookup"><span data-stu-id="81c5f-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="81c5f-216">**Код шага волны:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="81c5f-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="81c5f-217">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="81c5f-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="81c5f-218">На экспресс-вкладке **Общие** задайте в поле **Тип этикетки волны** значение *Упаковка*.</span><span class="sxs-lookup"><span data-stu-id="81c5f-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="81c5f-219">На экспресс-вкладке **Сведения шаблона этикетки волны** добавьте новую строку со следующими настройками:</span><span class="sxs-lookup"><span data-stu-id="81c5f-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-220">**Код макета этикетки:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="81c5f-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="81c5f-221">**Имя принтера:** выберите подходящий принтер ZPL.</span><span class="sxs-lookup"><span data-stu-id="81c5f-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="81c5f-222">**Выполнение запроса:** *Да* (Этот параметр не является обязательным, но рекомендуется для достижения оптимальной производительности.)</span><span class="sxs-lookup"><span data-stu-id="81c5f-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="81c5f-223">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="81c5f-224">Необязательно: если вы настраиваете дизайн этикеток для определенного клиента, необходимо создать запрос, чтобы найти учетную запись клиента.</span><span class="sxs-lookup"><span data-stu-id="81c5f-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="81c5f-225">На экспресс-вкладке **Сведения шаблона этикетки волны** выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="81c5f-226">Затем в диалоговом окне редактора запросов на вкладке **Диапазон** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-227">**Таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="81c5f-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="81c5f-228">**Производная таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="81c5f-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="81c5f-229">**Поле:** *Номер учетной записи*</span><span class="sxs-lookup"><span data-stu-id="81c5f-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="81c5f-230">**Критерии:** введите соответствующий номер учетной записи клиента.</span><span class="sxs-lookup"><span data-stu-id="81c5f-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="81c5f-231">После завершения нажмите кнопку **OK** , чтобы закрыть диалоговое окно редактора запросов.</span><span class="sxs-lookup"><span data-stu-id="81c5f-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="81c5f-232">На панели операций выберите **Изменить запрос** , чтобы открыть диалоговое окно редактора запросов для всего шаблона этикетки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="81c5f-233">В диалоговом окне редактора запросов на вкладке **Сортировка** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-234">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="81c5f-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="81c5f-235">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="81c5f-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="81c5f-236">**Поле:** *Код строки загрузки ссылки (ИД записи)*</span><span class="sxs-lookup"><span data-stu-id="81c5f-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="81c5f-237">**Направление поиска:** *Восходящее*</span><span class="sxs-lookup"><span data-stu-id="81c5f-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="81c5f-238">Выберите **ОК** , чтобы закрыть диалоговое окно редактора запроса.</span><span class="sxs-lookup"><span data-stu-id="81c5f-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="81c5f-239">В окне сообщение будет предложено подтвердить операцию сброса группы.</span><span class="sxs-lookup"><span data-stu-id="81c5f-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="81c5f-240">Выберите **Да** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="81c5f-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="81c5f-241">В области действий выберите **Группа шаблонов этикеток волн**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="81c5f-242">В диалоговом окне **Группа шаблонов этикеток волн** выберите строку, в которой поле **Имя поля ссылки** имеет значение *Код строки загрузки ссылки* , затем установите флажок **Код сборки этикетки** для этой строки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id* , and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="81c5f-243">Эта настройка создаст одну последовательность этикеток ("Упаковка 1 из X") для каждой строки загрузки в волне, независимо от настройки группировки работ.</span><span class="sxs-lookup"><span data-stu-id="81c5f-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="81c5f-244">Эта последовательность этикеток может быть распечатана в макете этикеток.</span><span class="sxs-lookup"><span data-stu-id="81c5f-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="81c5f-245">Настройка расширений номерной серии</span><span class="sxs-lookup"><span data-stu-id="81c5f-245">Configure number sequence extensions</span></span>

<span data-ttu-id="81c5f-246">Расширения номерных серий управляют GS1-соответствием для определенных номерных серий.</span><span class="sxs-lookup"><span data-stu-id="81c5f-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="81c5f-247">Эта настройка не является обязательной для текущего сценария.</span><span class="sxs-lookup"><span data-stu-id="81c5f-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="81c5f-248">Дополнительные сведения и инструкции по настройке см. в разделе [Настройка расширений номерных серий](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="81c5f-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="81c5f-249">Создание заказа на продажу и выпуск его на склад</span><span class="sxs-lookup"><span data-stu-id="81c5f-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="81c5f-250">Перейдите в раздел **Продажи и маркетинг \> Заказ на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="81c5f-251">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-252">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="81c5f-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="81c5f-253">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="81c5f-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="81c5f-254">Добавьте две строки заказа на продажу со следующими настройками:</span><span class="sxs-lookup"><span data-stu-id="81c5f-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="81c5f-255">Строка заказа на продажу 1:</span><span class="sxs-lookup"><span data-stu-id="81c5f-255">Sales order line 1:</span></span>

        - <span data-ttu-id="81c5f-256">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="81c5f-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="81c5f-257">**Количество:** *9024*</span><span class="sxs-lookup"><span data-stu-id="81c5f-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="81c5f-258">**Единица измерения:** *шт.* (9024 шт. = 376 коробок = 47 палет)</span><span class="sxs-lookup"><span data-stu-id="81c5f-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="81c5f-259">Строка заказа на продажу 2:</span><span class="sxs-lookup"><span data-stu-id="81c5f-259">Sales order line 2:</span></span>

        - <span data-ttu-id="81c5f-260">**Код номенклатуры:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="81c5f-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="81c5f-261">**Количество:** *9016*</span><span class="sxs-lookup"><span data-stu-id="81c5f-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="81c5f-262">**Единица измерения:** *шт.* (9016 шт. = 322 коробки = 46 палет)</span><span class="sxs-lookup"><span data-stu-id="81c5f-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="81c5f-263">Представленные здесь номенклатуры и количества являются только примерами.</span><span class="sxs-lookup"><span data-stu-id="81c5f-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="81c5f-264">Они должны использовать ранее определенную группу последовательности единиц измерения, подходящие преобразования единиц измерения из *шт.* в *коробки* и в *палеты* , для которых должны быть запасы на складе *62*.</span><span class="sxs-lookup"><span data-stu-id="81c5f-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="81c5f-265">Дополнительные сведения см. в разделе [Единицы измерения и политики хранения](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="81c5f-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="81c5f-266">Выберите строку заказа на продажу 1.</span><span class="sxs-lookup"><span data-stu-id="81c5f-266">Select sales order line 1.</span></span> <span data-ttu-id="81c5f-267">Затем в разделе **Строка заказа на продажу** в меню **Запасы** выберите **Резервирования**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="81c5f-268">На странице **Резервирование** в области действий выберите **Зарезервировать лот** , затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="81c5f-268">On the **Reservation** page, on the Action Pane, select **Reserve lot** , and then close the page.</span></span>
1. <span data-ttu-id="81c5f-269">Повторите шаги 4 и 5 для строки заказа на продажу 2.</span><span class="sxs-lookup"><span data-stu-id="81c5f-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="81c5f-270">На панели операций на вкладке **Склад** выберите вариант **Выпустить на склад**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="81c5f-271">Имеют место следующие события:</span><span class="sxs-lookup"><span data-stu-id="81c5f-271">The following events occur:</span></span>

    - <span data-ttu-id="81c5f-272">Система обрабатывает созданную отгрузку, используя шаблон, содержащий шаг печати этикеток.</span><span class="sxs-lookup"><span data-stu-id="81c5f-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="81c5f-273">Макет этикетки будет использоваться для определения формата этикетки, а результатом будет этикетка, которая печатается на принтере, выбранном в шаблоне этикетки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="81c5f-274">Этикетки волны создаются и печатаются.</span><span class="sxs-lookup"><span data-stu-id="81c5f-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="81c5f-275">Число этикеток будет равно количеству коробок (в данном примере 376 этикеток коробок для строки 1 и 322 этикетки коробок для строки 2).</span><span class="sxs-lookup"><span data-stu-id="81c5f-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="81c5f-276">Для отгрузок создается новый код транспортной накладной.</span><span class="sxs-lookup"><span data-stu-id="81c5f-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="81c5f-277">Если настроены расширения номерной серии, коды этикеток волны будут соответствовать формату номера **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="81c5f-278">На следующих страницах можно просматривать и перепечатывать этикетки волны.</span><span class="sxs-lookup"><span data-stu-id="81c5f-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="81c5f-279">На панели операций на каждой странице на вкладке **Отгрузки** в группе **Связанные сведения** выберите **Этикетки волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="81c5f-280">Все отгрузки \> Сведения об отгрузках</span><span class="sxs-lookup"><span data-stu-id="81c5f-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="81c5f-281">Все загрузки \> Сведения о загрузках</span><span class="sxs-lookup"><span data-stu-id="81c5f-281">All loads \> Load details</span></span>
- <span data-ttu-id="81c5f-282">Все волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-282">All waves</span></span>
- <span data-ttu-id="81c5f-283">Этикетки волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-283">Wave labels</span></span>
- <span data-ttu-id="81c5f-284">История этикеток волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="81c5f-285">Сценарий 2. Печать этикеток для контейнеризации (без записей этикеток волны)</span><span class="sxs-lookup"><span data-stu-id="81c5f-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="81c5f-286">Этот сценарий позволяет печатать этикетки волны, когда используется контейнеризация для автоматического разбиения номенклатур на коробки и, таким образом, не требуется запись этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="81c5f-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="81c5f-287">В этом случае идентификатор контейнера выступает в качестве местозаполнителя для SSCC.</span><span class="sxs-lookup"><span data-stu-id="81c5f-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="81c5f-288">Ниже приведены основные различия между этим сценарием и сценарием 1:</span><span class="sxs-lookup"><span data-stu-id="81c5f-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="81c5f-289">**Шаблоны этикеток волны:** вы не будете выбирать тип этикеток волны для шаблона волны, и при этом не требуется группирование сборки этикеток.</span><span class="sxs-lookup"><span data-stu-id="81c5f-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="81c5f-290">В противном случае будет настроен шаблон этикетки волны и ссылка на шаблон волны аналогично описанию в сценарии 1.</span><span class="sxs-lookup"><span data-stu-id="81c5f-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="81c5f-291">Чтобы не допустить создания этикеток волны, необходимо оставить поле типа этикеток волны пустым.</span><span class="sxs-lookup"><span data-stu-id="81c5f-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="81c5f-292">**Макет этикеток волны:** вы настроите параметры строки макета этикеток волны для строк работы вместо записей этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="81c5f-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="81c5f-293">Необходимо настроить параметр строки для макета этикеток, используя таблицу **WHSWorkLine** вместо таблицы **WHSWaveLabel**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="81c5f-294">Параметр **Строк на странице** определяет количество строк, которое будет иметь раздел текста.</span><span class="sxs-lookup"><span data-stu-id="81c5f-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="81c5f-295">Эта конфигурация также подходит для бизнес-сценариев, в которых несколько различных номенклатур упаковываются в одну маркированную коробку или на палету, и этот процесс упаковки может быть определен при помощи создания работы (например, работы, сгруппированной по отгрузке).</span><span class="sxs-lookup"><span data-stu-id="81c5f-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="81c5f-296">В этом сценарии показан сквозной поток.</span><span class="sxs-lookup"><span data-stu-id="81c5f-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="81c5f-297">Сделать демонстрационные данные доступными</span><span class="sxs-lookup"><span data-stu-id="81c5f-297">Make demo data available</span></span>

<span data-ttu-id="81c5f-298">Для выполнения этого сценария необходимо установить демонстрационные данные, а также необходимо выбрать юридическое лицо **USMF**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="81c5f-299">Убедитесь, что доступен метод этикеток волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="81c5f-300">Возможно, придется повторно создать методы обработки волны, чтобы сделать доступным метод печати этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="81c5f-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="81c5f-301">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Методы обработки волн**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="81c5f-302">Убедитесь, что **waveLabelPrinting** есть в списке.</span><span class="sxs-lookup"><span data-stu-id="81c5f-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="81c5f-303">Если его нет, выберите **Повторно создать методы** на панели операций, чтобы добавить его.</span><span class="sxs-lookup"><span data-stu-id="81c5f-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="81c5f-304">Настройка шаблона волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-304">Set up a wave template</span></span>

<span data-ttu-id="81c5f-305">Шаблоны волн позволяют связывать отдельные экземпляры методов волны с соответствующим шаблоном этикетки волны.</span><span class="sxs-lookup"><span data-stu-id="81c5f-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="81c5f-306">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Шаблоны волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="81c5f-307">Выберите шаблон, например **63 Контейнеризация**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="81c5f-308">На экспресс-вкладке **Методы** переместите метод **Печать этикеток волны** в столбец **Выбранные методы**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="81c5f-309">В столбце **Выбранные методы** выберите метод **Печать этикеток волны** и задайте для его поля **Код шага волны** значение *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="81c5f-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="81c5f-310">Дополнительные сведения о кодах шага волны см. в разделе [Коды шагов волны](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="81c5f-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="81c5f-311">Создание макета этикеток волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-311">Create a wave label layout</span></span>

1. <span data-ttu-id="81c5f-312">Перейдите в раздел **Управление складом \> Настройка \> Маршрутизация документов \> Печать этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="81c5f-313">Создайте запись со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-314">**Код макета этикетки:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="81c5f-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="81c5f-315">**Описание:** *Упаковка (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="81c5f-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="81c5f-316">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="81c5f-317">В области действий выберите **Параметры строки этикетки волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="81c5f-318">Будет открыта страница **Параметры строки этикетки волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="81c5f-319">Здесь можно настроить динамическую часть этикетки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="81c5f-320">Добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-321">**Код строки:** *WorkLine*</span><span class="sxs-lookup"><span data-stu-id="81c5f-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="81c5f-322">**Имя таблицы строк:** *WHSWorkLine*</span><span class="sxs-lookup"><span data-stu-id="81c5f-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="81c5f-323">**Положение начала строки:** *500*</span><span class="sxs-lookup"><span data-stu-id="81c5f-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="81c5f-324">В этом поле определяется вертикальная позиция, с которой строка будет начинаться на этикетке.</span><span class="sxs-lookup"><span data-stu-id="81c5f-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="81c5f-325">**Высота строки:** *-50*</span><span class="sxs-lookup"><span data-stu-id="81c5f-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="81c5f-326">Это поле определяет высоту каждой строки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-326">This field defines the height of each row.</span></span> <span data-ttu-id="81c5f-327">Высота строки является положительной для горизонтальных этикеток и отрицательных для вертикальных этикеток.</span><span class="sxs-lookup"><span data-stu-id="81c5f-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="81c5f-328">**Строк на странице:** *5*</span><span class="sxs-lookup"><span data-stu-id="81c5f-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="81c5f-329">В этом поле определяется число строк, которое может быть напечатано на каждой этикетке.</span><span class="sxs-lookup"><span data-stu-id="81c5f-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="81c5f-330">При этой настройке будет распечатано несколько этикеток ZPL на работу, где каждая страница может содержать до пяти строк работы.</span><span class="sxs-lookup"><span data-stu-id="81c5f-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="81c5f-331">Например, если для контейнера, имеющего 12 строк, печатается этикетка, будут распечатаны три этикетки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="81c5f-332">Если требуется напечатать отдельную этикетку для каждой строки комплектации, установите значение *1*.</span><span class="sxs-lookup"><span data-stu-id="81c5f-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="81c5f-333">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="81c5f-333">Close the page.</span></span>
1. <span data-ttu-id="81c5f-334">На панели операций выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="81c5f-335">В диалоговом окне редактора запросов на вкладке **Диапазон** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-336">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="81c5f-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="81c5f-337">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="81c5f-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="81c5f-338">**Поле:** *Тип работы*</span><span class="sxs-lookup"><span data-stu-id="81c5f-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="81c5f-339">**Критерии:** *Комплектации*</span><span class="sxs-lookup"><span data-stu-id="81c5f-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="81c5f-340">Если необходимо распечатать код транспортной накладной, на вкладке **Объединения** выберите таблицу **Строки работ** и присоедините к ней таблицу **Отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="81c5f-341">Закройте диалоговое окно редактора запросов.</span><span class="sxs-lookup"><span data-stu-id="81c5f-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="81c5f-342">На экспресс-вкладке **Макет текста принтера** имеется три раздела для написания кода принтера: **Раздел заголовка** , **Раздел текста** и **Раздел нижнего колонтитула**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="81c5f-343">В разделе **Раздел заголовка** в поле **Заголовок этикетки** введите код для требуемого заголовка.</span><span class="sxs-lookup"><span data-stu-id="81c5f-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="81c5f-344">Например, при использовании принтеров Zebra можно использовать следующий код.</span><span class="sxs-lookup"><span data-stu-id="81c5f-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="81c5f-345">В разделе **Раздел текста** в поле **Текст этикетки** введите код ZPL для требуемого текста.</span><span class="sxs-lookup"><span data-stu-id="81c5f-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="81c5f-346">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="81c5f-346">Here is an example.</span></span>

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

1. <span data-ttu-id="81c5f-347">В разделе **Раздел текста** в поле **Нижний колонтитул этикетки** введите код ZPL для требуемого нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="81c5f-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="81c5f-348">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="81c5f-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="81c5f-349">При этой настройке будет напечатана одна копия каждой этикетки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="81c5f-350">Если требуется больше копий (например, одна копия для каждой из сторон палеты), установите значение **n** для раздела **\^PQn** в нижнем колонтитуле равным требуемому числу копий.</span><span class="sxs-lookup"><span data-stu-id="81c5f-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="81c5f-351">Например, чтобы напечатать четыре копии каждой этикетки, укажите **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="81c5f-352">Теперь этикетка готова к использованию.</span><span class="sxs-lookup"><span data-stu-id="81c5f-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="81c5f-353">Создание шаблона этикеток волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-353">Create a wave label template</span></span>

1. <span data-ttu-id="81c5f-354">Перейдите в раздел **Управление складом \> Настройка \> Маршрутизация документов \> Шаблоны этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="81c5f-355">Добавьте шаблон этикетки волны, затем задайте следующие значения в заголовке:</span><span class="sxs-lookup"><span data-stu-id="81c5f-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="81c5f-356">**Наименование шаблона этикетки:** *Этикетки для контейнеров*</span><span class="sxs-lookup"><span data-stu-id="81c5f-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="81c5f-357">**Описание:** *Этикетки для контейнеров*</span><span class="sxs-lookup"><span data-stu-id="81c5f-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="81c5f-358">**Код шага волны:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="81c5f-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="81c5f-359">**Склад:** *63*</span><span class="sxs-lookup"><span data-stu-id="81c5f-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="81c5f-360">На экспресс-вкладке **Сведения шаблона этикетки волны** добавьте строку со следующими настройками:</span><span class="sxs-lookup"><span data-stu-id="81c5f-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-361">**Код макета этикетки:** *Контейнер*</span><span class="sxs-lookup"><span data-stu-id="81c5f-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="81c5f-362">**Имя принтера:** выберите подходящий принтер ZPL.</span><span class="sxs-lookup"><span data-stu-id="81c5f-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="81c5f-363">**Выполнение запроса:** *Да* (Этот параметр не является обязательным, но рекомендуется для достижения оптимальной производительности.)</span><span class="sxs-lookup"><span data-stu-id="81c5f-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="81c5f-364">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="81c5f-365">Необязательно: если вы настраиваете дизайн этикеток для определенного клиента, необходимо создать запрос, чтобы найти учетную запись клиента.</span><span class="sxs-lookup"><span data-stu-id="81c5f-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="81c5f-366">На экспресс-вкладке **Сведения шаблона этикетки волны** выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="81c5f-367">Затем в диалоговом окне редактора запросов на вкладке **Диапазон** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-368">**Таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="81c5f-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="81c5f-369">**Производная таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="81c5f-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="81c5f-370">**Поле:** *Номер учетной записи*</span><span class="sxs-lookup"><span data-stu-id="81c5f-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="81c5f-371">**Критерии:** введите соответствующий номер учетной записи клиента.</span><span class="sxs-lookup"><span data-stu-id="81c5f-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="81c5f-372">После завершения нажмите кнопку **OK** , чтобы закрыть диалоговое окно редактора запросов.</span><span class="sxs-lookup"><span data-stu-id="81c5f-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="81c5f-373">Настройка расширений номерной серии</span><span class="sxs-lookup"><span data-stu-id="81c5f-373">Configure number sequence extensions</span></span>

<span data-ttu-id="81c5f-374">Расширения номерных серий управляют GS1-соответствием для определенных номерных серий.</span><span class="sxs-lookup"><span data-stu-id="81c5f-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="81c5f-375">Эта настройка не является обязательной для текущего сценария.</span><span class="sxs-lookup"><span data-stu-id="81c5f-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="81c5f-376">Дополнительные сведения и инструкции по настройке см. в разделе [Настройка расширений номерных серий](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="81c5f-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="81c5f-377">Создание заказа на продажу и выпуск его на склад</span><span class="sxs-lookup"><span data-stu-id="81c5f-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="81c5f-378">Перейдите в раздел **Продажи и маркетинг \> Заказ на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="81c5f-379">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-380">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="81c5f-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="81c5f-381">**Склад:** *63*</span><span class="sxs-lookup"><span data-stu-id="81c5f-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="81c5f-382">Добавьте пять строк заказа на продажу:</span><span class="sxs-lookup"><span data-stu-id="81c5f-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="81c5f-383">Строка заказа на продажу 1:</span><span class="sxs-lookup"><span data-stu-id="81c5f-383">Sales order line 1:</span></span>

        - <span data-ttu-id="81c5f-384">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="81c5f-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="81c5f-385">**Количество:** *10*</span><span class="sxs-lookup"><span data-stu-id="81c5f-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="81c5f-386">Строка заказа на продажу 2:</span><span class="sxs-lookup"><span data-stu-id="81c5f-386">Sales order line 2:</span></span>

        - <span data-ttu-id="81c5f-387">**Код номенклатуры:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="81c5f-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="81c5f-388">**Количество:** *20*</span><span class="sxs-lookup"><span data-stu-id="81c5f-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="81c5f-389">Строка заказа на продажу 3:</span><span class="sxs-lookup"><span data-stu-id="81c5f-389">Sales order line 3:</span></span>

        - <span data-ttu-id="81c5f-390">**Код номенклатуры:** *L0006*</span><span class="sxs-lookup"><span data-stu-id="81c5f-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="81c5f-391">**Количество:** *20*</span><span class="sxs-lookup"><span data-stu-id="81c5f-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="81c5f-392">Строка заказа на продажу 4:</span><span class="sxs-lookup"><span data-stu-id="81c5f-392">Sales order line 4:</span></span>

        - <span data-ttu-id="81c5f-393">**Код номенклатуры:** *L0100*</span><span class="sxs-lookup"><span data-stu-id="81c5f-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="81c5f-394">**Количество:** *40*</span><span class="sxs-lookup"><span data-stu-id="81c5f-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="81c5f-395">Строка заказа на продажу 5:</span><span class="sxs-lookup"><span data-stu-id="81c5f-395">Sales order line 5:</span></span>

        - <span data-ttu-id="81c5f-396">**Код номенклатуры:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="81c5f-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="81c5f-397">**Количество:** *50*</span><span class="sxs-lookup"><span data-stu-id="81c5f-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="81c5f-398">Представленные здесь номенклатуры и количества являются только примерами.</span><span class="sxs-lookup"><span data-stu-id="81c5f-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="81c5f-399">Они должны иметь запасы на указанном складе.</span><span class="sxs-lookup"><span data-stu-id="81c5f-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="81c5f-400">Выберите строку заказа на продажу 1.</span><span class="sxs-lookup"><span data-stu-id="81c5f-400">Select sales order line 1.</span></span> <span data-ttu-id="81c5f-401">Затем в разделе **Строка заказа на продажу** в меню **Запасы** выберите **Резервирования**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="81c5f-402">На странице **Резервирование** в области действий выберите **Зарезервировать лот** , затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="81c5f-402">On the **Reservation** page, on the Action Pane, select **Reserve lot** , and then close the page.</span></span>
1. <span data-ttu-id="81c5f-403">Повторите шаги 4 и 5 для каждой дополнительной строки заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="81c5f-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="81c5f-404">На панели операций на вкладке **Склад** выберите вариант **Выпустить на склад**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="81c5f-405">Имеют место следующие события:</span><span class="sxs-lookup"><span data-stu-id="81c5f-405">The following events occur:</span></span>

    - <span data-ttu-id="81c5f-406">Система обрабатывает созданную отгрузку, используя шаблон, содержащий шаг печати этикеток.</span><span class="sxs-lookup"><span data-stu-id="81c5f-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="81c5f-407">Макет этикетки будет использоваться для определения формата этикетки, а конечным результатом будет этикетка, которая содержит пять строк и печатается на принтере, выбранном в шаблоне этикетки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="81c5f-408">Для отгрузок создается новый код транспортной накладной.</span><span class="sxs-lookup"><span data-stu-id="81c5f-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="81c5f-409">Если настроены расширения номерной серии, коды этикеток волны будут соответствовать формату номера **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="81c5f-410">Эти этикетки волны можно перепечатать, перейдя в раздел **Управление складом \> Запросы и отчеты \> История этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="81c5f-411">Сценарий 3. Печать этикеток волны для многоуровневых этикеток</span><span class="sxs-lookup"><span data-stu-id="81c5f-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="81c5f-412">В этом сценарии показано, как использовать функции печати этикеток волны, когда складские процессы требуют наличия нескольких уровней этикеток отгрузки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="81c5f-413">Например, может требоваться печатать отдельные этикетки для коробок и палет, а разделительная этикетка должна быть распечатана для всей отгрузки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="81c5f-414">Разделительные этикетки представляют собой отдельный тип этикетки, который может использоваться в качестве разделителя между рулонами и контейнерами, например этикетки для кода отгрузки и штрихкода, чтобы можно было легко отсортировать этикетки после их печати.</span><span class="sxs-lookup"><span data-stu-id="81c5f-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="81c5f-415">Основное различие между конфигурацией этого сценария и конфигурацией сценария 1, помимо того, что включены разделительные этикетки, состоит в том, что несколько типов этикеток волны должны быть связаны с шаблонами этикеток волны и строками группы последовательности единиц.</span><span class="sxs-lookup"><span data-stu-id="81c5f-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="81c5f-416">Для выполнения этой настройки в этом сценарии настраиваются следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="81c5f-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="81c5f-417">**Методы обработки волн:** вы пометите метод этикеток волны как "повторяемый", добавите его два (или более) раз в шаблон волн и зададите другие коды шагов волны.</span><span class="sxs-lookup"><span data-stu-id="81c5f-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="81c5f-418">**Шаблоны этикеток волны:** вы настроите шаблоны этикеток волны и свяжите их с шаблоном волны.</span><span class="sxs-lookup"><span data-stu-id="81c5f-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="81c5f-419">Каждый шаблон этикетки волны имеет свой собственный тип этикетки волны.</span><span class="sxs-lookup"><span data-stu-id="81c5f-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="81c5f-420">**Макеты этикеток волны:** будет создано несколько макетов этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="81c5f-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="81c5f-421">Для каждого "уровня" этикеток будет использоваться отдельный макет этикеток, а также будет макет разделительной этикетки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="81c5f-422">В этом сценарии показан сквозной поток.</span><span class="sxs-lookup"><span data-stu-id="81c5f-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="81c5f-423">Сделать демонстрационные данные доступными</span><span class="sxs-lookup"><span data-stu-id="81c5f-423">Make demo data available</span></span>

<span data-ttu-id="81c5f-424">Для выполнения этого сценария необходимо установить демонстрационные данные, а также необходимо выбрать юридическое лицо **USMF**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="81c5f-425">Настройка метода обработки волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-425">Set up a wave process method</span></span>

1. <span data-ttu-id="81c5f-426">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Методы обработки волн**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="81c5f-427">Убедитесь, что **waveLabelPrinting** есть в списке.</span><span class="sxs-lookup"><span data-stu-id="81c5f-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="81c5f-428">Если его нет, выберите **Повторно создать методы** на панели операций, чтобы добавить его.</span><span class="sxs-lookup"><span data-stu-id="81c5f-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="81c5f-429">Для метода **waveLabelPrinting** установите флажок **Сделать метод повторяемым**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="81c5f-430">Настройка шаблона волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-430">Set up a wave template</span></span>

1. <span data-ttu-id="81c5f-431">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Шаблоны волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="81c5f-432">Выберите шаблон, например **62 Отгрузка по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="81c5f-433">На экспресс-вкладке **Методы** переместите метод **Печать этикеток волны** в столбец **Выбранные методы**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="81c5f-434">В столбце **Выбранные методы** назначьте значение **Код шага волны** , например *Коробка* , для метода **Печать этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton* , to the **Wave label printing** method.</span></span> <span data-ttu-id="81c5f-435">Дополнительные сведения о кодах шага волны см. в разделе [Коды шагов волны](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="81c5f-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="81c5f-436">Переместите метод **Печать этикеток волны** в столбец **Выбранные методы** второй раз.</span><span class="sxs-lookup"><span data-stu-id="81c5f-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="81c5f-437">В столбце **Выбранные методы** назначьте другое значение **Код шага волны** , например *Палета* , для второго метода **Печать этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet* , to the second **Wave label printing** method.</span></span> <span data-ttu-id="81c5f-438">Дополнительные сведения о кодах шага волны см. в разделе [Коды шагов волны](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="81c5f-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="81c5f-439">Создание трех макетов этикеток волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="81c5f-440">Перейдите в раздел **Управление складом \> Настройка \> Маршрутизация документов \> Печать этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="81c5f-441">Создайте запись со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-442">**Код макета этикетки:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="81c5f-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="81c5f-443">**Описание:** *Упаковка (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="81c5f-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="81c5f-444">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="81c5f-445">В области действий выберите **Параметры строки этикетки волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="81c5f-446">Будет открыта страница **Параметры строки этикетки волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="81c5f-447">Здесь можно настроить динамическую часть этикетки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="81c5f-448">Добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-449">**Код строки:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="81c5f-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="81c5f-450">**Имя таблицы строк:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="81c5f-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="81c5f-451">**Положение начала строки:** *0*</span><span class="sxs-lookup"><span data-stu-id="81c5f-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="81c5f-452">В этом поле определяется вертикальная позиция, с которой строка будет начинаться на этикетке.</span><span class="sxs-lookup"><span data-stu-id="81c5f-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="81c5f-453">**Высота строки:** *0*</span><span class="sxs-lookup"><span data-stu-id="81c5f-453">**Row height:** *0*</span></span>

        <span data-ttu-id="81c5f-454">Это поле определяет высоту каждой строки (в пунктах) в соответствии со стандартом ZPL.</span><span class="sxs-lookup"><span data-stu-id="81c5f-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="81c5f-455">Высота строки является положительной для горизонтальных этикеток и отрицательных для вертикальных этикеток.</span><span class="sxs-lookup"><span data-stu-id="81c5f-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="81c5f-456">Поскольку в данном примере имеется только одна строка, можно установить значение равным *0* (нулю).</span><span class="sxs-lookup"><span data-stu-id="81c5f-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="81c5f-457">**Строк на странице:** *1*</span><span class="sxs-lookup"><span data-stu-id="81c5f-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="81c5f-458">В этом поле определяется число строк, которое может быть напечатано на каждой этикетке.</span><span class="sxs-lookup"><span data-stu-id="81c5f-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="81c5f-459">Эта настройка приведет к печати отдельной этикетки ZPL для каждой записи в таблице этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="81c5f-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="81c5f-460">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="81c5f-460">Close the page.</span></span>
1. <span data-ttu-id="81c5f-461">На панели операций выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="81c5f-462">В диалоговом окне редактора запросов на вкладке **Диапазон** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-463">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="81c5f-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="81c5f-464">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="81c5f-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="81c5f-465">**Поле:** *Тип работы*</span><span class="sxs-lookup"><span data-stu-id="81c5f-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="81c5f-466">**Критерии:** *Комплектации*</span><span class="sxs-lookup"><span data-stu-id="81c5f-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="81c5f-467">Этот запрос гарантирует, что в этикетке будут печататься только строки работа типа "Комплектация", а не строки типа "Размещение".</span><span class="sxs-lookup"><span data-stu-id="81c5f-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="81c5f-468">Если необходимо распечатать код транспортной накладной, на вкладке **Объединения** выберите таблицу **Строки работ** и присоедините к ней таблицу **Отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="81c5f-469">Закройте диалоговое окно редактора запросов.</span><span class="sxs-lookup"><span data-stu-id="81c5f-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="81c5f-470">На экспресс-вкладке **Макет текста принтера** имеется три раздела для написания кода принтера: **Раздел заголовка** , **Раздел текста** и **Раздел нижнего колонтитула**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="81c5f-471">В разделе **Раздел заголовка** в поле **Заголовок этикетки** введите код для требуемого заголовка.</span><span class="sxs-lookup"><span data-stu-id="81c5f-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="81c5f-472">Например, при использовании принтеров Zebra можно использовать следующий код.</span><span class="sxs-lookup"><span data-stu-id="81c5f-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


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

1. <span data-ttu-id="81c5f-473">В разделе **Раздел текста** в поле **Текст этикетки** введите код ZPL для требуемого текста.</span><span class="sxs-lookup"><span data-stu-id="81c5f-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="81c5f-474">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="81c5f-474">Here is an example.</span></span>

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

1. <span data-ttu-id="81c5f-475">В разделе **Раздел текста** в поле **Нижний колонтитул этикетки** введите код ZPL для требуемого нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="81c5f-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="81c5f-476">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="81c5f-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="81c5f-477">При этой настройке будет напечатана одна копия каждой этикетки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="81c5f-478">Если требуется больше копий (например, одна копия для каждой из сторон палеты), установите значение **n** для раздела **\^PQn** в нижнем колонтитуле равным требуемому числу копий.</span><span class="sxs-lookup"><span data-stu-id="81c5f-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="81c5f-479">Например, чтобы напечатать четыре копии каждой этикетки, укажите **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="81c5f-480">Первая этикетка готова к использованию.</span><span class="sxs-lookup"><span data-stu-id="81c5f-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="81c5f-481">Создайте вторую запись макета со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-482">**Код макета этикетки:** *Палета*</span><span class="sxs-lookup"><span data-stu-id="81c5f-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="81c5f-483">**Описание:** *Палета*</span><span class="sxs-lookup"><span data-stu-id="81c5f-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="81c5f-484">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="81c5f-485">В области действий выберите **Параметры строки этикетки волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="81c5f-486">Будет открыта страница **Параметры строки этикетки волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="81c5f-487">Здесь можно настроить динамическую часть этикетки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="81c5f-488">Добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-489">**Код строки:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="81c5f-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="81c5f-490">**Имя таблицы строк:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="81c5f-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="81c5f-491">**Положение начала строки:** *0*</span><span class="sxs-lookup"><span data-stu-id="81c5f-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="81c5f-492">В этом поле определяется вертикальная позиция, с которой строка будет начинаться на этикетке.</span><span class="sxs-lookup"><span data-stu-id="81c5f-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="81c5f-493">**Высота строки:** *0*</span><span class="sxs-lookup"><span data-stu-id="81c5f-493">**Row height:** *0*</span></span>

        <span data-ttu-id="81c5f-494">Это поле определяет высоту каждой строки (в пунктах) в соответствии со стандартом ZPL.</span><span class="sxs-lookup"><span data-stu-id="81c5f-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="81c5f-495">Высота строки является положительной для горизонтальных этикеток и отрицательных для вертикальных этикеток.</span><span class="sxs-lookup"><span data-stu-id="81c5f-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="81c5f-496">Поскольку в данном примере имеется только одна строка, можно установить значение равным *0* (нулю).</span><span class="sxs-lookup"><span data-stu-id="81c5f-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="81c5f-497">**Строк на странице:** *1*</span><span class="sxs-lookup"><span data-stu-id="81c5f-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="81c5f-498">В этом поле определяется число строк, которое может быть напечатано на каждой этикетке.</span><span class="sxs-lookup"><span data-stu-id="81c5f-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="81c5f-499">Эта настройка приводит к печати отдельной этикетки ZPL для каждой записи в таблице этикеток волны.</span><span class="sxs-lookup"><span data-stu-id="81c5f-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="81c5f-500">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="81c5f-500">Close the page.</span></span>
1. <span data-ttu-id="81c5f-501">На панели операций выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="81c5f-502">В диалоговом окне редактора запросов на вкладке **Диапазон** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-503">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="81c5f-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="81c5f-504">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="81c5f-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="81c5f-505">**Поле:** *Тип работы*</span><span class="sxs-lookup"><span data-stu-id="81c5f-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="81c5f-506">**Критерии:** *Комплектации*</span><span class="sxs-lookup"><span data-stu-id="81c5f-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="81c5f-507">Этот запрос гарантирует, что в этикетке будут печататься только строки работа типа "Комплектация", а не строки типа "Размещение".</span><span class="sxs-lookup"><span data-stu-id="81c5f-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="81c5f-508">Если необходимо распечатать код транспортной накладной, на вкладке **Объединения** выберите таблицу **Строки работ** и присоедините к ней таблицу **Отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="81c5f-509">Закройте диалоговое окно редактора запросов.</span><span class="sxs-lookup"><span data-stu-id="81c5f-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="81c5f-510">На экспресс-вкладке **Макет текста принтера** имеется три раздела для написания кода принтера: **Раздел заголовка** , **Раздел текста** и **Раздел нижнего колонтитула**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="81c5f-511">В разделе **Раздел заголовка** в поле **Заголовок этикетки** введите код для требуемого заголовка.</span><span class="sxs-lookup"><span data-stu-id="81c5f-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="81c5f-512">Например, при использовании принтеров Zebra можно использовать следующий код.</span><span class="sxs-lookup"><span data-stu-id="81c5f-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="81c5f-513">В разделе **Раздел текста** в поле **Текст этикетки** введите код ZPL для требуемого текста.</span><span class="sxs-lookup"><span data-stu-id="81c5f-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="81c5f-514">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="81c5f-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="81c5f-515">В разделе **Раздел текста** в поле **Нижний колонтитул этикетки** введите код ZPL для требуемого нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="81c5f-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="81c5f-516">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="81c5f-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="81c5f-517">При этой настройке будет напечатана одна копия каждой этикетки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="81c5f-518">Если требуется больше копий (например, одна копия для каждой из сторон палеты), установите значение **n** для раздела **\^PQn** в нижнем колонтитуле равным требуемому числу копий.</span><span class="sxs-lookup"><span data-stu-id="81c5f-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="81c5f-519">Например, чтобы напечатать четыре копии каждой этикетки, укажите **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="81c5f-520">Вторая этикетка готова к использованию.</span><span class="sxs-lookup"><span data-stu-id="81c5f-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="81c5f-521">Создайте третью запись макета со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-522">**Код макета этикетки:** *Разделитель*</span><span class="sxs-lookup"><span data-stu-id="81c5f-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="81c5f-523">**Описание:** *Разделительная этикетка*</span><span class="sxs-lookup"><span data-stu-id="81c5f-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="81c5f-524">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="81c5f-525">На экспресс-вкладке **Макет текста принтера** имеется три раздела для написания кода принтера: **Раздел заголовка** , **Раздел текста** и **Раздел нижнего колонтитула**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="81c5f-526">В разделе **Раздел заголовка** в поле **Заголовок этикетки** введите код ZPL для требуемого заголовка.</span><span class="sxs-lookup"><span data-stu-id="81c5f-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="81c5f-527">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="81c5f-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="81c5f-528">На этот раз текст не требуется.</span><span class="sxs-lookup"><span data-stu-id="81c5f-528">This time, no body is required.</span></span> <span data-ttu-id="81c5f-529">Таким образом, просто введите необходимый текст в раздел **Нижний колонтитул**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="81c5f-530">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="81c5f-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="81c5f-531">Третья этикетка готова к использованию.</span><span class="sxs-lookup"><span data-stu-id="81c5f-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="81c5f-532">Эта третья этикетка представляет собой разделительную этикетку, которая будет использоваться в качестве разделителя для рулонов этикеток.</span><span class="sxs-lookup"><span data-stu-id="81c5f-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="81c5f-533">Создание двух типов этикеток волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-533">Create two wave label types</span></span>

1. <span data-ttu-id="81c5f-534">Перейдите в раздел **Управление складом \> Настройка \> Маршрутизация документов \> Типы этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="81c5f-535">Создайте запись со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-536">**Тип этикетки:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="81c5f-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="81c5f-537">**Описание:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="81c5f-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="81c5f-538">Создайте вторую запись со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-539">**Тип этикетки:** *Палета*</span><span class="sxs-lookup"><span data-stu-id="81c5f-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="81c5f-540">**Описание:** *Палета*</span><span class="sxs-lookup"><span data-stu-id="81c5f-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="81c5f-541">Настройка групп упорядочения единиц</span><span class="sxs-lookup"><span data-stu-id="81c5f-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="81c5f-542">Перейдите в раздел **Управление складом \> Настройка \> Склад \> Группы упорядочения единиц**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="81c5f-543">Выберите или создайте группу **шт., коробка, палета**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="81c5f-544">Для строки **Ящик** введите в поле **Тип уровня волны** значение *Упаковка*.</span><span class="sxs-lookup"><span data-stu-id="81c5f-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="81c5f-545">Для строки **Палета** введите в поле **Тип уровня волны** значение *Палета*.</span><span class="sxs-lookup"><span data-stu-id="81c5f-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="81c5f-546">Создание шаблонов этикеток волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-546">Create wave label templates</span></span>

1. <span data-ttu-id="81c5f-547">Перейдите в раздел **Управление складом \> Настройка \> Маршрутизация документов \> Шаблоны этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="81c5f-548">Создайте шаблон этикеток со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-549">**Наименование шаблона этикетки:** *Этикетки для упаковки*</span><span class="sxs-lookup"><span data-stu-id="81c5f-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="81c5f-550">**Описание:** *Этикетки для упаковки*</span><span class="sxs-lookup"><span data-stu-id="81c5f-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="81c5f-551">**Код шага волны:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="81c5f-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="81c5f-552">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="81c5f-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="81c5f-553">На экспресс-вкладке **Общее** в поле **Тип этикеток волны** выберите значение, например, *Упаковка*.</span><span class="sxs-lookup"><span data-stu-id="81c5f-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="81c5f-554">На экспресс-вкладке **Сведения шаблона этикетки волны** добавьте строку со следующими настройками:</span><span class="sxs-lookup"><span data-stu-id="81c5f-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-555">**Код макета этикетки:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="81c5f-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="81c5f-556">**Имя принтера:** выберите подходящий принтер ZPL.</span><span class="sxs-lookup"><span data-stu-id="81c5f-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="81c5f-557">**Выполнение запроса:** *Да* (Этот параметр не является обязательным, но рекомендуется для достижения оптимальной производительности.)</span><span class="sxs-lookup"><span data-stu-id="81c5f-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="81c5f-558">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="81c5f-559">Необязательно: если вы настраиваете дизайн этикеток для определенного клиента, необходимо создать запрос, чтобы найти учетную запись клиента.</span><span class="sxs-lookup"><span data-stu-id="81c5f-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="81c5f-560">На экспресс-вкладке **Сведения шаблона этикетки волны** выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="81c5f-561">Затем в диалоговом окне редактора запросов на вкладке **Диапазон** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-562">**Таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="81c5f-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="81c5f-563">**Производная таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="81c5f-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="81c5f-564">**Поле:** *Номер учетной записи*</span><span class="sxs-lookup"><span data-stu-id="81c5f-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="81c5f-565">**Критерии:** введите соответствующий номер учетной записи клиента.</span><span class="sxs-lookup"><span data-stu-id="81c5f-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="81c5f-566">После завершения нажмите кнопку **OK** , чтобы закрыть диалоговое окно редактора запросов.</span><span class="sxs-lookup"><span data-stu-id="81c5f-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="81c5f-567">На панели операций выберите **Изменить запрос** , чтобы открыть диалоговое окно редактора запросов для всего шаблона этикетки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="81c5f-568">В диалоговом окне редактора запросов на вкладке **Сортировка** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-569">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="81c5f-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="81c5f-570">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="81c5f-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="81c5f-571">**Поле:** *Код строки загрузки ссылки (ИД записи)*</span><span class="sxs-lookup"><span data-stu-id="81c5f-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="81c5f-572">**Направление поиска:** *Восходящее*</span><span class="sxs-lookup"><span data-stu-id="81c5f-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="81c5f-573">Добавьте вторую строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-574">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="81c5f-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="81c5f-575">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="81c5f-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="81c5f-576">**Поле:** *Код отгрузки*</span><span class="sxs-lookup"><span data-stu-id="81c5f-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="81c5f-577">**Направление поиска:** *Восходящее*</span><span class="sxs-lookup"><span data-stu-id="81c5f-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="81c5f-578">Выберите **ОК** , чтобы закрыть диалоговое окно редактора запроса.</span><span class="sxs-lookup"><span data-stu-id="81c5f-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="81c5f-579">В окне сообщение будет предложено подтвердить операцию сброса группы.</span><span class="sxs-lookup"><span data-stu-id="81c5f-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="81c5f-580">Выберите **Да** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="81c5f-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="81c5f-581">В области действий выберите **Группа шаблонов этикеток волн**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="81c5f-582">В диалоговом окне **Группа шаблонов этикеток волны** для строки, в которой для поля **Имя поля ссылки** указано значение *Код отгрузки* , установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="81c5f-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID* , set the following values:</span></span>

    - <span data-ttu-id="81c5f-583">**Печатать разделительную этикетку:** установите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="81c5f-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="81c5f-584">**Код макета этикетки:** выберите разделительную этикетку.</span><span class="sxs-lookup"><span data-stu-id="81c5f-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="81c5f-585">(Например, выберите макет этикетки *Разделитель* , созданной ранее в этом сценарии.)</span><span class="sxs-lookup"><span data-stu-id="81c5f-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="81c5f-586">**Имя принтера:** выберите принтер для разделительной этикетки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="81c5f-587">(Обычно для задачи разделения рулонов этикеток следует выбирать тот же принтер, что и выбранный на экспресс-вкладка **Сведения о шаблоне этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="81c5f-588">Однако возможны и другие сценарии.)</span><span class="sxs-lookup"><span data-stu-id="81c5f-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="81c5f-589">Для строки, в которой поле **Имя поля ссылки** имеет значение *Код строки загрузки ссылки* , установите флажок **Код сборки этикетки**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-589">For the row where the **Reference field name** field is set to *Reference load line id* , select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="81c5f-590">Эта настройка создаст одну последовательность этикеток ("Упаковка 1 из X") для каждой строки загрузки в волне, независимо от настройки группировки работ.</span><span class="sxs-lookup"><span data-stu-id="81c5f-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="81c5f-591">Эта последовательность этикеток может быть распечатана в макете этикеток.</span><span class="sxs-lookup"><span data-stu-id="81c5f-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="81c5f-592">Кроме того, этикетки для различных отгрузок будут отделены выбранной разделительной этикеткой.</span><span class="sxs-lookup"><span data-stu-id="81c5f-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="81c5f-593">Выберите **ОК** , чтобы закрыть диалоговое окно **Группа шаблонов этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="81c5f-594">Создайте второй шаблон этикеток со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-595">**Наименование шаблона этикетки:** *Этикетки для палет*</span><span class="sxs-lookup"><span data-stu-id="81c5f-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="81c5f-596">**Описание:** *Этикетки для палет*</span><span class="sxs-lookup"><span data-stu-id="81c5f-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="81c5f-597">**Код шага волны:** *Палета*</span><span class="sxs-lookup"><span data-stu-id="81c5f-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="81c5f-598">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="81c5f-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="81c5f-599">На экспресс-вкладке **Общее** в поле **Тип этикеток волны** выберите значение, например, *Палета*.</span><span class="sxs-lookup"><span data-stu-id="81c5f-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="81c5f-600">На экспресс-вкладке **Сведения шаблона этикетки волны** добавьте строку со следующими настройками:</span><span class="sxs-lookup"><span data-stu-id="81c5f-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-601">**Код макета этикетки:** *Палета*</span><span class="sxs-lookup"><span data-stu-id="81c5f-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="81c5f-602">**Имя принтера:** выберите подходящий принтер ZPL.</span><span class="sxs-lookup"><span data-stu-id="81c5f-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="81c5f-603">**Выполнение запроса:** *Да* (Этот параметр не является обязательным, но рекомендуется для достижения оптимальной производительности.)</span><span class="sxs-lookup"><span data-stu-id="81c5f-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="81c5f-604">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="81c5f-605">Необязательно: если вы настраиваете дизайн этикеток для определенного клиента, необходимо создать запрос, чтобы найти учетную запись клиента.</span><span class="sxs-lookup"><span data-stu-id="81c5f-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="81c5f-606">На экспресс-вкладке **Сведения шаблона этикетки волны** выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="81c5f-607">Затем в диалоговом окне редактора запросов на вкладке **Диапазон** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-608">**Таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="81c5f-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="81c5f-609">**Производная таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="81c5f-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="81c5f-610">**Поле:** *Номер учетной записи*</span><span class="sxs-lookup"><span data-stu-id="81c5f-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="81c5f-611">**Критерии:** введите соответствующий номер учетной записи клиента.</span><span class="sxs-lookup"><span data-stu-id="81c5f-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="81c5f-612">После завершения нажмите кнопку **OK** , чтобы закрыть диалоговое окно редактора запросов.</span><span class="sxs-lookup"><span data-stu-id="81c5f-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="81c5f-613">На панели операций выберите **Изменить запрос** , чтобы открыть диалоговое окно редактора запросов для всего шаблона этикетки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="81c5f-614">В диалоговом окне редактора запросов на вкладке **Сортировка** добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-615">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="81c5f-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="81c5f-616">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="81c5f-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="81c5f-617">**Поле:** *Код строки загрузки ссылки (ИД записи)*</span><span class="sxs-lookup"><span data-stu-id="81c5f-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="81c5f-618">**Направление поиска:** *Восходящее*</span><span class="sxs-lookup"><span data-stu-id="81c5f-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="81c5f-619">Добавьте вторую строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-620">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="81c5f-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="81c5f-621">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="81c5f-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="81c5f-622">**Поле:** *Код отгрузки*</span><span class="sxs-lookup"><span data-stu-id="81c5f-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="81c5f-623">**Направление поиска:** *Восходящее*</span><span class="sxs-lookup"><span data-stu-id="81c5f-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="81c5f-624">Выберите **ОК** , чтобы закрыть диалоговое окно редактора запроса.</span><span class="sxs-lookup"><span data-stu-id="81c5f-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="81c5f-625">В окне сообщение будет предложено подтвердить операцию сброса группы.</span><span class="sxs-lookup"><span data-stu-id="81c5f-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="81c5f-626">Выберите **Да** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="81c5f-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="81c5f-627">В области действий выберите **Группа шаблонов этикеток волн**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="81c5f-628">В диалоговом окне **Группа шаблонов этикеток волны** для строки, в которой для поля **Имя поля ссылки** указано значение *Код отгрузки* , установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="81c5f-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID* , set the following values:</span></span>

    - <span data-ttu-id="81c5f-629">**Печатать разделительную этикетку:** установите этот флажок.</span><span class="sxs-lookup"><span data-stu-id="81c5f-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="81c5f-630">**Код макета этикетки:** выберите разделительную этикетку.</span><span class="sxs-lookup"><span data-stu-id="81c5f-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="81c5f-631">(Например, выберите макет этикетки *Разделитель* , созданной ранее в этом сценарии.)</span><span class="sxs-lookup"><span data-stu-id="81c5f-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="81c5f-632">**Имя принтера:** выберите принтер для разделительной этикетки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="81c5f-633">(Обычно для задачи разделения рулонов этикеток следует выбирать тот же принтер, что и выбранный на экспресс-вкладка **Сведения о шаблоне этикеток волны**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="81c5f-634">Однако возможны и другие сценарии.)</span><span class="sxs-lookup"><span data-stu-id="81c5f-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="81c5f-635">Для строки, в которой поле **Имя поля ссылки** имеет значение *Код строки загрузки ссылки* , установите флажок **Код сборки этикетки**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-635">For the row where the **Reference field name** field is set to *Reference load line id* , select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="81c5f-636">Эта настройка создаст одну последовательность этикеток ("Упаковка 1 из X") для каждой строки загрузки в волне, независимо от настройки группировки работ.</span><span class="sxs-lookup"><span data-stu-id="81c5f-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="81c5f-637">Эта последовательность этикеток может быть распечатана в макете этикеток.</span><span class="sxs-lookup"><span data-stu-id="81c5f-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="81c5f-638">Кроме того, этикетки для различных отгрузок будут отделены выбранной разделительной этикеткой.</span><span class="sxs-lookup"><span data-stu-id="81c5f-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="81c5f-639">Настройка расширений номерной серии</span><span class="sxs-lookup"><span data-stu-id="81c5f-639">Configure number sequence extensions</span></span>

<span data-ttu-id="81c5f-640">Расширения номерных серий управляют GS1-соответствием для определенных номерных серий.</span><span class="sxs-lookup"><span data-stu-id="81c5f-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="81c5f-641">Эта настройка не является обязательной для текущего сценария.</span><span class="sxs-lookup"><span data-stu-id="81c5f-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="81c5f-642">Дополнительные сведения и инструкции по настройке см. в разделе [Настройка расширений номерных серий](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="81c5f-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="81c5f-643">Создание заказа на продажу и выпуск его на склад</span><span class="sxs-lookup"><span data-stu-id="81c5f-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="81c5f-644">Перейдите в раздел **Продажи и маркетинг \> Заказ на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="81c5f-645">Создайте заказ на продажу со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="81c5f-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="81c5f-646">**Счет клиента:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="81c5f-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="81c5f-647">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="81c5f-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="81c5f-648">Добавьте две строки заказа на продажу:</span><span class="sxs-lookup"><span data-stu-id="81c5f-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="81c5f-649">Строка заказа на продажу 1:</span><span class="sxs-lookup"><span data-stu-id="81c5f-649">Sales order line 1:</span></span>

        - <span data-ttu-id="81c5f-650">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="81c5f-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="81c5f-651">**Количество:** *9024*</span><span class="sxs-lookup"><span data-stu-id="81c5f-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="81c5f-652">**Единица измерения:** *шт.* (9024 шт. = 376 коробок = 47 палет)</span><span class="sxs-lookup"><span data-stu-id="81c5f-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="81c5f-653">Строка заказа на продажу 2:</span><span class="sxs-lookup"><span data-stu-id="81c5f-653">Sales order line 2:</span></span>

        - <span data-ttu-id="81c5f-654">**Код номенклатуры:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="81c5f-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="81c5f-655">**Количество:** *9016*</span><span class="sxs-lookup"><span data-stu-id="81c5f-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="81c5f-656">**Единица измерения:** *шт.* (9016 шт. = 322 коробки = 46 палет)</span><span class="sxs-lookup"><span data-stu-id="81c5f-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="81c5f-657">Представленные здесь номенклатуры и количества являются только примерами.</span><span class="sxs-lookup"><span data-stu-id="81c5f-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="81c5f-658">Они должны использовать ранее определенную группу последовательности единиц измерения, подходящие преобразования единиц измерения из *шт.* в *коробки* и в *палеты* , для которых должны быть запасы на складе *62*.</span><span class="sxs-lookup"><span data-stu-id="81c5f-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="81c5f-659">Дополнительные сведения см. в разделе [Единицы измерения и политики хранения](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="81c5f-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="81c5f-660">Выберите строку заказа на продажу 1.</span><span class="sxs-lookup"><span data-stu-id="81c5f-660">Select sales order line 1.</span></span> <span data-ttu-id="81c5f-661">Затем в разделе **Строка заказа на продажу** в меню **Запасы** выберите **Резервирования**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="81c5f-662">На странице **Резервирование** в области действий выберите **Зарезервировать лот** , затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="81c5f-662">On the **Reservation** page, on the Action Pane, select **Reserve lot** , and then close the page.</span></span>
1. <span data-ttu-id="81c5f-663">Повторите шаги 4 и 5 для строки заказа на продажу 2.</span><span class="sxs-lookup"><span data-stu-id="81c5f-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="81c5f-664">На панели операций на вкладке **Склад** выберите вариант **Выпустить на склад**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="81c5f-665">Имеют место следующие события:</span><span class="sxs-lookup"><span data-stu-id="81c5f-665">The following events occur:</span></span> 

    - <span data-ttu-id="81c5f-666">Система обрабатывает созданную отгрузку, используя шаблон, содержащий шаг печати этикеток.</span><span class="sxs-lookup"><span data-stu-id="81c5f-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="81c5f-667">Макет этикетки будет использоваться для определения формата этикетки, а результатом будет этикетка, которая печатается на принтере, выбранном в шаблоне этикетки.</span><span class="sxs-lookup"><span data-stu-id="81c5f-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="81c5f-668">Этикетки волны создаются и печатаются.</span><span class="sxs-lookup"><span data-stu-id="81c5f-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="81c5f-669">Число этикеток равно числу коробок (в данном примере 376 этикеток коробок для строки 1, 322 этикетки коробок для строки 2, 47 этикеток палет для строки 1, 47 этикеток палет для строки 2 и две разделительных этикетки с кодом отгрузки).</span><span class="sxs-lookup"><span data-stu-id="81c5f-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="81c5f-670">Для отгрузок создается новый код транспортной накладной.</span><span class="sxs-lookup"><span data-stu-id="81c5f-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="81c5f-671">Если настроены расширения номерной серии, коды этикеток волны будут соответствовать формату номера **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="81c5f-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="81c5f-672">На следующих страницах можно просматривать и перепечатывать этикетки волны:</span><span class="sxs-lookup"><span data-stu-id="81c5f-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="81c5f-673">Все отгрузки \> Сведения об отгрузках</span><span class="sxs-lookup"><span data-stu-id="81c5f-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="81c5f-674">Все загрузки \> Сведения о загрузках</span><span class="sxs-lookup"><span data-stu-id="81c5f-674">All loads \> Load details</span></span>
- <span data-ttu-id="81c5f-675">Все волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-675">All waves</span></span>
- <span data-ttu-id="81c5f-676">Этикетки волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-676">Wave labels</span></span>
- <span data-ttu-id="81c5f-677">История этикеток волны</span><span class="sxs-lookup"><span data-stu-id="81c5f-677">Wave label history</span></span>

<span data-ttu-id="81c5f-678">Для большинства из этих страниц можно найти соответствующую функцию, выбрав **Этикетки волны** в группе **Связанные сведения** на вкладке **Отгрузки** в области действий.</span><span class="sxs-lookup"><span data-stu-id="81c5f-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>
