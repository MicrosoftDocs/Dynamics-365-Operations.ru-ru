---
title: Создание политики свертки затрат
description: Эта процедура показывает, как создать политику свертки затрат и создать правила для этой политики.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: facffeaf8d880bad01877b420197e29b6791ebbf
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187782"
---
# <a name="create-a-cost-rollup-policy"></a>Создание политики свертки затрат

[!include [task guide banner](../../includes/task-guide-banner.md)]

Эта процедура показывает, как создать политику свертки затрат и создать правила для этой политики. В качестве компании с демонстрационными данными для создания этой процедуры используется USP2.


## <a name="create-a-policy"></a>Создание политики
1. Перейдите в раздел "Учет затрат" > "Политики" > "Политики свертки затрат".
2. Щелкните "Создать".
3. В поле "Имя политики" введите значение.
4. В поле "Описание" введите значение.
5. В поле "Иерархия аналитик объектов затрат" введите или выберите значение.
    * Выберите "Cost rollup CC".  
6. В поле "Иерархия аналитик элементов затрат" введите или выберите значение.
    * Выберите "Cost rollup CC".  
7. Нажмите кнопку "Сохранить".

## <a name="create-rules-for-the-cost-rollup-policy"></a>Создание правил для политики свертки затрат
1. Щелкните "Создать".
2. В списке пометьте выбранную строку.
3. В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.
    * Вы6ерите "007".  
4. В поле "Узел иерархии аналитик элементов затрат" введите или выберите значение.
    * Выберите "Cost rollup CE".  
5. В поле "Элемент вторичных затрат" введите или выберите значение.
    * В этом примере сопоставьте элемент вторичных затрат CC-007 центру затрат.  
6. Щелкните "Создать".
7. В списке пометьте выбранную строку.
8. В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.
    * Вы6ерите "008".  
9. В поле "Узел иерархии аналитик элементов затрат" введите или выберите значение.
    * Выберите "Cost rollup CE".  
10. В поле "Элемент вторичных затрат" введите или выберите значение.
    * В этом примере сопоставьте элемент вторичных затрат CC-008 центру затрат.  
11. Щелкните "Создать".
12. В списке пометьте выбранную строку.
13. В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.
    * Вы6ерите "009".  
14. В поле "Узел иерархии аналитик элементов затрат" введите или выберите значение.
    * Выберите "Cost rollup CE".  
15. В поле "Элемент вторичных затрат" введите или выберите значение.
    * В этом примере сопоставьте элемент вторичных затрат CC-009 центру затрат.  
    * Продолжайте, пока все центры затрат не будут сопоставлены соответствующим им элементам вторичных затрат.  
16. Нажмите кнопку "Сохранить".
