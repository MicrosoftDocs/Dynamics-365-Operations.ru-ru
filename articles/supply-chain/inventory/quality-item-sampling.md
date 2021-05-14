---
title: Выборка номенклатуры управления качеством
description: В этой теме описывается, как настроить выборку номенклатур.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 495bef32d63738e367167ee69f2028bc77945cc4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956797"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="08148-103">Выборка номенклатуры управления качеством</span><span class="sxs-lookup"><span data-stu-id="08148-103">Quality management item sampling</span></span>

<span data-ttu-id="08148-104">Выборка номенклатур используется как часть сопоставления контроля качества.</span><span class="sxs-lookup"><span data-stu-id="08148-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="08148-105">Она определяет сумму текущих физических запасов, которые необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="08148-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="08148-106">Выборочный контроль может быть основан на фиксированных количествах, на процентном объеме или на полном грузоместе.</span><span class="sxs-lookup"><span data-stu-id="08148-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="08148-107">Настройка выборки номенклатур</span><span class="sxs-lookup"><span data-stu-id="08148-107">Set up item sampling</span></span>

<span data-ttu-id="08148-108">Чтобы настроить выборку номенклатур, сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="08148-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="08148-109">Перейдите в раздел **Управление запасами \> Настройка \> Контроль качества \> Выборка номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="08148-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="08148-110">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="08148-110">Select **New**.</span></span>
1. <span data-ttu-id="08148-111">В поле **Выборка номенклатуры** введите значение.</span><span class="sxs-lookup"><span data-stu-id="08148-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="08148-112">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="08148-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="08148-113">В поле **Значение** введите число.</span><span class="sxs-lookup"><span data-stu-id="08148-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="08148-114">Это значение относится к значению спецификации количества, выбранной в соседнем поле.</span><span class="sxs-lookup"><span data-stu-id="08148-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="08148-115">В разделе **Процесс** установите флажок **Полная блокировка**, если в случае неудачной проверки необходимо заблокировать количество всего лота или количество строки заказа.</span><span class="sxs-lookup"><span data-stu-id="08148-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="08148-116">Если этот флажок снят, только номенклатуры в заказе контроля качества будут заблокированы в случае сбоя проверки.</span><span class="sxs-lookup"><span data-stu-id="08148-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="08148-117">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="08148-117">Select **Save**.</span></span>
1. <span data-ttu-id="08148-118">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="08148-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="08148-119">Функция *Управление качеством для складских процессов* предоставляет дополнительные возможности выборки номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="08148-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="08148-120">Она добавляет концепцию *области выборки элементов*, а также возможность определения полного грузоместа в качестве спецификации количества.</span><span class="sxs-lookup"><span data-stu-id="08148-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="08148-121">Если эта функция включена, для получения дополнительных сведений см. раздел [Управление качеством для складских процессов](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="08148-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
