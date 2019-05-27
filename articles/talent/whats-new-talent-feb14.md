---
title: Что нового и что изменилось в Dynamics 365 for Talent (14 февраля 2019 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
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
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1db7d032eade3f996e0554e64d6ea0704a347ed8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518906"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-14-2019"></a><span data-ttu-id="c63de-103">Что нового и что изменилось в Dynamics 365 for Talent (14 февраля 2019 г.)</span><span class="sxs-lookup"><span data-stu-id="c63de-103">What's new or changed in Dynamics 365 for Talent (February 14, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c63de-104">В этой теме описываются новые и измененные компоненты в Talent.</span><span class="sxs-lookup"><span data-stu-id="c63de-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="c63de-105">Изменения в Attract</span><span class="sxs-lookup"><span data-stu-id="c63de-105">Changes in Attract</span></span>
<span data-ttu-id="c63de-106">Исправления незначительных ошибок включены в этот выпуск.</span><span class="sxs-lookup"><span data-stu-id="c63de-106">There are minor bug fixes included with this release.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="c63de-107">Изменения в Onboarding</span><span class="sxs-lookup"><span data-stu-id="c63de-107">Changes in Onboarding</span></span>
<span data-ttu-id="c63de-108">Исправления незначительных ошибок включены в этот выпуск.</span><span class="sxs-lookup"><span data-stu-id="c63de-108">There are minor bug fixes included with this release.</span></span>
 
## <a name="changes-in-core-hr"></a><span data-ttu-id="c63de-109">Изменения в Core HR</span><span class="sxs-lookup"><span data-stu-id="c63de-109">Changes in Core HR</span></span> 
<span data-ttu-id="c63de-110">**Сборка 8.1.2146**</span><span class="sxs-lookup"><span data-stu-id="c63de-110">**Build 8.1.2146**</span></span>

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a><span data-ttu-id="c63de-111">Сущность фиксированной компенсации сотруднику не экспортирует все записи</span><span class="sxs-lookup"><span data-stu-id="c63de-111">Employee fixed compensation entity doesn't export all records</span></span>
<span data-ttu-id="c63de-112">После этого изменения сущность **Фиксированная компенсация сотрудникам** сейчас будет экспортировать все записи.</span><span class="sxs-lookup"><span data-stu-id="c63de-112">With this change, the **Employee fixed compensation** entity will now export all records.</span></span> <span data-ttu-id="c63de-113">Сущность может использоваться для создания и обновления существующих записей о фиксированной компенсации для сотрудников.</span><span class="sxs-lookup"><span data-stu-id="c63de-113">The entity can be used to create and update existing fixed compensation records for employees.</span></span> 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a><span data-ttu-id="c63de-114">Дата окончания занятости не учитывает заданные параметры предпочтительного часового пояса сотрудника</span><span class="sxs-lookup"><span data-stu-id="c63de-114">Employment end date doesn't honor employee preferred time zone settings</span></span>
<span data-ttu-id="c63de-115">Даты окончания занятости сейчас учитывают предпочитаемый пользователем часовой пояс при создании или окончания занятости с компанией.</span><span class="sxs-lookup"><span data-stu-id="c63de-115">Employment end dates are now honoring the user-preferred time zone when creating or ending employment with a company.</span></span>
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a><span data-ttu-id="c63de-116">Адреса из Великобритании в Analytics отображаются как адреса из восточной Швейцарии</span><span class="sxs-lookup"><span data-stu-id="c63de-116">UK addresses display in Analytics as Eastern Switzerland addresses</span></span>
<span data-ttu-id="c63de-117">В этом выпуске внесено изменение для исправления рассогласования адресов в отчете "Численность сотрудников по местоположению" в области **Управление персоналом**.</span><span class="sxs-lookup"><span data-stu-id="c63de-117">In this release, a change has been made to correct misalignment in addresses in the **Personnel Management** "Headcount by location" report.</span></span>
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a><span data-ttu-id="c63de-118">Код увольнения не заполняется для записи назначения должности работника при завершении должности</span><span class="sxs-lookup"><span data-stu-id="c63de-118">Termination code is not populated on the worker position assignment record when ending the position</span></span>
<span data-ttu-id="c63de-119">Изменение внесено в код по умолчанию "Причина увольнения" при окончании назначения сотрудникам должности.</span><span class="sxs-lookup"><span data-stu-id="c63de-119">A change has been made to default the "Termination reason" code when ending the employees position assignment.</span></span>

### <a name="new-entity-created-for-job-compensation-levels"></a><span data-ttu-id="c63de-120">Создана новая сущность для уровней компенсации вакансии</span><span class="sxs-lookup"><span data-stu-id="c63de-120">New entity created for job compensation levels</span></span>
<span data-ttu-id="c63de-121">Создана новая сущность платформы управления данными (DMF).</span><span class="sxs-lookup"><span data-stu-id="c63de-121">A new data management framework (DMF) entity was created.</span></span> <span data-ttu-id="c63de-122">Сущность позволяет создавать и обновлять уровни компенсации, значения рынка и обзорные сведения для каждой вакансии, которая определена в системе.</span><span class="sxs-lookup"><span data-stu-id="c63de-122">The entity provides for creation and updates to compensation levels, market values, and survey information for each job defined in the system.</span></span>
