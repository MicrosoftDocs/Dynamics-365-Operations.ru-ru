---
title: Настройка событий будущего
description: Можно планировать будущие жизненные события в Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 78c65faa4ae0f428184700a912998e9dded026c5
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429413"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="9b688-103">Настройка событий будущего</span><span class="sxs-lookup"><span data-stu-id="9b688-103">Configure future life events</span></span>

<span data-ttu-id="9b688-104">Можно планировать будущие жизненные события в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9b688-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="9b688-105">В рабочей области **Управление льготами** в разделе **Настройка** выберите **Будущие жизненные события**.</span><span class="sxs-lookup"><span data-stu-id="9b688-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="9b688-106">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="9b688-106">Select **New**.</span></span>

3. <span data-ttu-id="9b688-107">Укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="9b688-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="9b688-108">Поле</span><span class="sxs-lookup"><span data-stu-id="9b688-108">Field</span></span> | <span data-ttu-id="9b688-109">Описание</span><span class="sxs-lookup"><span data-stu-id="9b688-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9b688-110">Дата жизненного события</span><span class="sxs-lookup"><span data-stu-id="9b688-110">Life event date</span></span> | <span data-ttu-id="9b688-111">Система обрабатывает все события в течение периода регистрации, которые выполняются до этой даты.</span><span class="sxs-lookup"><span data-stu-id="9b688-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="9b688-112">Жизненное событие зарегистрировано</span><span class="sxs-lookup"><span data-stu-id="9b688-112">Life event logged</span></span> | <span data-ttu-id="9b688-113">Дата и время внесения жизненного события в журнал.</span><span class="sxs-lookup"><span data-stu-id="9b688-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="9b688-114">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="9b688-114">Log type</span></span> | <span data-ttu-id="9b688-115">Показывает, является ли действие одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="9b688-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="9b688-116">- **Обновить** — изменение существующей записи, которая отслеживает жизненные события</span><span class="sxs-lookup"><span data-stu-id="9b688-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="9b688-117">- **Вставить** — создание новой записи о жизненном событии</span><span class="sxs-lookup"><span data-stu-id="9b688-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="9b688-118">Идентификатор типа жизненного события</span><span class="sxs-lookup"><span data-stu-id="9b688-118">Life event type ID</span></span> | <span data-ttu-id="9b688-119">Уникальный код типа жизненного события.</span><span class="sxs-lookup"><span data-stu-id="9b688-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="9b688-120">Тип жизненного события</span><span class="sxs-lookup"><span data-stu-id="9b688-120">Life event type</span></span> | <span data-ttu-id="9b688-121">Катализатор для обновления регистрации льгот сотрудника.</span><span class="sxs-lookup"><span data-stu-id="9b688-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="9b688-122">Дополнительные сведения см. в разделе триггеров жизненных событий.</span><span class="sxs-lookup"><span data-stu-id="9b688-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="9b688-123">Состояние</span><span class="sxs-lookup"><span data-stu-id="9b688-123">Status</span></span> | <span data-ttu-id="9b688-124">Обработано ли жизненное событие или нет.</span><span class="sxs-lookup"><span data-stu-id="9b688-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="9b688-125">Линейная</span><span class="sxs-lookup"><span data-stu-id="9b688-125">Line</span></span> | <span data-ttu-id="9b688-126">Номер строки будущего жизненного события.</span><span class="sxs-lookup"><span data-stu-id="9b688-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="9b688-127">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="9b688-127">Select **Save**.</span></span> 
