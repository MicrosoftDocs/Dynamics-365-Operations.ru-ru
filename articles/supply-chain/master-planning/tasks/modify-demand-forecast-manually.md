---
title: 'Руководство: изменение прогноза спроса вручную'
description: В этом разделе описывается, как внести изменения в прогноз для номенклатуры
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12ccf90b9971379e8931bd48d6243a855bb795
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224018"
---
# <a name="guide-modify-a-demand-forecast-manually"></a>Руководство: изменение прогноза спроса вручную

[!include [banner](../../includes/banner.md)]

В этой процедуре показано, как внести изменения в прогноз для номенклатуры. Эта процедура предназначена для планировщика производства.

## <a name="modify-the-forecast-for-a-selected-item"></a>Изменение прогноза для выбранной номенклатуры

Для изменения прогноза для выбранной номенклатуры:

1. Перейдите к **Модули \> Управление сведениями о производстве \> Продукты \> Выпущенные продукты**.
1. В списке найдите и выберите требуемую запись. Выберите номенклатуру, прогноз для которой требуется изменить.
1. На панели операций откройте вкладку **план** и выберите **прогноз спроса**.
1. В списке выберите строку. Если строк прогноза нет, создайте новую строку, выбрав **Создать** на панели операций.  
1. В поле **Продаваемое количество** введите положительное число. Это число представляет собой прогнозное количество для номенклатуры. При вводе отрицательного числа отображается сообщение об ошибке.
1. Заполните соответствующим образом остальные поля.
1. На панели операций выберите **Сохранить**.

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a>Изменение прогноза для одной или нескольких номенклатур с помощью Microsoft Excel

Чтобы изменить прогноз для одной или нескольких номенклатур с помощью Microsoft Excel:

1. Выполните одно из следующих действий.
    - Откройте страницу **прогноз спроса** для любой номенклатуры (но не имеет значения, какой из них), как описано в предыдущем разделе.
    - Перейдите в раздел **Сводное планирование \> Прогнозирование \> Ручной ввод прогноза \> Строки прогноза спроса**.
1. На панели операций выберите **Открыть в Microsoft Office \> записи прогноза спроса**.
1. Выберите место загрузки, сохраните, а затем откройте загруженный файл в Excel.
1. Если отображается предупреждение, выберите **Разрешить изменение**.
1. В Microsoft Excel выполните вход в Supply Chain Management с помощью панели задач Microsoft Dynamics. Необходимо войти в систему с включенным параметром **Оставаться в системе**, и вы должны доверять приложению для подключения к данным.
1. В таблице Excel отображаются все строки текущего прогноза спроса для вашей компании.  Добавлять, удалять и изменять строки прогноза спроса, при необходимости.
1. Выберите **Опубликовать** в панели задач Microsoft Dynamics, чтобы отправить изменения обратно в Supply Chain Management.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
