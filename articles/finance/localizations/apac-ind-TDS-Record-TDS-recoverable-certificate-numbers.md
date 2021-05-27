---
title: Запишите номера подлежащих возмещению сертификатов TDS
description: В этой теме объясняется, как использовать страницу подлежащих возмещению сертификатов для записи номеров и дат сертификатов для налога, удержанного в источнике (TDS), которые получаются для конкретного поставщика, клиента или главной книги.
author: kailiang
mms.date: 02/12/2021
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
ms.openlocfilehash: b501c331cccc6d030f36d0a13ba0a6a13c08c733
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023524"
---
# <a name="record-tds-recoverable-certificate-numbers"></a><span data-ttu-id="92a74-103">Запишите номера подлежащих возмещению сертификатов TDS</span><span class="sxs-lookup"><span data-stu-id="92a74-103">Record TDS recoverable certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92a74-104">В этой теме объясняется, как использовать страницу **подлежащих возмещению сертификатов** для записи номеров и дат сертификатов для налога, удержанного в источнике (TDS), которые получаются для конкретного поставщика, клиента или главной книги.</span><span class="sxs-lookup"><span data-stu-id="92a74-104">This topic explains how to use the **Recoverable certificates** page to record the certificate numbers and dates for Tax Deducted at Source (TDS) certificates that are received for a specific vendor, customer, or ledger.</span></span> <span data-ttu-id="92a74-105">Чтобы обновить номера и даты сертификатов TDS, записанных для проводок TDS на этой странице, воспользуйтесь страницей **Обновление сертификата** (**Главная книга \> Периодически \> Подоходный налог \> Обновление сертификата**).</span><span class="sxs-lookup"><span data-stu-id="92a74-105">To update the TDS certificate numbers and dates that are recorded for TDS transactions on this page, use the **Update certificate** page (**General ledger \> Periodic \> Withholding tax \> Update certificate**).</span></span> <span data-ttu-id="92a74-106">После завершения обновления номеров сертификатов TDS закройте их.</span><span class="sxs-lookup"><span data-stu-id="92a74-106">After you've finished updating TDS certificate numbers, close them.</span></span>

<span data-ttu-id="92a74-107">Чтобы записать номера и даты сертификатов TDS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="92a74-107">Follow these steps to record the TDS certificate numbers and dates.</span></span>

1. <span data-ttu-id="92a74-108">Перейдите в раздел **Налог \> Косвенный налог \> Подоходный налог \> Подлежащие возмещению сертификаты**.</span><span class="sxs-lookup"><span data-stu-id="92a74-108">Go to **Tax \> Indirect tax \> Withholding tax \> Recoverable certificates**.</span></span>

    <span data-ttu-id="92a74-109">[![Страница подлежащих возмещению сертификатов](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span><span class="sxs-lookup"><span data-stu-id="92a74-109">[![Recoverable certificates page](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span></span> 

2. <span data-ttu-id="92a74-110">На странице **Подлежащие возмещению сертификаты** в поле **Тип налога** выберите **TDS**.</span><span class="sxs-lookup"><span data-stu-id="92a74-110">On the **Recoverable certificates** page, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="92a74-111">Выберите **Создать**, чтобы создать запись.</span><span class="sxs-lookup"><span data-stu-id="92a74-111">Select **New** to create a record.</span></span>
4. <span data-ttu-id="92a74-112">В поле **Номер сертификата** введите номер сертификата TDS.</span><span class="sxs-lookup"><span data-stu-id="92a74-112">In the **Certificate number** field, enter the TDS certificate number.</span></span>
5. <span data-ttu-id="92a74-113">В поле **Тип счета** выберите тип счета, для которого получается сертификат TDS: **Поставщик**, **Клиент** или **Главная книга**.</span><span class="sxs-lookup"><span data-stu-id="92a74-113">In the **Account type** field, select the type of account that the TDS certificate is received for: **Vendor**, **Customer**, or **Ledger**.</span></span>
6. <span data-ttu-id="92a74-114">В поле **Счет** выберите поставщика, клиента или номер счета ГК, в зависимости от выбранного типа счета.</span><span class="sxs-lookup"><span data-stu-id="92a74-114">In the **Account** field, select the vendor, customer, or ledger account number, depending on the account type that you selected.</span></span> <span data-ttu-id="92a74-115">В поле **Имя** отображается имя поставщика, клиента или счета ГК.</span><span class="sxs-lookup"><span data-stu-id="92a74-115">The **Name** field shows the name of the vendor, customer, or ledger account.</span></span>
7. <span data-ttu-id="92a74-116">В поле **Сумма сертификата** введите сумму сертификата TDS.</span><span class="sxs-lookup"><span data-stu-id="92a74-116">In the **Certificate amount** field, enter the amount of the TDS certificate.</span></span>
8. <span data-ttu-id="92a74-117">В поле **Дата** введите дату сертификата для номера сертификата.</span><span class="sxs-lookup"><span data-stu-id="92a74-117">In the **Date** field, enter the certificate date for the certificate number.</span></span>
9. <span data-ttu-id="92a74-118">Выберите **Запросы**, чтобы открыть страницу **Проводки сертификата**, на которой можно просмотреть проводки TDS, для которых обновляются номер и дата сертификата TDS.</span><span class="sxs-lookup"><span data-stu-id="92a74-118">Select **Inquiries** to open the **Certificate transactions** page, where you can view the TDS transactions that the TDS certificate number and date are updated for.</span></span> <span data-ttu-id="92a74-119">Эти сведения могут быть обновлены на странице **Обновление сертификата** (**Налог \> Декларации \> Подоходный налог \> Обновление сертификата**).</span><span class="sxs-lookup"><span data-stu-id="92a74-119">This information can be updated on the **Update certificate** page (**Tax \> Declarations \> Withholding tax \> Update certificate**).</span></span>

    <span data-ttu-id="92a74-120">На странице **Обновление сертификата** в каждой проводке TDS отображаются следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="92a74-120">The **Update certificate** page shows the following information for each TDS transaction:</span></span>

    - <span data-ttu-id="92a74-121">**Дата** — дата разноски проводки TDS.</span><span class="sxs-lookup"><span data-stu-id="92a74-121">**Date** – The posting date of the TDS transaction.</span></span>
    - <span data-ttu-id="92a74-122">**Ваучер** — код ваучера проводки TDS.</span><span class="sxs-lookup"><span data-stu-id="92a74-122">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="92a74-123">**Источник** — модуль, в котором была создана проводка TDS.</span><span class="sxs-lookup"><span data-stu-id="92a74-123">**Source** – The module that the TDS transaction was created in.</span></span>
    - <span data-ttu-id="92a74-124">**Счет** — номер поставщика, клиента или счета ГК, для которого была создана проводка TDS.</span><span class="sxs-lookup"><span data-stu-id="92a74-124">**Account** – The vendor, customer, or ledger account number that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="92a74-125">**Имя** — имя поставщика, клиента или счета ГК, для которого была создана проводка TDS.</span><span class="sxs-lookup"><span data-stu-id="92a74-125">**Name** – The name of the vendor, customer, or ledger account that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="92a74-126">**Сумма** — сумма накладной, для которой рассчитан TDS.</span><span class="sxs-lookup"><span data-stu-id="92a74-126">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="92a74-127">**Сумма налога** — сумма налога TDS, рассчитанная для проводки.</span><span class="sxs-lookup"><span data-stu-id="92a74-127">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>
    - <span data-ttu-id="92a74-128">**Дата сертификата** — дата сертификата TDS, которая была обновлена для проводки TDS.</span><span class="sxs-lookup"><span data-stu-id="92a74-128">**Certificate date** – The TDS certificate date that was updated for the TDS transaction.</span></span>
    - <span data-ttu-id="92a74-129">**Номер сертификата** — номер сертификата TDS, который был обновлен для проводки TDS.</span><span class="sxs-lookup"><span data-stu-id="92a74-129">**Certificate number** – TDS certificate number that was updated for the TDS transaction.</span></span>

10. <span data-ttu-id="92a74-130">На странице **Подлежащие возмещению сертификаты** установите флажок **Закрыто**, чтобы закрыть номер сертификата TDS после завершения его обновления для проводок TDS на странице **Обновить сертификат**.</span><span class="sxs-lookup"><span data-stu-id="92a74-130">On the **Recoverable certificates** page, select the **Closed** check box to close the TDS certificate number after you've finished updating it for TDS transactions on the **Update certificate** page.</span></span>

    <span data-ttu-id="92a74-131">Чтобы установить флажок **Закрыто** для всех записей на странице, выберите **Пометить все**.</span><span class="sxs-lookup"><span data-stu-id="92a74-131">To select the **Closed** check box for all records on the page, select **Mark all**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="92a74-132">Номера сертификатов TDS, для которых установлен флажок **Закрыто** на странице **Обновить сертификат** недоступны.</span><span class="sxs-lookup"><span data-stu-id="92a74-132">TDS certificate numbers that the **Closed** check box is selected for aren't available on the **Update certificate** page.</span></span>
