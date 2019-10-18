---
title: Субподряд
description: Эта тема представляет собой пошаговое руководство по субподряду в производстве в Dynamics 365 Supply Chain Management.
author: christophernread
manager: AnnBe
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 83d1d7adf91c246ecad574043cbb60ca260bb328
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249926"
---
# <a name="subcontracting"></a><span data-ttu-id="e1248-103">Субподряд</span><span class="sxs-lookup"><span data-stu-id="e1248-103">Subcontracting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1248-104">Эта тема представляет собой пошаговое руководство по субподряду в производстве в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e1248-104">This topic will help you build a walkthrough of subcontracting in manufacturing in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e1248-105">В первой части этой темы рассматривается настройка данных.</span><span class="sxs-lookup"><span data-stu-id="e1248-105">The first part of this topic describes the setup of the data.</span></span> <span data-ttu-id="e1248-106">Вторая часть представляет собой описание шагов в руководстве.</span><span class="sxs-lookup"><span data-stu-id="e1248-106">The second part takes you through the steps in the walkthrough.</span></span>

## <a name="target-audience"></a><span data-ttu-id="e1248-107">Целевая аудитория</span><span class="sxs-lookup"><span data-stu-id="e1248-107">Target audience</span></span>

<span data-ttu-id="e1248-108">В этой теме рассматривается настройка субподряда в производстве.</span><span class="sxs-lookup"><span data-stu-id="e1248-108">In this topic, you will learn how to set up subcontracting in manufacturing.</span></span> <span data-ttu-id="e1248-109">Для базовой настройки потока мероприятия субподряда используются существующие данные в юридическом лице HQUS.</span><span class="sxs-lookup"><span data-stu-id="e1248-109">You will use existing data in the HQUS legal entity to do the basic setup of a subcontracting activity flow.</span></span> <span data-ttu-id="e1248-110">Демонстрационные данные в юридическом лице HQUS включают в себя параметры настройки, которые были предварительно заданы в соответствии с шагами в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="e1248-110">The demo data in the HQUS legal entity includes setup parameters that have been preset to support the steps in the walkthrough.</span></span> <span data-ttu-id="e1248-111">Хотя в руководстве рассматриваются проблемные моменты и затруднения для различных ролей, выполнять его может администратор системы.</span><span class="sxs-lookup"><span data-stu-id="e1248-111">Even though the walkthrough addresses key pain points and challenges for various roles, it can be completed by the system admin.</span></span>

## <a name="demo-scenario"></a><span data-ttu-id="e1248-112">Демонстрационный сценарий</span><span class="sxs-lookup"><span data-stu-id="e1248-112">Demo scenario</span></span>

<span data-ttu-id="e1248-113">Юридическое лицо HQUS занимается производством динамиков класса Hi-End.</span><span class="sxs-lookup"><span data-stu-id="e1248-113">In the HQUS legal entity, high-end speakers are manufactured.</span></span> <span data-ttu-id="e1248-114">В процессе производства динамики проходят через следующие три операции.</span><span class="sxs-lookup"><span data-stu-id="e1248-114">During the manufacturing process, speakers go through the following three operations.</span></span>

- <span data-ttu-id="e1248-115">**Предварительная сборка** — собирается корпус динамика.</span><span class="sxs-lookup"><span data-stu-id="e1248-115">**Pre-assembly** – The speaker cabinet is assembled.</span></span> <span data-ttu-id="e1248-116">Материал для корпуса комплектуется на складе материалов до начала операции.</span><span class="sxs-lookup"><span data-stu-id="e1248-116">The material for the cabinet is picked in the material warehouse before the operation is started.</span></span>
- <span data-ttu-id="e1248-117">**Нанесения покрытия** — после сборки корпуса динамика на него необходимо нанести покрытие.</span><span class="sxs-lookup"><span data-stu-id="e1248-117">**Coating** – After the speaker cabinet has been assembled, it must be coated.</span></span> <span data-ttu-id="e1248-118">Эта операция выполняется поставщиком (субподрядчиком).</span><span class="sxs-lookup"><span data-stu-id="e1248-118">This operation is completed by a vendor (subcontractor).</span></span> <span data-ttu-id="e1248-119">Предварительно собранный корпус динамика отправляется субподрядчику, который наносит покрытие, вместе с двумя материалами.</span><span class="sxs-lookup"><span data-stu-id="e1248-119">The pre-assembled speaker cabinet is shipped to the coating subcontractor together with two materials.</span></span>
- <span data-ttu-id="e1248-120">**Окончательная сборка** — после того как на предварительно собранный корпус динамика было нанесено покрытие субподпрядчиком, он возвращается в HQUS на окончательную сборку.</span><span class="sxs-lookup"><span data-stu-id="e1248-120">**Finish** – After the pre-assembled speaker cabinet has been coated by the subcontractor, it's returned to the HQUS legal entity so that final assembly of the speaker can be completed.</span></span>

<span data-ttu-id="e1248-121">На следующем рисунке показаны три операции и материалы, которые в них потребляются.</span><span class="sxs-lookup"><span data-stu-id="e1248-121">The following illustration shows the three operations and the materials that they consume.</span></span>

![Предварительная сборка, нанесение покрытия и окончательная сборка, а также потребляемые материалы](./media/subcontract01_operations-materials.png)

## <a name="setup"></a><span data-ttu-id="e1248-123">Настройка</span><span class="sxs-lookup"><span data-stu-id="e1248-123">Setup</span></span>

<span data-ttu-id="e1248-124">Прежде чем начать выполнение пошагового руководства, необходимо настроить данные.</span><span class="sxs-lookup"><span data-stu-id="e1248-124">Before you start the walkthrough, you must set up the data.</span></span>

### <a name="set-up-the-finished-product"></a><span data-ttu-id="e1248-125">Настройка для готового продукта</span><span class="sxs-lookup"><span data-stu-id="e1248-125">Set up the finished product</span></span>

<span data-ttu-id="e1248-126">Эта процедура заключается в настройке выпущенного продукта D8100 "Корпус с покрытием".</span><span class="sxs-lookup"><span data-stu-id="e1248-126">This procedure takes you through the setup of released product D8100, "Coated Cabinet."</span></span>

1. <span data-ttu-id="e1248-127">Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**, чтобы открыть страницу **Сведения о выпущенном продукте**.</span><span class="sxs-lookup"><span data-stu-id="e1248-127">Select **Product information management \> Products \> Released products** to open the **Released product details** page.</span></span>
2. <span data-ttu-id="e1248-128">В поле экспресс-фильтра введите **D8100**, чтобы найти существующий выпущенный продукт.</span><span class="sxs-lookup"><span data-stu-id="e1248-128">In the quick filter field, enter **D8100** to find the existing released product.</span></span>

    ![Фильтрация для поиска выпущенного продукта D8100 на странице "Сведения о выпущенном продукте"](./media/subcontract02_filtering-released-products.png)

3. <span data-ttu-id="e1248-130">В области действий на вкладке **Инжиниринг** выберите **Маршрут**, чтобы открыть страницу **Маршрут**.</span><span class="sxs-lookup"><span data-stu-id="e1248-130">On the Action Pane, on the **Engineer** tab, select **Route** to open the **Route** page.</span></span>

    <span data-ttu-id="e1248-131">На странице **Маршрут** отображается восемь версий маршрута для выпущенного продукта D8100.</span><span class="sxs-lookup"><span data-stu-id="e1248-131">The **Route** page shows the eight route versions for released product D8100.</span></span> <span data-ttu-id="e1248-132">Восемь версий маршрута делятся на четыре маршрута на сайте 1 и сайте 5.</span><span class="sxs-lookup"><span data-stu-id="e1248-132">The eight route versions are divided among four routes on site 1 and site 5.</span></span> <span data-ttu-id="e1248-133">Маршрут 000400 используется для калькуляции себестоимости, маршрут 00041 используется, когда нанесение покрытия представляет собой внутреннюю операцию, а маршрут 00042 используется, когда нанесение покрытия представляет собой внешнюю операцию.</span><span class="sxs-lookup"><span data-stu-id="e1248-133">Route 000400 is used for costing, route 00041 is used when the Coating operation is an internal operation, and route 00042 is used when the Coating operation is an external operation.</span></span>

    ![Восемь версий маршрута на странице "Маршрут"](./media/subcontract03_route-page.png)

4. <span data-ttu-id="e1248-135">В верхней области в сетке **Версии** выберите версию маршрута **00042** для сайта **5**.</span><span class="sxs-lookup"><span data-stu-id="e1248-135">In the upper pane, in the **Versions** grid, select route version **00042** for site **5**.</span></span>
5. <span data-ttu-id="e1248-136">В нижней области на вкладке **Обзор** выберите операцию **20** (**Cbnt CtSc**) в сетке.</span><span class="sxs-lookup"><span data-stu-id="e1248-136">In the lower pane, on the **Overview** tab, select operation **20** (**Cbnt CtSc**) in the grid.</span></span>

    ![Выбранная операция 20 для версии маршрута 00042 для сайта 5](./media/subcontract04_route-version-operation.png)

6. <span data-ttu-id="e1248-138">Выберите вкладку **Общие**.</span><span class="sxs-lookup"><span data-stu-id="e1248-138">Select the **General** tab.</span></span>

    <span data-ttu-id="e1248-139">Обратите внимание, что в поле **Тип маршрута** установлено значение **Поставщик**.</span><span class="sxs-lookup"><span data-stu-id="e1248-139">Notice that the field **Route type** field is set to **Vendor**.</span></span> <span data-ttu-id="e1248-140">Это значение указывает, что операция 20 (Cbnt CtSc) представляет собой субподрядную операцию.</span><span class="sxs-lookup"><span data-stu-id="e1248-140">This value indicates that operation 20 (Cbnt CtSc) is a subcontracted operation.</span></span>

    ![Значение "Поставщик" в поле "Тип маршрута" на вкладке "Общие"](./media/subcontract05_general-tab.png)

7. <span data-ttu-id="e1248-142">Выберите вкладку **Потребности ресурса**.</span><span class="sxs-lookup"><span data-stu-id="e1248-142">Select the **Resource requirements** tab.</span></span>

    <span data-ttu-id="e1248-143">Возможности будут использоваться для поиска соответствующих ресурсов во время планирования производства.</span><span class="sxs-lookup"><span data-stu-id="e1248-143">Capabilities will be used to find an applicable resource during production scheduling.</span></span> <span data-ttu-id="e1248-144">Для операции 20 (Cbnt CtSc) обратите внимание, что требуется ресурс, который имеет две возможности: **Coating** (Нанесение покрытия) и **Coated cabinets** (Корпуса с покрытием).</span><span class="sxs-lookup"><span data-stu-id="e1248-144">For operation 20 (Cbnt CtSc), notice that a resource that has two capabilities, **Coating** and **Coated cabinets**, is required.</span></span>

    ![Возможности Coating и Coated cabinets на вкладке "Требования ресурса"](./media/subcontract06_resource-requirements-tab.png)

8. <span data-ttu-id="e1248-146">Выберите **Применимые ресурсы**, чтобы открыть диалоговое окно **Применимые ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="e1248-146">Select **Applicable resources** to open the **Applicable resources** dialog box.</span></span>

    <span data-ttu-id="e1248-147">Найдено три ресурса, соответствующих требованиям к ресурсам для операции.</span><span class="sxs-lookup"><span data-stu-id="e1248-147">Three resources are found that match the resource requirements for the operation.</span></span> <span data-ttu-id="e1248-148">Обратите внимание, что ресурс, 8851 и 8852 имеют тип **Поставщик**.</span><span class="sxs-lookup"><span data-stu-id="e1248-148">Notice that resources 8851 and 8852 are of the **Vendor** type.</span></span>

    ![Три подходящих ресурса в диалоговом окне "Применимые ресурсы"](./media/subcontract07_applicable-resources-dialog.png)

9. <span data-ttu-id="e1248-150">Выберите **OK**, чтобы закрыть диалоговое окно **Применимые ресурсы** и вернуться на страницу **Маршрут**.</span><span class="sxs-lookup"><span data-stu-id="e1248-150">Select **OK** to close the **Applicable resources** dialog box and return to the **Route** page.</span></span>
10. <span data-ttu-id="e1248-151">Закройте страницу **Маршрут**, чтобы вернуться на страницу **Сведения о выпущенном продукте**.</span><span class="sxs-lookup"><span data-stu-id="e1248-151">Close the **Route** page to return to the **Released product details** page.</span></span>

    ![Страница "Сведения о выпущенном продукте"](./media/subcontract08_released-product-details-page.png)

11. <span data-ttu-id="e1248-153">В области действий на вкладке **Инжиниринг** выберите **Версии спецификации**, чтобы открыть страницу **Версии спецификации**.</span><span class="sxs-lookup"><span data-stu-id="e1248-153">On the Action Pane, on the **Engineer** tab, select **BOM versions** to open the **BOM versions** page.</span></span>

    <span data-ttu-id="e1248-154">На странице **Версии спецификации** отображается четыре версии спецификации (BOM) для выпущенного продукта D8100.</span><span class="sxs-lookup"><span data-stu-id="e1248-154">The **BOM versions** page shows the four bill of materials (BOM) versions for released product D8100.</span></span> <span data-ttu-id="e1248-155">Спецификация 000040 используется для калькуляции себестоимости и планирования, спецификация BOM 000041 используется, если нанесение покрытия производится внутри компании, а спецификации 000042 и 000043 используются, если нанесение покрытия передается на субподряд.</span><span class="sxs-lookup"><span data-stu-id="e1248-155">BOM 000040 is used for costing and planning, BOM 000041 is used if the Coating operation is done in-house, and BOMs 000042 and 000043 are used if the Coating operation is subcontracted.</span></span>

    <span data-ttu-id="e1248-156">Обратите внимание, что номенклатура S8050 — это продукт с типом номенклатуры **Услуга**.</span><span class="sxs-lookup"><span data-stu-id="e1248-156">Notice that item S8050 is a product of the **Service** item type.</span></span> <span data-ttu-id="e1248-157">Эта номенклатура представляет работу, передаваемую на субподряд.</span><span class="sxs-lookup"><span data-stu-id="e1248-157">This item represents the subcontracted work.</span></span>

    ![Четыре версии спецификации на странице "Версии спецификации"](./media/subcontract09_bom-versions-page.png)

12. <span data-ttu-id="e1248-159">На экспресс-вкладке **Строки спецификации** выберите **Редактировать**, чтобы открыть диалоговое окно **Редактировать строку спецификации**.</span><span class="sxs-lookup"><span data-stu-id="e1248-159">On the **Bill of materials lines** FastTab, select **Edit** to open the **Edit BOM line** dialog box.</span></span>

    <span data-ttu-id="e1248-160">При создании и оценке производственного заказа для выпущенного продукта D8100 автоматически создается заказ на покупку для номенклатуры S8050.</span><span class="sxs-lookup"><span data-stu-id="e1248-160">When a production order is created and estimated for released product D8100, a purchase order will be automatically generated for item S8050.</span></span> <span data-ttu-id="e1248-161">Этот заказ на покупку будет связан с производственным заказом.</span><span class="sxs-lookup"><span data-stu-id="e1248-161">This purchase order will be linked to the production order.</span></span> <span data-ttu-id="e1248-162">Для автоматического создания заказов на покупку в поле **Тип строки** должно быть установлено значение **Поставщик**, и должен быть выбран счет поставщика для субподрядчика.</span><span class="sxs-lookup"><span data-stu-id="e1248-162">For purchase orders to be automatically generated, the **Line type** field must be set to **Vendor**, and the vendor account for the subcontractor must be selected.</span></span> <span data-ttu-id="e1248-163">В данном случае счет поставщика — US-801.</span><span class="sxs-lookup"><span data-stu-id="e1248-163">In this case, the vendor account is US-801.</span></span>

    <span data-ttu-id="e1248-164">Обратите внимание, что строка спецификации связана с операцией нанесения покрытия через номер операции (в данном случае 20).</span><span class="sxs-lookup"><span data-stu-id="e1248-164">Notice that the BOM line is connected to the Coating operation through the operation number (in this case, 20).</span></span>

    ![Диалоговое окно "Редактировать строку спецификации"](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a><span data-ttu-id="e1248-166">Создание пароля для работников склада</span><span class="sxs-lookup"><span data-stu-id="e1248-166">Create a password for warehouse workers</span></span>

<span data-ttu-id="e1248-167">Необходимо определить пароль для работников склада, использующих карманные устройства.</span><span class="sxs-lookup"><span data-stu-id="e1248-167">You must define a password for the warehouse workers who use the hand-held device.</span></span>

1. <span data-ttu-id="e1248-168">Выберите **Управление складом \> Установка \> Работник**, чтобы открыть страницу **Пользователь работы**.</span><span class="sxs-lookup"><span data-stu-id="e1248-168">Select **Warehouse management \> Setup \> Worker** to open the **Work users** page.</span></span>
2. <span data-ttu-id="e1248-169">На экспресс-вкладке **Пользователи** выберите строку для пользователя **51**.</span><span class="sxs-lookup"><span data-stu-id="e1248-169">On the **Users** FastTab, select the row for user **51**.</span></span>

    ![Страница "Пользователь работы"](./media/subcontract11_work-users-page.png)

3. <span data-ttu-id="e1248-171">Выберите **Сброс пароля**.</span><span class="sxs-lookup"><span data-stu-id="e1248-171">Select **Reset password**.</span></span>
4. <span data-ttu-id="e1248-172">В поле **Пароль** и **Подтверждение пароля** введите **1**.</span><span class="sxs-lookup"><span data-stu-id="e1248-172">In the **Password** and **Confirm password** fields, enter **1**.</span></span>
5. <span data-ttu-id="e1248-173">Выберите **Установить пароль**.</span><span class="sxs-lookup"><span data-stu-id="e1248-173">Select **Set password**.</span></span>

## <a name="step-by-step-walkthrough"></a><span data-ttu-id="e1248-174">Пошаговое руководство</span><span class="sxs-lookup"><span data-stu-id="e1248-174">Step-by-step walkthrough</span></span>

<span data-ttu-id="e1248-175">**Сценарий и вводные сведения**</span><span class="sxs-lookup"><span data-stu-id="e1248-175">**Scenario and background**</span></span>

<span data-ttu-id="e1248-176">Создается производственный заказ на 10 штук продукта D8100 "Корпус с покрытием".</span><span class="sxs-lookup"><span data-stu-id="e1248-176">A production order of 10 pieces is created for product D8100, "Coated Cabinet."</span></span> <span data-ttu-id="e1248-177">Нанесение покрытия на корпуса — это передаваемая на субподряд операция, которую выполняет поставщик US-801 — компания Perfect Coating Solutions.</span><span class="sxs-lookup"><span data-stu-id="e1248-177">The coating of the cabinets is a sub-contracted operation that is done at vendor US-801, Perfect Coating Solutions.</span></span> <span data-ttu-id="e1248-178">Производственный заказ состоит из трех операций.</span><span class="sxs-lookup"><span data-stu-id="e1248-178">The production order consists of three operations.</span></span> <span data-ttu-id="e1248-179">В первой операции производится предварительная сборка корпуса; это внутренняя операция.</span><span class="sxs-lookup"><span data-stu-id="e1248-179">In the first operation, the cabinet is pre-assembled as an in-house operation.</span></span> <span data-ttu-id="e1248-180">Материал для предварительной сборки запускается для комплектации на складе сырья.</span><span class="sxs-lookup"><span data-stu-id="e1248-180">The material for the pre-assembly is released for picking in the raw material warehouse.</span></span> <span data-ttu-id="e1248-181">По завершении предварительной сборки предварительно собранный корпус отправляется компании Perfect Coating Solutions вместе с двумя материалами, необходимыми для операции нанесения покрытия.</span><span class="sxs-lookup"><span data-stu-id="e1248-181">After the pre-assembly is completed, the pre-assembled cabinet is sent to Perfect Coating Solutions together with two materials that are required for the Coating operation.</span></span> <span data-ttu-id="e1248-182">При получении корпуса с покрытием обратно от поставщика он проходит операцию окончательной сборки (внутри компании), прежде чем производится его приемка.</span><span class="sxs-lookup"><span data-stu-id="e1248-182">When the coated cabinet is received back from the vendor, it goes through a final in-house assembly operation before it's reported as finished.</span></span>

1. <span data-ttu-id="e1248-183">Выберите **Управление производством \> Производственные заказы \> Все производственные заказы**, чтобы открыть страницу **Все производственные заказы**.</span><span class="sxs-lookup"><span data-stu-id="e1248-183">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
2. <span data-ttu-id="e1248-184">В области действий выберите **Новый производственный заказ**, чтобы открыть диалоговое окно **Создать производственный заказ**.</span><span class="sxs-lookup"><span data-stu-id="e1248-184">On the Action Pane, select **New production order** to open the **Create production order** dialog box.</span></span>

    ![Диалоговое окно "Создать производственный заказ"](./media/subcontract12_create-production-order-dialog.png)

3. <span data-ttu-id="e1248-186">В поле **Код номенклатуры** выберите **D8100**.</span><span class="sxs-lookup"><span data-stu-id="e1248-186">In the **Item number** field, select **D8100**.</span></span>
4. <span data-ttu-id="e1248-187">После выбора кода номенклатуры появляются поля для складских аналитик.</span><span class="sxs-lookup"><span data-stu-id="e1248-187">After you select the item number, fields for the inventory dimensions appear.</span></span> <span data-ttu-id="e1248-188">В поле **Цвет** выберите **Хром**.</span><span class="sxs-lookup"><span data-stu-id="e1248-188">In the **Color** field, select **Chrome**.</span></span>

    <span data-ttu-id="e1248-189">Появится окно сообщения с вопросом, следует ли вставить активные версии спецификации и маршрута.</span><span class="sxs-lookup"><span data-stu-id="e1248-189">A message box appears that asks whether the active versions for the BOM and route should be inserted.</span></span>

    ![Окно сообщения](./media/subcontract13_message-box.png)

5. <span data-ttu-id="e1248-191">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="e1248-191">Select **Yes**.</span></span> 

    <span data-ttu-id="e1248-192">В диалоговом окне **Создать производственный заказ** в полях **Номер спецификации** и **Номер маршрута** автоматически выбираются активные версии спецификации и маршрута для продукта D8100.</span><span class="sxs-lookup"><span data-stu-id="e1248-192">In the **Create production order** dialog box, the active versions of the BOM and route for product D8100 are automatically selected in the **BOM number** and **Route number** fields, respectively.</span></span> <span data-ttu-id="e1248-193">В данном случае выбраны спецификация **000040** и маршрут **000040**.</span><span class="sxs-lookup"><span data-stu-id="e1248-193">In this case, BOM **000040** and route **000040** are selected.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="e1248-194">И в случае спецификации, и в случае маршрута версия 000040 используется для калькуляции себестоимости и планирования.</span><span class="sxs-lookup"><span data-stu-id="e1248-194">For both the BOM and the route, version 000040 is used for costing and planning.</span></span>

6. <span data-ttu-id="e1248-195">В поле **Сайт** выберите **5**.</span><span class="sxs-lookup"><span data-stu-id="e1248-195">In the **Site** field, select **5**.</span></span>
7. <span data-ttu-id="e1248-196">В поле **Склад** выберите **51**.</span><span class="sxs-lookup"><span data-stu-id="e1248-196">In the **Warehouse** field, select **51**.</span></span>
8. <span data-ttu-id="e1248-197">В полях **Номер спецификации** и **Номер маршрута** измените автоматически выбранное значение на **000042**.</span><span class="sxs-lookup"><span data-stu-id="e1248-197">In the **BOM number** and **Route number** fields, change the value that was automatically selected to **000042**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e1248-198">И в случае спецификации, и в случае маршрута версия 000042 используется для передачи нанесения покрытия на корпус на субподряд поставщику US-801.</span><span class="sxs-lookup"><span data-stu-id="e1248-198">For both the BOM and the route, version 000042 is used to subcontract the coating of the cabinet to vendor US-801.</span></span>

    ![Значения, заданные в диалоговом окне "Создать производственный заказ"](./media/subcontract14_create-production-order-dialog-set.png)

9. <span data-ttu-id="e1248-200">Выберите **Создать**,чтобы создать производственный заказ и вернуться на страницу **Все производственные заказы**.</span><span class="sxs-lookup"><span data-stu-id="e1248-200">Select **Create** to create the production order and return to the **All production orders** page.</span></span>

    ![Новый производственный заказ на странице "Все производственные заказы"](./media/subcontract15_new-production-order.png)

10. <span data-ttu-id="e1248-202">В области действий на вкладке **Производственный заказ** выберите **Оценка**, чтобы открыть диалоговое окно **Оценка**.</span><span class="sxs-lookup"><span data-stu-id="e1248-202">On the Action Pane, on the **Production order** tab, select **Estimate** to open the **Estimate** dialog box.</span></span>

    ![Диалоговое окно "Оценка"](./media/subcontract16_estimate-dialog.png)

11. <span data-ttu-id="e1248-204">Выберите **ОК**,чтобы подтвердить оценку и вернуться на страницу **Все производственные заказы**.</span><span class="sxs-lookup"><span data-stu-id="e1248-204">Select **OK** to confirm the estimate and return to the **All production orders** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e1248-205">При оценке производственного заказа создается заказа на покупку номенклатуры "услуга" S8050 для поставщика US-801.</span><span class="sxs-lookup"><span data-stu-id="e1248-205">When the production order is estimated, the purchase order for service item S8050 is generated for vendor US-801.</span></span>

12. <span data-ttu-id="e1248-206">В области действий на вкладке **Производственный заказ** выберите **Спецификация**, чтобы открыть страницу **Спецификация**, где можно просмотреть строки спецификации для производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="e1248-206">On the Action Pane, on the **Production order** tab, select **BOM** to open the **BOM** page, where you can view the BOM lines for the production order.</span></span>

    <span data-ttu-id="e1248-207">Для номенклатуры "услуга" S8050 обратите внимание, что имеется ссылка на заказ на покупку, созданный при оценке производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="e1248-207">For service item S8050, notice that there is a reference to the purchase order that was generated when the production order was estimated.</span></span>

    ![Строки спецификации производственного заказа на странице "Спецификация"](./media/subcontract17_production-order-bom-lines.png)

13. <span data-ttu-id="e1248-209">Закройте страницу **Спецификация**, чтобы вернуться на страницу **Все производственные заказы**.</span><span class="sxs-lookup"><span data-stu-id="e1248-209">Close the **BOM** page to return to the **All production orders** page.</span></span>
14. <span data-ttu-id="e1248-210">В области действий на вкладке **План** выберите **Планирование заданий**, чтобы открыть диалоговое окно **Планирование заданий**.</span><span class="sxs-lookup"><span data-stu-id="e1248-210">On the Action Pane, on the **Schedule** tab, select **Schedule jobs** to open the **Job scheduling** dialog box.</span></span>
15. <span data-ttu-id="e1248-211">Укажите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e1248-211">Specify the following values:</span></span>

    - <span data-ttu-id="e1248-212">В поле **Направление планирования** выберите **Начиная с завтрашнего дня**.</span><span class="sxs-lookup"><span data-stu-id="e1248-212">In the **Scheduling direction** field, select **Forward from tomorrow**.</span></span>
    - <span data-ttu-id="e1248-213">Установите для параметра **Ограничение по мощности** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="e1248-213">Set the **Finite capacity** option to **Yes**.</span></span>

    ![Диалоговое окно "Планирование заданий"](./media/subcontract18_job-scheduling-dialog.png)

16. <span data-ttu-id="e1248-215">Выберите **OK**, чтобы закрыть диалоговое окно **Планирование заданий** и вернуться на страницу **Все производственные заказы**.</span><span class="sxs-lookup"><span data-stu-id="e1248-215">Select **OK** to close the **Job scheduling** dialog box and return to the **All production orders** page.</span></span>
17. <span data-ttu-id="e1248-216">В области действий на вкладке **План** выберите **Гант**, чтобы открыть страницу **Диаграмма Ганта — Представление ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="e1248-216">On the Action Pane, on the **Schedule** tab, select **Gantt** to open the **Gantt chart - Resource view** page.</span></span>

    <span data-ttu-id="e1248-217">Диаграмма Ганта представляет визуальный обзор того, как производственные задания планируются на ресурсах.</span><span class="sxs-lookup"><span data-stu-id="e1248-217">The Gantt chart provides a visual overview of how the production jobs are scheduled on the resources.</span></span> <span data-ttu-id="e1248-218">Обратите внимание, что внешняя операция нанесения покрытия состоит из трех заданий: задания "обработка", задания "транспортировка" и задания "время в очереди".</span><span class="sxs-lookup"><span data-stu-id="e1248-218">Notice that the external Coating operation consists of three jobs: a process job, a transport job, and a queue time job.</span></span>

    ![Диаграмма Ганта на странице "Диаграмма Ганта — Представление ресурсов"](./media/subcontract19_gantt-chart.png)

18. <span data-ttu-id="e1248-220">Закройте страницу **Диаграмма Ганта — Представление ресурсов**, чтобы вернуться на страницу **Все производственные заказы**.</span><span class="sxs-lookup"><span data-stu-id="e1248-220">Close the **Gantt chart - Resource view** page to return to the **All production orders** page.</span></span>
19. <span data-ttu-id="e1248-221">В области действий на вкладке **Производственный заказ** выберите **Выпуск**, чтобы открыть диалоговое окно **Выпуск**.</span><span class="sxs-lookup"><span data-stu-id="e1248-221">On the Action Pane, on the **Production order** tab, select **Release** to open the **Release** dialog box.</span></span>

    ![Диалоговое окно "Выпуск"](./media/subcontract20_release-dialog.png)

20. <span data-ttu-id="e1248-223">Выберите **OK**, чтобы закрыть диалоговое окно **Запуск в производство**.</span><span class="sxs-lookup"><span data-stu-id="e1248-223">Select **OK** to close the **Release** dialog box.</span></span>
21. <span data-ttu-id="e1248-224">Выберите **Управление производством \> Периодические задачи \> Выпуск на склад \> Автоматический выпуск строк спецификации и формулы**, чтобы открыть диалоговое окно **Автоматический выпуск строк спецификации и формулы**.</span><span class="sxs-lookup"><span data-stu-id="e1248-224">Select **Production control \> Periodic tasks \> Release to warehouse \> Automatic release of BOM and formula lines** to open the **Automatic release of BOM and formula lines** dialog box.</span></span>

    ![Диалоговое окно "Автоматический выпуск строк спецификации и формулы"](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. <span data-ttu-id="e1248-226">Выберите **OK**, чтобы запустить задание "Автоматический выпуск строк спецификации и формулы".</span><span class="sxs-lookup"><span data-stu-id="e1248-226">Select **OK** to run the Automatic release of BOM and formula lines job.</span></span>

    <span data-ttu-id="e1248-227">Это задание выпускает на склад работу по комплектации сырья.</span><span class="sxs-lookup"><span data-stu-id="e1248-227">This job releases pick work for raw materials to the warehouse.</span></span>

23. <span data-ttu-id="e1248-228">Выберите **Управление производством \> Производственные заказы \> Все производственные заказы**, чтобы открыть страницу **Все производственные заказы**.</span><span class="sxs-lookup"><span data-stu-id="e1248-228">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
24. <span data-ttu-id="e1248-229">С помощью поля экспресс-фильтра выберите производственный заказ, над которым вы работали.</span><span class="sxs-lookup"><span data-stu-id="e1248-229">Use the quick filter field to select the production order that you've been working on.</span></span>
25. <span data-ttu-id="e1248-230">В области действий на вкладке **Склад** выберите **Сведения о работе**, чтобы открыть страницу **Работа**.</span><span class="sxs-lookup"><span data-stu-id="e1248-230">On the Action Pane, on the **Warehouse** tab, select **Work details** to open the **Work** page.</span></span>

    <span data-ttu-id="e1248-231">Обратите внимание, что на странице отображается два набора работ для комплектации сырья.</span><span class="sxs-lookup"><span data-stu-id="e1248-231">Notice that the page shows two sets of work for raw material picking.</span></span> <span data-ttu-id="e1248-232">Первая работа относится к материалам M8100 и M8101.</span><span class="sxs-lookup"><span data-stu-id="e1248-232">The first work is for materials M8100 and M8101.</span></span> <span data-ttu-id="e1248-233">Эти материалы потребляются операцией 10.</span><span class="sxs-lookup"><span data-stu-id="e1248-233">These materials are consumed by operation 10.</span></span> <span data-ttu-id="e1248-234">Вторая работа относится к материалам M8202 и M8250.</span><span class="sxs-lookup"><span data-stu-id="e1248-234">The second work is for materials M8202 and M8250.</span></span> <span data-ttu-id="e1248-235">Данные материалы потребляются операцией 20, которая является субподрядной операцией.</span><span class="sxs-lookup"><span data-stu-id="e1248-235">These materials are consumed by operation 20, which is the subcontracted operation.</span></span>

    ![Два набора работы для комплектации сырья на странице "Работа"](./media/subcontract22_work-page.png)

26. <span data-ttu-id="e1248-237">Запустите приложение склада для обработки работы склада для операции 10.</span><span class="sxs-lookup"><span data-stu-id="e1248-237">Start the warehouse app to process the warehouse work for operation 10.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. <span data-ttu-id="e1248-238">Выберите **Управление производством \> Производственные заказы \> Все производственные заказы**, чтобы открыть страницу **Все производственные заказы**.</span><span class="sxs-lookup"><span data-stu-id="e1248-238">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
28. <span data-ttu-id="e1248-239">С помощью поля экспресс-фильтра выберите производственный заказ, над которым вы работали.</span><span class="sxs-lookup"><span data-stu-id="e1248-239">Use the quick filter field to select the production order that you've been working on.</span></span>
29. <span data-ttu-id="e1248-240">В области действий на вкладке **Производственный заказ** выберите **Начало**, чтобы открыть диалоговое окно **Начало**.</span><span class="sxs-lookup"><span data-stu-id="e1248-240">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
30. <span data-ttu-id="e1248-241">На вкладке **Общие** укажите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e1248-241">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="e1248-242">В поле **От операции №**</span><span class="sxs-lookup"><span data-stu-id="e1248-242">In the **From Oper. No.**</span></span> <span data-ttu-id="e1248-243">выберите **10**.</span><span class="sxs-lookup"><span data-stu-id="e1248-243">field, select **10**.</span></span>
    - <span data-ttu-id="e1248-244">В поле **До операции №**</span><span class="sxs-lookup"><span data-stu-id="e1248-244">In the **To Oper. No.**</span></span> <span data-ttu-id="e1248-245">выберите **10**.</span><span class="sxs-lookup"><span data-stu-id="e1248-245">field, select **10**.</span></span>

    ![Значения, заданные на вкладке "Общие"](./media/subcontract23_start-dialog.png)

31. <span data-ttu-id="e1248-247">Выберите **OK**, чтобы закрыть диалоговое окно **Начало** и вернуться на страницу **Все производственные заказы**.</span><span class="sxs-lookup"><span data-stu-id="e1248-247">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="e1248-248">Обратите внимание, что статус производственного заказа теперь **Начато**.</span><span class="sxs-lookup"><span data-stu-id="e1248-248">Notice that the status of the production order is now **Started**.</span></span> <span data-ttu-id="e1248-249">Материалы для операции 10 потребляются путем автоматической разноски журнала ведомостей комплектации.</span><span class="sxs-lookup"><span data-stu-id="e1248-249">The materials for operation 10 are consumed by an automatic posting of the picking list journal.</span></span> <span data-ttu-id="e1248-250">Потребление времени для операции 10 учитывается путем автоматической разноски журнала карт маршрутов.</span><span class="sxs-lookup"><span data-stu-id="e1248-250">Time consumption for operation 10 is accounted for by an automatic posting of a route card journal.</span></span>

32. <span data-ttu-id="e1248-251">Запустите приложение склада для обработки работы склада для операции 20.</span><span class="sxs-lookup"><span data-stu-id="e1248-251">Start the warehouse app to process the warehouse work for operation 20.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. <span data-ttu-id="e1248-252">В области действий на вкладке **Производственный заказ** выберите **Начало**, чтобы открыть диалоговое окно **Начало**.</span><span class="sxs-lookup"><span data-stu-id="e1248-252">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
34. <span data-ttu-id="e1248-253">На вкладке **Общие** укажите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e1248-253">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="e1248-254">В поле **От операции №**</span><span class="sxs-lookup"><span data-stu-id="e1248-254">In the **From Oper. No.**</span></span> <span data-ttu-id="e1248-255">выберите **20**.</span><span class="sxs-lookup"><span data-stu-id="e1248-255">field, select **20**.</span></span>
    - <span data-ttu-id="e1248-256">В поле **До операции №**</span><span class="sxs-lookup"><span data-stu-id="e1248-256">In the **To Oper. No.**</span></span> <span data-ttu-id="e1248-257">выберите **20**.</span><span class="sxs-lookup"><span data-stu-id="e1248-257">field, select **20**.</span></span>
    - <span data-ttu-id="e1248-258">В поле **Количество** введите **10**.</span><span class="sxs-lookup"><span data-stu-id="e1248-258">In the **Quantity** field, enter **10**.</span></span>
    - <span data-ttu-id="e1248-259">Установите для параметра **Разнести отборочную накладную** значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="e1248-259">Set the **Post picking list now** option to **No**.</span></span>

    ![Значения, заданные на вкладке "Общие"](./media/subcontract24_general-tab.png)

35. <span data-ttu-id="e1248-261">Выберите **OK**, чтобы закрыть диалоговое окно **Начало** и вернуться на страницу **Все производственные заказы**.</span><span class="sxs-lookup"><span data-stu-id="e1248-261">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="e1248-262">Создается ведомость комплектации для материалов, используемых в операции нанесения покрытия, и для номенклатуры "услуга".</span><span class="sxs-lookup"><span data-stu-id="e1248-262">A picking list is created for the materials that are used for the Coating operation, and for the service item.</span></span> <span data-ttu-id="e1248-263">Номенклатура "услуга" представляет стоимость субподрядной операции.</span><span class="sxs-lookup"><span data-stu-id="e1248-263">The service item represents the cost of the subcontracted operation.</span></span>

36. <span data-ttu-id="e1248-264">В области действий на вкладке **Просмотр** выберите **Лист подбора**, чтобы открыть страницу **Лист подбора**.</span><span class="sxs-lookup"><span data-stu-id="e1248-264">On the Action Pane, on the **View** tab, select **Picking list** to open the **Picking list** page.</span></span>
37. <span data-ttu-id="e1248-265">Выберите ведомость комплектации, которая не разнесена, а затем выберите номер журнала для просмотра строк журнала.</span><span class="sxs-lookup"><span data-stu-id="e1248-265">Select the picking list that isn't posted, and then select the journal number to view the journal lines.</span></span>

    ![Строки журнала на странице "Лист подбора"](./media/subcontract25_picking-list.png)

38. <span data-ttu-id="e1248-267">В области действий выберите **Печать** \> **Отчет по листу подбора**, чтобы открыть диалоговое окно **Отчет по листу подбора**.</span><span class="sxs-lookup"><span data-stu-id="e1248-267">On the Action Pane, select **Print** \> **Picking list report** to open the **Picking list report** dialog box.</span></span>
39. <span data-ttu-id="e1248-268">Установите для параметра **Использовать макет транспортной накладной** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="e1248-268">Set the **Use delivery note layout** option to **Yes**.</span></span>

    ![Диалоговое окно "Отчет по листу подбора"](./media/subcontract26_picking-list-report-dialog.png)

40. <span data-ttu-id="e1248-270">Нажмите **ОК**, чтобы создать отчет **Лист подбора**.</span><span class="sxs-lookup"><span data-stu-id="e1248-270">Select **OK** to generate a **Picking list** report.</span></span>

    <span data-ttu-id="e1248-271">В данном случае транспортная накладная для поставщика печатается из журнала листов подбора производства.</span><span class="sxs-lookup"><span data-stu-id="e1248-271">In this case, a vendor delivery note is printed from the production picking list journal.</span></span> <span data-ttu-id="e1248-272">В транспортной накладной указываются материалы, отправляемые поставщику, который будет выполнять операцию нанесения покрытия.</span><span class="sxs-lookup"><span data-stu-id="e1248-272">The delivery note specifies the materials that are shipped to the vendor who will do the Coating operation.</span></span>

    ![Отчет по листу подбора](./media/subcontract27_picking-list-report.png)

41. <span data-ttu-id="e1248-274">Закройте отчет **Лист подбора**, чтобы вернуться на страницу **Лист подбора**.</span><span class="sxs-lookup"><span data-stu-id="e1248-274">Close the **Picking list** report to return to the **Picking list** page.</span></span>
42. <span data-ttu-id="e1248-275">В области действий выберите **Разнести**, чтобы открыть диалоговое окно **Разноска журнала**.</span><span class="sxs-lookup"><span data-stu-id="e1248-275">On the Action Pane, select **Post** to open the **Post journal** dialog box.</span></span>

    ![Диалоговое окно "Разноска журнала"](./media/subcontract28_post-journal-dialog.png)

43. <span data-ttu-id="e1248-277">Выберите **OK**, чтобы закрыть диалоговое окно **Разноска журнала**.</span><span class="sxs-lookup"><span data-stu-id="e1248-277">Select **OK** to close the **Post journal** dialog box.</span></span>
44. <span data-ttu-id="e1248-278">Откройте заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="e1248-278">Open the purchase order.</span></span>

    ![Страница "Заказ на покупку"](./media/subcontract29_purchase-order-page.png)

45. <span data-ttu-id="e1248-280">В области действий на вкладке **Покупка** выберите **Подтвердить**.</span><span class="sxs-lookup"><span data-stu-id="e1248-280">On the Action Pane, on the **Purchase** tab, select **Confirm**.</span></span>
46. <span data-ttu-id="e1248-281">Выберите **Разнести**, чтобы открыть диалоговое окно **Разноска журнала**.</span><span class="sxs-lookup"><span data-stu-id="e1248-281">Select **Post** to open the **Post journal** dialog box.</span></span>
47. <span data-ttu-id="e1248-282">Выберите **OK**, чтобы закрыть диалоговое окно **Разноска журнала** и вернуться на страницу **Заказ на покупку**.</span><span class="sxs-lookup"><span data-stu-id="e1248-282">Select **OK** to close the **Post journal** dialog box and return to the **Purchase order** page.</span></span>
48. <span data-ttu-id="e1248-283">Измените цену за единицу с **33** на **40**.</span><span class="sxs-lookup"><span data-stu-id="e1248-283">Change the unit price from **33** to **40**.</span></span>

    ![Изменение цены за единицу на странице "Заказ на покупку"](./media/subcontract30_unit-price.png)

49. <span data-ttu-id="e1248-285">Подтвердите заказ на покупку еще раз.</span><span class="sxs-lookup"><span data-stu-id="e1248-285">Confirm the purchase order again.</span></span>
50. <span data-ttu-id="e1248-286">Поступление продуктов.</span><span class="sxs-lookup"><span data-stu-id="e1248-286">Product receipt.</span></span>

    ![Диалоговое окно "Разноска поступления продуктов"](./media/subcontract31_posting-product-receipt-dialog.png)

51. <span data-ttu-id="e1248-288">Накладная по покупке.</span><span class="sxs-lookup"><span data-stu-id="e1248-288">Purchase invoice.</span></span>
52. <span data-ttu-id="e1248-289">Обновите статус сопоставления.</span><span class="sxs-lookup"><span data-stu-id="e1248-289">Update the match status.</span></span>

    ![Страница "Накладная поставщика"](./media/subcontract32_vendor-invoice-page.png)

53. <span data-ttu-id="e1248-291">Приемка.</span><span class="sxs-lookup"><span data-stu-id="e1248-291">Report as finished.</span></span>

    ![Диалоговое окно "Приемка"](./media/subcontract33_report-as-finished-dialog.png)

54. <span data-ttu-id="e1248-293">Конец.</span><span class="sxs-lookup"><span data-stu-id="e1248-293">End.</span></span>

    ![Диалоговое окно "Конец"](./media/subcontract34_end-dialog.png)

55. <span data-ttu-id="e1248-295">Сравнение стоимости.</span><span class="sxs-lookup"><span data-stu-id="e1248-295">Cost comparison.</span></span>

    ![Диаграммы сравнения стоимости](./media/subcontract35_cost-comparison-charts.png)

<span data-ttu-id="e1248-297">Отсутствует настройка в данных.</span><span class="sxs-lookup"><span data-stu-id="e1248-297">Missing setup in data.</span></span>
