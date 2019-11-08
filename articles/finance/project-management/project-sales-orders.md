---
title: Заказы на продажу для проектов "Время и расходы"
description: В этом разделе объясняется, как создавать заказы на продажу на основе проекта для проектов времени и расходов.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 2f27e3e0a2d6aadc4c5224b55f8a416cbe4e83aa
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551210"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="382f0-103">Заказы на продажу для проектов "Время и расходы"</span><span class="sxs-lookup"><span data-stu-id="382f0-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="382f0-104">В этом разделе описывается, как создать заказ на продажу для проекта.</span><span class="sxs-lookup"><span data-stu-id="382f0-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="382f0-105">Заказы на продажу можно создавать только для проектов типа **Время и расходы**.</span><span class="sxs-lookup"><span data-stu-id="382f0-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="382f0-106">Если проект "время и расходы" имеет много источников финансирования в контакте проекта, необходимо включить параметр **Разрешить заказы на продажу для проектов с несколькими источниками финансирования** на странице **Параметры модуля "Управление и учет по проектам"**.</span><span class="sxs-lookup"><span data-stu-id="382f0-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="382f0-107">Поддержка заказов на продажу проекта с несколькими источниками финансирования доступна с версии приложения 10.0.2 и выше.</span><span class="sxs-lookup"><span data-stu-id="382f0-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="382f0-108">Параметр для включения поддержки для заказов на продажу проекта с несколькими источниками финансирования будет удален в волне выпусков в апреле 2020 года, после чего эта функция всегда будет включена.</span><span class="sxs-lookup"><span data-stu-id="382f0-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="382f0-109">Заказы на продажу на основе проекта можно создать двумя способами:</span><span class="sxs-lookup"><span data-stu-id="382f0-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="382f0-110">Перейдите в сам проект.</span><span class="sxs-lookup"><span data-stu-id="382f0-110">Go to the project itself.</span></span> <span data-ttu-id="382f0-111">В области действий выберите **Управление > Задачи номенклатуры > Заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="382f0-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="382f0-112">Сведения о проекте по умолчанию соответствуют заказу на продажу из проекта.</span><span class="sxs-lookup"><span data-stu-id="382f0-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="382f0-113">Если контракт по проекту имеет несколько источников финансирования, необходимо выбрать источник финансирования для настройки клиента для заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="382f0-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="382f0-114">Если имеется только один источник финансирования для проекта, клиент автоматически задается.</span><span class="sxs-lookup"><span data-stu-id="382f0-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="382f0-115">Перейдите на страницу **Все заказы на продажу** и создайте новый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="382f0-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="382f0-116">Необходимо выбрать проект для заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="382f0-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="382f0-117">После выбора проекта клиента устанавливается из источника финансирования или требуется выбрать источник финансирования, если контракт по проекту содержит несколько источников финансирования.</span><span class="sxs-lookup"><span data-stu-id="382f0-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

