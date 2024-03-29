---
title: Запросы и отчеты по опасным материалам
description: В этой статье объясняется, как работать с различными отчетами, относящимися к опасным материалам. Многие из этих отчетов требуются для сохранения соответствия различным нормативам по опасным материалам при отгрузке и хранении.
author: t-benebo
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 784361f4e715921890ecff784b62935988732464
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335176"
---
# <a name="hazardous-materials-inquiries-and-reports"></a>Запросы и отчеты по опасным материалам

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management предоставляет различные отчеты, которые относятся к опасным материалам. Многие из этих отчетов требуются для сохранения соответствия различным нормативам по опасным материалам при отгрузке и хранении.

Все эти отчеты, за исключением отчета **Опасные товары при смешанных перевозках**, используют режим доставки, определенный для отгрузки, чтобы найти нормативные правила, которое должны использоваться для печати текста отгрузки для номенклатур. Способ доставки связан с перевозчиком и службой перевозчика. Поэтому необходимо настроить перевозчика и службу перевозчика и связать их с режимом доставки. Способ доставки относится к нормативному регулированию опасных материалов.

На следующем рисунке показана последовательность действий, которые выполняются, когда система создает отчеты по опасным материалам.

![Последовательность действий для отчетов по опасным материалам.](media/hazmat-report-sequence.png "Последовательность действий для отчетов по опасным материалам")

## <a name="set-up-hazardous-materials-reporting"></a><a name="set-up"></a>Настройка отчетности по опасным материалам

Обычно, если отгружаются номенклатуры, содержащие опасные материалы, необходимо создать специальные отчеты, помогающие обеспечить безопасность и соответствие с нормативными правилами по опасному материалу. Чтобы настроить отчеты, выполните следующие действия.

1. Перейдите в раздел **Управление складом \> Настройка \> Параметры управления складом**.
2. Откройте вкладку **Отчеты**. На экспресс-вкладке **Параметр отчета по опасным материалам** настройте следующие поля.

    | Секция | Поле | описание |
    |---|---|---|
    | Опасные грузы при смешанных перевозках | Код нормативов | Выберите нормативные правила, которое должны использоваться при создании отчета **Опасные грузы при смешанных перевозках**. |
    | Ограничения по запасам опасных материалов | Код нормативов | Выберите нормативное правило, которое должно использоваться при оценке ограничений запасов. |
    | Перевозка грузов автомобильным транспортом | Продукт группы CMR | CMR означает "канцерогенные, мутагенные и репротоксические вещества". Установите для этого параметра значение **Да**, чтобы настроить систему для печати определенных предупреждений и сообщений, связанных с обработкой этих веществ. |
    | Перевозка грузов автомобильным транспортом | Описание группы опасных материалов | Введите текст конкретных предупреждений, связанных с CMR и перевозкой грузов автомобильным транспортом. Этот текст будет включен в отчет. |
    | Декларация грузоотправителей | Предупреждение | Введите текст сообщения с предупреждением, которое должно быть напечатано в форме декларация грузоотправителя (например, "Осторожно: опасные товары, огнеопасно"). |
    | Декларация грузоотправителей | Декларация нижнего колонтитула | Введите текст сообщения, которое должно быть напечатано внизу документа декларации отгрузки. |
    | Язык отчета по опасным товарам | Язык отчета по опасным товарам внутри страны | Выберите язык по умолчанию для отчетов по опасным материалам, которые связаны с внутренними отгрузками. |
    | Язык отчета по опасным товарам | Язык отчета по экспорту опасных товаров | Выберите язык по умолчанию для отчетов по опасным материалам, которые связаны с международными отгрузками. |

## <a name="hazardous-materials-report"></a>Отчет об опасных материалах

В отчете **Опасные материалы** отображается список всех номенклатур, которые были настроены и определены, чтобы в них были данные об опасных товарах. Этот отчет можно использовать для отслеживания и просмотра информации, которую необходимо вести. На странице отчета отображается ограниченный выбор полей из настройки опасных материалов. Однако его можно персонализировать, добавляя необходимые поля.

Для просмотра этого отчета перейдите на страницу **Управление сведениями о продукте \> Запросы и отчеты \> Документация по отгрузке опасных материалов \> Опасные материалы**.

## <a name="hazardous-material-stock-limit-report"></a><a name="stock-limit-report"></a>Отчет об ограничениях запасов опасных материалов

Отчет **Предел запасов опасных материалов** позволяет отслеживать уровни запасов опасных материалов в местоположениях склада, чтобы убедиться, что они остаются ниже определенных безопасных пределов. Эти ограничения поступают из ограничений, которые определены для каждого выпущенного продукта.

Для просмотра этого отчета перейдите на страницу **Управление сведениями о продукте \> Запросы и отчеты \> Документация по отгрузке материалов \> Ограничения по запасам опасных материалов**.

Дополнительные сведения о настройке пределов запасов для выпущенного продукта см. в разделе [Задание пределов запасов для опасных продуктов](hazmat-items.md#stock-limits).

Нормативные правила, используемые для пределов запасов, определяются на странице **Параметры управления складом**. Выберите **Управление складом \> Настройка \> Параметры управления складом**, затем на вкладке **Отчеты** в поле **Предел запасов опасных материалов** укажите код нормативного правила. Дополнительные сведения см. в разделе [Настройка отчетности по опасным материалам](#set-up) ранее в данной статье.

## <a name="verified-gross-mass-report"></a>Проверенный отчет по валовой массе

Отчет **Проверенная валовая масса** позволяет распечатать информацию о весе отгрузки.

Чтобы создать и распечатать этот отчет, перейдите в раздел **Управление складом \> Отгрузки \> Все отгрузки** и откройте соответствующую отгрузку. Затем в области действий на вкладке **Отгрузки** в группе **Документ по опасным материалам** выберите **Проверенная валовая масса**.

## <a name="multimodal-dangerous-goods-report"></a>Отчет об опасных грузах при смешанных перевозках

Отчет **Опасные грузы при смешанных перевозках** предоставляется для отгрузок, которые должны быть перемещены с помощью комбинации способов перевозки. Обычно он используется, когда отгрузка сначала перемещается автомобильным транспортом и далее по морю.

Чтобы создать и распечатать этот отчет, перейдите в раздел **Управление складом \> Отгрузки \> Все отгрузки** и откройте соответствующую отгрузку. Затем в области действий на вкладке **Отгрузки** в группе **Документ по опасным материалам** выберите **Опасные грузы с несколькими моделями**.

При создании этого отчета сведения сохраняются, что позволяет редактировать их и/или перепечатывать отчет, если необходимо. Чтобы изменить созданный отчет, перейдите к разделу **Управление складом \> Запросы и отчеты \> Документация по отгрузке опасных материалов \> Опасные грузы при смешанных перевозках** и найдите соответствующий отчет в списке. После завершения требуемого редактирования содержимого выберите **Печать** на панели операций для печати отчета.

## <a name="shippers-declaration-report"></a>Отчет о декларации грузоотправителей

Отчет **Декларация грузоотправителей** позволяет распечатать сведения, которые относятся к декларации о материалах, включенных в отгрузку.

Чтобы создать и распечатать этот отчет, перейдите в раздел **Управление складом \> Отгрузки \> Все отгрузки** и откройте соответствующую отгрузку. Затем в области действий на вкладке **Отгрузки** в группе **Документ по опасным материалам** выберите **Декларация грузоотправителей**.

## <a name="carriage-of-merchandise-by-road-report"></a>Отчет о перевозке грузов автомобильным транспортом

Отчет **Перевозка грузов автомобильным транспортом** напоминает транспортную накладную, но обычно используется для перевозок автомобильным транспортом в Европе по соглашению в соответствии с правилами международной перевозки опасных грузов автомобильным транспортом (ADR). В этом отчете используется печатный текст отгрузки для номенклатуры, если не задано поле **Описание группы опасных материалов** на странице **Параметры управления складом**.

Чтобы создать и распечатать этот отчет, перейдите в раздел **Управление складом \> Отгрузки \> Все отгрузки** и откройте соответствующую отгрузку. Затем в области действий на вкладке **Отгрузки** в группе **Документ по опасным материалам** выберите **Перевозка грузов автомобильным транспортом**.

При создании этого отчета сведения сохраняются, что позволяет редактировать их и/или перепечатывать отчет, если необходимо. Чтобы изменить созданный отчет, перейдите к разделу **Управление складом \> Запросы и отчеты \> Документация по отгрузке опасных материалов \> Перевозка грузов автомобильным транспортом** и найдите соответствующий отчет в списке. После завершения требуемого редактирования содержимого выберите **Печать** на панели операций для печати отчета.

## <a name="shipment-summary-report"></a>Сводный отчет об отгрузке

Отчет **Сводка по отгрузке** содержит информацию, которая суммируется по категории транспортировки, которая относится к выпущенным номенклатурам.

Чтобы создать и распечатать этот отчет, перейдите в раздел **Управление складом \> Отгрузки \> Все отгрузки** и откройте соответствующую отгрузку. Затем в области действий на вкладке **Отгрузки** в группе **Документ по опасным материалам** выберите **Сводка отгрузки**.

## <a name="bill-of-lading-report"></a>отчет по транспортной накладной

Когда для системы включен компонент опасных материалов, в отчет по **транспортной накладной** включается столбец **Опасные материалы**, который указывает, включает ли загрузка опасные материалы. Этот отчет доступен со страницы **Все загрузки**, как обычно.

## <a name="packing-list-report"></a>Отчет по отборочной накладной

Когда функция опасных материалов включена для системы, в отборочные накладные входят дополнительные сведения, имеющие отношение к печатному тексту отгрузки для номенклатуры. Этот отчет доступен со страницы **Все загрузки**, как обычно.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]