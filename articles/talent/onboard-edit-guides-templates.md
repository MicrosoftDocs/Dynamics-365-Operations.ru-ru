---
title: Редактирование руководств и шаблонов по адаптации в Dynamics 365 Talent - Onboard
description: В этой теме объясняется, как добавлять действия и другие сведения к руководства и шаблоны по адаптации в Microsoft Dynamics 365 Talent - Onboard.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 291f7aefac61c26dfab81cfff28c1c6580d46de5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462369"
---
# <a name="edit-onboarding-guides-and-templates"></a><span data-ttu-id="cdfce-103">Редактирование руководств и шаблонов по адаптации</span><span class="sxs-lookup"><span data-stu-id="cdfce-103">Edit onboarding guides and templates</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cdfce-104">После создания руководства или шаблона по адаптации в Microsoft Dynamics 365 Talent: Onboard необходимо добавить сведения о мероприятиях, контактах и ресурсах.</span><span class="sxs-lookup"><span data-stu-id="cdfce-104">After you create an onboarding guide or template in Microsoft Dynamics 365 Talent: Onboard, you must add an introduction, activities, contacts, and resources.</span></span> <span data-ttu-id="cdfce-105">В приложении Onboard в руководство по адаптации можно включить обширное содержимое, включая:</span><span class="sxs-lookup"><span data-stu-id="cdfce-105">Onboard lets you include rich content in your onboarding guides, including:</span></span>

- <span data-ttu-id="cdfce-106">Видео с YouTube</span><span class="sxs-lookup"><span data-stu-id="cdfce-106">YouTube videos</span></span>
- <span data-ttu-id="cdfce-107">Презентации Microsoft Sway</span><span class="sxs-lookup"><span data-stu-id="cdfce-107">Microsoft Sway presentations</span></span>
- <span data-ttu-id="cdfce-108">Приложения Microsoft PowerApps</span><span class="sxs-lookup"><span data-stu-id="cdfce-108">Microsoft PowerApps apps</span></span>
- <span data-ttu-id="cdfce-109">Видео Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="cdfce-109">Microsoft Stream videos</span></span>
- <span data-ttu-id="cdfce-110">Формы Microsoft Forms</span><span class="sxs-lookup"><span data-stu-id="cdfce-110">Microsoft Forms forms</span></span>
- <span data-ttu-id="cdfce-111">Фреймы Iframes, которые содержат веб-содержимое</span><span class="sxs-lookup"><span data-stu-id="cdfce-111">Iframes that contains web content</span></span>

## <a name="edit-introductions-or-activities-imported-from-a-template"></a><span data-ttu-id="cdfce-112">Изменение введений или действий, импортированных из шаблона</span><span class="sxs-lookup"><span data-stu-id="cdfce-112">Edit introductions or activities imported from a template</span></span>

<span data-ttu-id="cdfce-113">Если вы создаете руководство по адаптации из шаблона или импортируете мероприятия из одного шаблона в другой, вы увидите кнопку **Блокировать** на импортированных мероприятиях.</span><span class="sxs-lookup"><span data-stu-id="cdfce-113">If you create an onboarding guide from a template, or if you import activities from one template into another, you'll notice a **Lock** button on the imported activities.</span></span> <span data-ttu-id="cdfce-114">Они называются *управляемыми мероприятиями*.</span><span class="sxs-lookup"><span data-stu-id="cdfce-114">These are called *managed activities*.</span></span>

<span data-ttu-id="cdfce-115">[![Управляемые мероприятия](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span><span class="sxs-lookup"><span data-stu-id="cdfce-115">[![Managed activities](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span></span>

<span data-ttu-id="cdfce-116">При выборе управляемого мероприятия можно просмотреть исходный шаблон в верхней части мероприятия.</span><span class="sxs-lookup"><span data-stu-id="cdfce-116">When you select a managed activity, you can see the source template at the top of the activity.</span></span>

<span data-ttu-id="cdfce-117">[![Источник управляемого мероприятия](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span><span class="sxs-lookup"><span data-stu-id="cdfce-117">[![Managed activity source](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span></span>

<span data-ttu-id="cdfce-118">При редактировании действия в шаблоне Onboard передает изменения во все шаблоны и неотправленные руководства, которые основаны на этом шаблоне.</span><span class="sxs-lookup"><span data-stu-id="cdfce-118">If you edit an activity in a template, Onboard will push the changes to all templates and unsent guides that are based on that template.</span></span> <span data-ttu-id="cdfce-119">При выборе неотправленного руководства на основе измененного шаблона и последующем выборе вкладки **Мероприятия** в этом руководстве вы увидите уведомление об изменении руководства.</span><span class="sxs-lookup"><span data-stu-id="cdfce-119">If you select an unsent guide based on a template you edited and then select the **Activities** tab in the guide, you will see a notice that your guide has changed.</span></span> <span data-ttu-id="cdfce-120">Чтобы закрыть уведомление, выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cdfce-120">To dismiss the notification, select **OK**.</span></span> 

<span data-ttu-id="cdfce-121">[![Уведомление об изменении](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span><span class="sxs-lookup"><span data-stu-id="cdfce-121">[![Change notification](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span></span>

<span data-ttu-id="cdfce-122">Рядом с обновленными мероприятиями отображается черная точка.</span><span class="sxs-lookup"><span data-stu-id="cdfce-122">You'll see a black dot next to the updated activities.</span></span>

<span data-ttu-id="cdfce-123">[![Измененное мероприятие](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span><span class="sxs-lookup"><span data-stu-id="cdfce-123">[![Changed activity](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span></span>

<span data-ttu-id="cdfce-124">Нельзя изменять управляемые мероприятия вне исходного шаблона, за исключением добавления уполномоченного, срока выполнения или другой информации в правый раздел мероприятия.</span><span class="sxs-lookup"><span data-stu-id="cdfce-124">You can't edit managed activities outside of the original template, except to add an assignee, due date, or other information in the right-hand section of the activity.</span></span>

<span data-ttu-id="cdfce-125">Если необходимо изменить управляемое мероприятие или если не требуется, чтобы мероприятие получало обновления из шаблона, из которого оно было создано, установите для этого мероприятия кнопку **Блокировка**.</span><span class="sxs-lookup"><span data-stu-id="cdfce-125">If you want to edit a managed activity, or if you don't want an activity to receive updates from the template it came from, select the **Lock** button for that activity.</span></span> <span data-ttu-id="cdfce-126">Кнопка **Блокировка** исчезнет.</span><span class="sxs-lookup"><span data-stu-id="cdfce-126">The **Lock** button will disappear.</span></span> <span data-ttu-id="cdfce-127">Это мероприятие больше не будет управляться исходным шаблоном, и оно больше не будет получать обновления из этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="cdfce-127">The activity will no longer be managed by the original template, and it will no longer receive updates from that template.</span></span> <span data-ttu-id="cdfce-128">Обновления, вносимые в мероприятие, не влияют на исходный шаблон.</span><span class="sxs-lookup"><span data-stu-id="cdfce-128">Updates you make to an activity do not affect the original template.</span></span>

<span data-ttu-id="cdfce-129">Если удалить мероприятие из руководства и передать изменения из шаблона этого руководства, мероприятие остается удаленным в руководстве.</span><span class="sxs-lookup"><span data-stu-id="cdfce-129">If you delete an activity from a guide and push changes from that guide's template, the activity will remain deleted in the guide.</span></span>

> [!NOTE]
> <span data-ttu-id="cdfce-130">Контакты и ресурсы не управляются шаблонами.</span><span class="sxs-lookup"><span data-stu-id="cdfce-130">Contacts and resources aren't managed by templates.</span></span> <span data-ttu-id="cdfce-131">Кроме того, разделы не управляются, поэтому при добавлении или редактировании раздела в шаблоне эти изменения не будут переданы в какие-либо руководства или шаблоны, использующие этот шаблон.</span><span class="sxs-lookup"><span data-stu-id="cdfce-131">In addition, sections aren't managed, so if you add or edit a section in a template, the changes won't be pushed to any guides or templates that use that template.</span></span>
> 
> <span data-ttu-id="cdfce-132">Если к шаблону добавлены новые мероприятия, новые мероприятия передаются в руководства и шаблоны, основанные на этом шаблоне, и новые мероприятия отображаются вверху.</span><span class="sxs-lookup"><span data-stu-id="cdfce-132">If you add new activities to a template, the new activities are pushed to guides and templates based on that template, and the new activities display at the top.</span></span>

## <a name="import-activities-from-another-template"></a><span data-ttu-id="cdfce-133">Импорт мероприятий из другого шаблона</span><span class="sxs-lookup"><span data-stu-id="cdfce-133">Import activities from another template</span></span>

<span data-ttu-id="cdfce-134">Мероприятия из одного или нескольких шаблонов можно импортировать в руководство или шаблон.</span><span class="sxs-lookup"><span data-stu-id="cdfce-134">You can import activities from one or more templates into a guide or template.</span></span>

1. <span data-ttu-id="cdfce-135">Выберите руководство или шаблон, который хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="cdfce-135">Select the guide or template you want to edit.</span></span>

2. <span data-ttu-id="cdfce-136">Выберите вкладку **Мероприятия**.</span><span class="sxs-lookup"><span data-stu-id="cdfce-136">Select the **Activities** tab.</span></span>

3. <span data-ttu-id="cdfce-137">Выберите вкладку **Импорт** в разделе справа.</span><span class="sxs-lookup"><span data-stu-id="cdfce-137">Select the **Import** tab in the section on the right.</span></span>

   <span data-ttu-id="cdfce-138">[![Импорт мероприятий](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span><span class="sxs-lookup"><span data-stu-id="cdfce-138">[![Import activities](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span></span>

4. <span data-ttu-id="cdfce-139">Чтобы просмотреть задачи на новой вкладке в браузере, нажмите кнопку **Открыть в новой вкладке** в любом шаблоне.</span><span class="sxs-lookup"><span data-stu-id="cdfce-139">To preview the tasks in a new tab in your browser, select the **Open in new tab** button on any template.</span></span>

   <span data-ttu-id="cdfce-140">[![Импорт мероприятий](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span><span class="sxs-lookup"><span data-stu-id="cdfce-140">[![Import activities](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span></span>

5. <span data-ttu-id="cdfce-141">Перетащите нужный шаблон на место в шаблоне руководства, где должны отображаться мероприятия.</span><span class="sxs-lookup"><span data-stu-id="cdfce-141">Drag and drop the desired template to the place in your guide template where you want the activities to appear.</span></span> <span data-ttu-id="cdfce-142">Продолжите редактирование руководства или шаблона.</span><span class="sxs-lookup"><span data-stu-id="cdfce-142">Continue editing your guide or template.</span></span>

<span data-ttu-id="cdfce-143">Импортированные мероприятия будут содержать кнопку **Блокировка**, которая показывает, что эти мероприятия управляются шаблоном, из которого они импортированы.</span><span class="sxs-lookup"><span data-stu-id="cdfce-143">The imported activities will contain a **Lock** button, which indicates those activities are managed by the template you imported from.</span></span> <span data-ttu-id="cdfce-144">При внесении изменений в импортированный шаблон эти мероприятия будут обновлены в шаблоне, в который они были импортированы.</span><span class="sxs-lookup"><span data-stu-id="cdfce-144">When you make changes to the template you imported, those activities will update in the template you imported them to.</span></span> <span data-ttu-id="cdfce-145">Однако эти изменения не передаются автоматически в любые руководства, созданные из шаблона, в который был выполнен импорт.</span><span class="sxs-lookup"><span data-stu-id="cdfce-145">However, the changes will not be pushed automatically to any guides created from the template you imported to.</span></span>

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a><span data-ttu-id="cdfce-146">Принудительная передача изменений из шаблона в другие шаблоны или руководства</span><span class="sxs-lookup"><span data-stu-id="cdfce-146">Push changes from a template to other templates or guides</span></span>

<span data-ttu-id="cdfce-147">При редактировании шаблона, содержащего мероприятия, которые используются в других шаблонах или руководствах, необходимо передать изменения, если они должны отображаться в других шаблонах или руководствах.</span><span class="sxs-lookup"><span data-stu-id="cdfce-147">If you edit a template that contains activities that are used in other templates or guides, you must push the changes if you want them to appear in the other templates or guides.</span></span>

<span data-ttu-id="cdfce-148">Если нет уверенности в том, что мероприятия шаблона используются в других шаблонах или руководствах, выберите вкладку **Используется в**, чтобы просмотреть, где эти мероприятия появляются.</span><span class="sxs-lookup"><span data-stu-id="cdfce-148">If you're not sure whether your template's activities are used in other templates or guides, select the **Used in** tab to view where those activities appear.</span></span>

   <span data-ttu-id="cdfce-149">[![Просмотр руководств и шаблонов, в которых используются мероприятия](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span><span class="sxs-lookup"><span data-stu-id="cdfce-149">[![View guides and templates activities are used in](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span></span>

<span data-ttu-id="cdfce-150">Чтобы передать изменения:</span><span class="sxs-lookup"><span data-stu-id="cdfce-150">To push your changes:</span></span>

1. <span data-ttu-id="cdfce-151">Сохраните изменения, выбрав кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="cdfce-151">Save your changes by selecting the **Save** button.</span></span> <span data-ttu-id="cdfce-152">Если это не сделать, будет предложено сохранить изменения на следующем шаге.</span><span class="sxs-lookup"><span data-stu-id="cdfce-152">If you don't do this, you'll be prompted to save your changes in the next step.</span></span>

2. <span data-ttu-id="cdfce-153">Выберите **Отправить эти изменения**.</span><span class="sxs-lookup"><span data-stu-id="cdfce-153">Select **Push these changes**.</span></span>

   
## <a name="add-or-edit-an-introduction"></a><span data-ttu-id="cdfce-154">Добавление или изменение введения</span><span class="sxs-lookup"><span data-stu-id="cdfce-154">Add or edit an introduction</span></span>

1. <span data-ttu-id="cdfce-155">На вкладке **Введение** введите заголовок для руководства и открывающее сообщение.</span><span class="sxs-lookup"><span data-stu-id="cdfce-155">On the **Introduction** tab, enter a title for your guide and an opening message.</span></span> <span data-ttu-id="cdfce-156">Для использования образца текста выберите **Использовать это сообщение**.</span><span class="sxs-lookup"><span data-stu-id="cdfce-156">To use the sample text, select **Use this message**.</span></span>

    <span data-ttu-id="cdfce-157">[![Вкладка "Введение" в шаблоне Onboard](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="cdfce-157">[![Introduction tab in an Onboard template](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span></span>

2. <span data-ttu-id="cdfce-158">Кнопки форматирования используются для выделения текста требуемым образом, а также для добавления изображений или ссылок.</span><span class="sxs-lookup"><span data-stu-id="cdfce-158">Use the formatting buttons to call out text as you require, or to add images or links.</span></span>
3. <span data-ttu-id="cdfce-159">Выберите **Сохранить** для сохранения работы.</span><span class="sxs-lookup"><span data-stu-id="cdfce-159">Select **Save** to save your work.</span></span>

## <a name="add-or-edit-activities"></a><span data-ttu-id="cdfce-160">Добавление или редактирование мероприятий</span><span class="sxs-lookup"><span data-stu-id="cdfce-160">Add or edit activities</span></span>

1. <span data-ttu-id="cdfce-161">На вкладке **Мероприятия** перетащите элементы справа в область редактирования.</span><span class="sxs-lookup"><span data-stu-id="cdfce-161">On the **Activities** tab, drag items from the right to the editing area.</span></span>
2. <span data-ttu-id="cdfce-162">Для организации руководства в разделы перетащите элемент **Новый раздел** в область редактирования, затем введите имя и необязательное описание раздела.</span><span class="sxs-lookup"><span data-stu-id="cdfce-162">To organize your guide into sections, drag the **New section** item to the editing area, and enter a name and an optional description for the section.</span></span>

    ![[<span data-ttu-id="cdfce-163">Добавление нового раздела в руководство или шаблон по адаптации</span><span class="sxs-lookup"><span data-stu-id="cdfce-163">Adding a new section to an onboarding guide or template</span></span>](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. <span data-ttu-id="cdfce-164">Чтобы добавить мероприятия для завершения нового найма, перетащите элемент **Новое мероприятие** в область редактирования и введите имя и описание мероприятия.</span><span class="sxs-lookup"><span data-stu-id="cdfce-164">To add activities for your new hire to complete, drag the **New activity** item to the editing area, and enter a name and description for the activity.</span></span>

    ![[<span data-ttu-id="cdfce-165">Добавление нового мероприятия в руководство или шаблон по адаптации</span><span class="sxs-lookup"><span data-stu-id="cdfce-165">Adding a new activity to an onboarding guide or template</span></span>](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. <span data-ttu-id="cdfce-166">Добавление обширного содержимого в руководство по адаптации:</span><span class="sxs-lookup"><span data-stu-id="cdfce-166">Add rich content to your onboarding guide:</span></span>

    - <span data-ttu-id="cdfce-167">Чтобы добавить видеозапись YouTube, перетащите элемент **YouTube** в область редактирования, введите имя и описание мероприятия и введите URL-адрес для видео YouTube.</span><span class="sxs-lookup"><span data-stu-id="cdfce-167">To add a YouTube video, drag the **YouTube** item to the editing area, enter a name and description for the activity, and enter the URL for the YouTube video.</span></span>
    - <span data-ttu-id="cdfce-168">Чтобы добавить презентацию или информационный бюллетень Sway, перетащите элемент **Sway** в область редактирования, введите имя и описание мероприятия и введите внедренный URL-адрес для презентации или бюллетеня Sway.</span><span class="sxs-lookup"><span data-stu-id="cdfce-168">To add a Sway presentation or newsletter, drag the **Sway** item to the editing area, enter a name and description for the activity, and enter the embedded URL for the Sway presentation or newsletter.</span></span>
    - <span data-ttu-id="cdfce-169">Чтобы добавить приложение Microsoft Power Apps, перетащите элемент **Power Apps** в область редактирования, введите имя и описание мероприятия, а также выберите приложение Power Apps или введите идентификатор приложения Power Apps.</span><span class="sxs-lookup"><span data-stu-id="cdfce-169">To add a Microsoft Power Apps app, drag the **Power Apps** item to the editing area, enter a name and description for the activity, and either select the Power Apps app or enter the Power Apps app ID.</span></span>
    - <span data-ttu-id="cdfce-170">Чтобы добавить видеозапись Microsoft Stream, перетащите элемент **Microsoft Stream** в область редактирования, введите имя и описание мероприятия и введите URL-адрес для видео Microsoft Stream.</span><span class="sxs-lookup"><span data-stu-id="cdfce-170">To add a Microsoft Stream video, drag the **Microsoft Stream** item to the editing area, enter a name and description for the activity, and enter the URL for the Microsoft Stream video.</span></span>
    - <span data-ttu-id="cdfce-171">Чтобы добавить форму Microsoft Forms, перетащите элемент **Microsoft Forms** в область редактирования, введите имя и описание мероприятия, введите URL-адрес для формы Microsoft Forms и укажите размер области экрана.</span><span class="sxs-lookup"><span data-stu-id="cdfce-171">To add a Microsoft Forms form, drag the **Microsoft Forms** item to the editing area, enter a name and description for the activity, enter the URL for the Microsoft Forms form, and specify the size of the screen area.</span></span>
    - <span data-ttu-id="cdfce-172">Чтобы добавить фрейм iFrame, содержащий веб-содержимое, перетащите элемент **Веб-содержимое (iFrame)** в область редактирования, введите имя и описание мероприятия, введите URL-адрес для веб-содержимого и укажите размер области экрана.</span><span class="sxs-lookup"><span data-stu-id="cdfce-172">To add an iframe that contains web content, drag the **Web Content (iframe)** item to the editing area, enter a name and description for the activity, enter the URL for the web content, and specify the size of the screen area.</span></span>

    ![[<span data-ttu-id="cdfce-173">Добавление обширного содержимого в руководство или шаблон по адаптации</span><span class="sxs-lookup"><span data-stu-id="cdfce-173">Adding rich content to an onboarding guide or template</span></span>](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. <span data-ttu-id="cdfce-174">Необязательно: в области справа от каждого мероприятия назначьте мероприятие конкретному лицу или роли, добавьте срок выполнения и контактное лицо и назначьте цвет категории.</span><span class="sxs-lookup"><span data-stu-id="cdfce-174">Optional: In the area on the right of each activity, assign the activity to a specific person or role, add a due date and contact person, and assign a category color.</span></span> <span data-ttu-id="cdfce-175">При назначении мероприятия лицу или роли создается задача для каждого сотрудника.</span><span class="sxs-lookup"><span data-stu-id="cdfce-175">When you assign an activity to a person or role, a task is created for each individual.</span></span> <span data-ttu-id="cdfce-176">Эта задача появляется в меню **Задачи** в приложении Onboard.</span><span class="sxs-lookup"><span data-stu-id="cdfce-176">This task appears on the **Tasks** menu in Onboard.</span></span>

    <span data-ttu-id="cdfce-177">[![Назначение мероприятия в руководстве или шаблоне](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span><span class="sxs-lookup"><span data-stu-id="cdfce-177">[![Assigning an activity in an onboarding guide or template](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span></span>

3. <span data-ttu-id="cdfce-178">Выберите **Сохранить** для сохранения работы.</span><span class="sxs-lookup"><span data-stu-id="cdfce-178">Select **Save** to save your work.</span></span>

<span data-ttu-id="cdfce-179">Чтобы удалить мероприятие или раздел, выберите кнопку **Удалить** (символ корзины) в верхнем правом углу мероприятия или раздела.</span><span class="sxs-lookup"><span data-stu-id="cdfce-179">To delete an activity or section, select the **Delete** button (the trash can symbol) in the upper-right corner of the activity or section.</span></span>

<span data-ttu-id="cdfce-180">Чтобы изменить порядок мероприятий и разделов, перетащите их в новое местоположение.</span><span class="sxs-lookup"><span data-stu-id="cdfce-180">To rearrange activities and sections, drag them to a new location.</span></span>

## <a name="add-or-edit-contacts"></a><span data-ttu-id="cdfce-181">Добавление или изменение контактов</span><span class="sxs-lookup"><span data-stu-id="cdfce-181">Add or edit contacts</span></span>

<span data-ttu-id="cdfce-182">Вы можете добавить контактные лица, которые могут помочь новому сотруднику успешно начать работать с первого дня.</span><span class="sxs-lookup"><span data-stu-id="cdfce-182">You can add contact people who can help your new hire succeed from day one.</span></span> <span data-ttu-id="cdfce-183">Эти контакты могут быть специалистами по найму, коллегами, кураторами адаптации, наставниками, администраторами и специалистами службы ИТ-поддержки.</span><span class="sxs-lookup"><span data-stu-id="cdfce-183">These contacts can be recruiters, teammates, onboarding buddies, mentors, admins, and IT support staff.</span></span>

1. <span data-ttu-id="cdfce-184">На вкладке **Контакты** выберите **Создать контакт**.</span><span class="sxs-lookup"><span data-stu-id="cdfce-184">On the **Contacts** tab, select **New contact**.</span></span>
2. <span data-ttu-id="cdfce-185">В диалоговом окне **Добавить участника группы** введите имя или адрес электронной почты контактного лица, введите краткое описание, поясняющее, как контактное лицо может помочь новому сотруднику, затем выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="cdfce-185">In the **Add team member** dialog box, enter the contact person's name or email address, enter a short description that explains how the contact person can help the new hire, and then select **Add**.</span></span> 

    ![[<span data-ttu-id="cdfce-186">Добавление контактов в руководство или шаблон по адаптации</span><span class="sxs-lookup"><span data-stu-id="cdfce-186">Adding contacts to an onboarding guide or template</span></span>](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    <span data-ttu-id="cdfce-187">В качестве альтернативы можно выбрать один или несколько контактов в пункте **Предложения**.</span><span class="sxs-lookup"><span data-stu-id="cdfce-187">Alternately, you can select one or more contacts under **Suggestions**.</span></span>

3. <span data-ttu-id="cdfce-188">Выберите **Сохранить** для сохранения работы.</span><span class="sxs-lookup"><span data-stu-id="cdfce-188">Select **Save** to save your work.</span></span>

<span data-ttu-id="cdfce-189">Чтобы удалить контакт, выберите кнопку **Удалить** (символ корзины) справа от контакта.</span><span class="sxs-lookup"><span data-stu-id="cdfce-189">To delete a contact, select the **Delete** button (the trash can symbol) to the right of the contact.</span></span>

<span data-ttu-id="cdfce-190">Чтобы изменить контакт, выберите кнопку **Изменить** (символ карандаша) справа от контакта.</span><span class="sxs-lookup"><span data-stu-id="cdfce-190">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the contact.</span></span>

## <a name="add-or-edit-resources"></a><span data-ttu-id="cdfce-191">Добавление или изменение ресурсов</span><span class="sxs-lookup"><span data-stu-id="cdfce-191">Add or edit resources</span></span>

<span data-ttu-id="cdfce-192">В раздел **Ресурсы** руководства по адаптации можно добавлять полезные файлы, карты и ссылки.</span><span class="sxs-lookup"><span data-stu-id="cdfce-192">You can add useful files, maps, and links to the **Resources** section of your onboarding guide.</span></span>

1. <span data-ttu-id="cdfce-193">На вкладке **Ресурсы** выберите **Создать ресурс**.</span><span class="sxs-lookup"><span data-stu-id="cdfce-193">On the **Resources** tab, select **New resource**.</span></span>
2. <span data-ttu-id="cdfce-194">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="cdfce-194">Follow one of these steps:</span></span>

    - <span data-ttu-id="cdfce-195">Чтобы добавить файл, перейдите на вкладку **Файл** и перетащите файл в указанную область.</span><span class="sxs-lookup"><span data-stu-id="cdfce-195">To add a file, select the **File** tab, and drag the file into the designated area.</span></span> <span data-ttu-id="cdfce-196">(Можно также щелкнуть в любом месте в этой области, чтобы найти файл на компьютере, или нажать кнопку **Обзор OneDrive**.) Введите имя файла и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="cdfce-196">(Alternatively, click anywhere in that area to browse for the file on your computer, or select **Browse OneDrive**.) Enter a name for the file, and then select **Add**.</span></span>
    - <span data-ttu-id="cdfce-197">Чтобы добавить ссылку, выберите вкладку **Ссылка**, введите имя и адрес ссылки, затем выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="cdfce-197">To add a link, select the **Link** tab, enter a name and address for the link, and then select **Add**.</span></span>
    - <span data-ttu-id="cdfce-198">Чтобы добавить карту, выберите вкладку **Карта**, введите имя и адрес карты, затем выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="cdfce-198">To add a map, select the **Map** tab, enter a name and address for the map, and then select **Add**.</span></span> <span data-ttu-id="cdfce-199">Приложение Onboard включит карту для указанного вами адреса.</span><span class="sxs-lookup"><span data-stu-id="cdfce-199">Onboard will include a map of the address that you specify.</span></span>

    ![[<span data-ttu-id="cdfce-200">Добавление ресурса в руководство или шаблон по адаптации</span><span class="sxs-lookup"><span data-stu-id="cdfce-200">Adding a resource to an onboarding guide or template</span></span>](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. <span data-ttu-id="cdfce-201">Выберите **Сохранить** для сохранения работы.</span><span class="sxs-lookup"><span data-stu-id="cdfce-201">Select **Save** to save your work.</span></span>

<span data-ttu-id="cdfce-202">Чтобы удалить ресурс, выберите кнопку **Удалить** (символ корзины) справа от ресурса.</span><span class="sxs-lookup"><span data-stu-id="cdfce-202">To delete a resource, select the **Delete** button (the trash can symbol) to the right of the resource.</span></span>

<span data-ttu-id="cdfce-203">Чтобы изменить ресурс, выберите кнопку **Изменить** (символ карандаша) справа от ресурса.</span><span class="sxs-lookup"><span data-stu-id="cdfce-203">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the resource.</span></span>

## <a name="next-steps"></a><span data-ttu-id="cdfce-204">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="cdfce-204">Next steps</span></span>

- [<span data-ttu-id="cdfce-205">Предоставление общего доступа к содержимому другим участникам</span><span class="sxs-lookup"><span data-stu-id="cdfce-205">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="cdfce-206">Просмотр состояния задач и адаптируемых сотрудников</span><span class="sxs-lookup"><span data-stu-id="cdfce-206">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="cdfce-207">Создание групп комплектации штата в Onboard</span><span class="sxs-lookup"><span data-stu-id="cdfce-207">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="cdfce-208">См. также</span><span class="sxs-lookup"><span data-stu-id="cdfce-208">See also</span></span>

- [<span data-ttu-id="cdfce-209">Попробуйте или купите приложение Onboard</span><span class="sxs-lookup"><span data-stu-id="cdfce-209">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="cdfce-210">Что нового и что изменилось в Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="cdfce-210">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="cdfce-211">Планы выпуска</span><span class="sxs-lookup"><span data-stu-id="cdfce-211">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="cdfce-212">Получение поддержки по Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="cdfce-212">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
