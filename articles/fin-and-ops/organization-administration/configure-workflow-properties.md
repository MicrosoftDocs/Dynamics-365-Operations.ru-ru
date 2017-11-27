---
title: "Настроить свойства workflow-процесса"
description: "В этом разделе описывается, как настроить различные свойства workflow-процесса."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5c24f6555508272b65aeb81c5a16a0bd2407f1b4
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="configure-the-properties-of-a-workflow"></a><span data-ttu-id="a5472-103">Настроить свойства workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="a5472-103">Configure the properties of a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a5472-104">В этом разделе описывается, как настроить различные свойства workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="a5472-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="a5472-105">Чтобы настроить свойства workflow-процесса, откройте workflow-процесс в редакторе workflow-процессов.</span><span class="sxs-lookup"><span data-stu-id="a5472-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="a5472-106">Щелкните холст редактора workflow-процессов, а затем щелкните **Свойства**, чтобы открыть страницу **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="a5472-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="a5472-107">Можно использовать следующие процедуры для настройки различных свойств workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="a5472-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="a5472-108">Указать название документооборота</span><span class="sxs-lookup"><span data-stu-id="a5472-108">Name the workflow</span></span>
<span data-ttu-id="a5472-109">Чтобы ввести название workflow-процесса, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a5472-109">Follow these steps to enter a name for the workflow.</span></span>

1.  <span data-ttu-id="a5472-110">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="a5472-110">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="a5472-111">В поле **Имя** введите уникальное название документооборота.</span><span class="sxs-lookup"><span data-stu-id="a5472-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="a5472-112">Например, если требуется создать workflow-процесс заявки на покупку для каждой страны или региона, в которых работает компания, можно назвать workflow-процесс заявки на покупку **Заявки на покупку: Дания** или **Заявки на покупку: Испания**.</span><span class="sxs-lookup"><span data-stu-id="a5472-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="a5472-113">Указать владельца документооборота</span><span class="sxs-lookup"><span data-stu-id="a5472-113">Specify the workflow owner</span></span>
<span data-ttu-id="a5472-114">Владелец workflow-процесса — это лицо, которое будет управлять данным workflow-процесс и вести его.</span><span class="sxs-lookup"><span data-stu-id="a5472-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="a5472-115">Чтобы указать владельца workflow-процесса, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a5472-115">Follow these steps to specify the workflow owner.</span></span>

1.  <span data-ttu-id="a5472-116">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="a5472-116">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="a5472-117">Из списка **Владелец** выберите имя сотрудника, который будет управлять workflow-процессом.</span><span class="sxs-lookup"><span data-stu-id="a5472-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="a5472-118">Выберите шаблон электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a5472-118">Select an email template</span></span>
<span data-ttu-id="a5472-119">Выполните следующие шаги для выбора шаблона электронной почты, который будет использоваться для создания уведомлений о workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="a5472-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1.  <span data-ttu-id="a5472-120">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="a5472-120">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="a5472-121">В списке **Шаблон электронной почты для уведомлений workflow-процесса** выберите шаблон.</span><span class="sxs-lookup"><span data-stu-id="a5472-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="a5472-122">Ввести инструкции для пользователей</span><span class="sxs-lookup"><span data-stu-id="a5472-122">Enter instructions for users</span></span>
<span data-ttu-id="a5472-123">Можно добавить инструкции для пользователей, представляющих документы на обработку и утверждения.</span><span class="sxs-lookup"><span data-stu-id="a5472-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="a5472-124">Эти пользователи также называются *инициаторами*.</span><span class="sxs-lookup"><span data-stu-id="a5472-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="a5472-125">Например, вы создаете workflow-процесс заявки на покупку и вводите инструкции.</span><span class="sxs-lookup"><span data-stu-id="a5472-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="a5472-126">Эти инструкции смогут просматривать пользователи, которые вводят заявки на покупку на странице **Заявки на покупку**.</span><span class="sxs-lookup"><span data-stu-id="a5472-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="a5472-127">Исходный пользователь может щелкнуть значок в строке сообщений workflow-процесса, чтобы просмотреть инструкции.</span><span class="sxs-lookup"><span data-stu-id="a5472-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="a5472-128">Чтобы ввести инструкции для пользователей, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a5472-128">Follow these steps to enter instructions for users.</span></span>

1.  <span data-ttu-id="a5472-129">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="a5472-129">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="a5472-130">В поле **Инструкции по отправке** введите инструкции.</span><span class="sxs-lookup"><span data-stu-id="a5472-130">In the **Submission instructions** field, enter the instructions.</span></span>
3.  <span data-ttu-id="a5472-131">Для того, чтобы персонализовать инструкции можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="a5472-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="a5472-132">Заполнители заменяются соответствующей информацией, когда инструкции отображаются пользователям.</span><span class="sxs-lookup"><span data-stu-id="a5472-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="a5472-133">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="a5472-133">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="a5472-134">Щелкните в поле **Инструкции по отправке**, чтобы указать, где должен находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="a5472-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="a5472-135">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="a5472-135">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="a5472-136">В открывшемся списке выберите заполнитель, который необходимо вставить.</span><span class="sxs-lookup"><span data-stu-id="a5472-136">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="a5472-137">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="a5472-137">Click **Insert**.</span></span>

4.  <span data-ttu-id="a5472-138">Для добавления переводов инструкций выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a5472-138">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="a5472-139">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="a5472-139">Click **Translations**.</span></span>
    2.  <span data-ttu-id="a5472-140">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="a5472-140">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="a5472-141">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="a5472-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="a5472-142">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="a5472-142">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="a5472-143">Для того, чтобы персонализовать текст можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="a5472-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="a5472-144">Инструкции по вводу заполнителя см. на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="a5472-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6.  <span data-ttu-id="a5472-145">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="a5472-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used"></a><span data-ttu-id="a5472-146">Указать, когда данный workflow-процесс используется</span><span class="sxs-lookup"><span data-stu-id="a5472-146">Specify when this workflow is used</span></span>
<span data-ttu-id="a5472-147">Можно создать несколько workflow-процессов на основе одного и того же типа.</span><span class="sxs-lookup"><span data-stu-id="a5472-147">You can create multiple workflows that are based on the same type.</span></span> <span data-ttu-id="a5472-148">Например, вы создаете workflow-процесс заявки на покупку для каждой страны или региона, в которых работает компания, например "Заявки на покупку: Дания" и "Заявки на покупку: Испания".</span><span class="sxs-lookup"><span data-stu-id="a5472-148">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain.</span></span> <span data-ttu-id="a5472-149">Если в основе нескольких workflow-процессов лежит один и тот же тип, необходимо указать, когда следует использовать каждое workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="a5472-149">When you have multiple workflows that are based on the same type, you must specify when each workflow is used.</span></span> <span data-ttu-id="a5472-150">В приведенном выше примере вы указали следующие условия:</span><span class="sxs-lookup"><span data-stu-id="a5472-150">For the preceding example, you specify the following conditions:</span></span>

-   <span data-ttu-id="a5472-151">Заявки на закупку: Дания используется, когда страна (регион) = DK</span><span class="sxs-lookup"><span data-stu-id="a5472-151">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
-   <span data-ttu-id="a5472-152">Заявки на закупку: Испания используется, когда страна (регион) = ES</span><span class="sxs-lookup"><span data-stu-id="a5472-152">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="a5472-153">Чтобы указать, когда следует использовать настраиваемый workflow-процесс, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a5472-153">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1.  <span data-ttu-id="a5472-154">В левой области щелкните **Активация**.</span><span class="sxs-lookup"><span data-stu-id="a5472-154">In the left pane, click **Activation**.</span></span>
2.  <span data-ttu-id="a5472-155">Установите флажок **Установка условий для запуска этого workflow-процесса**.</span><span class="sxs-lookup"><span data-stu-id="a5472-155">Select the **Set the conditions for running this workflow** check box.</span></span>
3.  <span data-ttu-id="a5472-156">Щелкните **Добавить условие**.</span><span class="sxs-lookup"><span data-stu-id="a5472-156">Click **Add condition**.</span></span>
4.  <span data-ttu-id="a5472-157">Введите условие.</span><span class="sxs-lookup"><span data-stu-id="a5472-157">Enter a condition.</span></span>
5.  <span data-ttu-id="a5472-158">Введите все необходимые дополнительные условия.</span><span class="sxs-lookup"><span data-stu-id="a5472-158">Enter any additional conditions that are required.</span></span>
6.  <span data-ttu-id="a5472-159">Чтобы убедиться, что введенные условия настроены верно, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a5472-159">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>
    1.  <span data-ttu-id="a5472-160">Щелкните **Тест**.</span><span class="sxs-lookup"><span data-stu-id="a5472-160">Click **Test**.</span></span>
    2.  <span data-ttu-id="a5472-161">На странице **Проверить условие workflow-процесса** в области **Проверить условие** выберите запись.</span><span class="sxs-lookup"><span data-stu-id="a5472-161">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3.  <span data-ttu-id="a5472-162">Щелкните **Тест**.</span><span class="sxs-lookup"><span data-stu-id="a5472-162">Click **Test**.</span></span> <span data-ttu-id="a5472-163">Система оценит запись и определит, соответствует ли она определенным вами условиям.</span><span class="sxs-lookup"><span data-stu-id="a5472-163">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="a5472-164">Например, если вы создаете workflow-процесс заявки на покупку для Испании, в области **Проверка условия** страницы будет отображаться список заявок на покупку.</span><span class="sxs-lookup"><span data-stu-id="a5472-164">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="a5472-165">Если нажать кнопку **Тест**, система проверит выбранную заявку на покупку, чтобы определить, является ли страной/регионом ES.</span><span class="sxs-lookup"><span data-stu-id="a5472-165">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4.  <span data-ttu-id="a5472-166">Нажмите кнопку **OK** или **Отмена** для возврата на страницу **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="a5472-166">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="a5472-167">Задать условия отправки уведомлений</span><span class="sxs-lookup"><span data-stu-id="a5472-167">Specify when notifications are sent</span></span>
<span data-ttu-id="a5472-168">Когда документ представлен на обработку, создается экземпляр workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="a5472-168">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="a5472-169">При запуске, выполнении, завершении или отмене экземпляров workflow-процесса (созданных на основе данного workflow-процесса), а также при их остановке из-за ошибки пользователям могут быть отправлены уведомления.</span><span class="sxs-lookup"><span data-stu-id="a5472-169">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="a5472-170">Чтобы указать, когда следует отправлять уведомления, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a5472-170">Follow these steps to specify when notifications are sent.</span></span>

1.  <span data-ttu-id="a5472-171">В левой области щелкните **Уведомления**.</span><span class="sxs-lookup"><span data-stu-id="a5472-171">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="a5472-172">Установите флажок для каждого события, запускающего уведомления:</span><span class="sxs-lookup"><span data-stu-id="a5472-172">Select the check box for each event that should trigger notifications:</span></span>
    -   <span data-ttu-id="a5472-173">**Запущено** — отправка уведомлений при запуске экземпляра workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="a5472-173">**Started** – Send notifications when a workflow instance is started.</span></span>
    -   <span data-ttu-id="a5472-174">**Остановлено** — уведомления будут отправляться, если экземпляр workflow-процесса остановлен из-за ошибки.</span><span class="sxs-lookup"><span data-stu-id="a5472-174">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    -   <span data-ttu-id="a5472-175">**Выполнено** — уведомления будут отправляться при выполнении экземпляра workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="a5472-175">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    -   <span data-ttu-id="a5472-176">**Неустранимо** — уведомления будут отправляться, если экземпляр workflow-процесса остановлен из-за неустранимой ошибки.</span><span class="sxs-lookup"><span data-stu-id="a5472-176">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    -   <span data-ttu-id="a5472-177">**Завершено** — уведомления будут отправляться при завершении экземпляра workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="a5472-177">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3.  <span data-ttu-id="a5472-178">Выберите строку для события, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="a5472-178">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="a5472-179">На вкладке **Текст уведомления** введите текст уведомления.</span><span class="sxs-lookup"><span data-stu-id="a5472-179">On the **Notification text** tab, enter the text of the notification.</span></span>
5.  <span data-ttu-id="a5472-180">Для того, чтобы персонализовать текст можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="a5472-180">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="a5472-181">Заполнители заменяются соответствующей информацией, когда текст отображается пользователям.</span><span class="sxs-lookup"><span data-stu-id="a5472-181">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="a5472-182">Выполните следующие действия, чтобы вставить заполнитель:</span><span class="sxs-lookup"><span data-stu-id="a5472-182">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="a5472-183">Щелкните в поле ,чтобы указать, где должен находиться заполнитель.</span><span class="sxs-lookup"><span data-stu-id="a5472-183">Click in the field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="a5472-184">Щелкните **Вставить заполнитель**.</span><span class="sxs-lookup"><span data-stu-id="a5472-184">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="a5472-185">В открывшемся списке выберите заполнитель, который необходимо вставить.</span><span class="sxs-lookup"><span data-stu-id="a5472-185">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="a5472-186">Нажмите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="a5472-186">Click **Insert**.</span></span>

6.  <span data-ttu-id="a5472-187">Для добавления переводов текста выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a5472-187">To add translations of the text, follow these steps:</span></span>
    1.  <span data-ttu-id="a5472-188">Щелкните **Переводы**.</span><span class="sxs-lookup"><span data-stu-id="a5472-188">Click **Translations**.</span></span>
    2.  <span data-ttu-id="a5472-189">На открывшейся странице щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="a5472-189">On the page that appears, Click **Add**.</span></span>
    3.  <span data-ttu-id="a5472-190">В отображаемом списке выберите язык, на котором будет вводиться текст.</span><span class="sxs-lookup"><span data-stu-id="a5472-190">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="a5472-191">В поле **Переведенный текст** введите текст.</span><span class="sxs-lookup"><span data-stu-id="a5472-191">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="a5472-192">Для того, чтобы персонализовать текст можно вставить заполнители.</span><span class="sxs-lookup"><span data-stu-id="a5472-192">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="a5472-193">Инструкции по вводу заполнителя см. на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="a5472-193">For instructions about how to enter a placeholder, see step 5.</span></span>
    6.  <span data-ttu-id="a5472-194">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="a5472-194">Click **Close**.</span></span>

7.  <span data-ttu-id="a5472-195">На вкладке **Получатель** используйте следующие параметры, чтобы указать, кто должен получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="a5472-195">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="a5472-196">Параметр</span><span class="sxs-lookup"><span data-stu-id="a5472-196">Option</span></span></th>
    <th><span data-ttu-id="a5472-197">Уведомления отправляются этим пользователям</span><span class="sxs-lookup"><span data-stu-id="a5472-197">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="a5472-198">Для отправки уведомлений выполните следующие действия</span><span class="sxs-lookup"><span data-stu-id="a5472-198">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="a5472-199">Участник</span><span class="sxs-lookup"><span data-stu-id="a5472-199">Participant</span></span></td>
    <td><span data-ttu-id="a5472-200">Пользователи, назначенные для конкретной группы или роли</span><span class="sxs-lookup"><span data-stu-id="a5472-200">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="a5472-201">На вкладке <strong>Получатель</strong> щелкните <strong>Участник</strong>.</span><span class="sxs-lookup"><span data-stu-id="a5472-201">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="a5472-202">На вкладке <strong>На основе роли</strong> в списке <strong>Тип участника</strong> выберите тип группы или роли, которой требуется отправить уведомления.</span><span class="sxs-lookup"><span data-stu-id="a5472-202">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="a5472-203">В списке <strong>Участник</strong> выберите группу или роль, которой нужно отправлять уведомления.</span><span class="sxs-lookup"><span data-stu-id="a5472-203">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="a5472-204">Пользователь workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="a5472-204">Workflow user</span></span></td>
    <td><span data-ttu-id="a5472-205">Пользователи-участники в этом workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="a5472-205">Users who are participants in this workflow</span></span></td>
    <td><ol>
    <li><span data-ttu-id="a5472-206">На вкладке <strong>Получатель</strong> щелкните <strong>Пользователь workflow-процесса</strong>.</span><span class="sxs-lookup"><span data-stu-id="a5472-206">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="a5472-207">На вкладке <strong>Пользователь workflow-процесса</strong> в списке <strong>Пользователь workflow-процесса</strong> выберите участника в этом workflow-процессе.</span><span class="sxs-lookup"><span data-stu-id="a5472-207">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="a5472-208">Пользователь</span><span class="sxs-lookup"><span data-stu-id="a5472-208">User</span></span></td>
    <td><span data-ttu-id="a5472-209">Определенные пользователи Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a5472-209">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="a5472-210">На вкладке <strong>Получатель</strong> щелкните <strong>Пользователь</strong>.</span><span class="sxs-lookup"><span data-stu-id="a5472-210">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="a5472-211">На вкладке <strong>Пользователь</strong> список <strong>Доступные пользователи</strong> включает всех пользователей Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a5472-211">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="a5472-212">Выберите пользователей, которым требуется отправить уведомления, а затем переместите этих пользователей в список <strong>Выбранные пользователи</strong>.</span><span class="sxs-lookup"><span data-stu-id="a5472-212">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="a5472-213">Повторите шаги 3–7 для каждого события, выбранного на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="a5472-213">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="a5472-214">Ввод комментариев об изменениях, внесенных в workflow-процесс</span><span class="sxs-lookup"><span data-stu-id="a5472-214">Enter comments about the changes that you made to the workflow</span></span>
<span data-ttu-id="a5472-215">Чтобы ввести комментарии об изменениях, внесенных в workflow-процесс, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a5472-215">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1.  <span data-ttu-id="a5472-216">В левой области щелкните **Примечания**.</span><span class="sxs-lookup"><span data-stu-id="a5472-216">In the left pane, click **Notes**.</span></span>
2.  <span data-ttu-id="a5472-217">В поле **Введите комментарии о workflow-процессе** введите комментарии.</span><span class="sxs-lookup"><span data-stu-id="a5472-217">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3.  <span data-ttu-id="a5472-218">Проверьте комментарии.</span><span class="sxs-lookup"><span data-stu-id="a5472-218">Review your comments.</span></span> <span data-ttu-id="a5472-219">После добавления комментариев их невозможно изменить.</span><span class="sxs-lookup"><span data-stu-id="a5472-219">After you add comments, you can't modify them.</span></span>
4.  <span data-ttu-id="a5472-220">Нажмите кнопку **Добавить** для добавления комментариев в область **История комментариев**.</span><span class="sxs-lookup"><span data-stu-id="a5472-220">Click **Add** to add your comments to the **Comment history** area.</span></span>





