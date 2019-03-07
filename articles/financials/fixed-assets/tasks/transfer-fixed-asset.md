---
title: Передача основного средства
description: В этом руководстве по задаче показано, как переместить финансовые сведения для журнала основных средств из одного набора финансовых аналитик в новый набор финансовых аналитик.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb8a5b94d9a0bb510daa2a698524e0c380597991
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "357205"
---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="e0708-103">Передача основного средства</span><span class="sxs-lookup"><span data-stu-id="e0708-103">Transfer a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e0708-104">В этом руководстве по задаче показано, как переместить финансовые сведения для журнала основных средств из одного набора финансовых аналитик в новый набор финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="e0708-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="e0708-105">В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="e0708-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="e0708-106">Перейдите в раздел "Основные средства" > "Основные средства" > "Основные средства".</span><span class="sxs-lookup"><span data-stu-id="e0708-106">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="e0708-107">Найдите в списке основное средство для переноса и выберите его.</span><span class="sxs-lookup"><span data-stu-id="e0708-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="e0708-108">В области действий щелкните "Основное средство".</span><span class="sxs-lookup"><span data-stu-id="e0708-108">On the Action Pane, click Fixed asset.</span></span>
4. <span data-ttu-id="e0708-109">Щелкните "Перенос основных средств".</span><span class="sxs-lookup"><span data-stu-id="e0708-109">Click Transfer fixed assets.</span></span>
5. <span data-ttu-id="e0708-110">В поле "Дата переноса" введите дату.</span><span class="sxs-lookup"><span data-stu-id="e0708-110">In the Transfer date field, enter a date.</span></span>
6. <span data-ttu-id="e0708-111">Введите комментарии для описания переноса.</span><span class="sxs-lookup"><span data-stu-id="e0708-111">Enter comments to describe the transfer.</span></span>
    * <span data-ttu-id="e0708-112">В этом списке отображаются все книги для основного средства.</span><span class="sxs-lookup"><span data-stu-id="e0708-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="e0708-113">Пометьте книги, которые необходимо перенести в новый набор финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="e0708-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="e0708-114">В этом списке отображаются существующие значения финансовых аналитик для выбранной книги.</span><span class="sxs-lookup"><span data-stu-id="e0708-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="e0708-115">Выберите финансовую аналитику, которую требуется обновить для выбранного журнала основных средств.</span><span class="sxs-lookup"><span data-stu-id="e0708-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="e0708-116">В поле "Финансовая аналитика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e0708-116">In the Financial dimension field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="e0708-117">Установите другие значения финансовых аналитик при необходимости.</span><span class="sxs-lookup"><span data-stu-id="e0708-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="e0708-118">Все значения финансовой аналитики изменяются при переносе независимо от того, было ли введено значение или нет.</span><span class="sxs-lookup"><span data-stu-id="e0708-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="e0708-119">Например, если было введено значение для параметра BusinessUnit, а финансовые аналитики CostCenter и Department оставлены пустыми.</span><span class="sxs-lookup"><span data-stu-id="e0708-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="e0708-120">Если структура счета допускает пустые значения для параметров CostCenter и Department, в результате переноса в каждой модели стоимости будет указано новое значение для BusinessUnit и пустое значение для CostCenter и Department.</span><span class="sxs-lookup"><span data-stu-id="e0708-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="e0708-121">Щелкните Обновить.</span><span class="sxs-lookup"><span data-stu-id="e0708-121">Click Update.</span></span>
    * <span data-ttu-id="e0708-122">Имеется возможность просмотреть изменения до оформления переноса.</span><span class="sxs-lookup"><span data-stu-id="e0708-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="e0708-123">Просмотрите результаты перед переносом журналов основных средств.</span><span class="sxs-lookup"><span data-stu-id="e0708-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="e0708-124">Щелкните Перенести.</span><span class="sxs-lookup"><span data-stu-id="e0708-124">Click Transfer.</span></span>

