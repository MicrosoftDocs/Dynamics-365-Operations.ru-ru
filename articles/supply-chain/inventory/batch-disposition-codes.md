---
title: Используйте коды методов обработки партий, чтобы пометить партии как доступные или недоступные
description: В этой статье описывается настройка и использование кодов методов обработки партий для маркировки партий как доступных или недоступных для использования в сводном планировании, резервировании, комплектации и/или отгрузке.
author: t-benebo
ms.date: 09/16/2022
ms.topic: article
ms.search.form: PdsDispositionMaster, InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-16
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: cfb0743a573550de93d75063df517e0c143f2568
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542476"
---
# <a name="use-batch-disposition-codes-to-mark-batches-as-available-or-unavailable"></a>Используйте коды методов обработки партий, чтобы пометить партии как доступные или недоступные

В этой статье описывается, как настроить и использовать *коды методов обработки партий*. Каждый код методов обработки партий имеет статус *Доступно* или *Недоступно*. Коды методов обработки партий присваиваются складским партиям, чтобы указать, доступна ли каждая партия для сводного планирования, резервирования, комплектации и/или отгрузки.

Чтобы использовать коды методов обработки партий, необходимо настроить коды и назначить их для тех партий, которыми вы хотите управлять.

## <a name="set-up-batch-disposition-codes"></a>Настройка кодов методов обработки партий

Необходимо настроить каждый код метода обработки партий, который будет использоваться в системе. Может быть создано любое нужное число кодов. (Например, можно создать коды для определения различных причин, по которым партия может быть доступна или недоступна.) Однако часто имеется только два кода: один для *доступных*, и один для *недоступных*. Можно также создавать пользовательские коды, которые позволяют использовать партию для некоторых операций, но не для других.

Выполните следующие действия, чтобы настроить коды методов обработки партий.

1. Перейдите в раздел **Управление запасами \> Настройка \> Партия \> Справочник метода обработки партии**.
1. Страница **Справочник метода обработки партии** содержит список текущих кодов методов обработки партий и позволяет создавать, удалять и изменять их. Выполните одно из следующих действий.

    - Чтобы изменить существующий код, выберите его в области списка.
    - Чтобы создать новый код, на панели операций выберите **Создать**.

1. Задайте следующие поля в заголовке нового или выбранного кода:

    - **Код метода обработки партий** — введите отображаемое имя для кода.
    - **Описание** — опишите, как код следует использовать.
    - **Статус метода обработки партий** — выберите статус, который применяется для партий, для которых назначен код:

        - *Недоступно* — партии нельзя использовать для сводного планирования, резервирования, комплектации или отгрузки. При выборе этого значения все параметры **Блокировать** на экспресс-вкладке **Настройка** устанавливаются в значение *Да*, а все параметры **Готовое** устанавливаются в значение *Нет*. Однако некоторые из этих настроек можно изменить для добавления исключений.
        - *Доступно* — партии можно использовать для сводного планирования, резервирования, комплектации и/или отгрузки. При выборе этого значения все параметры **Блокировать** на экспресс-вкладке **Настройка** устанавливаются в значение *Нет*, а все параметры **Готовое** устанавливаются в значение *Да*. Эти настройки будут доступны только для чтения, пока в поле **Статус метода обработки партии** установлено значение *Доступно*.

1. Если для поля **Статус метода обработки партии** указано значение *Недоступно*, можно настроить статус блокировки каждой операции (резервировать, скомплектовать и отгрузить) для каждого типа заказа (продажи, перемещение и производство). Для производственных заказов можно выбрать блокирование или разблокирование производственного журнала комплектации. Кроме того, можно выбрать блокирование или разблокирование сводного планирования. Параметры на экспресс-вкладке **Настройка** используются для блокирования или разблокирования каждой требуемой операции. Установите для параметра **Готовое** значение *Да*, чтобы включить сводное планирование, или установите для него значение *Нет*, чтобы заблокировать сводное планирование.

## <a name="assign-batch-disposition-codes-to-batches"></a>Назначение партиям кодов методов обработки партий

Определив необходимые коды методов обработки партий, выполните следующие действия, чтобы назначить их партиям.

1. Перейдите в раздел **Управление складом \> Настройка \> Запасы \> Партии**.
1. Выберите одну или несколько партий, которым нужно назначить код метода обработки партии.
1. В области действий откройте вкладку **Сброс** и выберите **Сброс кода метода обработки партии**.
1. В диалоговом окне **Изменить ограничения для складской партии** задайте в поле **Новый код метода обработки партии** имя кода, который необходимо назначить.
1. Выберите **ОК**, чтобы применить новый параметр и сохранить изменение.

    На странице **Партии** значения в столбцах **Код метода обработки партии** и **Статус метода обработки партии** обновляются таким образом, чтобы они соответствовали новым настройкам для выбранных партий.

## <a name="master-planning-example"></a>Пример сводного планирования

В этом примере показано, как коды метода обработки партий могут влиять на сводное планирование.

В данном примере коды методов обработки партий настраиваются следующим образом:

- *П-доступна:*

    - **Статуса метода обработки партии:** *Доступно*
    - **Готовое:** *Да*

- *П-недоступна*

    - **Статуса метода обработки партии:** *Недоступно*
    - **Готовое:** *Нет*

Имеется продукт (*Продукт-1*) с двумя партиями: *Партия-A* и *Партия-B*. Эти партии настроены следующим образом:

- *Партия-A*

    - **Код метода обработки партии:** *П-доступна*
    - **Количество в наличии:** 1

- *Партия-B*

    - **Код метода обработки партии:** *П-недоступна*
    - **Количество в наличии:** 1

Имеется заказ на продажу (*SO1*) для количества 2 продукта *Продукт-1*. Дата поставки — через три дня от сегодняшнего дня.

Вы запускаете сводное планирование и устанавливаете следующие значения, которые относятся к этому примеру:

- **Спланированный заказ:** *Заказ на покупку*
- **Стратегия пополнения:** *Требование*
- **Время упреждения:** *0*

В результате выполнения планирования система использует доступную партию (*Партия-A*) для покрытия количества 1 продукта *Продукт-1* для заказа на продажу *SO1*. Однако она не может использовать партию *Партия-B*, поскольку эта партия помечена как недоступная для планирования. Таким образом, для покрытия оставшегося количества система создает спланированный заказ на покупку (*PPO1*) для новой партии продукта *Продукт-1*.

На следующем рисунке показана временная шкала результата планирования.

![Пример, который показывает, как коды метода обработки партий могут влиять на сводное планирование.](media/batch-codes-planning-example.png "Пример, который показывает, как коды метода обработки партий могут влиять на сводное планирование")
