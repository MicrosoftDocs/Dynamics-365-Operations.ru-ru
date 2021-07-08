---
title: Рабочие процессы сделок управления ретробонусами
description: В этой теме объясняется, как настроить рабочий процесс сделок управления ретробонусами для утверждения и активации сделок.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 8436842b4f07ba000649075198bdef43ad508f8f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270965"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="75777-103">Рабочие процессы сделок управления ретробонусами</span><span class="sxs-lookup"><span data-stu-id="75777-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75777-104">Для утверждения сделок ретробонусов в управлении бонусами используется та же платформа рабочих процессов, что и в других приложениях Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="75777-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="75777-105">С каждым рабочим процессом связаны для процесса заданий:</span><span class="sxs-lookup"><span data-stu-id="75777-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="75777-106">Один элемент рабочего процесса утверждает сделку.</span><span class="sxs-lookup"><span data-stu-id="75777-106">One element of the workflow approves the deal.</span></span>
- <span data-ttu-id="75777-107">Один элемент рабочего процесса активирует сделку, чтобы пользователь или рабочий процесс мог утвердить проводки.</span><span class="sxs-lookup"><span data-stu-id="75777-107">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>

<span data-ttu-id="75777-108">Прежде чем можно будет использовать сделку ретробонусов, она должна быть активна в модуле **Управление ретробонусами**.</span><span class="sxs-lookup"><span data-stu-id="75777-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="75777-109">Чтобы активировать сделку, необходимо сначала создать и настроить *Рабочий процесс управления ретробонусами*.</span><span class="sxs-lookup"><span data-stu-id="75777-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="75777-110">Пользователи не могут утверждать сделки вручную.</span><span class="sxs-lookup"><span data-stu-id="75777-110">Users can't manually approve deals.</span></span> <span data-ttu-id="75777-111">Этот рабочий процесс должен использоваться всегда.</span><span class="sxs-lookup"><span data-stu-id="75777-111">The workflow must always be used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="75777-112">Создание рабочих процессов сделок управления ретробонусами и управление ими</span><span class="sxs-lookup"><span data-stu-id="75777-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="75777-113">Для работы с вашими рабочими процессами сделок управления ретробонусами перейдите в раздел **Управление ретробонусами \> Настройка \> Рабочие процессы управления ретробонусами**.</span><span class="sxs-lookup"><span data-stu-id="75777-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="75777-114">Там можно просмотреть, создать и обновить рабочие процессы, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="75777-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="75777-115">В каждый момент времени может быть активен только один рабочий процесс этого типа.</span><span class="sxs-lookup"><span data-stu-id="75777-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="75777-116">Дополнительные сведения о рабочих процессах, работе со страницей **Рабочие процессы управления ретробонусами** и создании рабочих процессов см. в разделе [Обзор системы рабочих процессов](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) и связанных с ним разделах.</span><span class="sxs-lookup"><span data-stu-id="75777-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="75777-117">Использование рабочего процесса для активации сделки</span><span class="sxs-lookup"><span data-stu-id="75777-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="75777-118">Чтобы активировать сделку через рабочий процесс, откройте эту сделку (например, на странице **Все сделки управления ретробонусами**).</span><span class="sxs-lookup"><span data-stu-id="75777-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="75777-119">Затем на панели операций выберите **Рабочий процесс \> Отправить**.</span><span class="sxs-lookup"><span data-stu-id="75777-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="75777-120">После того как новая сделка была обработана и утверждена в рамках рабочего процесса, она будет активна и готова к использованию.</span><span class="sxs-lookup"><span data-stu-id="75777-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="75777-121">После активации сделки изменить большую часть настроек невозможно.</span><span class="sxs-lookup"><span data-stu-id="75777-121">After a deal has been activated, you can't change most of its setup.</span></span> <span data-ttu-id="75777-122">Если необходимо изменить активную сделку, ее сначала следует деактивировать, а затем создать новую сделку.</span><span class="sxs-lookup"><span data-stu-id="75777-122">If you must change an active deal, first inactivate it, and then create a new deal.</span></span> <span data-ttu-id="75777-123">Если новая сделка будет похожа на старую, ее можно создать путем копирования старой сделки.</span><span class="sxs-lookup"><span data-stu-id="75777-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>

<span data-ttu-id="75777-124">Можно изменить следующие параметры для сделки после ее активации:</span><span class="sxs-lookup"><span data-stu-id="75777-124">You can change the following settings for a deal after it has been activated:</span></span>

- <span data-ttu-id="75777-125">Выверка по</span><span class="sxs-lookup"><span data-stu-id="75777-125">Reconcile by</span></span>
- <span data-ttu-id="75777-126">Кумулятивная гарантия</span><span class="sxs-lookup"><span data-stu-id="75777-126">Cumulative guarantee</span></span>
- <span data-ttu-id="75777-127">Профиль разноски</span><span class="sxs-lookup"><span data-stu-id="75777-127">Posting profile</span></span>
- <span data-ttu-id="75777-128">Профиль разноски для гарантии</span><span class="sxs-lookup"><span data-stu-id="75777-128">Posting profile for guarantee</span></span>
- <span data-ttu-id="75777-129">Примечания к документам</span><span class="sxs-lookup"><span data-stu-id="75777-129">Document notes</span></span>
- <span data-ttu-id="75777-130">Валютное</span><span class="sxs-lookup"><span data-stu-id="75777-130">Currency</span></span>
- <span data-ttu-id="75777-131">С даты</span><span class="sxs-lookup"><span data-stu-id="75777-131">From date</span></span>
- <span data-ttu-id="75777-132">По дату</span><span class="sxs-lookup"><span data-stu-id="75777-132">To date</span></span>

<span data-ttu-id="75777-133">Кроме того, можно удалить строки ретробонусов.</span><span class="sxs-lookup"><span data-stu-id="75777-133">In addition, rebate lines can be removed.</span></span>
