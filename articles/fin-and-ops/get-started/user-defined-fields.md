---
title: Создание настраиваемых полей и работа с ними
description: В этом разделе показано, как Microsoft Dynamics 365 for Finance and Operations позволяет некоторым пользователям создавать настраиваемые поля для настройки приложения в соответствии с их бизнесом.
author: jasongre
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 18402579789c17de7b46dd7a013b3b6327ea5d4f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561768"
---
# <a name="create-and-work-with-custom-fields"></a><span data-ttu-id="dea10-103">Создание настраиваемых полей и работа с ними</span><span class="sxs-lookup"><span data-stu-id="dea10-103">Create and work with custom fields</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dea10-104">В то время как Microsoft Dynamics 365 for Finance and Operations предоставляет обширный набор готовых полей для управления широким диапазоном бизнес-процессов, иногда компании требуется отслеживать дополнительную информацию в системе.</span><span class="sxs-lookup"><span data-stu-id="dea10-104">While Microsoft Dynamics 365 for Finance and Operations provides an extensive set of fields out-of-the-box for managing a broad range of business processes, sometimes there is a need for a company to track additional information in the system.</span></span> <span data-ttu-id="dea10-105">Чтобы удовлетворить эту потребность, Finance and Operations позволяет создавать пользовательские поля для настройки приложения в соответствии с вашим бизнесом, если у вас имеются разрешения на доступ к этой функции.</span><span class="sxs-lookup"><span data-stu-id="dea10-105">To accommodate this need, Finance and Operations allows you to create custom fields to tailor the application to fit your business, provided you have permissions to the feature.</span></span>

<span data-ttu-id="dea10-106">Возможность добавления настраиваемых полей доступна в обновлении платформы 13 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="dea10-106">The ability to add custom fields is available in platform update 13 and later.</span></span>

<span data-ttu-id="dea10-107">Это видео показывает, насколько просто можно добавить настраиваемое поле на страницу: [Добавление настраиваемых полей в Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span><span class="sxs-lookup"><span data-stu-id="dea10-107">This video shows how easy it is to add a custom field to a page: [Adding custom fields in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span></span>

## <a name="creating-custom-fields"></a><span data-ttu-id="dea10-108">Создание пользовательских полей</span><span class="sxs-lookup"><span data-stu-id="dea10-108">Creating custom fields</span></span>

<span data-ttu-id="dea10-109">Определив дополнительную информацию, которую вы хотите отслеживать в приложении, можно создать настраиваемое поле в соответствующей таблице и отобразить это новое поле на странице.</span><span class="sxs-lookup"><span data-stu-id="dea10-109">After you've identified additional information that you would like to track in the application, you can create the custom field on the appropriate table and expose that new field on a page.</span></span>

<span data-ttu-id="dea10-110">Следующие шаги описывают процесс создания настраиваемого поля и размещения этого поля в форме.</span><span class="sxs-lookup"><span data-stu-id="dea10-110">The following steps describe the process for creating a custom field and placing that field on a form.</span></span>

1. <span data-ttu-id="dea10-111">Перейдите в форму, в которой требуется новое поле.</span><span class="sxs-lookup"><span data-stu-id="dea10-111">Navigate to the form where the new field is needed.</span></span>
2. <span data-ttu-id="dea10-112">Поскольку конечной целью является размещение настраиваемого поля в форме, точка входа для создания настраиваемых полей существует внутри персонализации.</span><span class="sxs-lookup"><span data-stu-id="dea10-112">Because the end goal is to expose the custom field on a form, the entry point for creating custom fields exists inside the personalization experience.</span></span> <span data-ttu-id="dea10-113">Откройте панель инструментов персонализации, выбрав **Параметры**, а затем **Персонализировать эту форму**.</span><span class="sxs-lookup"><span data-stu-id="dea10-113">Open the personalization toolbar by selecting **Options**, and then **Personalize this form**.</span></span>
3. <span data-ttu-id="dea10-114">Щелкните **Вставить** и затем **Поле**.</span><span class="sxs-lookup"><span data-stu-id="dea10-114">Click **Insert** and then **Field**.</span></span>
4. <span data-ttu-id="dea10-115">Выберите область формы, в которой требуется разместить новое поле.</span><span class="sxs-lookup"><span data-stu-id="dea10-115">Select the region of the form where you want to expose the new field.</span></span> <span data-ttu-id="dea10-116">После выбора в диалоговом окне **Вставка полей** будет выведен список имеющихся полей, которые могут быть вставлены в выбранной области формы.</span><span class="sxs-lookup"><span data-stu-id="dea10-116">After selection, the **Insert fields** dialog box will display a list of existing fields that can be inserted into the selected region of the form.</span></span>
5. <span data-ttu-id="dea10-117">Убедитесь, что поле, которое вам требуется, отсутствует в списке.</span><span class="sxs-lookup"><span data-stu-id="dea10-117">Ensure that the field you are interested in does not already exist in the list.</span></span> <span data-ttu-id="dea10-118">Если оно присутствует, можно просто выбрать поле в списке и нажать кнопку **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="dea10-118">If it does, you can simply select that field in the list and click **Insert**.</span></span>
6. <span data-ttu-id="dea10-119">Нажмите кнопку **Создать новое поле** над списком, чтобы инициировать процесс создания настраиваемого поля.</span><span class="sxs-lookup"><span data-stu-id="dea10-119">Click the **Create new field** button above the list to initiate the process of creating a custom field.</span></span> <span data-ttu-id="dea10-120">При этом откроется диалоговое окно **Создать новое поле**.</span><span class="sxs-lookup"><span data-stu-id="dea10-120">This will open the **Create new field** dialog box.</span></span>

    <span data-ttu-id="dea10-121">Если вы не видите кнопку **Создать новое поле**, у вас нет необходимых разрешений для использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="dea10-121">If you do not see the **Create new field** button, you do not have the necessary permissions to use this feature.</span></span>

7. <span data-ttu-id="dea10-122">В диалоговом окне **Создать новое поле** укажите следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="dea10-122">In the **Create new field** dialog box, enter the following information.</span></span>

    1. <span data-ttu-id="dea10-123">Выберите таблицу базы данных, в которую необходимо добавить это поле.</span><span class="sxs-lookup"><span data-stu-id="dea10-123">Select the database table where this field should be added.</span></span> <span data-ttu-id="dea10-124">Обратите внимание, что только те таблицы, которые поддерживают настраиваемые поля, будут отображаться в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="dea10-124">Note that only tables that support custom fields will appear in the drop-down list.</span></span> <span data-ttu-id="dea10-125">Технические сведения о поддерживаемых таблицах см. в приведенном ниже разделе.</span><span class="sxs-lookup"><span data-stu-id="dea10-125">See the section below for technical details on supported tables.</span></span>
    2. <span data-ttu-id="dea10-126">Выберите тип данных для нового поля.</span><span class="sxs-lookup"><span data-stu-id="dea10-126">Select the data type for the new field.</span></span> <span data-ttu-id="dea10-127">Доступные типы данных: флажок, дата, дата и время, десятичное число, число, список выбора и текст.</span><span class="sxs-lookup"><span data-stu-id="dea10-127">The available data types are checkbox, date, date time, decimal, number, picklist, and text.</span></span>

        - <span data-ttu-id="dea10-128">Если выбран текстовый тип данных, можно также указать максимальную длину текста, который можно ввести в это поле.</span><span class="sxs-lookup"><span data-stu-id="dea10-128">If you choose the text data type, you can also specify the maximum length of the text that can be entered in this field.</span></span>
        - <span data-ttu-id="dea10-129">Если выбран тип данных "Список выбора", можно также выбрать набор допустимых значений для поля.</span><span class="sxs-lookup"><span data-stu-id="dea10-129">If you choose the picklist data type, you can also select the set of valid values for the field.</span></span>

    3. <span data-ttu-id="dea10-130">Укажите имя, метку и текст справки для поля.</span><span class="sxs-lookup"><span data-stu-id="dea10-130">Provide a name, label, and help text for the field.</span></span> <span data-ttu-id="dea10-131">Имя соответствует физическому имени поля в базе данных, тогда как метка и текст справки представляют собой текст, используемый для представления этого поля в интерфейсе пользователя.</span><span class="sxs-lookup"><span data-stu-id="dea10-131">The name corresponds to the physical field name in the database, whereas the label and help text are the text used to represent this field in the user interface.</span></span>

8. <span data-ttu-id="dea10-132">Если это единственное поле, которое требуется создать для этой формы, нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="dea10-132">If this is the only field that you need to create for this form, click **Save**.</span></span> <span data-ttu-id="dea10-133">Если необходимо создать дополнительные поля, щелкните **Сохранить и создать** и вернитесь к шагу 7.</span><span class="sxs-lookup"><span data-stu-id="dea10-133">If you need to create additional fields, click **Save and new** and go back to step 7.</span></span> <span data-ttu-id="dea10-134">Обратите внимание, что в настоящее время имеется ограничение в **20 настраиваемых полей на таблицу**.</span><span class="sxs-lookup"><span data-stu-id="dea10-134">Note that there is currently a limit of **20 custom fields per table**.</span></span>
9. <span data-ttu-id="dea10-135">При закрытии диалогового окна **Создать новое поле** производится возврат в диалоговое окно **Вставка полей**.</span><span class="sxs-lookup"><span data-stu-id="dea10-135">Leaving the **Create new field** dialog box will return you to the **Insert fields** dialog box.</span></span> <span data-ttu-id="dea10-136">Все пользовательские поля, которые только что были добавлены, автоматически помечаются в списке полей для вставки в форму.</span><span class="sxs-lookup"><span data-stu-id="dea10-136">Any custom fields that were just added will be automatically marked in the field list to be inserted into the form.</span></span>
10. <span data-ttu-id="dea10-137">Щелкните **Вставить** для вставки отмеченных полей в выбранную область формы.</span><span class="sxs-lookup"><span data-stu-id="dea10-137">Click **Insert** to insert the marked fields into the selected region of the form.</span></span>
11. <span data-ttu-id="dea10-138">**Необязательно:** включите режим **Перемещение** на панели инструментов персонализации, чтобы переместить новые поля в нужное место в выбранной области.</span><span class="sxs-lookup"><span data-stu-id="dea10-138">**Optional:** Enable **Move** mode from the personalization toolbar to move the new fields to their desired location in the selected region.</span></span> <span data-ttu-id="dea10-139">Дополнительные сведения о том, как использовать различные возможности персонализации для оптимизации формы для личного использования см. в разделе [Персонализация пользовательского интерфейса](personalize-user-experience.md).</span><span class="sxs-lookup"><span data-stu-id="dea10-139">See [Personalize the user experience](personalize-user-experience.md) for more information about how to use the various personalization capabilities to optimize a form for your personal usage.</span></span>

## <a name="sharing-custom-fields-with-other-users"></a><span data-ttu-id="dea10-140">Совместное использование настраиваемых полей с другими пользователями</span><span class="sxs-lookup"><span data-stu-id="dea10-140">Sharing custom fields with other users</span></span>

<span data-ttu-id="dea10-141">После создания настраиваемого поля и размещении его в форме может потребоваться предоставить это обновленное представление страницы, содержащее новое поле, другим пользователям в системе.</span><span class="sxs-lookup"><span data-stu-id="dea10-141">After you have created a custom field and exposed it on a form, you might want to provide this updated page view that includes the new field to other users in the system.</span></span> <span data-ttu-id="dea10-142">Это можно сделать двумя разными способами с помощью функций персонализации продукта:</span><span class="sxs-lookup"><span data-stu-id="dea10-142">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="dea10-143">Рекомендуется делать это через системного администратора, который может принудительно отправлять персонализации всеми пользователями или части пользователей.</span><span class="sxs-lookup"><span data-stu-id="dea10-143">The recommended route is through the system administrator, who can push a personalization to all users or a subset of users.</span></span> <span data-ttu-id="dea10-144">Подробнее см. в разделе [Персонализация работы пользователей](personalize-user-experience.md).</span><span class="sxs-lookup"><span data-stu-id="dea10-144">See [Personalize the user experience](personalize-user-experience.md) for more details.</span></span>
- <span data-ttu-id="dea10-145">Кроме того, можно экспортировать изменения (называемые *персонализациями*), отправить их одному или нескольким пользователям, и каждый из этих пользователей может импортировать изменения.</span><span class="sxs-lookup"><span data-stu-id="dea10-145">Alternatively, you can export your changes (called *personalizations*), send them to one or more users, and have each of those users import your changes.</span></span> <span data-ttu-id="dea10-146">Параметр **Управление** на панели инструментов персонализации позволяет экспортировать и импортировать персонализации.</span><span class="sxs-lookup"><span data-stu-id="dea10-146">The **Manage** option on the personalization toolbar enables you to export and import personalizations.</span></span>

## <a name="managing-custom-fields"></a><span data-ttu-id="dea10-147">Управление пользовательскими полями</span><span class="sxs-lookup"><span data-stu-id="dea10-147">Managing custom fields</span></span>

<span data-ttu-id="dea10-148">Управлять всеми настраиваемыми полями в системе можно на странице **Пользовательские поля** в модуле "Администрирование системы".</span><span class="sxs-lookup"><span data-stu-id="dea10-148">Management of all the custom fields in the system can be accomplished through the **Custom fields** page in the System administration module.</span></span> <span data-ttu-id="dea10-149">Эта страница обеспечивает пользователям доступ к многим возможностям, включая:</span><span class="sxs-lookup"><span data-stu-id="dea10-149">This page allows users access to many capabilities, including:</span></span>

- <span data-ttu-id="dea10-150">Просмотр списка всех настраиваемых полей в системе.</span><span class="sxs-lookup"><span data-stu-id="dea10-150">Viewing a list of all custom fields in the system.</span></span>
- <span data-ttu-id="dea10-151">Ограниченные возможности редактирования существующих настраиваемых полей.</span><span class="sxs-lookup"><span data-stu-id="dea10-151">Limited editing of existing custom fields.</span></span>
- <span data-ttu-id="dea10-152">Удаление пользовательских полей.</span><span class="sxs-lookup"><span data-stu-id="dea10-152">Deleting custom fields.</span></span>
- <span data-ttu-id="dea10-153">Предоставление настраиваемых полей для информационных объектов.</span><span class="sxs-lookup"><span data-stu-id="dea10-153">Exposing custom fields on data entities.</span></span>
- <span data-ttu-id="dea10-154">Предоставляет переводы меток настраиваемых полей и текста справки.</span><span class="sxs-lookup"><span data-stu-id="dea10-154">Providing translations of custom field labels and help text.</span></span>

### <a name="viewing-all-custom-fields"></a><span data-ttu-id="dea10-155">Просмотр всех настраиваемых полей</span><span class="sxs-lookup"><span data-stu-id="dea10-155">Viewing all custom fields</span></span>

<span data-ttu-id="dea10-156">Страница **Пользовательские поля** обеспечивает видимость всех пользовательских полей, которые были определены в системе.</span><span class="sxs-lookup"><span data-stu-id="dea10-156">The **Custom fields** page provides visibility to all the custom fields that have been defined in the system.</span></span> <span data-ttu-id="dea10-157">Просто выберите таблицу, которая вам интересна, и страница обновляется, чтобы отобразить список пользовательских полей, связанных с этой таблицей.</span><span class="sxs-lookup"><span data-stu-id="dea10-157">Simply select the table that you are interested in, and the page will update to show a list of the custom fields associated with that table.</span></span> <span data-ttu-id="dea10-158">Если выбрать пользовательское поле в списке, можно просмотреть все сведения о поле.</span><span class="sxs-lookup"><span data-stu-id="dea10-158">Choosing a custom field from the list will allow you to view all the details about the field.</span></span>

### <a name="editing-custom-fields"></a><span data-ttu-id="dea10-159">Редактирование пользовательских полей</span><span class="sxs-lookup"><span data-stu-id="dea10-159">Editing custom fields</span></span>

<span data-ttu-id="dea10-160">После создания пользовательского поля можно изменить только определенные части информации о пользовательском поле на странице **Пользовательские поля**.</span><span class="sxs-lookup"><span data-stu-id="dea10-160">After a custom field has been created, only certain pieces of information about the custom field can be modified on the **Custom fields** page.</span></span>

<span data-ttu-id="dea10-161">Вы *можете* изменять следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="dea10-161">You *can* modify these attributes:</span></span>

- <span data-ttu-id="dea10-162">Этикетка</span><span class="sxs-lookup"><span data-stu-id="dea10-162">Label</span></span>
- <span data-ttu-id="dea10-163">Текст справки</span><span class="sxs-lookup"><span data-stu-id="dea10-163">Help text</span></span>
- <span data-ttu-id="dea10-164">Длина для текстовых полей</span><span class="sxs-lookup"><span data-stu-id="dea10-164">Length, for Text fields</span></span>

<span data-ttu-id="dea10-165">Вы *не можете* изменять следующее атрибуты:</span><span class="sxs-lookup"><span data-stu-id="dea10-165">You *cannot* edit the following attributes:</span></span>

- <span data-ttu-id="dea10-166">Имя поля</span><span class="sxs-lookup"><span data-stu-id="dea10-166">Field name</span></span>
- <span data-ttu-id="dea10-167">Тип данных</span><span class="sxs-lookup"><span data-stu-id="dea10-167">Data type</span></span>

<span data-ttu-id="dea10-168">Кроме того, для полей списка выбора можно изменить порядок в наборе допустимых значений для настраиваемого поля и добавить новые значения; однако невозможно удалить существующие значения для поля списка выбора.</span><span class="sxs-lookup"><span data-stu-id="dea10-168">Additionally, for picklist fields, the set of valid values for the custom field can be reordered, and new values can be added; however, existing values for the picklist field cannot be removed.</span></span> <span data-ttu-id="dea10-169">Не забудьте щелкнуть **Применить изменить** после завершения редактирования полей для конкретной таблицы, чтобы изменения были сохранены.</span><span class="sxs-lookup"><span data-stu-id="dea10-169">Remember to click **Apply changes** when you are done editing fields for a particular table so the changes are saved.</span></span>

### <a name="exposing-custom-fields-on-data-entities"></a><span data-ttu-id="dea10-170">Предоставление пользовательских полей для информационных объектов</span><span class="sxs-lookup"><span data-stu-id="dea10-170">Exposing custom fields on data entities</span></span>

<span data-ttu-id="dea10-171">Также может быть важно разрешить, чтобы пользовательские поля были видимы в информационных объектах.</span><span class="sxs-lookup"><span data-stu-id="dea10-171">It may also be important to allow custom fields to be visible on data entities.</span></span> <span data-ttu-id="dea10-172">Информационные объекты используются в функции [Открыть в Office](../../dev-itpro/office-integration/office-integration.md), а также для сценариев импорта и экспорта данных.</span><span class="sxs-lookup"><span data-stu-id="dea10-172">Data entities are utilized in the [Open in Office](../../dev-itpro/office-integration/office-integration.md) feature, as well as for data import/export scenarios.</span></span>

<span data-ttu-id="dea10-173">Выполните следующие действия, чтобы отображение пользовательского поля для информационного объекта.</span><span class="sxs-lookup"><span data-stu-id="dea10-173">Follow these steps to expose a custom field on a data entity:</span></span>

1. <span data-ttu-id="dea10-174">Выберите пользовательское поле в форме **Пользовательские поля**.</span><span class="sxs-lookup"><span data-stu-id="dea10-174">Select the custom field on the **Custom fields** form.</span></span>
2. <span data-ttu-id="dea10-175">Разверните раздел **Объекты**, чтобы просмотреть набор соответствующих объектов.</span><span class="sxs-lookup"><span data-stu-id="dea10-175">Expand the **Entities** section to view the set of relevant entities.</span></span>
3. <span data-ttu-id="dea10-176">Нажмите кнопку **Правка**.</span><span class="sxs-lookup"><span data-stu-id="dea10-176">Click the **Edit** button.</span></span>
4. <span data-ttu-id="dea10-177">Измените поле **Включено**, которое должно быть выбрано для каждого объекта, который должен отображать это поле.</span><span class="sxs-lookup"><span data-stu-id="dea10-177">Modify the **Enabled** field to be selected for each entity that should expose this field.</span></span>
5. <span data-ttu-id="dea10-178">Щелкните **Применить изменение** для сохранения выбранных значений.</span><span class="sxs-lookup"><span data-stu-id="dea10-178">Click **Apply changes** to save your selections.</span></span>

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a><span data-ttu-id="dea10-179">Разрешение отображения пользовательских полей на других языках</span><span class="sxs-lookup"><span data-stu-id="dea10-179">Allowing custom fields to be displayed in other languages</span></span>

<span data-ttu-id="dea10-180">Так как доступ к пользовательским полям может потребоваться пользователям на различных языках, страница **Пользовательские поля** предоставляет механизм, позволяющий переводить метки и текст справки для пользовательского поля на другие языки.</span><span class="sxs-lookup"><span data-stu-id="dea10-180">Because custom fields may need to be accessed by users in a variety of languages, the **Custom fields** page provides a mechanism to allow the label and help text for a custom field to be translated into other languages.</span></span>

<span data-ttu-id="dea10-181">Следующие шаги описывают процесс перевода пользовательских полей на другие языки:</span><span class="sxs-lookup"><span data-stu-id="dea10-181">The following steps describe the process for translating custom fields in other languages:</span></span>

1. <span data-ttu-id="dea10-182">Выберите пользовательское поле на странице **Пользовательские поля**.</span><span class="sxs-lookup"><span data-stu-id="dea10-182">Select the custom field on the **Custom fields** page.</span></span>
2. <span data-ttu-id="dea10-183">Выберите кнопку **Переводы** в области действий.</span><span class="sxs-lookup"><span data-stu-id="dea10-183">Select the **Translations** button in the Action Pane.</span></span> <span data-ttu-id="dea10-184">Откроется раскрывающееся меню, содержащее существующие переводы для этого поля.</span><span class="sxs-lookup"><span data-stu-id="dea10-184">This will open a drop-down menu with existing translations for this field.</span></span>
3. <span data-ttu-id="dea10-185">В раскрывающемся меню **Язык** отображается набор языков, для которых уже были предоставлены переводы.</span><span class="sxs-lookup"><span data-stu-id="dea10-185">The **Language** drop-down menu shows the set of languages for which translations have already been provided.</span></span>

    <span data-ttu-id="dea10-186">Если требуется изменить существующий перевод, выберите нужный язык в меню и измените значения для метки и текста справки.</span><span class="sxs-lookup"><span data-stu-id="dea10-186">If you want to edit an existing translation, select the desired language from the menu and modify the values for the label and help text.</span></span>

    <span data-ttu-id="dea10-187">В противном случае нажмите кнопку **Добавить язык**, выберите нужный язык в меню и укажите переведенные значения метки и текста справки.</span><span class="sxs-lookup"><span data-stu-id="dea10-187">Otherwise, click the **Add language** button, select the desired language from the menu, and then provide translated values for the label and help text.</span></span>

4. <span data-ttu-id="dea10-188">После завершения щелкните **ОК**.</span><span class="sxs-lookup"><span data-stu-id="dea10-188">Click **OK** when you are finished.</span></span>

### <a name="deleting-custom-fields"></a><span data-ttu-id="dea10-189">Удаление пользовательских полей</span><span class="sxs-lookup"><span data-stu-id="dea10-189">Deleting custom fields</span></span>

<span data-ttu-id="dea10-190">В некоторых редких случаях вы можете решить, что пользовательское поле больше не нужно.</span><span class="sxs-lookup"><span data-stu-id="dea10-190">In some rare cases, you may decide that a custom field is no longer needed.</span></span> <span data-ttu-id="dea10-191">Когда это происходит, системный администратор может удалить поле со страницы **Пользовательские поля**.</span><span class="sxs-lookup"><span data-stu-id="dea10-191">When this occurs, a system administrator can choose to delete the field from the **Custom fields** page.</span></span> <span data-ttu-id="dea10-192">Для этого убедитесь, что выбрано правильное поле, щелкните **Удалить**, щелкните **Да**, чтобы подтвердить удаление, и снова щелкните **Применить изменения**.</span><span class="sxs-lookup"><span data-stu-id="dea10-192">To do this, ensure the correct field is selected, click **Delete**, click **Yes** to confirm the deletion, and finally click **Apply changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="dea10-193">Это действие не может быть отменено и приведет к окончательному удалению данных, связанных с полем, из базы данных.</span><span class="sxs-lookup"><span data-stu-id="dea10-193">This action cannot be undone, and will result in the data associated with the field being permanently deleted from the database.</span></span>

## <a name="appendix"></a><span data-ttu-id="dea10-194">Приложение</span><span class="sxs-lookup"><span data-stu-id="dea10-194">Appendix</span></span>

### <a name="who-can-create-custom-fields"></a><span data-ttu-id="dea10-195">Кто может создавать пользовательские поля?</span><span class="sxs-lookup"><span data-stu-id="dea10-195">Who can create custom fields?</span></span>

<span data-ttu-id="dea10-196">По умолчанию для безопасности системы только системные администраторы могут создавать пользовательские поля.</span><span class="sxs-lookup"><span data-stu-id="dea10-196">As a safeguard to the system, only system administrators are able to create custom fields by default.</span></span> <span data-ttu-id="dea10-197">Однако если это необходимо для организации, избранным опытным пользователям могут быть заданы права для создания настраиваемых полей системным администратором с помощью роли безопасности **Опытные пользователи для настройки во время выполнения**.</span><span class="sxs-lookup"><span data-stu-id="dea10-197">However, those power users whom the organization deems necessary can be given rights to create custom fields by a system administrator using the **Runtime customization power user** security role.</span></span> <span data-ttu-id="dea10-198">Пользователи, не имеющие этой роли безопасности, не смогут создавать настраиваемые поля, но по-прежнему смогут видеть и взаимодействовать с настраиваемыми полями, добавленными другими пользователями в систему.</span><span class="sxs-lookup"><span data-stu-id="dea10-198">Users without this security role will not be able to create custom fields, but will still be able to see and interact with custom fields added by other users in the system.</span></span>

### <a name="what-tables-support-custom-fields"></a><span data-ttu-id="dea10-199">Какие таблицы поддерживают пользовательские поля?</span><span class="sxs-lookup"><span data-stu-id="dea10-199">What tables support custom fields?</span></span>

<span data-ttu-id="dea10-200">Для причинам производительности и техническим причинам только таблицы, которые удовлетворяют следующим условиям, в настоящее время допускают добавление пользовательских полей.</span><span class="sxs-lookup"><span data-stu-id="dea10-200">For performance and technical reasons, only tables that meet the following conditions currently allow custom fields to be added.</span></span>

- <span data-ttu-id="dea10-201">Таблица должна быть маркирована как одна из следующих групп:</span><span class="sxs-lookup"><span data-stu-id="dea10-201">The table must be tagged as one of these groups:</span></span>

    - <span data-ttu-id="dea10-202">Групповое</span><span class="sxs-lookup"><span data-stu-id="dea10-202">Group</span></span>
    - <span data-ttu-id="dea10-203">WorksheetHeader</span><span class="sxs-lookup"><span data-stu-id="dea10-203">WorksheetHeader</span></span>
    - <span data-ttu-id="dea10-204">Основная</span><span class="sxs-lookup"><span data-stu-id="dea10-204">Main</span></span>
    - <span data-ttu-id="dea10-205">Разное</span><span class="sxs-lookup"><span data-stu-id="dea10-205">Miscellaneous</span></span>
    - <span data-ttu-id="dea10-206">Параметр</span><span class="sxs-lookup"><span data-stu-id="dea10-206">Parameter</span></span>
    - <span data-ttu-id="dea10-207">Справка</span><span class="sxs-lookup"><span data-stu-id="dea10-207">Reference</span></span>
    - <span data-ttu-id="dea10-208">TransactionHeader</span><span class="sxs-lookup"><span data-stu-id="dea10-208">TransactionHeader</span></span>

- <span data-ttu-id="dea10-209">Таблица не может расширять другую таблицу.</span><span class="sxs-lookup"><span data-stu-id="dea10-209">The table cannot extend another table.</span></span>
- <span data-ttu-id="dea10-210">Таблица не может быть отмечена как системная таблица.</span><span class="sxs-lookup"><span data-stu-id="dea10-210">The table cannot be marked as a system table.</span></span>
- <span data-ttu-id="dea10-211">Таблица не может быть временной таблицей.</span><span class="sxs-lookup"><span data-stu-id="dea10-211">The table cannot be a temporary table.</span></span>
