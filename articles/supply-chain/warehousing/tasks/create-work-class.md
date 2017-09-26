--- 
title: "Создание класса работ"
description: "В этой процедуре показано, как настроить класс работы."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 50b8ee1825391d7e5977f758628b559d006a334e
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-work-class"></a>Создание класса работ

[!include[task guide banner](../../includes/task-guide-banner.md)]

В этой процедуре показано, как настроить класс работы. Классы работы используются для определения и/или ограничения типа строк заказа на работу, которые работник склада может обрабатывать на мобильном устройстве. Строки, которые может обрабатывать работник склада, определяются по классам работы, соответствующим пунктам меню мобильного устройства, доступ к которым имеет работник, и классу работы, указанному в строках работы. Классы работы можно также использовать для проверки местонахождения размещения для строки заказа на работу. Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные. Эта процедура предназначена для менеджера склада.

1. Перейдите в раздел "Управление складом" > "Настройка" > "Работа" > "Классы работы".
2. Щелкните "Создать".
3. В поле "Код класса работы" введите значение.
4. В поле "Описание" введите значение.
5. В поле "Тип заказа на выполнение работ" выберите вариант.
6. Щелкните "Создать".
7. В поле "Тип местоположения" введите значение.
    * Если выбран тип местонахождения, это устанавливает ограничение на то, где могут быть размещены номенклатуры после их комплектации. Этот параметр используется, когда директива места хранения пытается разрешить местонахождение, или если работник склада вручную предоставляет местонахождение для пункта меню мобильного устройства.  
8. Закройте страницу.

