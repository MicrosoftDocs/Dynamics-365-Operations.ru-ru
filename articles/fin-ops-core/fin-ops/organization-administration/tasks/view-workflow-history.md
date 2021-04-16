---
title: Просмотр истории бизнес-правила
description: В этом разделе описываются шаги для просмотра статуса документа, отправленного в систему workflow-процессов для обработки и утверждения.
author: jasongre
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 351f9c80eab8e9810fa6a4538f003eaef1a4a4fd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747233"
---
# <a name="view-workflow-history"></a><span data-ttu-id="c5702-103">Просмотр истории бизнес-правила</span><span class="sxs-lookup"><span data-stu-id="c5702-103">View workflow history</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c5702-104">В этом разделе описываются шаги для просмотра статуса документа, отправленного в систему workflow-процессов для обработки и утверждения.</span><span class="sxs-lookup"><span data-stu-id="c5702-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="c5702-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="c5702-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="c5702-106">Перейдите к **Область перехода > Модули > Общее > Запросы > Workflow-процесс > История workflow-процесса**.</span><span class="sxs-lookup"><span data-stu-id="c5702-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="c5702-107">Данная форма предназначена для просмотра статуса документа, отправленного в систему workflow-процессов для обработки и утверждения.</span><span class="sxs-lookup"><span data-stu-id="c5702-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="c5702-108">**Код экземпляра** — это идентификационный код экземпляра workflow-процесса, в рамках которого обрабатывается или обработан данный документ.</span><span class="sxs-lookup"><span data-stu-id="c5702-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="c5702-109">**Статус** — это статус workflow-процесса документа.</span><span class="sxs-lookup"><span data-stu-id="c5702-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="c5702-110">**Код workflow-процесса** — это идентификационный код workflow-процесса, в рамках которого обрабатывается или обработан данный документ.</span><span class="sxs-lookup"><span data-stu-id="c5702-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="c5702-111">**Документ** — это идентификационный код документа.</span><span class="sxs-lookup"><span data-stu-id="c5702-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="c5702-112">**Тип документа** — это тип документа, который был отправлен на обработку.</span><span class="sxs-lookup"><span data-stu-id="c5702-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="c5702-113">**Workflow-процесс** — это имя workflow-процесса, в рамках которого обрабатывается или обработан данный документ.</span><span class="sxs-lookup"><span data-stu-id="c5702-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="c5702-114">**Версия** — это номер версии workflow-процесса, в рамках которого обрабатывается или обработан данный документ.</span><span class="sxs-lookup"><span data-stu-id="c5702-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="c5702-115">**Дата и время создания** — это дата и время отправки документа.</span><span class="sxs-lookup"><span data-stu-id="c5702-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="c5702-116">**Затраченное время** — это время, прошедшее с момента отправки документа.</span><span class="sxs-lookup"><span data-stu-id="c5702-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="c5702-117">Кнопка **Возобновить** позволяет возобновить workflow-процесс для выбранного документа.</span><span class="sxs-lookup"><span data-stu-id="c5702-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="c5702-118">Кнопка **Отзыв** позволяет отозвать выбранный документ, чтобы он не обрабатывался.</span><span class="sxs-lookup"><span data-stu-id="c5702-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="c5702-119">В списке выберите ссылку в требуемой строке.</span><span class="sxs-lookup"><span data-stu-id="c5702-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="c5702-120">Убедитесь, что раздел **Рабочие элементы** развернут.</span><span class="sxs-lookup"><span data-stu-id="c5702-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="c5702-121">В этом разделе можно просмотреть рабочие элементы, которые связаны с выбранным документом.</span><span class="sxs-lookup"><span data-stu-id="c5702-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="c5702-122">Например, необходимо завершить задачу, либо документ должен быть утвержден.</span><span class="sxs-lookup"><span data-stu-id="c5702-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="c5702-123">Кнопка **Назначить повторно** откроет диалоговое окно, в котором имеется возможность повторно назначить рабочий элемент другому пользователю.</span><span class="sxs-lookup"><span data-stu-id="c5702-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="c5702-124">Убедитесь, что раздел **Отслеживание сведений** развернут.</span><span class="sxs-lookup"><span data-stu-id="c5702-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="c5702-125">В этом разделе можно просмотреть историю workflow-процесса для выбранного документа.</span><span class="sxs-lookup"><span data-stu-id="c5702-125">In this section you can view the workflow history of the selected document.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]