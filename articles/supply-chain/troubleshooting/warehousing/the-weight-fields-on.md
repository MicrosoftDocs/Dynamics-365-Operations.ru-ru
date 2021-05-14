---
title: Поля веса в строках загрузки не соответствуют полям веса при загрузке
description: Поля веса в строках загрузки не соответствуют полям веса при загрузке
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 639b82a9d46b74f179d6904d2c3b8e7dfb813b58
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924359"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a><span data-ttu-id="15bc4-103">Поля веса в строках загрузки не соответствуют полям веса при загрузке</span><span class="sxs-lookup"><span data-stu-id="15bc4-103">The weight fields on load lines don't match the weight fields on the load</span></span>

<span data-ttu-id="15bc4-104">Коды ошибок: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span><span class="sxs-lookup"><span data-stu-id="15bc4-104">Error codes: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span></span>

## <a name="symptoms"></a><span data-ttu-id="15bc4-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="15bc4-105">Symptoms</span></span>

<span data-ttu-id="15bc4-106">Система отобразит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="15bc4-106">The system shows the following error message:</span></span>

> <span data-ttu-id="15bc4-107">Поля веса в строках загрузки не соответствуют полям веса при загрузке %1.</span><span class="sxs-lookup"><span data-stu-id="15bc4-107">The weight fields on load lines do not match the weight fields on load %1.</span></span> <span data-ttu-id="15bc4-108">Выполните проверку целостности веса загрузки склада, чтобы пересчитать поля веса.</span><span class="sxs-lookup"><span data-stu-id="15bc4-108">Run the Warehouse load weight consistency check to recalculate the weight fields.</span></span>

## <a name="cause"></a><span data-ttu-id="15bc4-109">Причина</span><span class="sxs-lookup"><span data-stu-id="15bc4-109">Cause</span></span>

<span data-ttu-id="15bc4-110">В полях **Вес нетто** и **Вес тары** задано значение *0* (ноль) в строке загрузки.</span><span class="sxs-lookup"><span data-stu-id="15bc4-110">The **Net weight** and **Tara weight** fields are set to *0* (zero) on the load line.</span></span> <span data-ttu-id="15bc4-111">Однако поля веса не заданы как *0* для измерений веса продукта.</span><span class="sxs-lookup"><span data-stu-id="15bc4-111">However, the weight fields aren't set to *0* for the weight measurements on the product.</span></span> <span data-ttu-id="15bc4-112">Если в строке загрузки не заданы поля веса, любая корректировка количества в строке загрузки может привести к неправильному расчету веса загрузки.</span><span class="sxs-lookup"><span data-stu-id="15bc4-112">When weight fields aren't set on the load line, any corrections of the quantity on the load line might cause incorrect weight calculation on the load.</span></span> <span data-ttu-id="15bc4-113">Эта проблема может возникнуть, если вес продукта был изменен с момента создания строки загрузки.</span><span class="sxs-lookup"><span data-stu-id="15bc4-113">This issue might occur if the weights on the product have been changed since the load line was created.</span></span>

## <a name="resolution"></a><span data-ttu-id="15bc4-114">Приказ</span><span class="sxs-lookup"><span data-stu-id="15bc4-114">Resolution</span></span>

<span data-ttu-id="15bc4-115">По умолчанию при создании строки загрузки в нее вводятся поля веса продукта.</span><span class="sxs-lookup"><span data-stu-id="15bc4-115">By default, when a load line is created, the weight fields from the product are entered on it.</span></span> <span data-ttu-id="15bc4-116">Если вес равен нулю, его можно пересчитать, используя функцию *Проверка целостности веса загрузки склада*.</span><span class="sxs-lookup"><span data-stu-id="15bc4-116">If the weight is zero, you can recalculate it by using the *Warehouse load weight consistency check* functionality.</span></span>

1. <span data-ttu-id="15bc4-117">Перейдите к пункту **Администрирование системы \> Периодические задачи \> База данных \> Проверка целостности**.</span><span class="sxs-lookup"><span data-stu-id="15bc4-117">Go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="15bc4-118">В диалоговом окне **Проверка целостности** в поле **Модуль** задайте *Управление складом*.</span><span class="sxs-lookup"><span data-stu-id="15bc4-118">In the **Consistency check** dialog box, set the **Module** field to *Warehouse management*.</span></span>
1. <span data-ttu-id="15bc4-119">Задайте в поле **Режим проверки** значение *Исправление ошибок*.</span><span class="sxs-lookup"><span data-stu-id="15bc4-119">Set the **Check/Fix** field to *Fix error*.</span></span>
1. <span data-ttu-id="15bc4-120">В списке флажков установите флажок **Проверка целостности веса загрузки склада** и убедитесь, что выделена только строка для этого флажка.</span><span class="sxs-lookup"><span data-stu-id="15bc4-120">In the checkbox list, select the **Warehouse load weight consistency check** checkbox, and make sure that only the row for this checkbox is highlighted.</span></span>
1. <span data-ttu-id="15bc4-121">В верхней части списка флажков выберите кнопку с многоточием (**…**), а затем выберите пункт **Диалоговое окно** в меню.</span><span class="sxs-lookup"><span data-stu-id="15bc4-121">At the top of the checkbox list, select the ellipsis button (**...**), and then select **Dialog** on the menu.</span></span>
1. <span data-ttu-id="15bc4-122">В диалоговом окне **Проверка целостности веса загрузки склада** установите следующие поля, чтобы указать критерии, для которых должен применяться проверка целостности:</span><span class="sxs-lookup"><span data-stu-id="15bc4-122">In the **Warehouse load weight consistency check** dialog box, set the following fields to specify the criteria that the consistency check should run for:</span></span>

    - <span data-ttu-id="15bc4-123">**Код загрузки:** укажите код загрузки.</span><span class="sxs-lookup"><span data-stu-id="15bc4-123">**Load ID:** Specify a load ID.</span></span> <span data-ttu-id="15bc4-124">Оставьте поле пустым для проверки всех кодов загрузки.</span><span class="sxs-lookup"><span data-stu-id="15bc4-124">Leave this blank to check all load IDs.</span></span>
    - <span data-ttu-id="15bc4-125">**Код номенклатуры:** укажите код номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="15bc4-125">**Item number:** Specify an item number.</span></span> <span data-ttu-id="15bc4-126">Оставьте поле пустым для проверки всех номенклатур.</span><span class="sxs-lookup"><span data-stu-id="15bc4-126">Leave this blank to check all items.</span></span>
    - <span data-ttu-id="15bc4-127">**Всегда пересчитывать вес при загрузке:** установите для этого параметра значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="15bc4-127">**Always recalculate weight on loads:** Set this option to *Yes*.</span></span>
    - <span data-ttu-id="15bc4-128">**Разрешить переопределение веса в строках загрузки:** установите для этого параметра значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="15bc4-128">**Allow overwrite of weight on load lines:** Set this option to *Yes*.</span></span>

1. <span data-ttu-id="15bc4-129">Нажмите **ОК**, чтобы закрыть диалоговое окно **Проверка целостности веса загрузки склада**.</span><span class="sxs-lookup"><span data-stu-id="15bc4-129">Select **OK** to close the **Warehouse load weight consistency check** dialog box.</span></span>
1. <span data-ttu-id="15bc4-130">Нажмите кнопку с многоточием, а затем выберите **Выполнить** в меню.</span><span class="sxs-lookup"><span data-stu-id="15bc4-130">Select the ellipsis button, and then select **Execute** on the menu.</span></span>

<span data-ttu-id="15bc4-131">Вес пересчитывается на основе заданных вами критериев.</span><span class="sxs-lookup"><span data-stu-id="15bc4-131">The weight is recalculated based on the criteria that you specified.</span></span> <span data-ttu-id="15bc4-132">Выберите ссылку **Сведения о сообщении**, чтобы просмотреть результат проверки целостности.</span><span class="sxs-lookup"><span data-stu-id="15bc4-132">Select the **Message details** link to view the result of the consistency check.</span></span>
