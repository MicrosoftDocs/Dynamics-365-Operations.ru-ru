---
title: Параметры склада для обработки волн
description: В этой теме описывается, как настроить параметры склада для обработки волн. Обработку волн можно использовать, чтобы сгруппировать работу комплектации для нескольких заказов на выполнение работ в одну волну.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 77513185a3323a2e78f641d25b86b2896f9f7881
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838018"
---
# <a name="warehouse-parameters-for-wave-processing"></a>Параметры склада для обработки волн

[!include [banner](../includes/banner.md)]

В этой теме описывается, как настроить параметры склада для обработки волн. Обработку волн можно использовать, чтобы сгруппировать работу комплектации для нескольких заказов на выполнение работ в одну волну.

Для использования обработки волн на странице **Параметры управления складом** укажите следующее:

- Выполняется ли обработка волн с помощью пакетного задания.
- Выполняется ли сбор данных в файле журнала при обработке волн.

## <a name="set-up-warehouse-management-parameters-for-wave-processing"></a>Настройка параметров управления складом для обработки волн

Чтобы настроить параметры склада для обработки волн, выполните следующие действия.

1. Перейдите в раздел **Управление складом** \> **Настройка** \> **Параметры управления складом**.

1. На экспресс-вкладке **Обработка волны** выполните следующие настройки:

    - **Группа партий обработки волны** — выберите пакетную группу для использования при обработке волн с помощью пакетных заданий. Пакетная группа определяет сервер, на котором выполняются пакетные задания.
    - **Обрабатывать волны в партии** — выберите, следует ли включать волны для автоматической обработки пакетным заданием. Необходимо задать для этого параметра значение *Да*, чтобы использовать параллельную обработку. Пакетное задание можно настроить на странице **Обработка волн**. (См. также примечание в конце этого списка.)
    - **Создать журнал хода выполнения волны** — укажите, должна ли система создавать запись журнала каждый раз, когда начинается и заканчивается распределение для номенклатуры и ее аналитик. Этот журнал следует включать только в том случае, если это необходимо, например при первоначальном тестировании или для устранения неполадок. Дополнительные сведения см. в разделе [Распределение волны](wave-allocation-method.md).
    - **Создать журнал истории обработки волн** — выберите, нужно ли автоматически сохранять сведения о волне в файле журнала после обработки волны, включая параллельную обработку ожидающих распределений. Обычно это следует включать только в ходе устранения неполадок, поскольку это добавляет дополнительные накладные расходы. Для просмотра журнала перейдите в раздел **Управление складом \> Исходящие волны \> Журнал истории обработки волн**. Дополнительные сведения см. в разделе [Создание и обработка волны](wave-processing.md).
    - **Создать журнал истории контейнеризации** — выберите, следует ли автоматически сохранять сведения о контейнеризации для волны в файле журнала после обработки волны. Для просмотра журнала перейдите в раздел **Управление складом \> Упаковка и контейнеризация \> Истории контейнеризации**.
    - **Ожидание блокировки (мс)** — введите время (в миллисекундах), в течение которого на данном этапе распределения будет ожидаться системный ресурс, заблокированный на другом этапе распределения. По истечении этого времени волна не будет обрабатываться, и отобразится сообщение об ошибке.

1. На экспресс-вкладке **Запуск на склад** выполните следующие настройки:

    - **Ошибка при сбое пакета** — необходимо указать, следует ли выдавать ошибку при сбое пакетного задания выпуска на склад. Если это разрешено, сбойные задания будут завершаться со статусом *Ошибка*. Если это запрещено, сбойные задания будут завершаться со статусом *Завершено*.

> [!NOTE]
> В шаблоне волны, который используется для обработки волны, можно задать параметры автоматизации обработки волн. Если настроен график для пакетного задания, необходимо скоординировать время с настройками для автоматизации в шаблоне волны. Дополнительные сведения см. в разделе [Создание шаблона волны](wave-templates.md).
>
> Если используется *Управление транспортировкой* и *Расширенное управление складом*, можно указать, следует ли консолидировать грузы при обработке волны. Например, это полезно, когда одновременно можно отгрузить несколько небольших грузов. Для консолидации загрузок при обработке волны на вкладке **Загрузки** установите флажок **Консолидировать загрузки во время обработки волны**.</P>

## <a name="set-up-full-or-partial-reservation-for-production-waves"></a>Настройка полного или частичного резервирования для волн производства

Для заказов на продажу и заказов канбана необходимо зарезервировать запасы до выпуска заказа на склад. В противном случае номенклатуры или строки распределения нельзя обрабатывать в волне. Однако производственные заказы немного более гибкие. Для производственных заказов можно определить следующее.

- Разрешить выпуск производственных заказов на склад, хотя невозможно зарезервировать все материалы. При выборе этого параметра необходимо вручную повторить процесс выпуска на склад, когда станут доступны дополнительные материалы. Например, это полезно, если имеются материалы, которые необходимы для запуска производства, и можно подождать, пока станут доступны дополнительные материалы.
- Указать, чтобы все материалы резервировались перед выпуском заказа на склад.

Чтобы указать полное резервирование или разрешить частичное резервирование, выполните следующие действия.

1. Перейдите в раздел **Управление производством** \> **Настройка** \> **Параметры управления производством**.
1. На вкладке **Общие** в поле **Запуск на склад** выберите значение по умолчанию.