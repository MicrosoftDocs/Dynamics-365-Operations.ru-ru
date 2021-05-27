---
title: Ошибка возникает, когда местонахождение выбирается при регистрации отгрузочной накладной
description: Ошибка возникает, когда местонахождение выбирается при регистрации отгрузочной накладной.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026831"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a><span data-ttu-id="b6dbb-103">Ошибка возникает, когда местонахождение выбирается при регистрации отгрузочной накладной</span><span class="sxs-lookup"><span data-stu-id="b6dbb-103">An error occurs when the location is selected during picking list registration</span></span>

<span data-ttu-id="b6dbb-104">Номер статьи базы знаний: 4613106</span><span class="sxs-lookup"><span data-stu-id="b6dbb-104">KB number: 4613106</span></span>

## <a name="symptoms"></a><span data-ttu-id="b6dbb-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="b6dbb-105">Symptoms</span></span>

<span data-ttu-id="b6dbb-106">Эта проблема возникает, если система настроена для автоматического резервирования заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="b6dbb-106">This issue occurs when your system is configured to automatically reserve sales orders.</span></span> <span data-ttu-id="b6dbb-107">При попытке выбрать местоположение для строки регистрации отгрузочных накладных при использовании процессов резервирования управления складом (WMS) появится следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="b6dbb-107">If you try to select the location for a picking list registration line, you receive the following error message when you use warehouse management (WMS) reservation processes:</span></span>

> <span data-ttu-id="b6dbb-108">Невозможно обновить количество с учетом новых аналитик</span><span class="sxs-lookup"><span data-stu-id="b6dbb-108">Can't update quantity with new dimensions</span></span>

<span data-ttu-id="b6dbb-109">Эта проблема может возникнуть из-за того, что запасов в наличии не хватает в указанном месте.</span><span class="sxs-lookup"><span data-stu-id="b6dbb-109">This issue can occur because you don't have enough on-hand inventory at a specified location.</span></span>

## <a name="resolution"></a><span data-ttu-id="b6dbb-110">Приказ</span><span class="sxs-lookup"><span data-stu-id="b6dbb-110">Resolution</span></span>

<span data-ttu-id="b6dbb-111">Система работает в соответствии с разработанным поведением.</span><span class="sxs-lookup"><span data-stu-id="b6dbb-111">The system is behaving as designed.</span></span>

<span data-ttu-id="b6dbb-112">В сценариях, в которых используется процесс резервирования на уровне склада, если запасы в наличии не будут резервироваться для всех уровней складских аналитик и в указанном местоположении не хватает запасов в наличии, рекомендуется использовать процесс резервирования вручную из строки комплектации.</span><span class="sxs-lookup"><span data-stu-id="b6dbb-112">In scenarios where you use the warehouse-level reservation process, if the on-hand inventory won't be reserved on all inventory dimension levels, and you don't have enough on-hand inventory at a specified location, we recommend that you use the manual reservation process from the picking line.</span></span> <span data-ttu-id="b6dbb-113">Затем можно использовать функцию *Зарезервировать лот* для распределения нижних резервирований, таких как местоположение, для всех доступных в наличии количеств.</span><span class="sxs-lookup"><span data-stu-id="b6dbb-113">You can then use the *Reserve lot* function to distribute the lower reservations, such as location, for all the available on-hand quantities.</span></span>
