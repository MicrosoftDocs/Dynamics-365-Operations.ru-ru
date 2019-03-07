---
title: Создание шаблона записи для облегчения ввода данных
description: В этой процедуре демонстрируется, как создать шаблон записи, чтобы значения полей, которые используются часто, не требовалось вводить явно для каждой новой записи.
author: margoc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36d14c386322adab0cc0ba9b7b47c874aefbe519
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "315989"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="52a4a-103">Создание шаблона записи для облегчения ввода данных</span><span class="sxs-lookup"><span data-stu-id="52a4a-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="52a4a-104">В этой процедуре демонстрируется, как создать шаблон записи, чтобы значения полей, которые используются часто, не требовалось вводить явно для каждой новой записи.</span><span class="sxs-lookup"><span data-stu-id="52a4a-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="52a4a-105">В этой процедуре предстоит создать новую запись для новых ноутбуков, которые должны быть добавлены к ОС.</span><span class="sxs-lookup"><span data-stu-id="52a4a-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="52a4a-106">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="52a4a-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="52a4a-107">Перейдите в раздел "Основные средства" > "Основные средства" > "Основные средства".</span><span class="sxs-lookup"><span data-stu-id="52a4a-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="52a4a-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="52a4a-108">Click New.</span></span>
3. <span data-ttu-id="52a4a-109">В поле "Группа ОС" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="52a4a-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="52a4a-110">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="52a4a-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="52a4a-111">Например, введите "Ноутбук корпоративного интереса".</span><span class="sxs-lookup"><span data-stu-id="52a4a-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="52a4a-112">В поле "Краткое наименование" введите значение.</span><span class="sxs-lookup"><span data-stu-id="52a4a-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="52a4a-113">Например, введите "ноутбук".</span><span class="sxs-lookup"><span data-stu-id="52a4a-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="52a4a-114">Разверните раздел "Техническая информация".</span><span class="sxs-lookup"><span data-stu-id="52a4a-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="52a4a-115">В поле "Марка" введите значение.</span><span class="sxs-lookup"><span data-stu-id="52a4a-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="52a4a-116">В поле "Модель" введите значение.</span><span class="sxs-lookup"><span data-stu-id="52a4a-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="52a4a-117">В поле "Год модели" введите значение.</span><span class="sxs-lookup"><span data-stu-id="52a4a-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="52a4a-118">В области действий щелкните "Параметры".</span><span class="sxs-lookup"><span data-stu-id="52a4a-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="52a4a-119">Щелкните "Сведения о записи".</span><span class="sxs-lookup"><span data-stu-id="52a4a-119">Click Record info.</span></span>
12. <span data-ttu-id="52a4a-120">Щелкните "Шаблон пользователя".</span><span class="sxs-lookup"><span data-stu-id="52a4a-120">Click User template.</span></span>
13. <span data-ttu-id="52a4a-121">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="52a4a-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="52a4a-122">Например, введите "Корпоративный ноутбук".</span><span class="sxs-lookup"><span data-stu-id="52a4a-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="52a4a-123">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="52a4a-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="52a4a-124">Например, введите "Корпоративный ноутбук".</span><span class="sxs-lookup"><span data-stu-id="52a4a-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="52a4a-125">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="52a4a-125">Click OK.</span></span>
16. <span data-ttu-id="52a4a-126">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="52a4a-126">Click Close.</span></span>

