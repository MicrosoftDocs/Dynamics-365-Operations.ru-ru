---
title: Включение и настройка автоматических накладных расходов по каналам
description: В этой теме объясняется, как включить и настроить автоматические накладные расходы по каналам в Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: d37b2b785dd29850dcd02d0905e5872445384990
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993736"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a><span data-ttu-id="b5e61-103">Включение и настройка автоматических накладных расходов по каналам</span><span class="sxs-lookup"><span data-stu-id="b5e61-103">Enable and configure auto charges by channel</span></span>

<span data-ttu-id="b5e61-104">В этой теме объясняется, как включить и настроить автоматические накладные расходы (авторасходы) по каналам в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b5e61-104">This topic explains how to enable and configure automatic charges (auto charges) by channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b5e61-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="b5e61-105">Overview</span></span>

<span data-ttu-id="b5e61-106">Могут существовать сценарии, в которых сборы за утилизацию или другие сборы должны быть применены к группе продуктов, которые продаются во всех или некоторых магазинах в определенном штате (например, в Калифорнии).</span><span class="sxs-lookup"><span data-stu-id="b5e61-106">You might have scenarios where recycling fees or other fees must be applied to a group of products that are sold in all or some stores in a specific state (for example, California).</span></span> <span data-ttu-id="b5e61-107">Функция **Включить фильтрацию автоматических расходов по каналам** в модуле Commerce позволяет задавать автоматические накладные расходы по каналам (например, конкретный физический канал).</span><span class="sxs-lookup"><span data-stu-id="b5e61-107">The **Enable filter auto charges by channel** feature in Commerce lets you specify auto charges by channel (for example, a specific brick-and-mortar channel).</span></span> <span data-ttu-id="b5e61-108">Эта функция доступна в Dynamics 365 Commerce версии 10.0.10 и выше.</span><span class="sxs-lookup"><span data-stu-id="b5e61-108">This feature is available in Dynamics 365 Commerce version 10.0.10 and later.</span></span>

<span data-ttu-id="b5e61-109">Чтобы включить и настроить автоматические накладные расходы по каналам, необходимо выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="b5e61-109">To enable and configure auto charges by channel, you must complete the following tasks:</span></span>

- <span data-ttu-id="b5e61-110">Включите функцию **Включить фильтрацию автоматических расходов по каналам**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-110">Turn on the **Enable filter auto charges by channel** feature.</span></span>
- <span data-ttu-id="b5e61-111">Настройте цель организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="b5e61-111">Configure the organization hierarchy purpose.</span></span>
- <span data-ttu-id="b5e61-112">Определите автоматические накладные расходы по каналам.</span><span class="sxs-lookup"><span data-stu-id="b5e61-112">Define auto charges by channel.</span></span>

> [!NOTE]
> <span data-ttu-id="b5e61-113">Функция **Включить фильтрацию автоматических расходов по каналам** работает только в том случае, если включена также функция расширенных автоматических накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="b5e61-113">The **Enable filter auto charges by channel** feature works only if the advanced auto charges feature is also turned on.</span></span> <span data-ttu-id="b5e61-114">Сведения о порядке включении функции расширенных автоматических накладных расходов см. в разделе [Омниканальные расширенные автоматические накладные расходы](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="b5e61-114">For information about how to turn on the advanced auto charges feature, see [Omni-channel advanced auto charges](omni-auto-charges.md).</span></span>

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a><span data-ttu-id="b5e61-115">Включение функции "Включить фильтрацию автоматических расходов по каналам"</span><span class="sxs-lookup"><span data-stu-id="b5e61-115">Turn on the Enable filter auto charges by channel feature</span></span>

<span data-ttu-id="b5e61-116">Чтобы включить автоматические накладные расходы по каналам в модуле Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b5e61-116">To enable auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b5e61-117">Перейдите в раздел **Системный администратор \> Рабочие области \> Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-117">Go to **System administrator \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="b5e61-118">На вкладке **Не включено** в списке **Имя функции** найдите и выберите **Включить фильтрацию автоматических расходов по каналам**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-118">On the **Not enabled** tab, in the **Feature name** list, find and select **Enable filter auto charges by channel**.</span></span>
1. <span data-ttu-id="b5e61-119">В правом нижнем углу установите флажок **Включить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-119">In the lower-right corner, select **Enable now**.</span></span> <span data-ttu-id="b5e61-120">После включения функции она появится в списке на вкладке **Все**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-120">After the feature has been turned on, it will appear in the list on the **All** tab.</span></span>
1. <span data-ttu-id="b5e61-121">Перейдите в раздел **Retail и Commerce \> ИТ Retail и Commerce \> График распределения**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-121">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="b5e61-122">В левой области найдите и выберите задание **1110** (**Глобальная конфигурация**).</span><span class="sxs-lookup"><span data-stu-id="b5e61-122">In the left pane, find and select the **1110** (**Global configuration**) job.</span></span>
1. <span data-ttu-id="b5e61-123">На панели операций выберите **Выполнить сейчас**, чтобы распространить изменения конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b5e61-123">On the Action Pane, select **Run now** to propagate the configuration changes.</span></span>

> [!WARNING]
> <span data-ttu-id="b5e61-124">Если выключить функцию **Включить фильтрацию автоматических расходов по каналам** после того, как она уже была использована, поле **Связь канала розничной торговли** в разделе **Автоматические затраты** больше не будет отображаться, и все существующие конфигурации будут утрачены.</span><span class="sxs-lookup"><span data-stu-id="b5e61-124">If you turn off the **Enable filter auto charges by channel** feature after you've already used it, the **Retail channel relation** field under **Auto charges** will no longer appear, and you will lose all existing configurations.</span></span> <span data-ttu-id="b5e61-125">Если удаление конфигураций **Связь канала розничной торговли** приведет к дублированию правил автоматических накладных расходов, попытка отключения функции будет невозможна.</span><span class="sxs-lookup"><span data-stu-id="b5e61-125">If removal of the **Retail channel relation** configurations will cause auto charges rules to be duplicated, an attempt to turn off the feature will fail.</span></span> <span data-ttu-id="b5e61-126">Прежде чем отключить функцию, просмотрите все правила автоматических накладных расходов и внесите необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="b5e61-126">Before you turn off the feature, be sure to review all auto charges rules and make any required changes.</span></span>

## <a name="configure-the-organization-hierarchy-purpose"></a><span data-ttu-id="b5e61-127">Настройка цели организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="b5e61-127">Configure the organization hierarchy purpose</span></span>

<span data-ttu-id="b5e61-128">Для управления иерархией автоматических накладных расходов по каналам была создана новая цель организационной иерархии, именуемая **Автоматические накладные расходы розничной торговли**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-128">A new organization hierarchy purpose that is named **Retail auto charge** has been created to manage the hierarchy for auto charges by channel.</span></span>

<span data-ttu-id="b5e61-129">Чтобы назначить иерархию по умолчанию цели организационной иерархии в модуле Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b5e61-129">To assign a default hierarchy to an organization hierarchy purpose in Commerce, follow these steps.</span></span>
        
1. <span data-ttu-id="b5e61-130">Перейдите в раздел **Управление организацией \> Организации \> Цели организационной иерархии**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-130">Go to **Organization administration \> Organizations \> Organization hierarchy purposes**.</span></span>
1. <span data-ttu-id="b5e61-131">В левой области выберите **Автоматические накладные расходы розничной торговли**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-131">In the left pane, select **Retail auto charge**.</span></span>
1. <span data-ttu-id="b5e61-132">В области **Назначенные иерархии** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-132">Under **Assigned hierarchies**, select **Add**.</span></span>
1. <span data-ttu-id="b5e61-133">В диалоговом окне **Организационные иерархии** выберите организационную иерархию (например, **Розничные магазины по регионам**), затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-133">In the **Organization hierarchies** dialog box, select an organization hierarchy (for example, **Retail Stores by Region**), and then select **OK**.</span></span>
1. <span data-ttu-id="b5e61-134">В области **Назначенные иерархии** выберите **Установить по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-134">Under **Assigned hierarchies**, select **Set as default**.</span></span>
1. <span data-ttu-id="b5e61-135">Перейдите в раздел **Retail и Commerce \> ИТ Retail и Commerce \> График распределения**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="b5e61-136">В левой области найдите и выберите задание **1040** (**Продукты**).</span><span class="sxs-lookup"><span data-stu-id="b5e61-136">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="b5e61-137">В области действий выберите **Выполнить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-137">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="b5e61-138">Повторите предыдущие два шага, чтобы выполнить задания **1070** (**Конфигурация канала**) и **1110** (**Глобальная конфигурация**).</span><span class="sxs-lookup"><span data-stu-id="b5e61-138">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>

![Конфигурация цели организационной иерархии автоматических накладных расходов для розничной торговли](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a><span data-ttu-id="b5e61-140">Определение автоматических накладных расходов по каналам</span><span class="sxs-lookup"><span data-stu-id="b5e61-140">Define auto charges by channel</span></span>

<span data-ttu-id="b5e61-141">После включения функции **Включить фильтрацию автоматических расходов по каналам** и настройки цели организационной иерархии **Автоматические накладные расходы розничной торговли** автоматические накладные расходы по каналам можно определить на уровне заголовка заказа или на уровне строки заказа.</span><span class="sxs-lookup"><span data-stu-id="b5e61-141">After you've turned on the **Enable filter auto charges by channel** feature and configured the **Retail auto charge** organization hierarchy purpose, auto charges by channel can be defined at either the order header level or the order line level.</span></span>

<span data-ttu-id="b5e61-142">Чтобы определить автоматические накладные расходы по каналам в модуле Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b5e61-142">To define auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b5e61-143">Перейдите в раздел **Расчеты с клиентами \> Настройка накладных расходов \> Автоматические затраты**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-143">Go to **Accounts receivable \> Charges setup \> Auto charges**.</span></span>
1. <span data-ttu-id="b5e61-144">В левой области в поле **Уровень** выберите **Заголовок** или **Строка**, в зависимости от бизнес-требований.</span><span class="sxs-lookup"><span data-stu-id="b5e61-144">In the left pane, in the **Level** field, select either **Header** or **Line**, depending on your business requirements.</span></span>
1. <span data-ttu-id="b5e61-145">В поле **Код канала розничной торговли** выберите соответствующий код канала (например, **Таблица** или **Группа**).</span><span class="sxs-lookup"><span data-stu-id="b5e61-145">In the **Retail channel code** field, select the appropriate channel code (for example, **Table** or **Group**).</span></span> <span data-ttu-id="b5e61-146">Если используется настройка по умолчанию **Все**, правила накладных расходов применяются ко всем каналам.</span><span class="sxs-lookup"><span data-stu-id="b5e61-146">If the default setting, **All**, is used, charge rules are applied to all channels.</span></span>

    - <span data-ttu-id="b5e61-147">Если выбрано значение **Группа**, убедитесь, что группа накладных расходов розничной торговли создана в пункте **Retail и Commerce \> Настройка канала \> Накладные расходы \> Группы накладных расходов каналов розничной торговли**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-147">If you select **Group**, make sure that a retail channel charges group is created at **Retail and Commerce \> Channel setup \> Charges \> Retail channel charge groups**.</span></span>
    - <span data-ttu-id="b5e61-148">Если выбрано значение **Таблица**, можно выбрать конкретный канал (например, **Сан-Франциско**) в поле **Связь канала розничной торговли**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-148">If you select **Table**, you can select a specific channel (for example, **San Francisco**) in the **Retail channel relation** field.</span></span>

1. <span data-ttu-id="b5e61-149">Перейдите в раздел **Retail и Commerce \> ИТ Retail и Commerce \> График распределения**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-149">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="b5e61-150">В левой области найдите и выберите задание **1040** (**Продукты**).</span><span class="sxs-lookup"><span data-stu-id="b5e61-150">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="b5e61-151">В области действий выберите **Выполнить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-151">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="b5e61-152">Повторите предыдущие два шага, чтобы выполнить задания **1070** (**Конфигурация канала**) и **1110** (**Глобальная конфигурация**).</span><span class="sxs-lookup"><span data-stu-id="b5e61-152">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>
    
![Автоматические накладные расходы, определенные по каналам](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a><span data-ttu-id="b5e61-154">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="b5e61-154">Example scenario</span></span>

<span data-ttu-id="b5e61-155">В следующем примере описываются шаги, необходимые для настройки продукта таким образом, чтобы сборы за утилизацию начисляются при продаже продукта через физический канал в Сан-Франциско.</span><span class="sxs-lookup"><span data-stu-id="b5e61-155">The following example outlines the steps that are required to configure a product so that recycling fees are charged when the product is sold through a San Francisco brick-and-mortar channel.</span></span> <span data-ttu-id="b5e61-156">В примере также показано, как автоматические накладные расходы появляются в POS-приложении Commerce.</span><span class="sxs-lookup"><span data-stu-id="b5e61-156">The example also shows how the auto charges appear in the Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="b5e61-157">Организация определяет код накладных расходов под названием **УТИЛИЗАЦИЯ**, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="b5e61-157">The organization defines a charges code that is named **RECYCLE**, as shown in the following illustration.</span></span>

![Код накладных расходов УТИЛИЗАЦИЯ](media/Auto-charges-charge-code.png)

<span data-ttu-id="b5e61-159">Автоматические накладные расходы созданы на уровне строки.</span><span class="sxs-lookup"><span data-stu-id="b5e61-159">An auto charge is created at the line level.</span></span> <span data-ttu-id="b5e61-160">Они имеют следующую конфигурацию:</span><span class="sxs-lookup"><span data-stu-id="b5e61-160">It has the following configuration:</span></span>

- <span data-ttu-id="b5e61-161">В поле **Код счета** задано значение **Все**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-161">The **Account code** field is set to **All**.</span></span>
- <span data-ttu-id="b5e61-162">В поле **Код номенклатуры** задано значение **Таблица**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-162">The **Item code** field is set to **Table**.</span></span>
- <span data-ttu-id="b5e61-163">В поле **Связь номенклатуры** задан код продукта **91001**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-163">The **Item relation** field is set to product ID **91001**.</span></span>
- <span data-ttu-id="b5e61-164">В поле **Код режима доставки** задано значение **Все**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-164">The **Mode of delivery code** field is set to **All**.</span></span>
- <span data-ttu-id="b5e61-165">В поле **Код канала розничной торговли** задано значение **Таблица**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-165">The **Retail channel code** field is set to **Table**.</span></span>
- <span data-ttu-id="b5e61-166">В поле **Связь канала розничной торговли** задан магазин **Сан-Франциско**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-166">The **Retail channel relation** field is set to the **San Francisco** store.</span></span>

<span data-ttu-id="b5e61-167">Создается строка с автоматическими накладными расходами.</span><span class="sxs-lookup"><span data-stu-id="b5e61-167">An auto charges line is created.</span></span> <span data-ttu-id="b5e61-168">Они имеют следующую конфигурацию:</span><span class="sxs-lookup"><span data-stu-id="b5e61-168">It has the following configuration:</span></span>

- <span data-ttu-id="b5e61-169">В поле **Валюта** установлено значение **Доллары США**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-169">The **Currency** field is set to **USD**.</span></span>
- <span data-ttu-id="b5e61-170">В поле **Код накладных расходов** задано значение **УТИЛИЗАЦИЯ**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-170">The **Charges code** field is set to **RECYCLE**.</span></span>
- <span data-ttu-id="b5e61-171">В поле **Категория** задано значение **Фиксированные**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-171">The **Category** field is set to **Fixed**.</span></span>
- <span data-ttu-id="b5e61-172">В поле **Расходы** установлено значение **6,25 долл. США**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-172">The **Charges** field is set to **$6.25**.</span></span>

![Конфигурация автоматических накладных расходов уровня строки и строка автоматических накладных расходов](media/Auto-charges-recyclingfee-line-fee.png)

<span data-ttu-id="b5e61-174">В POS-приложении заказ на продажу создается в канале магазина **Сан-Франциско**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-174">In the POS application, a sales order is created in the **San Francisco** store channel.</span></span> <span data-ttu-id="b5e61-175">В строке **Расходы** отображается сбор на утилизацию **6,25 долл. США**.</span><span class="sxs-lookup"><span data-stu-id="b5e61-175">The **Charges** line shows the recycling fee of **$6.25**.</span></span>

<span data-ttu-id="b5e61-176">Выбрав **Параметры проводок \> Накладные расходы \> Управление накладными расходами** в приложении POS, можно просмотреть код и описание накладных расходов для сборов за утилизацию.</span><span class="sxs-lookup"><span data-stu-id="b5e61-176">By selecting **Transaction options \> Charges \> Manage charges** in the POS application, you can view the charges code and description for the recycling fee.</span></span>

![Сбор за утилизацию в приложении для POS-терминала](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a><span data-ttu-id="b5e61-178">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b5e61-178">Additional resources</span></span>

[<span data-ttu-id="b5e61-179">Омниканальные расширенные автоматические накладные расходы</span><span class="sxs-lookup"><span data-stu-id="b5e61-179">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="b5e61-180">Пропорциональное распределение накладных расходов из заголовка по соответствующим строкам продаж</span><span class="sxs-lookup"><span data-stu-id="b5e61-180">Prorate header charges to matching sales lines</span></span>](pro-rate-charges-matching-lines.md)
