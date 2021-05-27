---
title: Функции разбиения накладных
description: В этой теме описывается настройка и функции разбиения накладных по адресу поставки и номеру налогового счета (TAN).
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
ms.openlocfilehash: 7dddbb9f69a9735c2a03d2b23928f5cb92d4e0fd
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023543"
---
# <a name="split-invoice-functionality"></a><span data-ttu-id="66d3d-103">Функции разбиения накладных</span><span class="sxs-lookup"><span data-stu-id="66d3d-103">Split invoice functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66d3d-104">В этой теме описывается настройка и функции разбиения накладных по адресу поставки и номеру налогового счета (TAN).</span><span class="sxs-lookup"><span data-stu-id="66d3d-104">This topic describes the setup and functionality for splitting invoices by delivery address and tax account number (TAN).</span></span>

<span data-ttu-id="66d3d-105">На странице **Параметры модуля расчетов с поставщиками** на вкладке **Общие** установите флажок **Поступление продуктов** или **Накладная**, чтобы разнести и разделить поступление продуктов или накладную, у которой другие адреса поставки и номера TAN на странице **Заказ на покупку**.</span><span class="sxs-lookup"><span data-stu-id="66d3d-105">On the **Accounts payable parameters** page, on the **General** tab, select the **Product receipt** or **Invoice** checkbox to post and split a product receipt or invoice that has different delivery addresses and TANs on the **Purchase order** page.</span></span> <span data-ttu-id="66d3d-106">После этого разнесенные накладные разбиваются по адресу поставки и TAN.</span><span class="sxs-lookup"><span data-stu-id="66d3d-106">The posted invoice will then be split by delivery address and TAN.</span></span>

<span data-ttu-id="66d3d-107">На вкладке **Суммарное обновление** на экспресс-вкладке **Разделение на основании** в строке **Сведения о поставке** установите для параметра **Подтверждение**, **Отгрузочная накладная**, **Отборочная накладная** или **Накладная** значение **Да**, чтобы разнести и разбить подтверждение, отгрузочную накладную, отборочную накладную или накладную, где указаны другие адреса поставки и номера TAN для разных строк накладной на странице **Заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="66d3d-107">On the **Summary update** tab, on the **Split based on** FastTab, in the **Delivery information** row, set the **Confirmation**, **Picking list**, **Packing slip**, or **Invoice** option to **Yes** to post and split a confirmation, picking list, packing slip, or invoice where different delivery addresses and TANs are defined for different invoice lines on the **Sales order** page.</span></span> <span data-ttu-id="66d3d-108">Накладная разбивается сначала по адресу поставки, затем по TAN.</span><span class="sxs-lookup"><span data-stu-id="66d3d-108">The invoice will be split first by delivery address and then by TAN.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="66d3d-109">Если для **Информация о доставке** задано **Да**, накладная будет разнесена как отдельная накладная.</span><span class="sxs-lookup"><span data-stu-id="66d3d-109">If no options for **Delivery information** are set to **Yes**, the invoice will be posted as a single invoice.</span></span> <span data-ttu-id="66d3d-110">Разбиение накладных не будет выполняться.</span><span class="sxs-lookup"><span data-stu-id="66d3d-110">No invoice splitting will occur.</span></span>
> - <span data-ttu-id="66d3d-111">Чтобы разбить и разнести отборочную накладную, где у строк накладной разные адреса поставки и номера TAN, необходимо задать параметр **Отборочная накладная** для **Сведения о поставке** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="66d3d-111">To split and post a packing slip where the invoice lines have different delivery addresses and TANs, you must set the **Packing slip** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="66d3d-112">Чтобы разбить и разнести накладную, где у строк накладной разные адреса поставки и номера TAN, необходимо задать параметр **Накладная** для **Сведения о поставке** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="66d3d-112">To split and post an invoice where the invoice lines have different delivery addresses and TANs, you must set the **Invoice** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="66d3d-113">Чтобы разбить и разнести накладную, где у строк накладной разные адреса поставки, но один и тот же номер TAN, необходимо задать параметр **Накладная** для **Сведения о поставке** как **Нет**.</span><span class="sxs-lookup"><span data-stu-id="66d3d-113">To post an invoice where the invoice lines have different delivery addresses but the same TAN, set the **Invoice** option for **Delivery information** to **No**.</span></span> <span data-ttu-id="66d3d-114">Накладная будет разбита по адресу поставки.</span><span class="sxs-lookup"><span data-stu-id="66d3d-114">The invoice will be split by delivery address.</span></span>

## <a name="example"></a><span data-ttu-id="66d3d-115">Пример</span><span class="sxs-lookup"><span data-stu-id="66d3d-115">Example</span></span>

<span data-ttu-id="66d3d-116">В этом примере параметр **Накладная** для **Информации о доставке** задан как **Да** на вкладке **Суммарная обработка** на странице **Параметры модуля расчетов с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="66d3d-116">In this example, the **Invoice** option for **Delivery information** is set to **Yes** on the **Summary update** tab of the **Accounts payable parameters** page.</span></span> <span data-ttu-id="66d3d-117">Разносится накладная по покупке, которая имеет следующую настройку для адресов поставки и номеров TAN по строкам:</span><span class="sxs-lookup"><span data-stu-id="66d3d-117">A purchase invoice is posted that has the following setup for delivery addresses and TANs on the lines:</span></span>

- <span data-ttu-id="66d3d-118">**Строка номенклатуры 1:** адрес поставки 1, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="66d3d-118">**Item line 1:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="66d3d-119">**Строка номенклатуры 2:** адрес поставки 1, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="66d3d-119">**Item line 2:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="66d3d-120">**Строка номенклатуры 3:** адрес поставки 2, TAN-ABCE12345B</span><span class="sxs-lookup"><span data-stu-id="66d3d-120">**Item line 3:** Delivery address 2, TAN-ABCE12345B</span></span>
- <span data-ttu-id="66d3d-121">**Строка номенклатуры 4:** адрес поставки 3, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="66d3d-121">**Item line 4:** Delivery address 3, TAN-ABCD12345A</span></span>

<span data-ttu-id="66d3d-122">В этом случае исходная накладная разделяется на две накладные и разносится следующим образом:</span><span class="sxs-lookup"><span data-stu-id="66d3d-122">In this case, the original invoice is split into two invoices and posted in the following way:</span></span>

- <span data-ttu-id="66d3d-123">Накладная 1 разносится для строки номенклатуры 1 и строки номенклатуры 2, поскольку обе строки имеют одинаковый адрес поставки и TAN.</span><span class="sxs-lookup"><span data-stu-id="66d3d-123">Invoice 1 is posted for item line 1 and item line 2, because both lines have the same delivery address and TAN.</span></span>
- <span data-ttu-id="66d3d-124">Накладная 2 разносится для строки номенклатуры 3.</span><span class="sxs-lookup"><span data-stu-id="66d3d-124">Invoice 2 is posted for item line 3.</span></span>
- <span data-ttu-id="66d3d-125">Накладная 3 разносится для строки номенклатуры 4.</span><span class="sxs-lookup"><span data-stu-id="66d3d-125">Invoice 3 is posted for item line 4.</span></span>
