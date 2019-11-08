---
title: Добавление ошибки в заказ на работу
description: В этом разделе описывается добавление регистраций неисправностей в заказы на работу в модуле "Управление активами".
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2b58cc31578d7bb102c6b5aa8b4ce2d6cfe8c893
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626209"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="56805-103">Добавление ошибки в заказ на работу</span><span class="sxs-lookup"><span data-stu-id="56805-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="56805-104">Можно добавить неисправности, настроенные в конструкторе неисправностей, в заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="56805-104">You can add faults that were set up in the fault designer to a work order.</span></span> <span data-ttu-id="56805-105">Одна или несколько записей о сбоях должны быть связаны с типами активов, которые используются для актива, выбранного в заказе на работу.</span><span class="sxs-lookup"><span data-stu-id="56805-105">One or more fault records must be connected to the asset types that are used for the asset that is selected in the work order.</span></span> <span data-ttu-id="56805-106">Дополнительные сведения о настройке см. в разделе [Управление ошибками](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="56805-106">For more information about the setup, see [Fault management](../setup-for-work-orders/fault-management.md).</span></span>

1. <span data-ttu-id="56805-107">Выберите **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="56805-107">Select **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="56805-108">Выберите заказ на работу, для которого необходимо выполнить регистрацию неисправности, а затем в области действий на вкладке **заказ на работу** в группе **Актив** выберите **сбой актива**.</span><span class="sxs-lookup"><span data-stu-id="56805-108">Select the work order to make a fault registration on, and then, on the Action Pane, on the **Work order** tab, in the **Asset** group, select **Asset fault**.</span></span>

3. <span data-ttu-id="56805-109">На экспресс-вкладке **Признаки** выберите **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="56805-109">On the **Symptoms** FastTab, select **Add line**.</span></span> <span data-ttu-id="56805-110">Последовательной номер ошибки автоматически вводится в поле **Ошибка**.</span><span class="sxs-lookup"><span data-stu-id="56805-110">A sequential fault number is automatically entered in the **Fault** field.</span></span>

4. <span data-ttu-id="56805-111">Выберите соответствующий симптом в поле **Симптом неисправности**.</span><span class="sxs-lookup"><span data-stu-id="56805-111">In the **Fault symptom** field, select the relevant symptom.</span></span>

5. <span data-ttu-id="56805-112">В полях **Область неисправности** и **тип неисправности** выберите соответствующие значения.</span><span class="sxs-lookup"><span data-stu-id="56805-112">In the **Fault area** and **Fault type** fields, select the appropriate values.</span></span>

6. <span data-ttu-id="56805-113">В поле **Дата неисправности** автоматически вставляется текущая дата.</span><span class="sxs-lookup"><span data-stu-id="56805-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="56805-114">Можно выбрать другую дату, при необходимости.</span><span class="sxs-lookup"><span data-stu-id="56805-114">You can select a different date as you require.</span></span>

7. <span data-ttu-id="56805-115">На экспресс-вкладке **Причины для выбранного симптома** добавьте строку, описывающую причину проблемы.</span><span class="sxs-lookup"><span data-stu-id="56805-115">On the **Causes for selected symptom** FastTab, add a line to describe the cause of the issue.</span></span>

8. <span data-ttu-id="56805-116">На экспресс-вкладке **Меры устранения для выбранного симптома** добавьте строку, описывающую возможный способ устранения проблемы.</span><span class="sxs-lookup"><span data-stu-id="56805-116">On the **Remedies for selected symptom** FastTab, add a line to describe a possible solution to the issue.</span></span>

9. <span data-ttu-id="56805-117">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="56805-117">Select **Save**.</span></span>

<span data-ttu-id="56805-118">Иллюстрация ниже показывает пример регистрации неисправностей.</span><span class="sxs-lookup"><span data-stu-id="56805-118">The illustration below shows an example of a fault registration.</span></span>

![Рисунок 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="56805-120">Просмотр неисправностей активов</span><span class="sxs-lookup"><span data-stu-id="56805-120">View asset faults</span></span>

<span data-ttu-id="56805-121">В списке **Ошибки по активам** можно получить обзор всех ошибок, зарегистрированных для активов.</span><span class="sxs-lookup"><span data-stu-id="56805-121">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="56805-122">На странице списка **Ошибки по активам** можно получить обзор всех неисправностей, зарегистрированных для активов.</span><span class="sxs-lookup"><span data-stu-id="56805-122">On the **Asset faults** list page, you can get an overview of all faults that have been registered on assets.</span></span> <span data-ttu-id="56805-123">Выберите **Управление активами** > **Запросы** > **Ошибка актива** > **Ошибки активов**, чтобы открыть страницу.</span><span class="sxs-lookup"><span data-stu-id="56805-123">To open the page, select **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="56805-124">Печать отчет о неисправностях активов</span><span class="sxs-lookup"><span data-stu-id="56805-124">Print asset fault report</span></span>

<span data-ttu-id="56805-125">На странице списка **Все активы** можно напечатать отчет об ошибках активов, отображающий все регистрации ошибок, а также графический обзор статистики ошибок.</span><span class="sxs-lookup"><span data-stu-id="56805-125">From the **All assets** list page, you can print an asset fault report that shows all fault registrations and a graphical overview of fault statistics.</span></span>

1. <span data-ttu-id="56805-126">Выберите **Управление активами** > **Общие** > **Активы** > **Все активы**.</span><span class="sxs-lookup"><span data-stu-id="56805-126">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="56805-127">Выбрать актив для печати отчета о неисправностях.</span><span class="sxs-lookup"><span data-stu-id="56805-127">Select the asset to print a fault report for.</span></span>

3. <span data-ttu-id="56805-128">В области действий на вкладке **Общие** в группе **Отчеты** выберите **Ошибка актива**.</span><span class="sxs-lookup"><span data-stu-id="56805-128">On the Action Pane, on the **General** tab, in the **Reports** group, select **Asset fault**.</span></span>

4. <span data-ttu-id="56805-129">Введите указанный период или выберите типа ошибки.</span><span class="sxs-lookup"><span data-stu-id="56805-129">Enter a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="56805-130">Выберите **OK**, чтобы напечатать отчет.</span><span class="sxs-lookup"><span data-stu-id="56805-130">Select **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="56805-131">Чтобы напечатать отчет об ошибке для нескольких активов или типов активов, выберите **Управление активами** > **Отчеты** > **Активы** > **Ошибка актива**.</span><span class="sxs-lookup"><span data-stu-id="56805-131">To print a fault report for several assets or asset types, select **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

