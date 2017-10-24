---
title: "Устранение несоответствий во время сопоставления итогов по накладным"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3f7e1261838866688c97529b0edfa1354034247b
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a><span data-ttu-id="99604-102">Устранение несоответствий во время сопоставления итогов по накладным</span><span class="sxs-lookup"><span data-stu-id="99604-102">Resolve discrepancies during invoice totals matching</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="99604-103">Один из типов валидации сопоставления накладных — это сопоставление итогов по накладным.</span><span class="sxs-lookup"><span data-stu-id="99604-103">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="99604-104">Чтобы указать, что система должна выполнять сопоставление итогов по накладным, на странице **Параметры модуля расчетов с поставщиками** на вкладке **Проверка накладной** установите параметр **Сопоставлять итоги по накладным** в значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="99604-104">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="99604-105">Сопоставление итогов накладных можно использовать, чтобы гарантировать, чтобы итоги накладных не отличаются от ожидаемых сумм более чем на допустимое отклонение.</span><span class="sxs-lookup"><span data-stu-id="99604-105">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="99604-106">На странице **Сведения о сопоставлении итогов по накладнымs** сравнивается шесть итогов.</span><span class="sxs-lookup"><span data-stu-id="99604-106">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="99604-107">Если какой-либо из итогов отличается от ожидаемого соответствующего итога по заказа ну покупку, несоответствие помечается флагом.</span><span class="sxs-lookup"><span data-stu-id="99604-107">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="99604-108">Чтобы просмотреть накладную, в которой обнаружены несоответствия при сопоставлении итогов, в рабочей области **Запись накладной поставщика** щелкните плитку **Накладные, ожидающие обработки**.</span><span class="sxs-lookup"><span data-stu-id="99604-108">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="99604-109">Затем на панели операций на вкладке **Просмотр** щелкните **Сведения о сопоставлении**.</span><span class="sxs-lookup"><span data-stu-id="99604-109">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="99604-110">Если при сопоставлении обнаружены несоответствия, рядом с суммой накладной отображаются значки-предупреждения.</span><span class="sxs-lookup"><span data-stu-id="99604-110">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="99604-111">Просмотреть дополнительные сведения об итогах можно, просмотрев сведения о сопоставлении итогов по накладной.</span><span class="sxs-lookup"><span data-stu-id="99604-111">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="99604-112">После выявления расхождения может возникнуть необходимость обратиться к поставщику, если вы считаете, что данные в накладной ошибочны.</span><span class="sxs-lookup"><span data-stu-id="99604-112">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="99604-113">В зависимости от результата переговоров с поставщиком вы можете выполнить одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="99604-113">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="99604-114">Принять расхождение в цене и разнести накладную с расхождениями сопоставления.</span><span class="sxs-lookup"><span data-stu-id="99604-114">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="99604-115">Ваша система может быть настроена так, что разноска при наличии расхождений сопоставления будет требовать утверждения.</span><span class="sxs-lookup"><span data-stu-id="99604-115">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="99604-116">В этом случае вы должны утвердить расхождение сопоставления; при желании можно ввести комментарий к утверждению.</span><span class="sxs-lookup"><span data-stu-id="99604-116">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="99604-117">После этого накладную можно будет разнести.</span><span class="sxs-lookup"><span data-stu-id="99604-117">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="99604-118">Изменить сумму накладной на ожидаемую и разнести накладную.</span><span class="sxs-lookup"><span data-stu-id="99604-118">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="99604-119">Запросить у поставщика полный зачет и новую, исправленную накладную.</span><span class="sxs-lookup"><span data-stu-id="99604-119">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="99604-120">Дополнительные сведения см. в разделе [Рассмотрение и разрешение исключений](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="99604-120">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>



