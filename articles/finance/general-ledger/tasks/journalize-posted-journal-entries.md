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
ms.openlocfilehash: f50ee568df492bcd811d2fefb1784bb55b50384b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447131"
---
# <a name="journalize-posted-journal-entries"></a>Учет учтенных записей журнала в субкниге

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]