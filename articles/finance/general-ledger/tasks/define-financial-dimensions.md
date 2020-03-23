---
title: Определение финансовых аналитик
description: В этом руководстве показано добавление финансовой аналитики на основе объекта и пользовательской финансовой аналитики.
author: aprilolson
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb2dc5df96198f3c9f68fcac70b2e5dcbe8c8832
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175603"
---
# <a name="define-financial-dimensions"></a>Определение финансовых аналитик

[!include [task guide banner](../../includes/task-guide-banner.md)]

В этом руководстве показано добавление финансовой аналитики на основе объекта и пользовательской финансовой аналитики.  В данном руководстве используется демонстрационная компания USMF.


## <a name="create-an-entity-backed-financial-dimension"></a>Создание финансовой аналитики с основой на объекте
1. Перейдите в раздел **Область переходов > Модули > Главная книга > План счетов > Аналитики > Финансовые аналитики**.
2. Нажмите кнопку **Создать**.
3. В поле формы **Значения пользователя** выберите определенный системой объект, на котором будет основана финансовая аналитика. 
4. В поле **Наименование аналитики** введите значение для описания финансовой аналитики. Имя может отличаться от заданного системой объекта, но не может содержать пробелы или специальные символы.
5. Нажмите кнопку **Активировать**. При активации финансовой аналитики обновляется таблица с именем финансовой аналитики и удаляются удаленные аналитики. Можно ввести значения аналитики перед активацией финансовой аналитики, но финансовую аналитику нельзя использовать, пока она не активирована.  
6. Нажмите **Закрыть** в сообщении активации.
7. Нажмите кнопку **Активировать**. Активацию аналитики можно запланировать для пакетного выполнения в определенные дату и время.  
8. В области **Панель операций** щелкните **Значения аналитик**. Некоторые значения аналитики учитывают специфику компании. Можно проверить, учитывают ли они специфику компании, если название компании отображается в списке значений аналитики.  

## <a name="create-a-custom-financial-dimension"></a>Создание пользовательской финансовой аналитики
1. Закройте страницу.
2. Нажмите кнопку **Создать**.
3. В поле **Использовать значения из** выберите **Настраиваемая аналитика**.
4. В поле **Наименование аналитики** введите значение для описания финансовой аналитики.
    - Имя не может содержать пробелы и специальные символы.  
    - Можно также указать маску формата для ограничения объема и типа сведений, которые можно указать для значений аналитик.   
    - Можно ввести символы, которые останутся одинаковыми для каждого значения аналитики, такие как буквы или дефис. Можно также ввести знак номера (#) и амперсанда (&) как местозаполнители для букв и цифр, которые изменятся каждый раз при создании значения аналитики. Используйте знак решетки (#) как заполнитель для номера и амперсанд (&) как заполнитель для букв.  Пример: чтобы ограничить значение аналитики до букв CC, дефиса и трех цифр, введите CC-### как маску формата.  
5. Нажмите кнопку **Активировать**. При активации финансовой аналитики обновляется таблица с именем финансовой аналитики и удаляются удаленные аналитики. Можно ввести значения аналитики перед активацией финансовой аналитики, но финансовую аналитику нельзя использовать, пока она не активирована.     
6. Нажмите кнопку **Активировать**. Активацию аналитики можно запланировать для пакетного выполнения в определенные дату и время.      
7. В области **Панель операций** щелкните **Значения аналитик**.
8. Нажмите кнопку **Создать**.
9. В поле **Значение аналитики** введите наименование для своего значения финансовой аналитики.
10. В поле **Описание** введите описание, которое описывает значение финансовой аналитики.
