---
title: Создание прогнозных моделей для бюджетов проекта
description: В этом разделе описывается создание прогнозной модели для оставшихся бюджетов.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321787"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="f6fb2-103">Создание прогнозных моделей для бюджетов проекта</span><span class="sxs-lookup"><span data-stu-id="f6fb2-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6fb2-104">В этом разделе описывается создание прогнозной модели для оставшихся бюджетов.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="f6fb2-105">Проект, подлежащий бюджетному контролю, использует два типа бюджетов: исходный и остаток.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="f6fb2-106">При создании бюджета проекта необходимо указать модели прогноза исходного бюджета и остатка бюджета, которые были созданы в на странице **Прогнозные модели**.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="f6fb2-107">Бюджеты проекта на основе указанных моделей создаются при отправке бюджета проекта.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="f6fb2-108">Прогнозная модель, используемая для бюджетного контроля, не может иметь подмодели, и ее нельзя использовать в качестве подмодели.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="f6fb2-109">Выберите **Управление и учет по проектам** > **Настройка** > **Прогнозы**  > **Прогнозные модели**.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="f6fb2-110">Выберите **Создать** , чтобы создать новую прогнозную модель, а затем введите ИД модели и ее имя.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="f6fb2-111">Для параметра **Остановлено** введите значение **Да**, чтобы исключить любые изменения в строках прогноза для прогнозной модели.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="f6fb2-112">Если строки прогноза, с которыми связана модель, должны создавать прогнозы движения денежных средств в главной книге, для параметра **Включить бюджеты в прогнозы движения денежных средств** установите значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="f6fb2-113">Чтобы использовать дату проекта в качестве даты накладной, для параметра **Прогнозировать дату накладной** установите значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="f6fb2-114">В поле **Тип бюджета** выберите один из следующих типов моделей:</span><span class="sxs-lookup"><span data-stu-id="f6fb2-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="f6fb2-115">**Исходный бюджет** - используйте этот тип модели для сумм первоначального бюджета, которые отправляются, когда создается и утверждается исходный бюджет.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="f6fb2-116">**Остаток бюджета** - этот тип модели предназначен для сумм остатков бюджета во время срока службы проекта.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="f6fb2-117">Сальдо в этой модели прогноза уменьшаются на размер фактических проводок и увеличиваются или уменьшаются версиями бюджета.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="f6fb2-118">**Перенесенный бюджет** - этот тип предназначен для сумм перенесенного бюджета для проекта.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="f6fb2-119">Перенос — необязательный процесс, который можно выполнить для переноса неиспользованных сумм бюджета из одного финансового года в другой.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="f6fb2-120">При необходимости задайте следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="f6fb2-120">Set the following options as required:</span></span>

   - <span data-ttu-id="f6fb2-121">Включите **Прогнозировать дату накладной**, чтобы использовать дату проекта в качестве даты накладной.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="f6fb2-122">Включите **Прогноз с НЗП**, чтобы строить прогноз на основе незавершенного производства (НЗП), а затем выберите тип НЗП.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="f6fb2-123">В поле **Тип бюджета** можно оставить значение **Нет** по умолчанию или ввести новый тип.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="f6fb2-124">Тип бюджета нельзя изменить после изменения записи.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="f6fb2-125">При изменении типа бюджета по умолчанию все остальные параметры будут недоступны для обновления, и вы не сможете повторно использовать эту прогнозную модель.</span><span class="sxs-lookup"><span data-stu-id="f6fb2-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

