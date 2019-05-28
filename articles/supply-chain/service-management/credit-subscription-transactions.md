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
# <a name="credit-subscription-transactions"></a>Кредитование проводок по подписке 

[!include [banner](../includes/banner.md)]


## <a name="credit-subscription-transactions"></a>Кредитование проводок по подписке

1.  Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Подписки на сервисное обслуживание** \> **Все подписки на сервисное обслуживание**.

2.  Выберите подписку, присоединенную к проводке подписки, для которой необходимо создать кредит-ноту.

3.  Перейдите на вкладку **Анализировать** и нажмите кнопку **Проводки по сборам** на панели операций.

4.  В форме **Проводки по сборам** выберите проводку, для которой необходимо создать кредит-ноту.

5.  Щелкните **Функции** \> **Выбор для кредит-ноты**.

6.  В форме **Выбор для кредит-ноты** выберите проводку, которую необходимо кредитовать, и щелкните **OK**.


> [!NOTE]
> <P>При создании кредит-ноты обязательно выберите <STRONG>Кредит-ноты</STRONG>. Это доступно в списке <STRONG>Метод выставления накладной</STRONG> в диалоговом окне <STRONG>Создать накладную</STRONG>.</P>

Если значение поля **Реверсировать начисления на кредитование** в форме **Параметры управления сервисным обслуживанием** равно **Вручную**, необходимо отдельно реверсировать каждую проводку начисленного дохода, и только после этого создавать предложение кредит-ноты для проводки.

## <a name="see-also"></a>См. также

[Обработка накладных для проводок по подписке](invoice-subscription-transactions.md)


 
