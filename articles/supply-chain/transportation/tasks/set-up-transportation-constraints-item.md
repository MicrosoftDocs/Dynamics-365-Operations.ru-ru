---
title: Настройка ограничений по транспортировке для номенклатуры
description: В этой процедуре показано, как настроить ограничение по транспортировке для предотвращения транспортировки выбранной номенклатуры через выбранный узел.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSConstraint, InventLocationIdLookup, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e2ff8458a9821e1aa2ae8d2dc93cc89cfc318d70
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233567"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="0cf20-103">Настройка ограничений по транспортировке для номенклатуры</span><span class="sxs-lookup"><span data-stu-id="0cf20-103">Set up transportation constraints for an item</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0cf20-104">В этой процедуре показано, как настроить ограничение по транспортировке для предотвращения транспортировки выбранной номенклатуры через выбранный узел.</span><span class="sxs-lookup"><span data-stu-id="0cf20-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="0cf20-105">Обычно эту задачу выполняет координатор транспортировки.</span><span class="sxs-lookup"><span data-stu-id="0cf20-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="0cf20-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="0cf20-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="0cf20-107">Создание ограничения номенклатуры</span><span class="sxs-lookup"><span data-stu-id="0cf20-107">Create an item constaint</span></span>
1. <span data-ttu-id="0cf20-108">Перейдите в раздел "Ограничения".</span><span class="sxs-lookup"><span data-stu-id="0cf20-108">Go to Constraints.</span></span>
2. <span data-ttu-id="0cf20-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="0cf20-109">Click New.</span></span>
3. <span data-ttu-id="0cf20-110">В поле "Ограничение номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="0cf20-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="0cf20-111">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="0cf20-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0cf20-112">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="0cf20-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="0cf20-113">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="0cf20-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="0cf20-114">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="0cf20-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="0cf20-115">В поле "Узел" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="0cf20-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="0cf20-116">В поле "Действие ограничения" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="0cf20-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="0cf20-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="0cf20-117">Click Save.</span></span>
11. <span data-ttu-id="0cf20-118">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="0cf20-118">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]