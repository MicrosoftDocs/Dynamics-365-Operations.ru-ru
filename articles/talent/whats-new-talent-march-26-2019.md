---
title: Что нового и что изменилось в Dynamics 365 for Talent (26 марта 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-26
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 568a16a17ed3269c7b72f27f0d4b7bbdbd56630e
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/12/2019
ms.locfileid: "949836"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-26-2019"></a><span data-ttu-id="d1bad-103">Что нового и что изменилось в Dynamics 365 for Talent (26 марта 2019 г.)</span><span class="sxs-lookup"><span data-stu-id="d1bad-103">What's new or changed in Dynamics 365 for Talent (March 26, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d1bad-104">В этой теме описываются новые и измененные компоненты Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="d1bad-104">This topic describes features that are either new or changed in Dynamics 365 for Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="d1bad-105">Изменения в Attract</span><span class="sxs-lookup"><span data-stu-id="d1bad-105">Changes in Attract</span></span>

### <a name="enhancements-to-interview-scheduling"></a><span data-ttu-id="d1bad-106">Улучшения планирования собеседований</span><span class="sxs-lookup"><span data-stu-id="d1bad-106">Enhancements to interview scheduling</span></span>
<span data-ttu-id="d1bad-107">При планировании собеседований доступны следующие улучшения.</span><span class="sxs-lookup"><span data-stu-id="d1bad-107">The following enhancements are available in interview scheduling.</span></span>

- <span data-ttu-id="d1bad-108">Агенты или менеджеры по найму теперь могут вручную напомнить сотруднику, проводящему собеседование, о необходимости отправить отзыв.</span><span class="sxs-lookup"><span data-stu-id="d1bad-108">Recruiters or hiring managers can now manually trigger a reminder for an interviewer to submit their feedback.</span></span> <span data-ttu-id="d1bad-109">Связанный шаблон электронной почты для напоминания также можно настроить.</span><span class="sxs-lookup"><span data-stu-id="d1bad-109">The associated email template for the reminder is configurable as well.</span></span>
- <span data-ttu-id="d1bad-110">При совместном доступе к сводке собеседования с кандидатом планировщик собеседования может решить скрыть имена сотрудников, проводивших собеседование, а также скрыть строки из представления сводки собеседования.</span><span class="sxs-lookup"><span data-stu-id="d1bad-110">While sharing the interview summary with the candidate, the interview scheduler can choose to hide the names of the interviewers and also choose to hide rows from the interview summary view.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="d1bad-111">Изменения в Onboard</span><span class="sxs-lookup"><span data-stu-id="d1bad-111">Changes in Onboard</span></span>

### <a name="embedded-images-in-activities"></a><span data-ttu-id="d1bad-112">Внедренные изображения в мероприятиях</span><span class="sxs-lookup"><span data-stu-id="d1bad-112">Embedded images in activities</span></span>
<span data-ttu-id="d1bad-113">Теперь можно внедрять изображения непосредственно в действия.</span><span class="sxs-lookup"><span data-stu-id="d1bad-113">You can now embed images directly into activities.</span></span> <span data-ttu-id="d1bad-114">В дополнение к возможности копирования и вставки изображений из Интернета, можно загрузить изображения из локальной файловой системы.</span><span class="sxs-lookup"><span data-stu-id="d1bad-114">In addition to being able to copy and paste images from the web, you can upload images from your local file system.</span></span> <span data-ttu-id="d1bad-115">Размер действия ограничивается 1 МБ.</span><span class="sxs-lookup"><span data-stu-id="d1bad-115">The size of the activity is limited to 1 MB.</span></span> <span data-ttu-id="d1bad-116">Если изображение слишком велико, измените его размер и повторите отправку.</span><span class="sxs-lookup"><span data-stu-id="d1bad-116">If the image is too large, resize and try to upload again.</span></span>

<span data-ttu-id="d1bad-117">[![Сопоставление](./media/embedimages.png)](./media/embedimages.png)</span><span class="sxs-lookup"><span data-stu-id="d1bad-117">[![Mapping](./media/embedimages.png)](./media/embedimages.png)</span></span>

<span data-ttu-id="d1bad-118">Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="d1bad-118">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="d1bad-119">Изменения в Core HR</span><span class="sxs-lookup"><span data-stu-id="d1bad-119">Changes in Core HR</span></span>
<span data-ttu-id="d1bad-120">**Сборка 8.1.2210**</span><span class="sxs-lookup"><span data-stu-id="d1bad-120">**Build 8.1.2210**</span></span>

### <a name="custom-field-support-available-for-select-entities-in-common-data-service"></a><span data-ttu-id="d1bad-121">Доступна поддержка настраиваемых полей для некоторых объектов в Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d1bad-121">Custom field support available for select entities in Common Data Service</span></span> 

<span data-ttu-id="d1bad-122">Следующие объекты Common Data Service теперь поддерживают пользовательские поля, созданные в Dynamics 365 for Talent:</span><span class="sxs-lookup"><span data-stu-id="d1bad-122">The following Common Data Service entities now support customer fields created in Dynamics 365 for Talent:</span></span>

- <span data-ttu-id="d1bad-123">Рабочий</span><span class="sxs-lookup"><span data-stu-id="d1bad-123">Worker</span></span>
- <span data-ttu-id="d1bad-124">Этническое происхождение</span><span class="sxs-lookup"><span data-stu-id="d1bad-124">Ethnic origin</span></span>
- <span data-ttu-id="d1bad-125">Статус ветерана</span><span class="sxs-lookup"><span data-stu-id="d1bad-125">Veteran status</span></span>
- <span data-ttu-id="d1bad-126">Код языка</span><span class="sxs-lookup"><span data-stu-id="d1bad-126">Language code</span></span>
- <span data-ttu-id="d1bad-127">Должность</span><span class="sxs-lookup"><span data-stu-id="d1bad-127">Job</span></span>
- <span data-ttu-id="d1bad-128">Тип вакансии</span><span class="sxs-lookup"><span data-stu-id="d1bad-128">Job type</span></span>
- <span data-ttu-id="d1bad-129">Должностные функции</span><span class="sxs-lookup"><span data-stu-id="d1bad-129">Job function</span></span>
- <span data-ttu-id="d1bad-130">Занимаемая должность</span><span class="sxs-lookup"><span data-stu-id="d1bad-130">Position</span></span>
- <span data-ttu-id="d1bad-131">Тип позиции</span><span class="sxs-lookup"><span data-stu-id="d1bad-131">Position type</span></span>
 
### <a name="employment-history-not-displayed-chronologically"></a><span data-ttu-id="d1bad-132">История занятости не отображается в хронологическом порядке</span><span class="sxs-lookup"><span data-stu-id="d1bad-132">Employment history not displayed chronologically</span></span>
<span data-ttu-id="d1bad-133">После этого изменения на странице истории занятости теперь записи трудоустройства отображаются в хронологическом порядке, независимо от компании.</span><span class="sxs-lookup"><span data-stu-id="d1bad-133">With this change, the employment history page now displays employment records chronologically, independent of company.</span></span> <span data-ttu-id="d1bad-134">Также можно использовать параметры сортировки для сортировки по компаниям.</span><span class="sxs-lookup"><span data-stu-id="d1bad-134">You can also use sorting options to sort by company.</span></span>

### <a name="fixed-compensation-plans-dont-appear-when-restricting-user-by-company-in-security"></a><span data-ttu-id="d1bad-135">Планы фиксированной компенсации не отображаются при ограничении пользователя по компании в системе безопасности.</span><span class="sxs-lookup"><span data-stu-id="d1bad-135">Fixed compensation plans don't appear when restricting user by company in security.</span></span>
<span data-ttu-id="d1bad-136">В этом выпуске планы фиксированной компенсации теперь отображаются при ограничении пользователей по компаниям в системе безопасности.</span><span class="sxs-lookup"><span data-stu-id="d1bad-136">In this release, fixed compensation plans now appear when restricting users by company in security.</span></span> <span data-ttu-id="d1bad-137">Все параметры безопасности будут учитываться, а планы фиксированной компенсации отображаются для тех компаний, для которых у пользователя имеется разрешение на доступ.</span><span class="sxs-lookup"><span data-stu-id="d1bad-137">All security settings will be honored, and fixed plans will appear for those companies the user has permissions to access.</span></span> 

### <a name="cant-delete-job-records-using-open-in-excel-option-in-talent"></a><span data-ttu-id="d1bad-138">Не удается удалить записи должности с помощью пункта "Открыть в Excel" в Talent</span><span class="sxs-lookup"><span data-stu-id="d1bad-138">Can't delete Job records using Open in Excel option in Talent</span></span>
<span data-ttu-id="d1bad-139">В этом выпуске появилась возможность удалять записи вакансии с помощью пункта **Открыть в Excel** в Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="d1bad-139">With this release, you can now remove job records by using the **Open in Excel** option in Dynamics 365 for Talent.</span></span>

### <a name="upgrade-to-common-data-service"></a><span data-ttu-id="d1bad-140">Обновление до Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d1bad-140">Upgrade to Common Data Service</span></span>
<span data-ttu-id="d1bad-141">Крайние сроки для обновления до Common Data Service быстро приближаются.</span><span class="sxs-lookup"><span data-stu-id="d1bad-141">Deadlines to upgrade to Common Data Service are quickly approaching.</span></span> <span data-ttu-id="d1bad-142">Войдите в центр администрирования PowerApps для определения, необходимо ли обновить вашу базу данных.</span><span class="sxs-lookup"><span data-stu-id="d1bad-142">Sign in to the PowerApps Admin center to determine if your database needs to be upgraded.</span></span> <span data-ttu-id="d1bad-143">Дополнительные сведения о крайних сроках и необходимых действиях по обновлению см. в разделе [Обновление до Common Data Service](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).</span><span class="sxs-lookup"><span data-stu-id="d1bad-143">For more information about deadlines and necessary steps to upgrade, see [Upgrade to Common Data Service](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

## <a name="in-preview"></a><span data-ttu-id="d1bad-144">В режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="d1bad-144">In preview</span></span>

<span data-ttu-id="d1bad-145">Сведения о включении предварительных версий функций см. в разделе [Доступ к функциям предварительного просмотра в Talent](./access-preview-feature.md).</span><span class="sxs-lookup"><span data-stu-id="d1bad-145">For information about enabling preview features, see [Access preview features in Talent](./access-preview-feature.md).</span></span>

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a><span data-ttu-id="d1bad-146">Разрешить указывать коды причины для типов отпусков</span><span class="sxs-lookup"><span data-stu-id="d1bad-146">Allow reason codes to be specified on leave types</span></span>
<span data-ttu-id="d1bad-147">Организациям могут потребоваться дополнительные сведения, относящиеся к запросам выходных.</span><span class="sxs-lookup"><span data-stu-id="d1bad-147">Organizations might need additional information related to time off requests.</span></span> <span data-ttu-id="d1bad-148">Для получения этой информации сотрудникам необходимо включить код причины в их запросы выходных.</span><span class="sxs-lookup"><span data-stu-id="d1bad-148">To get this information, employees need to include a reason code on their time off requests.</span></span> <span data-ttu-id="d1bad-149">В этом выпуске теперь можно задать коды причин, связанные с определенным типом отпуска, и дать рабочим возможность выбрать код причины в их запросе выходных.</span><span class="sxs-lookup"><span data-stu-id="d1bad-149">With this release, you can now specify the reason codes associated with a given leave type and enable employees to select a reason code on their time off requests.</span></span>

### <a name="configure-reason-codes-to-be-required-when-submitting-time-off-for-certain-leave-types"></a><span data-ttu-id="d1bad-150">Настройка кодов причин, чтобы они были обязательными при подаче запроса выходных для определенных типов отпусков</span><span class="sxs-lookup"><span data-stu-id="d1bad-150">Configure reason codes to be required when submitting time off for certain leave types</span></span>
<span data-ttu-id="d1bad-151">Организации могут требовать, чтобы для определенных типов отпусков были заданы коды причины, когда сотрудники отправляют запрос выходных.</span><span class="sxs-lookup"><span data-stu-id="d1bad-151">Organizations might require reason codes to be set on specific leave types when employees submit time off.</span></span> <span data-ttu-id="d1bad-152">Это может потребоваться на основе нормативных требований в стране или регионе или на основе политики компании.</span><span class="sxs-lookup"><span data-stu-id="d1bad-152">This may be required based on a regulatory requirement in their country/region or a company policy.</span></span> <span data-ttu-id="d1bad-153">Этот выпуск обеспечивает возможность для отдела кадров указать, какие типы отпусков требуют код причины.</span><span class="sxs-lookup"><span data-stu-id="d1bad-153">This release provides the ability for HR to specify which leave types require a reason code.</span></span> <span data-ttu-id="d1bad-154">Это обеспечивает, когда сотрудники отправляют запросы отгулов, в которых отпуск требует кода причины.</span><span class="sxs-lookup"><span data-stu-id="d1bad-154">This will be enforced when employees submit time off requests where the leave requires a reason code.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="d1bad-155">Скоро</span><span class="sxs-lookup"><span data-stu-id="d1bad-155">Coming soon</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="d1bad-156">Расширенная безопасность компенсации (фиксированной и переменной)</span><span class="sxs-lookup"><span data-stu-id="d1bad-156">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="d1bad-157">Во многих организациях менеджеры по компенсации и льготам могут иметь доступ только к определенным записям компенсаций.</span><span class="sxs-lookup"><span data-stu-id="d1bad-157">In many organizations, compensation and benefits managers might only have access to certain compensation records.</span></span> <span data-ttu-id="d1bad-158">Они могут быть для руководителей или региональных сотрудников.</span><span class="sxs-lookup"><span data-stu-id="d1bad-158">These could be for executives or regional employees.</span></span> <span data-ttu-id="d1bad-159">С этим изменением отдел кадров можете управлять и обслуживать планы компенсации для различных групп сотрудников в организации.</span><span class="sxs-lookup"><span data-stu-id="d1bad-159">With this change, HR can manage and maintain the compensation plans for different employee groups in the organization.</span></span> <span data-ttu-id="d1bad-160">Можно назначить роли безопасности фиксированным и переменным планам, которые будут определять доступ к этим планам и данным о сотрудниках, относящихся к планам, таким как записи сведений о зарплате и премиях.</span><span class="sxs-lookup"><span data-stu-id="d1bad-160">You can assign security roles to fixed and variable plans that determine access to the plans and the employee data related to the plans, such as salary or bonus records.</span></span> <span data-ttu-id="d1bad-161">Только роли, которым предоставлен доступ, могут обработать компенсацию для этих сотрудников.</span><span class="sxs-lookup"><span data-stu-id="d1bad-161">Only the roles granted with access can process compensation for these employees.</span></span>

###  <a name="email-support-for-alerts"></a><span data-ttu-id="d1bad-162">Поддержка по электронной почте для оповещений</span><span class="sxs-lookup"><span data-stu-id="d1bad-162">Email support for alerts</span></span>
<span data-ttu-id="d1bad-163">С обновлением платформы Platform update 25 пользователи могут создавать правила оповещений, которые автоматически отправляют уведомления по электронной почте контактам при наступлении события.</span><span class="sxs-lookup"><span data-stu-id="d1bad-163">With Platform update 25, users can create alert rules that automatically dispatch email notifications to contacts when triggered by an event.</span></span> 

### <a name="duplicate-employee-checks-user-interface-changes"></a><span data-ttu-id="d1bad-164">Проверки дублирования сотрудника: изменения интерфейса пользователя</span><span class="sxs-lookup"><span data-stu-id="d1bad-164">Duplicate employee checks: User interface changes</span></span>
<span data-ttu-id="d1bad-165">После этого изменения дубликаты определяются по мере ввода полей имени, и статус отображает число обнаруженных дубликатов.</span><span class="sxs-lookup"><span data-stu-id="d1bad-165">With this change, duplicates are detected as you enter name fields, and a status displays the number of duplicates found.</span></span> <span data-ttu-id="d1bad-166">Можно выбрать предоставленную ссылку, чтобы открыть новую страницу для оценки, следует ли использовать обнаруженное соответствие.</span><span class="sxs-lookup"><span data-stu-id="d1bad-166">You can select the provided link to open a new page to evaluate whether to use the detected match.</span></span> <span data-ttu-id="d1bad-167">Во избежание прерывания ввода данных форма дубликатов не открывается автоматически.</span><span class="sxs-lookup"><span data-stu-id="d1bad-167">To avoid interrupting data entry, the duplicates form doesn't open automatically.</span></span>
