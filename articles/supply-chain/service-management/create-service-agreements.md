---
title: Создание соглашения на обслуживание
description: В этом разделе описаны способы использования функций в модулях "Управление сервисным обслуживанием" и "Управление и учет по проектам" для создания соглашений о сервисном обслуживании.
author: ShylaThompson
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a094ce9f0d9323b089055e74d41cf1f45323a7d4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "310952"
---
# <a name="create-service-agreements"></a><span data-ttu-id="d384e-103">Создание соглашения на обслуживание</span><span class="sxs-lookup"><span data-stu-id="d384e-103">Create service agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d384e-104">В этом разделе описаны способы использования функций в модулях "Управление сервисным обслуживанием" и "Управление и учет по проектам" для создания соглашений о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="d384e-104">This topic describes how to use features in the Service management and the Project management and accounting modules to create service agreements.</span></span>

## <a name="create-a-service-agreement-from-service-management"></a><span data-ttu-id="d384e-105">Создание соглашения о сервисном обслуживании из модуля управления сервисным обслуживанием</span><span class="sxs-lookup"><span data-stu-id="d384e-105">Create a service agreement from Service management</span></span>

1. <span data-ttu-id="d384e-106">Перейдите к модулю **Управление сервисным обслуживанием**.</span><span class="sxs-lookup"><span data-stu-id="d384e-106">Navigate to **Service management**.</span></span>
2. <span data-ttu-id="d384e-107">Нажмите кнопку **Соглашения на обслуживание** для создания новой строки соглашения о сервисном обслуживании в заголовке страницы.</span><span class="sxs-lookup"><span data-stu-id="d384e-107">Click **Service agreements** to create a new service agreement line in the page header.</span></span> 
3. <span data-ttu-id="d384e-108">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d384e-108">Click **New**.</span></span> <span data-ttu-id="d384e-109">Введите описание, выберите ссылку на проект в поле **Код проекта** и заполните остальные поля и строки соглашения о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="d384e-109">Enter a description, select a reference to a project in the **Project ID** field, and fill in the rest of the fields and lines for the service agreement.</span></span> <span data-ttu-id="d384e-110">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d384e-110">Click **Save**.</span></span>
4. <span data-ttu-id="d384e-111">Перейдите на вкладку **Отношения** и выберите **Объекты обслуживания** или **Задачи обслуживания** для создания связей объектов сервисного обслуживания или связей задач сервисного обслуживания для соглашения о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="d384e-111">On the **Relations** tab, select **Service objects** or **Service tasks** to create service object relations or service task relations for the service agreement.</span></span> <span data-ttu-id="d384e-112">Объекты и задачи обслуживания, для которых вы создали связи, можно приложить в строках соглашения на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d384e-112">The service objects and tasks that you have created relations for can be attached on the lines of the service agreement.</span></span>
5. <span data-ttu-id="d384e-113">В нижней половине страницы создайте строки соглашения на обслуживание посредством копирования строк из шаблона обслуживания или другого соглашения на обслуживание или вручную.</span><span class="sxs-lookup"><span data-stu-id="d384e-113">In the lower half of the page, create service agreement lines by copying lines from a service template, another service agreement, or manually creating the service-agreement lines.</span></span>

> [!NOTE]
> <span data-ttu-id="d384e-114">При копировании строк в соглашение на обслуживание из другого соглашения на обслуживание можно указать, хотите ли вы копировать связи объектов или задач обслуживания.</span><span class="sxs-lookup"><span data-stu-id="d384e-114">If you copy lines into the service agreement from another service agreement, you can indicate whether you also want to copy service object and service task relations.</span></span> <span data-ttu-id="d384e-115">При копировании этих связей они добавляются к существующим связям в соглашении на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d384e-115">If you copy these relations, they are added to any existing relations on the service agreement.</span></span> <span data-ttu-id="d384e-116">При копировании строк соглашения на обслуживание из шаблона обслуживания связи объектов и задач обслуживания автоматически копируются в качестве связей объектов и задач обслуживания в новые строки соглашения на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d384e-116">If you copy service-agreement lines from a service template, the service-object and service-task relations are automatically copied as service-object relations and service-task relations on the new service-agreement lines.</span></span>

## <a name="create-service-agreement-lines-manually"></a><span data-ttu-id="d384e-117">Создание строк соглашения на обслуживание вручную</span><span class="sxs-lookup"><span data-stu-id="d384e-117">Create service agreement lines manually</span></span>

1. <span data-ttu-id="d384e-118">На странице **Соглашения на обслуживание** добавьте строку соглашения на обслуживание в таблицу строк.</span><span class="sxs-lookup"><span data-stu-id="d384e-118">From the **Service agreements** page, add a service agreement line in the lines grid.</span></span> 
2. <span data-ttu-id="d384e-119">Введите соответствующую информацию в строку соглашения на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d384e-119">Enter the appropriate information for the service agreement line.</span></span> 
3. <span data-ttu-id="d384e-120">Нажмите сочетание клавиш **CTRL+S**, чтобы сохранить строку, а затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d384e-120">Press **CTRL+S** to save the line, and then close the page.</span></span>

## <a name="create-a-service-agreement-from-project"></a><span data-ttu-id="d384e-121">Создание соглашения на обслуживание из модуля Проект</span><span class="sxs-lookup"><span data-stu-id="d384e-121">Create a service agreement from Project</span></span>

1. <span data-ttu-id="d384e-122">Щелкните **Управление и учет по проектам**.</span><span class="sxs-lookup"><span data-stu-id="d384e-122">Click **Project management and accounting**.</span></span>
2. <span data-ttu-id="d384e-123">Щелкните **Все проекты**.</span><span class="sxs-lookup"><span data-stu-id="d384e-123">Click **All projects**.</span></span>
3. <span data-ttu-id="d384e-124">Выберите проект в списке.</span><span class="sxs-lookup"><span data-stu-id="d384e-124">Select the project from the list.</span></span>
4. <span data-ttu-id="d384e-125">В области **Панель операций** щелкните **Управлять**.</span><span class="sxs-lookup"><span data-stu-id="d384e-125">On the **Action Pane**, click **Manage**.</span></span> <span data-ttu-id="d384e-126">В группе действий **Создать** щелкните **Сервисное обслуживание** и выберите **Соглашение о сервисном обслуживании**.</span><span class="sxs-lookup"><span data-stu-id="d384e-126">In the **New** Action group, click **Service** and select **Service agreement**.</span></span>
5. <span data-ttu-id="d384e-127">Следуйте шагам в разделе **Создание соглашения на обслуживание**, как описано ранее в этом разделе, чтобы ввести ссылку на проект.</span><span class="sxs-lookup"><span data-stu-id="d384e-127">Follow the steps in the section titled **Create a service agreement** as described earlier in this topic to enter the project reference.</span></span>


## <a name="related-topics"></a><span data-ttu-id="d384e-128">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="d384e-128">Related topics</span></span>

[<span data-ttu-id="d384e-129">Соглашения на обслуживание</span><span class="sxs-lookup"><span data-stu-id="d384e-129">Service agreements</span></span>](service-agreements.md)


