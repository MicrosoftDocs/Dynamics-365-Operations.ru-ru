---
title: Работа по упаковке для упаковки исходящих контейнеров и обработки отгрузок
description: В этой статье описывается тип заказа на работу "Упаковка", который управляет работой для упаковки контейнеров и поддерживает частичные отгрузки упакованных контейнеров, которые связаны с загрузками, в которых складируемые номенклатуры остаются неупакованными.
author: perlynne
ms.date: 7/13/2022
ms.topic: article
ms.search.form: WHSPackingWorkLocationSetup, WHSPack, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 34a7087df7e7768d0012ea4f534aa109654af8fa
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220594"
---
# <a name="packing-work-for-packing-outbound-containers-and-processing-shipments"></a>Работа по упаковке для упаковки исходящих контейнеров и обработки отгрузок

[!include [banner](../../includes/banner.md)]

В этой статье описывается тип заказа на работу *Упаковка*, который управляет работой для упаковки контейнеров и поддерживает частичные отгрузки упакованных контейнеров, которые связаны с загрузками, в которых складируемые номенклатуры остаются неупакованными. Работа по упаковке позволяет использовать функции [подтверждения и перемещения](confirm-and-transfer.md) для подтверждения исходящих отгрузок, связанных с контейнерами.

Работа по упаковке создается автоматически, когда запасы, имеющие отношение к работе с исходным документом, помещаются в местоположения с типом *Местонахождение упаковки*. Работа состоит из двух строк — одна для *Комплектации* и одна для *Размещения* — и автоматически выполняется как часть процесса закрытия/повторного открытия контейнера.

Дополнительные сведения о настройке и использовании процесса упаковки контейнеров см. в разделе [Упаковка контейнеров для отгрузки](packing-containers.md).

## <a name="turn-on-the-feature"></a>Включение функции

Если ваша система еще не содержит функций, описанных в этой статье, перейдите в [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) и включите следующие функции в следующем порядке: Обе функции являются частью модуля **Управление складом**.

1. *Подтвердить и перенести*
1. *Работа упаковки для упаковочных станций*

## <a name="set-up-a-location-for-packing-work"></a>Настройка местоположения для работы по упаковке

Для настройки местонахождений упаковки используется следующая процедура. Для каждого местоположения можно выбрать, будет ли система автоматически создавать работу по упаковке.

1. Перейдите в раздел **Управление складом \> Настройка \> Упаковка \> Настройка упаковочной станции**.
1. В области действий выберите **Создать**, чтобы добавить запись настройки станции упаковки.
1. В новой записи задайте следующие поля:

    - **Склад** — выберите или введите склад, где расположено местонахождение упаковки.
    - **Местонахождение** — введите или выберите значение местонахождение упаковки. Это местоположение должно быть назначено профилю местоположения, в котором используется тип местоположения, настроенный в качестве типа местоположения упаковки для вашей компании на странице **Параметры управления складом**. Дополнительные сведения см. в разделе [Упаковка контейнеров для отгрузки](packing-containers.md).
    - **Создать работу упаковки** — установите этот флажок, чтобы создавать работу по упаковке всякий раз, когда номенклатуры доставляются в местоположение упаковки. Работа будет содержать ссылки на соответствующие строки загрузки, чтобы можно было упаковать и отгрузить частичные загрузки.

## <a name="example-scenario"></a>Пример сценария

В этом примере демонстрируется обработка исходящего потока заказа на продажу путем упаковки контейнера и отгрузки частичной загрузки.

### <a name="make-sample-data-available"></a>Сделать образцы данных доступными

Для работы с этим сценарием с помощью образцов записей и значений, указанных здесь, необходимо использовать систему, в которой установлены стандартные [демонстрационные данные](../../fin-ops-core/fin-ops/get-started/demo-data.md). Дополнительно перед началом необходимо выбрать юридическое лицо **USMF**.

Этот сценарий можно также использовать в качестве руководства по использованию этой функции в производственной системе. Однако в этом случае необходимо подставить собственные значения для каждого из описанных здесь параметров.

### <a name="configure-packing-work-for-warehouse-packing-location"></a>Настройка работы упаковки для местонахождения упаковки склада

Чтобы начать работу, необходимо настроить рабочий процесс *Упаковка* для конкретного склада и местоположения.

1. Перейдите в раздел **Управление складом \> Настройка \> Упаковка \> Настройка упаковочной станции**.
1. В области действий выберите **Создать** для добавления новой записи настройки.
1. В новой записи установите следующие значения:

    - **Склад:** *62*
    - **Местонахождение:** *Упаковка*
    - **Создать работу упаковки:** *Да*

1. Закройте страницу **Настройка упаковочной станции**.

### <a name="create-a-load-template-that-allows-partial-shipping"></a>Создание шаблона загрузки, который допускает частичную отгрузку

Чтобы загрузка была доставляться по нескольким отгрузкам, необходимо связать ее с шаблоном загрузки, который позволяет выполнять частичную отгрузку. Чтобы создать необходимый шаблон, выполните следующие действия.

1. Перейдите в раздел **Управление складом \> Настройка \> Загрузка \> Шаблоны загрузки**.
1. В области действий выберите **Создать** для добавления новой записи настройки.
1. В новой записи установите следующие значения:

    - **Код шаблона загрузки:** *Частично*
    - **Разрешить разбиение загрузки во время подтверждения отгрузки:** *Да*

1. Закройте страницу **Шаблоны загрузки**.

Дополнительные сведения см. в разделе [Подтверждение и перемещение](Confirm-and-transfer.md).

### <a name="process-a-sales-order"></a>Обработка заказа на продажу

Выполните следующие действия, чтобы обработать заказ на продажу и частично отгрузите его.

1. Выполните [пример сценария](packing-containers.md#scenario), приведенный в разделе [Упаковка контейнеров для отгрузки](packing-containers.md). В этом сценарии создается заказ на продажу, в котором две единицы одной номенклатуры. Затем необходимо упаковать только одну единицу в контейнер и закрыть контейнер. Следует записать созданный код отгрузки, как описано в сценарии.
1. Перейдите в раздел **Управление складом \> Работа \> Все работы**.
1. В области фильтра установите флажок **Показать закрытую работу**. Затем введите код отгрузки в поле **Фильтр** и выберите фильтр, чтобы отфильтровать по значению **Код отгрузки**. Теперь вы должны увидеть три заголовка работ. Один из них относится к работе комплектации заказа на продажу и имеет статус *Закрыто*. Два остальных относятся к процессу упаковки: один связан с закрытым контейнером и имеет статус *Закрыто*, а другой — с неупакованной оставшейся номенклатурой и имеет статус *Открыто*.
1. Выберите значение **Код загрузки** для каждого из заголовков работ, чтобы открыть страницу **Сведения о загрузке** для загрузки.
1. Перейдите к представлению **Заголовок**.
1. На экспресс-вкладке **Общие** нажмите кнопку **Изменить** для поля **Код шаблона загрузки**. Затем выберите шаблон загрузки частичной отгрузки, который вы создали для этого сценария (*Частично*).
1. В области действий на вкладке **Отгрузка и получение** в группе **Подтверждение** выберите **Исходящая отгрузка**.
1. В диалоговом окне **Подтверждение отгрузки** выберите параметр **Разбить количество с созданием новой загрузки**.
1. Нажмите **ОК**.

Теперь вы отгрузили один контейнер, связанный с исходной загрузкой, и система создала новую загрузку для остальных номенклатур, которые должны быть упакованы в контейнеры.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
