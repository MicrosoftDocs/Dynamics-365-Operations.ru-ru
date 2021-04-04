---
title: Создание шаблона записи для облегчения ввода данных
description: В этой теме демонстрируется, как создать шаблон записи, чтобы значения полей, которые используются часто, не требовалось вводить явно для каждой новой записи.
author: margoc
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d50dbb161fca0b0bfda18a258e5cef03e43fbeb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561106"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="f1c2d-103">Создание шаблона записи для облегчения ввода данных</span><span class="sxs-lookup"><span data-stu-id="f1c2d-103">Create a record template to facilitate data entry</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f1c2d-104">В этой теме демонстрируется, как создать шаблон записи, чтобы значения полей, которые используются часто, не требовалось вводить явно для каждой новой записи.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="f1c2d-105">В этой процедуре предстоит создать новую запись для новых ноутбуков, которые должны быть добавлены к ОС.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-105">In this procedure, you'll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="f1c2d-106">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="f1c2d-107">В области перехода, перейдите к **Модули > Фиксированные активы > Фиксированные активы > Фиксированные активы**.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="f1c2d-108">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-108">Select **New**.</span></span>
3. <span data-ttu-id="f1c2d-109">В поле **Группа ОС** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="f1c2d-110">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="f1c2d-111">Например, введите **Ноутбук корпоративного интереса**.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="f1c2d-112">В поле **Краткое наименование** введите значение.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="f1c2d-113">Например, введите **ноутбук**.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="f1c2d-114">Разверните раздел **Техническая информация**.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="f1c2d-115">В полях **Марка**, **Модель** и **Модельный год** введите значения.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="f1c2d-116">В области панели операций выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="f1c2d-117">Выберите **Сведения о записи**.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-117">Select **Record info**.</span></span>
10. <span data-ttu-id="f1c2d-118">Выберите **Шаблон пользователя**.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-118">Select **User template**.</span></span>
11. <span data-ttu-id="f1c2d-119">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="f1c2d-120">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="f1c2d-121">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-121">Select **OK**.</span></span>
14. <span data-ttu-id="f1c2d-122">Выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-122">Select **Close**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]