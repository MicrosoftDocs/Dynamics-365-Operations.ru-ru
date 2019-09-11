---
title: Добавление ошибки в заказ на работу
description: В этом разделе описывается добавление регистраций неисправностей в заказы на работу в модуле "Управление активами".
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875866"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="e9a5e-103">Добавление ошибки в заказ на работу</span><span class="sxs-lookup"><span data-stu-id="e9a5e-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="e9a5e-104">Можно добавить неисправности, настроенные в конструкторе неисправностей, в заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-104">You can add faults set up in the fault designer to a work order.</span></span> <span data-ttu-id="e9a5e-105">Актив, выбранный в заказе на работу, должен содержать типы активов, к которым привязаны одна или несколько записей о сбоях.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-105">The asset selected in the work order must contain asset types that have one or more fault records connected to it.</span></span> <span data-ttu-id="e9a5e-106">Дополнительные сведения о настройке см. в разделе [Управление ошибками](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="e9a5e-106">Read more about setup in the [Fault management](../setup-for-work-orders/fault-management.md) section.</span></span>

1. <span data-ttu-id="e9a5e-107">Щелкните **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-107">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="e9a5e-108">В списке выберите заказ на работу, для которого необходимо выполнить регистрацию неисправности, и выберите пункт **Ошибка актива**.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-108">In the list, select the work order on which you want to make a fault registration and click **Asset fault**.</span></span>

3. <span data-ttu-id="e9a5e-109">На экспресс-вкладке **Признаки** щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-109">On the **Symptoms** FastTab, click **Add line**.</span></span> <span data-ttu-id="e9a5e-110">Последовательной номер ошибки автоматически вставляется в поле **Ошибка**.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-110">A sequential fault number is automatically inserted in the **Fault** field.</span></span>

4. <span data-ttu-id="e9a5e-111">Выберите соответствующий признак в поле **Признак неисправности**.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-111">Select the relevant symptom in the **Fault symptom** field.</span></span>

5. <span data-ttu-id="e9a5e-112">Выберите **Область неисправности** и **Тип неисправности**.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-112">Select **Fault area** and **Fault type**.</span></span>

6. <span data-ttu-id="e9a5e-113">В поле **Дата неисправности** автоматически вставляется текущая дата.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="e9a5e-114">Если необходимо, можно выбрать другую дату.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-114">You can select another date, if necessary.</span></span>

7. <span data-ttu-id="e9a5e-115">На экспресс-вкладке **Причины для выбранного признака** добавьте строку, описывающую причину проблемы.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-115">On the **Causes for selected symptom** FastTab, add a line describing the cause of the problem.</span></span>

8. <span data-ttu-id="e9a5e-116">На экспресс-вкладке **Меры устранения для выбранного признака** добавьте строку, описывающую возможный способ устранения проблемы.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-116">On the **Remedies for selected symptom** FastTab, add a line describing a possible solution to the problem.</span></span>

9. <span data-ttu-id="e9a5e-117">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-117">Click **Save**.</span></span>

![Рисунок 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="e9a5e-119">Просмотр неисправностей активов</span><span class="sxs-lookup"><span data-stu-id="e9a5e-119">View asset faults</span></span>

<span data-ttu-id="e9a5e-120">В списке **Ошибки по активам** можно получить обзор всех ошибок, зарегистрированных для активов.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-120">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="e9a5e-121">Щелкните **Управление активами** > **Запросы** > **Ошибка актива** > **Ошибки активов**, чтобы открыть список.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-121">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults** to open the list.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="e9a5e-122">Печать отчет о неисправностях активов</span><span class="sxs-lookup"><span data-stu-id="e9a5e-122">Print asset fault report</span></span>

<span data-ttu-id="e9a5e-123">На странице списка **Все активы** можно напечатать отчет об ошибках активов, отображающий все регистрации ошибок, а также графический обзор статистики ошибок.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-123">From the **All assets** list page, you can print an asset fault report displaying all fault registrations as well as a graphic overview of fault statistics.</span></span>

1. <span data-ttu-id="e9a5e-124">Щелкните **Управление активами** > **Общие** > **Активы** > **Все активы**.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-124">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="e9a5e-125">В списке **Активы** выберите актив, для которого требуется распечатать отчет о неисправностях.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-125">In the **Assets** list, select the asset for which you want to print a fault report.</span></span>

3. <span data-ttu-id="e9a5e-126">На вкладке **Общие** > раздел **Отчеты** щелкните **Неисправность актива**.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-126">On the **General** tab > **Reports section**, click **Asset fault**.</span></span>

4. <span data-ttu-id="e9a5e-127">Вставьте указанный период или выберите типа ошибки.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-127">Insert a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="e9a5e-128">Щелкните **OK**, чтобы напечатать отчет.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-128">Click **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="e9a5e-129">Можно также напечатать отчет об ошибке для нескольких активов или типов активов, щелкнув **Управление активами** > **Отчеты** > **Активы** > **Неисправность актива**.</span><span class="sxs-lookup"><span data-stu-id="e9a5e-129">You can also print a fault report for several assets or asset types by clicking **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

