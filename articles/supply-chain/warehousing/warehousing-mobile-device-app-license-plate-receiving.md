---
title: Получение грузоместа через складское мобильное приложение
description: В этой теме объясняется, как настроить складское мобильное приложение для поддержки использования процесса получения грузоместа для получения физических запасов.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 98cd608edea1d5365d0d3532244f1fcdb6293d3c
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261370"
---
# <a name="license-plate-receiving-via-the-warehousing-mobile-app"></a>Получение грузоместа через складское мобильное приложение

В этой теме объясняется, как настроить складское мобильное приложение, чтобы оно поддерживало использование процесса получения грузоместа для получения физических запасов.

Можно использовать эту функцию для быстрой регистрации прихода входящих запасов, которые относятся к предварительному уведомлению об отгрузке (ASN). Система автоматически создает ASN, когда процессы управления складом используются для отгрузки заказа на перемещение. Для процесса заказа на покупку ASN может быть записано вручную, либо оно может быть автоматически импортировано с помощью входящего процесса информационного объекта ASN.

Данные ASN связаны с загрузками и отгрузками через *упаковочные структуры*, где палеты (родительские грузоместа) могут содержать ящики (вложенные грузоместа).

> [!NOTE]
> Для уменьшения количества складских проводок при использовании структур упаковки, для которых используются вложенные грузоместа, система записывает физические запасы в наличии на родительском грузоместе. Для запуска перемещения физических запасов в наличии с родительского грузоместа во вложенные грузоместа, основанного на данных о структуре упаковки, на мобильном устройстве должен содержаться пункт меню, основанный на процесса создания работы *Упаковывать по вложенным грузоместам*.

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a>Отображение или пропуск страницы сводки получения

Можно использовать функцию *Управление отображением страницы сводки получения на мобильном устройстве*, чтобы воспользоваться преимуществом дополнительного подробного потока приложения склада в рамках процесса получения грузомест.

Прежде чем использовать эту функцию, она должна быть включена в системе. Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения. В рабочей области **Управление функциями** эта функция перечисляется следующими способами:

- **Модуль:** *Управление складом*
- **Имя функции:** *Управление отображением страницы сводки получения на мобильном устройстве*

Если эта функция включена, пункты меню мобильного устройства для получения грузомест или получения и размещения грузомест необходимо задать параметр **Отображать страницу сводки получения**. Эта настройка имеет следующие параметры:

- **Отображать подробную сводку** — во время получения грузоместа работники увидят дополнительную страницу, которая показывает полные сведения ASN.
- **Пропустить сводку** — сотрудники не будут видеть полные сведения ASN. Работники склада не смогут задавать код метода обработки или добавлять исключения в ходе процесса приемки.

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Блокировать использование грузомест, отправленных по заказам на перемещение, на складах, отличных от склада назначения.

Процесс получения грузомест не может использоваться, если ASN содержит идентификатор грузоместа, уже существующий и имеющий данные о физическом наличии в местоположении склада, отличном от местоположения склада, где выполняется регистрация этого грузоместа.

Для сценариев заказов на перемещение, когда транзитный склад не отслеживает грузоместа (и, таким образом, также не отслеживает физические запасы в наличии для каждого грузоместа), можно использовать функцию *Блокировать использование грузомест, отправленных по заказам на перемещение, на складах, отличных от склада назначения*, чтобы предотвратить физические обновления запасов в наличии для грузомест в процессе транзита.

Прежде чем использовать эту функцию, она должна быть включена в системе. Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения. В рабочей области **Управление функциями** эта функция перечисляется следующими способами:

- **Модуль:** *Управление складом*
- **Имя функции:** *Блокировать использование грузомест, отправленных по заказам на перемещение, на складах, отличных от склада назначения*

Чтобы управлять функциональностью, когда эта функция доступна, выполните следующие действия.

1. Перейдите в раздел **Управление складом \> Настройка \> Параметры управления складом**.
1. На вкладке **Общие** на экспресс-вкладке **Грузоместа** задайте в поле **Политика грузомест на транзитном складе** одно из следующих значений:

    - **Разрешить повторное использование неотслеживаемых грузомест** — система работает так же, как и при недоступности функции *Блокировать использование грузомест, отправленных по заказам на перемещение, на складах, отличных от склада назначения*. Это значение является значением по умолчанию при первой активации функции.
    - **Запретить повторное использование неотслеживаемых грузомест** — только обновления запасов в наличии, которые относятся к отгруженному грузоместу, будут разрешены на складе назначения до тех пор, пока не будет получен заказ на перемещение.

## <a name="more-information"></a>Дополнительные сведения

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

Дополнительные сведения о элементах меню для мобильных устройств см. в разделе [Настройка мобильных устройств для работы склада](configure-mobile-devices-warehouse.md).
