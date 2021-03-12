---
title: Счета разноски приобретения основных средств
description: В этой статье описывается, как настроить счета разноски ГК для приобретения активов.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa0d73790a20f3fe5bb76b87e635b1f16e034479
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976124"
---
# <a name="fixed-asset-acquisition-posting-accounts"></a><span data-ttu-id="3f020-103">Счета разноски приобретения основных средств</span><span class="sxs-lookup"><span data-stu-id="3f020-103">Fixed asset acquisition posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f020-104">В этой статье описывается, как настроить счета разноски ГК для приобретения активов.</span><span class="sxs-lookup"><span data-stu-id="3f020-104">This article explains how to set up general ledger posting accounts for acquiring assets.</span></span>

<span data-ttu-id="3f020-105">Счета, используемые для разноски приобретений основных средств, могут отличаться в зависимости от метода, используемого для приобретения основного средства.</span><span class="sxs-lookup"><span data-stu-id="3f020-105">Accounts used for posting fixed asset acquisitions may vary depending upon the method used to acquire the asset.</span></span> <span data-ttu-id="3f020-106">На странице "Профили разноски основных средств" на вкладке "Счета ГК" выберите значения "Приобретение" и "Корректировка приобретения", чтобы настроить счета основных средств для разноски в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="3f020-106">On the Fixed asset posting profiles page, on the Ledger accounts tab, select Acquisition and Acquisition adjustment to set up fixed asset accounts to post to the ledger.</span></span> 

<span data-ttu-id="3f020-107">В журналах и в заказах на покупку счет ГК обычно представляет собой балансовый счет, где стоимость приобретения новых основных средств дебетована.</span><span class="sxs-lookup"><span data-stu-id="3f020-107">In journals and on purchase orders, Ledger account is typically the balance sheet account, where the acquisition value of the new fixed asset is debited.</span></span> <span data-ttu-id="3f020-108">Этот счет не отображается в журнале и не может быть заменен в проводках.</span><span class="sxs-lookup"><span data-stu-id="3f020-108">This account is not displayed in the journal and cannot be replaced in transactions.</span></span> 

<span data-ttu-id="3f020-109">Корр. счет также является балансовым счетом.</span><span class="sxs-lookup"><span data-stu-id="3f020-109">Offset account is also a balance sheet account.</span></span> <span data-ttu-id="3f020-110">В общем журнале и в журнале основных средств этот счет часто является банковским счетом, который используется для оплаты приобретаемых активов.</span><span class="sxs-lookup"><span data-stu-id="3f020-110">In the general journal and in the fixed assets journal, this account often will be the bank account that is used to pay for the acquisition of the asset.</span></span> <span data-ttu-id="3f020-111">Корреспондентский счет является счетом по умолчанию, предлагаемым в журналах.</span><span class="sxs-lookup"><span data-stu-id="3f020-111">The offset account is a default account, which is suggested in the journals.</span></span> <span data-ttu-id="3f020-112">Его можно изменить в журнале на любой другой счет из плана счетов или на счет поставщика, если основное средства была покупка у поставщика.</span><span class="sxs-lookup"><span data-stu-id="3f020-112">It can be changed in the journal to any other account from the chart of accounts or to a vendor account, if the fixed asset was purchase from a vendor.</span></span> 

<span data-ttu-id="3f020-113">Если параметры "Журнал накладных" или "Заказы на покупку" в модуле "Расчеты с поставщиками" используются для приобретения основных средств, корр. счет для проводки основных средств заменяется счетом поставщика, выбранным для проводки.</span><span class="sxs-lookup"><span data-stu-id="3f020-113">When Invoice journal or Purchase orders in Accounts payable are used for fixed asset acquisitions, the offset account for the fixed asset transaction is replaced by the vendor account that is selected for the transaction.</span></span>

<span data-ttu-id="3f020-114">Для приобретений, разнесенных с помощью журнала "Запасы в основное средство" в главной книге, основные средства не приобретаются из внешних источников, но переносятся из собственных запасов компании.</span><span class="sxs-lookup"><span data-stu-id="3f020-114">For acquisitions posted using the Inventory to fixed assets journal in General ledger, the fixed asset is not bought from external sources, but transferred from the company's own inventory.</span></span> <span data-ttu-id="3f020-115">В этом случае корреспондентский счет — это счет расхода запасов для складской номенклатуры в модуле "управление запасами".</span><span class="sxs-lookup"><span data-stu-id="3f020-115">Therefore, the offset account is an inventory issue account for the inventory item in Inventory management.</span></span>

<span data-ttu-id="3f020-116">Дополнительные сведения см. в разделе [Приобретение активов через закупку](acquire-assets-procurement.md).</span><span class="sxs-lookup"><span data-stu-id="3f020-116">For more information, see [Acquire assets through procurement](acquire-assets-procurement.md).</span></span>



