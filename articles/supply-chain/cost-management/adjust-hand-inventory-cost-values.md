---
title: Настройка себестоимости запасов в наличии
description: Вы можете использовать страницу "Коррекция запасов в наличии", чтобы настроить себестоимость количеств запасов в наличии после выполнения процесса закрытия запасов.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a702a083d60bdb289712027fbaee5c0a72e60cb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963846"
---
# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="73aa8-103">Настройка себестоимости запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="73aa8-103">Adjust on-hand inventory cost values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73aa8-104">Вы можете использовать страницу "Коррекция запасов в наличии", чтобы настроить себестоимость количеств запасов в наличии после выполнения процесса закрытия запасов.</span><span class="sxs-lookup"><span data-stu-id="73aa8-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="73aa8-105">Вы можете использовать страницу **Настройка себестоимости запасов в наличии**, чтобы настроить себестоимость количеств запасов в наличии после выполнения процесса закрытия запасов.</span><span class="sxs-lookup"><span data-stu-id="73aa8-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="73aa8-106">**Примечание.** Чтобы открыть страницу **Коррекция запасов в наличии** на странице **Закрытие и коррекция** выберите запись завершенного процесса закрытия запасов и после этого щелкните **Корректировка** &gt; **В наличии**.</span><span class="sxs-lookup"><span data-stu-id="73aa8-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="73aa8-107">**Пример.** В феврале имеются следующие проводки:</span><span class="sxs-lookup"><span data-stu-id="73aa8-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="73aa8-108">1-ое февраля: Финансовый приход запасов в количестве равном 2 при себестоимости USD 10,00</span><span class="sxs-lookup"><span data-stu-id="73aa8-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="73aa8-109">5-ое февраля: Финансовый приход запасов в количестве равном 1 при себестоимости USD 13,00</span><span class="sxs-lookup"><span data-stu-id="73aa8-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="73aa8-110">19-ое февраля: Финансовый расход запасов в количестве равном 1 при скользящей средней себестоимости USD 11,00</span><span class="sxs-lookup"><span data-stu-id="73aa8-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="73aa8-111">Для этой номенклатуры настроена складская модель ФИФО, а закрытие запасов выполнялось 28 февраля.</span><span class="sxs-lookup"><span data-stu-id="73aa8-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="73aa8-112">Проводка по финансовому расходу в сумме USD 11,00 будет сопоставлена с финансовым приходом от 1 февраля, и будет выполнена коррекция на USD 1,00.</span><span class="sxs-lookup"><span data-stu-id="73aa8-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="73aa8-113">Следующие приходы на склад будут содержать открытые складские количества:</span><span class="sxs-lookup"><span data-stu-id="73aa8-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="73aa8-114">1-ое февраля: Количество 1 шт. при затратах USD 10,00</span><span class="sxs-lookup"><span data-stu-id="73aa8-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="73aa8-115">5-ое февраля: Количество 1 шт. при затратах USD 13,00</span><span class="sxs-lookup"><span data-stu-id="73aa8-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="73aa8-116">Для определения стоимости этих двух элементов равной USD 15,00, используйте опцию коррекции запасов в наличии для изменения открытых количеств запасов в наличии по состоянию на последний период закрытия складов.</span><span class="sxs-lookup"><span data-stu-id="73aa8-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="73aa8-117">**Примечание.** Датой разноски операции по коррекции запасов в наличии будет дата последнего закрытия складов.</span><span class="sxs-lookup"><span data-stu-id="73aa8-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="73aa8-118">Эту дату нельзя изменять.</span><span class="sxs-lookup"><span data-stu-id="73aa8-118">This date can't be modified.</span></span>
