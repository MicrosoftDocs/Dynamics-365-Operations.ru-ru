---
title: Передача основного средства
description: В этом руководстве по задаче показано, как переместить финансовые сведения для журнала основных средств из одного набора финансовых аналитик в новый набор финансовых аналитик.
author: saraschi2
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7588e0058713d7facf053aa269210fc88e5a3ff2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823892"
---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="aa213-103">Передача основного средства</span><span class="sxs-lookup"><span data-stu-id="aa213-103">Transfer a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa213-104">В этом руководстве по задаче показано, как переместить финансовые сведения для журнала основных средств из одного набора финансовых аналитик в новый набор финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="aa213-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="aa213-105">В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="aa213-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="aa213-106">В области перехода, перейдите к **Модули > Фиксированные активы > Фиксированные активы > Фиксированные активы**.</span><span class="sxs-lookup"><span data-stu-id="aa213-106">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="aa213-107">Найдите в списке основное средство для переноса и выберите его.</span><span class="sxs-lookup"><span data-stu-id="aa213-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="aa213-108">На панели операций щелкните **Основное средство**.</span><span class="sxs-lookup"><span data-stu-id="aa213-108">On the Action Pane, click **Fixed asset**.</span></span>
4. <span data-ttu-id="aa213-109">Щелкните **Перемещение основных средств**.</span><span class="sxs-lookup"><span data-stu-id="aa213-109">Click **Transfer fixed assets**.</span></span>
5. <span data-ttu-id="aa213-110">В поле **Дата перемещения** введите дату.</span><span class="sxs-lookup"><span data-stu-id="aa213-110">In the **Transfer date** field, enter a date.</span></span>
6. <span data-ttu-id="aa213-111">Введите комментарии для описания переноса.</span><span class="sxs-lookup"><span data-stu-id="aa213-111">Enter comments to describe the transfer.</span></span>
    
    <span data-ttu-id="aa213-112">В этом списке отображаются все книги для основного средства.</span><span class="sxs-lookup"><span data-stu-id="aa213-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="aa213-113">Пометьте книги, которые необходимо перенести в новый набор финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="aa213-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="aa213-114">В этом списке отображаются существующие значения финансовых аналитик для выбранной книги.</span><span class="sxs-lookup"><span data-stu-id="aa213-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="aa213-115">Выберите финансовую аналитику, которую требуется обновить для выбранного журнала основных средств.</span><span class="sxs-lookup"><span data-stu-id="aa213-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="aa213-116">В поле **Финансовая аналитика** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="aa213-116">In the **Financial dimension** field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="aa213-117">Установите другие значения финансовых аналитик при необходимости.</span><span class="sxs-lookup"><span data-stu-id="aa213-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="aa213-118">Все значения финансовой аналитики изменяются при переносе независимо от того, было ли введено значение или нет.</span><span class="sxs-lookup"><span data-stu-id="aa213-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="aa213-119">Например, если было введено значение для параметра BusinessUnit, а финансовые аналитики CostCenter и Department оставлены пустыми.</span><span class="sxs-lookup"><span data-stu-id="aa213-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="aa213-120">Если структура счета допускает пустые значения для параметров CostCenter и Department, в результате переноса в каждой модели стоимости будет указано новое значение для BusinessUnit и пустое значение для CostCenter и Department.</span><span class="sxs-lookup"><span data-stu-id="aa213-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="aa213-121">Щелкните **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="aa213-121">Click **Update**.</span></span>
    * <span data-ttu-id="aa213-122">Имеется возможность просмотреть изменения до оформления переноса.</span><span class="sxs-lookup"><span data-stu-id="aa213-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="aa213-123">Просмотрите результаты перед переносом журналов основных средств.</span><span class="sxs-lookup"><span data-stu-id="aa213-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="aa213-124">Щелкните **Перенести**.</span><span class="sxs-lookup"><span data-stu-id="aa213-124">Click **Transfer**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]