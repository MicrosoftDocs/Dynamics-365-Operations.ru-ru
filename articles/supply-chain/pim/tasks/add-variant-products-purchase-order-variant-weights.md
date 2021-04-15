---
title: Добавление вариантов продуктов в заказы на покупку с использованием весов вариантов
description: Эта процедура содержит инструкции по использованию различных вариантов веса для автоматического заполнения строк заказа на покупку для каждого варианта продукта.
author: ShylaThompson
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70e8cddd37127865debfc51eb1c2f39926e49f54
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812579"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="95bf9-103">Добавление вариантов продуктов в заказы на покупку с использованием весов вариантов</span><span class="sxs-lookup"><span data-stu-id="95bf9-103">Add variant products to purchase orders using variant weights</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="95bf9-104">Эта процедура содержит инструкции по использованию различных вариантов веса для автоматического заполнения строк заказа на покупку для каждого варианта продукта.</span><span class="sxs-lookup"><span data-stu-id="95bf9-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="95bf9-105">При выборе количества продукта, которое вы хотите купить, строки заказа на покупку создаются для всех вариантов продукта с предложенными количествами, основанными на весах, настроенных для вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="95bf9-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="95bf9-106">Эта процедура не включает действия по настройки значений весов в аналитиках продуктов и вариантах продуктов.</span><span class="sxs-lookup"><span data-stu-id="95bf9-106">This procedure doesn't include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="95bf9-107">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="95bf9-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="95bf9-108">Перейдите в раздел "Расчеты с поставщиками" > "Заказы на покупку" > "Все заказы на покупку".</span><span class="sxs-lookup"><span data-stu-id="95bf9-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="95bf9-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="95bf9-109">Click New.</span></span>
3. <span data-ttu-id="95bf9-110">В поле "Счет поставщика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="95bf9-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="95bf9-111">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="95bf9-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="95bf9-112">Переключите развертывание раздела "Общее".</span><span class="sxs-lookup"><span data-stu-id="95bf9-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="95bf9-113">В поле "Сайт" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="95bf9-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="95bf9-114">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="95bf9-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="95bf9-115">В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="95bf9-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="95bf9-116">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="95bf9-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="95bf9-117">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="95bf9-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="95bf9-118">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="95bf9-118">Click OK.</span></span>
12. <span data-ttu-id="95bf9-119">Переключите развертывание раздела "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="95bf9-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="95bf9-120">Перейдите на вкладку "Варианты".</span><span class="sxs-lookup"><span data-stu-id="95bf9-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="95bf9-121">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="95bf9-121">Click Add line.</span></span>
15. <span data-ttu-id="95bf9-122">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="95bf9-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="95bf9-123">В поле "Код номенклатуры" введите "0140".</span><span class="sxs-lookup"><span data-stu-id="95bf9-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="95bf9-124">В поле "Количество" укажите "1000".</span><span class="sxs-lookup"><span data-stu-id="95bf9-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="95bf9-125">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="95bf9-125">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]