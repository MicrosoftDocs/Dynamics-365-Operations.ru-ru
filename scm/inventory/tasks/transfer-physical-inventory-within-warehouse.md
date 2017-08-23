--- 
title: "Перемещение физических запасов в пределах склада"
description: "Эта процедура описывает процесс создания и разноски журнала перемещения запасов для регистрации перемещения номенклатуры из одного местонахождения на складе в другое."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: fedb209ab111ed1fb6281fda2f4dea345e0905ef
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Перемещение физических запасов в пределах склада

[!include[task guide banner](../../includes/task-guide-banner.md)]

Эта процедура описывает процесс создания и разноски журнала перемещения запасов для регистрации перемещения номенклатуры из одного местонахождения на складе в другое. Необходимо настроить наименование журнала запасов для перемещения запасов перед началом этой процедуры. Можно выполнить эту процедуру с помощью демонстрационных данных компании USMF, используя указанные значения из примеров, или можно использовать собственные данные, если настроены продукты и местонахождения. Эти задачи обычно выполняются работником склада.


## <a name="create-an-inventory-transfer-journal"></a>Создание журнала перемещения запасов
1. Перейдите к "Перемещение".
2. Щелкните "Создать".
3. В поле "Имя" введите или выберите значение.
4. Нажмите кнопку "OК".
    * Есть параметр для указания аналитик "От" и "До" для каждой строки журнала. Это необходимо для этого типа журнала. Можно перенести номенклатуры в местонахождения, используя различные правила. В этом примере мы перенесем номенклатуру в пределах одного склада из местонахождения, контролируемого номерными знаком, в местонахождение, не контролируемое номерным знаком.   

## <a name="create-journal-lines"></a>Создать строки журнала
1. Щелкните "Создать".
2. В поле "Код номенклатуры" введите или выберите значение.
    * При использовании USMF можно выбрать "A0001".  
3. В поле "С сайта" введите или выберите значение.
    * При использовании USMF можно выбрать "2".  
4. В поле "На сайт" введите или выберите значение.
    * При использовании USMF можно выбрать "2".  
5. В поле "Со склада" введите или выберите значение.
    * При использовании USMF можно выбрать "24".  
6. В поле "На склад" введите или выберите значение.
    * При использовании USMF можно выбрать "24".  
7. В поле "Из местонахождения" введите или выберите значение.
    * При использовании USMF можно выбрать "FL-001".  
8. В поле "В местонахождения" введите или выберите значение.
    * При использовании USMF можно выбрать "BULK-001".  
9. В поле "Количество" введите число.
10. Перейдите на вкладку "Складские аналитики".
11. В поле "Номерной знак" введите или выберите значение.
    * При использовании USMF можно выбрать "24".  
12. Нажмите кнопку "Сохранить".

## <a name="post-the-inventory-transfer-journal"></a>Разноска журнала перемещения запасов
1. Щелкните "Разнести".
2. Нажмите кнопку "OК".

## <a name="view-inventory-transactions"></a>Просмотр складских проводок
1. Щелкните запасы.
2. Щелкните "Проводки".
    * Здесь можно просмотреть проводки, созданные при разноске журнала.  

