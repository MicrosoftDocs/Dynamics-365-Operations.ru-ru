---
title: Кредитование проводок по подписке
description: Эта тема показывает, как кредитовать проводки по подписке.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd6c91126604fc704ac0283d5db062077275e725
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571267"
---
# <a name="credit-subscription-transactions"></a><span data-ttu-id="d43e6-103">Кредитование проводок по подписке</span><span class="sxs-lookup"><span data-stu-id="d43e6-103">Credit subscription transactions</span></span> 

[!include [banner](../includes/banner.md)]


## <a name="credit-subscription-transactions"></a><span data-ttu-id="d43e6-104">Кредитование проводок по подписке</span><span class="sxs-lookup"><span data-stu-id="d43e6-104">Credit subscription transactions</span></span>

1.  <span data-ttu-id="d43e6-105">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Подписки на сервисное обслуживание** \> **Все подписки на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="d43e6-105">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span>

2.  <span data-ttu-id="d43e6-106">Выберите подписку, присоединенную к проводке подписки, для которой необходимо создать кредит-ноту.</span><span class="sxs-lookup"><span data-stu-id="d43e6-106">Select the subscription attached to the subscription transaction for which you want to create a credit note.</span></span>

3.  <span data-ttu-id="d43e6-107">Перейдите на вкладку **Анализировать** и нажмите кнопку **Проводки по сборам** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="d43e6-107">Select the **Analyze** tab, and then click the **Fee transactions** button on the Action Pane.</span></span>

4.  <span data-ttu-id="d43e6-108">В форме **Проводки по сборам** выберите проводку, для которой необходимо создать кредит-ноту.</span><span class="sxs-lookup"><span data-stu-id="d43e6-108">From the **Fee transactions** form, select the transaction for which you want to create a credit note.</span></span>

5.  <span data-ttu-id="d43e6-109">Щелкните **Функции** \> **Выбор для кредит-ноты**.</span><span class="sxs-lookup"><span data-stu-id="d43e6-109">Click **Functions** \> **Select for credit note**.</span></span>

6.  <span data-ttu-id="d43e6-110">В форме **Выбор для кредит-ноты** выберите проводку, которую необходимо кредитовать, и щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="d43e6-110">From the **Select for credit note** form, select the transaction that you want to credit and then click **OK**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d43e6-111">При создании кредит-ноты обязательно выберите <STRONG>Кредит-ноты</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="d43e6-111">When you create the credit note, make sure that you select <STRONG>Credit notes</STRONG>.</span></span> <span data-ttu-id="d43e6-112">Это доступно в списке <STRONG>Метод выставления накладной</STRONG> в диалоговом окне <STRONG>Создать накладную</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="d43e6-112">This is found in the <STRONG>Invoicing method</STRONG> list in the <STRONG>Create invoice</STRONG> dialog box.</span></span></P>

<span data-ttu-id="d43e6-113">Если значение поля **Реверсировать начисления на кредитование** в форме **Параметры управления сервисным обслуживанием** равно **Вручную**, необходимо отдельно реверсировать каждую проводку начисленного дохода, и только после этого создавать предложение кредит-ноты для проводки.</span><span class="sxs-lookup"><span data-stu-id="d43e6-113">If the **Reverse accruals on crediting** field in the **Service management parameters** form is set to **Manual**, you have to reverse each accrued revenue transaction individually before you create a credit note proposal for the transaction.</span></span>

## <a name="see-also"></a><span data-ttu-id="d43e6-114">См. также</span><span class="sxs-lookup"><span data-stu-id="d43e6-114">See also</span></span>

[<span data-ttu-id="d43e6-115">Обработка накладных для проводок по подписке</span><span class="sxs-lookup"><span data-stu-id="d43e6-115">Invoice subscription transactions</span></span>](invoice-subscription-transactions.md)


 
