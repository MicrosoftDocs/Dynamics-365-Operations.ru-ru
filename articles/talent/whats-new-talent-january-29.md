---
title: Что нового и что изменилось в Dynamics 365 for Talent (31 января 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 1/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5c9449e2bdec8c17cc2cf659ed68ac1d713a26ad
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2019
ms.locfileid: "374742"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-january-31-2019"></a><span data-ttu-id="b684f-103">Что нового и что изменилось в Dynamics 365 for Talent (31 января 2019 г.)</span><span class="sxs-lookup"><span data-stu-id="b684f-103">What's new or changed in Dynamics 365 for Talent (January 31, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b684f-104">В этой теме описываются новые и измененные компоненты Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="b684f-104">This topic describes features that are either new or changed in Dynamics 365 for Talent</span></span>

<span data-ttu-id="b684f-105">**Сборка 8.1.2128**</span><span class="sxs-lookup"><span data-stu-id="b684f-105">**Build 8.1.2128**</span></span>

## <a name="core-hr-changes"></a><span data-ttu-id="b684f-106">Изменения Core HR</span><span class="sxs-lookup"><span data-stu-id="b684f-106">Core HR Changes</span></span>

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a><span data-ttu-id="b684f-107">Отгул, взятый на карточке отпусков людей, не учитывает даты плана отпусков</span><span class="sxs-lookup"><span data-stu-id="b684f-107">Time off taken on leave people card doesn't consider leave plan dates</span></span>
<span data-ttu-id="b684f-108">Для организаций, планы отпусков в которых не совпадают с календарным годом, карточка **Взято** теперь отображает отгулы, взятые в год, определенный планом отпусков.</span><span class="sxs-lookup"><span data-stu-id="b684f-108">For those that have leave plans that don’t run on a calendar year, the **Taken** card now displays time off that’s been taken in the plan-defined leave year.</span></span> <span data-ttu-id="b684f-109">Например, если год отпусков в организации начинается 1 июня и заканчивается 30 мая, а сотрудник взял 3 дня отгулов в декабре, на карточке **Взято** 15 января будет отображаться 3 дня.</span><span class="sxs-lookup"><span data-stu-id="b684f-109">For example, if an organization’s leave year is June 1 through May 30 and an employee has taken 3 days off in December, the **Taken** card on January 15, will display 3 days.</span></span> 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a><span data-ttu-id="b684f-110">Суммы начисления не совпадают с базисом даты уровня</span><span class="sxs-lookup"><span data-stu-id="b684f-110">Accrual amounts not matching tier date basis</span></span>
<span data-ttu-id="b684f-111">Были добавлены новые параметры для отпуска и отсутствия (параметры **Управление персоналом**), чтобы клиенты могли определять, когда вступают в силу месяцы даты службы сотрудников.</span><span class="sxs-lookup"><span data-stu-id="b684f-111">New options have been added to leave and absence (**Human resources** parameters) to enable customers to determine when employees’ months of service date are effective.</span></span> <span data-ttu-id="b684f-112">Для некоторых организаций эта дата является концом месяца, но для других это может быть начало следующего месяца.</span><span class="sxs-lookup"><span data-stu-id="b684f-112">For some organizations, the date is the end of the month, but for others it may be the start of the next month.</span></span> <span data-ttu-id="b684f-113">Например, одна организация может начислять отпускное время 31 декабря, в то время как другая может начислять отпускное время 1 января.</span><span class="sxs-lookup"><span data-stu-id="b684f-113">For example, one organization may award time off on December 31, while another may award time off on January 1.</span></span> <span data-ttu-id="b684f-114">Этот параметр позволяет выбрать, когда должно производиться начисление.</span><span class="sxs-lookup"><span data-stu-id="b684f-114">This option will allow you to choose when the award should occur.</span></span> 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a><span data-ttu-id="b684f-115">Действия приема на работу застопориваются в состоянии "Workflow-процесс завершен"</span><span class="sxs-lookup"><span data-stu-id="b684f-115">Worker hire actions are stuck in "Workflow complete" state</span></span>
<span data-ttu-id="b684f-116">Были внесены изменения для устранения проблемы, когда небольшое количество workflow-процессов завершалось с состоянием "Workflow-процесс завершен".</span><span class="sxs-lookup"><span data-stu-id="b684f-116">Changes have been made to correct an issue where a small number of workflows finished with a "Workflow complete" status.</span></span> <span data-ttu-id="b684f-117">Новые workflow-процессы теперь должны переходить в состояние "Завершено" при завершении workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="b684f-117">New workflows should now move to a "Completed" state when the workflow finishes.</span></span> <span data-ttu-id="b684f-118">Любые workflow-процессы в состоянии "Workflow-процесс завершен" будут переведены в состояние ошибки для обновления или удаления по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="b684f-118">Any workflows in a workflow completed status will be transitioned to an error status to allow for updating or removal if required.</span></span> 
