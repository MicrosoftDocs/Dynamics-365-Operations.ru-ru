---
title: Учет учтенных записей журнала в субкниге
description: Эта процедура описывает, как выполнить журнализацию разнесенных записей в журнале.
author: aprilolson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e20229ca910aa0d7d820434c22edf5a27030bba5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175601"
---
# <a name="journalize-posted-journal-entries"></a>Учет учтенных записей журнала в субкниге

[!include [task guide banner](../../includes/task-guide-banner.md)]

Эта процедура описывает, как выполнить журнализацию разнесенных записей в журнале. В этой процедуре используется компания с демонстрационными данными USMF.

1. В области **Область переходов** выберите **Модули > Главная книга > Настройка главной книги > Параметры главной книги**.
2. В поле **Расширенный журнал ГК** можно задать значение "Да" или "Нет". Если "Да", выходные данные отчета будут другими.
3. Выберите, можно ли закрыть период, если процесс журнализации не был запущен. Если для этого параметра задано значение "Да", период нельзя закрыть до тех пор, пока не будет завершен процесс журнализации за этот период.  
4. Закройте страницу.
5. В **области переходов** выберите **Модули > Главная книга > Периодические задачи > Журнализация**.
6. Щелкните **Фильтр**.
7. Выделите строку с критериями фильтра, которые вы хотите указать.
8. В поле **Критерии** введите или выберите критерий фильтра.
9. Чтобы закрыть страницу фильтра, нажмите кнопку **OK**.
10. Щелкните **ОК**, чтобы начать процесс журнализации. Отчет будет создан после завершения процесса.  
