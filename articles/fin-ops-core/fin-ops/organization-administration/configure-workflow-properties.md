---
title: Настройка свойств workflow-процесса
description: В этом разделе описывается, как настроить различные свойства workflow-процесса.
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bd3c9bea010099f83d16dad70261bc2d46a1dac
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693290"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="ec38b-103">Настройка свойств workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="ec38b-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec38b-104">В этом разделе описывается, как настроить различные свойства workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="ec38b-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="ec38b-105">Чтобы настроить свойства workflow-процесса, откройте workflow-процесс в редакторе workflow-процессов.</span><span class="sxs-lookup"><span data-stu-id="ec38b-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="ec38b-106">Щелкните холст редактора workflow-процессов, а затем щелкните **Свойства**, чтобы открыть страницу **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="ec38b-107">Можно использовать следующие процедуры для настройки различных свойств workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="ec38b-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="ec38b-108">Указать название документооборота</span><span class="sxs-lookup"><span data-stu-id="ec38b-108">Name the workflow</span></span>

<span data-ttu-id="ec38b-109">Чтобы ввести название workflow-процесса, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ec38b-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="ec38b-110">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="ec38b-111">В поле **Имя** введите уникальное название документооборота.</span><span class="sxs-lookup"><span data-stu-id="ec38b-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="ec38b-112">Например, если требуется создать workflow-процесс заявки на покупку для каждой страны или региона, в которых работает компания, можно назвать workflow-процесс заявки на покупку **Заявки на покупку: Дания** или **Заявки на покупку: Испания**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="ec38b-113">Указать владельца документооборота</span><span class="sxs-lookup"><span data-stu-id="ec38b-113">Specify the workflow owner</span></span>

<span data-ttu-id="ec38b-114">Владелец workflow-процесса — это лицо, которое будет управлять данным workflow-процесс и вести его.</span><span class="sxs-lookup"><span data-stu-id="ec38b-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="ec38b-115">Чтобы указать владельца workflow-процесса, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ec38b-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="ec38b-116">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="ec38b-117">Из списка **Владелец** выберите имя сотрудника, который будет управлять workflow-процессом.</span><span class="sxs-lookup"><span data-stu-id="ec38b-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="ec38b-118">Выберите шаблон электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ec38b-118">Select an email template</span></span>

<span data-ttu-id="ec38b-119">Выполните следующие шаги для выбора шаблона электронной почты, который будет использоваться для создания уведомлений о workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="ec38b-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="ec38b-120">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="ec38b-121">В списке **Шаблон электронной почты для уведомлений workflow-процесса** выберите шаблон.</span><span class="sxs-lookup"><span data-stu-id="ec38b-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="ec38b-122">Ввести инструкции для пользователей</span><span class="sxs-lookup"><span data-stu-id="ec38b-122">Enter instructions for users</span></span>

<span data-ttu-id="ec38b-123">Можно добавить инструкции для пользователей, представляющих документы на обработку и утверждения.</span><span class="sxs-lookup"><span data-stu-id="ec38b-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="ec38b-124">Эти пользователи также называются *инициаторами*.</span><span class="sxs-lookup"><span data-stu-id="ec38b-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="ec38b-125">Например, вы создаете workflow-процесс заявки на покупку и вводите инструкции.</span><span class="sxs-lookup"><span data-stu-id="ec38b-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="ec38b-126">Эти инструкции смогут просматривать пользователи, которые вводят заявки на покупку на странице **Заявки на покупку**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="ec38b-127">Исходный пользователь может щелкнуть значок в строке сообщений workflow-процесса, чтобы просмотреть инструкции.</span><span class="sxs-lookup"><span data-stu-id="ec38b-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="ec38b-128">Чтобы ввести инструкции для пользователей, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ec38b-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="ec38b-129">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="ec38b-130">В поле **Инструкции по отправке** введите инструкции.</span><span class="sxs-lookup"><span data-stu-id="ec38b-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="ec38b-131">Для того, чтобы персонализовать инструкции можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="ec38b-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="ec38b-132">Заполнители заменяются соответствующей информацией, когда инструкции отображаются пользователям.</span><span class="sxs-lookup"><span data-stu-id="ec38b-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="ec38b-133">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="ec38b-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="ec38b-134">Щелкните в поле **Инструкции по отправке**, чтобы указать, где должен находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="ec38b-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="ec38b-135">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="ec38b-136">В открывшемся списке выберите заполнитель, который необходимо вставить.</span><span class="sxs-lookup"><span data-stu-id="ec38b-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="ec38b-137">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-137">Click **Insert**.</span></span>

4. <span data-ttu-id="ec38b-138">Для добавления переводов инструкций выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ec38b-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="ec38b-139">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="ec38b-140">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="ec38b-141">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="ec38b-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="ec38b-142">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="ec38b-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="ec38b-143">Для того, чтобы персонализовать текст можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="ec38b-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="ec38b-144">Инструкции по вводу заполнителя см. на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="ec38b-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="ec38b-145">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a><span data-ttu-id="ec38b-146">Укажите, когда данный рабочей процесс используется в условиях активации</span><span class="sxs-lookup"><span data-stu-id="ec38b-146">Specify when this workflow is used through activation conditions</span></span>

<span data-ttu-id="ec38b-147">Можно создать несколько workflow-процессов на основе одного и того же типа рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="ec38b-147">You can create multiple workflows that are based on the same workflow type.</span></span> <span data-ttu-id="ec38b-148">Если в основе нескольких рабочих процессов лежит один и тот же тип, необходимо указать, когда следует использовать каждый рабочий процесс с помощью условий активации.</span><span class="sxs-lookup"><span data-stu-id="ec38b-148">When you have multiple workflows that are based on the same type, you must specify when each workflow is used using activation conditions.</span></span> <span data-ttu-id="ec38b-149">Если условия активации не выполняются, используется рабочий процесс по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ec38b-149">If activation conditions are not met, then the default workflow is used.</span></span> <span data-ttu-id="ec38b-150">Аналогично, если для типа рабочего процесса определена только одна конфигурация рабочего процесса, то эта конфигурация рабочего процесса будет использоваться независимо от условий активации.</span><span class="sxs-lookup"><span data-stu-id="ec38b-150">Similarly, if there is only one workflow configuration defined for a workflow type, then that workflow configuration will be used regardless of the activation conditions.</span></span>

<span data-ttu-id="ec38b-151">Например, пусть требуется создать рабочий процесс заявок на закупку для каждой страны или региона, в которых работает компания, (например, Заявки на закупку: Дания или Заявки на закупку: Испания) со следующими условиями.</span><span class="sxs-lookup"><span data-stu-id="ec38b-151">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain, with the following conditions:</span></span>

- <span data-ttu-id="ec38b-152">Заявки на закупку: Дания используется, когда страна (регион) = DK</span><span class="sxs-lookup"><span data-stu-id="ec38b-152">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="ec38b-153">Заявки на закупку: Испания используется, когда страна (регион) = ES</span><span class="sxs-lookup"><span data-stu-id="ec38b-153">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="ec38b-154">Чтобы указать, когда следует использовать настраиваемый workflow-процесс, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ec38b-154">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="ec38b-155">В левой области щелкните **Активация**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-155">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="ec38b-156">Установите флажок **Установка условий для запуска этого workflow-процесса**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-156">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="ec38b-157">Щелкните **Добавить условие**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-157">Click **Add condition**.</span></span>
4. <span data-ttu-id="ec38b-158">Введите условие.</span><span class="sxs-lookup"><span data-stu-id="ec38b-158">Enter a condition.</span></span>
5. <span data-ttu-id="ec38b-159">Введите все необходимые дополнительные условия.</span><span class="sxs-lookup"><span data-stu-id="ec38b-159">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="ec38b-160">Выполните рабочий процесс с несколькими целевыми записями, чтобы убедиться в том, что условие правильно включает или исключает записи.</span><span class="sxs-lookup"><span data-stu-id="ec38b-160">Run through the workflow with some target records to verify that the condition correctly includes and excludes records.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="ec38b-161">Задать условия отправки уведомлений</span><span class="sxs-lookup"><span data-stu-id="ec38b-161">Specify when notifications are sent</span></span>

<span data-ttu-id="ec38b-162">Когда документ представлен на обработку, создается экземпляр workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="ec38b-162">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="ec38b-163">При запуске, выполнении, завершении или отмене экземпляров workflow-процесса (созданных на основе данного workflow-процесса), а также при их остановке из-за ошибки пользователям могут быть отправлены уведомления.</span><span class="sxs-lookup"><span data-stu-id="ec38b-163">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="ec38b-164">Чтобы указать, когда следует отправлять уведомления, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ec38b-164">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="ec38b-165">В левой области щелкните **Уведомления**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-165">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="ec38b-166">Установите флажок для каждого события, запускающего уведомления:</span><span class="sxs-lookup"><span data-stu-id="ec38b-166">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="ec38b-167">**Запущено** — отправка уведомлений при запуске экземпляра workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="ec38b-167">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="ec38b-168">**Остановлено** — уведомления будут отправляться, если экземпляр workflow-процесса остановлен из-за ошибки.</span><span class="sxs-lookup"><span data-stu-id="ec38b-168">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="ec38b-169">**Выполнено** — уведомления будут отправляться при выполнении экземпляра workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="ec38b-169">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="ec38b-170">**Неустранимо** — уведомления будут отправляться, если экземпляр workflow-процесса остановлен из-за неустранимой ошибки.</span><span class="sxs-lookup"><span data-stu-id="ec38b-170">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="ec38b-171">**Завершено** — уведомления будут отправляться при завершении экземпляра workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="ec38b-171">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="ec38b-172">Выберите строку для события, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="ec38b-172">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="ec38b-173">На вкладке **Текст уведомления** введите текст уведомления.</span><span class="sxs-lookup"><span data-stu-id="ec38b-173">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="ec38b-174">Для того, чтобы персонализовать текст можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="ec38b-174">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="ec38b-175">Заполнители заменяются соответствующей информацией, когда текст отображается пользователям.</span><span class="sxs-lookup"><span data-stu-id="ec38b-175">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="ec38b-176">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="ec38b-176">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="ec38b-177">Щелкните в поле ,чтобы указать, где должен находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="ec38b-177">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="ec38b-178">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-178">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="ec38b-179">В открывшемся списке выберите заполнитель, который необходимо вставить.</span><span class="sxs-lookup"><span data-stu-id="ec38b-179">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="ec38b-180">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-180">Click **Insert**.</span></span>
    5. <span data-ttu-id="ec38b-181">Общий заполнитель **Текст уведомления**, который необходимо включить, это "Последние замечания: %Workflow.Last note%", который отображает все комментарии из предыдущего шага.</span><span class="sxs-lookup"><span data-stu-id="ec38b-181">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="ec38b-182">Для добавления переводов текста выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ec38b-182">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="ec38b-183">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-183">Click **Translations**.</span></span>
    2. <span data-ttu-id="ec38b-184">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-184">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="ec38b-185">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="ec38b-185">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="ec38b-186">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="ec38b-186">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="ec38b-187">Для того, чтобы персонализовать текст можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="ec38b-187">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="ec38b-188">Инструкции по вводу заполнителя см. на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="ec38b-188">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="ec38b-189">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-189">Click **Close**.</span></span>

7. <span data-ttu-id="ec38b-190">На вкладке **Получатель** используйте следующие параметры, чтобы указать, кто должен получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="ec38b-190">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="ec38b-191">Параметр</span><span class="sxs-lookup"><span data-stu-id="ec38b-191">Option</span></span></th>
    <th><span data-ttu-id="ec38b-192">Уведомления отправляются этим пользователям</span><span class="sxs-lookup"><span data-stu-id="ec38b-192">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="ec38b-193">Для отправки уведомлений выполните следующие действия</span><span class="sxs-lookup"><span data-stu-id="ec38b-193">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="ec38b-194">Участник</span><span class="sxs-lookup"><span data-stu-id="ec38b-194">Participant</span></span></td>
    <td><span data-ttu-id="ec38b-195">Пользователи, назначенные для конкретной группы или роли</span><span class="sxs-lookup"><span data-stu-id="ec38b-195">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ec38b-196">На вкладке <strong>Получатель</strong> щелкните <strong>Участник</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec38b-196">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="ec38b-197">На вкладке <strong>На основе роли</strong> в списке <strong>Тип участника</strong> выберите тип группы или роли, которой требуется отправить уведомления.</span><span class="sxs-lookup"><span data-stu-id="ec38b-197">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="ec38b-198">В списке <strong>Участник</strong> выберите группу или роль, которой нужно отправлять уведомления.</span><span class="sxs-lookup"><span data-stu-id="ec38b-198">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ec38b-199">Пользователь workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="ec38b-199">Workflow user</span></span></td>
    <td><span data-ttu-id="ec38b-200">Пользователи-участники в этом workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="ec38b-200">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ec38b-201">На вкладке <strong>Получатель</strong> щелкните <strong>Пользователь workflow-процесса</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec38b-201">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="ec38b-202">На вкладке <strong>Пользователь workflow-процесса</strong> в списке <strong>Пользователь workflow-процесса</strong> выберите участника в этом workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="ec38b-202">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ec38b-203">Пользователь</span><span class="sxs-lookup"><span data-stu-id="ec38b-203">User</span></span></td>
    <td><span data-ttu-id="ec38b-204">Определенные пользователи</span><span class="sxs-lookup"><span data-stu-id="ec38b-204">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ec38b-205">На вкладке <strong>Получатель</strong> щелкните <strong>Пользователь</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec38b-205">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="ec38b-206">На вкладке <strong>Пользователь</strong> список <strong>Доступные пользователи</strong> включает всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="ec38b-206">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="ec38b-207">Выберите пользователей, которым требуется отправить уведомления, а затем переместите этих пользователей в список <strong>Выбранные пользователи</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec38b-207">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="ec38b-208">Повторите шаги 3–7 для каждого события, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="ec38b-208">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="ec38b-209">Ввод комментариев об изменениях, внесенных в workflow-процесс</span><span class="sxs-lookup"><span data-stu-id="ec38b-209">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="ec38b-210">Чтобы ввести комментарии об изменениях, внесенных в workflow-процесс, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ec38b-210">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="ec38b-211">В левой области щелкните **Примечания**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-211">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="ec38b-212">В поле **Введите комментарии о workflow-процессе** введите комментарии.</span><span class="sxs-lookup"><span data-stu-id="ec38b-212">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="ec38b-213">Проверьте комментарии.</span><span class="sxs-lookup"><span data-stu-id="ec38b-213">Review your comments.</span></span> <span data-ttu-id="ec38b-214">После добавления комментариев их невозможно изменить.</span><span class="sxs-lookup"><span data-stu-id="ec38b-214">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="ec38b-215">Нажмите кнопку **Добавить** для добавления комментариев в область **История комментариев**.</span><span class="sxs-lookup"><span data-stu-id="ec38b-215">Click **Add** to add your comments to the **Comment history** area.</span></span>
