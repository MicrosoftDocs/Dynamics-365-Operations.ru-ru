---
title: Просмотр разнесенных платежей TDS и проводок для периода сопоставления TDS
description: В этой теме объясняется, как просмотреть платежи и проводки по налогу, удержанный в источнике (TDS), которые были разнесены для периода сопоставления.
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 2bada42073e46c69101e6d31f3328a2eeb95f880
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023531"
---
# <a name="view-posted-tds-payments-and-transactions-for-a-tds-settlement-period"></a><span data-ttu-id="cc446-103">Просмотр разнесенных платежей TDS и проводок для периода сопоставления TDS</span><span class="sxs-lookup"><span data-stu-id="cc446-103">View posted TDS payments and transactions for a TDS settlement period</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc446-104">В этой теме объясняется, как просмотреть платежи и проводки по налогу, удержанный в источнике (TDS), которые были разнесены для периода сопоставления.</span><span class="sxs-lookup"><span data-stu-id="cc446-104">This topic explains how to view the Tax Deducted at Source (TDS) payments and transactions that were posted for a settlement period.</span></span>

1. <span data-ttu-id="cc446-105">Перейдите в раздел **Налог \> Косвенные налоги \> Подоходный налог \> Периоды сопоставления подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="cc446-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="cc446-106">[![Страница периодов сопоставления подоходного налога](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)</span><span class="sxs-lookup"><span data-stu-id="cc446-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)</span></span>

2. <span data-ttu-id="cc446-107">На странице **Периоды сопоставления подоходного налога** выберите **Платежи подоходного налога**, чтобы открыть страницу **Платежи подоходного налога**, на которой можно просмотреть сопоставления TDS, сделанные для конкретного периода сопоставления TDS.</span><span class="sxs-lookup"><span data-stu-id="cc446-107">On the **Withholding tax settlement periods** page, select **Withholding tax payments** to open the **Withholding tax payments** page, where you can view the TDS settlements that were made for a specific TDS settlement period.</span></span>

    <span data-ttu-id="cc446-108">На вкладке **Обзор** показаны следующие данные:</span><span class="sxs-lookup"><span data-stu-id="cc446-108">The **Overview** tab shows the following information:</span></span>

    - <span data-ttu-id="cc446-109">**Дата** — дата сопоставления TDS.</span><span class="sxs-lookup"><span data-stu-id="cc446-109">**Date** – The date of TDS settlement.</span></span>
    - <span data-ttu-id="cc446-110">**Ваучер** — код ваучера проводки сопоставления TDS.</span><span class="sxs-lookup"><span data-stu-id="cc446-110">**Voucher** – The voucher number of the TDS settlement transaction.</span></span>
    - <span data-ttu-id="cc446-111">**Тип налога** — тип налога, для которого запускается процесс сопоставления.</span><span class="sxs-lookup"><span data-stu-id="cc446-111">**Tax type** – The tax type that the settlement process is run for.</span></span>
    - <span data-ttu-id="cc446-112">**Номер налогового счета (TAN)** — номер налогового счета (TAN) сопоставленной проводки TDS.</span><span class="sxs-lookup"><span data-stu-id="cc446-112">**Tax Account Number (TAN)** – The Tax Account Number (TAN) of the settled TDS transaction.</span></span>
    - <span data-ttu-id="cc446-113">**Период сопоставления** — период сопоставления TDS, для которого необходимо выполнить процесс сопоставления.</span><span class="sxs-lookup"><span data-stu-id="cc446-113">**Settlement period** – The settlement period that the TDS settlement process is run for.</span></span>
    - <span data-ttu-id="cc446-114">**Начальная дата** — начальная дата периода сопоставления.</span><span class="sxs-lookup"><span data-stu-id="cc446-114">**From date** – The start date of the settlement period.</span></span>
    - <span data-ttu-id="cc446-115">**Конечная дата** — конечная дата периода сопоставления.</span><span class="sxs-lookup"><span data-stu-id="cc446-115">**To date** – The end date of the settlement period.</span></span>
    - <span data-ttu-id="cc446-116">**Версия платежа подоходного налога** — версия платежа по подоходному налогу: **Исходная**, **Последние корректировки** или **Итоговый список**.</span><span class="sxs-lookup"><span data-stu-id="cc446-116">**Withholding tax payment version** – The version of the withholding tax payment: **Original**, **Latest corrections**, or **Total list**.</span></span>

5. <span data-ttu-id="cc446-117">Выберите **Ваучер** для просмотра записей ваучера для проводки TDS.</span><span class="sxs-lookup"><span data-stu-id="cc446-117">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
6. <span data-ttu-id="cc446-118">Выберите **Проводки подоходного налога** для просмотра подробных сведений о проводках TDS, которые были сопоставлены для определенного периода в течение периода сопоставления.</span><span class="sxs-lookup"><span data-stu-id="cc446-118">Select **Withholding tax transactions** to view the details of the TDS transactions that were settled for a specific period during a settlement period.</span></span> <span data-ttu-id="cc446-119">Выберите **Ваучер** для просмотра записей ваучера для проводки TDS.</span><span class="sxs-lookup"><span data-stu-id="cc446-119">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span> <span data-ttu-id="cc446-120">Выберите **Компоненты подоходного налога** для просмотра TDS, рассчитанного по компонентам налогов для конкретного налогового кода TDS.</span><span class="sxs-lookup"><span data-stu-id="cc446-120">Select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>
7. <span data-ttu-id="cc446-121">Закройте страницу **Платежи подоходного налога**, чтобы вернуться на страницу **Периоды сопоставления подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="cc446-121">Close the **Withholding tax payments** page to return to the **Withholding tax settlement periods** page.</span></span>
8. <span data-ttu-id="cc446-122">Выберите **Проводки подоходного налога** для просмотра подробных сведений о проводках TDS, которые были сопоставлены для периода сопоставления.</span><span class="sxs-lookup"><span data-stu-id="cc446-122">Select **Withholding tax transactions** to view the details of the TDS transactions that were settled for the settlement period.</span></span>
