---
title: Создание заказов на работу
description: В этой статье описывается, как создавать заказы на работу в модуле "Управление активами".
author: johanhoffmann
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ba01a90f805300a27e4550e1371fb55d5e3a7536
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335056"
---
# <a name="creating-work-orders"></a>Создание заказов на работу

[!include [banner](../../includes/banner.md)]

После планирования заданий профилактического обслуживания следующим шагом будет создание заказов на работу для них. Можно выполнить этот шаг, используя одно из графиков обслуживания. Запланированные задания в графике обслуживания могут иметь различные типы ссылок, как описано в следующей таблице.

| Тип ссылки | описание |
|---|---|
| Планы обслуживания | Задания профилактического обслуживания, основанные на типах планов обслуживания *Время* или *Счетчик*. |
| Циклы обслуживания | Задания профилактического обслуживания, содержащие несколько активов, требующих подобного типа обслуживания. |
| Запрос на обслуживание | Запрос, созданный вручную для обслуживания или ремонта актива. Этот запрос может быть преобразован в заказ на работу. |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a>Создание заказов на работу на основе графика обслуживания

Для создания заказов на работу, которые основаны на расписании обслуживания, выполните следующие действия.

1. Откройте одну из следующих страниц, в зависимости от того, как вы хотите выбирать элементы планирования для заказов на работу:

    - Все расписание обслуживания ( **Управление активами \> Расписание обслуживания \> Все расписание обслуживания**)
    - Откройте строки расписания обслуживания (**Управление активами \> Расписание обслуживания \> Открыть строки расписания обслуживания**)
    - Откройте пулы расписаний обслуживания (**Управление активами \> Расписание обслуживания \> Открыть пулы расписаний обслуживания**)

1. В сетке установите флажок для каждого задания планового обслуживания, для которого необходимо создать заказ на работу. Затем на панели операций выберите **Заказ на работу**.

    Откроется диалоговое окно **Создание заказов на работу**. В поле **Прогноз часов обслуживания** отображается общее количество часов прогноза для выбранных строк.

    ![Диалоговое окно создания заказов на работу.](media/18-preventive-maintenance.png)

1. В разделе **Параметры** укажите количество заказов на работу, которые должны быть созданы. Выберите один из следующих вариантов:

    - **Один заказ на работу на строку** — создание одного заказа на работу на каждую строку графика обслуживания.
    - **Один заказ на работу на** — создание заказов на работу, сгруппированных в соответствии с настройками других параметров, которые становятся доступными при выборе данного параметра.

1. В поле **Тип заказа на работу** выберите тип заказа на работу, который будет использоваться для всех создаваемых заказов на работу.
1. Выберите **ОК**, чтобы создать заказы на работу в соответствии с вашими настройками.

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a>Группировка строк заказов на работу, которые создаются автоматически при выполнении плана обслуживания

Эта функция позволяет определить правила для группировки строк заказа на работу в одном заказе на работу, когда система настроена на автоматическое создание заказов на работу на основе плана обслуживания. Ранее автоматически созданные заказы на работу могли содержать только одну строку. Однако теперь можно группировать заказы на работу по, например, активу, типу актива или функциональному местоположению. (Созданные вручную заказы на работу уже могут быть сгруппированы таким образом, как это описано в предыдущем разделе этой статьи.)

### <a name="enable-grouping-for-automatically-generated-work-orders"></a>Включение группировки для автоматически создаваемых заказов на работу

Прежде чем использовать эту функцию, ее необходимо включить для системы. Администраторы могут использовать параметры [управления компонентами](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения. В рабочей области **Управление функциями** эта функция перечисляется следующими способами:

- **Модуль:** *Управление активами*
- **Имя компонента:** *Применение правил группировки заказов на работу во время выполнения плана обслуживания*

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a>Настройка группирования для автоматически создаваемых заказов на работу

Чтобы настроить группирование для автоматически создаваемых заказов на работу, выполните следующие действия.

1. Перейдите в раздел **Управление активами \> Настройка \> Профилактическое обслуживание \> Планы обслуживания**.
1. Для каждого плана, в котором необходимо создать сгруппированные заказы на работу, выполните следующие действия:

    1. Выберите план в области списка.
    1. На экспресс-вкладке **Строки** убедитесь, что флажок **Автоматически создать** установлен на каждой строке.

1. Перейдите в раздел **Управление активами \> Периодические \> Профилактическое обслуживание \> Составление графика планов обслуживания**.
1. В диалоговом окне **Составление графика планов обслуживания** в разделе **Период** укажите временной горизонт для плана (насколько далеко вперед искать запланированных задания обслуживания для создания для них работы).
1. Установите для параметра **Автоматически создавать заказ на работу по графику** значение *Да*.
1. В разделе **Заказ на работу** выберите один из следующих вариантов:

    - **Один заказ на работу на строку** — создание одного заказа на работу на каждую строку графика обслуживания. (Этот параметр предоставляет те же функциональные возможности, которые доступны, если функция *Применение правил группировки заказов на работу во время выполнения плана обслуживания* отключена.)
    - **Один заказ на работу на** — создание заказов на работу, сгруппированных в соответствии с настройками других параметров, которые становятся доступными при выборе данного параметра.

1. Если требуется применить параметры при выполнении только некоторых планов обслуживания, на экспресс-вкладке **Включаемые записи** добавьте фильтры так же, как это возможно для других пакетных заданий в Microsoft Dynamics 365 Supply Chain Management.
1. На экспресс-вкладке **Выполнять в фоновом режиме** настройте параметры пакетной обработки и планирования так, как вы бы это делали для других пакетных заданий в Supply Chain Management.
1. Выберите **ОК**, чтобы выполнить и/или спланировать выбранные планы обслуживания.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]