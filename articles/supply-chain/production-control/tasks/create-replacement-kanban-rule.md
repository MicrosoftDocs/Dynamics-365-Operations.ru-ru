---
title: Создание правила канбана замены
description: Эта процедура рассматривает замену существующего правила канбана на новое правило канбана на конкретную дату.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5aebd88dee9621d2c85af3a4fb5bf76ae8e6b80
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828954"
---
# <a name="create-a-replacement-kanban-rule"></a>Создание правила канбана замены

[!include [banner](../../includes/banner.md)]

Эта процедура рассматривает замену существующего правила канбана на новое правило канбана на конкретную дату. Это полезно, когда необходимо скоординировать и запланировать изменения в производственном потоке или правилах пополнения. В качестве компании с демонстрационными данными для создания процедуры используется USMF. Эта процедура предназначена для инженер-технолога или менеджера потока создания ценности, так как он подготавливает производство измененного производственного потока или нового правила пополнения. Эта задача заменяет правило канбана 000022 на новое правило и увеличивает максимальное количество с 48 до 100 для нового правила.


## <a name="select-a-kanban-rule-to-replace"></a>Выбор правила канбана для замены
1. Перейти к правилам канбана.
2. В списке найдите и выберите требуемую запись.
    * Выберите правило канбана 000022.  

## <a name="create-a-replacement-kanban-rule"></a>Создание правила канбана замены
1. Щелкните "Заменить правило канбана".
2. В поле "Действует с" введите дату и время.
    * Выберите дату в будущем, например одна неделя, начиная с сегодняшнего дня. Это дата и время, когда новое правило канбана станет активным и заменит старое правило канбана.  
    * Если правило канбана изменяет путь в производственном потоке, можно выбрать другое мероприятие.  В этой процедуре мероприятие не изменяется.  
3. Нажмите кнопку "OК".
    * Обратите внимание, что новое правило канбана создается для замены правила канбана 000022.  
    * Дата вступления в силу настраивается в соответствии с датой, выбранной при замене правила канбана.  
4. В списке найдите и выберите требуемую запись.
    * Выберите замененное правило канбана 000022.  
    * Обратите внимание, что дата замененного правила канбана совпадает с датой вступления в силу, поскольку это дата окончание его срока действия.  
5. В списке выберите строку 1.
    * Выберите новое правило канбана вверху списка. Это правило канбана с самым большим номером правила канбана.  
6. В списке перейдите по ссылке в выбранной строке.
    * Щелкните номер правила канбана, чтобы открыть правило канбана.  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a>Изменение максимального количества для заменяющего правила канбана
1. Установите для параметра "Максимальное количество" значение "100".
    * Разверните экспресс-вкладку "Количества", чтобы просмотреть поле "Максимальное количество". Изменение максимального количества на 100 позволит обрабатывать до 100 канбанов.    Это последний этап в этой задаче.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]