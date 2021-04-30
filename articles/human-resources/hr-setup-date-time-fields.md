---
title: Сведения о полях даты и времени
description: Узнайте, что следует ожидать при использовании полей даты и времени в Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3a8bc27bb4560b4a15aef483ff465c4b943bf02b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889892"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="0af20-103">Сведения о полях даты и времени</span><span class="sxs-lookup"><span data-stu-id="0af20-103">Understand Date and Time fields</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0af20-104">Поля **Дата и время** являются фундаментальным понятием в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0af20-104">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0af20-105">Важно понимать, как работать с данными **Дата и время** в формах, Dataverse и во внешних источниках.</span><span class="sxs-lookup"><span data-stu-id="0af20-105">It's important to understand how to work with **Date and Time** data in forms, Dataverse, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="0af20-106">Общее представление о разнице между типами данных полей "Дата" и "Дата и время"</span><span class="sxs-lookup"><span data-stu-id="0af20-106">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="0af20-107">Поля **Дата и время** содержатся сведения о часовом поясе, а поля **Дата** — не содержат.</span><span class="sxs-lookup"><span data-stu-id="0af20-107">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="0af20-108">В полях **Дата** отображается одна и та же информация в любом местонахождении.</span><span class="sxs-lookup"><span data-stu-id="0af20-108">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="0af20-109">При вводе даты в поле **Дата** Human Resources записывают эту же дату в базу данных.</span><span class="sxs-lookup"><span data-stu-id="0af20-109">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="0af20-110">При отображении данных в поле **Дата и время** Human Resources корректирует дату и время на основе часового пояса, заданного в форме **Параметры пользователя** (**Общие > Настройка > Параметры пользователя**).</span><span class="sxs-lookup"><span data-stu-id="0af20-110">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="0af20-111">Сведения о дате и времени, вводимые в поле, могут не совпадать со сведениями, записанными в базу данных.</span><span class="sxs-lookup"><span data-stu-id="0af20-111">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="0af20-112">[![Форма "Параметры пользователя"](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="0af20-112">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="0af20-113">Общие сведения о полях даты и времени в формах</span><span class="sxs-lookup"><span data-stu-id="0af20-113">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="0af20-114">Данные **Дата и время**, отображаемые на экране, не будут совпадать с данными, хранящимися в базе данных, если часовой пояс пользователя не установлен в значение времени в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="0af20-114">**Date and Time** data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="0af20-115">Данные в полях **Дата и время** всегда хранятся в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="0af20-115">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="0af20-116">[![Время в формате UTC формы работника](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="0af20-116">[![Worker form UTC](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="0af20-117">Общие сведения о полях даты и времени в базе данных</span><span class="sxs-lookup"><span data-stu-id="0af20-117">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="0af20-118">Когда Human Resources записывает значение **Дата и время** в базу данных, он сохраняет данные в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="0af20-118">When Human Resources writes a **Date and Time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="0af20-119">Это позволяет пользователям просматривать любые данные **Дата и время** относительно часового пояса, определенного в параметрах пользователя.</span><span class="sxs-lookup"><span data-stu-id="0af20-119">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="0af20-120">В приведенном выше примере время начала — это момент времени, а не конкретная дата.</span><span class="sxs-lookup"><span data-stu-id="0af20-120">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="0af20-121">При изменении часового пояса зарегистрированного пользователя с GMT +12:00 на GMT UTC та же самая запись отображает 30.04.2019 12:00:00 вместо 01.05.2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="0af20-121">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="0af20-122">В приведенном ниже примере занятость сотрудника 000724 становится активной в то же время, независимо от часового пояса.</span><span class="sxs-lookup"><span data-stu-id="0af20-122">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="0af20-123">Сотрудник будет активным 30.04.2019 в часовом поясе GMT, что совпадает с 01.05.2019 в часовом поясе GMT+12:00.</span><span class="sxs-lookup"><span data-stu-id="0af20-123">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="0af20-124">Они ссылаются на один и тот же момент времени, а не на конкретную дату.</span><span class="sxs-lookup"><span data-stu-id="0af20-124">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="0af20-125">[![Время в формате GMT формы работника](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="0af20-125">[![Worker form GMT](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a><span data-ttu-id="0af20-126">Данные даты и времени в платформе управления данными, Excel, Dataverse и Power BI</span><span class="sxs-lookup"><span data-stu-id="0af20-126">Date and Time data in Data Management Framework, Excel, Dataverse, and Power BI</span></span> 

<span data-ttu-id="0af20-127">Отчеты платформы управления данными, надстройки Excel, Dataverse и Power BI все предназначены для непосредственного взаимодействия с данными на уровне базы данных.</span><span class="sxs-lookup"><span data-stu-id="0af20-127">The Data Management Framework, Excel Add-In, Dataverse, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="0af20-128">Так как нет клиента для корректировки данных **Дата и время** в соответствии с часовым поясом пользователя, все значения **Дата и время** заданы в формате UTC, что может привести к некоторым неправильным допущениям при вводе или просмотре данных.</span><span class="sxs-lookup"><span data-stu-id="0af20-128">Since there's no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="0af20-129">База данных предполагают, что данные **Дата и время**, которые передаются через DMF, Excel или Dataverse, введены в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="0af20-129">**Date and Time** data submitted via DMF, Excel, or Dataverse is assumed to be in UTC by the database.</span></span> <span data-ttu-id="0af20-130">Это может привести к путанице, когда введенное значение **Дата и время** не отображается ожидаемым образом, поскольку у пользователя, просматривающего данные, не задан часовой пояс UTC.</span><span class="sxs-lookup"><span data-stu-id="0af20-130">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="0af20-131">То же самое происходит в обратную сторону при экспорте данных.</span><span class="sxs-lookup"><span data-stu-id="0af20-131">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="0af20-132">Данные **Дата и время** в экспортированном объекте DMF могут отличаться при отображении в клиенте Dynamics.</span><span class="sxs-lookup"><span data-stu-id="0af20-132">The **Date and Time** data in the exported DMF entity can be different than what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="0af20-133">При использовании внешних источников, таких как DMF, для просмотра или разработки данных помните, что значения **Дата и время** по умолчанию учитываются в формате UTC, независимо от часового пояса компьютера пользователя или настроек часового пояса текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="0af20-133">When using external sources like DMF to view or author data, keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="0af20-134">Примеры одной и той же записи, отображаемой в разных областях продукта</span><span class="sxs-lookup"><span data-stu-id="0af20-134">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="0af20-135">**Human Resources, когда установлен часовой пояс пользователя UTC**</span><span class="sxs-lookup"><span data-stu-id="0af20-135">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="0af20-136">[![Форма сотрудника, заданная для времени в формате UTC](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="0af20-136">[![Worker form set to UTC](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="0af20-137">**Human Resources, когда установлен часовой пояс пользователя GMT +12:00**</span><span class="sxs-lookup"><span data-stu-id="0af20-137">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="0af20-138">[![Форма сотрудника, заданная для времени в формате GMT](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="0af20-138">[![Worker form set to GMT](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="0af20-139">**Excel через OData**</span><span class="sxs-lookup"><span data-stu-id="0af20-139">**Excel Via OData**</span></span>

<span data-ttu-id="0af20-140">[![Excel через OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="0af20-140">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="0af20-141">**Промежуточное хранение DMF**</span><span class="sxs-lookup"><span data-stu-id="0af20-141">**DMF Staging**</span></span>

<span data-ttu-id="0af20-142">[![Промежуточное хранение DMF](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="0af20-142">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="0af20-143">**Экспорт DMF**</span><span class="sxs-lookup"><span data-stu-id="0af20-143">**DMF Export**</span></span>

<span data-ttu-id="0af20-144">[![Экспорт DMF](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="0af20-144">[![DMF Export](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="0af20-145">**Excel через Dataverse**</span><span class="sxs-lookup"><span data-stu-id="0af20-145">**Excel via Dataverse**</span></span>

<span data-ttu-id="0af20-146">[![Excel через Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="0af20-146">[![Excel via Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="0af20-147">См. также</span><span class="sxs-lookup"><span data-stu-id="0af20-147">See also</span></span>

[<span data-ttu-id="0af20-148">Данные "Дата и время"</span><span class="sxs-lookup"><span data-stu-id="0af20-148">Date and time data</span></span>](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="0af20-149">Предпочтительные часовые пояса пользователя</span><span class="sxs-lookup"><span data-stu-id="0af20-149">User preferred time zones</span></span>](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]