---
title: Настройка налоговых кодов
description: В этом разделе описывается, как настроить налоговые коды в Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45a4a7a20b20961d707e43b35d61c10a08c74943
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185988"
---
# <a name="set-up-sales-tax-codes"></a>Настройка налоговых кодов

[!include [task guide banner](../../includes/task-guide-banner.md)]

В этом разделе описывается, как настроить налоговые коды. Налоговые коды создаются для каждого косвенного налога или пошлины, которые юридическое лицо должно рассчитывать, собирать и платить налоговым органам.

В этой задаче используется демонстрационная компания USMF.

1. Перейдите к **Область перехода > Налог > Косвенные налоги > Налог > Налоговые коды**.
2. Выберите **Создать**.
3. В поле **Налоговый код** введите значение.
4. В поле **Имя** введите значение.
5. Выберите **Период сопоставления**, открыв раскрывающийся список, чтобы указать, в какие налоговые органы и через какие интервалы времени следует отправлять налоговые отчеты и выплачивать налоги.
6. Выберите **Группу разноски ГК**, чтобы указать счета ГК для разноски налога в главную книгу.
7. Разверните экспресс-вкладку **Расчет**. Это включает в себя несколько полей, с помощью которых можно управлять способом расчета сумм налогов. Заполните эти поля по мере необходимости.  
8. На **Панели операций** в верхней части интерфейса выберите **Налоговый код**.
9. Выберите **Значения**.
10. Введите значение для этого налогового кода в столбце **значение**.
    - На экспресс-вкладке **Расчет** в поле «Источник», если выбран параметр «Сумма на единицу», значение будет умножаться на количество в проводке для расчета суммы налога.  Если налоговый код не основан на единице, значение выражается в процентах, которые применяются к источнику для данного налогового кода для расчета суммы налога.     
11. Нажмите **Сохранить**.
12. Закройте страницу.
13. Нажмите **Сохранить**.
