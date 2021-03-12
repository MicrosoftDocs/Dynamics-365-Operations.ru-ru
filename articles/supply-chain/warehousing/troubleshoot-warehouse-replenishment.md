---
title: Устранение неполадок пополнения склада
description: В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с пополнением склада в Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7748a18d2b6f612b3ac9ac1a75efb6ae5f13859a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993903"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="5f436-103">Устранение неполадок пополнения склада</span><span class="sxs-lookup"><span data-stu-id="5f436-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f436-104">В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с пополнением склада в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5f436-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="5f436-105">Я получаю следующее сообщение об ошибке: "Код работы %1 не может быть разблокирован, поскольку у него есть незаконченная работу по пополнению".</span><span class="sxs-lookup"><span data-stu-id="5f436-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="5f436-106">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="5f436-106">Issue description</span></span>

<span data-ttu-id="5f436-107">Работа по комплектации заблокирована из-за зависимой работы пополнения.</span><span class="sxs-lookup"><span data-stu-id="5f436-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5f436-108">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="5f436-108">Issue resolution</span></span>

<span data-ttu-id="5f436-109">При использовании пополнения по спросу волны, если местонахождение комплектации должно быть пополнено для удовлетворения спроса по исходному заказу, система создает и работу пополнения, и работу комплектации.</span><span class="sxs-lookup"><span data-stu-id="5f436-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="5f436-110">Однако она блокирует работу комплектации, пока не будет завершена работа пополнения.</span><span class="sxs-lookup"><span data-stu-id="5f436-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="5f436-111">Такое поведение является умышленным, поскольку местонахождение комплектации не имеет достаточного количества запасов, если только работа по пополнению не завершена.</span><span class="sxs-lookup"><span data-stu-id="5f436-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="5f436-112">Выполните работу по пополнению, а затем обработайте работу комплектации.</span><span class="sxs-lookup"><span data-stu-id="5f436-112">Complete the replenishment work, and then process the picking work.</span></span>
