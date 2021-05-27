---
title: Обновление номеров сертификатов и дат для проводок TDS
description: В этой теме объясняется, как обновлять номера подлежащих возмещению сертификатов и даты, записанные для поставщика, клиента и счетов ГК для налога, удержанного в источнике (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023534"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a><span data-ttu-id="498f6-103">Обновление номеров сертификатов и дат для проводок TDS</span><span class="sxs-lookup"><span data-stu-id="498f6-103">Update certificate numbers and dates for TDS transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="498f6-104">В этой теме объясняется, как обновлять номера подлежащих возмещению сертификатов и даты, записанные для поставщика, клиента и счетов ГК для налога, удержанного в источнике (TDS).</span><span class="sxs-lookup"><span data-stu-id="498f6-104">This topic explains how to update the recoverable certificate numbers and dates that were recorded for vendor, customer, and ledger accounts for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="498f6-105">Сертификаты для проводок TDS можно просмотреть на странице **Подлежащие возмещению сертификаты**.</span><span class="sxs-lookup"><span data-stu-id="498f6-105">You can view the certificates for TDS transactions on the **Recoverable certificates** page.</span></span> <span data-ttu-id="498f6-106">Для обновления сертификатов можно воспользоваться страницей **Обновление сертификатов**.</span><span class="sxs-lookup"><span data-stu-id="498f6-106">You can update the certificates by using the **Update Certificates** page.</span></span>

<span data-ttu-id="498f6-107">Чтобы обновить номера и даты сертификатов для проводок TDS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="498f6-107">Follow these steps to update certificate numbers and dates for TDS transactions.</span></span>

1. <span data-ttu-id="498f6-108">Перейдите **Налог \> Декларации \> Подоходный налог \> Обновление сертификата**.</span><span class="sxs-lookup"><span data-stu-id="498f6-108">Go to **Tax \> Declarations \> Withholding tax \> Update certificate**.</span></span>

    <span data-ttu-id="498f6-109">[![Страница «Обновление сертификата»](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span><span class="sxs-lookup"><span data-stu-id="498f6-109">[![Update certificate page](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span></span>

2. <span data-ttu-id="498f6-110">На странице **Обновление сертификата** в разделе **Выбор** в поле **Тип налога** выберите **TDS**.</span><span class="sxs-lookup"><span data-stu-id="498f6-110">On the **Update certificate** page, in the **Select** section, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="498f6-111">В поле **Номер сертификата** выберите номер сертификата TDS клиента или поставщика.</span><span class="sxs-lookup"><span data-stu-id="498f6-111">In the **Certificate number** field, select the customer's or vendor's TDS certificate number.</span></span>

    > [!NOTE]
    > <span data-ttu-id="498f6-112">В поле **Номер сертификата** перечислены только те номера сертификатов TDS, для которых флажок **Закрыто** на странице **Подлежащие возмещению сертификаты** снят.</span><span class="sxs-lookup"><span data-stu-id="498f6-112">The **Certificate number** field lists only TDS certificate numbers that the **Closed** check box is cleared for on the **Recoverable certificates** page.</span></span>

    <span data-ttu-id="498f6-113">В поле **Дата сертификата** показана дата сертификата.</span><span class="sxs-lookup"><span data-stu-id="498f6-113">The **Certificate date** field shows the certificate date.</span></span> <span data-ttu-id="498f6-114">В поле **Тип счета** отображается тип счета, для которого получен номер сертификата TDS, а в поле **Имя** отображается имя счета.</span><span class="sxs-lookup"><span data-stu-id="498f6-114">The **Account type** field shows the type of account that the TDS certificate number is received for, and the **Name** field shows the name of the account.</span></span>

5. <span data-ttu-id="498f6-115">В полях **Дата от** и **Дата до** выберите начальную и конечную даты периода, для которого отображаются проводки TDS.</span><span class="sxs-lookup"><span data-stu-id="498f6-115">In the **From date** and **To date** fields, select the start and end dates of the period to show the TDS transactions for.</span></span>
6. <span data-ttu-id="498f6-116">Выберите **Показать данные**, чтобы просмотреть проводки TDS, которые были разнесены в течение выбранного периода.</span><span class="sxs-lookup"><span data-stu-id="498f6-116">Select **Show data** to view the TDS transactions that were posted during the selected period.</span></span>

    <span data-ttu-id="498f6-117">На вкладке **Обзор** сетка в верхней области содержит следующие сведения о каждой проводке TDS, которая была разнесена для поставщика или клиента в течение выбранного периода:</span><span class="sxs-lookup"><span data-stu-id="498f6-117">On the **Overview** tab, the grid in the upper pane shows the following information about each TDS transaction that was posted for the vendor or customer during the selected period:</span></span>

    - <span data-ttu-id="498f6-118">**Ваучер** — код ваучера проводки TDS.</span><span class="sxs-lookup"><span data-stu-id="498f6-118">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="498f6-119">**Дата** — дата проводки TDS.</span><span class="sxs-lookup"><span data-stu-id="498f6-119">**Date** – The date of the TDS transaction.</span></span>
    - <span data-ttu-id="498f6-120">**Сумма** — сумма накладной, для которой рассчитан TDS.</span><span class="sxs-lookup"><span data-stu-id="498f6-120">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="498f6-121">**Сумма налога** — сумма налога TDS, рассчитанная для проводки.</span><span class="sxs-lookup"><span data-stu-id="498f6-121">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>

7. <span data-ttu-id="498f6-122">Чтобы переместить отдельные проводки TDS из верхней сетки в нижнюю сетку, выберите проводки, а затем выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="498f6-122">To move specific TDS transactions from the upper grid to the lower grid, select the transactions, and then select **Include**.</span></span> <span data-ttu-id="498f6-123">Можно также выбрать **Включить все**, чтобы переместить все проводки TDS из верхней сетки в нижнюю сетку.</span><span class="sxs-lookup"><span data-stu-id="498f6-123">Alternatively, select **Include all** to move all TDS transactions from the upper grid to the lower grid.</span></span>

    <span data-ttu-id="498f6-124">Чтобы переместить отдельные проводки TDS или все проводки TDS из нижней сетки в верхнюю, используйте кнопку **Исключить** или **Исключить все**.</span><span class="sxs-lookup"><span data-stu-id="498f6-124">To move specific TDS transactions or all TDS transactions from the lower grid to the upper grid, use the **Exclude** or **Exclude all** button.</span></span>

8. <span data-ttu-id="498f6-125">Выберите **Обновить**, чтобы обновить поля **Номер сертификата** и **Дата сертификата** для проводок TDS в нижней сетке.</span><span class="sxs-lookup"><span data-stu-id="498f6-125">Select **Update** to update the **Certificate number** and **Certificate date** fields for TDS transactions in the lower grid.</span></span>
10. <span data-ttu-id="498f6-126">Перейдите **Налог \> Косвенные налоги \> Подоходный налог \> Подлежащий возмещению сертификат** и выберите **Запрос** для просмотра обновленных строк проводок с новыми номерами сертификатов на странице **Проводки сертификата**.</span><span class="sxs-lookup"><span data-stu-id="498f6-126">Go to **Tax \> Indirect taxes \> Withholding tax \> Recoverable certificate**, and select **Inquiry** to view the updated transaction lines that have the new certificate numbers on the **Certificate transactions** page.</span></span>

    <span data-ttu-id="498f6-127">[![Страница "Проводки сертификата"](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span><span class="sxs-lookup"><span data-stu-id="498f6-127">[![Certificate transactions page](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span></span>
