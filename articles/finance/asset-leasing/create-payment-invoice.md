---
title: Создание накладных платежей
description: В этой теме описывается, как создавать ежемесячные накладные по аренде. Можно создать накладные для индивидуальных аренд, или можно использовать процесс пакетной обработки для создания накладных для нескольких аренд.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 303fb0e70530fdc29cb129736b01c0e0e8d02075
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969586"
---
# <a name="create-payment-invoices"></a><span data-ttu-id="17cca-104">Создание накладных платежей</span><span class="sxs-lookup"><span data-stu-id="17cca-104">Create payment invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17cca-105">Можно создать ежемесячные накладные для индивидуальных аренд, или можно использовать процесс пакетной обработки для создания накладных для нескольких аренд.</span><span class="sxs-lookup"><span data-stu-id="17cca-105">You can create monthly invoices for individual leases, or you can use a batch process to create them for multiple leases.</span></span> <span data-ttu-id="17cca-106">Следующая процедура показывает, как создать отдельную запись платежа по аренде, когда параметр **Платеж поставщику** на странице **Настройка книги аренды** включен.</span><span class="sxs-lookup"><span data-stu-id="17cca-106">The following procedure shows how to create an individual lease payment entry when the **Pay to Vendor** parameter on the **Lease book setup** page is turned on.</span></span>

1. <span data-ttu-id="17cca-107">На странице **Сводка по аренде** выберите аренду, а затем выберите **Книги \> График платежей**.</span><span class="sxs-lookup"><span data-stu-id="17cca-107">On the **Lease summary** page, select a lease, and then select **Books \> Payment schedule**.</span></span>
2. <span data-ttu-id="17cca-108">Выберите платеж, который должен быть создан, а затем выберите **Создать журнал**.</span><span class="sxs-lookup"><span data-stu-id="17cca-108">Select the payment that must be made, and then select **Create journal**.</span></span> <span data-ttu-id="17cca-109">Вы получите сообщение о том, что для выбранного платежа был создан журнал.</span><span class="sxs-lookup"><span data-stu-id="17cca-109">You receive a message that states that a journal was created against the selected payment.</span></span>
3. <span data-ttu-id="17cca-110">Выберите **Журналы накладных**, а затем выберите накладную, которая должна быть оплачена.</span><span class="sxs-lookup"><span data-stu-id="17cca-110">Select **Invoice journals**, and then select the invoice that must be paid.</span></span>
4. <span data-ttu-id="17cca-111">На вкладке **Строки** проверьте запись журнала до ее разноски в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="17cca-111">On the **Lines** tab, review the journal entry before you post it to the general ledger.</span></span>

    > [!NOTE]
    > <span data-ttu-id="17cca-112">По умолчанию созданные строки накладной поставщика используют профиль разноски поставщика на странице **Параметры модуля расчетов с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="17cca-112">By default, the vendor invoice lines that are created use the vendor posting profile from the **Accounts payable parameters** page.</span></span>

5. <span data-ttu-id="17cca-113">Выберите правильный журнал, а затем выберите накладную, которая должна быть оплачена.</span><span class="sxs-lookup"><span data-stu-id="17cca-113">Select the correct journal, and then select the invoice that must be paid.</span></span>

    <span data-ttu-id="17cca-114">В данном примере параметр **Платеж поставщику** в книге аренды включен.</span><span class="sxs-lookup"><span data-stu-id="17cca-114">For this example, the **Pay to Vendor** parameter on the lease book is turned on.</span></span> <span data-ttu-id="17cca-115">Поэтому накладная будет в журнале накладных.</span><span class="sxs-lookup"><span data-stu-id="17cca-115">Therefore, the invoice will be in the invoice journal.</span></span> <span data-ttu-id="17cca-116">Раздел **Обзор** содержит сводку записи журнала, а в разделе **Строки** отображаются сведения о фактических строках журнала.</span><span class="sxs-lookup"><span data-stu-id="17cca-116">The **Overview** section shows a summary of the journal entry, and the **Lines** section shows details of the actual journal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="17cca-117">Если параметр **Платеж поставщику** отключен, записи журнала платежей будут перечислены на странице **Аренда активов** для книги аренды, а в системе вместо накладной будет создана запись аренды актива.</span><span class="sxs-lookup"><span data-stu-id="17cca-117">If the **Pay to Vendor** parameter is turned off, payment journal entries will be listed on the **Asset leasing** page for the lease book, and the system will create an asset leasing entry instead of an invoice.</span></span> <span data-ttu-id="17cca-118">Запись платежа по аренде будет разнесена по имени журнала, которое указано в поле **Месячный журнал аренды**.</span><span class="sxs-lookup"><span data-stu-id="17cca-118">The lease payment entry will be posted to the journal name that is specified in the **Monthly lease journal** field.</span></span>

6. <span data-ttu-id="17cca-119">После разноски проводки можно просмотреть сведения о проводке и остаточную стоимость обязательств по аренде, выбрав **Проводки по обязательствам** в книге аренды.</span><span class="sxs-lookup"><span data-stu-id="17cca-119">After the transaction is posted, you can view the transaction information and the carrying value of the lease liability by selecting **Liability transactions** in the lease book.</span></span>

    <span data-ttu-id="17cca-120">В графике платежей будет установлен флажок **Журнал разнесен**, а в строке будет показан номер журнала накладных.</span><span class="sxs-lookup"><span data-stu-id="17cca-120">In the payment schedule, the **Journal posted** check box will be selected, and the line will show the invoice journal number.</span></span> <span data-ttu-id="17cca-121">После создания журнала платежей и записи для этого журнала необходимо реверсировать запись, прежде чем ее можно будет создать повторно.</span><span class="sxs-lookup"><span data-stu-id="17cca-121">After a payment journal and an entry for that journal have been created, you must reverse the entry before it can be re-created.</span></span>
