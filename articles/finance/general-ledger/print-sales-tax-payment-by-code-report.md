---
title: Печать отчета о налоговых платежах по коду
description: В этой теме приводятся сведения о параметрах и действиях, которые необходимы для печати отчета о налоговых платежах по кодам в валюте учета или валюте налогового кода.
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eb3ee4a12d2d29c2769f1ae22e11dc05608b47c1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815460"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a><span data-ttu-id="323b8-103">Печать отчета о налоговых платежах по коду</span><span class="sxs-lookup"><span data-stu-id="323b8-103">Print the Sales tax payment by code report</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="323b8-104">Для печати отчета **Налоговые платежи по коду** выберите **Налог** \> **Запросы и отчеты** \> **Налоговые отчеты** \> **Налоговые платежи по коду**.</span><span class="sxs-lookup"><span data-stu-id="323b8-104">To print the **Sales tax payment by code** report, go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span> <span data-ttu-id="323b8-105">По умолчанию суммы отчета создаются в валюте учета юридического лица для всех кодов отчетности, настроенных на странице **Коды налоговой отчетности**.</span><span class="sxs-lookup"><span data-stu-id="323b8-105">By default, report amounts are generated in the accounting currency of the legal entity for all reporting codes that are set up on the **Sales tax reporting codes** page.</span></span>

<span data-ttu-id="323b8-106">Можно также создать этот отчет, чтобы в нем отображались суммы налоговых платежей в валютах налоговых кодов для всех кодов отчетности, назначенных налоговым кодам на странице **Налоговые коды**.</span><span class="sxs-lookup"><span data-stu-id="323b8-106">You can also generate this report so that it shows the sales tax payment amounts in the currencies of sales tax codes for all reporting codes that are assigned to sales tax codes on the **Sales tax codes** page.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="323b8-107">Включение функции</span><span class="sxs-lookup"><span data-stu-id="323b8-107">Turn on the feature</span></span>

<span data-ttu-id="323b8-108">В рабочей области **Управление функциями** включите следующую функцию: **Создание отчета о налоговых платежах по кодам в валюте налогового кода**.</span><span class="sxs-lookup"><span data-stu-id="323b8-108">In the **Feature management** workspace, turn on the following feature: **Generate the Sales tax payment by code report in the sales tax code currency**.</span></span>

## <a name="run-the-report"></a><span data-ttu-id="323b8-109">Выполнение отчета</span><span class="sxs-lookup"><span data-stu-id="323b8-109">Run the report</span></span>

1. <span data-ttu-id="323b8-110">Перейдите в раздел **Налог** \> **Запросы и отчеты** \> **Налоговые отчеты** \> **Налоговые платежи по коду**.</span><span class="sxs-lookup"><span data-stu-id="323b8-110">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span>
2. <span data-ttu-id="323b8-111">В поле **Валюта отчета** выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="323b8-111">In the **Report currency** field, select one of the following values:</span></span>

    - <span data-ttu-id="323b8-112">**Валюта учета** — печать сумм отчета в валюте учета.</span><span class="sxs-lookup"><span data-stu-id="323b8-112">**Accounting currency** – Print the report amounts in the accounting currency.</span></span>
    - <span data-ttu-id="323b8-113">**Валюта налогового кода** — печать сумм отчета в валютах налоговых кодов.</span><span class="sxs-lookup"><span data-stu-id="323b8-113">**Sales tax code currency** – Print the report amounts in the currencies of sales tax codes.</span></span>

    ![Диалоговое окно налоговых платежей по коду](media/Sales-tax-payment-by-code.png)

<span data-ttu-id="323b8-115">На следующем рисунке показан пример создаваемого отчета.</span><span class="sxs-lookup"><span data-stu-id="323b8-115">The following illustration shows an example of the report that is generated.</span></span> <span data-ttu-id="323b8-116">Отчет показывает, что код отчетности **101** имеет валюту **EUR**, если в поле **Валюта налога** указано значение **EUR** для налогового кода, которому назначен код отчетности.</span><span class="sxs-lookup"><span data-stu-id="323b8-116">The report shows that reporting code **101** has the **EUR** currency if the **Sales tax currency** field is set to **EUR** for the sales tax code that the reporting code is assigned to.</span></span>

![Пример отчета о налоговых платежах по коду](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]