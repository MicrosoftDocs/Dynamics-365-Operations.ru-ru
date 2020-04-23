---
title: Обновление стандартных затрат в непроизводственной среде
description: Эта статья содержит рекомендации по обновлению стандартных затрат в непроизводственной среде.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09dca3012952b739a75a6930908752fba73a4550
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214121"
---
# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a><span data-ttu-id="a7fc9-103">Обновление стандартных затрат в непроизводственной среде</span><span class="sxs-lookup"><span data-stu-id="a7fc9-103">Update standard costs in a non-manufacturing environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7fc9-104">Эта статья содержит рекомендации по обновлению стандартных затрат в непроизводственной среде.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-104">This article provides guidance for updating standard costs in a non-manufacturing environment.</span></span>

<span data-ttu-id="a7fc9-105">В приведенных ниже указаниях предполагается использование подхода на основе двух версий для обновления стандартной стоимости.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-105">The following guidelines assume that you use a two-version approach to update standard cost.</span></span> <span data-ttu-id="a7fc9-106">В этом подходе одна версия расчета себестоимости содержит изначально определенные стандартные затраты для "замороженного" периода, а вторая версия расчета себестоимости содержит инкрементные обновления.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-106">In this approach, one costing version contains the standard costs that were originally defined for the frozen period, and the second costing version contains the incremental updates.</span></span> <span data-ttu-id="a7fc9-107">Каждое обновление вводится как запись стоимости, которая входит во вторую версию расчета себестоимости, после чего оно активируется.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-107">Each update is entered as a cost record that is enclosed in the second costing version, and eventually it's enabled.</span></span> <span data-ttu-id="a7fc9-108">Также можно использовать подход на основе одной версии, который использует первоначально определенный набор стандартных затрат.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-108">An alternative, one-version approach uses the set of standard costs that was originally defined.</span></span> <span data-ttu-id="a7fc9-109">Подход на основе двух версий требует определения второй версии цены.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-109">The two-version approach requires that you define a second costing version.</span></span> <span data-ttu-id="a7fc9-110">Далее приведены инструкции по определению этой версии расчета себестоимости.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-110">Here are the guidelines for defining this costing version:</span></span>

-   <span data-ttu-id="a7fc9-111">Назначьте тип расчета себестоимости цены **Стандартная себестоимость**.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-111">Assign a costing type of **Standard costs**.</span></span>
-   <span data-ttu-id="a7fc9-112">Назначьте понятный идентификатор, который отражает содержимое версии расчета себестоимости, например **2016-UPDATES**.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-112">Assign a meaningful identifier that indicates the contents of the costing version, such as **2016-UPDATES**.</span></span>
-   <span data-ttu-id="a7fc9-113">Убедитесь, что это содержимое включает в себя записи себестоимости.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-113">Make sure that the content includes cost records.</span></span>
-   <span data-ttu-id="a7fc9-114">Разрешите ввод записей затрат для всех cайтов.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-114">Allow cost records to be entered for all sites.</span></span> <span data-ttu-id="a7fc9-115">Если вы указываете сайт, записи затрат можно ввести только для этого сайта.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-115">If you specify a site, cost records can be entered only for that site.</span></span>
-   <span data-ttu-id="a7fc9-116">Укажите принципа отката **Нет**.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-116">Indicate a fallback principle of **None**.</span></span> <span data-ttu-id="a7fc9-117">Принцип отката используется только при калькуляции затрат по произведенным номенклатурам.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-117">The fallback principle applies only to cost calculations for manufactured items.</span></span>

<span data-ttu-id="a7fc9-118">Для исправления, корректировки или обновления стандартных затрат для новых номенклатур выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-118">To correct, adjust, or update standard costs for new items, follow these steps.</span></span>

1.  <span data-ttu-id="a7fc9-119">Используйте страницу **Настройка версии** **калькуляции издержек**, чтобы разрешить ввод данных по затратам во вторую версию расчета себестоимости.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-119">Use the **Costing version** **setup** page to enable cost data to be entered into the second costing version.</span></span> <span data-ttu-id="a7fc9-120">По желанию запретите активацию ожидающих затрат, чтобы такая активация разрешалась после полного и точного определения ожидающих затрат.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-120">Optionally, prevent the activation of pending costs, so that activation will be allowed after pending costs have been completely and accurately defined.</span></span> <span data-ttu-id="a7fc9-121">При желании можно также ввести дату в поле **Дата начала**.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-121">You can also optionally enter a date in the **From date** field.</span></span> <span data-ttu-id="a7fc9-122">Указание общего порядка: используйте дату, которая представляет дату планируемого выполнения инкрементных обновлений.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-122">As a general guideline, use the date when you intend to enable the incremental updates.</span></span> <span data-ttu-id="a7fc9-123">Можно также оставить пустым поле **Дата начала** для версии расчета себестоимости, а затем вводить дату в поле **Дата начала** для каждой записи затрат.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-123">Alternatively, leave the **From date** field blank for the costing version, and then enter a date in the **From date** field for each cost record.</span></span>
2.  <span data-ttu-id="a7fc9-124">Используйте страницу **Цена номенклатуры** для ввода обновлений в виде записей затрат по номенклатуре, которые входят во вторую версию расчета себестоимости.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-124">Use the **Item price** page to enter updates as item cost records that are enclosed in the second costing version.</span></span>
3.  <span data-ttu-id="a7fc9-125">Используйте отчет **Цены номенклатуры** для проверки полноты и точности записей затрат по номенклатуре, которые входят во вторую версию расчета себестоимости.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-125">Use the **Item prices** report to verify the completeness and accuracy of the item cost records that are enclosed in the second costing version.</span></span>
4.  <span data-ttu-id="a7fc9-126">Используйте страницу **Поддержка версии калькуляции издержек** для изменения блокирующего флага, чтобы активировать записи предстоящих затрат в рамках второй версии расчета себестоимости.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-126">Use the **Costing version maintenance** page to change the blocking flag to allow activation of the pending cost records that are enclosed in the second costing version.</span></span>
5.  <span data-ttu-id="a7fc9-127">Используйте страницу **Активировать цены** (которая открывается со страницы **Поддержка версии калькуляции издержек**) для активирования всех записей предстоящих затрат в рамках второй версии расчета себестоимости.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-127">Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to activate all pending item cost records that are enclosed in the second costing version.</span></span> <span data-ttu-id="a7fc9-128">Кроме того, записи по ожидаемым затратам для отдельных номенклатур можно активировать, нажав кнопку **Активировать ожидающие цены** на странице **Цена номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-128">You can also activate the pending cost records for individual items by clicking the **Activate pending price** button on the **Item price** page.</span></span>
6.  <span data-ttu-id="a7fc9-129">Используйте страницу **Настройка версии калькуляции издержек** для изменения блокирующих флагов в рамках второй версии расчета себестоимости, чтобы избежать поддержки дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-129">To prevent additional data maintenance, use the **Costing version setup** page to change the blocking flags that are enclosed in the second costing version.</span></span> <span data-ttu-id="a7fc9-130">Политики блокирования помогут предотвратить ввод новых предстоящих затрат и активацию предстоящих затрат.</span><span class="sxs-lookup"><span data-stu-id="a7fc9-130">The blocking policies will prevent the entry of new pending costs and the activation of pending costs.</span></span>




