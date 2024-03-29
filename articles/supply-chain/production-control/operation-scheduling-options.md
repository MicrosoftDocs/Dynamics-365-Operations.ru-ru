---
title: Параметры планирования операций
description: В этой статье описываются возможности для планирования операций. Планирование операций можно использовать, чтобы получить общую оценку производственного процесса по времени.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 198123
ms.assetid: d680d7be-da64-4132-89fe-ad2fa59afb77
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2f4d1e74855a0a8f73030c222c3f2fe27ce58a2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907271"
---
# <a name="operations-scheduling-options"></a>Параметры планирования операций

[!include [banner](../includes/banner.md)]

В этой статье описываются возможности для планирования операций. Планирование операций можно использовать, чтобы получить общую оценку производственного процесса по времени.

Планирование операций вычисляет следующую информацию для производственного заказа:

-   Даты начала и завершения устанавливается для производственного заказа и каждой операции.
-   Ресурсы назначены операциям.

Несколько параметров определяют, как рассчитываются планы производства. Эти параметры определяются на странице **Планирование операций**. Следующие сведения описывают параметры планирования.

## <a name="operations-scheduling"></a>Планирование операций
### <a name="scheduling-direction"></a>Направление планирования

Направление планирования является фундаментальным понятием для процесса планирования. Производство может планироваться вперед или назад от любой даты, в зависимости от требований расчета времени и планирования.

-   **Планирование от начальной даты** — можно запланировать начало производство как можно раньше. Производство может начаться сегодня, завтра или с любой другой конкретной даты в будущем. Начало производства намечается на самую раннюю доступную дату и далее производство планируется так, чтобы дата окончания была самой ранней из возможных.
-   **Планирование от конечной даты**— можно запланировать начало производство как можно позже. В основе расписания лежит дата, когда производство должно быть завершено, и отсчет производится назад от самой поздней доступной даты, так чтобы производство могло быть начато без нарушения конечного крайнего срока.

Имеются следующие варианты:

-   **Вперед от текущего дня** — планирование вперед от текущей даты. (Текущая дата является системной датой.)
-   **Вперед от спланированного начала** — планирование вперед от более ранней даты начала. Если ранее планирование не выполнялось, направление планирования будет вперед от текущей даты.
-   **Вперед от даты планирования** — планирование вперед от даты, указанной в поле **Дата планирования**. Если дата планирования не указана, направление планирования будет вперед от текущей даты.
-   **Назад от даты поставки** — планирование назад от даты поставки, указанной для производственного заказа. Если выбран этот вариант, но не указана дата поставки, дата поставки будет текущей датой.
-   **Назад от спланированного окончания** — планирование назад от предварительно рассчитанной даты окончания. Если предварительное планирование не было выполнено, датой окончания считается текущая дата.
-   **Назад от даты планирования** — планирование назад от даты, указанной в поле **Дата планирования**. Если дата планирования не указана, используется текущая дата. Планирование назад от даты планирования рассчитывается для производственного заказа при последнем расчете потребности. Если дата для производственного заказа не указана, используется текущая системная дата.
-   **Назад от даты фьючерса** — планирование назад от даты фьючерса, которая была рассчитана для производственного заказа при последнем расчете потребности. Если дата фьючерса для производственного заказа не указана, используется текущая системная дата.
-   **Как при последнем планировании** — при планировании операций и планировании заданий сохраняются выбранные направление планирования и дата. Поэтому можно выбрать этот вариант для последующего планирования. Если планирование для этого производственного заказа ранее не выполнялось, то оно будет вестись назад от текущей системной даты.
-   **Начиная с завтрашнего дня** — планирование начиная с текущей даты плюс один день.
-   **Вперед от предыдущего задания** — этот вариант функция относится только к планированию заданий. Если выбрать это направление планирования при планировании операций, для производственного заказа будет выполнено планирование вперед с текущей даты. При планировании заданий планирование выполняется для одного задания, а все остальные задания для данного производства планируются на основе этого задания.
-   **Назад от предыдущего задания** — этот вариант относится только к планированию заданий. Если выбрать это направление планирования при планировании операций, для производственного заказа будет выполнено планирование назад с текущей даты. При планировании заданий планирование выполняется для одного задания, а все остальные задания для данного производства планируются на основе этого задания.

### <a name="scheduling-date"></a>Дата планирования

Эта дата используется для направлений планирования **Вперед от даты планирования** и **Назад от даты планирования**. Планирование выполняется назад или вперед от этой даты. Дополнительные сведения см. в предыдущем разделе, "Направление планирования".

### <a name="recalculate-bom-levels"></a>Пересчитать уровни спецификации

Если выбран параметр **Пересчитать уровни спецификации**, выбранные уровни спецификаций (BOM) будут пересчитаны, чтобы гарантировать правильный заказ планирования.

## <a name="limitations"></a>Ограничения
### <a name="finite-capacity"></a>Ограничение по мощности

Планирование зависит от доступности ресурсов, необходимых для выполнения производства. Если имеющиеся мощности недостаточны, производственные заказы будет задержаны или даже остановлены. Если ограничение по мощности применяется к планированию операций, рассматриваются существующие резервирования мощностей ресурсов и эти мощности считаются недоступными. Производственный заказ планируется на основе доступности мощностей необходимых ресурсов. Планирование операций использует указанную последовательность операций для определения порядка операций в маршруте производства. При планировании операций резервируется мощность в группах ресурсов на основе времени операций, заданных в маршруте производства. Мощность группы ресурсов — это сумма доступной мощности по всем ресурсам в группах ресурсов.

### <a name="finite-material"></a>Ограничение по материалам

Планирование зависит также от доступности материалов, необходимых для производства. Недостаточное наличие компонентов также может привести к задержкам производства. Планирование также может основываться на использовании материалов. Просто укажите материалы, необходимые для производства, вместо материалов, которые не принципиально важны. Этот тип планирования известен как планирование с ограничением по материалам. При указании ограничения по материалам, производство планируется на основе того, имеются ли материалы в наличии. **Примечание.** При оптимизации как по мощности, так и по материалам, производство рассчитывается так, чтобы удовлетворять обоим ограничениям. Доступность мощностей и материалов учитывается и операции производственного заказа не могут быть запланированы для запуска, до тех пор пока мощности и материалы не будут доступны в одно и то же время и в необходимых количествах. Установите этот флажок, если материалы должны рассматриваться при планировании в качестве ограниченного ресурса. При наличии ограничений по материалам будет учитываться покрытие по материалам на соответствующее время. Иными словами, при планировании учитываются даты будущих поставок соответствующих номенклатур. При планировании резервируется сырье и разворачивается текущее производство. Если планирование выполняется несколько раз, развертывание и резервирование выполняются только при первом планировании. При внесении изменений в производственную спецификацию или маршрут в ходе следующего планирования выполняется развертывание. Для развертывания предполагается, что материалы потребуются в тот же день. Поскольку производство не планируется во время выполнения развертывания сводного графика, текущая дата используется в качестве наилучшей оценки времени, когда номенклатуры станут доступны. Затем при развертывании проверяется, доступны ли эти номенклатуры. Если номенклатуры доступны, производственные потребности могут быть удовлетворены. Если номенклатуры недоступны на текущую дату, то создается спланированный заказ с интервалом переноса отбора. Если для спланированного заказа задано автоматическое подтверждение, этот заказ подтверждается автоматически на покупку или производство. Статус производства автоматически изменится на статус, заданный в поле **Запрошенный производственный статус** диалогового окна **Группы покрытия**. Если этот флажок снят, материалы всегда считаются доступными. Поэтому при планировании не учитывается, имеются ли материалы в наличии на момент требования.

### <a name="finite-property"></a>Ограничение по свойствам

Установите этот флажок, если при планировании заданий необходимо учитывать требования к свойствам.

### <a name="keep-production-unit"></a>Сохранить производственное подразделение

Выберите, должен ли механизм планирования планировать только ресурсы, уже указанные в производственном подразделении.

### <a name="keep-warehouse-from-resource"></a>Сохранить склад из ресурса

Выберите, должен ли механизм планирования планировать только ресурсы, связанные с входным складом, который определен для ресурса.

## <a name="references"></a>Ссылки
### <a name="schedule-references"></a>Ссылки графика

Когда ссылки зависят от производственных заказов, они также называются вспомогательными производствами. Вспомогательные производства можно запланировать как часть планирования производственного заказа. Установите этот флажок, если планирование вспомогательных производств должно быть основано на графике основного производства. Для производной продукции планирование будет вестись вперед, а для базовой — назад по отношению к основной продукции. Ссылки производственного заказа можно просмотреть в поле **Уровень ссылки** на странице **Производственные заказы**.

### <a name="synchronize-references"></a>Синхронизировать ссылки

Можно синхронизировать ссылки с производственным заказом. Если выбран этот параметр, даты вспомогательных производств передвигаются и выравниваются при внесении изменений в график производственного заказа. Если производственный заказ имеет одно или несколько вспомогательных производств, их планирование вспомогательных производств желательно осуществлять вместе с планированием основного производства. В этом случае основное производство не может быть запущено, пока не завершены связанные с ним вспомогательные производства. Поэтому установите этот флажок, если планирование вспомогательных производств должно быть основано на времени начала и завершения выбранного производства. Этот флажок можно установить, только если флажок **Ссылки графика** также установлен.

## <a name="cancellation"></a>Отмена
### <a name="cancel-queue-time"></a>Отменить время ожидания

Установите этот флажок, чтобы исключить время ожидания из планирования.

### <a name="cancel-setup"></a>Отменить настройку

Установите этот флажок, чтобы исключить время настройки из планирования.

### <a name="cancel-process"></a>Отменить процесс

Установите этот флажок, чтобы исключить время выполнения из планирования.

### <a name="cancel-overlap"></a>Отменить перекрытие

Установите этот флажок, чтобы исключить время перекрытия из планирования.

### <a name="cancel-transport"></a>Отменить транспортировку

Установите этот флажок, чтобы исключить время транспортировки из планирования.

## <a name="set-default"></a>Установить по умолчанию
Можно сохранить текущие значения в качестве значений по умолчанию. Имеется две возможности:

-   Установить по умолчанию для меня
-   Установить по умолчанию для всех


## <a name="additional-resources"></a>Дополнительные ресурсы

[Планирование операций](operations-scheduling.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]