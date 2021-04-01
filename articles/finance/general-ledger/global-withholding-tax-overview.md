---
title: Глобальный подоходный налог
description: В этом разделе приводятся сведения о функции глобального подоходного налога и порядке ее настройки. Функция глобального подоходного налога улучшена для проводок поставщиков и клиентов, поэтому подоходный налог рассчитывается на уровне номенклатуры.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 25fc503d6145872b8e9f28b8d9a4d7b9c1ba53a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249175"
---
# <a name="global-withholding-tax"></a><span data-ttu-id="cf8f3-104">Глобальный подоходный налог</span><span class="sxs-lookup"><span data-stu-id="cf8f3-104">Global withholding tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf8f3-105">В этом разделе приводятся сведения о функции глобального подоходного налога и объясняется порядке ее настройки.</span><span class="sxs-lookup"><span data-stu-id="cf8f3-105">This topic provides information about global withholding tax functionality and explains how to set it up.</span></span> <span data-ttu-id="cf8f3-106">Эта новая функция доступна в версии 10.0.17 и выше.</span><span class="sxs-lookup"><span data-stu-id="cf8f3-106">The new functionality is available in version 10.0.17 and later.</span></span>

<span data-ttu-id="cf8f3-107">Функция глобального подоходного налога улучшена для проводок поставщиков и клиентов, поэтому подоходный налог рассчитывается на уровне номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="cf8f3-107">Global withholding tax functionality is enhanced for vendor and customer transactions, so that withholding tax is calculated at the item level.</span></span> <span data-ttu-id="cf8f3-108">Сальдо в счете подоходного налога из проводок по покупке может быть сопоставлено путем запуска задания платежей по подоходному налогу для счета сопоставления подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="cf8f3-108">The balance in the withholding tax account from purchase transactions can be settled by running the withholding tax payment job against the withholding tax settlement account.</span></span>

> [!NOTE]
> <span data-ttu-id="cf8f3-109">Глобальный подоходный налог не поддерживает функцию **Ведение накладных расходов** на страницах заказа на покупку, накладной поставщика и заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="cf8f3-109">Global withholding tax doesn't support the **Maintain charges** function on the purchase order, vendor invoice, and sales order pages.</span></span>

## <a name="turn-on-global-withholding-tax"></a><span data-ttu-id="cf8f3-110">Включение глобального подоходного налога</span><span class="sxs-lookup"><span data-stu-id="cf8f3-110">Turn on global withholding tax</span></span>

1. <span data-ttu-id="cf8f3-111">В рабочей области **Управление функциями** выберите **Глобальный подоходный налог** в списке и выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="cf8f3-111">In the **Feature management** workspace, select **Global withholding tax**, and then select **Enable now**.</span></span>
2. <span data-ttu-id="cf8f3-112">Перейдите в раздел **Налог \> Настройка \> Параметры \> Параметры главной книги**, затем на вкладке **Подоходный налог** установите для параметра **Включить глобальный подоходный налог** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="cf8f3-112">Go to **Tax \> Setup \> Parameters \> General ledger parameters**, and then, on the **Withholding tax** tab, set the **Enable global withholding tax** option to **Yes**.</span></span>
3. <span data-ttu-id="cf8f3-113">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="cf8f3-113">Select **Save**.</span></span>
4. <span data-ttu-id="cf8f3-114">Обновите страницу в веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="cf8f3-114">Refresh the page in your web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="cf8f3-115">Функция глобального подоходного налога не может быть включена для стран и регионов, где уже существуют локализованные решения по подоходному налогу.</span><span class="sxs-lookup"><span data-stu-id="cf8f3-115">Global withholding tax functionality can’t be turned on for countries/regions where localized withholding tax solutions already exist.</span></span> <span data-ttu-id="cf8f3-116">Эти области включают, но не ограничиваются этим, Индию, Бразилию, Таиланд, Саудовскую Аравия, Ирландию, Великобританию и США.</span><span class="sxs-lookup"><span data-stu-id="cf8f3-116">These areas include but are not restricted to India, Brazil, Thailand, Saudi Arabia, Ireland, Great Britain and the United States.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]