---
title: Что нового и что изменилось в Dynamics 365 Talent — Core HR (31 октября 2018 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
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
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4851c62a19bb562c7f5f578aecbae99cfcdb982f
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897381"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-31-2018"></a><span data-ttu-id="ee192-103">Что нового и что изменилось в Dynamics 365 Talent — Core HR (31 октября 2018 г.)</span><span class="sxs-lookup"><span data-stu-id="ee192-103">What's new or changed in Dynamics 365 Talent - Core HR (October 31, 2018)</span></span>

<span data-ttu-id="ee192-104">**Сборка 8.1.2031**</span><span class="sxs-lookup"><span data-stu-id="ee192-104">**Build 8.1.2031**</span></span>

<span data-ttu-id="ee192-105">В этой теме описываются новые и измененные компоненты Core HR.</span><span class="sxs-lookup"><span data-stu-id="ee192-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="create-links-from-talent-to-finance"></a><span data-ttu-id="ee192-106">Создание ссылок из Talent в Finance</span><span class="sxs-lookup"><span data-stu-id="ee192-106">Create links from Talent to Finance</span></span>
<span data-ttu-id="ee192-107">Эта новая возможность переходов позволяет создавать ссылки из Talent в Finance, что обеспечит прямые переходы на страницы Finance.</span><span class="sxs-lookup"><span data-stu-id="ee192-107">This new navigation functionality allows you to link from Talent to Finance, giving you direct navigation into Finance pages.</span></span> <span data-ttu-id="ee192-108">Когда ссылки настроены, можно указать имя и группу ссылки, место появления ссылки в Talent и целевую страницу, которая должна открываться в Finance.</span><span class="sxs-lookup"><span data-stu-id="ee192-108">When links are configured, you can specify the name and group of the link, where the link should surface in Talent, and the target page to be opened within Finance.</span></span>

#### <a name="coming-soon"></a><span data-ttu-id="ee192-109">Скоро</span><span class="sxs-lookup"><span data-stu-id="ee192-109">Coming soon</span></span>
<span data-ttu-id="ee192-110">Контекст поля будет добавлен в будущем, чтобы обеспечить прямой переход к соответствующим записям в Finance.</span><span class="sxs-lookup"><span data-stu-id="ee192-110">Field context will be added in the future to allow for direct navigation to corresponding records in Finance.</span></span> <span data-ttu-id="ee192-111">Например, можно использовать **Ссылка на поле** для предоставления контекста для перехода непосредственно к конкретному сотруднику или должности в Finance.</span><span class="sxs-lookup"><span data-stu-id="ee192-111">For example, you can use **Link to field** to provide the context to navigate directly to a specific employee or position in Finance.</span></span>

### <a name="configure-target-systems"></a><span data-ttu-id="ee192-112">Настройка целевых систем</span><span class="sxs-lookup"><span data-stu-id="ee192-112">Configure target systems</span></span>

<span data-ttu-id="ee192-113">В Talent системные администраторы могут определять ссылки, которые будут отображаться с помощью рабочей области администрирования системы.</span><span class="sxs-lookup"><span data-stu-id="ee192-113">In Talent, system administrators can define links that will be surfaced through the System Administration workspace.</span></span> <span data-ttu-id="ee192-114">Частью конфигурация являются среды Finance, в которые вы хотите переходить в качестве "цели" ссылки.</span><span class="sxs-lookup"><span data-stu-id="ee192-114">Part of the configuration is the Finance environments that you would like to navigate to as the "target" of the link.</span></span> <span data-ttu-id="ee192-115">Это можно сделать, присвоив целевой системе имя и указав URL-адрес среды Finance.</span><span class="sxs-lookup"><span data-stu-id="ee192-115">You do this by giving the target system a name and providing the URL of the Finance environment.</span></span> <span data-ttu-id="ee192-116">Ниже приведен пример URL-адреса Finance, который мог бы быть предоставлен: https://devax00124aos.cloud.test.dynamics.com/.</span><span class="sxs-lookup"><span data-stu-id="ee192-116">Here is an example of a Finance URL that you would provide: https://devax00124aos.cloud.test.dynamics.com/.</span></span> <span data-ttu-id="ee192-117">После настройки ваших целевых систем можно определить ссылки.</span><span class="sxs-lookup"><span data-stu-id="ee192-117">After you have configured your target systems,  you can define your links.</span></span>

### <a name="configure-links"></a><span data-ttu-id="ee192-118">Настроить ссылки</span><span class="sxs-lookup"><span data-stu-id="ee192-118">Configure links</span></span>

<span data-ttu-id="ee192-119">В каждой созданной ссылке будут определены следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="ee192-119">Each link that is created will have the following information defined.</span></span>

- <span data-ttu-id="ee192-120">Ссылка — имя ссылки, используемое для идентификации только.</span><span class="sxs-lookup"><span data-stu-id="ee192-120">Link - Name of the link, used for identification only.</span></span>

- <span data-ttu-id="ee192-121">Включить эту ссылку — задайте значение **Да**, если требуется отобразить эту ссылку для пользователей Talent.</span><span class="sxs-lookup"><span data-stu-id="ee192-121">Enable this Link - Set to **Yes** if you want to display the link to users of Talent.</span></span>

- <span data-ttu-id="ee192-122">Отображаемое имя — определите имя, которое будет отображаться как ссылка на Finance.</span><span class="sxs-lookup"><span data-stu-id="ee192-122">Display name - Define the name that will appear as a link to Finance.</span></span> <span data-ttu-id="ee192-123">Эти данные в настоящее время не переведены.</span><span class="sxs-lookup"><span data-stu-id="ee192-123">This data is currently is not translated.</span></span>

- <span data-ttu-id="ee192-124">Поверхностная ссылка на форму — выберите, на какой странице должна отображаться эта ссылка.</span><span class="sxs-lookup"><span data-stu-id="ee192-124">Surface link on form - Choose which page you would like to display the link on.</span></span>

- <span data-ttu-id="ee192-125">Группа — группы не являются обязательными, но если требуется упорядочить ссылки с помощью групп, выберите существующую группу или создайте новую, используя поле **Группа**.</span><span class="sxs-lookup"><span data-stu-id="ee192-125">Group - Groups are not required, but if you want to organize your links using groups, select an existing group or create a new one using the **Group** field.</span></span>

- <span data-ttu-id="ee192-126">Целевая система — выберите целевую систему, которая была создана с помощью параметра **Настроить целевую систему**.</span><span class="sxs-lookup"><span data-stu-id="ee192-126">Target system - Select the target system that was created using the **Configure target system** option.</span></span> <span data-ttu-id="ee192-127">Это будет среда Finance, которая будет использоваться при переходе с помощью ссылки.</span><span class="sxs-lookup"><span data-stu-id="ee192-127">This will be the Finance environment that will be used when navigating by using the link.</span></span>

- <span data-ttu-id="ee192-128">Использовать текущую компанию пользователя — выберите **Да**, если вы хотите использовать контекст текущей компании пользователя при переходе к Finance.</span><span class="sxs-lookup"><span data-stu-id="ee192-128">Use user's current Company - Select **Yes** if you would like to use the User's current company context when navigating to Finance.</span></span> <span data-ttu-id="ee192-129">Если выбрано значение **Нет**, можно выбрать компанию, которую следует использовать.</span><span class="sxs-lookup"><span data-stu-id="ee192-129">If **No** is selected, then you can select the company that should be used.</span></span>

- <span data-ttu-id="ee192-130">Целевой пункт меню — введите пункт меню из Finance, который ссылка должна использовать при переходе.</span><span class="sxs-lookup"><span data-stu-id="ee192-130">Target menu item - Enter the menu item from Finance that the link should use when navigating.</span></span> <span data-ttu-id="ee192-131">Доступны пункты меню, к которым можно перейти напрямую.</span><span class="sxs-lookup"><span data-stu-id="ee192-131">Menu items that you can directly navigate to are available.</span></span> <span data-ttu-id="ee192-132">Чтобы найти требуемый пункт меню, откройте Finance и откройте страницу, которая является целевой для навигации.</span><span class="sxs-lookup"><span data-stu-id="ee192-132">To find the menu item required, open Finance and open the page that is the target of the navigation.</span></span> <span data-ttu-id="ee192-133">Скопируйте пункт меню из URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="ee192-133">Copy the menu item from the URL.</span></span> <span data-ttu-id="ee192-134">Например, если вы хотите, чтобы ссылка вела на список сотрудников в Finance and Operations, введите значение, которое появляется после "&mi" в URL-адресе.</span><span class="sxs-lookup"><span data-stu-id="ee192-134">For example, if you want the link to take you to the employee list in Finance and Operations, enter the value that appears after the "&mi" in the URL.</span></span> <span data-ttu-id="ee192-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="ee192-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span></span> <span data-ttu-id="ee192-136">Пункт меню для перехода к странице списка сотрудников в этом примере имеет вид: HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="ee192-136">The menu item to navigate to the employee list page in this example is: HcmWorkerListPage_Employees.</span></span>

- <span data-ttu-id="ee192-137">Ссылка на источник данных — выберите источник данных, на который ссылается ссылка.</span><span class="sxs-lookup"><span data-stu-id="ee192-137">Link to data source - Select the source of data that the link is referencing.</span></span> <span data-ttu-id="ee192-138">Доступны наиболее распространенные источники, такие как **Рабочий** и **Должность**.</span><span class="sxs-lookup"><span data-stu-id="ee192-138">The most common sources like **Worker** and **Position** are available.</span></span>

- <span data-ttu-id="ee192-139">Ссылка на поле — (Скоро появится) выбор этого поля обеспечивает прямой переход из одной записи в Talent на одну запись в Finance.</span><span class="sxs-lookup"><span data-stu-id="ee192-139">Link to field - (Coming soon) This field selection will allow for direct navigation from a single record in Talent to a single record in Finance.</span></span>

### <a name="access-to-links"></a><span data-ttu-id="ee192-140">Доступ к ссылкам</span><span class="sxs-lookup"><span data-stu-id="ee192-140">Access to links</span></span>

<span data-ttu-id="ee192-141">Системные администраторы будут видеть вновь созданные ссылки на определенные страницы, даже если для параметра **Включить эту ссылку** задано значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="ee192-141">System administrators will see the newly created links on the defined pages even if the **Enable this link** option is set to **No**.</span></span> <span data-ttu-id="ee192-142">Это можно использовать для тестирования ссылок перед их отображением другим сотрудникам.</span><span class="sxs-lookup"><span data-stu-id="ee192-142">This can be used for testing links prior to surfacing them to other employees.</span></span> <span data-ttu-id="ee192-143">Все другие роли будут видеть настроенные ссылки только после того, как для параметра **Включить эту ссылку** было задано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="ee192-143">All other roles will only see the configured links after the **Enable this link** option is set to **Yes**.</span></span> <span data-ttu-id="ee192-144">Сотрудники, которые имеют доступ к страницам, на которых отображаются ссылки, будут иметь доступ к ссылкам.</span><span class="sxs-lookup"><span data-stu-id="ee192-144">Employees who have access to the pages in which the links are surfaced will have access to the links.</span></span>

<span data-ttu-id="ee192-145">Пользователи также могут иметь права безопасности в Finance, определенные для доступа к страницам в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ee192-145">Users can also have security rights within Finance defined to access the pages in Finance and Operations.</span></span> <span data-ttu-id="ee192-146">Если они отсутствуют, при использовании ссылки будет отображаться диалоговое окно безопасности.</span><span class="sxs-lookup"><span data-stu-id="ee192-146">If they don't, a security dialog box will be displayed when using the link.</span></span>


## <a name="other-changesfixes"></a><span data-ttu-id="ee192-147">Другие изменения/исправления</span><span class="sxs-lookup"><span data-stu-id="ee192-147">Other changes/fixes</span></span>

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a><span data-ttu-id="ee192-148">Должности с датой начала в будущем не могут назначаться новому сотруднику</span><span class="sxs-lookup"><span data-stu-id="ee192-148">Positions with a future start date cannot be assigned to a new employee</span></span>

<span data-ttu-id="ee192-149">Внесены изменения, чтобы разрешить назначений сотрудников на должности с датой в будущем.</span><span class="sxs-lookup"><span data-stu-id="ee192-149">Changes have been made to allow employee assignments to future-dated positions.</span></span> <span data-ttu-id="ee192-150">Должности с начальными датами в будущем могут быть выбраны и назначение сотрудника будет выполнено после сохранения или завершения workflow-процесс (если workflow-процесс включен).</span><span class="sxs-lookup"><span data-stu-id="ee192-150">Positions that have start dates in the future can be selected and the employee assignment will be made upon save or completion of the workflow (if the workflow is enabled).</span></span>

### <a name="new-employee-cannot-be-assigned-existing-position"></a><span data-ttu-id="ee192-151">Новый сотрудник не может быть назначен существующей должности</span><span class="sxs-lookup"><span data-stu-id="ee192-151">New employee cannot be assigned existing position</span></span>

<span data-ttu-id="ee192-152">Изменения были сделаны, чтобы новое назначение сотрудника могло быть назначено существующей должности.</span><span class="sxs-lookup"><span data-stu-id="ee192-152">Changes have been made so new employee assignment can now be assigned to existing positions.</span></span>

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a><span data-ttu-id="ee192-153">Дата трудового стажа или расположение офиса исчезает, если начальная дата приема на работу находится в прошлом и запись сохранена</span><span class="sxs-lookup"><span data-stu-id="ee192-153">Seniority date/Office location disappears when the employment start date is in the past and the record is saved</span></span>

<span data-ttu-id="ee192-154">Были внесены изменения для исправления видимости полей **Дата начала стажа** и **Расположение офиса** при сохранении изменений для прошлых сотрудников.</span><span class="sxs-lookup"><span data-stu-id="ee192-154">Changes have been made to correct the visibilty of the **Senority date** and **Office location** when saving changes for past employees.</span></span>

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a><span data-ttu-id="ee192-155">Невозможно ввести данные для трудоустройства с будущей датой на странице работника</span><span class="sxs-lookup"><span data-stu-id="ee192-155">Can't enter data for future-dated employments on the worker page</span></span>

<span data-ttu-id="ee192-156">Данные о занятости для трудоустройства с будущей датой была отключена на основной странице работника.</span><span class="sxs-lookup"><span data-stu-id="ee192-156">Employment data for future-dated employments has been disabled on the main worker page.</span></span> <span data-ttu-id="ee192-157">Данные трудоустройства можно вводить с помощью страниц **Диспетчер дат**.</span><span class="sxs-lookup"><span data-stu-id="ee192-157">Employment data can be entered through the **Date Manager** pages.</span></span> <span data-ttu-id="ee192-158">Дополнительные изменения будет выполнены в будущих выпусках, чтобы разрешить ввод данных о трудоустройстве непосредственно во время workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="ee192-158">Additional changes will be made in future releases to enable entering employment data directly during the workflow process.</span></span>

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a><span data-ttu-id="ee192-159">Добавление ValidFrom и ValidTo в HcmPersonalContactPersonEntity</span><span class="sxs-lookup"><span data-stu-id="ee192-159">Add ValidFrom and ValidTo to HcmPersonalContactPersonEntity</span></span>

<span data-ttu-id="ee192-160">Объект платформы управления данными (DMF) HcmPersonalContactPersonEntity был обновлен для включения дат "действительно с" и "действительно до" для включения определенных сценариев интеграции льгот.</span><span class="sxs-lookup"><span data-stu-id="ee192-160">The Data Management Framework (DMF) entity HcmPersonalContactPersonEntity has been updated to include "valid from" and "valid to" dates to enable certain benefit integration scenarios.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="ee192-161">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="ee192-161">Known issue</span></span>
- <span data-ttu-id="ee192-162">**Проблема**: при добавлении нового вложения для работника кнопки **Создать** и **Изменить** неактивны.</span><span class="sxs-lookup"><span data-stu-id="ee192-162">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="ee192-163">**Временное решение:** перед открытием страницы вложения убедитесь, что информационные панели на странице **Рабочий** закрыты.</span><span class="sxs-lookup"><span data-stu-id="ee192-163">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="ee192-164">Если информационные панели закрыты при загрузке страницы **Работник**, кнопки вложений будут активны.</span><span class="sxs-lookup"><span data-stu-id="ee192-164">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="ee192-165">(Эта проблема будет исправлена в следующем обновлении платформы.)</span><span class="sxs-lookup"><span data-stu-id="ee192-165">(This issue will be fixed in the next platform update.)</span></span>
