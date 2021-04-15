---
title: Настройка кодов причин
description: Dynamics 365 Human Resources использует коды причин, чтобы объяснить причину изменения льготы сотрудника.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ee74cb8b11c9b72940448077ee485ade4c0b7a39
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801055"
---
# <a name="set-up-reason-codes"></a><span data-ttu-id="45585-103">Настройка кодов причин</span><span class="sxs-lookup"><span data-stu-id="45585-103">Set up reason codes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="45585-104">Dynamics 365 Human Resources использует коды причин, чтобы объяснить причину изменения льготы сотрудника.</span><span class="sxs-lookup"><span data-stu-id="45585-104">Dynamics 365 Human Resources uses reason codes to explain why an employee’s benefits are changing.</span></span>

> [!NOTE]
> <span data-ttu-id="45585-105">По состоянию на январь 2021 года коды причин переходят в рабочую область **Управление персоналом** вместо рабочей области **Управление льготами**.</span><span class="sxs-lookup"><span data-stu-id="45585-105">As of January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="45585-106">Дополнительные сведения см. в разделе [Миграция кодов причин в управление персоналом вручную](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span><span class="sxs-lookup"><span data-stu-id="45585-106">For more information, see [Manually migrate reason codes to Personnel management](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span></span>

## <a name="create-reason-codes"></a><span data-ttu-id="45585-107">Создание кодов причины</span><span class="sxs-lookup"><span data-stu-id="45585-107">Create reason codes</span></span>

1. <span data-ttu-id="45585-108">В рабочей области **Управление персоналом** (или в рабочей области **Управление льготами**, если коды причин еще не перенесены), выберите **Ссылки**, затем выберите **Коды причин**.</span><span class="sxs-lookup"><span data-stu-id="45585-108">In the **Personnel management** workspace (or **Benefits management** workspace if your reason codes haven't yet migrated), select **Links**, and then select **Reason codes**.</span></span>

2. <span data-ttu-id="45585-109">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="45585-109">Select **New**.</span></span>

3. <span data-ttu-id="45585-110">Укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="45585-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="45585-111">Поле</span><span class="sxs-lookup"><span data-stu-id="45585-111">Field</span></span> | <span data-ttu-id="45585-112">Описание</span><span class="sxs-lookup"><span data-stu-id="45585-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="45585-113">**Код основания**</span><span class="sxs-lookup"><span data-stu-id="45585-113">**Reason code**</span></span> | <span data-ttu-id="45585-114">Уникальное имя, определяющее причину, по которой у сотрудника изменится регистрация плана льгот.</span><span class="sxs-lookup"><span data-stu-id="45585-114">A unique name to identify the reason an employee would change a benefit plan enrollment.</span></span> |
   | <span data-ttu-id="45585-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="45585-115">**Description**</span></span> | <span data-ttu-id="45585-116">Описание кода причины.</span><span class="sxs-lookup"><span data-stu-id="45585-116">A description of the reason code.</span></span> |

4. <span data-ttu-id="45585-117">В области **Применимые сценарии** задайте для параметра **Управление льготами** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="45585-117">Under **Applicable scenarios**, set **Benefits management** to **Yes**.</span></span> <span data-ttu-id="45585-118">(Не применяется, если коды причин еще не перенесены в рабочую область **Управление персоналом**.)</span><span class="sxs-lookup"><span data-stu-id="45585-118">(Not applicable if your reason codes haven't yet migrated to the **Personnel management** workspace.)</span></span>

5. <span data-ttu-id="45585-119">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="45585-119">Select **Save**.</span></span>

## <a name="manually-migrate-reason-codes-to-personnel-management"></a><span data-ttu-id="45585-120">Миграция кодов причин в управление персоналом вручную</span><span class="sxs-lookup"><span data-stu-id="45585-120">Manually migrate reason codes to Personnel management</span></span>

<span data-ttu-id="45585-121">В январе 2021 года коды причин переходят в рабочую область **Управление персоналом** вместо рабочей области **Управление льготами**.</span><span class="sxs-lookup"><span data-stu-id="45585-121">In January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="45585-122">Большая часть данных кодов причин будет автоматически перенесена в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="45585-122">Most reason code data will automatically migrate in your environment.</span></span> <span data-ttu-id="45585-123">По некоторым причинам данные кодов причин могут быть не перенесены.</span><span class="sxs-lookup"><span data-stu-id="45585-123">Some reason code data might not migrate.</span></span> <span data-ttu-id="45585-124">Например, коды причин теперь имеют максимальное значение в 15 знаков, поэтому все коды причин, длина которых превышает 15 символов, не переносятся автоматически.</span><span class="sxs-lookup"><span data-stu-id="45585-124">For example, reason codes now have a 15-character maximum, so any reason codes longer than 15 characters won't migrate automatically.</span></span>

<span data-ttu-id="45585-125">Вы увидите баннер на странице **Ссылки** в рабочей области **Управление льготами**, которая информирует вас о миграции и о том, были ли перенесены коды причин.</span><span class="sxs-lookup"><span data-stu-id="45585-125">You'll see a banner on the **Links** page of the **Benefits management** workspace informing you about the migration and whether any reason codes didn't migrate.</span></span>

1. <span data-ttu-id="45585-126">Выберите **Коды причин** для получения сведений о статусе миграции.</span><span class="sxs-lookup"><span data-stu-id="45585-126">Select **Reason codes** for details about migration status.</span></span>

   <span data-ttu-id="45585-127">[![Коды оснований](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span><span class="sxs-lookup"><span data-stu-id="45585-127">[![Reason codes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span></span>

2. <span data-ttu-id="45585-128">Выберите код причины, для которого не удалось выполнить миграцию.</span><span class="sxs-lookup"><span data-stu-id="45585-128">Select a reason code that failed to migrate.</span></span>

   <span data-ttu-id="45585-129">[![Статус миграции кода причины](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span><span class="sxs-lookup"><span data-stu-id="45585-129">[![Reason code migration status](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span></span>

3. <span data-ttu-id="45585-130">Выберите **Перенести код причины**.</span><span class="sxs-lookup"><span data-stu-id="45585-130">Select **Migrate reason code**.</span></span>

   <span data-ttu-id="45585-131">[![Мигрировать код основания](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span><span class="sxs-lookup"><span data-stu-id="45585-131">[![Migrate reason code](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span></span>

4. <span data-ttu-id="45585-132">В области **Миграция кода причины льготы** имеются два параметра для сопоставления с кодом причины управления персоналом:</span><span class="sxs-lookup"><span data-stu-id="45585-132">In the **Benefit reason code migration** pane, you have two options for mapping to a Personnel management reason code:</span></span>

   - <span data-ttu-id="45585-133">Чтобы использовать существующий код причины в модуле управления персоналом, выберите его в раскрывающемся списке **Использовать существующий код причины**.</span><span class="sxs-lookup"><span data-stu-id="45585-133">To use an existing reason code in Personnel management, choose one from the **Use existing reason code** dropdown.</span></span>
     > [!NOTE]
     > <span data-ttu-id="45585-134">Можно использовать существующий код причины в модуле "Управление персоналом" только в том случае, если еще не выполнена миграция другого кода причины модуля управления льготами.</span><span class="sxs-lookup"><span data-stu-id="45585-134">You can only use an existing reason code in Personnel management if another Benefits management reason code hasn't already migrated to it.</span></span>
   - <span data-ttu-id="45585-135">Чтобы создать новый код причины в модуле "Управление персоналом", введите новое значение в поле **Создать код причины**, затем введите описание в поле **Создать описание**.</span><span class="sxs-lookup"><span data-stu-id="45585-135">To create a new reason code in Personnel management, enter a new one in **New reason code**, and then enter a description in **New description**.</span></span>

   <span data-ttu-id="45585-136">[![Сопоставление с кодом причины в модуле "Управление персоналом"](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span><span class="sxs-lookup"><span data-stu-id="45585-136">[![Map to a Personnel management reason code](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span></span>

<span data-ttu-id="45585-137">После того как коды причин переносятся в модуль "Управление персоналом", параметр использования их в модуле "Управление льготами" автоматически устанавливается значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="45585-137">After reason codes migrate to Personnel management, the option for using them in Benefits management is automatically set to **Yes**.</span></span>

<span data-ttu-id="45585-138">[![Использование кода причин в управлении льготами](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span><span class="sxs-lookup"><span data-stu-id="45585-138">[![Use reason code in Benefits management](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]