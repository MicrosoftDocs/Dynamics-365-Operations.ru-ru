---
title: Внутрихолдинговые расходы
description: Работник, нанятый одним юридическим лицом в организации может, выполнять работу для другого юридического лица в той же организации. В этом случае можно использовать функцию внутрихолдинговых расходов, чтобы отнести расходы на работника на то юридическое лицо, для которого была выполнена работа.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390892"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="7de1c-104">Внутрихолдинговые расходы</span><span class="sxs-lookup"><span data-stu-id="7de1c-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7de1c-105">Работник, нанятый одним юридическим лицом в организации может, выполнять работу для другого юридического лица в той же организации.</span><span class="sxs-lookup"><span data-stu-id="7de1c-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="7de1c-106">В этом случае можно использовать функцию внутрихолдинговых расходов, чтобы отнести расходы на работника на то юридическое лицо, для которого была выполнена работа.</span><span class="sxs-lookup"><span data-stu-id="7de1c-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="7de1c-107">Юридический субъект, в котором используется работник, называется юридическое лицо, передающее дополнительных работников.</span><span class="sxs-lookup"><span data-stu-id="7de1c-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="7de1c-108">Юридическое лицо, для которого работник производит расходы, называется юридическим лицом, берущим работников в аренду.</span><span class="sxs-lookup"><span data-stu-id="7de1c-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="7de1c-109">Прежде чем работник сможет создать и отправить расходы за работу, выполненную для другого юридического лица, в юридическом лице, которое предоставляет работников в аренду, на странице **Параметры управления расходами** необходимо установить флажок **Разрешать строки внутрихолдинговых расходов**.</span><span class="sxs-lookup"><span data-stu-id="7de1c-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="7de1c-110">Разноска налога для внутрихолдинговых расходов</span><span class="sxs-lookup"><span data-stu-id="7de1c-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7de1c-111">Если необходимо использовать налоговые группы, которые связаны с юридическим лицом, предоставляющим дополнительных работников (источник), а не с юридическим лицом (место назначения) привлекающим дополнительных работников в отчете о расходах, необходимо настроить это в главной книге в соответствии с настройкой налога.</span><span class="sxs-lookup"><span data-stu-id="7de1c-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="7de1c-112">Если параметр главной книги, **юридическое лицо для внутрихолдинговой разноски налога** настроена на **Источник** и для **Применить правила налогообложения** установлено значение **нет**, будет использоваться комбинация налогов для юридического лица, предоставляющего дополнительных работников.</span><span class="sxs-lookup"><span data-stu-id="7de1c-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="7de1c-113">Когда для одного и того же параметра указано **Место назначения**, будет использоваться комбинация налогов для юридического лица, привлекающего дополнительных работников.</span><span class="sxs-lookup"><span data-stu-id="7de1c-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="7de1c-114">Для юридических лиц в США, если для параметра выбрано значение **Источник**, поле **Входящий налог** должно быть также настроено на странице **Группы разноски ГК**.</span><span class="sxs-lookup"><span data-stu-id="7de1c-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="7de1c-115">В механизме учета будут использоваться сведения из этого поля для записи учета связанного налога.</span><span class="sxs-lookup"><span data-stu-id="7de1c-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="7de1c-116">Поведение соответствует строкам расходов, разнесенным с проектом или без него.</span><span class="sxs-lookup"><span data-stu-id="7de1c-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
