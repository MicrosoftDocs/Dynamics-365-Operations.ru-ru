---
title: "Просмотр и экспорт описаний полей"
description: "В этой статье описываются способы просмотра описаний полей и использования страницы \"Описания полей\" для экспорта описаний."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 812db9f1d319e4d16f83700a7153a0a3b318963e
ms.openlocfilehash: cfe5126841905248d0ab04ed9a718098c11bbd22
ms.contentlocale: ru-ru
ms.lasthandoff: 03/23/2018

---

# <a name="view-and-export-field-descriptions"></a><span data-ttu-id="d72f4-103">Просмотр и экспорт описаний полей</span><span class="sxs-lookup"><span data-stu-id="d72f4-103">View and export field descriptions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d72f4-104">В этой статье описываются способы просмотра описаний полей и использования страницы "Описания полей" для экспорта описаний.</span><span class="sxs-lookup"><span data-stu-id="d72f4-104">This article describes how to view field descriptions and how to use the Field descriptions page to export descriptions.</span></span>

<span data-ttu-id="d72f4-105">В Microsoft Dynamics 365 for Finance and Operations предусмотрены описания для некоторых из более сложных полей.</span><span class="sxs-lookup"><span data-stu-id="d72f4-105">Microsoft Dynamics 365 for Finance and Operations has descriptions for some of the more complex fields.</span></span> <span data-ttu-id="d72f4-106">Эти описания отображаются при наведении указателя мыши на поле.</span><span class="sxs-lookup"><span data-stu-id="d72f4-106">These descriptions appear when you hover over a field.</span></span> <span data-ttu-id="d72f4-107">Также можно просмотреть и экспортировать описания на странице **Описания полей**.</span><span class="sxs-lookup"><span data-stu-id="d72f4-107">You can also view and export descriptions on the **Field descriptions** page.</span></span> 

<span data-ttu-id="d72f4-108">Не все страницы имеют описания полей.</span><span class="sxs-lookup"><span data-stu-id="d72f4-108">Not all pages have field descriptions.</span></span> <span data-ttu-id="d72f4-109">Мы хотим предоставить описания только для более сложных полей, а не для полей, использование которых очевидно.</span><span class="sxs-lookup"><span data-stu-id="d72f4-109">We want to provide descriptions only for the more complex fields, not where the use of the field is obvious.</span></span> <span data-ttu-id="d72f4-110">Таким образом, некоторые страницы не имеют описаний полей, некоторые страницы имеют несколько описаний, а некоторые из более сложных страниц, например многие страницы параметров, имеют множество описаний.</span><span class="sxs-lookup"><span data-stu-id="d72f4-110">Therefore, some pages don't have any field descriptions, some pages have a few descriptions, and some of the more complex pages, such as many of the parameters pages, have many descriptions.</span></span> 

<span data-ttu-id="d72f4-111">Если вы имеете доступ к среде разработки Finance and Operations, вы можете добавить новые описания полей и настроить существующие описания.</span><span class="sxs-lookup"><span data-stu-id="d72f4-111">If you have access to the Finance and Operations development environment, you can add new field descriptions and customize existing descriptions.</span></span> <span data-ttu-id="d72f4-112">Например, можно добавить сведения о конкретной компании в описание поля.</span><span class="sxs-lookup"><span data-stu-id="d72f4-112">For example, you can add company-specific information to a field description.</span></span> <span data-ttu-id="d72f4-113">Дополнительные сведения см. в разделе [Настройка справки полей](../../dev-itpro/user-interface/customize-field-help.md).</span><span class="sxs-lookup"><span data-stu-id="d72f4-113">For more information, see [Customize field help](../../dev-itpro/user-interface/customize-field-help.md).</span></span>

## <a name="see-field-descriptions-in-the-user-interface"></a><span data-ttu-id="d72f4-114">Просмотр описаний полей в пользовательском интерфейсе</span><span class="sxs-lookup"><span data-stu-id="d72f4-114">See field descriptions in the user interface</span></span>
<span data-ttu-id="d72f4-115">Можно просматривать описания полей, наведя указатель мыши на поле.</span><span class="sxs-lookup"><span data-stu-id="d72f4-115">You can view field descriptions by hovering over a field.</span></span> <span data-ttu-id="d72f4-116">Если описание отсутствует, при наведении указателя мыши на поле отобразится имя поля.</span><span class="sxs-lookup"><span data-stu-id="d72f4-116">If no description is available, you see the field name when you hover over the field.</span></span> <span data-ttu-id="d72f4-117">(Примечание. В Dynamics AX 7.0 (февраль 2016 г.), описания полей можно просмотреть только на странице **Описания полей**.) На следующем рисунке показано описание поля, которое отображается при наведении указателя мыши на поле **Блокир. номенкл. при инвентаризации**.</span><span class="sxs-lookup"><span data-stu-id="d72f4-117">(Note: In Dynamics AX 7.0 (February 2016), field descriptions can be viewed only on the **Field descriptions** page.) The following illustration shows the field description that appears when you hover over the **Lock items during count** field.</span></span> 

<span data-ttu-id="d72f4-118">[![Пример описания поля](./media/field-description.png)](./media/field-description.png)</span><span class="sxs-lookup"><span data-stu-id="d72f4-118">[![Example of a field description](./media/field-description.png)](./media/field-description.png)</span></span>

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a><span data-ttu-id="d72f4-119">Использование страницы "Описания полей" для просмотра и экспорта справки поля</span><span class="sxs-lookup"><span data-stu-id="d72f4-119">Use the Field descriptions page to view and export field help</span></span>
<span data-ttu-id="d72f4-120">Страница **Описания полей** позволяет просматривать и экспортировать описания полей.</span><span class="sxs-lookup"><span data-stu-id="d72f4-120">The **Field descriptions** page lets you view and export field descriptions.</span></span> <span data-ttu-id="d72f4-121">Можно одновременно просмотреть описания, доступные для одной страницы.</span><span class="sxs-lookup"><span data-stu-id="d72f4-121">You can see the descriptions that are available for one page at a time.</span></span>

### <a name="view-the-descriptions-for-a-page"></a><span data-ttu-id="d72f4-122">Просмотр описаний для страницы</span><span class="sxs-lookup"><span data-stu-id="d72f4-122">View the descriptions for a page</span></span>

<span data-ttu-id="d72f4-123">Чтобы просмотреть описания для страницы, выполните этот шаг.</span><span class="sxs-lookup"><span data-stu-id="d72f4-123">To view the descriptions for a page, follow this step.</span></span>

-   <span data-ttu-id="d72f4-124">В поле **Выбор страницы** введите имя страницы.</span><span class="sxs-lookup"><span data-stu-id="d72f4-124">In the **Select a page** field, type the name of the page.</span></span> <span data-ttu-id="d72f4-125">Либо щелкните стрелку, чтобы открыть список всех страниц, и просмотрите либо отфильтруйте список.</span><span class="sxs-lookup"><span data-stu-id="d72f4-125">Alternatively, click the arrow to open a list of all the pages, and then browse or filter the list.</span></span>

<span data-ttu-id="d72f4-126">Можно использовать либо имя страницы, которое отображается в пользовательском интерфейсе (например, **Клиенты**), либо имя кода (имя AOT), доступное при щелчке страницы правой кнопкой мыши (например, **CustTable**).</span><span class="sxs-lookup"><span data-stu-id="d72f4-126">You can use either the name of the page that is shown in the user interface (UI) (for example, **Customers**) or the code name (AOT name) that's available when you right-click a page (for example, **CustTable**).</span></span> 

<span data-ttu-id="d72f4-127">Сведения о различных способах фильтрации списка страниц см. в разделе "Поиск страницы" далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="d72f4-127">For information about the various ways to filter the list of pages, see the "Searching for a page" section later in this article.</span></span> 

<span data-ttu-id="d72f4-128">Если для параметра **Включить поля без описания** задать значение **Да**, будут отображаться все поля на странице независимо от того, имеют ли они описание поля.</span><span class="sxs-lookup"><span data-stu-id="d72f4-128">If you set the **Include fields without a description** option to **Yes**, all the fields on the page are shown, even if they don't have a field description.</span></span>

### <a name="export-the-descriptions-for-a-page"></a><span data-ttu-id="d72f4-129">Экспорт описаний для страницы</span><span class="sxs-lookup"><span data-stu-id="d72f4-129">Export the descriptions for a page</span></span>

<span data-ttu-id="d72f4-130">Чтобы экспортировать описания для страницы, выполните эти шаги.</span><span class="sxs-lookup"><span data-stu-id="d72f4-130">To export the descriptions for a page, follow these steps.</span></span>

1.  <span data-ttu-id="d72f4-131">В поле **Выбор страницы** выберите страницу.</span><span class="sxs-lookup"><span data-stu-id="d72f4-131">In the **Select a page** field, select a page.</span></span>
2.  <span data-ttu-id="d72f4-132">Нажмите кнопку **Открыть в Microsoft Office** в правом верхнем углу и щелкните **FieldDescriptionTmp**.</span><span class="sxs-lookup"><span data-stu-id="d72f4-132">Click the **Open in Microsoft Office** button in the upper-right corner, and then click **FieldDescriptionTmp**.</span></span>

### <a name="searching-for-a-page"></a><span data-ttu-id="d72f4-133">Поиск страницы</span><span class="sxs-lookup"><span data-stu-id="d72f4-133">Searching for a page</span></span>

<span data-ttu-id="d72f4-134">Существует несколько способов поиска страницы в поле **Выбор страницы**.</span><span class="sxs-lookup"><span data-stu-id="d72f4-134">There are several ways to search for a page in the **Select a page** field.</span></span> <span data-ttu-id="d72f4-135">Во многих случаях вам потребуется щелкнуть стрелку в поле **Выбор страницы**, чтобы открыть раскрывающийся список, и выбрать страницу из отфильтрованного списка страниц.</span><span class="sxs-lookup"><span data-stu-id="d72f4-135">In many cases, you must click the arrow in the **Select a page** field to open the drop-down list, and then select from a filtered list of pages.</span></span>

-   <span data-ttu-id="d72f4-136">Введите часть имени и откройте раскрывающийся список, чтобы выбрать страницу из списка отфильтрованных страниц.</span><span class="sxs-lookup"><span data-stu-id="d72f4-136">Type part of the name, and then open the drop-down list to select from a filtered list of pages.</span></span>
-   <span data-ttu-id="d72f4-137">Откройте раскрывающийся список и щелкните заголовок **Имя страницы** в верхней части списка или заголовок **Имя AOT страницы**.</span><span class="sxs-lookup"><span data-stu-id="d72f4-137">Open the drop-down list, and then click either the **Page name** heading at the top of the list or the **Page AOT name** heading.</span></span> <span data-ttu-id="d72f4-138">Откроется диалоговое окно, в котором можно использовать параметры расширенной фильтрации, например **Имя страницы начинается с**.</span><span class="sxs-lookup"><span data-stu-id="d72f4-138">A dialog box appears, where you can use advanced filtering options, such as **Page name begins with**.</span></span>
-   <span data-ttu-id="d72f4-139">Введите полное название страницы.</span><span class="sxs-lookup"><span data-stu-id="d72f4-139">Type the full name of the page.</span></span> <span data-ttu-id="d72f4-140">При использовании этого параметра рекомендуется открыть раскрывающийся список и посмотреть, что еще есть в списке, даже если описания полей отображаются.</span><span class="sxs-lookup"><span data-stu-id="d72f4-140">When you use this option, it's best to open the drop-down list and see what else is in the list, even if field descriptions are shown.</span></span>
    -   <span data-ttu-id="d72f4-141">Если есть одно точное соответствие имени, будут показаны описания полей для этой страницы.</span><span class="sxs-lookup"><span data-stu-id="d72f4-141">If there is a single exact match to the name, the field descriptions for that page are shown.</span></span>
    -   <span data-ttu-id="d72f4-142">Если имеется несколько точных совпадений, описания не будут отображаться.</span><span class="sxs-lookup"><span data-stu-id="d72f4-142">If there is more than one exact match, no descriptions are shown.</span></span> <span data-ttu-id="d72f4-143">Необходимо открыть раскрывающийся список и выбрать нужную страницу.</span><span class="sxs-lookup"><span data-stu-id="d72f4-143">You must open the drop-down list and select the page that you want.</span></span>
    -   <span data-ttu-id="d72f4-144">Если введенное имя является частью имени другой страницы, отобразятся описания для страницы.</span><span class="sxs-lookup"><span data-stu-id="d72f4-144">If the name that you typed is part of the name of another page, you see the descriptions for your page.</span></span> <span data-ttu-id="d72f4-145">Однако при открытии раскрывающегося списка, можно просмотреть дополнительные страницы, которые содержат это имя.</span><span class="sxs-lookup"><span data-stu-id="d72f4-145">However, if you open the drop-down list, you see additional pages that contain that name.</span></span>

<span data-ttu-id="d72f4-146">Например, описания не отображаются при вводе **Инвентаризация** в поле ****Выбор страницы****.</span><span class="sxs-lookup"><span data-stu-id="d72f4-146">For example, no descriptions are shown when you type **Counting** in the ****Select a page**** field.</span></span> <span data-ttu-id="d72f4-147">Вы открываете раскрывающийся список и увидите две страницы с именем **Инвентаризация** и несколько страниц, в имени которых содержится слово "Инвентаризация".</span><span class="sxs-lookup"><span data-stu-id="d72f4-147">You open the drop-down list, and see that there are two pages that have the name **Counting** and several pages that contain the word "Counting" in the name.</span></span> <span data-ttu-id="d72f4-148">При выборе страницы с именем AOT **InventJournalCount** отобразятся описания полей для этой страницы.</span><span class="sxs-lookup"><span data-stu-id="d72f4-148">If you select the page that has the AOT name **InventJournalCount**, the field descriptions are shown for that page.</span></span> <span data-ttu-id="d72f4-149">Однако, если снова открыть раскрывающийся список, вы увидите, что теперь список содержит все страницы, в имени AOT которых имеется InventJournalCount.</span><span class="sxs-lookup"><span data-stu-id="d72f4-149">However, if you open the drop-down list again, you will see that the list now contains all pages that have "InventJournalCount" as part of their AOT name.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="d72f4-150">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="d72f4-150">Troubleshooting</span></span>
<span data-ttu-id="d72f4-151">В этом разделе содержатся сведения, которые помогут устранить неполадки, с которыми можно столкнуться при использовании описаний полей.</span><span class="sxs-lookup"><span data-stu-id="d72f4-151">This section provides information to help you troubleshoot issues that you might encounter when you use field descriptions.</span></span>

### <a name="i-cant-find-a-field-description"></a><span data-ttu-id="d72f4-152">Не удается найти описание поля</span><span class="sxs-lookup"><span data-stu-id="d72f4-152">I can't find a field description</span></span>

<span data-ttu-id="d72f4-153">Мы в процессе добавления описаний для более сложных полей.</span><span class="sxs-lookup"><span data-stu-id="d72f4-153">We’re in the process of adding descriptions for the more complex fields.</span></span> <span data-ttu-id="d72f4-154">Если вам необходима помощь по определенному полю, дайте нам знать, добавив комментарий для этого раздела.</span><span class="sxs-lookup"><span data-stu-id="d72f4-154">If you require help for a particular field, let us know by adding a comment for this topic.</span></span>

### <a name="the-field-description-isnt-helpful"></a><span data-ttu-id="d72f4-155">Описание полей не полезно</span><span class="sxs-lookup"><span data-stu-id="d72f4-155">The field description isn't helpful</span></span>

<span data-ttu-id="d72f4-156">Дайте нам знать, добавив комментарий для этого раздела.</span><span class="sxs-lookup"><span data-stu-id="d72f4-156">Let us know by adding a comment for this topic.</span></span> <span data-ttu-id="d72f4-157">Если возможно, укажите, какая дополнительная информация вам требуется.</span><span class="sxs-lookup"><span data-stu-id="d72f4-157">If you can, describe the additional information that you require.</span></span>

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a><span data-ttu-id="d72f4-158">Не удается найти поле на странице "Описания полей"</span><span class="sxs-lookup"><span data-stu-id="d72f4-158">I can't find a field on the Field descriptions page</span></span>

<span data-ttu-id="d72f4-159">Для отображения всех полей на странице задайте параметру **Включить поля без описания** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="d72f4-159">To show all the fields on a page, set the **Include fields without a description** option to **Yes**.</span></span> <span data-ttu-id="d72f4-160">Щелкните поле **Выбор страницы**, чтобы убедиться, что выбрана правильная страница.</span><span class="sxs-lookup"><span data-stu-id="d72f4-160">Click the **Select a page** field to verify that you've selected the correct page.</span></span> <span data-ttu-id="d72f4-161">Если введенное имя является частью другого имени поля, возможно, вы выбрали страницу, которая имеет более длинное имя.</span><span class="sxs-lookup"><span data-stu-id="d72f4-161">If the name that you typed is part of another field name, you might have selected the page that has the longer name.</span></span>

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a><span data-ttu-id="d72f4-162">Не удается найти страницу на странице "Описания полей"</span><span class="sxs-lookup"><span data-stu-id="d72f4-162">I can't find a page on the Field descriptions page</span></span>

<span data-ttu-id="d72f4-163">Сведения о различных способах поиска страниц см. в разделе "Поиск страниц" ранее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="d72f4-163">For information about the various way to find pages, see the "Searching for pages" section earlier in this article.</span></span> <span data-ttu-id="d72f4-164">Если вы ввели точное имя страницы, описания полей могут не отображаться, если существует несколько страниц с одинаковым именем.</span><span class="sxs-lookup"><span data-stu-id="d72f4-164">If you've typed the exact name of the page, the field descriptions might not be shown if more than one page has the same name.</span></span> <span data-ttu-id="d72f4-165">Щелкните стрелку в поле **Выбор страницы**, чтобы открыть отфильтрованный список доступных страниц.</span><span class="sxs-lookup"><span data-stu-id="d72f4-165">Click the arrow in the **Select a page** field to open a filtered list of the pages that are available.</span></span>

<a name="see-also"></a><span data-ttu-id="d72f4-166">См. также</span><span class="sxs-lookup"><span data-stu-id="d72f4-166">See also</span></span>
--------

[<span data-ttu-id="d72f4-167">Настройка справки полей</span><span class="sxs-lookup"><span data-stu-id="d72f4-167">Customize field help</span></span>](../../dev-itpro/user-interface/customize-field-help.md)





