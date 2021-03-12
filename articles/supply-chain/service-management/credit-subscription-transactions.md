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
ms.openlocfilehash: ff8dbf5cad2cc1fa2cd465420629e39c9ffb512b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974618"
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


 
