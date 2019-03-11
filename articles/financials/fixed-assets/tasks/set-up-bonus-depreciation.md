---
title: Настройка амортизационной премии
description: В этой процедуре показано, как создать амортизационную премию и связать ее с моделью стоимости ОС.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6bbd6b78d05fcc9d95f6e6409db2619a210ad760
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "339219"
---
# <a name="set-up-bonus-depreciation"></a>Настройка амортизационной премии

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

