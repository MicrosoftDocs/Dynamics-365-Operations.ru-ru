---
title: Управление стоимостью для ошибки актива
description: В этой статье описывается контроль затрат на неисправности активов в модуле "Управление активами".
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 553b89a43b656669b7730b19898f3a5d81a3873a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889674"
---
# <a name="asset-fault-cost-control"></a>Управление стоимостью для ошибки актива

[!include [banner](../../includes/banner.md)]

 

В управлении активами можно рассчитать затраты на регистрации неисправностей активов, чтобы получить обзор фактических затрат по сравнению с бюджетными затратами. Фактические затраты основываются на разнесенных проводках. Датой является дата неисправности, в которую был записан признак неисправности.

1. Щелкните **Управление активами** > **Запросы** > **Ошибка актива** > **Управление стоимостью для ошибки актива**.

2. В диалоговом окне **Управление стоимостью для ошибки актива** выберите набор финансовых аналитик, который должен быть включен в расчет, если это необходимо.

4. Если не требуется показывать результаты, содержащие нулевые затраты, выберите "Да" для переключателя **Исключать нули**.

5. Можно использовать поле **Уровень**, чтобы указать, насколько подробными должны быть строки контроля затрат относительно функциональных местоположений. 

    Например, если вставить число "1" в это поле, и имеется структура функциональных местоположений с несколькими уровнями, все строки контроля затрат на неисправности активов для функционального местоположения будут показаны на верхнем уровне, и поэтому часы по строке могут быть добавлены из функциональных местоположений, расположенных на более низком уровне. 
    
    Если вставить число "0" в поле **Уровень**, будет выведен подробный результат, отображающий все строки контроля затрат на неисправности активов на всех уровнях функциональных местоположений, к которым они относятся.

6. Если требуется ограничить поиск, можно выбрать отдельные активы, даты сбоя и причины неисправности на экспресс-вкладке **Записи для добавления**.

7. Нажмите **ОК**, чтобы начать расчет.

8. Щелкните кнопки **Группировать по...**, чтобы отобразить необходимый уровень детализации для расчета. Выбранные кнопки **Группировать по...** выделяются. Нажимайте кнопку, чтобы активировать или деактивировать ее.

## <a name="example"></a>Пример

В этом примере показан расчет контроля затрат на ошибки в активах.

- В поле **Исходный бюджет** отображаются бюджетные затраты из прогноза заказа на работу. 
- В поле **Фактические затраты** отображаются разнесенные затраты по заказам на работу. 
- В поле **Подтвержденные затраты** отображается общая сумма затрат, которые подтверждены компанией в связи с заказами на работу.

    ![Рисунок 1.](media/05-controlling-and-reporting.png)

Сведения о настройке неисправностей см. в статье [Управление неисправностями](../setup-for-work-orders/fault-management.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]