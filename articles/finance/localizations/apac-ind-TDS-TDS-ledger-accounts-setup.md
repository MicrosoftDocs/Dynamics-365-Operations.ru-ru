---
title: Настройка счетов ГК TDS
description: В этой теме объясняется, как настроить счета ГК для функции налогов, которые удерживаются в источнике (TDS).
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
ms.openlocfilehash: 93d4cb54488ec0eeee40ca56f3e46f30012f54f5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023537"
---
# <a name="set-up-tds-ledger-accounts"></a><span data-ttu-id="6ca7e-103">Настройка счетов ГК TDS</span><span class="sxs-lookup"><span data-stu-id="6ca7e-103">Set up TDS ledger accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ca7e-104">В этой теме объясняется, как настроить счета ГК для функции налогов, которые удерживаются в источнике (TDS).</span><span class="sxs-lookup"><span data-stu-id="6ca7e-104">This topic explains how to set up ledger accounts for the Tax Deducted at Source (TDS) feature.</span></span> <span data-ttu-id="6ca7e-105">Страница **План счетов** используется для настройки счетов главной книги для TDS.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-105">You use the **Chart of accounts** page to set up ledger accounts for TDS.</span></span>

1. <span data-ttu-id="6ca7e-106">Перейдите в раздел **Главная книга \> План счетов \> Счета \> Счета ГК**.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-106">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**.</span></span>
2. <span data-ttu-id="6ca7e-107">На вкладке **Обзор** нажмите сочетание клавиш **ALT+N**, чтобы создать счет ГК для TDS, а затем введите необходимые сведения.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-107">On the **Overview** tab, select **Alt+N** to create a TDS ledger account, and enter the required details.</span></span>
3. <span data-ttu-id="6ca7e-108">На вкладке **Настройка** в поле **Тип разноски** выберите **Подоходный налог**.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-108">On the **Setup** tab, in the **Posting type** field, select **Withholding tax**.</span></span>     

    > [!NOTE]
    > <span data-ttu-id="6ca7e-109">Счета ГК, имеющие тип разноски **Подоходный налог**, могут быть определены только как счета модуля "расчеты с клиентами", которые используются для разноски суммы расчетов с клиентами TDS для налогового кода TDS.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-109">Ledger accounts that have a posting type of **Withholding tax** can be defined only as receivable accounts that are used to post the TDS receivable amount for a TDS tax code.</span></span>

4. <span data-ttu-id="6ca7e-110">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-110">Close the page.</span></span>
