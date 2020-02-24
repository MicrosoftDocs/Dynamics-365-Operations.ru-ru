---
title: Как избежать усечения текста в иерархии должностей и при экспорте в Visio
description: В этой статье объясняется, как решить проблему, когда имена людей и названия должностей усекаются при просмотре иерархии должностей клиентами в Microsoft Dynamics 365 Human Resources. Усечение текста затрудняет получение снимков экрана или печать иерархии.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 39ac850b70974dd15906039293bb6c60492da324
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010352"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a><span data-ttu-id="3af77-104">Исключение усечения текста по иерархии должностей и экспорт в Visio</span><span class="sxs-lookup"><span data-stu-id="3af77-104">Avoid text truncation on the position hierarchy and export to Visio</span></span>

<span data-ttu-id="3af77-105">**Расход**</span><span class="sxs-lookup"><span data-stu-id="3af77-105">**Issue**</span></span>

<span data-ttu-id="3af77-106">Когда клиент просматривает иерархию должностей в Microsoft Dynamics 365 Human Resources, имена людей и названия должностей усекаются.</span><span class="sxs-lookup"><span data-stu-id="3af77-106">When a customer views the position hierarchy in Microsoft Dynamics 365 Human Resources, the names of individuals and positions are truncated.</span></span> <span data-ttu-id="3af77-107">Поэтому может быть сложно сделать снимок экрана или распечатать иерархию для распространения.</span><span class="sxs-lookup"><span data-stu-id="3af77-107">Therefore, it can be difficult to take a screenshot, or to print and distribute the hierarchy.</span></span>

![Иерархия штатных единиц](media/position-h.png)

<span data-ttu-id="3af77-109">**Причина**</span><span class="sxs-lookup"><span data-stu-id="3af77-109">**Cause**</span></span>

<span data-ttu-id="3af77-110">Такое поведение предусмотрено разработчиками.</span><span class="sxs-lookup"><span data-stu-id="3af77-110">This behavior is by design.</span></span>

<span data-ttu-id="3af77-111">**Разрешение**</span><span class="sxs-lookup"><span data-stu-id="3af77-111">**Resolution**</span></span>

<span data-ttu-id="3af77-112">К сожалению, у пользователей нет простого способа изменить размер текста.</span><span class="sxs-lookup"><span data-stu-id="3af77-112">Unfortunately, users can't easily change the size of the text.</span></span> <span data-ttu-id="3af77-113">Тем не менее, можно экспортировать иерархию должностей из Human Resources, а затем импортировать ее в Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="3af77-113">However, you can export the position hierarchy out of Human Resources and then import it into Microsoft Visio.</span></span> <span data-ttu-id="3af77-114">Хотя следующая статья был написан для Microsoft Dynamics AX 2012, процесс все еще применим к Human Resources: [Экспорт иерархии должностей в Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span><span class="sxs-lookup"><span data-stu-id="3af77-114">Although the following article was written for Microsoft Dynamics AX 2012, the process still applies to Human Resources: [Export a position hierarchy to Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span></span>

<span data-ttu-id="3af77-115">Выполните следующие действия для экспорта в Visio.</span><span class="sxs-lookup"><span data-stu-id="3af77-115">Follow these steps to export to Visio.</span></span>

1. <span data-ttu-id="3af77-116">В Human Resources откройте страницу списка **Должности**.</span><span class="sxs-lookup"><span data-stu-id="3af77-116">In Human Resources, open the **Positions** list page.</span></span>

    <span data-ttu-id="3af77-117">Чтобы включить дополнительные сведения в диаграмму структуры организации, добавьте поля в список **Должности**, чтобы они были доступны при использовании мастера далее в этой процедуре.</span><span class="sxs-lookup"><span data-stu-id="3af77-117">To include more information in the organization structure diagram, add fields to the **Positions** list, so that they are available when you use the wizard later in this procedure.</span></span>

2. <span data-ttu-id="3af77-118">В области действий выберите кнопку **Открыть в Microsoft Office**, затем, в разделе **Экспорт в Excel**, выберите **Должности**.</span><span class="sxs-lookup"><span data-stu-id="3af77-118">On the Action Pane, select the **Open in Microsoft Office** button, and then, under **Export to Excel**, select **Positions**.</span></span> <span data-ttu-id="3af77-119">Также можно нажать сочетание клавиш Ctrl + T.</span><span class="sxs-lookup"><span data-stu-id="3af77-119">Alternatively, press Ctrl+T.</span></span>

    ![Экспорт страницы списка должностей в Excel](media/org-admin.png)

3. <span data-ttu-id="3af77-121">Сохраните экспортированный файл Excel.</span><span class="sxs-lookup"><span data-stu-id="3af77-121">Save the Excel file that is exported.</span></span>

    ![Диалоговое окно экспорта в Excel](media/export-excel.png)

4. <span data-ttu-id="3af77-123">В Visio выберите **Visio — создать новый**и выберите категорию шаблонов **Бизнес**.</span><span class="sxs-lookup"><span data-stu-id="3af77-123">In Visio, select **Visio - Create New**, and select the **Business** template category.</span></span>

    ![Создать диаграмму](media/new.png)

5. <span data-ttu-id="3af77-125">Выберите **Мастер организационных диаграмм**, затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3af77-125">Select **Organization Chart Wizard**, and then select **Create**.</span></span>

    ![Диалоговое окно мастера организационных диаграмм](media/orgchart-wizard.png)

6. <span data-ttu-id="3af77-127">Выберите **Информация, уже сохраненная в файл или базу данных**, затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3af77-127">Select **Information that's already stored in a file or database**, and then select **Next**.</span></span>

    ![Мастер организационной диаграммы 1](media/orgchart-wizard7.png)

7. <span data-ttu-id="3af77-129">Выберите **Текстовый файл, файл Org Plus (\*.txt) или файл Excel**, затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3af77-129">Choose **A text, Org Plus (\*.txt), or Excel file**, and then select **Next**.</span></span>

    ![Мастер организационной диаграммы 2](media/orgchart-wizard3.png)

8. <span data-ttu-id="3af77-131">Найдите и выберите экспортированный файл Excel, содержащий иерархию должностей, затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3af77-131">Browse to select the exported Excel file that contains the position hierarchy, and then select **Next**.</span></span>

    ![Мастер организационной диаграммы 3](media/orgchart-wizard2.png)

9. <span data-ttu-id="3af77-133">Задайте в поле **Имя** значение **Должность**, задайте в поле **Отчитывается перед** значение **Отчитывается перед должностью**, затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3af77-133">Set the **Name** field to **Position**, set the **Reports to** field to **Reports to position**, and then select **Next**.</span></span>

    ![Мастер организационной диаграммы 4](media/orgchart-wizard1.png)

10. <span data-ttu-id="3af77-135">Выберите поля, которые должны отображаться в каждом узле, затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3af77-135">Select the fields that should be shown on each node, and then select **Next**.</span></span>

    ![Мастер организационной диаграммы 5](media/orgchart-wizard5.png)

11. <span data-ttu-id="3af77-137">Добавьте столбец **Должность** в список **Поля данных фигуры**, затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3af77-137">Add the **Position** column to the **Shape Data fields** list, and then select **Next**.</span></span>

    ![Мастер организационной диаграммы 6](media/orgchart-wizard6.png)

12. <span data-ttu-id="3af77-139">Рисунки в настоящее время недоступны.</span><span class="sxs-lookup"><span data-stu-id="3af77-139">Pictures aren't currently available.</span></span> <span data-ttu-id="3af77-140">Поэтому на следующей странице выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3af77-140">Therefore, on the next page, select **Next**.</span></span>
13. <span data-ttu-id="3af77-141">Выберите **Мастер должен автоматически разбить организационную диаграмму на страницы**.</span><span class="sxs-lookup"><span data-stu-id="3af77-141">Select **I want the wizard to automatically break my organization chart across pages**.</span></span>

    ![Мастер организационной диаграммы 7](media/orgchart-wizard4.png)

14. <span data-ttu-id="3af77-143">Выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="3af77-143">Select **Finish**.</span></span>

    <span data-ttu-id="3af77-144">Если имеются какие-либо должности, которые не входят в структуру, вам будет предложено включить их в диаграмму.</span><span class="sxs-lookup"><span data-stu-id="3af77-144">If there are any positions that aren't in the structure, you're asked to include them in the diagram.</span></span>

<span data-ttu-id="3af77-145">Схема, которая создается в Visio, показывает каждого руководителя на отдельном листе.</span><span class="sxs-lookup"><span data-stu-id="3af77-145">The diagram that is generated in Visio shows each manager on a separate worksheet.</span></span>

<span data-ttu-id="3af77-146">На основании полей, которые были выбраны для включения в диаграмму, каждый узел отображает соответствующую информацию при создании файла Visio.</span><span class="sxs-lookup"><span data-stu-id="3af77-146">Based on the fields that you selected to include in the diagram, each node shows the appropriate information when the Visio file is generated.</span></span>

![Диаграмма иерархии](media/hierarchy.png)

<span data-ttu-id="3af77-148">**Дополнительный параметр**</span><span class="sxs-lookup"><span data-stu-id="3af77-148">**Additional option**</span></span>

<span data-ttu-id="3af77-149">В Human Resources также можно использовать рабочую область **Люди**, чтобы просмотреть некоторую информацию, относящуюся к иерархии.</span><span class="sxs-lookup"><span data-stu-id="3af77-149">In Human Resources, you might also be able to use the **People** workspace to view some hierarchy-related information.</span></span>
