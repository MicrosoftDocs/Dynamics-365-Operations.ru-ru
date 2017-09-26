--- 
title: "Изменение отношений подотчетности для должности"
description: "Ниже описан порядок изменения связи подотчетных отношений для сотрудника."
author: ShielaSogge
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: aa74bfe5540df7be37ac79dfd48c0c1c510c694d
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="modify-reporting-relationships-for-a-position"></a>Изменение отношений подотчетности для должности

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ниже описан порядок изменения связи подотчетных отношений для сотрудника. Подотчетные отношения позволяют перенаправлять документы через workflow-процесс. Эта процедура также показывает, как назначать сотрудника в дополнительные иерархии. Например, сотрудник может быть частью проектной группы с неофициальным подотчетным отношением к супервизору проекта. Можно определить для должности дополнительные отношения подотчетности, чтобы учесть различные сценарии проекта или матрицы. В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.

1. Перейдите в раздел "Управление персоналом" > "Должности" > "Должности".
2. Используйте экспресс-фильтр для поиска записей. Например, отфильтруйте поле "Должность" по значению "000091".
3. В списке перейдите по ссылке в выбранной строке.
4. Разверните раздел "Отчитывается перед должностью".
5. Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.
6. В поле "Отчитывается перед" введите или выберите значение.
7. Щелкните "Создать".
8. Разверните раздел "Отношения".
9. Нажмите кнопку Добавить.
10. Установите флажок слева от сетки.
11. В поле "Имя иерархии" введите или выберите значение.
    * Пример: проект  
12. В поле "Отчитывается перед должностью" введите или выберите значение.  Пример: 000437
13. Нажмите кнопку "Сохранить".

