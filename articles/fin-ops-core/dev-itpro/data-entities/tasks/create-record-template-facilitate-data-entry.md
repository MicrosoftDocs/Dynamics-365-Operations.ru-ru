---
title: Создание шаблона записи для облегчения ввода данных
description: В этой теме демонстрируется, как создать шаблон записи, чтобы значения полей, которые используются часто, не требовалось вводить явно для каждой новой записи.
author: margoc
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec21415158ad611d0ad55778e76aa128f53561bd
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143392"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="1ae03-103">Создание шаблона записи для облегчения ввода данных</span><span class="sxs-lookup"><span data-stu-id="1ae03-103">Create a record template to facilitate data entry</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1ae03-104">В этой теме демонстрируется, как создать шаблон записи, чтобы значения полей, которые используются часто, не требовалось вводить явно для каждой новой записи.</span><span class="sxs-lookup"><span data-stu-id="1ae03-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="1ae03-105">В этой процедуре предстоит создать новую запись для новых ноутбуков, которые должны быть добавлены к ОС.</span><span class="sxs-lookup"><span data-stu-id="1ae03-105">In this procedure, you'll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="1ae03-106">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="1ae03-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="1ae03-107">В области перехода, перейдите к **Модули > Фиксированные активы > Фиксированные активы > Фиксированные активы**.</span><span class="sxs-lookup"><span data-stu-id="1ae03-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="1ae03-108">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1ae03-108">Select **New**.</span></span>
3. <span data-ttu-id="1ae03-109">В поле **Группа ОС** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1ae03-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="1ae03-110">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1ae03-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="1ae03-111">Например, введите **Ноутбук корпоративного интереса**.</span><span class="sxs-lookup"><span data-stu-id="1ae03-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="1ae03-112">В поле **Краткое наименование** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1ae03-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="1ae03-113">Например, введите **ноутбук**.</span><span class="sxs-lookup"><span data-stu-id="1ae03-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="1ae03-114">Разверните раздел **Техническая информация**.</span><span class="sxs-lookup"><span data-stu-id="1ae03-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="1ae03-115">В полях **Марка**, **Модель** и **Модельный год** введите значения.</span><span class="sxs-lookup"><span data-stu-id="1ae03-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="1ae03-116">В области панели операций выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="1ae03-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="1ae03-117">Выберите **Сведения о записи**.</span><span class="sxs-lookup"><span data-stu-id="1ae03-117">Select **Record info**.</span></span>
10. <span data-ttu-id="1ae03-118">Выберите **Шаблон пользователя**.</span><span class="sxs-lookup"><span data-stu-id="1ae03-118">Select **User template**.</span></span>
11. <span data-ttu-id="1ae03-119">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1ae03-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="1ae03-120">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1ae03-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="1ae03-121">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1ae03-121">Select **OK**.</span></span>
14. <span data-ttu-id="1ae03-122">Выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="1ae03-122">Select **Close**.</span></span>

