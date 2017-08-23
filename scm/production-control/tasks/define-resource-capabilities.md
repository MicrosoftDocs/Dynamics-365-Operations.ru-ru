--- 
title: "Определение возможностей ресурса"
description: "Возможности ресурса описывают, что могут делать операционные ресурсы."
author: sorenva
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 4a7d342eeb16fd76f2dde58151bfc7973de76e2d
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="define-resource-capabilities"></a>Определение возможностей ресурса

[!include[task guide banner](../../includes/task-guide-banner.md)]

Возможности ресурса описывают, что могут делать операционные ресурсы. Во время планирования требования каждого задания и операции сопоставляются с возможностями доступных ресурсов. Это руководство по задаче поможет создать способность ресурса и назначить ее ресурсу. В качестве компании с демонстрационными данными для создания этой задачи используется USMF.


## <a name="create-a-resource-capability"></a>Создание возможности ресурса
1. Перейдите в раздел "Возможности ресурса".
2. Нажмите Создать.
3. В поле "Возможность" введите код возможности ресурса.
    * Для данной операций используйте код возможности, чтобы указать, что ресурсы должны иметь эту возможность для выполнения операции.  
4. В поле "Описание" введите описание возможности.

## <a name="assign-capability-to-a-resource"></a>Назначение возможности ресурсу
1. Нажмите кнопку Добавить.
2. В поле "Ресурс" введите код ресурса.
    * Возможность ресурса можно назначить одному или нескольким ресурсам.  
3. В поле "Истечение срока" введите дату.
    * Это поле можно использовать для указания того, что ресурс имеет возможность только на ограниченное время.  
4. В поле "Приоритет" введите число.
    * При планировании заданий и операций можно указать, следует ли выбирать ресурсы по приоритету. Если выбрать этот параметр и если нескольких ресурсов могут выполнить задание либо операцию к запрашиваемой дате, будет выбран ресурс с наименьшим приоритетом по отношению к необходимой возможности.  
5. В поле "Уровень" введите число.
    * Если указать, что для задания или операции требуется определенная возможность, можно также указать минимальный необходимый уровень. Используйте уровень возможности для дифференциации ресурсов, которые могут выполнить одно задание, но различаются по скорости, сильным сторонам, размерам и т. д.  

