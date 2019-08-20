---
title: Настройка ограничений по транспортировке для номенклатуры
description: В этой процедуре показано, как настроить ограничение по транспортировке для предотвращения транспортировки выбранной номенклатуры через выбранный узел.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSConstraint, InventLocationIdLookup, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f686b29151cfbbeeffbf1f8fb98ea6ce5bc51d1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836077"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="94cfe-103">Настройка ограничений по транспортировке для номенклатуры</span><span class="sxs-lookup"><span data-stu-id="94cfe-103">Set up transportation constraints for an item</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="94cfe-104">В этой процедуре показано, как настроить ограничение по транспортировке для предотвращения транспортировки выбранной номенклатуры через выбранный узел.</span><span class="sxs-lookup"><span data-stu-id="94cfe-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="94cfe-105">Обычно эту задачу выполняет координатор транспортировки.</span><span class="sxs-lookup"><span data-stu-id="94cfe-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="94cfe-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="94cfe-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="94cfe-107">Создание ограничения номенклатуры</span><span class="sxs-lookup"><span data-stu-id="94cfe-107">Create an item constaint</span></span>
1. <span data-ttu-id="94cfe-108">Перейдите в раздел "Ограничения".</span><span class="sxs-lookup"><span data-stu-id="94cfe-108">Go to Constraints.</span></span>
2. <span data-ttu-id="94cfe-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="94cfe-109">Click New.</span></span>
3. <span data-ttu-id="94cfe-110">В поле "Ограничение номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="94cfe-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="94cfe-111">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="94cfe-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="94cfe-112">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="94cfe-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="94cfe-113">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="94cfe-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="94cfe-114">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="94cfe-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="94cfe-115">В поле "Узел" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="94cfe-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="94cfe-116">В поле "Действие ограничения" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="94cfe-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="94cfe-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="94cfe-117">Click Save.</span></span>
11. <span data-ttu-id="94cfe-118">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="94cfe-118">Close the page.</span></span>

