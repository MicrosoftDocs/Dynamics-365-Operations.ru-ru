---
title: Устранение неполадок непрерывного производства
description: В этом разделе описывается устранение проблем, которые могут встретиться при работе с непрерывным производством.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d999c91aa1cc14f29ebfa6be8e456e45ef0d3fa4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966188"
---
# <a name="troubleshoot-process-manufacturing"></a><span data-ttu-id="9756c-103">Устранение неполадок непрерывного производства</span><span class="sxs-lookup"><span data-stu-id="9756c-103">Troubleshoot process manufacturing</span></span>

<span data-ttu-id="9756c-104">В этом разделе описывается устранение проблем, которые могут встретиться при работе с непрерывным производством.</span><span class="sxs-lookup"><span data-stu-id="9756c-104">This topic describes how to fix issues that you might encounter while you work with process manufacturing.</span></span>

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a><span data-ttu-id="9756c-105">Когда используется устройство карты задания для отчета о частичном количестве по последнему заданию в производственном заказе, все предыдущие задания в этом заказе, имеющие статус "Выполняется", автоматически закрываются.</span><span class="sxs-lookup"><span data-stu-id="9756c-105">When I use the job card device to report a partial quantity on the last job in a production order, all the previous jobs on that order that have a status of In progress are automatically ended.</span></span>

<span data-ttu-id="9756c-106">Такое поведение предусмотрено разработчиками.</span><span class="sxs-lookup"><span data-stu-id="9756c-106">This behavior is by design.</span></span> <span data-ttu-id="9756c-107">На странице **Значения по умолчанию для производственного заказа** на вкладке **Приемка** имеется параметр, который называется **Метка конца маршрута**.</span><span class="sxs-lookup"><span data-stu-id="9756c-107">On the **Production order defaults** page, on the **Report as finished** tab, there is an option that is named **End-mark route**.</span></span> <span data-ttu-id="9756c-108">Если для этого раздела установлено значение *Да*, журнал карт маршрутов разносится, когда работник использует устройство карты задания или терминал карты задания для регистрации последней операции.</span><span class="sxs-lookup"><span data-stu-id="9756c-108">If this topic is set to *Yes*, a route card journal is posted when a worker uses the job card device or job card terminal to report the last operation.</span></span> <span data-ttu-id="9756c-109">Этот журнал помечает все операции как завершенные и завершает все производственные задания.</span><span class="sxs-lookup"><span data-stu-id="9756c-109">This journal marks all the operations as completed and ends all the production jobs.</span></span> <span data-ttu-id="9756c-110">Когда для параметра **Метка конца маршрута** установлено значение *Да*, система не учитывает статус задания, который выбран сотрудником при регистрации последней операции.</span><span class="sxs-lookup"><span data-stu-id="9756c-110">When the **End-mark route** option is set to *Yes*, the system doesn't consider the job status that the worker selected when they reported the last operation.</span></span> <span data-ttu-id="9756c-111">Кроме того, система не учитывает, сообщает ли работник о полном или частичном количестве.</span><span class="sxs-lookup"><span data-stu-id="9756c-111">The system also doesn't consider whether the worker is reporting a full or partial quantity.</span></span>

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a><span data-ttu-id="9756c-112">При попытке закрытия запасов получено следующее предупредительное сообщение: "Не было зарегистрировано выполнение вычисления backflush-расчета себестоимости с датой %1, соответствующее концу периода."</span><span class="sxs-lookup"><span data-stu-id="9756c-112">When I attempt a stock closing, I receive the following warning message: "No execution of Backflush costing calculation with a date %1 matching period end has been registered."</span></span>

<span data-ttu-id="9756c-113">В выпусках до выпуска 10.0.13 если не используется поток расчета себестоимости бережливого производства, при закрытии запасов выводится следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="9756c-113">In releases before release 10.0.13, if you aren't using the lean production costing flow, you receive the following erroneous warning message during inventory closing:</span></span>

> <span data-ttu-id="9756c-114">Вы собираетесь выполнить закрытие запасов с датой %1.</span><span class="sxs-lookup"><span data-stu-id="9756c-114">You are about to execute an Inventory close with a date %1.</span></span> <span data-ttu-id="9756c-115">Не было зарегистрировано выполнение вычисления backflush-расчета себестоимости с датой %1, соответствующее концу периода.</span><span class="sxs-lookup"><span data-stu-id="9756c-115">No execution of Backflush costing calculation with a date %1 matching period end has been registered.</span></span> <span data-ttu-id="9756c-116">Не забудьте выполнить вычисление backflush-расчета себестоимости с датой %1, соответствующее концу периода.</span><span class="sxs-lookup"><span data-stu-id="9756c-116">Please remember to execute a Backflush costing calculation with a date of %1 matching period end.</span></span> <span data-ttu-id="9756c-117">Оценка стоимости запасов, себестоимости проданных товаров и отклонений может быть неверна в субкниге или в главной книге до тех пор, пока оно не будет выполнено.</span><span class="sxs-lookup"><span data-stu-id="9756c-117">The valuation of inventories, cost of goods sold and variances might not be correct in Subledger or General ledger until this has been executed.</span></span>

<span data-ttu-id="9756c-118">Эта проблема исправлена в версии 10.0.13 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="9756c-118">This issue has been fixed in release 10.0.13 and later.</span></span> <span data-ttu-id="9756c-119">Дополнительные сведения см. в статье базы знаний [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span><span class="sxs-lookup"><span data-stu-id="9756c-119">For more information, see [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span></span>
