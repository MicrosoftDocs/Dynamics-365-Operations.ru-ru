---
title: Профиль местоположения запрещает отрицательные запасы, но отрицательные запасы в наличии разрешаются
description: Параметр "Разрешить отрицательные запасы" для профиля местоположения имеет значение "Нет", но система по-прежнему допускает отрицательные запасы в наличии.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026845"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a><span data-ttu-id="3581f-103">Профиль местоположения запрещает отрицательные запасы, но отрицательные запасы в наличии разрешаются</span><span class="sxs-lookup"><span data-stu-id="3581f-103">Location profile disallows negative inventory, but negative on-hand inventory is permitted</span></span>

<span data-ttu-id="3581f-104">Номер статьи базы знаний: 4613622</span><span class="sxs-lookup"><span data-stu-id="3581f-104">KB number: 4613622</span></span>

## <a name="symptoms"></a><span data-ttu-id="3581f-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="3581f-105">Symptoms</span></span>

<span data-ttu-id="3581f-106">Параметр **Разрешить отрицательные запасы** для профиля местоположения имеет значение *Нет*, но система по-прежнему допускает отрицательные запасы в наличии.</span><span class="sxs-lookup"><span data-stu-id="3581f-106">The **Allow negative inventory** option for the location profile is set to *No*, but the system still allows negative on-hand inventory.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="3581f-107">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="3581f-107">Example scenario</span></span>

<span data-ttu-id="3581f-108">Для регулируемых правительством проводок система должна иметь возможность записи отрицательных запасов в убытки журнала.</span><span class="sxs-lookup"><span data-stu-id="3581f-108">For government-regulated transactions, the system must be able to record negative inventory to book losses.</span></span> <span data-ttu-id="3581f-109">Требуется, чтобы номенклатура отображала отрицательные запасы, но только в определенных местоположениях, таких как "баки".</span><span class="sxs-lookup"><span data-stu-id="3581f-109">You want an item to be able to show negative inventory, but only in designated locations, such as tanks.</span></span> <span data-ttu-id="3581f-110">Однако, если группа номенклатурных моделей разрешает отрицательные запасы, можно обнаружить, что не имеет значения, разрешены ли для местоположения отрицательные запасы.</span><span class="sxs-lookup"><span data-stu-id="3581f-110">However, if the item model group allows negative inventory, you find that it doesn't matter whether the location is set to allow negative inventory.</span></span> <span data-ttu-id="3581f-111">Если номенклатура настроена так, что отрицательные запасы не разрешены, не имеет значения, каким образом настроен профиль местоположения.</span><span class="sxs-lookup"><span data-stu-id="3581f-111">If the item is set up so that negative inventory isn't allowed, it doesn't matter how the location profile is set up.</span></span>

## <a name="resolution"></a><span data-ttu-id="3581f-112">Приказ</span><span class="sxs-lookup"><span data-stu-id="3581f-112">Resolution</span></span>

<span data-ttu-id="3581f-113">Параметр **Разрешить отрицательные запасы** из профиля местоположения применяется только к складским процессам, таким как комплектация.</span><span class="sxs-lookup"><span data-stu-id="3581f-113">The **Allow negative inventory** setting from the location profile applies only to warehouse processes, such as picking.</span></span> <span data-ttu-id="3581f-114">Однако группы номенклатурных моделей, которые настроены на разрешение отрицательных запасов, влияют на все процессы модуля управления запасами и управления складом, а профиль местоположения не переопределяет настройку.</span><span class="sxs-lookup"><span data-stu-id="3581f-114">However, item model groups that are set to allow negative inventory affect all processes from the Inventory management and Warehouse management modules, and the location profile won't override the setting.</span></span>

<span data-ttu-id="3581f-115">Можно указать, разрешены ли отрицательные запасы на складе.</span><span class="sxs-lookup"><span data-stu-id="3581f-115">You can control whether a warehouse is allowed to carry negative inventory.</span></span> <span data-ttu-id="3581f-116">Настройте группы моделей номенклатуры таким образом, чтобы запретить отрицательные физические запасы, и установите только соответствующий склад, чтобы разрешить отрицательные запасы.</span><span class="sxs-lookup"><span data-stu-id="3581f-116">Set your item model groups to disallow negative physical inventory, and set only the relevant warehouse to allow negative inventory.</span></span>
