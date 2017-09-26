--- 
title: "Ведение спецификации для модели конфигурации продукта"
description: "Выполнение этой процедуры требует существующей модели конфигурации продукта."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 645d748235935ae67867295a87a84a6539710ab0
ms.contentlocale: ru-ru
ms.lasthandoff: 07/28/2017

---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Ведение спецификации для модели конфигурации продукта

[!include[task guide banner](../../includes/task-guide-banner.md)]

Выполнение этой процедуры требует существующей модели конфигурации продукта. Модель динамика класса Hi-End в демонстрационной компании USMF используется для создания этой процедуры.


## <a name="add-a-bom-line"></a>Добавление строки спецификации
1. Щелкните "Определение модели вариантов продукта".
2. Щелкните "Модели конфигурации продукта".
3. В списке найдите и выберите требуемую запись.
    * Выберите динамик класса Hi--End для этой процедуры.  
4. В списке перейдите по ссылке в выбранной строке.
5. Развернуть раздел "Строки спецификации".
6. Нажмите кнопку Добавить.
7. В поле "Имя" введите значение.
8. В поле "Описание" введите значение.
9. Нажмите кнопку "Сохранить".

## <a name="add-bom-line-details"></a>Добавление сведений о строке спецификации
1. Щелкните "Сведения о строке спецификации".
2. В поле "Код номенклатуры" введите или выберите значение.
    * Например, можно выбрать номенклатуру M0055.  
    * Для каждого свойства строки спецификации можно выбрать, имеет ли оно фиксированное значение или сопоставляется с атрибутом.  
3. Установите флажок "Задать".
4. Выберите значение "Да" в поле "Расчет".
    * Настройка свойства расчета как "Да" гарантирует, что строка спецификации включается в расчет затрат.  
5. Перейдите на вкладку "Настройка".
6. Установите флажок "Задать".
7. В поле "Количество" введите число.
    * Поле количества определяет количество номенклатуры, которое будет включено в спецификацию. Это могло быть очевидным кандидатом для сопоставления атрибута.  
8. Щелкните вкладку "Аналитика".
    * Проверьте наличие активных аналитик продукта, и поэтому необходимо назначить значение или атрибут.  
9. Нажмите кнопку "OК".

