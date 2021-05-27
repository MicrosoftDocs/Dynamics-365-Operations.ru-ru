---
title: После запроса изменения добавление строки в заявку на покупку невозможно
description: Система не позволяет добавлять строку в заявку на покупку после запроса изменения.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchReqTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: jeyao
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5dbb55a6a352a7acf16729c1cfe1afdac2e2eef8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026852"
---
# <a name="you-cant-add-a-line-to-a-purchase-requisition-after-you-request-a-change"></a><span data-ttu-id="2dd66-103">После запроса изменения добавление строки в заявку на покупку невозможно</span><span class="sxs-lookup"><span data-stu-id="2dd66-103">You can't add a line to a purchase requisition after you request a change</span></span>

<span data-ttu-id="2dd66-104">Номер статьи базы знаний: 4611211</span><span class="sxs-lookup"><span data-stu-id="2dd66-104">KB number: 4611211</span></span>

## <a name="symptoms"></a><span data-ttu-id="2dd66-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="2dd66-105">Symptoms</span></span>

<span data-ttu-id="2dd66-106">Система не позволяет добавлять строку в заявку на покупку после запроса изменения.</span><span class="sxs-lookup"><span data-stu-id="2dd66-106">The system doesn't allow you to add a line to a purchase requisition after you request a change.</span></span>

## <a name="resolution"></a><span data-ttu-id="2dd66-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="2dd66-107">Resolution</span></span>

<span data-ttu-id="2dd66-108">Необходимо отозвать рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="2dd66-108">You must recall the workflow.</span></span> <span data-ttu-id="2dd66-109">После того как заявка на покупку получает статус *Черновик*, ее можно продолжить редактировать или добавить к ней строку.</span><span class="sxs-lookup"><span data-stu-id="2dd66-109">After the purchase requisition is in *Draft* status, you can continue to edit it or add a line to it.</span></span>
