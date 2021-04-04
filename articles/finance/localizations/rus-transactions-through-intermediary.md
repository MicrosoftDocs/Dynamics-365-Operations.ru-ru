---
title: Проводки через посредников
description: В этой теме приводятся сведения о функциях для бухгалтерских сделок через посредника, выполненных агентом.
author: v-nadyuz
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: roschlom
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 072f1b3ffc7ec6cc2f02f3c3f78d71bd6ea73871
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253894"
---
# <a name="transactions-through-intermediary"></a><span data-ttu-id="ab7e2-103">Проводки через посредников</span><span class="sxs-lookup"><span data-stu-id="ab7e2-103">Transactions through intermediary</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab7e2-104">В экономических действиях, включающих посредников, существует три участника:</span><span class="sxs-lookup"><span data-stu-id="ab7e2-104">In economic activities that involve an intermediary, there are three participants:</span></span>

- <span data-ttu-id="ab7e2-105">Лицо, которое продает или покупает товары (работы или услуги)</span><span class="sxs-lookup"><span data-stu-id="ab7e2-105">The person who sells or purchases goods (works or services)</span></span>
- <span data-ttu-id="ab7e2-106">Сторонний поставщик или покупатель</span><span class="sxs-lookup"><span data-stu-id="ab7e2-106">The third-party supplier or buyer</span></span>
- <span data-ttu-id="ab7e2-107">Посредник между двумя первыми участниками</span><span class="sxs-lookup"><span data-stu-id="ab7e2-107">The intermediary between the first two participants</span></span>

<span data-ttu-id="ab7e2-108">Российский законодательство определяет три юридические формы посреднических услуг:</span><span class="sxs-lookup"><span data-stu-id="ab7e2-108">Russian legislation defines three legal forms of intermediation:</span></span>

- <span data-ttu-id="ab7e2-109">Комиссионный договор, в котором доверитель (называемая также принципалом) нанимает комиссионера</span><span class="sxs-lookup"><span data-stu-id="ab7e2-109">A commission agreement, where the committer (also known as the principal) engages a commissioner</span></span>
- <span data-ttu-id="ab7e2-110">Агентский договор, в котором доверитель нанимает агента</span><span class="sxs-lookup"><span data-stu-id="ab7e2-110">An agency agreement, where the principal engages an agent</span></span>
- <span data-ttu-id="ab7e2-111">Договор цессии, в котором доверитель нанимает адвоката</span><span class="sxs-lookup"><span data-stu-id="ab7e2-111">An assignment agreement, where the principal retains an attorney</span></span>

<span data-ttu-id="ab7e2-112">Посредник (то есть, комиссионер, агент или юрист) выполняет юридические действия и другие действия (проводки) от имени доверителя.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-112">The intermediary (that is, the commissioner, agent, or attorney) performs legal actions and other actions (transactions) on behalf of the principal.</span></span> <span data-ttu-id="ab7e2-113">Посредники могут выполнять эти действия одним из двух способов:</span><span class="sxs-lookup"><span data-stu-id="ab7e2-113">Intermediaries can perform these actions in one of two ways:</span></span>

- <span data-ttu-id="ab7e2-114">От своего имени, но за счет доверителя</span><span class="sxs-lookup"><span data-stu-id="ab7e2-114">In their own name but at the principal's expense</span></span>
- <span data-ttu-id="ab7e2-115">От имени доверителя и за счет доверителя</span><span class="sxs-lookup"><span data-stu-id="ab7e2-115">In the principal's name and at the principal's expense</span></span>

<span data-ttu-id="ab7e2-116">В этой теме термин *доверитель* относится к субъекту, который нанимает агента.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-116">Throughout this topic, the term *principal* refers to the party that engages the agent.</span></span>

## <a name="overview"></a><span data-ttu-id="ab7e2-117">Обзор</span><span class="sxs-lookup"><span data-stu-id="ab7e2-117">Overview</span></span>

<span data-ttu-id="ab7e2-118">Текущая реализация этой функциональности имеет следующие ограничения:</span><span class="sxs-lookup"><span data-stu-id="ab7e2-118">The current implementation of this functionality has the following limitations:</span></span>

- <span data-ttu-id="ab7e2-119">Кредит-ноты могут регистрироваться только в модуле, в котором были зарегистрированы исходные счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-119">Credit notes can be registered only in the module where the original factures were registered.</span></span>
- <span data-ttu-id="ab7e2-120">Вложенная комиссия не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-120">Sub-commission isn't supported.</span></span>
- <span data-ttu-id="ab7e2-121">Комиссионные премиальные не рассчитываются.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-121">No commission bonus is calculated.</span></span>
- <span data-ttu-id="ab7e2-122">Никакие проводки не создаются в главной книге на основе отчета для доверителя.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-122">No transactions are created in the general ledger, based on the report for the principal.</span></span>

## <a name="preliminary-setup"></a><span data-ttu-id="ab7e2-123">Предварительная настройка</span><span class="sxs-lookup"><span data-stu-id="ab7e2-123">Preliminary setup</span></span>

### <a name="set-up-an-inventory-profile-for-an-agents-transactions"></a><span data-ttu-id="ab7e2-124">Настройка профиля учета для проводок агента</span><span class="sxs-lookup"><span data-stu-id="ab7e2-124">Set up an inventory profile for an agent's transactions</span></span>

1. <span data-ttu-id="ab7e2-125">Перейдите в раздел **Управление запасами** \> **Настройка** \> **Аналитики** \> **Профили учета**.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-125">Go to **Inventory management** \> **Setup** \> **Dimensions** \> **Inventory profiles**.</span></span>
2. <span data-ttu-id="ab7e2-126">Выберите **Создать**, чтобы создать профиль учета.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-126">Select **New** to create an inventory profile.</span></span>
3. <span data-ttu-id="ab7e2-127">В поле **Профиль учета** введите имя для профиля учета.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-127">In the **Inventory profile** field, enter a name for the inventory profile.</span></span>
4. <span data-ttu-id="ab7e2-128">В поле **Имя** введите описание.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-128">In the **Name** field, enter a description.</span></span>
5. <span data-ttu-id="ab7e2-129">В поле **Вид деятельности** выберите **Комиссионер**.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-129">In the **Kind of activity** field, select **Commission agent**.</span></span>
6. <span data-ttu-id="ab7e2-130">Задайте для параметра **Не подбирать** значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-130">Set the **Don't match** option to **No**.</span></span>
7. <span data-ttu-id="ab7e2-131">В поле **Вид запасов** укажите **Общие**.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-131">In the **Kind of inventory** field, specify **Common**.</span></span>
8. <span data-ttu-id="ab7e2-132">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-132">Select **Save**.</span></span>

![Страница профилей учета](media/1_Inventory_profiles.jpg)

### <a name="set-up-the-inventory-profile-and-owner-tracking-dimensions"></a><span data-ttu-id="ab7e2-134">Настройка аналитик отслеживания профиля учета и владельца</span><span class="sxs-lookup"><span data-stu-id="ab7e2-134">Set up the Inventory profile and Owner tracking dimensions</span></span>

1. <span data-ttu-id="ab7e2-135">Откройте **Управление сведениями о продукте** \> **Настройка** \> **Группы аналитик и вариантов** \> **Группы аналитик отслеживания**.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-135">Go to **Product information management** \> **Setup** \> **Dimension and variant groups** \> **Tracking dimension groups**.</span></span>
2. <span data-ttu-id="ab7e2-136">Выберите **Создать**, чтобы создать группу аналитик.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-136">Select **New** to create a dimension group.</span></span>
3. <span data-ttu-id="ab7e2-137">В поле **Имя** введите название группы аналитик.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-137">In the **Name** field, enter a name for the dimension group.</span></span>
4. <span data-ttu-id="ab7e2-138">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-138">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="ab7e2-139">На экспресс-вкладке **Аналитики отслеживания** настройте аналитики отслеживания "Профиль учета" и "Владелец":</span><span class="sxs-lookup"><span data-stu-id="ab7e2-139">On the **Tracking dimensions** FastTab, set up the Inventory profile and Owner tracking dimensions:</span></span>

    - <span data-ttu-id="ab7e2-140">В строке **Профиль учета** установите флажки **Активный**, **Первичная аналитика хранения**, **Физические запасы**, **Финансовые запасы**, **План покрытия по аналитикам** и **Перемещение**.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-140">On the **Inventory profile** line, select the **Active**, **Primary stocking**, **Physical inventory**, **Financial inventory**, **Coverage plan by dimensions**, and **Transfer** check boxes.</span></span>
    - <span data-ttu-id="ab7e2-141">В строке **Владелец** установите флажки **Активный**, **Физические запасы** и **Перемещение**.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-141">On the **Owner** line, select the **Active**, **Physical inventory**, and **Transfer** check boxes.</span></span>

6. <span data-ttu-id="ab7e2-142">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-142">Select **Save**.</span></span>

![Страница групп аналитик отслеживания](media/2_Tracking_dimension_groups.jpg)

### <a name="set-up-a-number-sequence-for-the-report-for-the-principal"></a><span data-ttu-id="ab7e2-144">Настройка номерной серии для отчета для доверителя</span><span class="sxs-lookup"><span data-stu-id="ab7e2-144">Set up a number sequence for the report for the principal</span></span>

1. <span data-ttu-id="ab7e2-145">Перейдите в раздел **Главная книга** \> **Настройка главной книги** \> **Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-145">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="ab7e2-146">На вкладке **Номерные серии** в поле **Код номерной серии** выберите код номерной серии для ссылки **Код отчета**.</span><span class="sxs-lookup"><span data-stu-id="ab7e2-146">On the **Number sequences** tab, in the **Number sequence code** field, select a number sequence code for the **Report code** reference.</span></span>

<span data-ttu-id="ab7e2-147">Дополнительные сведения см. в разделах [Покупки по комиссии](rus-purchases-on-commission.md) и [Продажи по комиссии](rus-sales-on-commission.md).</span><span class="sxs-lookup"><span data-stu-id="ab7e2-147">For more information, see [Purchases on commission](rus-purchases-on-commission.md) and [Sales on commission](rus-sales-on-commission.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]