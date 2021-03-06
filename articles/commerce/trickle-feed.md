---
title: Поточное создание заказов по проводкам розничного магазина
description: В этом разделе описана процедура поточного создания заказов по проводкам магазина в Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: e0686b1b3113440808ea195683e15fb2c66b4558
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801851"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Поточное создание заказов по проводкам розничного магазина

[!include [banner](includes/banner.md)]

В Dynamics 365 Retail 10.0.4 и более ранних версий разноска журналов операций выполняется в конце каждого дня. При этом большие проводки должны быть обработаны за ограниченное время, что иногда приводит к перегрузке, блокировкам и сбоям в процессе разноски. Кроме того, при этом невозможно отслеживать доходы и платежи в бухгалтерских книгах в течение дня.

В Retail версии 10.0.5 появилась функция поточного создания заказов, позволяющая обрабатывать проводки в течение дня, а в конце дня выполнять только финансовую выверку платежных средств и других операций с наличными. Эта функция распределяет нагрузку по созданию заказов на продажу, накладных и платежей на весь день, упрощая отслеживание результатов и позволяя отражать доходы и платежи в книгах почти в режиме реального времени. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Как использовать поточную разноску
  
1. Чтобы включить разноску розничных проводок на основе поточной загрузки, включите функцию **Журналы операций розничной торговли — поточная разноска**, используя управление функциями.

    > [!IMPORTANT]
    > Перед включением этой функции убедитесь в отсутствии ожидающих разноски журналов операций.

2. Текущий журнал операций будет разбит на два: журнал проводок и финансовый отчет.

      - В журнале проводок будут собраны все неразнесенные и проверенные проводки для создания с заданной периодичностью заказов на продажу, накладных по продаже, журналов платежей и скидок и проводок по доходам/расходам. Необходимо настроить этот процесс на частое выполнение, чтобы документы создавались при загрузке проводок в Headquarters через P-задание. Поскольку журнал проводок уже создает заказы на продажу и накладные по продаже, настраивать пакетное задание **Разнести запасы** больше не требуется. Однако его все равно можно использовать при необходимости.  
      
     - Финансовый отчет должен создаваться в конце дня и поддерживает только способ закрытия **Смена**. Это отчет служит только для финансовой выверки и создания журналов для разниц между суммами инвентаризации и суммами проводок по различным платежным средствам, а также журналов для других проводок управления кассой.   

3. Чтобы сформировать журнал проводок, выберите **Retail и Commerce > ИТ Retail и Commerce > Разноска POS > Пакетный расчет журналов проводок**. Чтобы разнести журналы проводок в пакетном режиме, выберите **Retail и Commerce > ИТ Retail и Commerce > Разноска POS > Пакетная разноска журналов проводок**.

4. Чтобы сформировать финансовый отчет, выберите **Retail и Commerce > ИТ Retail и Commerce > Разноска POS > Пакетный расчет финансовых отчетов**. Чтобы разнести финансовые отчеты в пакетном режиме, выберите **Retail и Commerce > ИТ Retail и Commerce > Разноска POS > Пакетная разноска финансовых отчетов**.

> [!NOTE]
> Пункты меню **Retail и Commerce > ИТ Retail и Commerce > Разноска POS > Пакетный расчет журналов операций** и **Retail и Commerce > ИТ Retail и Commerce > Разноска POS > Пакетная разноска журналов операций** будут удалены с появлением этой новой функции.

Кроме того, журналы операций и финансовые отчеты можно создавать вручную. Выберите **Retail и Commerce > Каналы > Магазины**, а затем — **Журналы операций**. Щелкните **Создать**, затем выберите тип журнала операций, который требуется создать. В полях на странице **Журналы операций** и действиях раздела **Группа журналов** будут показаны данные и действия, соответствующие выбранному типу журнала.


[!INCLUDE[footer-include](../includes/footer-banner.md)]