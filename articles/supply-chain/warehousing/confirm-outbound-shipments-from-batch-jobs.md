---
title: Подтвердить исходящие отгрузки из пакетных заданий
description: В этом разделе описывается, как настроить пакетное задание, которое автоматически подтверждает исходящие отгрузки по заказу на перемещение для готовых нагрузок в отгрузку.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 41dbfb90b7b19c964e725ee0a4c769402414fb17
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/03/2020
ms.locfileid: "3652262"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="16f60-103">Подтвердить исходящие отгрузки из пакетных заданий</span><span class="sxs-lookup"><span data-stu-id="16f60-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16f60-104">В этом разделе описывается, как настроить пакетное задание, которое автоматически подтверждает исходящие отгрузки по заказу на перемещение для готовых нагрузок в отгрузку.</span><span class="sxs-lookup"><span data-stu-id="16f60-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="16f60-105">Описываемое здесь пакетное задание применяется только к отгрузкам заказа на перемещение, а не к заказам на продажу.</span><span class="sxs-lookup"><span data-stu-id="16f60-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="16f60-106">Включите функцию "Подтвердить исходящие отгрузки из пакетных заданий"</span><span class="sxs-lookup"><span data-stu-id="16f60-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="16f60-107">Прежде чем использовать эту функцию, необходимо включить ее в системе.</span><span class="sxs-lookup"><span data-stu-id="16f60-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="16f60-108">Администраторы могут использовать страницу [управления функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса компонента и включения их при необходимости.</span><span class="sxs-lookup"><span data-stu-id="16f60-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="16f60-109">Функция указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="16f60-109">The feature is listed as:</span></span>

- <span data-ttu-id="16f60-110">**Модуль** - *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="16f60-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="16f60-111">**Название функции** - *Подтвердить исходящие отгрузки из пакетных заданий*</span><span class="sxs-lookup"><span data-stu-id="16f60-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="16f60-112">Обработка исходящих отгрузок</span><span class="sxs-lookup"><span data-stu-id="16f60-112">Process outbound shipments</span></span>

<span data-ttu-id="16f60-113">Настройка запланированного пакетного задания для запуска подтверждения исходящего отгрузки для загрузок, готовых к отгрузке:</span><span class="sxs-lookup"><span data-stu-id="16f60-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="16f60-114">Перейдите **Управление складом \> Периодические задачи \> Обработка исходящих отгрузок**.</span><span class="sxs-lookup"><span data-stu-id="16f60-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="16f60-115">Откроется диалоговое окно **Подтверждение отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="16f60-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="16f60-116">На экспресс-вкладке **Записи для добавления** выберите **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="16f60-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="16f60-117">Откроется диалоговое окно редактора запросов.</span><span class="sxs-lookup"><span data-stu-id="16f60-117">The query editor dialog box opens.</span></span> <span data-ttu-id="16f60-118">На вкладке **Диапазон** выберите добавьте строку со следующими значениями:</span><span class="sxs-lookup"><span data-stu-id="16f60-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="16f60-119">**Таблица** - *Загрузки*</span><span class="sxs-lookup"><span data-stu-id="16f60-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="16f60-120">**Производная таблица** - *Загрузки*</span><span class="sxs-lookup"><span data-stu-id="16f60-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="16f60-121">**Поле** - *Статус загрузки*</span><span class="sxs-lookup"><span data-stu-id="16f60-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="16f60-122">**Критерий** - *Загружено*</span><span class="sxs-lookup"><span data-stu-id="16f60-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="16f60-123">Нажмите **ОК**, чтобы вернуться в диалоговое окно **Подтверждение отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="16f60-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="16f60-124">На экспресс-вкладке **Выполнять в фоновом режиме** установите для **Пакетная обработка** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="16f60-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="16f60-125">На экспресс-вкладке **Выполнять в фоновом режиме** выберите **Повторение**.</span><span class="sxs-lookup"><span data-stu-id="16f60-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="16f60-126">Откроется диалоговое окно **Определение повторения**.</span><span class="sxs-lookup"><span data-stu-id="16f60-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="16f60-127">Настройте расписание запуска в соответствии с потребностями компании.</span><span class="sxs-lookup"><span data-stu-id="16f60-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="16f60-128">Нажмите **ОК**, чтобы вернуться в диалоговое окно **Подтверждение отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="16f60-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="16f60-129">Нажмите **ОК** в диалоговом окне **Подтверждение отгрузки**, чтобы добавить пакетное задание в очередь пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="16f60-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="16f60-130">Дополнительные сведения см. в разделе [Обзор пакетной обработки](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="16f60-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>
