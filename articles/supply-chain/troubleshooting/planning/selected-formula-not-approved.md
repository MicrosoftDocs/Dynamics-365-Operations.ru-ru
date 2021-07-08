---
title: Выбранный номер формулы не утверждается для заказа партии
description: При попытке утверждения спланированного заказа выводится сообщение об ошибке, в котором говорится, что выбранный номер формулы не утвержден для заказа партии.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294160"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a><span data-ttu-id="cb817-103">Выбранный номер формулы не утверждается для заказа партии</span><span class="sxs-lookup"><span data-stu-id="cb817-103">Selected formula number isn't approved for a batch order</span></span>

<span data-ttu-id="cb817-104">Код ошибки: PRO2614</span><span class="sxs-lookup"><span data-stu-id="cb817-104">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="cb817-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="cb817-105">Symptoms</span></span>

<span data-ttu-id="cb817-106">При попытке утвердить спланированный заказ выводится следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="cb817-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="cb817-107">Выбранный номер формулы не утвержден для партионного заказа.</span><span class="sxs-lookup"><span data-stu-id="cb817-107">The selected formula number is not approved for a batch order.</span></span>

## <a name="cause"></a><span data-ttu-id="cb817-108">Причина</span><span class="sxs-lookup"><span data-stu-id="cb817-108">Cause</span></span>

<span data-ttu-id="cb817-109">Система проверяет операцию утверждения, чтобы убедиться, что утвержденная формула доступна для активной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="cb817-109">The system validates the firming operation to make sure that an approved formula is available for the active item.</span></span> <span data-ttu-id="cb817-110">Вероятно, необходимо утвердить формулу.</span><span class="sxs-lookup"><span data-stu-id="cb817-110">You must probably approve the formula.</span></span>

## <a name="resolution"></a><span data-ttu-id="cb817-111">Решение</span><span class="sxs-lookup"><span data-stu-id="cb817-111">Resolution</span></span>

<span data-ttu-id="cb817-112">Чтобы утвердить формулу, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cb817-112">To approve a formula, follow these steps.</span></span>

1. <span data-ttu-id="cb817-113">Перейдите в раздел **Управление сведениями о продукте \> Спецификации и формулы \> Формулы**.</span><span class="sxs-lookup"><span data-stu-id="cb817-113">Go to **Product information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="cb817-114">Выберите соответствующую формулу.</span><span class="sxs-lookup"><span data-stu-id="cb817-114">Select the relevant formula.</span></span>
1. <span data-ttu-id="cb817-115">В области действий на вкладке **Формула** в группе **Поддержка** выберите **Утвердить формулу**.</span><span class="sxs-lookup"><span data-stu-id="cb817-115">On the Action Pane, on the **Formula** tab, in the **Maintain** group, select **Approve formula**.</span></span>
1. <span data-ttu-id="cb817-116">В диалоговом окне **Утверждение спецификации или формулы** выберите утверждающего и затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cb817-116">In the **Approve BOM or formula** dialog box, select an approver, and then select **OK**.</span></span>
