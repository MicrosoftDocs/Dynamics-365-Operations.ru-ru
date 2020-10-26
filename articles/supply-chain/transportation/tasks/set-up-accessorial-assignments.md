---
title: Настройка дополнительных назначений
description: В этой процедуре показано, как настроить назначение дополнения.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f0ea4a3914b7214dcceb22595809eaa3118a0ca
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987288"
---
# <a name="set-up-accessorial-assignments"></a><span data-ttu-id="39117-103">Настройка дополнительных назначений</span><span class="sxs-lookup"><span data-stu-id="39117-103">Set up accessorial assignments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="39117-104">В этой процедуре показано, как настроить назначение дополнения.</span><span class="sxs-lookup"><span data-stu-id="39117-104">This procedure shows how to set up an accessorial assignment.</span></span> <span data-ttu-id="39117-105">Обычно это делает координатор транспортировки.</span><span class="sxs-lookup"><span data-stu-id="39117-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="39117-106">Перед использованием этого руководства необходимо выполнить руководство "Настройка дополнительных расходов и справочников дополнений для узла".</span><span class="sxs-lookup"><span data-stu-id="39117-106">Before you use this guide you need to run the "Set up hub accessorial charges and accessorial masters" guide.</span></span>


## <a name="set-up-accessorial-assignment"></a><span data-ttu-id="39117-107">Настройка дополнительного назначения</span><span class="sxs-lookup"><span data-stu-id="39117-107">Set up Accessorial assignment</span></span>
1. <span data-ttu-id="39117-108">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Расчет ставок" > "Дополнительные назначения".</span><span class="sxs-lookup"><span data-stu-id="39117-108">Go to Transportation management > Setup > Rating > Accessorial assignments.</span></span>
2. <span data-ttu-id="39117-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="39117-109">Click New.</span></span>
3. <span data-ttu-id="39117-110">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="39117-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="39117-111">Переключите развертывание раздела "Подробности".</span><span class="sxs-lookup"><span data-stu-id="39117-111">Toggle the expansion of the Details section.</span></span>
5. <span data-ttu-id="39117-112">В поле "Узел" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="39117-112">In the Hub field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="39117-113">Выберите в списке узел, который вы создали в качестве при выполнении руководства "Настройка дополнительных расходов и справочников дополнений для узла".</span><span class="sxs-lookup"><span data-stu-id="39117-113">In the list, select the Hub that you created an accessorial master for when you ran the "Set up hub accessorial charges and accessorial masters" guide.</span></span> 
7. <span data-ttu-id="39117-114">В поле "Код дополнительного узла" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="39117-114">In the Hub accessorial ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="39117-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="39117-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="39117-116">Переключите развертывание раздела "Критерии".</span><span class="sxs-lookup"><span data-stu-id="39117-116">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="39117-117">В разделе "Критерии" можно выбрать точные критерии того, когда должен применяться сбор, в зависимости от различных предложенных здесь значений.</span><span class="sxs-lookup"><span data-stu-id="39117-117">In the Criteria section you can choose the exact criteria for when the charge should apply, based on the different values offered here.</span></span>  
10. <span data-ttu-id="39117-118">Установите параметр "Применять всегда" в значение "Да".</span><span class="sxs-lookup"><span data-stu-id="39117-118">Set the Always apply option to Yes.</span></span>
11. <span data-ttu-id="39117-119">В поле "Уровень дополнительной встречи" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="39117-119">In the Accessorial assignment level field, select an option.</span></span>
12. <span data-ttu-id="39117-120">Переключите развертывание раздела "Расчет".</span><span class="sxs-lookup"><span data-stu-id="39117-120">Toggle the expansion of the Calculation section.</span></span>
13. <span data-ttu-id="39117-121">В поле "Тип дополнительного сбора" выберите "Фиксированная".</span><span class="sxs-lookup"><span data-stu-id="39117-121">In the Accessorial fee type field, select 'Flat'.</span></span>
    * <span data-ttu-id="39117-122">Тип дополнительного сбора определяет, как рассчитывается фактическая сумма сбора.</span><span class="sxs-lookup"><span data-stu-id="39117-122">The Accessorial fee type determines how to calculate the actual charge.</span></span> <span data-ttu-id="39117-123">В данном примере это фиксированный сбор.</span><span class="sxs-lookup"><span data-stu-id="39117-123">In this example it's a flat charge.</span></span>  
14. <span data-ttu-id="39117-124">В поле "Дополнительный сбор" введите число.</span><span class="sxs-lookup"><span data-stu-id="39117-124">In the Accessorial fee field, enter a number.</span></span>
15. <span data-ttu-id="39117-125">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="39117-125">Click Save.</span></span>

