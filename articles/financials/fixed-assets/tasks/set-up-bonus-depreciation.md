--- 
title: "Настройка амортизационной премии"
description: "В этой процедуре показано, как создать амортизационную премию и связать ее с моделью стоимости ОС."
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7e6ebb13084626b477b6e0b24acdc09e2c0d3d6d
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-bonus-depreciation"></a>Настройка амортизационной премии

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

В этой процедуре показано, как создать амортизационную премию и связать ее с моделью стоимости ОС. В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.


## <a name="create-a-special-depreciation-allowance"></a>Создание амортизационной премии
1. Перейдите в раздел "Основные средства" > "Настройка" > "Амортизационная премия".
2. Щелкните "Создать".
3. В поле "Амортизационная премия" введите значение.
4. В поле "Описание" введите значение.
5. В поле "Процент" введите число.
    * Если процент не указан, настройте сумму.  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a>Связь амортизационной премии с журналом группы основных средств
1. Перейдите в раздел "Основные средства" > "Настройка" > "Группы ОС".
2. В списке выберите группу основных средств, связанную с амортизационной премией.
3. Нажмите "Книги".
4. В списке выберите книгу, связанную с амортизационной премией.
5. Щелкните "Амортизационная премия".
6. Щелкните "Создать".
7. В поле "Амортизационная премия" введите или выберите значение.
    * Значения по умолчанию "Процент" и "Сумма" берутся из настройки амортизационной премии.  
8. В поле "Приоритет" введите число.


