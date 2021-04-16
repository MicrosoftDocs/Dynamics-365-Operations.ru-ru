---
title: Настройка автоматической выверки фрахта
description: Эта процедура показывает порядок настройки данных для автоматической выверки фрахта.
author: ShylaThompson
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4bc3998dea2e953191151f8e54345ec648ff33e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837617"
---
# <a name="set-up-automatic-freight-reconciliation"></a><span data-ttu-id="7587d-103">Настройка автоматической выверки фрахта</span><span class="sxs-lookup"><span data-stu-id="7587d-103">Set up automatic freight reconciliation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7587d-104">Эта процедура показывает порядок настройки данных для автоматической выверки фрахта.</span><span class="sxs-lookup"><span data-stu-id="7587d-104">This procedure shows how to set up data for automatic freight reconciliation.</span></span> <span data-ttu-id="7587d-105">Это обычно выполняется менеджером склада.</span><span class="sxs-lookup"><span data-stu-id="7587d-105">This is typically done by a warehouse manager.</span></span> <span data-ttu-id="7587d-106">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="7587d-106">You can use this procedure in demo data company USMF.</span></span>


## <a name="set-up-the-freight-bill-type"></a><span data-ttu-id="7587d-107">Настройка типа векселя фрахта</span><span class="sxs-lookup"><span data-stu-id="7587d-107">Set up the freight bill type</span></span>
1. <span data-ttu-id="7587d-108">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Выверка фрахта" > "Тип векселя фрахта".</span><span class="sxs-lookup"><span data-stu-id="7587d-108">Go to Transportation management > Setup > Freight reconciliation > Freight bill type.</span></span>
    * <span data-ttu-id="7587d-109">Тип счета за фрахт определяет, как счета за фрахт и накладные перевозчика должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="7587d-109">The freight bill type defines how freight bills and carrier invoices  should be matched.</span></span>  
2. <span data-ttu-id="7587d-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="7587d-110">Click New.</span></span>
3. <span data-ttu-id="7587d-111">В поле "Тип векселя фрахта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="7587d-111">In the Freight bill type field, type a value.</span></span>
4. <span data-ttu-id="7587d-112">В поле "Сборка механизма" введите "Microsoft.Dynamics.Ax.Tms.dll".</span><span class="sxs-lookup"><span data-stu-id="7587d-112">In the Engine assembly field, type 'Microsoft.Dynamics.Ax.Tms.dll'.</span></span>
    * <span data-ttu-id="7587d-113">Это стандартная библиотека кода модуля сопоставления для управления транспортировкой.</span><span class="sxs-lookup"><span data-stu-id="7587d-113">This is the standard Transportation management matching engine code library.</span></span>  
5. <span data-ttu-id="7587d-114">В поле "Класс механизма" введите "Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer".</span><span class="sxs-lookup"><span data-stu-id="7587d-114">In the Engine class field, type 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span></span>
    * <span data-ttu-id="7587d-115">Это стандартный класс модуля сопоставления для управления транспортировкой.</span><span class="sxs-lookup"><span data-stu-id="7587d-115">This is the standard Transportation management matching engine class.</span></span>  
6. <span data-ttu-id="7587d-116">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="7587d-116">Click New.</span></span>
7. <span data-ttu-id="7587d-117">В поле "Описание" выберите значение, которое должно соответствовать в счете за фрахт и накладной перевозчика.</span><span class="sxs-lookup"><span data-stu-id="7587d-117">In the Description field, choose the value that should match on the freight bill and the carrier invoice.</span></span>  
8. <span data-ttu-id="7587d-118">В поле "Требуется сопоставление" выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="7587d-118">In the Match required field, select 'Yes'.</span></span>
    * <span data-ttu-id="7587d-119">Если в этом поле задано значение "Да", это означает, что значение, выбранное в поле "Описание", должно совпадать как в счете за фрахт, так и в накладной перевозчика.</span><span class="sxs-lookup"><span data-stu-id="7587d-119">If you set this field to Yes this means that the value selected in the Description field needs to match on both the freight bill and the carrier invoice.</span></span> <span data-ttu-id="7587d-120">Если задано значение "Нет", это поле может быть пустым в одном из этих документов.</span><span class="sxs-lookup"><span data-stu-id="7587d-120">If you set it to No, the field can be blank on one of these.</span></span>  
9. <span data-ttu-id="7587d-121">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="7587d-121">Click Save.</span></span>

## <a name="set-up-the-freight-bill-type-assignment"></a><span data-ttu-id="7587d-122">Настройка назначения типа векселя фрахта</span><span class="sxs-lookup"><span data-stu-id="7587d-122">Set up the freight bill type assignment</span></span>
1. <span data-ttu-id="7587d-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7587d-123">Close the page.</span></span>
2. <span data-ttu-id="7587d-124">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Выверка фрахта" > "Назначения типов векселей фрахта".</span><span class="sxs-lookup"><span data-stu-id="7587d-124">Go to Transportation management > Setup > Freight reconciliation > Freight bill type assignments.</span></span>
    * <span data-ttu-id="7587d-125">Назначение типа счета за фрахт используется, чтобы определить, какой тип счета за фрахт используется для определенного перевозчика.</span><span class="sxs-lookup"><span data-stu-id="7587d-125">The freight bill type assignment is used to specify which freight bill type is used for a particular carrier.</span></span>   
3. <span data-ttu-id="7587d-126">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="7587d-126">Click New.</span></span>
4. <span data-ttu-id="7587d-127">В поле "Режим" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="7587d-127">In the Mode field, enter or select a value.</span></span>
5. <span data-ttu-id="7587d-128">В поле "Перевозчик, осуществляющий доставку" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="7587d-128">In the Shipping carrier field, enter or select a value.</span></span>
6. <span data-ttu-id="7587d-129">В поле "Тип векселя фрахта" выберите тип счета за фрахт, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="7587d-129">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
7. <span data-ttu-id="7587d-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7587d-130">Close the page.</span></span>

## <a name="set-up-the-audit-master"></a><span data-ttu-id="7587d-131">Настройка мастера аудита</span><span class="sxs-lookup"><span data-stu-id="7587d-131">Set up the audit master</span></span>
1. <span data-ttu-id="7587d-132">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Выверка фрахта" > "Шаблон аудита".</span><span class="sxs-lookup"><span data-stu-id="7587d-132">Go to Transportation management > Setup > Freight reconciliation > Audit master.</span></span>
    * <span data-ttu-id="7587d-133">Мастер аудита определяет лимиты отклонения для автоматической выверки фрахта.</span><span class="sxs-lookup"><span data-stu-id="7587d-133">The audit master defines the tolerance limits for automatic freight reconciliation.</span></span> <span data-ttu-id="7587d-134">Он определяет, насколько денежные суммы в счете за фрахт и накладной перевозчика могут отличаться и при этом все еще допускать выполнение выверки.</span><span class="sxs-lookup"><span data-stu-id="7587d-134">It specifies by how much the monetary amounts on the freight bill and the carrier invoice can differ and still allow reconciliation to occur.</span></span> <span data-ttu-id="7587d-135">Он также определяет способ обработки несоответствий.</span><span class="sxs-lookup"><span data-stu-id="7587d-135">It also defines how to handle discrepancies.</span></span>  
2. <span data-ttu-id="7587d-136">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="7587d-136">Click New.</span></span>
3. <span data-ttu-id="7587d-137">В поле "Код шаблона аудита" введите значение.</span><span class="sxs-lookup"><span data-stu-id="7587d-137">In the Audit master ID field, type a value.</span></span>
4. <span data-ttu-id="7587d-138">В поле "Перевозчик, осуществляющий доставку" выберите того же перевозчика, что и ранее.</span><span class="sxs-lookup"><span data-stu-id="7587d-138">In the Shipping carrier  field, select the same shipping carrier as you did earlier.</span></span>
5. <span data-ttu-id="7587d-139">В поле "Тип векселя фрахта" выберите тип счета за фрахт, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="7587d-139">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
6. <span data-ttu-id="7587d-140">Разверните раздел "Допуск".</span><span class="sxs-lookup"><span data-stu-id="7587d-140">Expand the Tolerance section.</span></span>
7. <span data-ttu-id="7587d-141">В поле "Минимальный уровень отклонения" введите число.</span><span class="sxs-lookup"><span data-stu-id="7587d-141">In the Minimum tolerance level field, enter a number.</span></span>
8. <span data-ttu-id="7587d-142">В поле "Максимальный уровень отклонения" введите число.</span><span class="sxs-lookup"><span data-stu-id="7587d-142">In the Maximum tolerance level field, enter a number.</span></span>
9. <span data-ttu-id="7587d-143">Разверните раздел "Результат".</span><span class="sxs-lookup"><span data-stu-id="7587d-143">Expand the Result section.</span></span>
10. <span data-ttu-id="7587d-144">В поле "Код основания переплаты" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="7587d-144">In the Overpayment reason code field, enter or select a value.</span></span>
    * <span data-ttu-id="7587d-145">Если денежные суммы отличаются в счете за фрахт и в накладной перевозчика, то коды причин переплаты и недоплаты определяют счета, на которых должна быть зарегистрирована разница, если эта разница находится в допустимых пределах.</span><span class="sxs-lookup"><span data-stu-id="7587d-145">If the monetary amounts differ on the freight bill and the carrier invoice, the overpayment and underpayment reason codes specify the accounts that the difference should be registered on, as long as the difference is within the tolerance levels.</span></span>  
11. <span data-ttu-id="7587d-146">В поле "Код основания недоплаты" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="7587d-146">In the Underpayment reason code field, enter or select a value.</span></span>
12. <span data-ttu-id="7587d-147">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7587d-147">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]