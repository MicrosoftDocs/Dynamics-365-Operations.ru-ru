---
title: Работники, ответственные за утверждение несоответствий
description: В этой теме описывается, как настроить работников, ответственных за утверждение несоответствий.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d3f647de2c188661c2c9c5f31e2642c3f8ca0b5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021788"
---
# <a name="workers-responsible-for-approving-nonconformances"></a><span data-ttu-id="e1b46-103">Работники, ответственные за утверждение несоответствий</span><span class="sxs-lookup"><span data-stu-id="e1b46-103">Workers responsible for approving nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1b46-104">В этой теме описывается, как настроить работников, ответственных за утверждение несоответствий.</span><span class="sxs-lookup"><span data-stu-id="e1b46-104">This topic describes how to configure workers that are responsible for approving nonconformances.</span></span>

<span data-ttu-id="e1b46-105">Несоответствия должны быть утверждены, прежде чем пользователи смогут начать вводить такие сведения, как исправления или операции.</span><span class="sxs-lookup"><span data-stu-id="e1b46-105">Nonconformances must be approved before users can start to enter details such as corrections or operations.</span></span> <span data-ttu-id="e1b46-106">Прежде чем пользователи смогут утверждать или отклонять несоответствия, их код пользователя (запись пользователя) должен быть связан с записью работника.</span><span class="sxs-lookup"><span data-stu-id="e1b46-106">Before users can approve or reject nonconformances, their user ID (user record) must be linked to a worker record.</span></span> <span data-ttu-id="e1b46-107">При необходимости можно настроить работников, ответственных за качество, а затем позволить одному работнику утверждать работу от имени другого работника.</span><span class="sxs-lookup"><span data-stu-id="e1b46-107">You can optionally configure workers that are responsible for quality and then allow one worker to approve work on behalf of another worker.</span></span>

## <a name="enable-a-user-for-nonconformance-processing"></a><span data-ttu-id="e1b46-108">Включение пользователя для обработки несоответствия</span><span class="sxs-lookup"><span data-stu-id="e1b46-108">Enable a user for nonconformance processing</span></span>

<span data-ttu-id="e1b46-109">Прежде чем пользователь сможет утверждать или отклонять несоответствия, следует связать код пользователя с записью работника.</span><span class="sxs-lookup"><span data-stu-id="e1b46-109">Before a user can approve or reject nonconformances, you must link their user record to a worker record.</span></span> <span data-ttu-id="e1b46-110">Поля утверждения можно настроить автоматически, и текущий пользователь может быть автоматически заполнен для табеля учета рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="e1b46-110">The approval fields can then be automatically set, and the current user can be automatically filled in for the timesheet.</span></span> <span data-ttu-id="e1b46-111">Перед тем, как пользователь сможет использовать примечания к документам, следует активировать обработку документов в параметрах пользователя.</span><span class="sxs-lookup"><span data-stu-id="e1b46-111">Before the user can use the document notes, you must activate document handling in their user options.</span></span>

1. <span data-ttu-id="e1b46-112">Перейдите в раздел **Администрирование системы \> Пользователи \> Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="e1b46-112">Go to **System administration \> Users \> Users**.</span></span>
1. <span data-ttu-id="e1b46-113">Найдите и откройте пользователя, у которого должна быть возможность утвердить или отклонить несоответствия.</span><span class="sxs-lookup"><span data-stu-id="e1b46-113">Find and open the user who should be able to approve or reject nonconformances.</span></span>
1. <span data-ttu-id="e1b46-114">В поле **Лицо** задайте имя работника, который связан с текущей записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="e1b46-114">Set the **Person** field to the name of the worker that is related to the current user record.</span></span>
1. <span data-ttu-id="e1b46-115">На панели операций выберите **Параметры пользователя**.</span><span class="sxs-lookup"><span data-stu-id="e1b46-115">On the Action Pane, select **User options**.</span></span>
1. <span data-ttu-id="e1b46-116">На странице **Параметры** текущей записи пользователя на вкладке **Параметры** установите для параметра **Разрешить обработку документов** значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="e1b46-116">On the **Options** page for the current user record, on the **Preferences** tab, set the **Enable document handling** option to *Yes*.</span></span>
1. <span data-ttu-id="e1b46-117">Закройте страницы.</span><span class="sxs-lookup"><span data-stu-id="e1b46-117">Close the pages.</span></span>

## <a name="define-workers-that-are-responsible-for-quality"></a><span data-ttu-id="e1b46-118">Определение сотрудников, ответственных за контроль качества</span><span class="sxs-lookup"><span data-stu-id="e1b46-118">Define workers that are responsible for quality</span></span>

1. <span data-ttu-id="e1b46-119">Перейдите в раздел **Управление запасами \> Настройка \> Контроль качества \> Работники, ответственные за контроль качества**.</span><span class="sxs-lookup"><span data-stu-id="e1b46-119">Go to **Inventory management \> Setup \> Quality control \> Workers responsible for quality**.</span></span>
2. <span data-ttu-id="e1b46-120">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="e1b46-120">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="e1b46-121">В поле **Работник** выберите работника, который вводит данные контроля качества.</span><span class="sxs-lookup"><span data-stu-id="e1b46-121">In the **Worker** field, select the worker that enters quality data.</span></span>
4. <span data-ttu-id="e1b46-122">В поле **Ответственный работник** выберите работника, от лица которого выбранный работник вводит работу.</span><span class="sxs-lookup"><span data-stu-id="e1b46-122">In the **Worker responsible** field, select the worker that the selected worker enters work on behalf of.</span></span> <span data-ttu-id="e1b46-123">Когда несоответствия создаются и обновляются, этот работник будет введен по умолчанию в поля **Работник**.</span><span class="sxs-lookup"><span data-stu-id="e1b46-123">When nonconformances are created and updated, this worker will be entered by default in **Worker** fields.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1b46-124">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e1b46-124">Additional resources</span></span>

- [<span data-ttu-id="e1b46-125">Обзор управления качеством</span><span class="sxs-lookup"><span data-stu-id="e1b46-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="e1b46-126">Включение управления качеством и несоответствием</span><span class="sxs-lookup"><span data-stu-id="e1b46-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="e1b46-127">Расходы по контролю качества</span><span class="sxs-lookup"><span data-stu-id="e1b46-127">Quality charges</span></span>](quality-charges.md)
- [<span data-ttu-id="e1b46-128">Карантинные зоны для несоответствий</span><span class="sxs-lookup"><span data-stu-id="e1b46-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="e1b46-129">Типы диагностики для несоответствий</span><span class="sxs-lookup"><span data-stu-id="e1b46-129">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="e1b46-130">Расходы по контролю качества для несоответствий</span><span class="sxs-lookup"><span data-stu-id="e1b46-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="e1b46-131">Операции для несоответствий</span><span class="sxs-lookup"><span data-stu-id="e1b46-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="e1b46-132">Управление качеством для складских процессов</span><span class="sxs-lookup"><span data-stu-id="e1b46-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
