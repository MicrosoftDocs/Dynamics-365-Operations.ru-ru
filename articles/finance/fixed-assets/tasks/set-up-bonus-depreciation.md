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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91243a4cee44410a221902990d31a10f1805eb08
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447122"
---
# <a name="set-up-bonus-depreciation"></a>Настройка амортизационной премии

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]