---
title: Что нового и что изменилось в Dynamics 365 for Talent Core HR (15 ноября 2018 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
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
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b90d4230fe1e666aba4075670f6df206e8df7ce9
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518947"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-15-2018"></a><span data-ttu-id="50121-103">Что нового и что изменилось в Dynamics 365 for Talent Core HR (15 ноября 2018 г.)</span><span class="sxs-lookup"><span data-stu-id="50121-103">What's new or changed in Dynamics 365 for Talent Core HR (November 15, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="50121-104">**Сборка 8.1.2045**</span><span class="sxs-lookup"><span data-stu-id="50121-104">**Build 8.1.2045**</span></span>

<span data-ttu-id="50121-105">В этой теме описываются новые и измененные компоненты Core HR.</span><span class="sxs-lookup"><span data-stu-id="50121-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="other-changesfixes"></a><span data-ttu-id="50121-106">Другие изменения/исправления</span><span class="sxs-lookup"><span data-stu-id="50121-106">Other changes/fixes</span></span>

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a><span data-ttu-id="50121-107">Не удается изменить текущую должность сотрудника на будущую открытую должность</span><span class="sxs-lookup"><span data-stu-id="50121-107">Unable to change employee´s current position to a future open position</span></span>

<span data-ttu-id="50121-108">Изменение было сделано для обеспечения переносов должностей, когда должность будет доступна только в будущем.</span><span class="sxs-lookup"><span data-stu-id="50121-108">A change has been made to enable position transfers when the position is only available in the future.</span></span> 

### <a name="position-does-not-display-when-creating-a-new-employee"></a><span data-ttu-id="50121-109">Должность не отображается при создании нового сотрудника</span><span class="sxs-lookup"><span data-stu-id="50121-109">Position does not display when creating a new employee</span></span>

<span data-ttu-id="50121-110">Внесено изменение для отображения всех открытых вакансий, которые доступны для назначения при приеме на работу новых сотрудников в Talent.</span><span class="sxs-lookup"><span data-stu-id="50121-110">A change has been made to display all open positions that are available for assignment when hiring new employees in Talent.</span></span> <span data-ttu-id="50121-111">Это включает исторические должности или должности с будущей датой.</span><span class="sxs-lookup"><span data-stu-id="50121-111">This includes historical positions or if the postitions have been future dated.</span></span> <span data-ttu-id="50121-112">Должности теперь будут появляться правильно в зависимости от даты начала работы.</span><span class="sxs-lookup"><span data-stu-id="50121-112">Positions will now appear correctly based on the employment start date.</span></span> 

### <a name="termination-date-is-displaying-based-on-user-settings"></a><span data-ttu-id="50121-113">Дату увольнения отображается на основе параметров пользователя</span><span class="sxs-lookup"><span data-stu-id="50121-113">Termination date is displaying based on user settings</span></span>

<span data-ttu-id="50121-114">Внесено изменение в список прошлых сотрудников для учета любые смещений часового пояса для предпочтительного часового пояса сотрудников при просмотре даты увольнения.</span><span class="sxs-lookup"><span data-stu-id="50121-114">A change has been made to the past employees list to account for any time zone offsets for the employees preferred time zone when viewing the termination date.</span></span>

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a><span data-ttu-id="50121-115">Ссылки на рабочие элементы, назначенные мне, не отображают правильную информацию</span><span class="sxs-lookup"><span data-stu-id="50121-115">Work items assigned to me links not displaying the correct information</span></span>

<span data-ttu-id="50121-116">С этим изменением переход к подробным сведениям отдельных рабочих элементов в списке будет отображаться правильная информация для выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="50121-116">With this change, navigation to the details of the individual work items in the list will display the correct information for the item selected.</span></span> <span data-ttu-id="50121-117">Эта проблема возникает только с расширенными параметрами безопасности.</span><span class="sxs-lookup"><span data-stu-id="50121-117">This issue only occurred with advanced security options.</span></span>


## <a name="known-issue"></a><span data-ttu-id="50121-118">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="50121-118">Known issue</span></span>

- <span data-ttu-id="50121-119">**Проблема**: при добавлении нового вложения для работника кнопки **Создать** и **Изменить** неактивны.</span><span class="sxs-lookup"><span data-stu-id="50121-119">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="50121-120">**Временное решение:** перед открытием страницы вложения убедитесь, что информационные панели на странице **Рабочий** закрыты.</span><span class="sxs-lookup"><span data-stu-id="50121-120">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="50121-121">Если информационные панели закрыты при загрузке страницы **Работник**, кнопки вложений будут активны.</span><span class="sxs-lookup"><span data-stu-id="50121-121">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="50121-122">(Эта проблема будет исправлена в следующем обновлении платформы.)</span><span class="sxs-lookup"><span data-stu-id="50121-122">(This issue will be fixed in the next platform update.)</span></span>
