---
title: Добавление вариантов продуктов в заказы на покупку с использованием весов вариантов
description: Эта процедура содержит инструкции по использованию различных вариантов веса для автоматического заполнения строк заказа на покупку для каждого варианта продукта.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cd4ca3652c1ce7422e8f80426a7b11545e09861
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242573"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="8965d-103">Добавление вариантов продуктов в заказы на покупку с использованием весов вариантов</span><span class="sxs-lookup"><span data-stu-id="8965d-103">Add variant products to purchase orders using variant weights</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8965d-104">Эта процедура содержит инструкции по использованию различных вариантов веса для автоматического заполнения строк заказа на покупку для каждого варианта продукта.</span><span class="sxs-lookup"><span data-stu-id="8965d-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="8965d-105">При выборе количества продукта, которое вы хотите купить, строки заказа на покупку создаются для всех вариантов продукта с предложенными количествами, основанными на весах, настроенных для вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="8965d-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="8965d-106">Эта процедура не включает действия по настройки значений весов в аналитиках продуктов и вариантах продуктов.</span><span class="sxs-lookup"><span data-stu-id="8965d-106">This procedure doesn't include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="8965d-107">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="8965d-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="8965d-108">Перейдите в раздел "Расчеты с поставщиками" > "Заказы на покупку" > "Все заказы на покупку".</span><span class="sxs-lookup"><span data-stu-id="8965d-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="8965d-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8965d-109">Click New.</span></span>
3. <span data-ttu-id="8965d-110">В поле "Счет поставщика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8965d-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8965d-111">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8965d-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="8965d-112">Переключите развертывание раздела "Общее".</span><span class="sxs-lookup"><span data-stu-id="8965d-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="8965d-113">В поле "Сайт" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8965d-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8965d-114">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8965d-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="8965d-115">В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8965d-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="8965d-116">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8965d-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="8965d-117">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8965d-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="8965d-118">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="8965d-118">Click OK.</span></span>
12. <span data-ttu-id="8965d-119">Переключите развертывание раздела "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="8965d-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="8965d-120">Перейдите на вкладку "Варианты".</span><span class="sxs-lookup"><span data-stu-id="8965d-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="8965d-121">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="8965d-121">Click Add line.</span></span>
15. <span data-ttu-id="8965d-122">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="8965d-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="8965d-123">В поле "Код номенклатуры" введите "0140".</span><span class="sxs-lookup"><span data-stu-id="8965d-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="8965d-124">В поле "Количество" укажите "1000".</span><span class="sxs-lookup"><span data-stu-id="8965d-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="8965d-125">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8965d-125">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]