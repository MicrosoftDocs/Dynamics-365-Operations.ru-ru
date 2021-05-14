---
title: Вес должен быть положительным
description: Вес должен быть положительным
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924311"
---
# <a name="weight-must-be-positive"></a><span data-ttu-id="1337e-103">Вес должен быть положительным</span><span class="sxs-lookup"><span data-stu-id="1337e-103">Weight must be positive</span></span>

<span data-ttu-id="1337e-104">Код ошибки: WeightMustBePositive</span><span class="sxs-lookup"><span data-stu-id="1337e-104">Error code: WeightMustBePositive</span></span>

## <a name="symptoms"></a><span data-ttu-id="1337e-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="1337e-105">Symptoms</span></span>

<span data-ttu-id="1337e-106">Система отобразит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="1337e-106">The system shows the following error message:</span></span>

> <span data-ttu-id="1337e-107">Вес должен быть положительным.</span><span class="sxs-lookup"><span data-stu-id="1337e-107">Weight must be positive.</span></span>

## <a name="cause"></a><span data-ttu-id="1337e-108">Причина</span><span class="sxs-lookup"><span data-stu-id="1337e-108">Cause</span></span>

<span data-ttu-id="1337e-109">В поле **Вес брутто** установлено значение *0* (ноль) или отрицательное значение.</span><span class="sxs-lookup"><span data-stu-id="1337e-109">The **Gross Weight** field is set to *0* (zero) or a negative value.</span></span>

## <a name="resolution"></a><span data-ttu-id="1337e-110">Приказ</span><span class="sxs-lookup"><span data-stu-id="1337e-110">Resolution</span></span>

<span data-ttu-id="1337e-111">Чтобы указать вес, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="1337e-111">To specify a weight, follow one of these steps.</span></span>

- <span data-ttu-id="1337e-112">В поле **Вес брутто** задайте значение.</span><span class="sxs-lookup"><span data-stu-id="1337e-112">In the **Gross weight** field, set a value.</span></span> <span data-ttu-id="1337e-113">Затем выберите единицу измерения из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="1337e-113">Then select a unit in the drop-down list.</span></span>
- <span data-ttu-id="1337e-114">Выберите **Получить вес системы** для расчета значения **Вес брутто**.</span><span class="sxs-lookup"><span data-stu-id="1337e-114">Select **Get system weight** to calculate the **Gross weight** value.</span></span>
