---
title: Расчет прогноза номенклатуры
description: В этой статье описывается, как рассчитать прогноз по номенклатуре в модуле "Управление активами".
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 25e9b00533fb183b27c1bbe616cf6f414b44b5e7
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016111"
---
# <a name="calculate-item-forecast"></a>Рассчитать прогноз номенклатуры

[!include [banner](../../includes/banner.md)]

 

Точно так же, как можно выполнить расчеты загрузки мощностей, которые описаны в предыдущем разделе, можно также выполнять расчеты прогноза по номенклатурам:

- строки графика обслуживания  
- заказы на работу, которые еще не были запланированы  
- запланированные заказы на работу

Это полезно, если требуется получить обзор ожидаемого потребления номенклатур (запасные части, а также другие номенклатуры, необходимые для выполнения заказов на работу) за конкретный период. Расчет прогноза по номенклатурам может выполняться по всем активам или по выбранным активам. Кроме того, можно выполнить расчет по мероприятию простоя из-за обслуживания (**Все мероприятия по простою из-за обслуживания** или **Активные мероприятия по простою из-за обслуживания**) или по пулу заказов на работу (**Все пулы заказов на работу** или **Активные пулы заказов на работу**).

1. Щелкните **Управление активами** > **Запросы** > **Прогноз по номенклатурам** или **Управление активами** > **Пулы заказов на работу** > **Все пулы заказов на работу** / **Активные пулы заказов на работу** > выберите пул заказов на работу в списке > кнопка **Прогноз по номенклатурам** или **Управление активами** > **Мероприятия по простою из-за обслуживания** > **Все мероприятия по простою из-за обслуживания** / **Активные мероприятия по простою из-за обслуживания** > выберите мероприятие по простою из-за обслуживания в списке > кнопка **Прогноз по номенклатурам**.

2. В диалоговом окне **Рассчитать прогноз номенклатуры** выберите период для расчета в полях **Дата и время начала** и **Дата и время окончания**.

3. Выберите "Да" на кнопке-переключателе **Включить график обслуживания**, если требуется включить строки графика обслуживания в расчет прогноза.

4. Выберите "Да" на кнопке-переключателе **Включить заказ на работу**, если требуется включить задания заказа на работу в расчет прогноза.

5. Можно использовать поле **Уровень**, чтобы указать, насколько подробными должны быть строки прогноза по номенклатурам относительно функциональных местоположений. 

      Например, если вставить число "1" в это поле, и имеется структура функциональных местоположений с несколькими уровнями, все строки графика обслуживания и заказы на работу для функционального местоположения будут показаны на верхнем уровне, и поэтому часы по строке могут быть добавлены из функциональных местоположений, расположенных на более низком уровне. 
  
      Если вставить число "0" в поле **Уровень**, будет выведен подробный результат, отображающий все строки графика обслуживания и все заказы на работу на всех уровнях функциональных местоположений, к которым они относятся.

6. Нажмите **ОК**, чтобы начать расчет.

7. В группах **Группировать по...** щелкните соответствующие кнопки, чтобы отобразить необходимый уровень детализации для расчета. На снимке экрана ниже выбранные кнопки **Группировать по** выделяются синим цветом. Нажимайте кнопку, чтобы активировать или деактивировать ее.

8. Нажмите кнопку **Отобразить аналитики**, если требуется просмотреть аналитики продукта, хранения или отслеживания, имеющие отношение к номенклатурам. Выберите соответствующие флажки и щелкните **OK**.

![Рисунок 1.](media/02-capacity-planning.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]