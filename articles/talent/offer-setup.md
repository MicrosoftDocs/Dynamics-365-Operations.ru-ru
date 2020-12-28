---
title: Настройка управления предложениями в Attract
description: В этом разделе описывается, как настроить предложения в Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc91a83afd5ce1627376685bcf612d6998ddbc02
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462342"
---
# <a name="set-up-offer-management-in-attract"></a><span data-ttu-id="52707-103">Настройка управления предложениями в Attract</span><span class="sxs-lookup"><span data-stu-id="52707-103">Set up offer management in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="52707-104">При перемещении кандидата на стадию предложения в Dynamics 365 Talent: Attract необходимо убедиться, что предложения может быть быстро создано для кандидата, одобрено по необходимости и отправлено кандидату.</span><span class="sxs-lookup"><span data-stu-id="52707-104">When a candidate is moved to the offer stage in Dynamics 365 Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="52707-105">Поскольку большинство предложений являются стандартными, они могут быть созданы на основе шаблонов для повторного использования.</span><span class="sxs-lookup"><span data-stu-id="52707-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="52707-106">В Attract все предложения упакованы в пакет предложений, который представляет собой набор из одного или нескольких документов для предложения.</span><span class="sxs-lookup"><span data-stu-id="52707-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="52707-107">В этом разделе перечислены все действия, которым администратору Attract нужно следовать, чтобы настроить шаблоны пакета как часть возможности управления предложениями в Attract.</span><span class="sxs-lookup"><span data-stu-id="52707-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="52707-108">Пользователи с ролями, не являющими администраторами, не будут иметь доступ к этим возможностям.</span><span class="sxs-lookup"><span data-stu-id="52707-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="52707-109">Возможности управления предложениями доступны в рамках надстройки Comprehensive Hiring.</span><span class="sxs-lookup"><span data-stu-id="52707-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="52707-110">Данные предложения</span><span class="sxs-lookup"><span data-stu-id="52707-110">Offer data</span></span> 

<span data-ttu-id="52707-111">Данные предложений являются наименьшей единицей в шаблоне пакета предложений.</span><span class="sxs-lookup"><span data-stu-id="52707-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="52707-112">Типичное предложение состоит из стандартного текста и набора значений.</span><span class="sxs-lookup"><span data-stu-id="52707-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="52707-113">Наборы значений являются единственными элементами, которые могут изменяться между предложениями.</span><span class="sxs-lookup"><span data-stu-id="52707-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="52707-114">При создании предложения самый важный аспект, на котором создатель предложения может сосредоточиться, — это список заполнителей данных предложений, имеющиеся в шаблоне пакета предложения.</span><span class="sxs-lookup"><span data-stu-id="52707-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="52707-115">Чтобы настроить данные предложения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="52707-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="52707-116">Перейдите в **Управление предложением**.</span><span class="sxs-lookup"><span data-stu-id="52707-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="52707-117">Разверните раздел **Библиотека** в левой области навигации, затем перейдите к **Данные предложения**.</span><span class="sxs-lookup"><span data-stu-id="52707-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="52707-118">На странице **Данные предложения** имеются разделы **Сведения о кандидате** и **Сведения о вакансии**.</span><span class="sxs-lookup"><span data-stu-id="52707-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="52707-119">Attract предоставляет несколько готовых заполнителей данных предложения.</span><span class="sxs-lookup"><span data-stu-id="52707-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    > 
    > <span data-ttu-id="52707-120">На странице имеются разделы для организации различных заполнителей данных предложения вместе в логические группы.</span><span class="sxs-lookup"><span data-stu-id="52707-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="52707-121">Эти разделы могут помочь в ведении данных предложения и заполнения данных во время создания предложения.</span><span class="sxs-lookup"><span data-stu-id="52707-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>
    > 
    > <span data-ttu-id="52707-122">Чтобы создать список значений для заполнителя, загрузите таблицу Excel, которая имеет одну колонку с заголовком столбца в качестве заголовка столбца и список вариантов в строках внизу.</span><span class="sxs-lookup"><span data-stu-id="52707-122">To create a list of values for a placeholder, upload an Excel spreadsheet that has one column with the placeholder as the column title and the list of choices in the rows underneath.</span></span> <span data-ttu-id="52707-123">Если на тот же заполнитель есть ссылка в другом наборе правил данных, убедитесь, что у них есть общий набор значений.</span><span class="sxs-lookup"><span data-stu-id="52707-123">If the same placeholder is referenced in another data rule set, ensure they have a common set of values.</span></span>
    
1.  <span data-ttu-id="52707-124">Чтобы создать новый раздел данных предложения, щелкните **Добавить раздел** и введите уникальное имя для раздела.</span><span class="sxs-lookup"><span data-stu-id="52707-124">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="52707-125">Чтобы добавить заполнители данных предложение к какому-либо разделу, нажмите **Добавить данные предложения** и введите уникальное имя для заполнителя.</span><span class="sxs-lookup"><span data-stu-id="52707-125">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="52707-126">Чтобы изменить имя любого раздела, наведите указатель мыши на имя раздела и обновите имя.</span><span class="sxs-lookup"><span data-stu-id="52707-126">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="52707-127">Чтобы изменить имя любого существующего заполнителя данных предложения, сначала убедитесь, что заполнитель еще не является частью какого-либо шаблона.</span><span class="sxs-lookup"><span data-stu-id="52707-127">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="52707-128">Затем наведите указатель мыши на имя заполнителя данных предложения и обновите имя при необходимости.</span><span class="sxs-lookup"><span data-stu-id="52707-128">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="52707-129">Чтобы удалить существующий заполнитель данных предложения, сначала убедитесь, что заполнитель еще не является частью какого-то другого шаблона.</span><span class="sxs-lookup"><span data-stu-id="52707-129">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="52707-130">Затем наведите указатель мыши на заполнитель и, когда появится значок корзины, щелкните корзину для удаления заполнителя данных предложения.</span><span class="sxs-lookup"><span data-stu-id="52707-130">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="52707-131">Можно увидеть, в сколько шаблонов входит заполнитель данных предложений, но числовому индикатору рядом с каждым элементом данных предложения.</span><span class="sxs-lookup"><span data-stu-id="52707-131">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="52707-132">Чтобы удалить любой раздел, наведите указатель мыши на имя.</span><span class="sxs-lookup"><span data-stu-id="52707-132">To delete any section, hover over the name.</span></span> <span data-ttu-id="52707-133">Если ни один заполнитель данных предложения внутри раздела не используется ни в одном шаблоне, можно щелкнуть значок корзины для его удаления.</span><span class="sxs-lookup"><span data-stu-id="52707-133">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="52707-134">Удаление раздела приведет к удалению всех заполнителей данных предложений в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="52707-134">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="52707-135">После того как заполнители данных предложений были настроены, их можно использовать в любом шаблоне документа.</span><span class="sxs-lookup"><span data-stu-id="52707-135">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="52707-136">Заполнители данных предложений не ограничены определенным шаблоном — тот же набор может использоваться во всех шаблонах.</span><span class="sxs-lookup"><span data-stu-id="52707-136">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="52707-137">Правила данных в приложении</span><span class="sxs-lookup"><span data-stu-id="52707-137">Offer data rules</span></span>

<span data-ttu-id="52707-138">Большинство организации предусматривают правила в отношении того, как должны создаваться предложения.</span><span class="sxs-lookup"><span data-stu-id="52707-138">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="52707-139">Например, организация может требовать, чтобы комбинация максимальной ежегодной зарплаты для определенного местоположения и уровень трудового стажа находились в пределах определенного диапазона, или чтобы были возможны только несколько конкретных значений для уровня предложение для найма новых сотрудников.</span><span class="sxs-lookup"><span data-stu-id="52707-139">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="52707-140">Attract в настоящее время поддерживает все такие правила данных с использованием файла CSV.</span><span class="sxs-lookup"><span data-stu-id="52707-140">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="52707-141">Чтобы подготовить CSV-файл с правилами данных, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="52707-141">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="52707-142">Определите заполнитель данных предложения для набора правил.</span><span class="sxs-lookup"><span data-stu-id="52707-142">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="52707-143">Например **Ежегодная зарплата**.</span><span class="sxs-lookup"><span data-stu-id="52707-143">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="52707-144">Укажите значения заполнителей зависимых данных предложения.</span><span class="sxs-lookup"><span data-stu-id="52707-144">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="52707-145">Например, **Местонахождение должности** и **Уровень**.</span><span class="sxs-lookup"><span data-stu-id="52707-145">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="52707-146">Укажите столбцы 1 и 2 в качестве **Местонахождение должности** и **Уровень**.</span><span class="sxs-lookup"><span data-stu-id="52707-146">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="52707-147">Чтобы отправить значение диапазона, сделайте столбцы 3 и 4 **Ежегодная зарплата**.</span><span class="sxs-lookup"><span data-stu-id="52707-147">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="52707-148">Чтобы отправить определенное значение, а не диапазон, только сделайте столбец 3 **Ежегодная зарплата**.</span><span class="sxs-lookup"><span data-stu-id="52707-148">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="52707-149">Заполните файл Microsoft Excel в зависимости от требуемых ролей.</span><span class="sxs-lookup"><span data-stu-id="52707-149">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="52707-150">Убедитесь, что каждая строка содержит уникальное сочетание всех значений, объединенных вместе.</span><span class="sxs-lookup"><span data-stu-id="52707-150">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="52707-151">Сохраните файл в формате CSV.</span><span class="sxs-lookup"><span data-stu-id="52707-151">Save the file as a CSV format.</span></span>

<span data-ttu-id="52707-152">Чтобы отправить файл с правилами данных предложения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="52707-152">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="52707-153">Перейдите в **Управление предложением**.</span><span class="sxs-lookup"><span data-stu-id="52707-153">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="52707-154">Разверните раздел **Библиотека** в левой области навигации, затем перейдите к **Правила данных в предложении**.</span><span class="sxs-lookup"><span data-stu-id="52707-154">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="52707-155">Щелкните **Создать набор данных** для отображения диалогового окна **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="52707-155">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="52707-156">Укажите уникальное имя для набора правил, затем отправьте сохраненный CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="52707-156">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="52707-157">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="52707-157">Click **Add**.</span></span>
    <span data-ttu-id="52707-158">Набор правил будут обрабатываться в фоновом режиме, и вы будете оповещены в приложения и по электронной почте после завершения.</span><span class="sxs-lookup"><span data-stu-id="52707-158">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="52707-159">Вы будете оповещены в случае ошибок при обработке отправки.</span><span class="sxs-lookup"><span data-stu-id="52707-159">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="52707-160">Затем можно загрузить журнал ошибок, исправить файл и отправить его еще раз.</span><span class="sxs-lookup"><span data-stu-id="52707-160">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="52707-161">Используйте параметр кнопки с многоточием (**...**), если хотите загрузить набор правил и отправить набор значений.</span><span class="sxs-lookup"><span data-stu-id="52707-161">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="52707-162">После обновления можно отправить файл еще раз.</span><span class="sxs-lookup"><span data-stu-id="52707-162">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="52707-163">Можно удалить существующую загрузку набора правил, если удаляемый заполнитель не используется в другом шаблоне документа.</span><span class="sxs-lookup"><span data-stu-id="52707-163">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!NOTE]
> - <span data-ttu-id="52707-164">Каждый заполнитель может иметь только один уникальный набор столбцов, от которых он зависит.</span><span class="sxs-lookup"><span data-stu-id="52707-164">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="52707-165">Например, если **Ежегодная зарплата** зависит от **Местонахождение должности** и **Уровень**, невозможно отправить другой набор правил, где **Ежегодная зарплата** является зависимой от другого набора столбцов.</span><span class="sxs-lookup"><span data-stu-id="52707-165">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="52707-166">Можно загрузить примеры наборов правил данных предложений на вкладке **Примеры** на странице **Правила данных в предложении**.</span><span class="sxs-lookup"><span data-stu-id="52707-166">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="52707-167">Когда создатель предложения переопределяет значения, которые рекомендуются правилами данных предложения, предложение помечается как нестандартное и будет обязателен workflow-процесс утверждения.</span><span class="sxs-lookup"><span data-stu-id="52707-167">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="52707-168">Шаблоны документов</span><span class="sxs-lookup"><span data-stu-id="52707-168">Document templates</span></span>

<span data-ttu-id="52707-169">Шаблон документа предложения может помочь администраторам создавать письма с предложениями.</span><span class="sxs-lookup"><span data-stu-id="52707-169">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="52707-170">Шаблон документа предложения представляет собой сочетание текста, который будет частью предложения, а также определенных заполнителей данных предложения.</span><span class="sxs-lookup"><span data-stu-id="52707-170">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="52707-171">Чтобы создать шаблон документа предложения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="52707-171">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="52707-172">Перейдите в **Управление предложением**.</span><span class="sxs-lookup"><span data-stu-id="52707-172">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="52707-173">Разверните раздел **Библиотека** в левой области навигации и перейдите к пункты **Шаблоны**.</span><span class="sxs-lookup"><span data-stu-id="52707-173">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="52707-174">На странице **Шаблоны** будет отображаться список шаблонов документов, которые уже были определены.</span><span class="sxs-lookup"><span data-stu-id="52707-174">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="52707-175">Чтобы создать новый шаблон документа, щелкните **Создать шаблон**.</span><span class="sxs-lookup"><span data-stu-id="52707-175">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="52707-176">Введите уникальное имя для шаблона и щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="52707-176">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="52707-177">С помощью редактора форматированного текста вставьте или отредактируйте содержимое документа предложения.</span><span class="sxs-lookup"><span data-stu-id="52707-177">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="52707-178">Можно вставлять таблицы, изображения и гиперссылки, используя параметры, доступные в верхней части текстового редактора.</span><span class="sxs-lookup"><span data-stu-id="52707-178">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="52707-179">В документе шаблона предложения можно вставить заполнители данных предложения следующими способами:</span><span class="sxs-lookup"><span data-stu-id="52707-179">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="52707-180">Перетаскивание из правой области.</span><span class="sxs-lookup"><span data-stu-id="52707-180">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="52707-181">Вставка хэштега заполнителя данных предложения непосредственно в нужное место.</span><span class="sxs-lookup"><span data-stu-id="52707-181">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="52707-182">Введите **\#**, затем начинайте вводить имя заполнителя данных предложения.</span><span class="sxs-lookup"><span data-stu-id="52707-182">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="52707-183">В раскрывающемся списке отображаются параметры.</span><span class="sxs-lookup"><span data-stu-id="52707-183">Options will appear in the drop-down list.</span></span> <span data-ttu-id="52707-184">Щелкните или нажмите кнопку или клавишу **ВВОД**, чтобы вставить заполнитель данных предложения.</span><span class="sxs-lookup"><span data-stu-id="52707-184">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="52707-185">Чтобы связать заполнитель в шаблон документа предложения, не показывая его значение кандидату, наведите указатель мыши на заполнитель данных предложения и щелкните значок **Прикрепить**.</span><span class="sxs-lookup"><span data-stu-id="52707-185">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="52707-186">В результате заполнитель будет перемещен в раздел **Закрепленные данные предложения** шаблона документа предложения.</span><span class="sxs-lookup"><span data-stu-id="52707-186">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="52707-187">Чтобы отменить закрепление, следуйте тем же инструкциям, но выберите **Отменить закрепление** в списке заполнителей данных предложения.</span><span class="sxs-lookup"><span data-stu-id="52707-187">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="52707-188">Чтобы просмотреть список активных заполнителей данные предложения, переключитесь на вкладку **Активные** в правой области.</span><span class="sxs-lookup"><span data-stu-id="52707-188">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="52707-189">При вставке заполнителя, который обрабатывается набором правил данных предложения, отображаются зависимости этого заполнителя данных предложения от других значений.</span><span class="sxs-lookup"><span data-stu-id="52707-189">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="52707-190">Кроме того, имеется возможность **Импортировать** содержимое из DOCX-файла на локальном компьютере и внести требуемые изменения.</span><span class="sxs-lookup"><span data-stu-id="52707-190">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="52707-191">Таким образом, не нужно вводить все содержимое в редакторе.</span><span class="sxs-lookup"><span data-stu-id="52707-191">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="52707-192">Для предварительного просмотра документа предложения используйте параметр **Предварительный просмотр** в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="52707-192">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="52707-193">Для управления тем, может ли создатель предложения редактировать содержимое документа предложения, используйте параметр **Управление разрешением** в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="52707-193">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="52707-194">Если требуется, чтобы создатель предложения мог только вставлять значения заполнителей, но не редактировать текст, задайте значение разрешения **Нет**.</span><span class="sxs-lookup"><span data-stu-id="52707-194">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="52707-195">Щелкните **Сохранить** для сохранения хода работы.</span><span class="sxs-lookup"><span data-stu-id="52707-195">Click **Save** to save your progress.</span></span> <span data-ttu-id="52707-196">Шаблон будет сохранен в состоянии черновика.</span><span class="sxs-lookup"><span data-stu-id="52707-196">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="52707-197">Чтобы завершить работу и пометить документ как опубликованный, нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="52707-197">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="52707-198">Можно просмотреть, какие шаблоны документов в данный момент активные, в режиме черновика и архивированы и больше не используются в библиотеке шаблонов документов приема сотрудников.</span><span class="sxs-lookup"><span data-stu-id="52707-198">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="52707-199">Можно удалить любой шаблон документа предложения, который не является частью существующего шаблона пакетов предложений.</span><span class="sxs-lookup"><span data-stu-id="52707-199">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="52707-200">Шаблоны пакетов предложений</span><span class="sxs-lookup"><span data-stu-id="52707-200">Offer package templates</span></span>

<span data-ttu-id="52707-201">Пакеты предложений — это артефакты предложений, которые используются совместно с кандидатом и состоят из одного или нескольких шаблонов документов предложения.</span><span class="sxs-lookup"><span data-stu-id="52707-201">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="52707-202">Чтобы создать пакет предложений, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="52707-202">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="52707-203">Перейдите в **Управление предложением**.</span><span class="sxs-lookup"><span data-stu-id="52707-203">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="52707-204">Выберите пункт **Пакеты** на левой навигационной панели.</span><span class="sxs-lookup"><span data-stu-id="52707-204">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="52707-205">Отображается список активных шаблонов пакетов, доступных для использования создателями предложений.</span><span class="sxs-lookup"><span data-stu-id="52707-205">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="52707-206">Чтобы создать новый пакет предложений, щелкните **Создать пакет**.</span><span class="sxs-lookup"><span data-stu-id="52707-206">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="52707-207">Введите уникальное имя и щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="52707-207">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="52707-208">Щелкните **Добавить шаблон**.</span><span class="sxs-lookup"><span data-stu-id="52707-208">Click **Add template**.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="52707-209">Можно создать новый шаблон или выбрать один из существующих.</span><span class="sxs-lookup"><span data-stu-id="52707-209">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="52707-210">Если вы решите добавить существующий шаблон, необходимо убедиться в том, что шаблон документа предложения был сохранен, завершен и помечен как активный.</span><span class="sxs-lookup"><span data-stu-id="52707-210">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="52707-211">Можно выбрать любое требуемое число шаблонов документов.</span><span class="sxs-lookup"><span data-stu-id="52707-211">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="52707-212">Щелкните **Готово**, чтобы вернуться к **Управление пакетами**.</span><span class="sxs-lookup"><span data-stu-id="52707-212">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="52707-213">Можно настроить последовательность документов и также отметить, является ли конкретный документ предложения необходимым при создании предложения.</span><span class="sxs-lookup"><span data-stu-id="52707-213">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="52707-214">Создатель предложения будет иметь возможность удалить документы, которые помечены как **Не требуется**.</span><span class="sxs-lookup"><span data-stu-id="52707-214">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="52707-215">Чтобы сохранить шаблон пакета предложения, чтобы его могли использовать все создатели предложений, щелкните **Сохранить и опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="52707-215">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="52707-216">Для просмотра черновиков шаблонов пакетов предложений перейдите на вкладку **Черновики**. При внесении изменений в шаблон пакета предложения его необходимо сохранить и снова опубликовать.</span><span class="sxs-lookup"><span data-stu-id="52707-216">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="52707-217">Настройка процесса предложения</span><span class="sxs-lookup"><span data-stu-id="52707-217">Configure an offer process</span></span>

<span data-ttu-id="52707-218">Существует несколько частей процесса создания предложения, которые может настраивать администратор Attract.</span><span class="sxs-lookup"><span data-stu-id="52707-218">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="52707-219">**Утверждения предложений.** Выберите, требуется ли утверждать предложения перед отправкой кандидатам.</span><span class="sxs-lookup"><span data-stu-id="52707-219">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="52707-220">Администратор может также решить, должны ли все утверждения выполняться последовательно или в параллельном workflow-процессе утверждения.</span><span class="sxs-lookup"><span data-stu-id="52707-220">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="52707-221">Можно также задать, должны ли лица, утверждающие предложение, добавлять комментарий вместе со своим утверждением предложения.</span><span class="sxs-lookup"><span data-stu-id="52707-221">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="52707-222">Утверждения предложений являются обязательными для всех нестандартных предложений.</span><span class="sxs-lookup"><span data-stu-id="52707-222">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="52707-223">**Параметры предложения для кандидатов.** С правами администратора можно указать, должны ли все предложения иметь дату окончания срока действия, и, если должны, какое смещения по умолчанию для даты окончания срока годности должно быть.</span><span class="sxs-lookup"><span data-stu-id="52707-223">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="52707-224">Можно также настроить, могут ли кандидаты отклонить предложение.</span><span class="sxs-lookup"><span data-stu-id="52707-224">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="52707-225">**Электронные подписи** — -с правами администратора можно также выбрать метод, который кандидаты могут использовать для подписи предложений.</span><span class="sxs-lookup"><span data-stu-id="52707-225">**e-Signatures** - As an administrator, you can also choose the method that candidates can use to sign offers.</span></span>
    - <span data-ttu-id="52707-226">Adobe Sign — все пакеты предложений будут отправляться и подписываться с помощью Adobe Sign.</span><span class="sxs-lookup"><span data-stu-id="52707-226">Adobe Sign - All offer packages will be sent and signed via Adobe Sign.</span></span> <span data-ttu-id="52707-227">Каждый создатель предложений, публикующий предложение, должен иметь учетную запись Adobe Sign, подключенную к Attract.</span><span class="sxs-lookup"><span data-stu-id="52707-227">Each offer creator publishing the offer needs to have their Adobe Sign account connected to Attract.</span></span> <span data-ttu-id="52707-228">Для получения лицензий на Adobe Sign и бесплатной пробной версии перейдите по этой [ссылке](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span><span class="sxs-lookup"><span data-stu-id="52707-228">For Adobe Sign licenses and a free Trial, please visit this [link](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span></span>

    - <span data-ttu-id="52707-229">DocuSign — все пакеты предложений будут отправляться и подписываться с помощью DocuSign.</span><span class="sxs-lookup"><span data-stu-id="52707-229">DocuSign - All offer packages will be sent and signed via DocuSign.</span></span> <span data-ttu-id="52707-230">Каждый создатель предложений, публикующий предложение, должен иметь учетную запись DocuSign, подключенную к Attract.</span><span class="sxs-lookup"><span data-stu-id="52707-230">Each offer creator publishing the offer needs to have their DocuSign account connected to Attract.</span></span> 
    
    - <span data-ttu-id="52707-231">ESign — это параметр по умолчанию, поставляющийся готовым, с которым пользователь может подписывать предложение, вводя свое имя и инициалы.</span><span class="sxs-lookup"><span data-stu-id="52707-231">ESign - This is the default option, provided out of the box, where the user can sign an offer by typing their name and initials.</span></span>


<span data-ttu-id="52707-232">Дополнительные сведения о процессе создания предложения см. в разделе [Создание, утверждение и подписание предложений](./creating-offers.md).</span><span class="sxs-lookup"><span data-stu-id="52707-232">To learn more about the offer creation process, see [Create, approve, and sign offers](./creating-offers.md).</span></span>
