---
title: Сведения о полях даты и времени
description: Узнайте, что следует ожидать при использовании полей даты и времени в Microsoft Dynamics 365 Human Resources. Узнайте, что следует ожидать при взаимодействии с данными даты и времени в форме в Human Resources, во внешнем источнике или в Common Data Service.
author: Darinkramer
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9dd80415f33a4d671bdc2662704799775daad177
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010300"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="574c5-104">Сведения о полях даты и времени</span><span class="sxs-lookup"><span data-stu-id="574c5-104">Understand Date and Time fields</span></span>

<span data-ttu-id="574c5-105">Поля **Дата и время** являются фундаментальным понятием в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="574c5-105">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="574c5-106">Важно понимать, как работать с данными **Дата и время** в формах Dynamics 365 Human Resources, Common Data Service и во внешних источниках.</span><span class="sxs-lookup"><span data-stu-id="574c5-106">It's important to understand how to work with **Date and Time** data in Dynamics 365 Human Resources forms, Common Data Service, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="574c5-107">Общее представление о разнице между типами данных полей "Дата" и "Дата и время"</span><span class="sxs-lookup"><span data-stu-id="574c5-107">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="574c5-108">Поля **Дата и время** содержатся сведения о часовом поясе, а поля **Дата** — не содержат.</span><span class="sxs-lookup"><span data-stu-id="574c5-108">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="574c5-109">В полях **Дата** отображается одна и та же информация в любом местонахождении.</span><span class="sxs-lookup"><span data-stu-id="574c5-109">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="574c5-110">При вводе даты в поле **Дата** Human Resources записывают эту же дату в базу данных.</span><span class="sxs-lookup"><span data-stu-id="574c5-110">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="574c5-111">При отображении данных в поле **Дата и время** Human Resources корректирует дату и время на основе часового пояса, заданного в форме **Параметры пользователя** (**Общие > Настройка > Параметры пользователя**).</span><span class="sxs-lookup"><span data-stu-id="574c5-111">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="574c5-112">Сведения о дате и времени, вводимые в поле, могут не совпадать со сведениями, записанными в базу данных.</span><span class="sxs-lookup"><span data-stu-id="574c5-112">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="574c5-113">[![Форма "Параметры пользователя"](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="574c5-113">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="574c5-114">Общие сведения о полях даты и времени в формах</span><span class="sxs-lookup"><span data-stu-id="574c5-114">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="574c5-115">При вводе данных в поле **Дата и время** отображаемые на экране данные не будут совпадать с данными, хранящимися в базе данных, если часовой пояс пользователя не установлен в значение времени в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="574c5-115">When entering data in a **Date and Time** field, the data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="574c5-116">Данные в полях **Дата и время** всегда хранятся в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="574c5-116">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="574c5-117">[![Форма работника](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="574c5-117">[![Worker form](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="574c5-118">Общие сведения о полях даты и времени в базе данных</span><span class="sxs-lookup"><span data-stu-id="574c5-118">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="574c5-119">Когда Human Resources записывает значение **Дата и время** в базу данных, он сохраняет данные в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="574c5-119">When Human Resources writes a **Date and time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="574c5-120">Это позволяет пользователям просматривать любые данные **Дата и время** относительно часового пояса, определенного в параметрах пользователя.</span><span class="sxs-lookup"><span data-stu-id="574c5-120">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="574c5-121">В приведенном выше примере время начала — это момент времени, а не конкретная дата.</span><span class="sxs-lookup"><span data-stu-id="574c5-121">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="574c5-122">При изменении часового пояса зарегистрированного пользователя с GMT +12:00 на GMT UTC та же самая созданная запись отображает 30.04.2019 12:00:00 вместо 01.05.2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="574c5-122">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record just created shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="574c5-123">В приведенном ниже примере занятость сотрудника 000724 становится активной в то же время, независимо от часового пояса.</span><span class="sxs-lookup"><span data-stu-id="574c5-123">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="574c5-124">Сотрудник будет активным 30.04.2019 в часовом поясе GMT, что совпадает с 01.05.2019 в часовом поясе GMT+12:00.</span><span class="sxs-lookup"><span data-stu-id="574c5-124">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="574c5-125">Они ссылаются на один и тот же момент времени, а не на конкретную дату.</span><span class="sxs-lookup"><span data-stu-id="574c5-125">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="574c5-126">[![Форма работника](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="574c5-126">[![Worker form](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a><span data-ttu-id="574c5-127">Данные даты и времени в платформе управления данными, Excel, Common Data Service и Power BI</span><span class="sxs-lookup"><span data-stu-id="574c5-127">Date and Time data in Data Management Framework, Excel, Common Data Service, and Power BI</span></span> 

<span data-ttu-id="574c5-128">Отчеты платформы управления данными, надстройки Excel, Common Data Service и Power BI все предназначены для непосредственного взаимодействия с данными на уровне базы данных.</span><span class="sxs-lookup"><span data-stu-id="574c5-128">The Data Management Framework, Excel Add-In, Common Data Service, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="574c5-129">Так как нет клиента для корректировки данных **Дата и время** в соответствии с часовым поясом пользователя, все значения **Дата и время** заданы в формате UTC, что может привести к некоторым неправильным допущениям при вводе или просмотре данных.</span><span class="sxs-lookup"><span data-stu-id="574c5-129">Since there is no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="574c5-130">База данных предполагают, что данные **Дата и время**, которые передаются через DMF, Excel или Common Data Service, введены в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="574c5-130">**Date and Time** data that is submitted via DMF, Excel, or Common Data Service is assumed to be in UTC by the database.</span></span> <span data-ttu-id="574c5-131">Это может привести к путанице, когда введенное значение **Дата и время** не отображается ожидаемым образом, поскольку у пользователя, просматривающего данные, не задан часовой пояс UTC.</span><span class="sxs-lookup"><span data-stu-id="574c5-131">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="574c5-132">То же самое происходит в обратную сторону при экспорте данных.</span><span class="sxs-lookup"><span data-stu-id="574c5-132">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="574c5-133">Данные **Дата и время** в экспортированном объекте DMF могут отличаться при отображении в клиенте Dynamics.</span><span class="sxs-lookup"><span data-stu-id="574c5-133">The **Date and Time** data in the exported DMF entity can be different then what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="574c5-134">При использовании внешних источников, таких как DMF, для просмотра или разработки данных, важно помнить, что значения **Дата и время** по умолчанию учитываются в формате UTC, независимо от часового пояса компьютера пользователя или настроек часового пояса текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="574c5-134">When using external sources like DMF to view or author data, it is important to keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="574c5-135">Примеры одной и той же записи, отображаемой в разных областях продукта</span><span class="sxs-lookup"><span data-stu-id="574c5-135">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="574c5-136">**Human Resources, когда установлен часовой пояс пользователя UTC**</span><span class="sxs-lookup"><span data-stu-id="574c5-136">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="574c5-137">[![Форма работника](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="574c5-137">[![Worker form](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="574c5-138">**Human Resources, когда установлен часовой пояс пользователя GMT +12:00**</span><span class="sxs-lookup"><span data-stu-id="574c5-138">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="574c5-139">[![Форма работника](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="574c5-139">[![Worker form](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="574c5-140">**Excel через OData**</span><span class="sxs-lookup"><span data-stu-id="574c5-140">**Excel Via OData**</span></span>

<span data-ttu-id="574c5-141">[![Excel через OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="574c5-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="574c5-142">**Промежуточное хранение DMF**</span><span class="sxs-lookup"><span data-stu-id="574c5-142">**DMF Staging**</span></span>

<span data-ttu-id="574c5-143">[![Промежуточное хранение DMF](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="574c5-143">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="574c5-144">**Экспорт DMF**</span><span class="sxs-lookup"><span data-stu-id="574c5-144">**DMF Export**</span></span>

<span data-ttu-id="574c5-145">[![Промежуточное хранение DMF](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="574c5-145">[![DMF Staging](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="574c5-146">**Excel через Common Data Service**</span><span class="sxs-lookup"><span data-stu-id="574c5-146">**Excel via Common Data Service**</span></span>

<span data-ttu-id="574c5-147">[![Excel через Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="574c5-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="574c5-148">См. также</span><span class="sxs-lookup"><span data-stu-id="574c5-148">See also</span></span>

[<span data-ttu-id="574c5-149">Данные "Дата и время"</span><span class="sxs-lookup"><span data-stu-id="574c5-149">Date and time data</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="574c5-150">Предпочтительные часовые пояса пользователя</span><span class="sxs-lookup"><span data-stu-id="574c5-150">User preferred time zones</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
