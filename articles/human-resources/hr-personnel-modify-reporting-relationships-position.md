---
title: Изменение отношений подотчетности для должности
description: Ниже описан порядок изменения связи подотчетных отношений для сотрудника.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 78410347e7e6cf67f692c7e9193419ffd87e3057
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057100"
---
# <a name="modify-reporting-relationships-for-a-position"></a>Изменение отношений подотчетности для должности

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



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



[!INCLUDE[footer-include](../includes/footer-banner.md)]