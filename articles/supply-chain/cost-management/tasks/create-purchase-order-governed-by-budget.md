---
title: Создание заказа на покупку в соответствии с бюджетом
description: Эта процедура служит для создания заказа на покупку, который проверяется на наличие доступного бюджета.
author: JennySong-SH
ms.date: 06/15/2020
ms.topic: business-process
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa9777ad3aa487dfb558879335f93f347b8ac749
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016198"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Создание заказа на покупку в соответствии с бюджетом

[!include [banner](../../includes/banner.md)]

Эта процедура служит для создания заказа на покупку, который проверяется на наличие доступного бюджета.

## <a name="review-the-budget-control-configuration"></a>Просмотр конфигурации бюджетного контроля

1. Перейдите в раздел **Бюджетирование > Настройка > Бюджетный контроль > Конфигурация бюджетного контроля**.
1. Выберите вкладку **Доступные бюджетные средства**.
1. Выберите вкладку **Документы и журналы**.
1. Выберите вкладку **Определение правил бюджетного контроля**.
1. Выберите вкладку **Определить бюджетные группы**.
1. Закройте страницу.

## <a name="create-a-purchase-order"></a>Создание заказа на покупку

1. Перейдите в раздел **Закупки и источники > Заказы на покупку > Все заказы на покупку**.
1. Выберите **Создать**.
1. В поле **Счет поставщика** введите или выберите значение.
1. Перейдите на экспресс-вкладку **Общие**.
1. В поле **Дата учета** задайте дату.
1. Выберите **ОК**, чтобы закрыть диалоговое окно и открыть новый заказ на покупку.
1. На экспресс-вкладке **Строки заказа на покупку** выберите **Добавить строку** на панели инструментов, чтобы добавить новую строку, затем внесите в строку необходимые данные, чтобы добавить номенклатуру в заказ.
1. На панели инструментов экспресс-вкладки **Строки заказа на покупку** выберите **Финансы \> Распределить суммы**.
1. В поле **Счет учета** укажите счет.
1. Закройте страницу.

## <a name="perform-budget-checking"></a>Выполнить проверку бюджета

1. Продолжайте работать с заказом на покупку, к которому была добавлена строка.
1. На панели инструментов экспресс-вкладки **Строки заказа на покупку** выберите **Финансы \> Выполнить проверку бюджета**.
1. На панели инструментов экспресс-вкладки **Строки заказа на покупку** выберите **Финансы \> Ошибки или предупреждения бюджетных проверок**.
1. Открывается диалоговое окно **Ошибки или предупреждения бюджетных проверок**. Проверьте результаты проверки, затем выберите кнопку **Закрыть**, чтобы закрыть диалоговое окно.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]