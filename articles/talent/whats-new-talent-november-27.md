---
title: Что нового и что изменилось в Dynamics 365 for Talent Core HR (27 ноября 2018 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
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
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 81ea0e4f4878d1967234c597504071ce464a22c5
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "857809"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-27-2018"></a><span data-ttu-id="94700-103">Что нового и что изменилось в Dynamics 365 for Talent Core HR (27 ноября 2018 г.)</span><span class="sxs-lookup"><span data-stu-id="94700-103">What's new or changed in Dynamics 365 for Talent Core HR (November 27, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="94700-104">**Сборка 8.1.2064**</span><span class="sxs-lookup"><span data-stu-id="94700-104">**Build 8.1.2064**</span></span>

<span data-ttu-id="94700-105">В этой теме описываются новые и измененные компоненты Core HR.</span><span class="sxs-lookup"><span data-stu-id="94700-105">This topic describes features that are either new or changed in Core HR.</span></span>


## <a name="changes"></a><span data-ttu-id="94700-106">Изменения</span><span class="sxs-lookup"><span data-stu-id="94700-106">Changes</span></span>

### <a name="unable-to-create-a-note-in-case-management"></a><span data-ttu-id="94700-107">Не удается создать примечание в управлении обращениями</span><span class="sxs-lookup"><span data-stu-id="94700-107">Unable to create a note in Case Management</span></span>

<span data-ttu-id="94700-108">Было сделано изменение для проблемы при попытке изменить или создать примечание в журнале обращений управления обращениями.</span><span class="sxs-lookup"><span data-stu-id="94700-108">A change has been made for an issue when attempting to edit or create a note in the case log of Case Management.</span></span>

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a><span data-ttu-id="94700-109">Неправильно написанное слово на вкладке аналитики в рабочей области компенсации</span><span class="sxs-lookup"><span data-stu-id="94700-109">Misspelled word on the analytics tab in the compensation workspace</span></span> 

<span data-ttu-id="94700-110">Изменение сделано для исправления орфографии слов "Этническое происхождение" в диаграмме аналитики компенсации в рабочей области компенсации.</span><span class="sxs-lookup"><span data-stu-id="94700-110">A change has been made to correct the spelling of 'Ethnic Origin' in the compensation analytics chart in the compensation workspace.</span></span>

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a><span data-ttu-id="94700-111">Рабочая область самообслуживания сотрудников не отображается, когда пользователь не назначен работнику</span><span class="sxs-lookup"><span data-stu-id="94700-111">Employee self-service workspace not displaying when a user isn't assigned to a worker</span></span> 

<span data-ttu-id="94700-112">Внесено изменение, когда рабочая область **Самообслуживание сотрудников** выбрана в качестве начальной страницы при запуске для пользователя, которому не назначен работник.</span><span class="sxs-lookup"><span data-stu-id="94700-112">A change has been made when the **Employee self-service** workspace is selected as the initial page on startup for a user who is not assigned to a worker.</span></span> <span data-ttu-id="94700-113">В этом случае будет отображена панель мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="94700-113">In this situation, the default dashboard will be displayed.</span></span>

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a><span data-ttu-id="94700-114">Ошибка отпусков и отсутствия: ссылка на объект не указывает на экземпляр объекта</span><span class="sxs-lookup"><span data-stu-id="94700-114">Leave and Absence error: Object reference not set to an instance of an object</span></span>

<span data-ttu-id="94700-115">Были внесены изменения в модуль отпусков и отсутствия для исправления этой ошибки после утверждения записей отпусков и отсутствия в списке **Рабочие элементы, назначенные мне**.</span><span class="sxs-lookup"><span data-stu-id="94700-115">Changes have been made to Leave and Absence to correct this error after approving leave and absence records in the **Work items assigned to me** list.</span></span>

### <a name="unable-to-recall-an-image-workflow"></a><span data-ttu-id="94700-116">Не удается вызвать workflow-процесс изображения</span><span class="sxs-lookup"><span data-stu-id="94700-116">Unable to recall an image workflow</span></span>

<span data-ttu-id="94700-117">После отзыва workflow-процесса изображения workflow-процесс будет задано значение "отменен" и существующий запрос может быть удален из рабочей области самообслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="94700-117">After recalling an image workflow, the workflow will be set to "cancelled" and the existing request can be deleted in the employee self-service workspace.</span></span>

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a><span data-ttu-id="94700-118">Повторно принятые на работу сотрудники или подрядчики отображаются несколько раз после увольнения</span><span class="sxs-lookup"><span data-stu-id="94700-118">Rehired employees or contractors show up multiple times after termination</span></span> 

<span data-ttu-id="94700-119">С этим обновлением уволенные сотрудники, которые были повторно приняты на работу, будут отображаться только один раз в списке уволенных.</span><span class="sxs-lookup"><span data-stu-id="94700-119">With this update, terminated employees that are rehired will only display one time in the exited list.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="94700-120">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="94700-120">Known issue</span></span>

- <span data-ttu-id="94700-121">**Проблема**: при добавлении нового вложения для работника кнопки **Создать** и **Изменить** неактивны.</span><span class="sxs-lookup"><span data-stu-id="94700-121">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="94700-122">**Временное решение:** перед открытием страницы вложения убедитесь, что информационные панели на странице **Рабочий** закрыты.</span><span class="sxs-lookup"><span data-stu-id="94700-122">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="94700-123">Если информационные панели закрыты при загрузке страницы **Работник**, кнопки вложений будут активны.</span><span class="sxs-lookup"><span data-stu-id="94700-123">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="94700-124">(Эта проблема будет исправлена в следующем обновлении платформы.)</span><span class="sxs-lookup"><span data-stu-id="94700-124">(This issue will be fixed in the next platform update.)</span></span>
