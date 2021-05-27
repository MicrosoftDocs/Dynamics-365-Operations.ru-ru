---
title: Непосредственно производный подтвержденный заказ обрабатывается в рамках рабочего процесса рассмотрения
description: Непосредственно производный подтвержденный заказ обрабатывается рабочим процессом со статусом "рассмотрение".
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026855"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a><span data-ttu-id="0a070-103">Непосредственно производный подтвержденный заказ обрабатывается в рамках рабочего процесса рассмотрения</span><span class="sxs-lookup"><span data-stu-id="0a070-103">Directly derived firmed orders are processed by an in-review workflow</span></span>

<span data-ttu-id="0a070-104">Номер статьи базы знаний: 4612450</span><span class="sxs-lookup"><span data-stu-id="0a070-104">KB number: 4612450</span></span>

## <a name="symptoms"></a><span data-ttu-id="0a070-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="0a070-105">Symptoms</span></span>

<span data-ttu-id="0a070-106">Непосредственно производный подтвержденный заказ обрабатывается рабочим процессом со статусом *Рассмотрение*.</span><span class="sxs-lookup"><span data-stu-id="0a070-106">Directly derived firmed orders are processed by a workflow that has a status of *In-review*.</span></span>

## <a name="resolution"></a><span data-ttu-id="0a070-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="0a070-107">Resolution</span></span>

<span data-ttu-id="0a070-108">Когда включено отслеживание изменений статус *На рассмотрении* назначается утвержденным производным заказам (субподрядным заказам на покупку).</span><span class="sxs-lookup"><span data-stu-id="0a070-108">When change tracking is enabled, a status of *In-review* is assigned to firmed derived orders (subcontract purchase orders).</span></span> <span data-ttu-id="0a070-109">Таким образом, если заказ на покупку является производным (заказ на покупку субподряда), он будет отправлен только в рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="0a070-109">Therefore, if a purchase order is derived (a subcontract purchase order), it's only submitted to a workflow.</span></span> <span data-ttu-id="0a070-110">Если заказ на покупку является утвержденным спланированным заказом на покупку, он автоматически утверждается, чтобы гарантировать, что механизм планирования не создает новые спланированные заказы, пока заказ на покупку остается в состоянии *Черновик*.</span><span class="sxs-lookup"><span data-stu-id="0a070-110">If a purchase order is a firmed planned purchase order, it's automatically approved to ensure that the planning engine doesn't create new planned orders while the purchase order is still in *Draft* status.</span></span>
