---
title: Что нового и что изменилось в Dynamics 365 Talent - Core HR (23 января 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
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
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f97462f088fc1a3cb94f2a34204fc09f1cd66fb0
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899136"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-23-2019"></a><span data-ttu-id="607e3-103">Что нового и что изменилось в Dynamics 365 Talent - Core HR (23 января 2019 г.)</span><span class="sxs-lookup"><span data-stu-id="607e3-103">What's new or changed in Dynamics 365 Talent - Core HR (January 23, 2019)</span></span>

<span data-ttu-id="607e3-104">**Сборка 8.1.2121**</span><span class="sxs-lookup"><span data-stu-id="607e3-104">**Build 8.1.2121**</span></span>

<span data-ttu-id="607e3-105">В этой теме описываются новые и измененные компоненты Core HR.</span><span class="sxs-lookup"><span data-stu-id="607e3-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="607e3-106">Изменения</span><span class="sxs-lookup"><span data-stu-id="607e3-106">Changes</span></span>

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a><span data-ttu-id="607e3-107">Импорт фиксированной компенсации сотрудников не работает при создании новых записей фиксированной компенсации</span><span class="sxs-lookup"><span data-stu-id="607e3-107">Import of employee fixed compensation not working when creating new fixed compensation records</span></span>
<span data-ttu-id="607e3-108">Сделано изменение, чтобы сущность фиксированной компенсации сотрудников извлекала уровень компенсации при импорте.</span><span class="sxs-lookup"><span data-stu-id="607e3-108">A change has been made to the employee fixed compensation entity to retrieve the compensation level upon import.</span></span> <span data-ttu-id="607e3-109">До этого выпуска отображалось сообщение, указывающее на то, что требовался уровень.</span><span class="sxs-lookup"><span data-stu-id="607e3-109">Prior to this release, a message was displayed indicating that the level was required.</span></span>

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a><span data-ttu-id="607e3-110">Удалить поле минимального сальдо из диалогового окна запроса отгула</span><span class="sxs-lookup"><span data-stu-id="607e3-110">Remove the minimum balance field from the time off request dialog box</span></span>
<span data-ttu-id="607e3-111">Поле **Минимальное сальдо** было удалено из диалогового окна **Запрос отгула**.</span><span class="sxs-lookup"><span data-stu-id="607e3-111">The **Minimum balance** field has been removed from the **Time off request** dialog box.</span></span> <span data-ttu-id="607e3-112">Это изменение затрагивает все области, где можно запросить отгул.</span><span class="sxs-lookup"><span data-stu-id="607e3-112">This change affects all areas where time off can be requested.</span></span>

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a><span data-ttu-id="607e3-113">Обновление данных для уровней компенсации обновляется не во всех сценариях</span><span class="sxs-lookup"><span data-stu-id="607e3-113">Data upgrade for compensation levels not updating in all scenarios</span></span>
<span data-ttu-id="607e3-114">Изменение сделано для обновления уровня компенсации в планах фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="607e3-114">A change has been made to update the compensation level on fixed compensation plans.</span></span> <span data-ttu-id="607e3-115">Это изменение приведет к заполнению уровня компенсации в фиксированных планах для должности, назначенной сотруднику.</span><span class="sxs-lookup"><span data-stu-id="607e3-115">This change will populate the compensation level on fixed plans for the job assigned to the employee.</span></span>

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a><span data-ttu-id="607e3-116">Информация о заработной плате на странице "Управление изменениями" доступна только при входе от имени системного администратора</span><span class="sxs-lookup"><span data-stu-id="607e3-116">Payroll information in the Manage changes page is only available when logged in as System Administrator</span></span>
<span data-ttu-id="607e3-117">Это изменение позволяет сотрудникам с ролью администратора заработной платы получать доступ к информации на странице **Временная шкала изменений > Управление изменениями** для должности.</span><span class="sxs-lookup"><span data-stu-id="607e3-117">This change allows employees with the Payroll Administrator role access to the payroll information on the **Changes timeline > Manage changes** page for the position.</span></span>

### <a name="job-fields-default-to-positions"></a><span data-ttu-id="607e3-118">Поля должности принимают значения по умолчанию для позиций</span><span class="sxs-lookup"><span data-stu-id="607e3-118">Job fields default to positions</span></span>
<span data-ttu-id="607e3-119">При изменении должности на позицию поля должности принимают значения по умолчанию для этой позиции.</span><span class="sxs-lookup"><span data-stu-id="607e3-119">When changing the job on a position, job fields will default to the position.</span></span> <span data-ttu-id="607e3-120">Оповещающее сообщение появится, давая возможность принять значения по умолчанию или сохранить текущие значения для этих полей.</span><span class="sxs-lookup"><span data-stu-id="607e3-120">An alert message will appear giving an option to accept the default values or keep the existing values for those fields.</span></span>

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a><span data-ttu-id="607e3-121">Период надзора и календарь не отображаются для будущих нанимаемых сотрудников.</span><span class="sxs-lookup"><span data-stu-id="607e3-121">Probation period and calendar are not displayed for future hired employees.</span></span>
<span data-ttu-id="607e3-122">После этого изменения поля **Период надзора** и **Календарь** были добавлены на страницу **Управление изменениями**, чтобы позволить вводить данные для будущих и прошлых сотрудников.</span><span class="sxs-lookup"><span data-stu-id="607e3-122">With this change, **Probation period** and **Calendar** fields have been added to the **Manage changes** page to allow for data entry for future and past employees.</span></span>

### <a name="platform-update-23-for-finance-and-operations"></a><span data-ttu-id="607e3-123">Platform update 23 для Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="607e3-123">Platform update 23 for Finance and Operations</span></span>
<span data-ttu-id="607e3-124">Исправления мелких ошибок были включены в состав обновления платформы Platform Update 23 для Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="607e3-124">Minor bug fixes have been included as part of Platform update 23 for Finance and Operations.</span></span> <span data-ttu-id="607e3-125">Дополнительные сведения см. в разделе [Что нового и что изменилось в Dynamics 365 Finance and Operations, обновление платформы 23 (январь 2019 г.)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span><span class="sxs-lookup"><span data-stu-id="607e3-125">For more information, see [What's new or changed in Dynamics 365 Finance and Operations platform update 23 (January 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span></span> 
