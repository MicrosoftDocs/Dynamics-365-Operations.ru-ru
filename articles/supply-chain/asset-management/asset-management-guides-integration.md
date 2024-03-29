---
title: Интеграция Dynamics 365 Supply Chain Management (управление активами) с Dynamics 365 Guides
description: В этой статье объясняется, как интегрировать модуль управления активами в Microsoft Dynamics 365 Supply Chain Management с Dynamics 365 Guides, чтобы пользоваться руководствами в смешанной реальности в повседневных процессах обслуживания.
author: johanhoffmann
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: d06978bcbd6205111384f5c7cefdf34fdbdbfbf5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875694"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a>Интеграция Dynamics 365 Supply Chain Management (управление активами) с Dynamics 365 Guides

[!include [banner](../includes/banner.md)]

Вы можете интегрировать модуль **Управление активами** в Microsoft Dynamics 365 Supply Chain Management с Dynamics 365 Guides, чтобы пользоваться руководствами в смешанной реальности в повседневных процессах обслуживания. Если руководство связано с заказом на работу по управлению активами, работник, открывающий контрольный список обслуживания в мобильном приложении Supply Chain Management (Dynamics 365), видит, что доступно руководство. Работник может также найти и открыть руководство в приложении Dynamics 365 Guides HoloLens.

## <a name="prerequisites"></a>Необходимые условия

Прежде чем прикрепить руководств к рабочим заказам на работу при управлении активами, необходимо выполнить следующие условия:

- [Настройте Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) версии 10.0.9 или более поздней.
- [Включите двойную запись для приложений Supply Chain Management](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).
- [Включите фокус-тестирование](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) для функции **MRGuidesFeature**. (Для производственных сред необходимо сначала отправить запрос в службу поддержки, чтобы ваш клиент был добавлен в группу фокус-тестирования.)
- [Включите следующие конфигурационные ключи](/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) на странице **Конфигурация лицензии**:

    - Управление активами \> Смешанная реальность управления активами
    - Смешанная реальность \> Руководство в смешанной реальности

- [Настройте Dynamics 365 Guides](/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) версии 200.0.0.96 или более поздней.

## <a name="use-dynamics-365-guides-with-asset-management"></a>Используйте Dynamics 365 Guides с управлением активами

Чтобы установить связь с руководством, используется строка контрольного списка обслуживания в модуле управления активами. Связь можно создать с помощью шаблона контрольного списка обслуживания, типа задания обслуживания или заказа на работу, так как все три объекта содержат строки контрольного списка обслуживания. Вы можете сэкономить время, используя шаблон, поскольку шаблон можно связать со всеми типами заданий обслуживания, в которых он используется. Например, руководство, связанное с типом задания обслуживания, автоматически связывается со всеми рабочими заказами, в которых указывается этот тип задания. С другой стороны, руководство, связанное непосредственно с заказом на работу, существует только для данного заказа на работу.

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a>Связывание руководства с шаблоном контрольного списка обслуживания

Чтобы связать руководство с шаблоном контрольного списка обслуживания, выполните следующие действия.

1. Создайте руководство с помощью приложений Dynamics 365 Guides для Windows и HoloLens. Информацию о том, как создать руководство, см. в следующих статьях:

    - [Создание руководства с помощью приложения для Windows](/dynamics365/mixed-reality/guides/pc-app-overview)
    - [Использование приложения HoloLens для размещения голограмм](/dynamics365/mixed-reality/guides/hololens-app-overview)

1. В Supply Chain Management [создайте шаблон контрольного списка обслуживания](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).
1. Свяжите руководство, созданное в строке контрольного списка обслуживания шаблона:

    1. На экспресс-вкладке **Строки контрольного списка обслуживания** выберите строку, которую необходимо связать с руководством.
    1. На экспресс-вкладке **Связанные руководства** выберите **Добавить руководство**.

        ![Связывание руководства со строкой контрольного списка обслуживания.](media/am-guides-integration-add-guide.png "Связывание руководства со строкой контрольного списка обслуживания")

    1. В поле **Имя** выберите руководство, а затем выберите **Сохранить**.

        ![Выберите руководство в поле "Имя".](media/am-guides-integration-select-guide.png "Выберите руководство в поле &quot;Имя&quot;")

1. Связывание шаблона контрольного списка обслуживания с типом задания:

    1. [Создайте тип задания обслуживания](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) или выберите существующий тип.
    1. В области действий выберите **Значения по умолчанию для типа заданий обслуживания**.

        ![Кнопка "Значения по умолчанию для типа заданий обслуживания".](media/am-guides-integration-job-defaults.png "Кнопка &quot;Значения по умолчанию для типа заданий обслуживания&quot;")

    1. Создайте строку, а затем выберите **Сохранить**.

        ![Создайте строку.](media/am-guides-integration-add-line.png "Создайте строку")

    1. В области действий выберите **Контрольный список обслуживания**.

        ![Кнопка "Контрольный список обслуживания".](media/am-guides-integration-maintenance-checklist.png "Кнопка &quot;Контрольный список обслуживания&quot;")

    1. На экспресс-вкладке **Строки контрольного списка обслуживания** добавьте строку, а затем измените значение в поле **Тип** на **Шаблон**.

        ![Изменение значения типа.](media/am-guides-integration-checklist-lines.png "Изменение значения типа")

    1. На экспресс-вкладке **Сведения по строке** в поле **Шаблон** выберите шаблон, с которым связано данное руководство, а затем выберите **Сохранить**.

        ![Выбор шаблона.](media/am-guides-integration-checklist-line-details.png "Выбор шаблона")

1. [Создайте заказ на работу](work-orders/manually-created-workorders.md#create-work-order), а затем выберите тип задания обслуживания, которое использует шаблон контрольного списка обслуживания, с которым связано руководство. Руководство будет автоматически связано с этим заказом на работу.

    ![Выберите тип задания обслуживания.](media/am-guides-integration-create-work-order.png "Выберите тип задания обслуживания")

1. Просмотр руководства, связанного с заказом на работу и работниками:

    1. Откройте [мобильную рабочую область управления активами](asset-management-mobile-workspace.md), чтобы увидеть заказ на работу.
    1. [Откройте контрольный список обслуживания](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) для заказа на работу.
    1. Выберите строку контрольного списка для просмотра связанного руководства.

        ![Руководство, связанное со строкой контрольного списка.](media/am-guides-integration-show-guide.png "Руководство, связанное со строкой контрольного списка")

    1. Откройте руководство в HoloLens.

        ![Откройте руководство в HoloLens.](media/am-guides-integration-hololens-select.png "Откройте руководство в HoloLens")

> [!NOTE]
> Можно также связать руководство непосредственно в контрольном списке обслуживания заказа на работу или в типе задания.

> [!IMPORTANT]
> Существует известная проблема, в которой при связывании шаблона контрольного списка обслуживания с типом задания обслуживания по умолчанию руководство, связанное с этим шаблоном, не появляется на экспресс-вкладке **Связанные руководства** на странице **Значения по умолчанию для типа заданий обслуживания**. Однако руководство появится там после применения этого типа заданий к заказу на работу на Экспресс-вкладке **Связанные руководства**.

## <a name="see-also"></a>См. также

- [Обзор двойной записи](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [Обзор управления активами](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]