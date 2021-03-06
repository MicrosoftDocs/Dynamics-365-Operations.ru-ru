---
title: Определение баллов поощрения по программе лояльности
description: Эта процедура содержит инструкции по определению баллов поощрения лояльности.
author: scott-tucker
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e7f3b19513bb25d1976d2e4d0e235c347c38ccb4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798473"
---
# <a name="define-loyalty-reward-points"></a>Определение баллов поощрения по программе лояльности

[!include [banner](../includes/banner.md)]

Эта процедура содержит инструкции по определению баллов поощрения лояльности. Необходимо настроить баллы поощрения лояльности перед настройкой программы лояльности. В этой процедуре используется компания с демонстрационными данными USRT.

1. Перейдите в раздел "Retail и Commerce" > "Клиенты" > "Лояльность" > "Баллы поощрения по программе лояльности".
2. Нажмите Создать.
3. В поле "Код точки вознаграждения" введите значение.
4. В поле "Описание" введите значение.
5. В поле "Тип точки вознаграждения" выберите один из вариантов.
    * Выберите количество, если вы хотите, чтобы баллы поощрения округлялись до ближайшего целого числа. Выберите "Сумма", если вы хотите, чтобы баллы поощрения округлялись в соответствии с правилами округления валюты. При выборе варианта "Количество" пропустите следующий шаг этой процедуры.  
6. В поле "Валюта" введите значение.
    * В случае выбора варианта "Сумма" для баллов поощрения все начисленные баллы поощрения будут иметь выбранную валюту. В случае выбора для баллов поощрения типа "Количество" это поле неприменимо, пропустите данный шаг.  
7. Снимите или установите флажок "Погашаемо".
8. В поле "Классификация погашения" введите число.
    * Классификация погашения используется, если два или более подлежащих погашению набора баллов поощрения могут быть использованы для оплаты продуктов. Если два набора баллов поощрения имеют одинаковый класс погашения, будет использоваться тот из них, который требует меньшего числа баллов.  
9. В поле "Значение срока действия" введите число.
    * Срок действия баллов поощрения истекает через определенное количество дней, месяцев или лет после даты начисления баллов. Значение "0" означает, что срок действия баллов поощрения лояльности никогда не истечет.  
10. В поле "Единица измерения срока действия" выберите параметр.
11. Нажмите кнопку "Сохранить".



[!INCLUDE[footer-include](../../includes/footer-banner.md)]