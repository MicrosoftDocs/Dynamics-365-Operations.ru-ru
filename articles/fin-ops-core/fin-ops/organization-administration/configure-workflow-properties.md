---
title: Настройка свойств workflow-процесса
description: В этом разделе описывается, как настроить различные свойства workflow-процесса.
author: sericks007
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d745389b37b899760ea32ae75c5cb80d9139be2d
ms.sourcegitcommit: 1852f08f015acd106f4cefd03fa07985dc009123
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2020
ms.locfileid: "3199444"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="19cd6-103">Настройка свойств workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="19cd6-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19cd6-104">В этом разделе описывается, как настроить различные свойства workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="19cd6-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="19cd6-105">Чтобы настроить свойства workflow-процесса, откройте workflow-процесс в редакторе workflow-процессов.</span><span class="sxs-lookup"><span data-stu-id="19cd6-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="19cd6-106">Щелкните холст редактора workflow-процессов, а затем щелкните **Свойства**, чтобы открыть страницу **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="19cd6-107">Можно использовать следующие процедуры для настройки различных свойств workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="19cd6-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="19cd6-108">Указать название документооборота</span><span class="sxs-lookup"><span data-stu-id="19cd6-108">Name the workflow</span></span>

<span data-ttu-id="19cd6-109">Чтобы ввести название workflow-процесса, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="19cd6-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="19cd6-110">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="19cd6-111">В поле **Имя** введите уникальное название документооборота.</span><span class="sxs-lookup"><span data-stu-id="19cd6-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="19cd6-112">Например, если требуется создать workflow-процесс заявки на покупку для каждой страны или региона, в которых работает компания, можно назвать workflow-процесс заявки на покупку **Заявки на покупку: Дания** или **Заявки на покупку: Испания**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="19cd6-113">Указать владельца документооборота</span><span class="sxs-lookup"><span data-stu-id="19cd6-113">Specify the workflow owner</span></span>

<span data-ttu-id="19cd6-114">Владелец workflow-процесса — это лицо, которое будет управлять данным workflow-процесс и вести его.</span><span class="sxs-lookup"><span data-stu-id="19cd6-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="19cd6-115">Чтобы указать владельца workflow-процесса, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="19cd6-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="19cd6-116">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="19cd6-117">Из списка **Владелец** выберите имя сотрудника, который будет управлять workflow-процессом.</span><span class="sxs-lookup"><span data-stu-id="19cd6-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="19cd6-118">Выберите шаблон электронной почты.</span><span class="sxs-lookup"><span data-stu-id="19cd6-118">Select an email template</span></span>

<span data-ttu-id="19cd6-119">Выполните следующие шаги для выбора шаблона электронной почты, который будет использоваться для создания уведомлений о workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="19cd6-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="19cd6-120">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="19cd6-121">В списке **Шаблон электронной почты для уведомлений workflow-процесса** выберите шаблон.</span><span class="sxs-lookup"><span data-stu-id="19cd6-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="19cd6-122">Ввести инструкции для пользователей</span><span class="sxs-lookup"><span data-stu-id="19cd6-122">Enter instructions for users</span></span>

<span data-ttu-id="19cd6-123">Можно добавить инструкции для пользователей, представляющих документы на обработку и утверждения.</span><span class="sxs-lookup"><span data-stu-id="19cd6-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="19cd6-124">Эти пользователи также называются *инициаторами*.</span><span class="sxs-lookup"><span data-stu-id="19cd6-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="19cd6-125">Например, вы создаете workflow-процесс заявки на покупку и вводите инструкции.</span><span class="sxs-lookup"><span data-stu-id="19cd6-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="19cd6-126">Эти инструкции смогут просматривать пользователи, которые вводят заявки на покупку на странице **Заявки на покупку**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="19cd6-127">Исходный пользователь может щелкнуть значок в строке сообщений workflow-процесса, чтобы просмотреть инструкции.</span><span class="sxs-lookup"><span data-stu-id="19cd6-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="19cd6-128">Чтобы ввести инструкции для пользователей, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="19cd6-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="19cd6-129">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="19cd6-130">В поле **Инструкции по отправке** введите инструкции.</span><span class="sxs-lookup"><span data-stu-id="19cd6-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="19cd6-131">Для того, чтобы персонализовать инструкции можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="19cd6-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="19cd6-132">Заполнители заменяются соответствующей информацией, когда инструкции отображаются пользователям.</span><span class="sxs-lookup"><span data-stu-id="19cd6-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="19cd6-133">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="19cd6-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="19cd6-134">Щелкните в поле **Инструкции по отправке**, чтобы указать, где должен находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="19cd6-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="19cd6-135">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="19cd6-136">В открывшемся списке выберите заполнитель, который необходимо вставить.</span><span class="sxs-lookup"><span data-stu-id="19cd6-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="19cd6-137">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-137">Click **Insert**.</span></span>

4. <span data-ttu-id="19cd6-138">Для добавления переводов инструкций выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="19cd6-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="19cd6-139">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="19cd6-140">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="19cd6-141">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="19cd6-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="19cd6-142">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="19cd6-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="19cd6-143">Для того, чтобы персонализовать текст можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="19cd6-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="19cd6-144">Инструкции по вводу заполнителя см. на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="19cd6-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="19cd6-145">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a><span data-ttu-id="19cd6-146">Укажите, когда данный рабочей процесс используется в условиях активации</span><span class="sxs-lookup"><span data-stu-id="19cd6-146">Specify when this workflow is used through activation conditions</span></span>

<span data-ttu-id="19cd6-147">Можно создать несколько workflow-процессов на основе одного и того же типа рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="19cd6-147">You can create multiple workflows that are based on the same workflow type.</span></span> <span data-ttu-id="19cd6-148">Если в основе нескольких рабочих процессов лежит один и тот же тип, необходимо указать, когда следует использовать каждый рабочий процесс с помощью условий активации.</span><span class="sxs-lookup"><span data-stu-id="19cd6-148">When you have multiple workflows that are based on the same type, you must specify when each workflow is used using activation conditions.</span></span> <span data-ttu-id="19cd6-149">Если условия активации не выполняются, используется рабочий процесс по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19cd6-149">If activation conditions are not met, then the default workflow is used.</span></span> <span data-ttu-id="19cd6-150">Аналогично, если для типа рабочего процесса определена только одна конфигурация рабочего процесса, то эта конфигурация рабочего процесса будет использоваться независимо от условий активации.</span><span class="sxs-lookup"><span data-stu-id="19cd6-150">Similarly, if there is only one workflow configuration defined for a workflow type, then that workflow configuration will be used regardless of the activation conditions.</span></span>

<span data-ttu-id="19cd6-151">Например, пусть требуется создать рабочий процесс заявок на закупку для каждой страны или региона, в которых работает компания, (например, Заявки на закупку: Дания или Заявки на закупку: Испания) со следующими условиями.</span><span class="sxs-lookup"><span data-stu-id="19cd6-151">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain, with the following conditions:</span></span>

- <span data-ttu-id="19cd6-152">Заявки на закупку: Дания используется, когда страна (регион) = DK</span><span class="sxs-lookup"><span data-stu-id="19cd6-152">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="19cd6-153">Заявки на закупку: Испания используется, когда страна (регион) = ES</span><span class="sxs-lookup"><span data-stu-id="19cd6-153">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="19cd6-154">Чтобы указать, когда следует использовать настраиваемый workflow-процесс, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="19cd6-154">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="19cd6-155">В левой области щелкните **Активация**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-155">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="19cd6-156">Установите флажок **Установка условий для запуска этого workflow-процесса**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-156">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="19cd6-157">Щелкните **Добавить условие**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-157">Click **Add condition**.</span></span>
4. <span data-ttu-id="19cd6-158">Введите условие.</span><span class="sxs-lookup"><span data-stu-id="19cd6-158">Enter a condition.</span></span>
5. <span data-ttu-id="19cd6-159">Введите все необходимые дополнительные условия.</span><span class="sxs-lookup"><span data-stu-id="19cd6-159">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="19cd6-160">Чтобы убедиться, что введенные условия настроены верно, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="19cd6-160">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>

    1. <span data-ttu-id="19cd6-161">Щелкните **Тест**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-161">Click **Test**.</span></span>
    2. <span data-ttu-id="19cd6-162">На странице **Проверить условие workflow-процесса** в области **Проверить условие** выберите запись.</span><span class="sxs-lookup"><span data-stu-id="19cd6-162">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="19cd6-163">Щелкните **Тест**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-163">Click **Test**.</span></span> <span data-ttu-id="19cd6-164">Система оценит запись и определит, соответствует ли она определенным вами условиям.</span><span class="sxs-lookup"><span data-stu-id="19cd6-164">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="19cd6-165">Например, если вы создаете workflow-процесс заявки на покупку для Испании, в области **Проверка условия** страницы будет отображаться список заявок на покупку.</span><span class="sxs-lookup"><span data-stu-id="19cd6-165">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="19cd6-166">Если нажать кнопку **Тест**, система проверит выбранную заявку на покупку, чтобы определить, является ли страной/регионом ES.</span><span class="sxs-lookup"><span data-stu-id="19cd6-166">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4. <span data-ttu-id="19cd6-167">Нажмите кнопку **OK** или **Отмена** для возврата на страницу **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-167">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="19cd6-168">Задать условия отправки уведомлений</span><span class="sxs-lookup"><span data-stu-id="19cd6-168">Specify when notifications are sent</span></span>

<span data-ttu-id="19cd6-169">Когда документ представлен на обработку, создается экземпляр workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="19cd6-169">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="19cd6-170">При запуске, выполнении, завершении или отмене экземпляров workflow-процесса (созданных на основе данного workflow-процесса), а также при их остановке из-за ошибки пользователям могут быть отправлены уведомления.</span><span class="sxs-lookup"><span data-stu-id="19cd6-170">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="19cd6-171">Чтобы указать, когда следует отправлять уведомления, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="19cd6-171">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="19cd6-172">В левой области щелкните **Уведомления**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-172">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="19cd6-173">Установите флажок для каждого события, запускающего уведомления:</span><span class="sxs-lookup"><span data-stu-id="19cd6-173">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="19cd6-174">**Запущено** — отправка уведомлений при запуске экземпляра workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="19cd6-174">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="19cd6-175">**Остановлено** — уведомления будут отправляться, если экземпляр workflow-процесса остановлен из-за ошибки.</span><span class="sxs-lookup"><span data-stu-id="19cd6-175">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="19cd6-176">**Выполнено** — уведомления будут отправляться при выполнении экземпляра workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="19cd6-176">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="19cd6-177">**Неустранимо** — уведомления будут отправляться, если экземпляр workflow-процесса остановлен из-за неустранимой ошибки.</span><span class="sxs-lookup"><span data-stu-id="19cd6-177">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="19cd6-178">**Завершено** — уведомления будут отправляться при завершении экземпляра workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="19cd6-178">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="19cd6-179">Выберите строку для события, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="19cd6-179">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="19cd6-180">На вкладке **Текст уведомления** введите текст уведомления.</span><span class="sxs-lookup"><span data-stu-id="19cd6-180">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="19cd6-181">Для того, чтобы персонализовать текст можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="19cd6-181">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="19cd6-182">Заполнители заменяются соответствующей информацией, когда текст отображается пользователям.</span><span class="sxs-lookup"><span data-stu-id="19cd6-182">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="19cd6-183">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="19cd6-183">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="19cd6-184">Щелкните в поле ,чтобы указать, где должен находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="19cd6-184">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="19cd6-185">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-185">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="19cd6-186">В открывшемся списке выберите заполнитель, который необходимо вставить.</span><span class="sxs-lookup"><span data-stu-id="19cd6-186">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="19cd6-187">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-187">Click **Insert**.</span></span>
    5. <span data-ttu-id="19cd6-188">Общий заполнитель **Текст уведомления**, который необходимо включить, это "Последние замечания: %Workflow.Last note%", который отображает все комментарии из предыдущего шага.</span><span class="sxs-lookup"><span data-stu-id="19cd6-188">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="19cd6-189">Для добавления переводов текста выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="19cd6-189">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="19cd6-190">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-190">Click **Translations**.</span></span>
    2. <span data-ttu-id="19cd6-191">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-191">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="19cd6-192">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="19cd6-192">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="19cd6-193">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="19cd6-193">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="19cd6-194">Для того, чтобы персонализовать текст можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="19cd6-194">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="19cd6-195">Инструкции по вводу заполнителя см. на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="19cd6-195">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="19cd6-196">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-196">Click **Close**.</span></span>

7. <span data-ttu-id="19cd6-197">На вкладке **Получатель** используйте следующие параметры, чтобы указать, кто должен получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="19cd6-197">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="19cd6-198">Параметр</span><span class="sxs-lookup"><span data-stu-id="19cd6-198">Option</span></span></th>
    <th><span data-ttu-id="19cd6-199">Уведомления отправляются этим пользователям</span><span class="sxs-lookup"><span data-stu-id="19cd6-199">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="19cd6-200">Для отправки уведомлений выполните следующие действия</span><span class="sxs-lookup"><span data-stu-id="19cd6-200">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="19cd6-201">Участник</span><span class="sxs-lookup"><span data-stu-id="19cd6-201">Participant</span></span></td>
    <td><span data-ttu-id="19cd6-202">Пользователи, назначенные для конкретной группы или роли</span><span class="sxs-lookup"><span data-stu-id="19cd6-202">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="19cd6-203">На вкладке <strong>Получатель</strong> щелкните <strong>Участник</strong>.</span><span class="sxs-lookup"><span data-stu-id="19cd6-203">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="19cd6-204">На вкладке <strong>На основе роли</strong> в списке <strong>Тип участника</strong> выберите тип группы или роли, которой требуется отправить уведомления.</span><span class="sxs-lookup"><span data-stu-id="19cd6-204">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="19cd6-205">В списке <strong>Участник</strong> выберите группу или роль, которой нужно отправлять уведомления.</span><span class="sxs-lookup"><span data-stu-id="19cd6-205">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="19cd6-206">Пользователь workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="19cd6-206">Workflow user</span></span></td>
    <td><span data-ttu-id="19cd6-207">Пользователи-участники в этом workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="19cd6-207">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="19cd6-208">На вкладке <strong>Получатель</strong> щелкните <strong>Пользователь workflow-процесса</strong>.</span><span class="sxs-lookup"><span data-stu-id="19cd6-208">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="19cd6-209">На вкладке <strong>Пользователь workflow-процесса</strong> в списке <strong>Пользователь workflow-процесса</strong> выберите участника в этом workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="19cd6-209">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="19cd6-210">Пользователь</span><span class="sxs-lookup"><span data-stu-id="19cd6-210">User</span></span></td>
    <td><span data-ttu-id="19cd6-211">Определенные пользователи</span><span class="sxs-lookup"><span data-stu-id="19cd6-211">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="19cd6-212">На вкладке <strong>Получатель</strong> щелкните <strong>Пользователь</strong>.</span><span class="sxs-lookup"><span data-stu-id="19cd6-212">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="19cd6-213">На вкладке <strong>Пользователь</strong> список <strong>Доступные пользователи</strong> включает всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="19cd6-213">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="19cd6-214">Выберите пользователей, которым требуется отправить уведомления, а затем переместите этих пользователей в список <strong>Выбранные пользователи</strong>.</span><span class="sxs-lookup"><span data-stu-id="19cd6-214">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="19cd6-215">Повторите шаги 3–7 для каждого события, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="19cd6-215">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="19cd6-216">Ввод комментариев об изменениях, внесенных в workflow-процесс</span><span class="sxs-lookup"><span data-stu-id="19cd6-216">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="19cd6-217">Чтобы ввести комментарии об изменениях, внесенных в workflow-процесс, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="19cd6-217">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="19cd6-218">В левой области щелкните **Примечания**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-218">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="19cd6-219">В поле **Введите комментарии о workflow-процессе** введите комментарии.</span><span class="sxs-lookup"><span data-stu-id="19cd6-219">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="19cd6-220">Проверьте комментарии.</span><span class="sxs-lookup"><span data-stu-id="19cd6-220">Review your comments.</span></span> <span data-ttu-id="19cd6-221">После добавления комментариев их невозможно изменить.</span><span class="sxs-lookup"><span data-stu-id="19cd6-221">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="19cd6-222">Нажмите кнопку **Добавить** для добавления комментариев в область **История комментариев**.</span><span class="sxs-lookup"><span data-stu-id="19cd6-222">Click **Add** to add your comments to the **Comment history** area.</span></span>
