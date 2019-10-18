---
title: Что нового и что изменилось в Dynamics 365 Talent — Core HR (8 октября 2018 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
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
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 330ffebf73c8948a1bbab2ee57acba7b97a93b6f
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008881"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-8-2018"></a><span data-ttu-id="2a9f7-103">Что нового и что изменилось в Dynamics 365 Talent — Core HR (8 октября 2018 г.)</span><span class="sxs-lookup"><span data-stu-id="2a9f7-103">What's new or changed in Dynamics 365 Talent - Core HR (October 8, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2a9f7-104">**Сборка 8.1.1050.0**</span><span class="sxs-lookup"><span data-stu-id="2a9f7-104">**Build 8.1.1050.0**</span></span>

<span data-ttu-id="2a9f7-105">В этой теме описываются новые и измененные компоненты Core HR.</span><span class="sxs-lookup"><span data-stu-id="2a9f7-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a><span data-ttu-id="2a9f7-106">Разрешить использовать другие даты для использования на базе уровня отпусков (управление отпусками)</span><span class="sxs-lookup"><span data-stu-id="2a9f7-106">Allow other dates to be used on leave tier basis (Leave Management)</span></span>

<span data-ttu-id="2a9f7-107">При предоставлении отпуска сотрудникам база уровня вознаграждения определяет, сколько отгулов начислено сотруднику.</span><span class="sxs-lookup"><span data-stu-id="2a9f7-107">When awarding leave to employees, the award tier basis determines how much time off an employee accrues.</span></span> <span data-ttu-id="2a9f7-108">В настоящее время эти уровни основаны на дате приема сотрудника на работу и дате трудового стажа.</span><span class="sxs-lookup"><span data-stu-id="2a9f7-108">Currently, these tiers are based on employee start date and seniority date.</span></span> <span data-ttu-id="2a9f7-109">В некоторых сценариях организациям требуются, чтобы эти уровни были основаны на других датах, таких как дата юбилея или исходная дата приема на работу.</span><span class="sxs-lookup"><span data-stu-id="2a9f7-109">In some scenarios, organizations need these tiers to be based on other dates, like anniversary date or original hire date.</span></span> <span data-ttu-id="2a9f7-110">Эти даты уже используются в плане отпусков для определения, когда происходит начисление, возможность использовать эти же даты при регистрации сотрудника в плане была добавлена для определения суммы начисления.</span><span class="sxs-lookup"><span data-stu-id="2a9f7-110">These dates are already used on the leave plan to determine when accruals happen, the ability for these same dates to be used when an employee is enrolled in a plan have been added to determine the accrual amount.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="2a9f7-111">Другие изменения</span><span class="sxs-lookup"><span data-stu-id="2a9f7-111">Other changes</span></span>
<span data-ttu-id="2a9f7-112">Прочие исправления были включены в данный выпуск.</span><span class="sxs-lookup"><span data-stu-id="2a9f7-112">Miscellanous fixes have been included in this release.</span></span>

## <a name="known-issue"></a><span data-ttu-id="2a9f7-113">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="2a9f7-113">Known issue</span></span>

<span data-ttu-id="2a9f7-114">**Проблема:** при добавлении нового вложения в работника кнопки **Создать** и **Редактировать** неактивны. **Обход:** перед открытием страницы вложения убедитесь, что информационные панели на странице **Работник** закрыты.</span><span class="sxs-lookup"><span data-stu-id="2a9f7-114">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="2a9f7-115">Если информационные панели закрыты при загрузке страницы **Работник**, кнопки вложений будут активны.</span><span class="sxs-lookup"><span data-stu-id="2a9f7-115">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="2a9f7-116">(Эта проблема будет исправлена в следующем обновлении платформы.)</span><span class="sxs-lookup"><span data-stu-id="2a9f7-116">(This issue will be fixed in the next platform update.)</span></span>
