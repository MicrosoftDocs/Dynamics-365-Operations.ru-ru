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
ms.search.form: BenefitFutureLifeEvents
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 134152bb8ae2b9f42b59cc9202e244435a607eba
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230093"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="c72c1-103">Настройка событий будущего</span><span class="sxs-lookup"><span data-stu-id="c72c1-103">Configure future life events</span></span>

<span data-ttu-id="c72c1-104">Можно планировать будущие жизненные события в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c72c1-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="c72c1-105">В рабочей области **Управление льготами** в разделе **Настройка** выберите **Будущие жизненные события**.</span><span class="sxs-lookup"><span data-stu-id="c72c1-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="c72c1-106">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="c72c1-106">Select **New**.</span></span>

3. <span data-ttu-id="c72c1-107">Укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="c72c1-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="c72c1-108">Поле</span><span class="sxs-lookup"><span data-stu-id="c72c1-108">Field</span></span> | <span data-ttu-id="c72c1-109">Описание</span><span class="sxs-lookup"><span data-stu-id="c72c1-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c72c1-110">Дата жизненного события</span><span class="sxs-lookup"><span data-stu-id="c72c1-110">Life event date</span></span> | <span data-ttu-id="c72c1-111">Система обрабатывает все события в течение периода регистрации, которые выполняются до этой даты.</span><span class="sxs-lookup"><span data-stu-id="c72c1-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="c72c1-112">Жизненное событие зарегистрировано</span><span class="sxs-lookup"><span data-stu-id="c72c1-112">Life event logged</span></span> | <span data-ttu-id="c72c1-113">Дата и время внесения жизненного события в журнал.</span><span class="sxs-lookup"><span data-stu-id="c72c1-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="c72c1-114">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="c72c1-114">Log type</span></span> | <span data-ttu-id="c72c1-115">Показывает, является ли действие одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="c72c1-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="c72c1-116">- **Обновить** — изменение существующей записи, которая отслеживает жизненные события</span><span class="sxs-lookup"><span data-stu-id="c72c1-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="c72c1-117">- **Вставить** — создание новой записи о жизненном событии</span><span class="sxs-lookup"><span data-stu-id="c72c1-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="c72c1-118">Идентификатор типа жизненного события</span><span class="sxs-lookup"><span data-stu-id="c72c1-118">Life event type ID</span></span> | <span data-ttu-id="c72c1-119">Уникальный код типа жизненного события.</span><span class="sxs-lookup"><span data-stu-id="c72c1-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="c72c1-120">Тип жизненного события</span><span class="sxs-lookup"><span data-stu-id="c72c1-120">Life event type</span></span> | <span data-ttu-id="c72c1-121">Катализатор для обновления регистрации льгот сотрудника.</span><span class="sxs-lookup"><span data-stu-id="c72c1-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="c72c1-122">Дополнительные сведения см. в разделе триггеров жизненных событий.</span><span class="sxs-lookup"><span data-stu-id="c72c1-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="c72c1-123">Состояние</span><span class="sxs-lookup"><span data-stu-id="c72c1-123">Status</span></span> | <span data-ttu-id="c72c1-124">Обработано ли жизненное событие или нет.</span><span class="sxs-lookup"><span data-stu-id="c72c1-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="c72c1-125">Линейная</span><span class="sxs-lookup"><span data-stu-id="c72c1-125">Line</span></span> | <span data-ttu-id="c72c1-126">Номер строки будущего жизненного события.</span><span class="sxs-lookup"><span data-stu-id="c72c1-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="c72c1-127">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c72c1-127">Select **Save**.</span></span> 
