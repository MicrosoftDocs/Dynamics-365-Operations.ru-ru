---
title: "Что нового и что изменилось в Dynamics 365 for Talent Core HR (1 октября 2018 г.)"
description: "В этой теме описываются новые и измененные компоненты в текущем выпуске Microsoft Dynamics 365 for Talent Core HR."
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: 97820cd25ece48dc0b8045d9ba509d0971ca5aad
ms.contentlocale: ru-ru
ms.lasthandoff: 10/01/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-1-2018"></a><span data-ttu-id="cd014-103">Что нового и что изменилось в Dynamics 365 for Talent Core HR (1 октября 2018 г.)</span><span class="sxs-lookup"><span data-stu-id="cd014-103">What's new or changed in Dynamics 365 for Talent Core HR (October 1, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cd014-104">**Сборка 8.1.1035.0**</span><span class="sxs-lookup"><span data-stu-id="cd014-104">**Build 8.1.1035.0**</span></span>

<span data-ttu-id="cd014-105">В этой теме описываются новые и измененные компоненты Core HR.</span><span class="sxs-lookup"><span data-stu-id="cd014-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="turn-off-electronic-payment-validation"></a><span data-ttu-id="cd014-106">Отключение проверки электронных платежей</span><span class="sxs-lookup"><span data-stu-id="cd014-106">Turn off electronic payment validation</span></span>

<span data-ttu-id="cd014-107">Проверка информации электронных платежей имеет место при настройке выплат для прямого депозита либо с помощью рабочей области **Самообслуживание сотрудников**, либо непосредственно в форме "Сотрудник".</span><span class="sxs-lookup"><span data-stu-id="cd014-107">Electronic payment information validation occurs if you set up disbursements for direct deposit either through **Employee self-service** workspace (ESS) or directly on the employee form.</span></span> <span data-ttu-id="cd014-108">Этот параметр дает вам возможность отключить эту проверку, если вам не требуется проверять суммы и значения остатков.</span><span class="sxs-lookup"><span data-stu-id="cd014-108">This option gives you the flexibility to remove that validation if you do not require the validation checks for amounts and remainder values.</span></span> <span data-ttu-id="cd014-109">Эта полезно, если у вас есть интеграция с внешней системой обработки заработной платы, которая предъявляет другие требования.</span><span class="sxs-lookup"><span data-stu-id="cd014-109">This feature is helpful if you're integrating with an external payroll system that has different requirements.</span></span>

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a><span data-ttu-id="cd014-110">Портал самообслуживания менеджеров — добавление целей для участников группы посредством плитки "Групповые цели производительности"</span><span class="sxs-lookup"><span data-stu-id="cd014-110">Manager self-service - Add goals for team members through the Team performance goals tile</span></span>

<span data-ttu-id="cd014-111">До этого выпуска менеджеры могли добавлять цели для своих сотрудников по отдельности посредством целей производительности, связанных с каждым сотрудником.</span><span class="sxs-lookup"><span data-stu-id="cd014-111">Prior to this release, managers can add goals to their employees individually through the performance goals associated to each employee.</span></span> <span data-ttu-id="cd014-112">С этим обновлением менеджеры получают доступ к плитке **Групповые цели производительности** и могут создавать новые цели путем выбора любого из своих непосредственных подчиненных.</span><span class="sxs-lookup"><span data-stu-id="cd014-112">With this update, managers can access the **Team performance goals** tile and create new goals by selecting any of their direct reports.</span></span>

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a><span data-ttu-id="cd014-113">Портал самообслуживания менеджеров — добавление оценок для участников группы посредством плитки "Оценка групповой производительности"</span><span class="sxs-lookup"><span data-stu-id="cd014-113">Manager self-service - Add reviews for team members through the Team performance reviews tile</span></span>

<span data-ttu-id="cd014-114">До этого выпуска менеджеры могли добавлять оценки для своих сотрудников по отдельности посредством оценок, связанных с каждым сотрудником.</span><span class="sxs-lookup"><span data-stu-id="cd014-114">Prior to this release, managers can add reviews to their employees individually through the reviews associated to each employee.</span></span> <span data-ttu-id="cd014-115">С этим обновлением менеджеры получают доступ к плитке **Оценка групповой производительности** и могут создавать новые оценки путем выбора любого из своих непосредственных подчиненных.</span><span class="sxs-lookup"><span data-stu-id="cd014-115">With this update, managers can access the **Team performance reviews** tile and create new reviews by selecting any of their direct reports.</span></span>

## <a name="configure-proration-options-by-leave-plan"></a><span data-ttu-id="cd014-116">Настройка параметров пропорционального распределения по плану отпусков</span><span class="sxs-lookup"><span data-stu-id="cd014-116">Configure proration options by leave plan</span></span>

<span data-ttu-id="cd014-117">Организации назначают отпуска по-разному в зависимости от того, когда сотрудники приходят в компанию и покидают ее.</span><span class="sxs-lookup"><span data-stu-id="cd014-117">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="cd014-118">В некоторых организациях сотрудники получают все выделенное им время в день начала работы, тогда как в других оно распределяется пропорциональным образом.</span><span class="sxs-lookup"><span data-stu-id="cd014-118">For some organizations, employees are awarded their full allocation on their start date while others prorate the award.</span></span> <span data-ttu-id="cd014-119">В этом выпуске предусмотрены новые параметры для пропорционального распределения времени отпуска и начислений для людей, которые только поступили на работу в организацию или увольняются из нее.</span><span class="sxs-lookup"><span data-stu-id="cd014-119">New options are provided in this release to choose how to prorate the awards and accruals for joiners and leavers in an organization.</span></span> <span data-ttu-id="cd014-120">Возможные значения: пропорционально, полное начисление, без начисления.</span><span class="sxs-lookup"><span data-stu-id="cd014-120">Options include: Prorated, Full accrual, and No accrual.</span></span>

## <a name="other-changes"></a><span data-ttu-id="cd014-121">Другие изменения</span><span class="sxs-lookup"><span data-stu-id="cd014-121">Other changes</span></span>

-   <span data-ttu-id="cd014-122">Обновлен объект "Сотрудник" — **Обращение** теперь можно обновлять с помощью надстройки Excel/управления данными.</span><span class="sxs-lookup"><span data-stu-id="cd014-122">Employee entity updated - The **Personal** title can now be updated using the Excel add-in/data management.</span></span>

-   <span data-ttu-id="cd014-123">Изменение правд доступа для разрешения удаления кнопок **Удалить** и **Деактивировать** на портале самообслуживания сотрудников для платежной информации.</span><span class="sxs-lookup"><span data-stu-id="cd014-123">Security change to allow removal of the **Delete** and **Deactivate** buttons in employee self-service for payment information.</span></span>

## <a name="known-issue"></a><span data-ttu-id="cd014-124">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="cd014-124">Known issue</span></span>

-   <span data-ttu-id="cd014-125">**Проблема:** при добавлении нового вложения в работника кнопки **Создать** и **Редактировать** неактивны. **Обход:** перед открытием страницы вложения убедитесь, что информационные панели на странице **Работник** закрыты.</span><span class="sxs-lookup"><span data-stu-id="cd014-125">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="cd014-126">Если информационные панели закрыты при загрузке страницы **Работник**, кнопки **Вложения** будут активны.</span><span class="sxs-lookup"><span data-stu-id="cd014-126">If the FactBoxes are closed when the **Worker** page is loaded, the **Attachments** buttons will be enabled.</span></span> <span data-ttu-id="cd014-127">(Эта проблема будет исправлена в следующем обновлении платформы.)</span><span class="sxs-lookup"><span data-stu-id="cd014-127">(This issue will be fixed in the next platform update.)</span></span>

