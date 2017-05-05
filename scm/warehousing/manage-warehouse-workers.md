---
title: "Управление работниками склада"
description: "В этой статье рассматривается использование Microsoft Dynamics AX для контроля и мониторинга работы, выполняемой сотрудниками на складах."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: b63ec70a7d02d23ccdc9fd295a65431ac6b012ba
ms.lasthandoff: 03/31/2017


---

# <a name="manage-warehouse-workers"></a>Управление работниками склада

[!include[banner](../includes/banner.md)]


В этой статье рассматривается использование Microsoft Dynamics AX для контроля и мониторинга работы, выполняемой сотрудниками на складах.

Если вы используете функциональность в модуле "Управление складом", все операции, выполняемые работниками склада, называются *работой*. Работа, такая как комплектация, перемещение и подсчет запасов в наличии регистрируется путем использования мобильных устройств. Прежде чем работник склада сможет выполнять работу, его необходимо связать с работником в модуле "Управление персоналом". С каждой учетной записью **работника** может быть связано несколько пользователей работы склада. Эти пользователи работы могут работать на разных складах и иметь разные уровни доступа к различным меню на мобильных устройствах. Пользователей работы склада можно рассматривать как несколько разных учетных записей для входа для одного работника. У каждого пользователя работы есть склад по умолчанию и конкретные workflow-процессы, представленные пунктами меню, доступными этому пользователю работы. 

Чтобы создать нового пользователя работы, на странице **Работники** на вкладке **Общее** в разделе **Склады** щелкните **Работник**. Вы должны указать код пользователя, имя пользователя, склад по умолчанию и имя меню. Это меню загружается, когда пользователь входит на портал мобильных устройств склада, и позволяет вам определить, к каким пунктам меню имеет доступ пользователь. 

В рамках настройки каждого пользователя работы можно также определить конкретные worklow-процессы. Например, можно использовать поле **Является супервизор по подсчету циклов**, чтобы указать, может пользователь обрабатывать корректировки расхождений подсчета циклов во время операции подсчета или эти корректировки должны сначала быть рассмотрены другим лицом.

## <a name="defining-labor-standards"></a>Определение трудовых стандартов
Страница **Трудовые стандарты** позволяет определить методы расчета, которые система использует для расчета предполагаемого времени, которое должно уходить на выполнение работы того или иного типа. Это определение может быть установлено на общем уровне или на конкретном уровне. Например, вы можете определить время, необходимое для обработки комплектации заказа на продажу по весу для конкретного определения единицы измерения при использовании конкретного процесса комплектации. В то же время вы можете записать время, основанное на другом методе расчета, для операции складирования скомплектованных запасов в наличии. 

Чтобы включить определенные вами трудовые стандарты, необходимо выбрать параметр **Разрешить трудовые стандарты** для каждого склада, где будут использовать стандарты труда.

## <a name="monitoring-and-controlling-warehouse-work"></a>Мониторинг и контроль работы склада
Страница **Вся работа** позволяет осуществлять мониторинг и корректировку всей запланированной, выполняющейся и завершенной работы. С этой страницы вы можете обновлять различные процессы, такие как назначение складской работы пользователям и приоритет работы. Также можно детализировать сведения, связанные с заголовком работы и строками работы, чтобы получить представление об ожидаемых или завершенных процессах работы. 

Если вы включили параметр **Стандарты труда**, вы можете видеть рассчитанное предполагаемое время выполнения работы. После этого, когда работа будет выполнена, для каждой операции работы также будет отображаться фактическое время. Таким образом, вы можете сравнить расчетное (предполагаемое) время с фактическим. 

Кроме того, вы можете использовать расчетное время в правилах для автоматического разбиения работы во время создания работы. Так вы можете балансировать нагрузку между работниками, исходя из предполагаемого времени выполнения задач. 

Анализ времени, затраченного на обработку элементов работы, может помочь повысить эффективность работы работников склада. Для такого анализа предусмотрены следующие отчеты:

-   **Труд по пользователям** — этот отчет показывает производительность работника, исходя из сравнения фактического времени с предполагаемым.
-   **Труд по типу проводки работы** — вы можете использовать этот отчет для изучения неэффективных моментов в в конкретных складских процессах. Предположим, вы заметили, что комплектация для заказов на перемещение на этой неделе занимает больше времени, чем на предыдущих неделях. Эту информацию можно использовать для дальнейшего изучения проблемы.




