---
title: Кредитование проводок по подписке
description: Эта тема показывает, как кредитовать проводки по подписке.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4238c625930767990d28a206b10a4d71841f2ad8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247510"
---
# <a name="credit-subscription-transactions"></a><span data-ttu-id="439bb-103">Кредитование проводок по подписке</span><span class="sxs-lookup"><span data-stu-id="439bb-103">Credit subscription transactions</span></span> 

[!include [banner](../includes/banner.md)]


## <a name="credit-subscription-transactions"></a><span data-ttu-id="439bb-104">Кредитование проводок по подписке</span><span class="sxs-lookup"><span data-stu-id="439bb-104">Credit subscription transactions</span></span>

1.  <span data-ttu-id="439bb-105">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Подписки на сервисное обслуживание** \> **Все подписки на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="439bb-105">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span>

2.  <span data-ttu-id="439bb-106">Выберите подписку, присоединенную к проводке подписки, для которой необходимо создать кредит-ноту.</span><span class="sxs-lookup"><span data-stu-id="439bb-106">Select the subscription attached to the subscription transaction for which you want to create a credit note.</span></span>

3.  <span data-ttu-id="439bb-107">Перейдите на вкладку **Анализировать** и нажмите кнопку **Проводки по сборам** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="439bb-107">Select the **Analyze** tab, and then click the **Fee transactions** button on the Action Pane.</span></span>

4.  <span data-ttu-id="439bb-108">В форме **Проводки по сборам** выберите проводку, для которой необходимо создать кредит-ноту.</span><span class="sxs-lookup"><span data-stu-id="439bb-108">From the **Fee transactions** form, select the transaction for which you want to create a credit note.</span></span>

5.  <span data-ttu-id="439bb-109">Щелкните **Функции** \> **Выбор для кредит-ноты**.</span><span class="sxs-lookup"><span data-stu-id="439bb-109">Click **Functions** \> **Select for credit note**.</span></span>

6.  <span data-ttu-id="439bb-110">В форме **Выбор для кредит-ноты** выберите проводку, которую необходимо кредитовать, и щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="439bb-110">From the **Select for credit note** form, select the transaction that you want to credit and then click **OK**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="439bb-111">При создании кредит-ноты обязательно выберите <STRONG>Кредит-ноты</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="439bb-111">When you create the credit note, make sure that you select <STRONG>Credit notes</STRONG>.</span></span> <span data-ttu-id="439bb-112">Это доступно в списке <STRONG>Метод выставления накладной</STRONG> в диалоговом окне <STRONG>Создать накладную</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="439bb-112">This is found in the <STRONG>Invoicing method</STRONG> list in the <STRONG>Create invoice</STRONG> dialog box.</span></span></P>

<span data-ttu-id="439bb-113">Если значение поля **Реверсировать начисления на кредитование** в форме **Параметры управления сервисным обслуживанием** равно **Вручную**, необходимо отдельно реверсировать каждую проводку начисленного дохода, и только после этого создавать предложение кредит-ноты для проводки.</span><span class="sxs-lookup"><span data-stu-id="439bb-113">If the **Reverse accruals on crediting** field in the **Service management parameters** form is set to **Manual**, you have to reverse each accrued revenue transaction individually before you create a credit note proposal for the transaction.</span></span>

## <a name="see-also"></a><span data-ttu-id="439bb-114">См. также</span><span class="sxs-lookup"><span data-stu-id="439bb-114">See also</span></span>

[<span data-ttu-id="439bb-115">Обработка накладных для проводок по подписке</span><span class="sxs-lookup"><span data-stu-id="439bb-115">Invoice subscription transactions</span></span>](invoice-subscription-transactions.md)


 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]