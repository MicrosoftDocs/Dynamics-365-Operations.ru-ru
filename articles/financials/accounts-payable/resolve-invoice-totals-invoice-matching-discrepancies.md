---
title: Обзор устранения несоответствий во время сопоставления итогов по накладным
description: Сопоставление итогов накладных можно использовать, чтобы гарантировать, чтобы итоги накладных не отличаются от ожидаемых сумм более чем на допустимое отклонение.
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4a20368385ec43547ee3d29770bd83cdec47e4a
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864950"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching-overview"></a><span data-ttu-id="cadca-103">Обзор устранения несоответствий во время сопоставления итогов по накладным</span><span class="sxs-lookup"><span data-stu-id="cadca-103">Resolve discrepancies during invoice totals matching overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cadca-104">Один из типов валидации сопоставления накладных — это сопоставление итогов по накладным.</span><span class="sxs-lookup"><span data-stu-id="cadca-104">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="cadca-105">Чтобы указать, что система должна выполнять сопоставление итогов по накладным, на странице **Параметры модуля расчетов с поставщиками** на вкладке **Проверка накладной** установите параметр **Сопоставлять итоги по накладным** в значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="cadca-105">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="cadca-106">Сопоставление итогов накладных можно использовать, чтобы гарантировать, чтобы итоги накладных не отличаются от ожидаемых сумм более чем на допустимое отклонение.</span><span class="sxs-lookup"><span data-stu-id="cadca-106">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="cadca-107">На странице **Сведения о сопоставлении итогов по накладнымs** сравнивается шесть итогов.</span><span class="sxs-lookup"><span data-stu-id="cadca-107">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="cadca-108">Если какой-либо из итогов отличается от ожидаемого соответствующего итога по заказа ну покупку, несоответствие помечается флагом.</span><span class="sxs-lookup"><span data-stu-id="cadca-108">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="cadca-109">Чтобы просмотреть накладную, в которой обнаружены несоответствия при сопоставлении итогов, в рабочей области **Запись накладной поставщика** щелкните плитку **Накладные, ожидающие обработки**.</span><span class="sxs-lookup"><span data-stu-id="cadca-109">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="cadca-110">Затем на панели операций на вкладке **Просмотр** щелкните **Сведения о сопоставлении**.</span><span class="sxs-lookup"><span data-stu-id="cadca-110">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="cadca-111">Если при сопоставлении обнаружены несоответствия, рядом с суммой накладной отображаются значки-предупреждения.</span><span class="sxs-lookup"><span data-stu-id="cadca-111">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="cadca-112">Просмотреть дополнительные сведения об итогах можно, просмотрев сведения о сопоставлении итогов по накладной.</span><span class="sxs-lookup"><span data-stu-id="cadca-112">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="cadca-113">После выявления расхождения может возникнуть необходимость обратиться к поставщику, если вы считаете, что данные в накладной ошибочны.</span><span class="sxs-lookup"><span data-stu-id="cadca-113">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="cadca-114">В зависимости от результата переговоров с поставщиком вы можете выполнить одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="cadca-114">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="cadca-115">Принять расхождение в цене и разнести накладную с расхождениями сопоставления.</span><span class="sxs-lookup"><span data-stu-id="cadca-115">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="cadca-116">Ваша система может быть настроена так, что разноска при наличии расхождений сопоставления будет требовать утверждения.</span><span class="sxs-lookup"><span data-stu-id="cadca-116">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="cadca-117">В этом случае вы должны утвердить расхождение сопоставления; при желании можно ввести комментарий к утверждению.</span><span class="sxs-lookup"><span data-stu-id="cadca-117">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="cadca-118">После этого накладную можно будет разнести.</span><span class="sxs-lookup"><span data-stu-id="cadca-118">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="cadca-119">Изменить сумму накладной на ожидаемую и разнести накладную.</span><span class="sxs-lookup"><span data-stu-id="cadca-119">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="cadca-120">Запросить у поставщика полный зачет и новую, исправленную накладную.</span><span class="sxs-lookup"><span data-stu-id="cadca-120">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="cadca-121">Дополнительные сведения см. в разделе [Рассмотрение и разрешение исключений](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="cadca-121">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>


